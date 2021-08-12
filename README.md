# Instructions to create new subgraph

1. Go to https://thegraph.com/studio and connect from metamask wallet.

2. Create a new subgraph by choosing a unique subgraph name

3. In your cli, execute the following commands:

> `$ npm install -g @graphprotocol/graph-cli`

> `$ graph init --contract-name Token --index-events --product subgraph-studio --from-contract 0xabEFBc9fD2F806065b4f3C237d4b59D9A97Bcac7`

4. Edit schema.graphql and subgraph.yaml by refering the code in the repo

5. Execute this codegen command:

> `$ graph codegen`

6. Edit mapping.ts with the event handling code from the repo

7. Enter the following command followed by the deploy key from the subgraph dashboard:

> `$ graph auth --studio`

8. Deploy the subgraph:

> `$ graph deploy --studio your_subgraph_name`

9. Check the subgraph studio, the syncing process would begin. Fire the example query to check if data is retrieved.

10. Publish the subgraph on the rinkeby testnet. Check the faucet for rinkeby if you are running low on funds. 

11. Once a subgraph is published, curators can start signalling and indexers can start indexing the data for queries.