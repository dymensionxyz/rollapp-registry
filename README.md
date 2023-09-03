# RollApp Registry

![RR](https://github.com/dymensionxyz/rollapp-registry/assets/109034310/081caab5-01c4-4183-93dc-ae2604a1129f)


A registry for RollApps on Froopyland testnet:

This repository is dedicated to the listing process of RollApps on the [Portal](https://portal.dymension.xyz/rollapps).

Please follow the instructions for listing a RollApp:

1. Make sure to have successfully deployed and are running a RollApp instance. All outputs on `Roller Run` screen should show the RollApp running in `active` state.

2. Fund the Faucet and test the IBC connection by submitting an IBC transfer of your RollApp token to the Dymension Hub faucet with the following command:

    ```
    roller tx fund-faucet
    ```

    Subsequently, check the balance of the RollApp token on the Dymension Hub faucet which should arrive within 15-30 minutes:

    ```
    $balance dym1g8sf7w4cz5gtupa6y62h3q6a4gjv37pgefnpt5 <RollApp-ID>
    ```

3. Fork the RollApp-registry [this repo] into your GitHub account and then clone it using:

    ```bash
    git clone https://github.com/<your-github-username>/rollapp-registry
    ```

4. Create a new folder with the following structure:

    ```tree
    ├── <RollApp-ID>
    │   ├── <RollApp-ID>.json
    │   └── logos
    │       └── <RollApp-ID>-logo.svg
    ```

5. Export the RollApps configuration JSON by running 

     ```
    roller config export
    ``` 

6. Copy paste the JSON output to the `<RollApp-ID>.json` and fill in the following fields:

    a. RPC: ```"https://<your-ip-or-domain>:<port>" (default port 26657)``` 
    
    b. REST: ``` "https://<your-ip-or-domain>:<port>" (default port 1317)```
    
    c. EVM RPC *(ONLY IF EVM): ```"https://<your-ip-or-domain>:<port>" (default port 1317)``` 
    
    d. Logo path: ```"/logos/<RollApp-ID>-logo.svg"```

7. Add your RollApp logo to the `logos` folder. This can be SVG, PNG, or JPG format. Please keep the size of the file under 50KB.

8. Create a PR to https://github.com/dymensionXYZ/rollapp-registry. For a demonstration of a step-by-step guide to creating a PR please follow the [GitHub documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) or watch this helpful [youtube video](https://www.youtube.com/watch?v=a_FLqX3vGR4).

9. Pair the RollApp on the Discord channel: [here](https://discord.com/channels/956961633165529098/1140590139022782474) by entering `$pair <RollApp-ID>` (replace <RollApp-ID> with your customized RollApp ID). 

    A community moderator will then begin a conversation with you in Discord. Please follow attentively to get the listing process fulfilled quickly. If you have any question please feel free to reach out to the coreteam and community on Discord. We're here for you!
