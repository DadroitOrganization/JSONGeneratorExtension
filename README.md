# Dadroit JSON Generator VSCode Extension
![Version](https://img.shields.io/badge/version-1.1.7-brightgreen) [![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/DadroitOrganization/JSONGeneratorExtension/blob/main/LICENSE)

Generate random nested data using custom templates to craft sample JSON files directly within your development workspace. This user-friendly JSON data generator tool is beneficial for debugging, schema validation, and optimizing your application's performance.

## Install

To install, search for "Dadroit JSON Generator" in the VSCode Extensions panel or download it directly from the VSCode Marketplace.

## Usage and Commands

To access the extension's features, open the Command Palette by pressing `F1` or `Ctrl+Shift+P` (on Windows), then type "Dadroit" to see the list of commands that you can select from. Here’s an overview of the currently available commands:

![Animated demonstration of using the Generate JSON Sample command in the VSCode extension.](https://raw.githubusercontent.com/DadroitOrganization/JSONGeneratorExtension/main/images/sample-command.gif)

### `Dadroit: Generate JSON Sample`

- **Purpose**: Automatically generate a JSON file based on a pre-defined template that was embedded in the extension for demonstration purposes.
- **How to Use**: After executing the command, you can view the template used for generating the JSON file opened in the VSCode editor.

### `Dadroit: Generate JSON`

- **Purpose**: Create a customized JSON file based on your own template code.
- **How to Use**:
    1. Open a new editor tab in VSCode.
    2. Paste or write your template code. For sample templates, you can visit our [GitHub samples](https://github.com/DadroitOrganization/Generator/tree/main/Samples).
    3. With the template opened in the editor, execute the `Dadroit: Generate JSON` command to generate the JSON file based on it.

After executing each command, you’ll be presented with 2 action buttons in the notification message which you can choose from. The first one is to open the resultant JSON data in VSCode, and the latter is for opening the JSON file location.

### Dynamic Templates

Use templates with loop syntax to handle repetitive data structures.

```json
{
  "List": {
    "$Loop": {
      "$From": 0,
      "$To": 9,
      "$Var": "I",
      "$Block": {
        "X": {
          "$GetVar": "I"
        }
      }
    }
  }
}
```

### Random Data Generation

Use the template language's built-in random function to generate varied data in JSON files.

```json
{
  "Age": {
    "$Random": {
      "$Min": 25,
      "$Max": 75
    }
  }
}
```

### Build from Source

For developers interested in modifying or contributing to the extension:

1. **Clone the repository:**
   
    ```bash
    git clone https://github.com/DadroitOrganization/JSONGeneratorExtension.git
    ```
    
2. **Install dependencies:** Navigate to the project directory and run:
   
    ```bash
    npm install
    ```
    
3. **Build and run:** Build the project and launch VSCode in an extension development host by hitting `F5` or running `Run Extension` from the debug menu.

For a comprehensive guide on how to use the JSON generator, visit [https://dadroit.com/blog/json-generator/](https://dadroit.com/blog/json-generator).

## Compatibility

This extension is now available for Windows, macOS, and Linux operating systems. Stay tuned for further updates and expanded compatibility.

## License

The extension is licensed under the [Apache-2.0 license](https://github.com/DadroitOrganization/JSONGeneratorExtension/blob/main/LICENSE).

## Contributing

Your contributions are invaluable to making the Dadroit JSON Generator better! If you've crafted a useful template and wish to share it with the community:

- Visit our [GitHub repository sample folder](https://github.com/DadroitOrganization/Generator/tree/main/Samples) to understand the structure and formatting of existing templates.
- Feel free to submit a pull request with your added template, ensuring it adheres to the syntax found in the sample folder.

## Introducing the Capabilities of Dadroit JSON Generator 

For a better understanding of the core values and features of this extension, don't miss our introductory blog post: [https://dadroit.com/blog/json-generator-vscode-extension/](https://dadroit.com/blog/json-generator-vscode-extension/).

## Issues and Support

For any questions, issues, or assistance, please [Create an issue on GitHub](https://github.com/DadroitOrganization/JSONGeneratorExtension/issues).