# 🧬 Automated Bioinformatics Pipeline for DNA/RNA Isolate Classification

A robust and modular **Bash Scripting** pipeline designed to automate the processing, verification, and backup of genomic sample information (Bacteria and Viruses) in alignment with NCBI BioSample standards.

---

## Key Features
* **Automated Processing:** Iterates through multiple sample files using a custom `for loop`.
* **Pattern Matching:** Utilizes `grep` with advanced regex flags (`-i`, `-q`) to accurately distinguish DNA samples from RNA and other microbial isolates.
* **Modular Operations (`case`):** Supports multiple execution modes (analyze, backup, all).
* **Robust Error Handling:** Implements systematic `Exit Codes` for strict debugging and pipeline integrity.
* **Data Streams & Logging:** Automatically generates structured reports (`pipeline_report.txt`) and comprehensive event logs (`pipeline.log`) with timestamps.
* **Automated Backup:** Safely isolates and duplicates raw sample data into a secure directory.

---

## 🛠️ Project Structure
text
Check_DNA_Isolate/
│
├── script.sh               # Main automated Bash pipeline script
├── pipeline_report.txt     # Generated classification report
├── pipeline.log            # Execution log with timestamps
└── backup/                 # Secure backup directory of sample files
## How to Run

    Clone the repository:
    Bash

    git clone [https://github.com/ahmed-mostafa-dotcom/Check_DNA_Isolates.git](https://github.com/ahmed-mostafa-dotcom/Check_DNA_Isolates.git)
    cd Check_DNA_Isolates

    Give execution permissions to the script:
    Bash

    chmod +x script.sh

    Run the pipeline:

        Run full pipeline (Backup + Analysis):
        Bash

        ./script.sh <folder_name> all

        Run analysis only:
        Bash

        ./script.sh <folder_name> analyze

        Run backup only:
        Bash

        ./script.sh <folder_name> backup

🔍 Exit Codes Reference

    0: Success (Pipeline completed without errors)

    1: Missing arguments error

    2: Target directory not found error

    3: Backup operation failure

    4: Invalid operation selected
