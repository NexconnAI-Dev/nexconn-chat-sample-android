# NexconnChat Samples

Scenario-based Android sample apps for the Nexconn Chat SDK.

## Initialization

SDK initialization (`NCEngine.initialize`) is performed in the shared `SampleApplication` class
(located in `commonmodule/`), which runs in `Application.onCreate()`. Each sample module references
`SampleApplication` in its `AndroidManifest.xml`, so initialization happens automatically at app
startup — the **Connect** button in each sample only calls `NCEngine.connect()`.

## Structure

- `commonmodule/` — shared library: `SampleConfig`, `LogOutputActivity`, `SampleApplication`
- `directchannel-send-text/` — Send text message in Direct Channel
- `directchannel-send-media/` — Pick and send image message in Direct Channel
- `groupchannel-create-send/` — Create Group Channel and send message
- `channel-list/` — Fetch recent Direct + Group Channel list
- `channel-dnd/` — Set Do-Not-Disturb for channels
- `groupchannel-members/` — Fetch Group Channel member info

## Configuration

Edit `commonmodule/.../SampleConfig.kt`:

| Field | Description |
|---|---|
| `appKey` | Your Nexconn Chat app key |
| `token` | User authentication token |
| `naviServer` | Navigation server URL (optional, for private deployment) |
| `directTargetId` | Target user ID for Direct Channel samples |
| `groupId` | Group Channel ID |
| `groupName` | Group Channel name |
| `memberUserIds` | Member user IDs for group operations |

## Build & Run

1. Clone or download this repository.
2. Open the project root directory in Android Studio.
3. Select any sample module (e.g., `directchannel-send-text`) from the run configuration dropdown.
4. Click **Run**.
