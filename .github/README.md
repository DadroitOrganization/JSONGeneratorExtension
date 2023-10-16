# Dadroit JSON Generator VSCode Extension
![Version](https://img.shields.io/badge/version-1.1.2-brightgreen) [![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/DadroitOrganization/JSONGeneratorExtension/blob/main/LICENSE)

Use custom templates to easily create random nested JSON data right in your development workspace. This simple tool helps with debugging, checking schemas, and improving app performance.

### **Built Upon Dadroit Generator CLI Application**

The Dadroit JSON Generator VSCode extension is built upon the [Dadroit JSON Generator CLI](https://github.com/DadroitOrganization/Generator/tree/main) application. It integrates the CLI's capabilities for generating structured and detailed JSON data directly within your VSCode environment. 

### Practical Use Cases of Dadroit JSON Generator

This extension is particularly useful for:

- Generating structured JSON data with custom-defined schema by template.
- Ensuring consistency and integrity of JSON data for testing and development purposes.
- Making it easier to create diverse and large JSON data without complexity.

## How to use

### **Installation**

To install the extension:

- Open VSCode.
- Navigate to the Extensions panel and search for "Dadroit JSON Generator".
- Or install directly from the [VSCode Marketplace](https://marketplace.visualstudio.com/items?itemName=Dadroit.dadroit-json-generator).

### **Usage**

1. **Command Palette Usage:**
    To access the extension's features, open the Command Palette by pressing `Cmd+Shift+P` (on macOS) or `Ctrl+Shift+P` (on Windows and Linux), and select from the available commands such as `Dadroit: Generate JSON Sample` or `Dadroit: Generate JSON`.
2. **Template Utilization:**
    Use your custom templates or leverage the pre-built ones from our [GitHub Samples](https://github.com/DadroitOrganization/Generator/tree/main/Samples) to generate custom-defined JSON data.

## **Features**

### **Dynamic Templates:**

Employ templates with loop syntax for repetitive data structures.

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

### **Random Data Generation**

Utilizes built-in random function within the template language to produce varied data in JSON files.

```json
{
    "Age": {"$Random": {"$Min": 25,"$Max": 75}
}
```

## **Build from Source**

For developers wanting to modify or contribute to the extension:

1. **Clone the Repository:**
   
    ```bash
    git clone https://github.com/DadroitOrganization/JSONGeneratorExtension.git
    ```
    
2. **Install Dependencies:** Navigate to the project directory and run:
   
    ```bash
    npm install
    ```
    
3. **Build and Run:** Build the project and launch VSCode in an extension development host by hitting `F5` or running `Run Extension` from the debug menu.

For a comprehensive guide on how to use the JSON generator, visit [https://dadroit.com/blog/json-generator/](https://dadroit.com/blog/json-generator/).

## Contributing

We warmly welcome and value contributions from the community! If you have a template to share or want to improve the extension, here's how you can help:

- Explore our [sample templates](https://github.com/DadroitOrganization/Generator/tree/main/Samples) and adhere to their structure and syntax when creating yours.
- Submit a pull request with your valuable additions.

## License

The extension is under the [Apache-2.0 license](https://github.com/DadroitOrganization/JSONGeneratorExtension/blob/main/LICENSE).

## Issues and Support

Encounter an issue or need assistance? Please [create an issue on GitHub](https://github.com/DadroitOrganization/JSONGeneratorExtension/issues), and we'll be happy to help!

Thank you for exploring the Dadroit JSON Generator! Your feedback and contributions significantly shape this tool. Together, let's refine it further! Learn more in our blog post: [https://dadroit.com/blog/json-generator-vscode-extension/](https://dadroit.com/blog/json-generator-vscode-extension/).
