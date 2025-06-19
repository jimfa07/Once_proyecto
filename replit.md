# Pollo Management System

## Overview

This is a Streamlit-based inventory and financial management system designed for poultry business operations. The application manages supplier transactions, deposits, debit notes, sales, and expenses with comprehensive reporting capabilities including PDF generation and data visualization.

## System Architecture

### Frontend Architecture
- **Framework**: Streamlit web application
- **UI Components**: Native Streamlit widgets for forms, tables, and charts
- **Visualization**: Matplotlib for chart generation
- **Styling**: Custom theme configuration with red primary color (#FF6B6B)

### Backend Architecture
- **Language**: Python 3.11
- **Data Processing**: Pandas for data manipulation and analysis
- **File Storage**: Pickle files for main system data, CSV files for sales/expenses
- **Report Generation**: ReportLab for PDF document creation

### Data Storage Solutions
- **Primary Data**: Pickle files stored in `/data` directory
  - `registro_data.pkl` - Main supplier transaction records
  - `registro_depositos.pkl` - Deposit records
  - `registro_notas_debito.pkl` - Debit note records
- **Secondary Data**: CSV files for sales and expenses
  - `ventas.csv` - Sales records
  - `gastos.csv` - Expense records

## Key Components

### Core Business Logic
- **Inventory Management**: Tracks poultry quantities, weights (kg), and pricing
- **Financial Tracking**: Manages accumulated balances starting from $44.64
- **Document Management**: Handles invoices, debit notes, and credit notes
- **Multi-Provider Support**: Manages transactions with multiple suppliers (LIRIS SA, Gallina 1, Monze Anzules, Medina)

### Data Processing
- **Unit Conversion**: Automatic conversion between pounds and kilograms (1 kg = 2.20462 lbs)
- **Price Calculations**: Automatic unit price and average calculations
- **Balance Tracking**: Real-time accumulated balance computation

### Reporting System
- **PDF Generation**: Professional reports with tables, charts, and formatted layouts
- **Data Visualization**: Matplotlib charts for trend analysis
- **Export Capabilities**: Data export functionality for external analysis

## Data Flow

1. **Input**: User enters transaction data through Streamlit forms
2. **Validation**: Data validation and unit conversions applied
3. **Storage**: Data persisted to pickle/CSV files in `/data` directory
4. **Processing**: Real-time calculations for balances and averages
5. **Output**: Data displayed in tables, charts, and PDF reports

## External Dependencies

### Core Libraries
- **Streamlit**: Web application framework
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Chart generation and visualization
- **ReportLab**: PDF document generation

### System Dependencies
- **Cairo**: Graphics rendering support
- **FFmpeg**: Media processing capabilities
- **Ghostscript**: PostScript/PDF processing
- **GTK3**: GUI toolkit support

## Deployment Strategy

### Platform
- **Target**: Replit autoscale deployment
- **Runtime**: Python 3.11 with Nix package management
- **Port**: Application runs on port 5000

### Configuration
- **Streamlit Server**: Headless mode, accessible on all interfaces
- **Workflow**: Parallel execution with automated startup
- **Dependencies**: Managed through `pyproject.toml` with UV lock file

### Environment Setup
- **Nix Channel**: stable-24_05 for reproducible builds
- **Data Persistence**: Local file system storage in `/data` directory
- **Auto-creation**: Data directory created automatically if missing

## User Preferences

Preferred communication style: Simple, everyday language.

## Changelog

Changelog:
- June 19, 2025. Initial setup
