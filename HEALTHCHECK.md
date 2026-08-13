# Healthcheck Script

A simple Bash script that checks whether a website is reachable and displays its HTTP status code and response time.

## How to Run

First, make the script executable:

```bash
chmod +x scripts/healthcheck.sh
```

Then run the script with a website URL:

```bash
./scripts/healthcheck.sh http://127.0.0.1/
```


If no URL is provided, the script will display a usage message and exit with an error code.

## Exit Codes

Every program or script returns an **exit code** when it finishes.

- `0` means the program or script completed successfully.
- Any **non-zero value** means the program or script encountered a problem or failed.

In this healthcheck script:

- `0` means the website is healthy and returned a successful HTTP status code.
- `1` means there was a problem, such as:
  - No URL was provided.
  - The website could not be reached.
  - The website returned an unsuccessful HTTP status code.

You can check the exit code of the last command using:

```bash
echo $?
```

Example:

```bash
./scripts/healthcheck.sh http://127.0.0.1/
echo $?
```

If the healthcheck is successful:

```text
0
```

## Files That Should Never Be Saved in Git

Sensitive files should never be committed to Git, including:

- `.env` files
- `*.pem` private key files
- Passwords
- API keys
- Private keys
- Other secrets or credentials

These files should be added to `.gitignore` to prevent them from being accidentally committed.
