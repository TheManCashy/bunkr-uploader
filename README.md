## Usage
#### Requirements
- You must have an bunkr account to be able to upload.
- `https://dash.bunkr.cr/dashboard` visit your dashboard to get the account token.

#### Installation
```
cargo install bunkr-uploader
```
#### View available commands and options

```
bunkr-uploader --help
```

#### Upload a file or directory

```
bunkr-uploader <path-to-file-or-directory>
```

#### Flags

| Flag | Short | Description |
|------|-------|-------------|
| `--force` | `-f` | Force upload without skipping (re-upload previously uploaded files) |
| `--no-album` | | Skip adding files to an album |
| `--album-id <ID>` | | Upload to an existing album by ID (skips interactive prompt) |
| `--new-album` | | Create a new album and upload to it (skips interactive prompt) |

#### Examples

```
# Upload a file, skipping album prompt
bunkr-uploader --no-album file.mp4

# Upload to an existing album
bunkr-uploader --album-id 42 file.mp4

# Upload and create a new album automatically
bunkr-uploader --new-album file.mp4

# Re-upload a previously uploaded file
bunkr-uploader --force file.mp4
```
