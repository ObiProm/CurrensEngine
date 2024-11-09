MessageBoxHandler Class
=======================

The `MessageBoxHandler` class provides functionality to display Windows API MessageBoxes with specified text, caption, icons, and buttons.

Namespace
---------
CurrensEngine

Public Enums
-------------
- **Icons**: Defines the available icon types that can be displayed in the MessageBox.
  - **None**: No icon.
  - **Error**: Error icon.
  - **Question**: Question icon.
  - **Warning**: Warning icon.
  - **Information**: Information icon.

- **Buttons**: Defines the available button configurations that can be used in the MessageBox.
  - **None**: No buttons.
  - **Ok**: OK button.
  - **OkCancel**: OK and Cancel buttons.
  - **YesNo**: Yes and No buttons.

Public Methods
--------------
- **static void Show(string text, string caption, Icons icon, Buttons button)**:
  Displays a MessageBox with specified text, caption, icon, and button configuration.

  **Parameters**:
  - **text** (string): The text to display in the MessageBox.
  - **caption** (string): The caption (title) of the MessageBox.
  - **icon** (Icons): The icon to display in the MessageBox.
  - **button** (Buttons): The button configuration for the MessageBox.

- **static void Show(string text, string caption)**:
  Displays a MessageBox with specified text and caption, using default icon and button configuration.

  **Parameters**:
  - **text** (string): The text to display in the MessageBox.
  - **caption** (string): The caption (title) of the MessageBox.

- **static void Show(string text)**:
  Displays a MessageBox with specified text, using default caption, icon, and button configuration.

  **Parameters**:
  - **text** (string): The text to display in the MessageBox.

Usage Example
-------------
.. code-block:: csharp

   MessageBoxHandler.Show("This is a message.", "Message Title", MessageBoxHandler.Icons.Information, MessageBoxHandler.Buttons.Ok);

Exceptions
----------
No specific exceptions are documented for this class as it relies on the Windows API.

.. note::

   This project is under active development.
