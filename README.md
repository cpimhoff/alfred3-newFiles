# alfred3-newFiles
An Alfred 3 workflow which allows for the fast creation of new documents and folders.

## Usage
_New Files_ takes in the following parameters to create a new file:
- File Type (from defaults list or specify file extension)
- File Name
- Location (from defaults list or browse for folder)

For non-folders, you can then create the document with specific contents:
- No Contents (blank)
- Contents of Clipboard (text only)
- Type Contents in Alfred Window

## Configuration
_New Files_ supports modifying the behavior of the workflow in simple ways.

### Options
Certain options can be configured in the **Workflow Enviromental Variables**:

- **openNewFiles = 'default':** New files will automatically be opened in the default application after being created.
- **openNewFiles = 'none':** New files will not be automatically opened.
- **openNewFolders = 'finder':** New folders will automatically be opened in Finder.
- **openNewFolders = 'terminal':** New folders will automatically be opened in a new Terminal Window.
- **openNewFolders = 'none':** New folders will not be automatically opened.

### Editing Defaults Lists
To edit the defaults lists of File Type and Location, configure the **List Filter** nodes in the workflow tree.

##### File Types
Ensure the _args_ parameter of any option is the extension of the file type. **'custom' is reserved for the workflow.**

##### Locations
Ensure the _args_ parameter of any option is a valid path to the folder. Use '~/' to start the path at the User folder. **'browse' is reserved for the workflow.**
