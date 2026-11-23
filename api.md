# BoxFleet hosted control plane (boxfleet.io) Python API

<!-- omniwrap-api-reference eyJjb250cmFjdF9maW5nZXJwcmludCI6ImUzZmQ0Yzc0NGFlODkzM2MwZTBiZDBjMjFhNjkyODk3Nzk1YTE0NjU3ZTU3N2ZiODIxMDg1MDBkMzlmMmFjOGQiLCJvcGVyYXRpb25fY291bnQiOjU2LCJyZW5kZXJlciI6InB5dGhvbiIsInZlcnNpb24iOiIxLjUuMCJ9 -->

This generated index is tied to Semantic IR `1.14.0` and contract fingerprint `e3fd4c744ae8933c0e0bd0c21a692897795a14657e577fb82108500d39f2ac8d`. Every operation below is rendered from the same semantic contract and artifact-attested public member allocation as the SDK.

SDK maturity: **experimental**  
Artifact evidence: [`omniwrap-artifact.json`](omniwrap-artifact.json) binds this file by SHA-256 and is revalidated by the package gate.

## Client hooks and tracing

`Client(hooks=Hooks(...))` registers four callbacks. Every attempt starts with `before_request` and ends with exactly one of `on_retry` (another attempt follows), `after_response` (the success the call returns) or `on_error` (the failure the call reports). Each receives the operation id, the HTTP method, the URL, the request headers, the attempt number (from 1), the time elapsed since the call started and, once the server answered, the HTTP status. No context carries a credential: `Authorization`, `Proxy-Authorization`, `Cookie`, every API-key header and API-key query parameter, and any configured credential value read `[redacted]`. Every context is a frozen `HookContext`: no hook can change the request.

`Client(tracer=...)` opens one span per call through the tracer interface this SDK defines, named after the operation id, with `http.request.method`, `http.response.status_code` and `http.request.resend_count`. It needs no tracing library; README.md maps it onto the OpenTelemetry API.

## Shared types

- `HostedPersistentBoxClose`
- `HostedPersistentBoxRead`
- `HostedPersistentUsageMeter`
- `HostedPersistentUsageRead`
- `ObservedBox`

## Resource `accounts`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhY2NvdW50cy5nZXRfY29uZmlnIiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoiZ2V0QWNjb3VudHNDb25maWciLCJwYXRoIjoiL3YxL2FjY291bnRzL2NvbmZpZyIsInJlc291cmNlIjoiYWNjb3VudHMiLCJzZWN0aW9uX3NoYTI1NiI6ImRjMWQ1MDQ4NzY2YWNkNWZjY2JkZjExM2Y5ZmEyODQyMDVkZWE0Zjg4YTgwNGU1ZDA3MTIwMmEzOTBlYzMzNjgiLCJzaWduYXR1cmVfc2hhMjU2IjoiZDZiYzk1NjVmODUxNTk3ZWU0Yzc1MWVjZGFkY2VkMTgwMWY5NDZiZWM3ZTA5NTdhMDFjODE5ZTBmYjMwYjAzZCJ9 -->
### `client.accounts.get_config`

Operation ID: `getAccountsConfig`  
Route: `GET` `/v1/accounts/config`  
Equivalent member: `client.get_accounts_config`  

#### Signature

```python
client.accounts.get_config(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | OK | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.accounts.get_config()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRBY2NvdW50c0NvbmZpZyJ9 -->

## Resource `admin`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhZG1pbi5jb250cm9sX3VzZXIiLCJtZXRob2QiOiJQT1NUIiwib3BlcmF0aW9uX2lkIjoiY29udHJvbFVzZXIiLCJwYXRoIjoiL3YxL2FkbWluL3VzZXJzIiwicmVzb3VyY2UiOiJhZG1pbiIsInNlY3Rpb25fc2hhMjU2IjoiZDg1Nzg5YWJkN2M0ZWYwOWMwYjE4ZGZmNGVmOWFhZmNmMzI1MGMxYThmMmEyMzIzNTEyNmFmMGI3MzY1ZDQ5NCIsInNpZ25hdHVyZV9zaGEyNTYiOiI4YWQwYjE4ZDVlODc3M2Q1YmI1YmFkZGEyODM5MmFjM2I2MGJiOTZiYWIyN2I2YTQzMmExOGUyMGZjZDRlNzA1In0 -->
### `client.admin.control_user`

Operation ID: `controlUser`  
Route: `POST` `/v1/admin/users`  
Equivalent member: `client.control_user`  

#### Signature

```python
client.admin.control_user(body: dict[str, Any], *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Applied | none |
| `401` | Admin token required | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.admin.control_user({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJjb250cm9sVXNlciJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhZG1pbi5nZXRfY29uc29sZSIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6ImdldEFkbWluQ29uc29sZSIsInBhdGgiOiIvdjEvYWRtaW4vY29uc29sZSIsInJlc291cmNlIjoiYWRtaW4iLCJzZWN0aW9uX3NoYTI1NiI6ImU2MzlkZGUwOWNhNjA1YjU5YzMwNWI5OTViZTA1OGI1OWMyNWZjN2E1MmYxODdjMDQ0ODNkZGVmZTQ5YTA3MmYiLCJzaWduYXR1cmVfc2hhMjU2IjoiNjVlOTVlMTViNmFiMTY2NjQyYThlNzIyNzYxOTNiNmNhY2E0NzlkYTRlYzAwNjNiZGYzNDYwNmMwMzEzNmViOCJ9 -->
### `client.admin.get_console`

Operation ID: `getAdminConsole`  
Route: `GET` `/v1/admin/console`  
Equivalent member: `client.get_admin_console`  

#### Signature

```python
client.admin.get_console(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Console | none |
| `401` | Admin token required | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.admin.get_console()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRBZG1pbkNvbnNvbGUifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhZG1pbi5nZXRfcGxhbnMiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJnZXRBZG1pblBsYW5zIiwicGF0aCI6Ii92MS9hZG1pbi9wbGFucyIsInJlc291cmNlIjoiYWRtaW4iLCJzZWN0aW9uX3NoYTI1NiI6ImU5OGIzMWZmOGI0YTkwNmZiYzBjOWIxY2NhY2FjMzc0MTc2Zjc4NTU2N2M1YjVlZmVhMmU5OGQ3ZDliZDEzY2YiLCJzaWduYXR1cmVfc2hhMjU2IjoiZWU4MTFjYTI1NDRkNDU2ODRjMDM3YzNiOTM4ZDYwMzllYzAzMmU3Mzg1ZjYzMjY2ODM5NGY1OTQzYTY2NmUxYiJ9 -->
### `client.admin.get_plans`

Operation ID: `getAdminPlans`  
Route: `GET` `/v1/admin/plans`  
Equivalent member: `client.get_admin_plans`  

#### Signature

```python
client.admin.get_plans(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Plans | none |
| `401` | Admin token required | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.admin.get_plans()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRBZG1pblBsYW5zIn0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhZG1pbi5saXN0X3VzZXJzIiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoibGlzdFVzZXJzIiwicGF0aCI6Ii92MS9hZG1pbi91c2VycyIsInJlc291cmNlIjoiYWRtaW4iLCJzZWN0aW9uX3NoYTI1NiI6IjZhNTZjNDE0MDg3ZGU1NGI5NjQ1NmEyZTAwZDcwMTE2ZDRlYjU2YjI5YjFjYTllMTIyNTlkYmJhMzFmYjI0ZDMiLCJzaWduYXR1cmVfc2hhMjU2IjoiZTI2ZWJkZTcxNDA1NTQwZmY5NzdiNjI5M2NlY2NhOGZmYzg5ODljYjhkNjE5ZGQxOWM0Y2JiN2M4M2Y0YmE2NSJ9 -->
### `client.admin.list_users`

Operation ID: `listUsers`  
Route: `GET` `/v1/admin/users`  
Equivalent member: `client.list_users`  

#### Signature

```python
client.admin.list_users(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Users | none |
| `401` | Admin token required | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.admin.list_users()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0VXNlcnMifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhZG1pbi5yZWFkX3RlbGVtZXRyeSIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6InJlYWRUZWxlbWV0cnkiLCJwYXRoIjoiL3YxL2FkbWluL3RlbGVtZXRyeSIsInJlc291cmNlIjoiYWRtaW4iLCJzZWN0aW9uX3NoYTI1NiI6ImEzMDAzNTFkMTQ0ODc0ZGI4YmUyNzAyMmMwNTI0YWRhOThjYmEyZjMzMDgwYjU5MGJiODBhNzkzNjU5Zjk1Y2UiLCJzaWduYXR1cmVfc2hhMjU2IjoiZWIxMTI3ZTIzOGQ5M2Q2OGNkNzhmOTJmNWY0YjNjMTE4ZmUzNjE5MGYyYjExMTZlNWRjMmY2YWZlYjkxMzczMyJ9 -->
### `client.admin.read_telemetry`

Operation ID: `readTelemetry`  
Route: `GET` `/v1/admin/telemetry`  
Equivalent member: `client.read_telemetry`  

#### Signature

```python
client.admin.read_telemetry(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Events | none |
| `401` | Admin token required | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.admin.read_telemetry()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJyZWFkVGVsZW1ldHJ5In0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhZG1pbi51cGRhdGVfcGxhbiIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJ1cGRhdGVQbGFuIiwicGF0aCI6Ii92MS9hZG1pbi9wbGFucyIsInJlc291cmNlIjoiYWRtaW4iLCJzZWN0aW9uX3NoYTI1NiI6IjU5ZGVlYjk5OTA3OGE4Y2JkNTY1NmUxOWE4YjYwZmE1OGZiMmNkZjFmNjc3ODAxOGRjYzA3NDlkMmJjMjJjNjMiLCJzaWduYXR1cmVfc2hhMjU2IjoiMTNkODAyMjQ3ZDFkNjE4ZTRlNGFkYjQ1OGFiNzliODkxNTYwNmMyODJmZmIwYzk5NWUxYzJjN2MzMDFjYmIzOSJ9 -->
### `client.admin.update_plan`

Operation ID: `updatePlan`  
Route: `POST` `/v1/admin/plans`  
Equivalent member: `client.update_plan`  

#### Signature

```python
client.admin.update_plan(body: dict[str, Any], *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Updated | none |
| `401` | Admin token required | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.admin.update_plan({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJ1cGRhdGVQbGFuIn0 -->

## Resource `auth_`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhdXRoXy5nZXRfZ2F0ZSIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6ImdldEF1dGhHYXRlIiwicGF0aCI6Ii92MS9hdXRoL2dhdGUiLCJyZXNvdXJjZSI6ImF1dGhfIiwic2VjdGlvbl9zaGEyNTYiOiI4ZTRlMjE3NGQ5YjA1NDU3M2ExMzNlNDllNDc0ZmExOWY3YmQ5YWU0ZmU0MzgxMjgzNWZjMjNhYWFmNGUyN2Y0Iiwic2lnbmF0dXJlX3NoYTI1NiI6IjNkZTJkMTJlN2UzNjlhZjYzMjFiMGU1ZDNjYjM0ZDA0YWM0YzY5ZWJkNjE5NzFmNzAzYjJjNTkzZmNjYzQ1ZjgifQ -->
### `client.auth_.get_gate`

Operation ID: `getAuthGate`  
Route: `GET` `/v1/auth/gate`  
Equivalent member: `client.get_auth_gate`  

#### Signature

```python
client.auth_.get_gate(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | OK | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.auth_.get_gate()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRBdXRoR2F0ZSJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhdXRoXy5yZWdpc3RlciIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJyZWdpc3RlciIsInBhdGgiOiIvdjEvYXV0aC9yZWdpc3RlciIsInJlc291cmNlIjoiYXV0aF8iLCJzZWN0aW9uX3NoYTI1NiI6ImRkMmMwYzY4YjRlYjJiOTUyNWM2MzkxZGY4ZGFiYzI3MDBhNjRkOTQ0NjMyOTQyZmUzY2VmMjhhNzBhOWJjOTEiLCJzaWduYXR1cmVfc2hhMjU2IjoiNjU3M2QyMGZjOWVmOGE0ODZjZWZiMWIwODJhOTBlNGRiMmMyN2RiY2Q2ZjBlYjBlNDk4YTVmYmJhMjM1OTUzOSJ9 -->
### `client.auth_.register`

Operation ID: `register`  
Route: `POST` `/v1/auth/register`  
Equivalent member: `client.register`  

#### Signature

```python
client.auth_.register(body: dict[str, Any], *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `201` | License issued | none |
| `202` | Verification code sent (or withheld by the resend cooldown) | none |
| `400` | Invalid or expired code | none |
| `403` | Not invited or refused | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |
| `429` | Rate limited | none |
| `503` | Registration not configured | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.auth_.register({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJyZWdpc3RlciJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhdXRoXy51cGRhdGVfZ2F0ZSIsIm1ldGhvZCI6IlBVVCIsIm9wZXJhdGlvbl9pZCI6InVwZGF0ZUF1dGhHYXRlIiwicGF0aCI6Ii92MS9hdXRoL2dhdGUiLCJyZXNvdXJjZSI6ImF1dGhfIiwic2VjdGlvbl9zaGEyNTYiOiJlYjY1NDFkNWY1MGQ1ZjI2YzdhZWExZTExZmViNGNhZTExNDY2ZTExNWMwODZlN2I3ZTRiOTNjZTUzOTNhZGE4Iiwic2lnbmF0dXJlX3NoYTI1NiI6IjVmYmFiNzM4ZTg1ZmFlMDcxYWY1YTNiYTllN2FmMGUxOWYwNDRhY2UzNWRkNWYwMGU2ZWI3MjU3OTgxZjNjZjEifQ -->
### `client.auth_.update_gate`

Operation ID: `updateAuthGate`  
Route: `PUT` `/v1/auth/gate`  
Equivalent member: `client.update_auth_gate`  

#### Signature

```python
client.auth_.update_gate(body: dict[str, Any], *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Updated | none |
| `401` | Admin token required | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.auth_.update_gate({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJ1cGRhdGVBdXRoR2F0ZSJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJhdXRoXy52ZXJpZnlfbGljZW5zZSIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJ2ZXJpZnlMaWNlbnNlIiwicGF0aCI6Ii92MS9hdXRoL3ZlcmlmeSIsInJlc291cmNlIjoiYXV0aF8iLCJzZWN0aW9uX3NoYTI1NiI6ImU4MzdlYjQxNjAzM2M5ZDFmNjY0MTM4YTZmZDc1ODYzMzM3Y2JlNzRlZTRjNGU5NWU4YjFlMDRjYzUyYzI5ZWMiLCJzaWduYXR1cmVfc2hhMjU2IjoiYTllODQ5MWVlNWNlMTI5M2M4NGQzMDYxNzlhMzQ1ZDQzNzczNDFjMjc4Yzc2M2ZkYTEwOWExNmViZWY2OGY1NyJ9 -->
### `client.auth_.verify_license`

Operation ID: `verifyLicense`  
Route: `POST` `/v1/auth/verify`  
Equivalent member: `client.verify_license`  

#### Signature

```python
client.auth_.verify_license(body: dict[str, Any], *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Valid | none |
| `401` | Invalid license | none |
| `403` | Refused | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |
| `503` | Verification not configured | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.auth_.verify_license({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJ2ZXJpZnlMaWNlbnNlIn0 -->

## Resource `billing`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJiaWxsaW5nLnN0cmlwZV93ZWJob29rIiwibWV0aG9kIjoiUE9TVCIsIm9wZXJhdGlvbl9pZCI6InN0cmlwZVdlYmhvb2siLCJwYXRoIjoiL3YxL2JpbGxpbmcvc3RyaXBlL3dlYmhvb2siLCJyZXNvdXJjZSI6ImJpbGxpbmciLCJzZWN0aW9uX3NoYTI1NiI6ImQ4MDYyYTkxZWRiNTIyMzZlMDQwODdhYjc0OTBjZjIwYTgyYjc0MTE3NzlkN2FhMmIyOGE1ZTAyYjY1OGEyNmYiLCJzaWduYXR1cmVfc2hhMjU2IjoiNWU5NDc1NWE3OTBkZjA4NzJhMTRiZTY3N2QwM2U1NDRlMjI5ZTdmZGI4ZTUwM2IxOGMyMzJjODQ3ODA1NzVhYiJ9 -->
### `client.billing.stripe_webhook`

Operation ID: `stripeWebhook`  
Route: `POST` `/v1/billing/stripe/webhook`  
Equivalent member: `client.stripe_webhook`  

#### Signature

```python
client.billing.stripe_webhook(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Received | none |
| `400` | Invalid signature or payload | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.billing.stripe_webhook()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJzdHJpcGVXZWJob29rIn0 -->

## Resource `health`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJoZWFsdGguZ2V0IiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoiZ2V0SGVhbHRoIiwicGF0aCI6Ii9oZWFsdGgiLCJyZXNvdXJjZSI6ImhlYWx0aCIsInNlY3Rpb25fc2hhMjU2IjoiMWNlNjljNWJmYWE5NTgwM2RhODdhMmJmODlkYThjNzNhNzE4OTEyNmYyOGU3NjdlY2IxMzQ1ODdiNjY5NWE5OSIsInNpZ25hdHVyZV9zaGEyNTYiOiIxOWRiZmQ0MTM1N2I1ZWZlNzVhNjU5YzA5ZjNiNWU5ZjY5YWY0YzUwNDViNTJiZGM5NmRjNzNlN2QzNjkzNWM0In0 -->
### `client.health.get`

Operation ID: `getHealth`  
Route: `GET` `/health`  
Equivalent member: `client.get_health`  

#### Signature

```python
client.health.get(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | OK | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.health.get()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRIZWFsdGgifQ -->

## Resource `jobs`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJqb2JzLmNhbmNlbCIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJjYW5jZWxKb2IiLCJwYXRoIjoiL3YxL2pvYnMve2pvYklkfS9jYW5jZWwiLCJyZXNvdXJjZSI6ImpvYnMiLCJzZWN0aW9uX3NoYTI1NiI6IjllYjQ4Mzc1Y2RiYWQ2YWQ1YTYzODg4OWNjYTdjOGM0ZTVjYzQyMzA0ZjdhNTliZDJhY2U5ZWE5M2E2OTE5ZGUiLCJzaWduYXR1cmVfc2hhMjU2IjoiOWE5YzRmZjhiZjA3ZTFjNDE5M2ViODYyMjU2ZGQ0YjI3ZmM4YzYwNDczN2Q3OGU0ZDczNzg2YTNiMjMzYzMyOSJ9 -->
### `client.jobs.cancel`

Operation ID: `cancelJob`  
Route: `POST` `/v1/jobs/{jobId}/cancel`  
Equivalent member: `client.cancel_job`  

#### Signature

```python
client.jobs.cancel(job_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `jobId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | OK | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "jobId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.jobs.cancel('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJjYW5jZWxKb2IifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJqb2JzLmdldCIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6ImdldEpvYiIsInBhdGgiOiIvdjEvam9icy97am9iSWR9IiwicmVzb3VyY2UiOiJqb2JzIiwic2VjdGlvbl9zaGEyNTYiOiIxZWU5Nzg4NTcyODk2MDAxM2U3ODE0YzZhMmUxNzg5YTJlNjVjMzNlNjVmMDk2Y2E2NmYwMTdmMmVkNWZlYTU3Iiwic2lnbmF0dXJlX3NoYTI1NiI6IjRkYzkwOGJjMTA0MjkyN2I4NmMyZTNiZDVmNWIyNzA5NjM1YzQzMzMzZDc0MTY3ODU4NWY4NGEzYzg3MjljMjYifQ -->
### `client.jobs.get`

Operation ID: `getJob`  
Route: `GET` `/v1/jobs/{jobId}`  
Equivalent member: `client.get_job`  

#### Signature

```python
client.jobs.get(job_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `jobId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | OK | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "jobId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.jobs.get('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRKb2IifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJqb2JzLmxpc3RfZXZlbnRzIiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoibGlzdEpvYkV2ZW50cyIsInBhdGgiOiIvdjEvam9icy97am9iSWR9L2V2ZW50cyIsInJlc291cmNlIjoiam9icyIsInNlY3Rpb25fc2hhMjU2IjoiZTkyMTFiNDM5OTQwZGE2OGNlODk5Yzg1YzBlNGIwZDYzNDhkZjEyYjFkMzc4ZDU2Y2M4YmUyMDA2OTMyODVkMyIsInNpZ25hdHVyZV9zaGEyNTYiOiI4Mzc0M2ZlMDA1MjYxNTQyZWZhNjI1MTUyY2FmZTJlMjI3OTI1YmRiYTMzOTE4MmE0ZTEyNjIwNjNmOTgyMTY1In0 -->
### `client.jobs.list_events`

Operation ID: `listJobEvents`  
Route: `GET` `/v1/jobs/{jobId}/events`  
Equivalent member: `client.list_job_events`  

#### Signature

```python
client.jobs.list_events(job_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `jobId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | OK | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "jobId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.jobs.list_events('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0Sm9iRXZlbnRzIn0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJqb2JzLmxpc3QiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJsaXN0Sm9icyIsInBhdGgiOiIvdjEvam9icyIsInJlc291cmNlIjoiam9icyIsInNlY3Rpb25fc2hhMjU2IjoiM2I0MzI2ZjRlNTk2MThhNmUzNzJiYTJkM2Y5MmVjNWUxMmFjMjc2NjA4ZGRiYzQ3YjhlZTBjNzRjYTI5NjRjYSIsInNpZ25hdHVyZV9zaGEyNTYiOiIyYjJhNWRjOGUyNjAzNzdmYWIxNDA1ZjQ3Mzk2YTc5OGNjYmY3YWZjNDgwODNmMjYwMzYxZDcxODhhOGZlZGNjIn0 -->
### `client.jobs.list`

Operation ID: `listJobs`  
Route: `GET` `/v1/jobs`  
Equivalent member: `client.list_jobs`  

#### Signature

```python
client.jobs.list(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Jobs | none |
| `401` | Session required | none |
| `503` | Storage not configured | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.jobs.list()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0Sm9icyJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJqb2JzLnN1Ym1pdCIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJzdWJtaXRKb2IiLCJwYXRoIjoiL3YxL2pvYnMiLCJyZXNvdXJjZSI6ImpvYnMiLCJzZWN0aW9uX3NoYTI1NiI6ImY0YzE0MWJkZTc4Y2NjNjZmOWNmY2RkM2Q0MGI1YWQ3ZWQ5MDA0NmY5ZWZkODIxZTdhZDlhN2ZmNDI2NTYxNDUiLCJzaWduYXR1cmVfc2hhMjU2IjoiZjZhZDhlZTA1N2ZkYWJjYjJkODkwZTgzMDJiZjI5ODQ0MWZkZjAyOTcxZDNhNzk5NTZjNTZkOWJkZTg4OWE0OCJ9 -->
### `client.jobs.submit`

Operation ID: `submitJob`  
Route: `POST` `/v1/jobs`  
Equivalent member: `client.submit_job`  

#### Signature

```python
client.jobs.submit(body: dict[str, Any], *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Replayed | none |
| `201` | Created | none |
| `401` | Session required | none |
| `503` | Storage not configured | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.jobs.submit({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJzdWJtaXRKb2IifQ -->

## Resource `organizations`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmNsb3NlX3BlcnNpc3RlbnRfYm94IiwibWV0aG9kIjoiUE9TVCIsIm9wZXJhdGlvbl9pZCI6ImNsb3NlUGVyc2lzdGVudEJveCIsInBhdGgiOiIvdjEvb3JnYW5pemF0aW9ucy97b3JnYW5pemF0aW9uSWR9L3BlcnNpc3RlbnQtYm94ZXMve2JveElkfS9jbG9zZSIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiMzIzODk1Yzg4M2I3MDM2OWZiYzU4MzcwOWYyYTViOWJkMDJmNmFhN2YzOGM2OTdmOTEzOGM4OTg2ZjM5ZGQyZiIsInNpZ25hdHVyZV9zaGEyNTYiOiIyZDM0N2VhNDhhY2VkMWVlNDQxNzkzYjc4ZTU2OGU3Njk4YjY3YWFlOTIzZmNiNWI1MWEzY2M2Y2FjN2IxY2YzIn0 -->
### `client.organizations.close_persistent_box`

Operation ID: `closePersistentBox`  
Route: `POST` `/v1/organizations/{organizationId}/persistent-boxes/{boxId}/close`  
Equivalent member: `client.close_persistent_box`  

#### Signature

```python
client.organizations.close_persistent_box(organization_id: str, box_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> HostedPersistentBoxClose
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `boxId` | `path` | yes | `string&lt;uuid&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Closure is recorded; repeat requests return the same result without deleting again. | application/json (HostedPersistentBoxClose) |
| `202` | Closure is unconfirmed. Lost, late, negative or mismatched acknowledgements and failed receipt persistence retain reservations. Repeat requests never dispatch another deletion; operator reconciliation is required. | application/json (HostedPersistentBoxClose) |
| `400` | Invalid UUID, body or query parameters. | none |
| `401` | Missing or rejected product session. | none |
| `403` | Current authority denied cleanup or the organization/product/environment differs. | none |
| `404` | No durable box in this exact target scope. | none |
| `409` | Unconfirmed or changed provider allocation requires operator reconciliation. | none |
| `503` | Authority or storage unavailable, or no matching operator provider adapter. Missing configuration refuses before any close intention or deletion. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "boxId",
      "value": "00000000-0000-0000-c54d-988d0e4e7e77"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.close_persistent_box('example', '00000000-0000-0000-c54d-988d0e4e7e77')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJjbG9zZVBlcnNpc3RlbnRCb3gifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmNyZWF0ZV9iaWxsaW5nX3BvcnRhbCIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJjcmVhdGVCaWxsaW5nUG9ydGFsIiwicGF0aCI6Ii92MS9vcmdhbml6YXRpb25zL3tvcmdhbml6YXRpb25JZH0vYmlsbGluZy9wb3J0YWwiLCJyZXNvdXJjZSI6Im9yZ2FuaXphdGlvbnMiLCJzZWN0aW9uX3NoYTI1NiI6IjIxODMxY2RjMTU4YTU0NTRkZjQ1ZWI2NzQzNzFmYjViOTdjODdhMjk4OGQ0ZTMyYWE5NjI0MTE4MWY1YWM3YjgiLCJzaWduYXR1cmVfc2hhMjU2IjoiNDM4YzVkZmFjNzkwMmZmNGJlMGI5MWE3NGFkMjBmZTMyN2ViZTJiMGQ0MzE5MzU1MmViODI5YTBmMGY1NGM1NyJ9 -->
### `client.organizations.create_billing_portal`

Operation ID: `createBillingPortal`  
Route: `POST` `/v1/organizations/{organizationId}/billing/portal`  
Equivalent member: `client.create_billing_portal`  

#### Signature

```python
client.organizations.create_billing_portal(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `201` | portalUrl | none |
| `404` | No Stripe customer yet | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.create_billing_portal('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJjcmVhdGVCaWxsaW5nUG9ydGFsIn0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmNyZWF0ZV9ib3giLCJtZXRob2QiOiJQT1NUIiwib3BlcmF0aW9uX2lkIjoiY3JlYXRlQm94IiwicGF0aCI6Ii92MS9vcmdhbml6YXRpb25zL3tvcmdhbml6YXRpb25JZH0vYm94ZXMiLCJyZXNvdXJjZSI6Im9yZ2FuaXphdGlvbnMiLCJzZWN0aW9uX3NoYTI1NiI6ImE1MWY1N2UwZTJhN2ExNmQ0MjA2Njk1NDM1Y2FlNjFiYmVkZmNlNjRkNGI2N2M5NTgxYmNjMzUwZDRjMjUxYmYiLCJzaWduYXR1cmVfc2hhMjU2IjoiMTEyOWRhNmIyNTA4NDcxZjk4ZGRhMWRkMzRmMWZhZDgzMTE4ZDM3NDUyYzRiZWQxODU0MDk1ZTFjOWZlNTA3NCJ9 -->
### `client.organizations.create_box`

Operation ID: `createBox`  
Route: `POST` `/v1/organizations/{organizationId}/boxes`  
Equivalent member: `client.create_box`  

#### Signature

```python
client.organizations.create_box(organization_id: str, body: CreateBoxBody, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `201` | Box running at the provider | none |
| `402` | Concurrent-box limit reached | none |
| `502` | The provider refused; recorded as failed | none |
| `503` | No provider or no storage | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.create_box('example', {}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJjcmVhdGVCb3gifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmNyZWF0ZV9jaGVja291dCIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJjcmVhdGVDaGVja291dCIsInBhdGgiOiIvdjEvb3JnYW5pemF0aW9ucy97b3JnYW5pemF0aW9uSWR9L2JpbGxpbmcvY2hlY2tvdXQiLCJyZXNvdXJjZSI6Im9yZ2FuaXphdGlvbnMiLCJzZWN0aW9uX3NoYTI1NiI6IjVjMmE0ZTA0NjAzNGQ2NmMwMDQ2NGY5MjBhOWQ4YzJmMWRjOGRlNmZlZDQ4MjEyMzhjYzhmMmU5OWRiNzQ1YjUiLCJzaWduYXR1cmVfc2hhMjU2IjoiNGJjZTYyZmU0NjJkMzJkMjJiNTUzZWU3ZmYzMGQ1ZTYwMTMxNjMxMGU5ZDY3MDU1NDJmNWQ4NDliZjIwNGRjYyJ9 -->
### `client.organizations.create_checkout`

Operation ID: `createCheckout`  
Route: `POST` `/v1/organizations/{organizationId}/billing/checkout`  
Equivalent member: `client.create_checkout`  

#### Signature

```python
client.organizations.create_checkout(organization_id: str, body: CreateCheckoutBody, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `201` | checkoutUrl of the Stripe Checkout Session | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. Autonomous mode: Plan not on sale or subscription exists | none |

#### Canonical required-input example

```json
{
  "body": {
    "planKey": "pro"
  },
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.create_checkout('example', {'planKey': 'pro'}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJjcmVhdGVDaGVja291dCJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmdldF9iaWxsaW5nIiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoiZ2V0QmlsbGluZyIsInBhdGgiOiIvdjEvb3JnYW5pemF0aW9ucy97b3JnYW5pemF0aW9uSWR9L2JpbGxpbmciLCJyZXNvdXJjZSI6Im9yZ2FuaXphdGlvbnMiLCJzZWN0aW9uX3NoYTI1NiI6IjFmNWJhNTkzNjBjNjVjZDQzNzUxMjM0YmM3Yzk3MmM0MTRlN2RiYzcwNjU3YTdlNTc4N2NkMWVjM2MzZjBhMTAiLCJzaWduYXR1cmVfc2hhMjU2IjoiMTY2NjVmM2IxZjIzYTYxMmMzZjVlYTFjNzExY2JlNTI1YmU0MDQzZTRmYzI5MzdkNWY2NzYwZjlmMWRhYjZhOCJ9 -->
### `client.organizations.get_billing`

Operation ID: `getBilling`  
Route: `GET` `/v1/organizations/{organizationId}/billing`  
Equivalent member: `client.get_billing`  

#### Signature

```python
client.organizations.get_billing(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Billing status | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.get_billing('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRCaWxsaW5nIn0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmdldF9ib3giLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJnZXRCb3giLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9ib3hlcy97Ym94SWR9IiwicmVzb3VyY2UiOiJvcmdhbml6YXRpb25zIiwic2VjdGlvbl9zaGEyNTYiOiJiMGY2NThkZmE2YzE3ZDQxNDM5YzE4ZWNiYzgyYWIwZTZlOGRhODczOWJkMjgwZDhhYzg2ZTkwNmM0N2UzNTg4Iiwic2lnbmF0dXJlX3NoYTI1NiI6ImFhYjYyMGIyMjY5M2Q4Y2QwYWRkY2QzNmQ2MTRiZDM3NDMyMmZhNTA3MTQ4YzhhYzNjYjE3NTMyNGQ4ZmNkNzYifQ -->
### `client.organizations.get_box`

Operation ID: `getBox`  
Route: `GET` `/v1/organizations/{organizationId}/boxes/{boxId}`  
Equivalent member: `client.get_box`  

#### Signature

```python
client.organizations.get_box(organization_id: str, box_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `boxId` | `path` | yes | `string&lt;uuid&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Stored box | none |
| `404` | Unknown box | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "boxId",
      "value": "00000000-0000-0000-d32a-0e84cb70d88a"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.get_box('example', '00000000-0000-0000-d32a-0e84cb70d88a')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRCb3gifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmdldF9lbnRpdGxlbWVudHMiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJnZXRFbnRpdGxlbWVudHMiLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9lbnRpdGxlbWVudHMiLCJyZXNvdXJjZSI6Im9yZ2FuaXphdGlvbnMiLCJzZWN0aW9uX3NoYTI1NiI6IjVlMjZmYzkyYjZiOTQzODZmMDdmMzcyY2I3NmNhN2ViMmRhMDBjM2ZlYjRmNDI3ZWE5ZWI2ODdlYjEzYzEzMjQiLCJzaWduYXR1cmVfc2hhMjU2IjoiMTVlYTZmZjNlMmZhNjA4NjRjZWM4MDU5MTdhZDVhYTI4MGJjY2E4MmE1ZTMwNjgyMjhkOGNlMGZjNzkwYzllNiJ9 -->
### `client.organizations.get_entitlements`

Operation ID: `getEntitlements`  
Route: `GET` `/v1/organizations/{organizationId}/entitlements`  
Equivalent member: `client.get_entitlements`  

#### Signature

```python
client.organizations.get_entitlements(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Entitlements and usage | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.get_entitlements('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRFbnRpdGxlbWVudHMifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmdldF9mbGVldCIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6ImdldEZsZWV0IiwicGF0aCI6Ii92MS9vcmdhbml6YXRpb25zL3tvcmdhbml6YXRpb25JZH0vZmxlZXQiLCJyZXNvdXJjZSI6Im9yZ2FuaXphdGlvbnMiLCJzZWN0aW9uX3NoYTI1NiI6IjExMTJhZjM3NTExMjE2YTBjODA2MzhhNzY3ZDgxMzA4ZWZlN2U3ZTRkNTUxNGRhYjhkMjk0YWEwYTkzMzIyNGIiLCJzaWduYXR1cmVfc2hhMjU2IjoiYTNiNWRjN2RlMTRiNzllOTAxOWQyMWZmOWE3NDEzZmEzM2NkOGVjMzRmOTkzNjUzZGJmYTJhYWU5Yzk2Y2FjYyJ9 -->
### `client.organizations.get_fleet`

Operation ID: `getFleet`  
Route: `GET` `/v1/organizations/{organizationId}/fleet`  
Equivalent member: `client.get_fleet`  

#### Signature

```python
client.organizations.get_fleet(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Stored fleet | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.get_fleet('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRGbGVldCJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmdldF9mbGVldF9wb2xpY3kiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJnZXRGbGVldFBvbGljeSIsInBhdGgiOiIvdjEvb3JnYW5pemF0aW9ucy97b3JnYW5pemF0aW9uSWR9L2ZsZWV0L3BvbGljeSIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiMjgxODljMzVhOTcwNDNhZTRlYmEyYjcyZWQ2M2I0ZGNjMTU4NDQ2ZjNmOGJjNDFmZDFjYTg1MGIxZGExZjY5MCIsInNpZ25hdHVyZV9zaGEyNTYiOiI2MmU0MWViNDUwYWE1Yzg5ZjkzYjY4ODhhNzJkNTg0ZTc3NDNmYWVjZDQ0NjA3MTI5Y2VjN2I4NWI0ZGZhNjgzIn0 -->
### `client.organizations.get_fleet_policy`

Operation ID: `getFleetPolicy`  
Route: `GET` `/v1/organizations/{organizationId}/fleet/policy`  
Equivalent member: `client.get_fleet_policy`  

#### Signature

```python
client.organizations.get_fleet_policy(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Effective policy | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.get_fleet_policy('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRGbGVldFBvbGljeSJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmdldF9wZXJzaXN0ZW50X2JveCIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6ImdldFBlcnNpc3RlbnRCb3giLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9wZXJzaXN0ZW50LWJveGVzL3tib3hJZH0iLCJyZXNvdXJjZSI6Im9yZ2FuaXphdGlvbnMiLCJzZWN0aW9uX3NoYTI1NiI6ImM1NjhjYjliYjI3ZDA0ZDlkMzFjYTAzNzM4NmE5ZjJhZmEyODJkMzc5OTI3YzM5ZTk1OGY3M2UwNzAyZDA5YTIiLCJzaWduYXR1cmVfc2hhMjU2IjoiYzBmMjM1N2Q1MzY0NmFiZDAyNDAwMTgzNTRjNzRhMTdiYWNlMDhmNWYwNzk2OGNkNzIyNWE5NmIyNGRiNTUyMSJ9 -->
### `client.organizations.get_persistent_box`

Operation ID: `getPersistentBox`  
Route: `GET` `/v1/organizations/{organizationId}/persistent-boxes/{boxId}`  
Equivalent member: `client.get_persistent_box`  

#### Signature

```python
client.organizations.get_persistent_box(organization_id: str, box_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `boxId` | `path` | yes | `string&lt;uuid&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Private stored record and reserved budget; runtime status is not-metered. | application/json (object) |
| `400` | Invalid UUID or query parameters. | none |
| `401` | Missing or rejected product session. | none |
| `403` | Current authority denied access or the organization/product/environment differs. | none |
| `404` | No durable box in this exact target scope. | none |
| `503` | Authority or durable record storage unavailable. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "boxId",
      "value": "00000000-0000-0000-098c-d4f2b24057fb"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.get_persistent_box('example', '00000000-0000-0000-098c-d4f2b24057fb')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRQZXJzaXN0ZW50Qm94In0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmdldF9wZXJzaXN0ZW50X2JveF9wcm92aWRlcl91c2FnZSIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6ImdldFBlcnNpc3RlbnRCb3hQcm92aWRlclVzYWdlIiwicGF0aCI6Ii92MS9vcmdhbml6YXRpb25zL3tvcmdhbml6YXRpb25JZH0vcGVyc2lzdGVudC1ib3hlcy97Ym94SWR9L3VzYWdlIiwicmVzb3VyY2UiOiJvcmdhbml6YXRpb25zIiwic2VjdGlvbl9zaGEyNTYiOiJjNGJjOWNiZWM3MzI3ZTBjMjQ1NzY1NjUxMjZmYTFhZTZkNWI2NzAyNzYzNGEyNzA2MDFlYzA3ZWQxZjQ3YTgxIiwic2lnbmF0dXJlX3NoYTI1NiI6IjFjYWQwYWE4NzQ3NjA4NThiM2U0MTA0ODRjMGJhNjRiNzNiMjU0YmQ4NGQ5OGY2ZGRiZWViZDYyZDA0NjczNTYifQ -->
### `client.organizations.get_persistent_box_provider_usage`

Operation ID: `getPersistentBoxProviderUsage`  
Route: `GET` `/v1/organizations/{organizationId}/persistent-boxes/{boxId}/usage`  
Equivalent member: `client.get_persistent_box_provider_usage`  

#### Signature

```python
client.organizations.get_persistent_box_provider_usage(organization_id: str, box_id: str, from_: str, to: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `boxId` | `path` | yes | `string&lt;uuid&gt;` |  |
| `from` | `query` | yes | `string&lt;date-time&gt;` |  |
| `to` | `query` | yes | `string&lt;date-time&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Private provider evidence summary with explicit interval coverage. | application/json (object) |
| `400` | Invalid box ID or bounded UTC window. | none |
| `401` | Missing or rejected product session. | none |
| `403` | Current authority denied access or target scope differs. | none |
| `404` | No durable box in this exact target scope. | none |
| `413` | Stored evidence exceeds the per-read record bound; select a smaller window. | none |
| `503` | Authority or usage storage unavailable. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "boxId",
      "value": "00000000-0000-0000-0848-7a89fcbe4ab4"
    },
    {
      "in": "query",
      "name": "from",
      "value": "2026-01-01T00:00:00Z"
    },
    {
      "in": "query",
      "name": "to",
      "value": "2026-01-01T00:00:27Z"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.get_persistent_box_provider_usage('example', '00000000-0000-0000-0848-7a89fcbe4ab4', '2026-01-01T00:00:00Z', '2026-01-01T00:00:27Z')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRQZXJzaXN0ZW50Qm94UHJvdmlkZXJVc2FnZSJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmxpc3RfYm94ZXMiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJsaXN0Qm94ZXMiLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9ib3hlcyIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiZTg5YmNhNjZiODZiZTY2NjA0NGQzMTU5NDZkZjg3NDY0YmIxOTNjYmI4NWEyZTcxNTEwZjE4YzQwNmJhMjA1OSIsInNpZ25hdHVyZV9zaGEyNTYiOiI2OTkzZjVmNTYwYzdiNWNjMTg1MmJiMmU3NjVkNzk2Y2NhMTM3OTA0NTNkMWE1NDVjNjZkZjJmYzg2YjZjY2UzIn0 -->
### `client.organizations.list_boxes`

Operation ID: `listBoxes`  
Route: `GET` `/v1/organizations/{organizationId}/boxes`  
Equivalent member: `client.list_boxes`  

#### Signature

```python
client.organizations.list_boxes(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Stored boxes with their provider state | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.list_boxes('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0Qm94ZXMifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmxpc3RfaW52b2ljZXMiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJsaXN0SW52b2ljZXMiLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9iaWxsaW5nL2ludm9pY2VzIiwicmVzb3VyY2UiOiJvcmdhbml6YXRpb25zIiwic2VjdGlvbl9zaGEyNTYiOiJjNTg3Nzc0MTc4YzQ4OTVjMDdkMjAzZTIxNDMwOWY4Y2VjOGUyYzQ0MzdmYWI0YjU3MTljZmY0ODBmMjg2NDQ5Iiwic2lnbmF0dXJlX3NoYTI1NiI6ImQxYjg4YTc0NmQ4NzkxOGE2NzI4NWQ2Zjg3OTkzYWI3MmFjMWQxYmQwMDEzOGNiYmEzZGJjM2M3NWRmMTRlYTEifQ -->
### `client.organizations.list_invoices`

Operation ID: `listInvoices`  
Route: `GET` `/v1/organizations/{organizationId}/billing/invoices`  
Equivalent member: `client.list_invoices`  

#### Signature

```python
client.organizations.list_invoices(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Invoices | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.list_invoices('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0SW52b2ljZXMifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmxpc3RfbWVtYmVycyIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6Imxpc3RNZW1iZXJzIiwicGF0aCI6Ii92MS9vcmdhbml6YXRpb25zL3tvcmdhbml6YXRpb25JZH0vbWVtYmVycyIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiMTVhMGRmNDNiZDAxMTQ0ZGFlOTk1MzhjNTA5ZjQzNjIwOWY3YTM3NDYxOGNiNWE0MTc4OTBmNjViYzE3ZmRiOSIsInNpZ25hdHVyZV9zaGEyNTYiOiJjZmE0YzlkMGM3MmE1MDI5Nzc4Mjg0ZGU5MTAzMGU2MTIwMDliNWY2YTBjOWUzZWU1NDhiODE2MTMzOTBhOThmIn0 -->
### `client.organizations.list_members`

Operation ID: `listMembers`  
Route: `GET` `/v1/organizations/{organizationId}/members`  
Equivalent member: `client.list_members`  

#### Signature

```python
client.organizations.list_members(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Stored members and the plan seat limit | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.list_members('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0TWVtYmVycyJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmxpc3Rfb2JzZXJ2ZWRfYm94ZXMiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJsaXN0T2JzZXJ2ZWRCb3hlcyIsInBhdGgiOiIvdjEvb3JnYW5pemF0aW9ucy97b3JnYW5pemF0aW9uSWR9L29ic2VydmVkLWJveGVzIiwicmVzb3VyY2UiOiJvcmdhbml6YXRpb25zIiwic2VjdGlvbl9zaGEyNTYiOiIzNDZkN2NhMDY0ZDkxNmVkZTkzNmFiMDBmMWYzZGU3NmMxZmNiN2QwMjZhYmY3OWJkZDA2YzY1ZTMxNWNhNGY4Iiwic2lnbmF0dXJlX3NoYTI1NiI6ImU1Y2Y2ZmIxYzUwNzExOTdiNTE4ZTk2NGMzYWVmOWU4MTcxMDMxYTRiM2QwYjEwNTY3ZGJmM2U4YzU4ZjdiZjkifQ -->
### `client.organizations.list_observed_boxes`

Operation ID: `listObservedBoxes`  
Route: `GET` `/v1/organizations/{organizationId}/observed-boxes`  
Equivalent member: `client.list_observed_boxes`  

#### Signature

```python
client.organizations.list_observed_boxes(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Up to 100 non-expired client snapshots, private and not cacheable. | application/json (object) |
| `401` | No valid product session. | none |
| `403` | Organization or scope denied. | none |
| `503` | Inventory storage unavailable. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.list_observed_boxes('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0T2JzZXJ2ZWRCb3hlcyJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmxpc3RfcGVyc2lzdGVudF9ib3hfb2ZmZXJzIiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoibGlzdFBlcnNpc3RlbnRCb3hPZmZlcnMiLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9wZXJzaXN0ZW50LWJveGVzL29mZmVycyIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiNjdhZWNmY2RjMDYxYTE5YjI4ODY3M2M0ZDIwZmVjM2Y1MGU4NTc2Mjk1MjZlYjViOWE0MDdmM2UyZTY4YmFmZCIsInNpZ25hdHVyZV9zaGEyNTYiOiI1OWQ1Y2E1ZjhjNGQ3NDQ0YTdjNDU1ODFhOGZiOWMzZTJlZmUwOGY3YWVhZjhlZjE0YzQ1MWQwMTI2M2ExNTdjIn0 -->
### `client.organizations.list_persistent_box_offers`

Operation ID: `listPersistentBoxOffers`  
Route: `GET` `/v1/organizations/{organizationId}/persistent-boxes/offers`  
Equivalent member: `client.list_persistent_box_offers`  

#### Signature

```python
client.organizations.list_persistent_box_offers(organization_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Private configured offers. | application/json (object) |
| `401` | Product session required. | none |
| `403` | Current read authority denied. | none |
| `503` | Storage or operator offer configuration unavailable. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.list_persistent_box_offers('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0UGVyc2lzdGVudEJveE9mZmVycyJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLmxpc3RfcGVyc2lzdGVudF9ib3hlcyIsIm1ldGhvZCI6IkdFVCIsIm9wZXJhdGlvbl9pZCI6Imxpc3RQZXJzaXN0ZW50Qm94ZXMiLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9wZXJzaXN0ZW50LWJveGVzIiwicmVzb3VyY2UiOiJvcmdhbml6YXRpb25zIiwic2VjdGlvbl9zaGEyNTYiOiI1Yzg2Y2NjODlmYWRlNzk5YzU1MWNmZjQ4M2JhODBiMjAwZGNmODAyZDM2YTEzNmZhZWNjYzJlODZmNzY1M2QwIiwic2lnbmF0dXJlX3NoYTI1NiI6IjRjZTIwOGU4ZDQ0YjBhNzM3NTA5ZDdlNTY3NGNlMmQ4YjNjNDJhMGY2YjUwNGI2NGVmMDA0NjM5Zjg0YzY5MWIifQ -->
### `client.organizations.list_persistent_boxes`

Operation ID: `listPersistentBoxes`  
Route: `GET` `/v1/organizations/{organizationId}/persistent-boxes`  
Equivalent member: `client.list_persistent_boxes`  

#### Signature

```python
client.organizations.list_persistent_boxes(organization_id: str, limit: Optional[int] = None, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `limit` | `query` | no | `integer` | Maximum recent records; duplicates and other query parameters are rejected. |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Bounded stored records, private and not cacheable. limitReached indicates the requested bound was filled, not an exact total or proof that more records exist. | application/json (object) |
| `400` | Invalid query parameters. | none |
| `401` | Missing or rejected product session. | none |
| `403` | Current authority denied access or the organization/product/environment differs. | none |
| `503` | Authority or durable record storage unavailable. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.list_persistent_boxes('example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0UGVyc2lzdGVudEJveGVzIn0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnByb3Zpc2lvbl9wZXJzaXN0ZW50X2JveCIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJwcm92aXNpb25QZXJzaXN0ZW50Qm94IiwicGF0aCI6Ii92MS9vcmdhbml6YXRpb25zL3tvcmdhbml6YXRpb25JZH0vcGVyc2lzdGVudC1ib3hlcyIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiODdhMGIxN2Q2YTgyN2ZiN2FkYjQzM2Q1YWYyMmE1NzRjNDg5YWI5YmMyM2M3OTk5ODY2NWM0OTZkYzU2NDU1NiIsInNpZ25hdHVyZV9zaGEyNTYiOiI2ZThjYjNiYWVhMzJhOTY0NzJiZTZiOTA4OTQ2ZGEzY2Y5MDVkZWE3MjA3ZDI2YTY2YTQ1ZGIyNGY3MWRmYTA4In0 -->
### `client.organizations.provision_persistent_box`

Operation ID: `provisionPersistentBox`  
Route: `POST` `/v1/organizations/{organizationId}/persistent-boxes`  
Equivalent member: `client.provision_persistent_box`  

#### Signature

```python
client.organizations.provision_persistent_box(organization_id: str, body: ProvisionPersistentBoxBody, idempotency_key_2: Optional[str] = None, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> Union[None, dict[str, Any]]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `Idempotency-Key` | `header` | no | `string` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Previously recorded running or closed allocation; replayed is true. | none |
| `201` | Provider allocation confirmed and recorded as running. Runtime remains reserved, not measured. | application/json (object) |
| `202` | The reservation is held and the allocation remains unconfirmed. Repeated requests never dispatch create again; operator reconciliation is required. | none |
| `400` | Invalid body, unsupported fields, query parameters or idempotency key. | none |
| `401` | Missing or rejected product session. | none |
| `402` | Missing durable entitlement, bounded allowance or available capacity. | none |
| `403` | Current authority denied the operation or target scope. | none |
| `409` | Idempotency conflict, unresolved prior budget or UTC month boundary. | none |
| `413` | Request body exceeds 4 KiB. | none |
| `503` | Authority, storage, operator offer or independent runtime enforcement unavailable. Missing configuration is refused before reservation. | none |

#### Canonical required-input example

```json
{
  "body": {
    "offer": "example",
    "reserveMinutes": 1
  },
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.provision_persistent_box('example', {'offer': 'example', 'reserveMinutes': 1}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJwcm92aXNpb25QZXJzaXN0ZW50Qm94In0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnB1dF9mbGVldF9wb2xpY3kiLCJtZXRob2QiOiJQVVQiLCJvcGVyYXRpb25faWQiOiJwdXRGbGVldFBvbGljeSIsInBhdGgiOiIvdjEvb3JnYW5pemF0aW9ucy97b3JnYW5pemF0aW9uSWR9L2ZsZWV0L3BvbGljeSIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiNTA0MTY4NTA2ZGJmZjlmOTM5MWE4ZGUwNWI3ZmE2ZWQ1MDQ4OGM4MTAzZjI5MmMzMDljMDdhMmEyNjIyOWRiNiIsInNpZ25hdHVyZV9zaGEyNTYiOiI2Yjc3YjA5NzljMmQ4MGUyNzYyMWJiZGVmODdjYzFmMjM2NGYyODhhYzk4YzNhOTFkZjFhZmEzYmNhZGIwNzA0In0 -->
### `client.organizations.put_fleet_policy`

Operation ID: `putFleetPolicy`  
Route: `PUT` `/v1/organizations/{organizationId}/fleet/policy`  
Equivalent member: `client.put_fleet_policy`  

#### Signature

```python
client.organizations.put_fleet_policy(organization_id: str, body: PutFleetPolicyBody, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Stored policy | none |
| `400` | Invalid or unenforced field | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.put_fleet_policy('example', {}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJwdXRGbGVldFBvbGljeSJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnJlY29uY2lsZV9wZXJzaXN0ZW50X2JveCIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJyZWNvbmNpbGVQZXJzaXN0ZW50Qm94IiwicGF0aCI6Ii92MS9vcmdhbml6YXRpb25zL3tvcmdhbml6YXRpb25JZH0vcGVyc2lzdGVudC1ib3hlcy97Ym94SWR9L3JlY29uY2lsZSIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiZGMzMjc5YjAyZGIwYzViNGRlZDFjMDBmMTA5YTU2Zjc2Zjc4M2JmMzkyNTEzYmRkNDI0NDY4NGExNTNmNWY2NiIsInNpZ25hdHVyZV9zaGEyNTYiOiIxNjZkYTJhYWRlMzdmZjM5ZWFlNmM0MTZmZDRhNGJlY2JlYTQzODgxZjFkNGM5YWE5YmFkODI3ZmRjZThmYjJmIn0 -->
### `client.organizations.reconcile_persistent_box`

Operation ID: `reconcilePersistentBox`  
Route: `POST` `/v1/organizations/{organizationId}/persistent-boxes/{boxId}/reconcile`  
Equivalent member: `client.reconcile_persistent_box`  

#### Signature

```python
client.organizations.reconcile_persistent_box(organization_id: str, box_id: str, body: ReconcilePersistentBoxBody, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `boxId` | `path` | yes | `string&lt;uuid&gt;` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Confirmed operation or replayed receipt. | application/json (object) |
| `202` | Operation remains unconfirmed; reconcile its operation ID without repeating the mutation. | application/json (object) |
| `400` | Invalid bounded lifecycle request. | none |
| `401` | Product session required. | none |
| `402` | Durable feature or quota denied. | none |
| `403` | Fresh operation authority denied. | none |
| `404` | Box or operation missing in the exact organization and deployment. | none |
| `409` | Conflicting operation, unresolved evidence or unavailable runtime budget. | none |
| `503` | Authority, storage or matching operator adapter unavailable. | none |

#### Canonical required-input example

```json
{
  "body": {
    "operationId": "00000000-0000-0000-f735-3d332872b96e"
  },
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "boxId",
      "value": "00000000-0000-0000-a264-3ce9cdfbbeff"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.reconcile_persistent_box('example', '00000000-0000-0000-a264-3ce9cdfbbeff', {'operationId': '00000000-0000-0000-f735-3d332872b96e'}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJyZWNvbmNpbGVQZXJzaXN0ZW50Qm94In0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnJlbW92ZV9tZW1iZXIiLCJtZXRob2QiOiJERUxFVEUiLCJvcGVyYXRpb25faWQiOiJyZW1vdmVNZW1iZXIiLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9tZW1iZXJzL3t1c2VySWR9IiwicmVzb3VyY2UiOiJvcmdhbml6YXRpb25zIiwic2VjdGlvbl9zaGEyNTYiOiJiMDljOGUzMjViYmUwY2Q1MWRjYWFhMjU5YWY5MjU2ZDBmNDgxNWJlYjY4ZTU4MDdmMGIzNzZjNjYyYTQwMzEzIiwic2lnbmF0dXJlX3NoYTI1NiI6ImRiNTg4Mzg3MDhmOTdhNWI2Y2UzOGExZjE1NzlhZmFmMjMwN2I2MTQwMzg5MDRmZjkzNmNhYmMxYmM0MDFmMzcifQ -->
### `client.organizations.remove_member`

Operation ID: `removeMember`  
Route: `DELETE` `/v1/organizations/{organizationId}/members/{userId}`  
Equivalent member: `client.remove_member`  

#### Signature

```python
client.organizations.remove_member(organization_id: str, user_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `userId` | `path` | yes | `string` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Removed | none |
| `404` | Unknown member | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "userId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.remove_member('example', 'example')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJyZW1vdmVNZW1iZXIifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnN0YXJ0X3BlcnNpc3RlbnRfYm94IiwibWV0aG9kIjoiUE9TVCIsIm9wZXJhdGlvbl9pZCI6InN0YXJ0UGVyc2lzdGVudEJveCIsInBhdGgiOiIvdjEvb3JnYW5pemF0aW9ucy97b3JnYW5pemF0aW9uSWR9L3BlcnNpc3RlbnQtYm94ZXMve2JveElkfS9zdGFydCIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiZTUyNGNmMWRiMGIzOWFmMTM5M2QwOGQ2NDI1ZDQ2ODViODU4MmMyYTE0ZDk2NWI4ODEzOTk3MmQ5YmNkZjY2ZCIsInNpZ25hdHVyZV9zaGEyNTYiOiJlNWU3ZWNjYzM0NTk4NTVjZTVmYTNjY2ViZTk1NzM3NWU1ZjVhNjA3YmJjMjVjZWVmODQ2OGM1NGFlN2U3YmY4In0 -->
### `client.organizations.start_persistent_box`

Operation ID: `startPersistentBox`  
Route: `POST` `/v1/organizations/{organizationId}/persistent-boxes/{boxId}/start`  
Equivalent member: `client.start_persistent_box`  

#### Signature

```python
client.organizations.start_persistent_box(organization_id: str, box_id: str, body: StartPersistentBoxBody, idempotency_key_2: Optional[str] = None, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `boxId` | `path` | yes | `string&lt;uuid&gt;` |  |
| `Idempotency-Key` | `header` | no | `string` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Confirmed operation or replayed receipt. | application/json (object) |
| `202` | Operation remains unconfirmed; reconcile its operation ID without repeating the mutation. | application/json (object) |
| `400` | Invalid bounded lifecycle request. | none |
| `401` | Product session required. | none |
| `402` | Durable feature or quota denied. | none |
| `403` | Fresh operation authority denied. | none |
| `404` | Box or operation missing in the exact organization and deployment. | none |
| `409` | Conflicting operation, unresolved evidence or unavailable runtime budget. | none |
| `503` | Authority, storage or matching operator adapter unavailable. | none |

#### Canonical required-input example

```json
{
  "body": {
    "reserveMinutes": 1
  },
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "boxId",
      "value": "00000000-0000-0000-d7e8-d81c5e30ed9a"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.start_persistent_box('example', '00000000-0000-0000-d7e8-d81c5e30ed9a', {'reserveMinutes': 1}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJzdGFydFBlcnNpc3RlbnRCb3gifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnN0b3BfYm94IiwibWV0aG9kIjoiREVMRVRFIiwib3BlcmF0aW9uX2lkIjoic3RvcEJveCIsInBhdGgiOiIvdjEvb3JnYW5pemF0aW9ucy97b3JnYW5pemF0aW9uSWR9L2JveGVzL3tib3hJZH0iLCJyZXNvdXJjZSI6Im9yZ2FuaXphdGlvbnMiLCJzZWN0aW9uX3NoYTI1NiI6IjVhZTUzODY1YjE5MzZmNzFlYWZkZDJiNThhNGE4MmYwZDU5YTEwMDA0NWM3YWY1MDk3ZjMxNDM4NjViMDE1MTciLCJzaWduYXR1cmVfc2hhMjU2IjoiMWIyZTM2NzQwNzJhZTQ5YjI4NDFjZTcwNGUzY2VhYmJjNGRiZDZmMjlkY2I0MGNmZWQyM2MyMWZiMzQwN2ZjNSJ9 -->
### `client.organizations.stop_box`

Operation ID: `stopBox`  
Route: `DELETE` `/v1/organizations/{organizationId}/boxes/{boxId}`  
Equivalent member: `client.stop_box`  

#### Signature

```python
client.organizations.stop_box(organization_id: str, box_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `boxId` | `path` | yes | `string&lt;uuid&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Stopped | none |
| `502` | The provider refused; state unchanged | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "boxId",
      "value": "00000000-0000-0000-265e-7c895c60153e"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.stop_box('example', '00000000-0000-0000-265e-7c895c60153e')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJzdG9wQm94In0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnN0b3BfcGVyc2lzdGVudF9ib3giLCJtZXRob2QiOiJQT1NUIiwib3BlcmF0aW9uX2lkIjoic3RvcFBlcnNpc3RlbnRCb3giLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9wZXJzaXN0ZW50LWJveGVzL3tib3hJZH0vc3RvcCIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiMWU2YmZkZDcxOWExNjljMGVmMjM5MzcyOGI5NjZlMTcwODA2MTE4NmM1NDNhODQ5ODM3MzViNzAxM2ZkOTdlMCIsInNpZ25hdHVyZV9zaGEyNTYiOiJlODk2MmYzMzMxOTNlOTE5MGJmMjhiNGM0OWY1NWVjMDMzOTljODQxMzljZGU5Y2YwZmIxMGQ5Zjk1ZWE0ODg2In0 -->
### `client.organizations.stop_persistent_box`

Operation ID: `stopPersistentBox`  
Route: `POST` `/v1/organizations/{organizationId}/persistent-boxes/{boxId}/stop`  
Equivalent member: `client.stop_persistent_box`  

#### Signature

```python
client.organizations.stop_persistent_box(organization_id: str, box_id: str, body: StopPersistentBoxBody, idempotency_key_2: Optional[str] = None, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `boxId` | `path` | yes | `string&lt;uuid&gt;` |  |
| `Idempotency-Key` | `header` | no | `string` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Confirmed operation or replayed receipt. | application/json (object) |
| `202` | Operation remains unconfirmed; reconcile its operation ID without repeating the mutation. | application/json (object) |
| `400` | Invalid bounded lifecycle request. | none |
| `401` | Product session required. | none |
| `402` | Durable feature or quota denied. | none |
| `403` | Fresh operation authority denied. | none |
| `404` | Box or operation missing in the exact organization and deployment. | none |
| `409` | Conflicting operation, unresolved evidence or unavailable runtime budget. | none |
| `503` | Authority, storage or matching operator adapter unavailable. | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    },
    {
      "in": "path",
      "name": "boxId",
      "value": "00000000-0000-0000-978f-a93165cf6579"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.stop_persistent_box('example', '00000000-0000-0000-978f-a93165cf6579', {}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJzdG9wUGVyc2lzdGVudEJveCJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnN5bmNfb2JzZXJ2ZWRfYm94ZXMiLCJtZXRob2QiOiJQT1NUIiwib3BlcmF0aW9uX2lkIjoic3luY09ic2VydmVkQm94ZXMiLCJwYXRoIjoiL3YxL29yZ2FuaXphdGlvbnMve29yZ2FuaXphdGlvbklkfS9vYnNlcnZlZC1ib3hlcy9zeW5jIiwicmVzb3VyY2UiOiJvcmdhbml6YXRpb25zIiwic2VjdGlvbl9zaGEyNTYiOiJmMDZiMjE5YjE1NTBmNmZiZmZmZTZhMTY5MmFlMDdmNGUxZmExM2I5YThjN2NmYTkzNzk4YzFmMjU5YjA3ZTAzIiwic2lnbmF0dXJlX3NoYTI1NiI6Ijk1MzQ3OTc2NWY5YWIyNTRmZjlhMWRlMWVmMzZmNjFhOGU3NWNlNzViMmY4MjE0ZDQzMTRmN2VlYzM0NmQ5MTcifQ -->
### `client.organizations.sync_observed_boxes`

Operation ID: `syncObservedBoxes`  
Route: `POST` `/v1/organizations/{organizationId}/observed-boxes/sync`  
Equivalent member: `client.sync_observed_boxes`  

#### Signature

```python
client.organizations.sync_observed_boxes(organization_id: str, body: SyncObservedBoxesBody, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> dict[str, Any]
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Snapshot accepted; private and not cacheable. | application/json (object) |
| `400` | Invalid observation snapshot. | none |
| `401` | No valid product session. | none |
| `403` | Organization or scope denied. | none |
| `413` | Snapshot exceeds 64 KiB. | none |
| `503` | Inventory storage unavailable. | none |

#### Canonical required-input example

```json
{
  "body": {
    "boxes": [
      {
        "boxId": "example",
        "kind": "provider-list",
        "provider": "example",
        "state": "running"
      }
    ],
    "sourceId": "00000000-0000-0000-ae61-93cfab8e5e4b"
  },
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.sync_observed_boxes('example', {'boxes': [{'boxId': 'example', 'kind': 'provider-list', 'provider': 'example', 'state': 'running'}], 'sourceId': '00000000-0000-0000-ae61-93cfab8e5e4b'}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJzeW5jT2JzZXJ2ZWRCb3hlcyJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJvcmdhbml6YXRpb25zLnVwc2VydF9tZW1iZXIiLCJtZXRob2QiOiJQT1NUIiwib3BlcmF0aW9uX2lkIjoidXBzZXJ0TWVtYmVyIiwicGF0aCI6Ii92MS9vcmdhbml6YXRpb25zL3tvcmdhbml6YXRpb25JZH0vbWVtYmVycyIsInJlc291cmNlIjoib3JnYW5pemF0aW9ucyIsInNlY3Rpb25fc2hhMjU2IjoiOThmMzIwMmFkZWY3NzliOGQwMTI5MjA5OTQ0NzcxYjRhYjgwMmEyYWRiZmE5NTlmMWRlMWQ4NWIzN2RlZGZkNSIsInNpZ25hdHVyZV9zaGEyNTYiOiJiOWQ0MjUxZWUzZTMyZmJhNTU2ODcxZTcxODg3Mjg0ZTk0MmYxZTA4YTAwNzgwZThiYWU4ODYzMTBmOGYwNTYzIn0 -->
### `client.organizations.upsert_member`

Operation ID: `upsertMember`  
Route: `POST` `/v1/organizations/{organizationId}/members`  
Equivalent member: `client.upsert_member`  

#### Signature

```python
client.organizations.upsert_member(organization_id: str, body: UpsertMemberBody, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | `path` | yes | `string` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Member updated | none |
| `201` | Member added | none |
| `402` | Seat limit reached or entitlement missing | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "body": {
    "email": "example-f35c@example.test",
    "role": "owner"
  },
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "organizationId",
      "value": "example"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.organizations.upsert_member('example', {'email': 'example-f35c@example.test', 'role': 'owner'}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJ1cHNlcnRNZW1iZXIifQ -->

## Resource `plans`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJwbGFucy5nZXQiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJnZXRQbGFucyIsInBhdGgiOiIvdjEvcGxhbnMiLCJyZXNvdXJjZSI6InBsYW5zIiwic2VjdGlvbl9zaGEyNTYiOiJlNjdiMzkyMzdmZjFjMjBjOGU2MDI3ODY0OTE0YmNjMTdmNzAxMWYzMDJhNjMxYzI0MWVlNGVjOWU1MDM1MDViIiwic2lnbmF0dXJlX3NoYTI1NiI6IjMwNjk3OWFlMzIxNmY2ZjIyZDQxNzQ3NTJjMmQwYTIyYTNmZGYwYWE5MmI5MTYyMTA4YThiYTA3NjRiYmQxNWEifQ -->
### `client.plans.get`

Operation ID: `getPlans`  
Route: `GET` `/v1/plans`  
Equivalent member: `client.get_plans`  

#### Signature

```python
client.plans.get(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | OK | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.plans.get()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRQbGFucyJ9 -->

## Resource `telemetry`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ0ZWxlbWV0cnkuaW5nZXN0IiwibWV0aG9kIjoiUE9TVCIsIm9wZXJhdGlvbl9pZCI6ImluZ2VzdFRlbGVtZXRyeSIsInBhdGgiOiIvdjEvdGVsZW1ldHJ5L2luZ2VzdCIsInJlc291cmNlIjoidGVsZW1ldHJ5Iiwic2VjdGlvbl9zaGEyNTYiOiI5ODZkN2UwMGQzMTcyYzVjZjJlMjk1YWRhYWJkNzJkNzlmZTE1YTdmZmI4NDAxMzY1NmI3ZjdiMzhkMjUyM2UxIiwic2lnbmF0dXJlX3NoYTI1NiI6IjU2NWIzZGUzZDYxOTI3ZTM3OTY5ZmI0YzVkNjU3MjQ2YjE3YWI1ZmExMDYzNWFjOTMzNTY3NDdjZTIzMzU0NTgifQ -->
### `client.telemetry.ingest`

Operation ID: `ingestTelemetry`  
Route: `POST` `/v1/telemetry/ingest`  
Equivalent member: `client.ingest_telemetry`  

#### Signature

```python
client.telemetry.ingest(body: dict[str, Any], *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `201` | Stored | none |
| `400` | Invalid event | none |
| `401` | License required | none |
| `409` | Managed account authority required; use the returned JackAISaaS accountUrl or portalUrl. | none |
| `413` | Body too large | none |
| `503` | Ingestion not configured | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.telemetry.ingest({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJpbmdlc3RUZWxlbWV0cnkifQ -->

## Resource `waitlist`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3YWl0bGlzdC5saXN0IiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoibGlzdFdhaXRsaXN0IiwicGF0aCI6Ii92MS93YWl0bGlzdCIsInJlc291cmNlIjoid2FpdGxpc3QiLCJzZWN0aW9uX3NoYTI1NiI6IjViNDY5MzA5ZTQ4NDcwN2I3ZTJjZWRiYTk5NzZlZTViZjViMTZkNzFkNDdiMWU2MWQzNTVkNDQzOGNjZmI2OGEiLCJzaWduYXR1cmVfc2hhMjU2IjoiMGFhMDFiZGE1ZTBkNGQ2YmMzNDdlZjlmZGFlMTZkNGI0YWE5ZTlmZmQ2NjNmNDdlMTRkOGQ2MmZlODA1MjVkZiJ9 -->
### `client.waitlist.list`

Operation ID: `listWaitlist`  
Route: `GET` `/v1/waitlist`  
Equivalent member: `client.list_waitlist`  

#### Signature

```python
client.waitlist.list(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Requests | none |
| `401` | Admin token required | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.waitlist.list()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0V2FpdGxpc3QifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3YWl0bGlzdC5yZXF1ZXN0X2FjY2VzcyIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJyZXF1ZXN0QWNjZXNzIiwicGF0aCI6Ii92MS93YWl0bGlzdCIsInJlc291cmNlIjoid2FpdGxpc3QiLCJzZWN0aW9uX3NoYTI1NiI6IjNiM2ViZWU3ZWI4MTIyYmEzMzI4NTZmNmU2NTMzZDlmYWRlY2VlMGViOTU5Zjg3Yjc0YzIyNGUxOTNiYWY2MTciLCJzaWduYXR1cmVfc2hhMjU2IjoiMmZjZTQ2ZDJkYjkzY2MzODEyY2IwMjcxMmI5MjkyNTVjNzg3MzliYzdjOGRmOTJiOGU0Y2ExMzFjYmYzOGYxNiJ9 -->
### `client.waitlist.request_access`

Operation ID: `requestAccess`  
Route: `POST` `/v1/waitlist`  
Equivalent member: `client.request_access`  

#### Signature

```python
client.waitlist.request_access(body: dict[str, Any], *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `202` | Received | none |
| `400` | Invalid email | none |
| `413` | Body too large | none |
| `429` | Rate limited | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.waitlist.request_access({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJyZXF1ZXN0QWNjZXNzIn0 -->

## Resource `workspaces`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3b3Jrc3BhY2VzLmNsb3NlX2hvc3RlZCIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJjbG9zZUhvc3RlZFdvcmtzcGFjZSIsInBhdGgiOiIvdjEvd29ya3NwYWNlcy97d29ya3NwYWNlSWR9L2Nsb3NlIiwicmVzb3VyY2UiOiJ3b3Jrc3BhY2VzIiwic2VjdGlvbl9zaGEyNTYiOiI3YmM2YWRmZGM2MjE3NDU4NTc3NWI1YzQ4MzBiMjY1MjFhOWU2YmI3NTdkMDk0ZWE5Nzk4N2NkNzQyOGY5YjRjIiwic2lnbmF0dXJlX3NoYTI1NiI6IjA3Nzc4ODA2MTcyNzhhMjFmNWY4MDIxMmFhNDJiYTBiOWY1M2NiZmQ4MmY1MmYxZjc1NWFmM2IzZjQ4MGMyODIifQ -->
### `client.workspaces.close_hosted`

Operation ID: `closeHostedWorkspace`  
Route: `POST` `/v1/workspaces/{workspaceId}/close`  
Equivalent member: `client.close_hosted_workspace`  

#### Signature

```python
client.workspaces.close_hosted(workspace_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | `path` | yes | `string&lt;uuid&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authorized workspace state or result | none |
| `400` | Invalid bounded request | none |
| `401` | Product session rejected | none |
| `402` | Hub entitlement or atomic quota denied | none |
| `403` | Operation or fleet policy denied | none |
| `404` | Resource not found in the authorized tenant and product environment | none |
| `409` | Idempotency conflict, incompatible state or cleanup unconfirmed | none |
| `503` | Operator provider, template, storage or authority unavailable | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "workspaceId",
      "value": "00000000-0000-0000-6658-e129a559a4dd"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.workspaces.close_hosted('00000000-0000-0000-6658-e129a559a4dd')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJjbG9zZUhvc3RlZFdvcmtzcGFjZSJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3b3Jrc3BhY2VzLmdldF9ob3N0ZWQiLCJtZXRob2QiOiJHRVQiLCJvcGVyYXRpb25faWQiOiJnZXRIb3N0ZWRXb3Jrc3BhY2UiLCJwYXRoIjoiL3YxL3dvcmtzcGFjZXMve3dvcmtzcGFjZUlkfSIsInJlc291cmNlIjoid29ya3NwYWNlcyIsInNlY3Rpb25fc2hhMjU2IjoiNjZhYzlmOTRjMDA5NDIwZTc0NjA5NWQyYjhiOGUxOTVhYjVhY2ZiZmU2Y2UxOThkMDEzNGY5ZDkxN2VlNDljYyIsInNpZ25hdHVyZV9zaGEyNTYiOiJmZTMyYWUyM2IxYTQzODUyYjBiOTA5ZDJkYTk4ZWI5MzljNjU4ZTNkN2E4NTMzM2M5YWNmOGUyY2YxNTVkN2ViIn0 -->
### `client.workspaces.get_hosted`

Operation ID: `getHostedWorkspace`  
Route: `GET` `/v1/workspaces/{workspaceId}`  
Equivalent member: `client.get_hosted_workspace`  

#### Signature

```python
client.workspaces.get_hosted(workspace_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | `path` | yes | `string&lt;uuid&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authorized workspace state or result | none |
| `400` | Invalid bounded request | none |
| `401` | Product session rejected | none |
| `402` | Hub entitlement or atomic quota denied | none |
| `403` | Operation or fleet policy denied | none |
| `404` | Resource not found in the authorized tenant and product environment | none |
| `409` | Idempotency conflict, incompatible state or cleanup unconfirmed | none |
| `503` | Operator provider, template, storage or authority unavailable | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "workspaceId",
      "value": "00000000-0000-0000-dd2f-cd2edd1eeb24"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.workspaces.get_hosted('00000000-0000-0000-dd2f-cd2edd1eeb24')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRIb3N0ZWRXb3Jrc3BhY2UifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3b3Jrc3BhY2VzLmdldF9ob3N0ZWRfb3BlcmF0aW9uIiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoiZ2V0SG9zdGVkV29ya3NwYWNlT3BlcmF0aW9uIiwicGF0aCI6Ii92MS93b3Jrc3BhY2VzL3t3b3Jrc3BhY2VJZH0vb3BlcmF0aW9ucy97b3BlcmF0aW9uSWR9IiwicmVzb3VyY2UiOiJ3b3Jrc3BhY2VzIiwic2VjdGlvbl9zaGEyNTYiOiI3ZTgzYjQ0NjNiMTg5YmU4MTI0MWVhM2NhNjRkMDRmZjY1MmNiMjc3NGI1NTJmYTU3NDMwODI5ODgzNmU5ZWVkIiwic2lnbmF0dXJlX3NoYTI1NiI6ImIzZjljMjJlZTc0NmZkYjVkYThkMmZiMDRhMzIyMDMyYTFiMWY4NWM3N2IxMjJjMDI3ZTVmNTg2YTA1NzE0MDIifQ -->
### `client.workspaces.get_hosted_operation`

Operation ID: `getHostedWorkspaceOperation`  
Route: `GET` `/v1/workspaces/{workspaceId}/operations/{operationId}`  
Equivalent member: `client.get_hosted_workspace_operation`  

#### Signature

```python
client.workspaces.get_hosted_operation(workspace_id: str, operation_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | `path` | yes | `string&lt;uuid&gt;` |  |
| `operationId` | `path` | yes | `string&lt;uuid&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authorized workspace state or result | none |
| `400` | Invalid bounded request | none |
| `401` | Product session rejected | none |
| `402` | Hub entitlement or atomic quota denied | none |
| `403` | Operation or fleet policy denied | none |
| `404` | Resource not found in the authorized tenant and product environment | none |
| `409` | Idempotency conflict, incompatible state or cleanup unconfirmed | none |
| `503` | Operator provider, template, storage or authority unavailable | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "workspaceId",
      "value": "00000000-0000-0000-7261-284a8b699ebd"
    },
    {
      "in": "path",
      "name": "operationId",
      "value": "00000000-0000-0000-5ba1-19fa55640b6d"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.workspaces.get_hosted_operation('00000000-0000-0000-7261-284a8b699ebd', '00000000-0000-0000-5ba1-19fa55640b6d')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRIb3N0ZWRXb3Jrc3BhY2VPcGVyYXRpb24ifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3b3Jrc3BhY2VzLmdldF9ob3N0ZWRfc291cmNlIiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoiZ2V0SG9zdGVkV29ya3NwYWNlU291cmNlIiwicGF0aCI6Ii92MS93b3Jrc3BhY2VzL3t3b3Jrc3BhY2VJZH0vc291cmNlIiwicmVzb3VyY2UiOiJ3b3Jrc3BhY2VzIiwic2VjdGlvbl9zaGEyNTYiOiJhOGRjYmEzYmVjYTkwMWUxNTBhN2M2OGIwMGI2MDg1MzI5M2U5OGQ2NjZmN2JhMDg1N2Q3OTY2MDZhOWE3NjAzIiwic2lnbmF0dXJlX3NoYTI1NiI6ImRiZWM1Njk0ZjY4NGExMzEwNzk2MzZkNzMyZDVmMDc5ZGRkMTJmNjRjM2E4YjVmOWIyMTNjYmY3MmYwYzFkZTYifQ -->
### `client.workspaces.get_hosted_source`

Operation ID: `getHostedWorkspaceSource`  
Route: `GET` `/v1/workspaces/{workspaceId}/source`  
Equivalent member: `client.get_hosted_workspace_source`  

#### Signature

```python
client.workspaces.get_hosted_source(workspace_id: str, *, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | `path` | yes | `string&lt;uuid&gt;` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authorized workspace state or result | none |
| `400` | Invalid bounded request | none |
| `401` | Product session rejected | none |
| `402` | Hub entitlement or atomic quota denied | none |
| `403` | Operation or fleet policy denied | none |
| `404` | Resource not found in the authorized tenant and product environment | none |
| `409` | Idempotency conflict, incompatible state or cleanup unconfirmed | none |
| `503` | Operator provider, template, storage or authority unavailable | none |

#### Canonical required-input example

```json
{
  "parameters": [
    {
      "in": "path",
      "name": "workspaceId",
      "value": "00000000-0000-0000-43c8-d895a22336ed"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.workspaces.get_hosted_source('00000000-0000-0000-43c8-d895a22336ed')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRIb3N0ZWRXb3Jrc3BhY2VTb3VyY2UifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3b3Jrc3BhY2VzLmxpc3RfaG9zdGVkIiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoibGlzdEhvc3RlZFdvcmtzcGFjZXMiLCJwYXRoIjoiL3YxL3dvcmtzcGFjZXMiLCJyZXNvdXJjZSI6IndvcmtzcGFjZXMiLCJzZWN0aW9uX3NoYTI1NiI6ImFkM2YwMWExZmZhZGY2Mjg4ZGQ5NDY4NjZjNTE4ZjFhYjQ0ZjY5MTA5NTNlMGE0MjE1YTA1ZjZiYTA4ZDFmOWEiLCJzaWduYXR1cmVfc2hhMjU2IjoiNDI4ZTUyOWRkNzU5NTEyNTc4Nzk1NjYxZDIwNWQxMDMzZWU3ODQ1ZWViZjQ2ZGNiYWU3MzQ0NTE4OWQ0NDMwMiJ9 -->
### `client.workspaces.list_hosted`

Operation ID: `listHostedWorkspaces`  
Route: `GET` `/v1/workspaces`  
Equivalent member: `client.list_hosted_workspaces`  

#### Signature

```python
client.workspaces.list_hosted(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authorized workspace state or result | none |
| `400` | Invalid bounded request | none |
| `401` | Product session rejected | none |
| `402` | Hub entitlement or atomic quota denied | none |
| `403` | Operation or fleet policy denied | none |
| `404` | Resource not found in the authorized tenant and product environment | none |
| `409` | Idempotency conflict, incompatible state or cleanup unconfirmed | none |
| `503` | Operator provider, template, storage or authority unavailable | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.workspaces.list_hosted()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsaXN0SG9zdGVkV29ya3NwYWNlcyJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3b3Jrc3BhY2VzLm9wZW5faG9zdGVkIiwibWV0aG9kIjoiUE9TVCIsIm9wZXJhdGlvbl9pZCI6Im9wZW5Ib3N0ZWRXb3Jrc3BhY2UiLCJwYXRoIjoiL3YxL3dvcmtzcGFjZXMiLCJyZXNvdXJjZSI6IndvcmtzcGFjZXMiLCJzZWN0aW9uX3NoYTI1NiI6IjYxOTNmNjYwYmU4N2RiYWQ1Y2RlZTY0ZDkyOTU4MTY2OTkwNTlkMWQ3OTgyZjNiMWZiYThmZDFlMWYzZGFjZGYiLCJzaWduYXR1cmVfc2hhMjU2IjoiMzVhZjcyOTJmZGM3NGMzMmQxOTc5NTNmOWJhOWRiYTVjZDY2YWRjNGU0NjVmMDM4ZGZmZGNhMTZiYmY5YmIxOCJ9 -->
### `client.workspaces.open_hosted`

Operation ID: `openHostedWorkspace`  
Route: `POST` `/v1/workspaces`  
Equivalent member: `client.open_hosted_workspace`  

#### Signature

```python
client.workspaces.open_hosted(body: OpenHostedWorkspaceBody, idempotency_key_2: Optional[str] = None, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `Idempotency-Key` | `header` | no | `string` | Required here or in the idempotencyKey body field. Replays never allocate or execute again. |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authorized workspace state or result | none |
| `201` | Prepared workspace; source and provider allocation recorded durably | none |
| `400` | Invalid bounded request | none |
| `401` | Product session rejected | none |
| `402` | Hub entitlement or atomic quota denied | none |
| `403` | Operation or fleet policy denied | none |
| `404` | Resource not found in the authorized tenant and product environment | none |
| `409` | Idempotency conflict, incompatible state or cleanup unconfirmed | none |
| `503` | Operator provider, template, storage or authority unavailable | none |

#### Canonical required-input example

```json
{
  "body": {},
  "content_type": "application/json",
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.workspaces.open_hosted({}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJvcGVuSG9zdGVkV29ya3NwYWNlIn0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3b3Jrc3BhY2VzLnJlY292ZXJfaG9zdGVkIiwibWV0aG9kIjoiUE9TVCIsIm9wZXJhdGlvbl9pZCI6InJlY292ZXJIb3N0ZWRXb3Jrc3BhY2UiLCJwYXRoIjoiL3YxL3dvcmtzcGFjZXMve3dvcmtzcGFjZUlkfS9yZWNvdmVyIiwicmVzb3VyY2UiOiJ3b3Jrc3BhY2VzIiwic2VjdGlvbl9zaGEyNTYiOiJiZWQ3OGMwYzViMTM0OTU5ODFhZTk4NGRmNGNjNTk0NGIwZTFkYWUxMTY4NjRhNDZjY2Y0MDY0MmZmYjVjNTRkIiwic2lnbmF0dXJlX3NoYTI1NiI6ImY5MzVkZGQ2MDA3MDdhYTIyNDEwNGM1ZWZiYjQ4NDY0NTY5NjQ5NzljZjc4NDk3OTU2MGQxZDVhMmRkMjVkZWIifQ -->
### `client.workspaces.recover_hosted`

Operation ID: `recoverHostedWorkspace`  
Route: `POST` `/v1/workspaces/{workspaceId}/recover`  
Equivalent member: `client.recover_hosted_workspace`  

#### Signature

```python
client.workspaces.recover_hosted(workspace_id: str, body: RecoverHostedWorkspaceBody, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | `path` | yes | `string&lt;uuid&gt;` |  |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authorized workspace state or result | none |
| `202` | No verified terminal receipt yet; workspace remains unavailable for new commands | none |
| `400` | Invalid bounded request | none |
| `401` | Product session rejected | none |
| `402` | Hub entitlement or atomic quota denied | none |
| `403` | Operation or fleet policy denied | none |
| `404` | Resource not found in the authorized tenant and product environment | none |
| `409` | Idempotency conflict, incompatible state or cleanup unconfirmed | none |
| `503` | Operator provider, template, storage or authority unavailable | none |

#### Canonical required-input example

```json
{
  "body": {
    "operationId": "00000000-0000-0000-d4ac-b0b84827b6d9"
  },
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "workspaceId",
      "value": "00000000-0000-0000-973a-c9ae0260973d"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.workspaces.recover_hosted('00000000-0000-0000-973a-c9ae0260973d', {'operationId': '00000000-0000-0000-d4ac-b0b84827b6d9'}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJyZWNvdmVySG9zdGVkV29ya3NwYWNlIn0 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ3b3Jrc3BhY2VzLnJ1bl9ob3N0ZWQiLCJtZXRob2QiOiJQT1NUIiwib3BlcmF0aW9uX2lkIjoicnVuSG9zdGVkV29ya3NwYWNlIiwicGF0aCI6Ii92MS93b3Jrc3BhY2VzL3t3b3Jrc3BhY2VJZH0vcnVuIiwicmVzb3VyY2UiOiJ3b3Jrc3BhY2VzIiwic2VjdGlvbl9zaGEyNTYiOiJiZDBhM2NhYzQ3YzgxMjQyZDU4OGY5MGQ3MThlNjhkOGJkYTg4NGVhYjFhZDZmN2U2Y2FlZjI5OTE2M2Q2YTY2Iiwic2lnbmF0dXJlX3NoYTI1NiI6IjVjNmJjMjYxMTUzNzVmZmNhNzU3NzEyZTM4MDczZTExZjRkZTcxMzJjZTY3MGM0Njg4ZmRjNWM2MzUwMDA5YzAifQ -->
### `client.workspaces.run_hosted`

Operation ID: `runHostedWorkspace`  
Route: `POST` `/v1/workspaces/{workspaceId}/run`  
Equivalent member: `client.run_hosted_workspace`  

#### Signature

```python
client.workspaces.run_hosted(workspace_id: str, body: RunHostedWorkspaceBody, idempotency_key_2: Optional[str] = None, *, content_type: Optional[str] = None, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | `path` | yes | `string&lt;uuid&gt;` |  |
| `Idempotency-Key` | `header` | no | `string` | Required here or in the idempotencyKey body field. Replays never allocate or execute again. |
| `body` | body | yes | `object` |  |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authorized workspace state or result | none |
| `202` | Running or uncertain operation; inspect or explicitly recover, never resend with a new key | none |
| `400` | Invalid bounded request | none |
| `401` | Product session rejected | none |
| `402` | Hub entitlement or atomic quota denied | none |
| `403` | Operation or fleet policy denied | none |
| `404` | Resource not found in the authorized tenant and product environment | none |
| `409` | Idempotency conflict, incompatible state or cleanup unconfirmed | none |
| `503` | Operator provider, template, storage or authority unavailable | none |

#### Canonical required-input example

```json
{
  "body": {
    "command": "example"
  },
  "content_type": "application/json",
  "parameters": [
    {
      "in": "path",
      "name": "workspaceId",
      "value": "00000000-0000-0000-4862-6c003dd1756b"
    }
  ]
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.workspaces.run_hosted('00000000-0000-0000-4862-6c003dd1756b', {'command': 'example'}, content_type='application/json')
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJydW5Ib3N0ZWRXb3Jrc3BhY2UifQ -->

