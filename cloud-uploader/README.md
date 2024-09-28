# Cloud Uploader

A bash-based CLI tool for uploading files to Azure Storage. This tool offers a seamless upload experience similar to popular storage services.

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/cloudquill/cloud-uploader.git
   cd cloud-uploader
   ```

2. **Ensure Prerequisites are Installed**:
   - Bash
   - Azure CLI (`az` command)

3. **Set Up a Service Principal**:
   - Create a service principal (sp) with Bash CLI:
     ```bash
     az ad sp create-for-rbac \
       --name <your-sp-name> \
       --role Contributor \
       --scopes /subscriptions/<your-subscription-id>
     ```

4. **Fill the service principal details in the config file.**

5. **Fill the storage account and container details in the config file.**

## Usage

1. **Upload a File**:
   ```bash
   ./file-cloud-uploader <file-path>
   ```

2. **Example**:
   ```bash
   ./file-cloud-uploader myfile.txt
   ```

## Configuration

- Ensure you have the necessary permissions to upload files to the specified Azure container.
- Configure your Azure CLI with the required subscription and storage account.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue.

## License

This project is licensed under the MIT License.