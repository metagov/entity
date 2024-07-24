## EIP-4824 

Instructions at [instructions.md](instructions.md). [Copy all of the below over. Keep just a few very easily digestable isntructions here.]

### Introduction to EIP-4824

EIP-4824 addresses the challenge of collecting and standardizing essential DAO metadata. With over 20,000 DAOs spread across various blockchains, governance frameworks, and operational structures, consolidating this data has become a complex task. The metadata needed to understand a DAO's structure, proposals, members, contracts, and activities is often scattered across multiple platforms, making it difficult to access and manage.

EIP-4824 introduces a standardized way to handle DAO metadata using a `daoURI`, which is a URI (Uniform Resource Identifier) that points to a DAO's metadata. This metadata can be published both on-chain and off-chain, providing a comprehensive view of a DAO's operations and governance.

### Publishing DAO URIs 

One effective method for publishing and managing DAO URIs is using a GitHub repository. This approach offers several advantages, including modifiability, version control, and ease of use. By leveraging GitHub, DAOs can maintain their metadata in a familiar and widely adopted platform, reducing the need for on-chain transactions for updates.

### Creating and Hosting DAO URIs via GitHub

#### Step 1: Clone the Repository

1. **Clone the Repository**:
   - Clone the EIP-4824 GitHub repository for the branch `eip4824` to get started:
     ```sh
     git clone -b eip4824 https://github.com/metagov/eip4824.git
     ```

2. **Navigate to the Repository**:
   - Change into the repository directory:
     ```sh
     cd eip4824
     ```

#### Step 2: Define the DAO URI JSON-LD Schema

1. **Modify a JSON File**:
   - In the repository, modify file named `daoURI.json`.

2. **Schema Definition**:
   - Use the following JSON-LD schema as defined by EIP-4824:
     ```json
     {
         "@context": "http://www.daostar.org/schemas",
         "type": "DAO",
         "name": "<name of the DAO>",
         "description": "<description>",
         "membersURI": "<URI>",
         "proposalsURI": "<URI>",
         "activityLogURI": "<URI>",
         "governanceURI": "<URI>",
         "contractsRegistryURI": "<URI>"
     }
     ```
   - Refer to the [EIP-4824 documentation](https://eips.ethereum.org/EIPS/eip-4824) for more details on building the JSON schema.

3. **Populate the JSON**:
   - Fill in the required fields with your DAO’s specific information.
   - Ensure all URIs provided are valid and point to relevant resources.

#### Step 3: Commit and Push the Changes

1. **Commit the File**:
   - Once the JSON file is created and populated, commit the changes with a meaningful message, e.g., `Initial commit of DAO URI`.
     ```sh
     git add daoURI.json
     git commit -m "Initial commit of DAO URI"
     ```

2. **Push to Repository**:
   - Push the committed changes to the GitHub repository.
     ```sh
     git push origin eip4824
     ```

#### Step 4: Make the Repository Public

1. **Repository Settings**:
   - Ensure the repository is public so that anyone can access the DAO URI.

2. **Access URL**:
   - The JSON file can be accessed via the GitHub URL, e.g., `https://github.com/YourUsername/eip4824/blob/eip4824/daoURI.json`.

#### Step 5: Update and Maintain

1. **Regular Updates**:
   - Regularly update the `daoURI.json` file to reflect any changes in members, proposals, governance, etc.

2. **Commit and Push**:
   - Follow the commit and push process for any updates to maintain version control and transparency.

### Example JSON-LD for DAO URI

```json
{
    "@context": "http://www.daostar.org/schemas",
    "type": "DAO",
    "name": "Example DAO",
    "description": "This is an example DAO.",
    "membersURI": "https://example.com/members",
    "proposalsURI": "https://example.com/proposals",
    "activityLogURI": "https://example.com/activity-log",
    "governanceURI": "https://example.com/governance",
    "contractsRegistryURI": "https://example.com/contracts-registry"
}
```

### Publishing DAO URI On-Chain

After creating and hosting your DAO URI via GitHub, the next crucial step is to publish it on-chain. This ensures that the metadata is verifiable and publicly accessible in a decentralized manner. You can choose any methods listed below to publish DAO URI

#### Method 1: Deploy a Registration Contract

1. **Initiate a Forum Proposal**:
   - Start a forum proposal/discussion on adopting EIP-4824 and the potential daoURI for your DAO.
   
2. **Create the daoURI**:
   - Follow the steps above to create the daoURI and host it on GitHub.

3. **Execute the Transaction**:
   - If the governance proposal passes, execute the transaction to deploy a registration contract that stores your daoURI on-chain.
   - The EIP-4824 registration factory contract is deployed to nearly all EVM chains. For mainnet, the address is `0x2Dac5DBbF1D024c1E0D9c92D3AeDa7618e15aDd7`.

#### Method 2: Use an ENS Text Record

1. **Set as an ENS Text Record**:
   - You can set the daoURI as an ENS (Ethereum Name Service) text record. Depending on the management of the ENS name, this may require governance approval.

#### Method 3: Use Ethereum Attestation Service (EAS)

1. **EAS Attestations**:
   - Utilize the Ethereum Attestation Service to issue on-chain attestations containing the DAO's daoURI.
   - This method is akin to notarizing the daoURI on the blockchain, providing a secure and transparent way to verify the DAO’s metadata.


##### Congratulations on taking a step towards transparent governance!

### Support

For further assistance or questions, feel free to reach out to the community or the DAOstar support team.

Contact: rashmi@daostar.org
Telegram: https://t.me/+3gf-K5c2iDllOGZl




