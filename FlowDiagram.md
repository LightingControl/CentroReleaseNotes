# Github Action Flow

```mermaid

flowchart TD
    Trigger["👆 You trigger workflow with tag v1.2.0"]
    Checkout["📥 Checkout public repo"]
    Init["📝 Create/prepare CHANGELOG.md"]
    FetchA["📡 Fetch Release from repo-a"]
    FetchB["📡 Fetch Release from repo-b"]
    FetchC["📡 Fetch Release from repo-c"]
    Append["➕ Append all to CHANGELOG.md"]
    Commit["💾 Commit and push changelog"]

    Trigger --> Checkout --> Init
    Init --> FetchA --> Append
    Init --> FetchB --> Append
    Init --> FetchC --> Append
    Append --> Commit

    ```