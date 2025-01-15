# Add and Retrieve Information React App

This project provides a React-based interface with two main tabs:

1. **Add New Person**
   - Allows users to dynamically add rows to a table and input details.
   - Validates inputs and saves data to local storage.

2. **Retrieve Information**
   - Displays the saved data from local storage in a user-friendly format.

## Features

### Add New Person Tab
- **Dynamic Row Creation**: Add rows with empty input fields.
- **Automatic Age Calculation**: Calculate age based on the Date of Birth (DOB) input.
- **Local Storage Integration**: Save valid entries into local storage as an array of objects.
- **Delete Functionality**: Remove rows from the table and local storage.
- **Input Validation**:
  - Aadhar Number must be exactly 12 digits.
  - Mobile Number must be exactly 10 digits.

### Retrieve Information Tab
- Displays the data saved in local storage in a readable format.

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open the app in your browser:
   ```
   http://localhost:3000
   ```

## File Structure

- `src/components/AddPerson.js`: Component for the "Add New Person" tab.
- `src/components/RetrieveInformation.js`: Component for the "Retrieve Information" tab.
- `src/App.js`: Main component that renders the tabbed interface.
- `src/index.js`: Entry point of the application.

## Implementation Details

### AddPerson.js
- **Table Structure**: Each row contains the following columns:
  - Name
  - Date of Birth
  - Aadhar Number
  - Mobile Number
  - Age (auto-calculated)
  - Save and Delete buttons

- **Row Operations**:
  - **Save Button**: Validates inputs and stores the data in local storage.
  - **Delete Button**: Deletes unsaved rows or removes data from local storage and the table.

- **Validation Logic**:
  - Checks if all fields are filled.
  - Validates Aadhar and Mobile Number lengths.

### RetrieveInformation.js
- Fetches and displays data from local storage.

## Usage

1. Navigate to the "Add New Person" tab.
2. Click the "Add Row" button to add a new row.
3. Enter details into the fields and click "Save" to store the data.
4. Use the "Delete" button to remove rows.
5. Switch to the "Retrieve Information" tab to view saved data.

## Example Data Format in Local Storage

```json
[
  {
    "Name": "Joe",
    "Date of Birth": "22/12/1995",
    "Aadhar Number": "123456789023",
    "Mobile Number": "1234567890",
    "Age": "25"
  },
  {
    "Name": "John",
    "Date of Birth": "22/01/1991",
    "Aadhar Number": "364728901237",
    "Mobile Number": "1234567890",
    "Age": "30"
  }
]
```

## Notes
- Ensure to handle edge cases such as invalid input formats or duplicate entries.
- Use modern React features such as functional components and hooks.

## Future Enhancements
- Add sorting and filtering options to the "Retrieve Information" tab.
- Improve UI/UX with better styling and responsive design.
- Add search functionality to locate specific entries.

## License
This project is open-source and free to use. Feel free to contribute!
