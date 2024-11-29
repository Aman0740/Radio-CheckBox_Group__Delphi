# Radio-CheckBox_Group__Delphi

This Delphi code defines a form named `TFormRadioCheckBoxGroup` with various UI components for performing basic arithmetic operations (Addition, Subtraction, Multiplication, Division). Here's a brief explanation:
![img_20241129](https://github.com/user-attachments/assets/245a9122-cf1d-4ea1-976f-398079a56707)

### Components:
1. **`TEdit` (edtValue, edtValue2, edtTotal):**
   - `edtValue` and `edtValue2` accept two integer inputs from the user.
   - `edtTotal` displays the result of the operation selected in the `TRadioGroup`.

2. **`TMemo` (Memo1):**
   - Used to display the results of operations selected via checkboxes in `TCheckListBox`.

3. **`TCheckListBox` (CheckListBox1):**
   - Contains checkboxes to allow the user to select multiple operations (Addition, Subtraction, Multiplication, Division) to display in the memo.

4. **`TRadioGroup` (RadioGroup1):**
   - Contains radio buttons to allow the user to select a single arithmetic operation to compute and display in `edtTotal`.

5. **`TButton` (btnSubmit):**
   - Triggers the logic for calculations when clicked.

---

### Logic:
- **Event Handler: `btnSubmitClick`:**
  This procedure executes when the button `btnSubmit` is clicked.
  
  **1. Retrieve Input:**
  - Reads and converts the text values from `edtValue` and `edtValue2` to integers (`a` and `b`). If the conversion fails, it defaults to `0`.

  **2. Checkbox Operations (`CheckListBox1`):**
  - If a checkbox is checked, the corresponding operation is performed, and the result is added as a new line to `Memo1`.

  **3. Radio Group Operation (`RadioGroup1`):**
  - Executes a single arithmetic operation based on the selected radio button (`ItemIndex`).
  - If "Division" is selected and the second value (`b`) is zero, it shows an error message in `edtTotal`.

  **4. Display Result:**
  - The result of the radio button operation is displayed in `edtTotal`.

---

### Features:
- **Error Handling:**
  - Prevents division by zero for both checkboxes and radio buttons with appropriate error messages.
  
- **UI Interaction:**
  - Multiple operations via checkboxes (outputs to `Memo1`).
  - Single operation selection via radio buttons (outputs to `edtTotal`).

### Use Case:
This program is designed to perform basic arithmetic operations interactively, allowing users to compute results using either a single operation (radio group) or multiple operations (checkbox list).
