# Folder to Markdown

## Overview

This project is a Python application that generates a Markdown file documenting the structure and content of a specified directory. It uses the `tkinter` library for the graphical user interface (GUI) and `ttkbootstrap` for styling.

## Key Features

1. **Directory Structure to Markdown**:

   - The application scans a specified directory and generates a Markdown file that lists all the files and subdirectories in a hierarchical format.
   - Hidden directories and files (those starting with a dot) are excluded from the output.

2. **Docstring Extraction**:

   - The application extracts docstrings or initial comments from various file types (`.py`, `.js`, `.php`, `.css`, `.html`) and includes them in the Markdown file under a "Documentación de Archivos" section.

3. **Code Inclusion**:
   - The application includes the content of each file in the Markdown file within code blocks, with appropriate syntax highlighting based on the file extension.

## Main Components

- **GUI**:

  - The main window allows users to select the source directory and the output Markdown file.
  - Buttons are provided to initiate the process and display the status of the operation.

- **Functions**:
  - `filtrar_directorios(dirs)`: Filters out hidden directories.
  - `listar_estructura_markdown(ruta, archivo_salida)`: Generates the directory structure in Markdown format.
  - `extraer_docstring(file_path)`: Extracts docstrings or initial comments from files.
  - `agregar_docstrings_markdown(ruta, archivo_salida)`: Adds extracted docstrings to the Markdown file.
  - `agregar_codigo_markdown(ruta, archivo_salida)`: Adds the content of each file to the Markdown file within code blocks.
  - `procesar(carpeta, archivo_md, actualizar_label)`: Executes the entire process and updates the status label.
  - `iniciar_proceso(carpeta, archivo_md, actualizar_label)`: Starts the process in a separate thread to keep the UI responsive.

## Usage

1. **Select the Source Directory**:

   - Click the "Seleccionar Carpeta" button to choose the directory you want to document.

2. **Select the Output Markdown File**:

   - Click the "Seleccionar Archivo" button to specify the name and location of the output Markdown file.

3. **Start the Process**:
   - Click the "Iniciar Proceso" button to start generating the Markdown documentation.
   - The status label will update to show the progress and completion of the process.

## Example Output

The generated Markdown file will have sections for the directory structure, extracted docstrings, and the content of each file, formatted with appropriate syntax highlighting.

## Files

- `folder-to-markdown.py`: The main script containing the logic and GUI for the application.
- `LICENSE`: The MIT license file.
- `README.md`: A brief description of the project and usage instructions.
- `w.md`: An example output file generated by the application.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
