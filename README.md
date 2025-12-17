# WynTenantBasedLogin

---

This sample showcases the feature to Login to the Wyn Portal using Tenant based authentication in an Embedded app.
The users will see only those features where the organization that they're part of, has permissions.

Steps to run the sample using npm:

1. Install http-server package globally:
   npm install http-server -g
2. Open cmd as administrator
3. Navigate to the sample's location
4. Run the following command:
   http-server
5. Open http://localhost:8080/ in a browser

## Configuring Wyn instances (admin) 🔧

This sample now supports multiple Wyn instances. The login form shows a dropdown (`#wynSelect`) populated from a `.env` file (variable `WYN_INSTANCES`) or from `instances.json` as a fallback.

- `.env` format (required key: `WYN_INSTANCES`) example:

```text
WYN_INSTANCES='[{"name":"Local","url":"http://localhost:8080"},{"name":"Production","url":"https://wyn.example.com"}]'
```

- `instances.json` fallback format (array of objects):

```json
[
  { "name": "Local", "url": "http://localhost:8080" },
  { "name": "Production", "url": "https://wyn.example.com" }
]
```

To add or remove instances, edit `.env` or `instances.json` and restart the static server if required. The admin can add instances by providing a `name` (displayed in the dropdown) and a `url` (used to call the Wyn Portal endpoints).
