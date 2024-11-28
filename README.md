# Secret Santa Mailer 🎅

Welcome to the **Secret Santa Mailer**! This Python notebook simplifies organizing a Secret Santa event by randomly assigning gift recipients and sending personalized email notifications. Let's spread the holiday cheer! 🎄✨

## Table of Contents
- [Requirements](#requirements)
- [Setup](#setup)
- [Usage](#usage)
- [Potential Pitfalls](#potential-pitfalls)
- [License](#license)

## Requirements
- Python 3.x
- Required Python packages (listed in `requirements.txt`)

## Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/sachstimo/secret-santa-mailer.git
   cd secret-santa-mailer
   ```

2. **Install Dependencies**:
   Install the required Python packages using pip:
   ```bash
   pip install -r requirements.txt
   ```

3. **Prepare Your Data**:
   Create an Excel file (e.g., `Secret_Santa_Participants.xlsx`) with the following columns:
   - **Name**: Participant's name
   - **Email**: Participant's email address
   - **Preferences**: Gift preferences (optional)

4. **Configure SMTP Settings**:
   Open the notebook (`miba-santa-mailer.ipynb`) and update the SMTP settings with your email server details.

## Usage

1. **Load the Notebook**:
   Open the `miba-santa-mailer.ipynb` notebook in Jupyter Notebook or JupyterLab.

2. **Load Participants Data**:
   Update the `file_path` variable to point to your Excel file:
   ```python
   file_path = "Secret_Santa_Participants.xlsx"
   ```

3. **Assign Secret Santas**:
   Run the cell to assign Secret Santas and generate the assignments file (`SecretSanta_Assignments_SECRET.xlsx`).

4. **Send Test Email**:
   Send a test email to verify the SMTP configuration.

5. **Send Secret Santa Emails**:
   Uncomment and run the final cell to send personalized emails to all participants.
  ```python
   send_email("test sender", SENDER_EMAIL, "test recipient", "test preferences", test_mode=True)
   ```

## Potential Pitfalls
1. **SMTP Configuration**:
   - SMTP Configuration: Ensure your SMTP settings are correct. Some email providers require app-specific passwords or additional security settings.

2. **Excel File Format**:
   - Ensure the Excel file is correctly formatted with the required columns (`Name`, `Email`, `Preferences`).

3. **Email Sending Limits**:
   - Check your email provider's sending limits to avoid being flagged for spam or blocked.

4. **Data Privacy**:
   - Handle participant data securely.
   - Keep the assignments file (`SecretSanta_Assignments_SECRET.xlsx`) confidential.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

Enjoy organizing your Secret Santa event and have a Merry Christmas! 🎅🎁