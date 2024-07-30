### Adopting daoURI: Two-Step Process

### Step 1: Creating and Hosting DAO URI JSON

#### Step 1.1: Clone the Repository

1. **Clone the Repository**:
   - Clone the EIP-4824 GitHub repository to get started:
     ```sh
     git clone https://github.com/metagov/eip4824.git
     ```

#### Step 1.2: Define the DAO URI JSON-LD Schema

1. **Modify a JSON File**:
   - In the repository, modify a file named `daoURI.json`.

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

#### Step 1.3: Commit and Push the Changes

1. **Commit the File**:
   - Once the JSON file is populated, commit the changes with a meaningful message, e.g., `Initial commit of DAO URI`.
     ```sh
     git commit -m "Initial commit of DAO URI"
     ```

2. **Push to Repository**:
   - Push the committed changes to the GitHub repository.
     ```sh
     git push
     ```

### Step 2: Publishing DAO URI

After creating and hosting your DAO URI via GitHub, the next crucial step is to publish it on-chain. This ensures that the metadata is verifiable and publicly accessible in a decentralized manner. For detailed instructions, refer to the [DAOstar documentation on publishing the daoURI](https://docs.daostar.org/How%20To's/Adopt%20EIP-4824#step-2-publish-the-daouri).

#### Congratulations on taking a step towards transparent governance!

By following these steps, you ensure that your DAO’s metadata is both accessible and verifiable, promoting transparency and interoperability within the decentralized ecosystem.
