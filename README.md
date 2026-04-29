



# Invoice_Processing_Automation_Bot
Hybrid Multi-Format Invoice Extraction &amp; GSuite Automation🤖

A robust UiPath automation designed to process invoices from multiple sources (PDF & Excel), extract critical data points, and deliver a consolidated report via Gmail.
https://github.com/user-attachments/assets/935b9b08-ab51-4736-a65e-04d020bcb28c
## 🚀 Technical Architecture
The bot employs a **Decision-Logic Flow**:
1. **Source Identification**: Detects file extensions (.pdf vs .xlsx).
2. **Intelligent PDF Processing**: 
   - Attempts Native Text Extraction.
   - Fallback: If text is null, triggers **Tesseract OCR** for scanned documents.
3. **Data Pattern Matching**: Uses advanced **Regular Expressions (RegEx)** to parse Invoice Numbers, Dates, and Totals.
4. **Data Consolidation**: Aggregates all data into a master report.
5. **GSuite Integration**: OAuth2 Authentication and sends the final `Process_Invoice_report.xlsx` via Gmail.

## 🛠️ Tech Stack
- **RPA Tool**: UiPath Studio
- **OCR Engine**: Tesseract
- **Data Handling**: VB.NET, Datatables, RegEx
- **External APIs**: Google Workspace / GSuite (via UiPath.GSuite.Activities)

## 📂 Project Structure
- `Main.xaml`: Orchestrator and file routing.
- `Extract__Pdf.xaml`: Logic for text extraction and OCR fallback.
- `Extract_Excel.xaml`: Logic for reading structured workbook data.
