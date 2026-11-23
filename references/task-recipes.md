# Agent task recipes

Corpus SHA-256: `af4beef7d06f6698e5d8fdfb9c6346732606854906d82d9e55d0bcd7712e697c`

These recipes are retrieval and planning evidence. They never authorize API execution.

## `authentication-canceljob-productsession` — authentication

How is productSession authentication applied to cancelJob? Cite exactly: operation:cancelJob, auth:productSession

Intent: Recover the exact authentication scheme, location or flow, and required scopes.

Expected evidence:

- operation: `cancelJob`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/cancelJob`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `authentication-controluser-admintoken` — authentication

How is adminToken authentication applied to controlUser? Cite exactly: operation:controlUser, auth:adminToken

Intent: Recover the exact authentication scheme, location or flow, and required scopes.

Expected evidence:

- operation: `controlUser`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/controlUser`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-canceljob` — discovery

Find the exact operation cancelJob (POST /v1/jobs/{jobId}/cancel) for Cancel a job. Cite exactly: operation:cancelJob, auth:productSession

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `cancelJob`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/cancelJob`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-closehostedworkspace` — discovery

Find the exact operation closeHostedWorkspace (POST /v1/workspaces/{workspaceId}/close) for Delete the owned provider box and private source; available after paid entitlement loss with current close authority. Cite exactly: operation:closeHostedWorkspace, auth:productSession

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `closeHostedWorkspace`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/closeHostedWorkspace`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-closepersistentbox` — discovery

Find the exact operation closePersistentBox (POST /v1/organizations/{organizationId}/persistent-boxes/{boxId}/close) for Close a hosted durable box through its pinned operator provider. Cite exactly: operation:closePersistentBox, schema:HostedPersistentBoxClose, auth:productSession

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `closePersistentBox`
- schema: `HostedPersistentBoxClose`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/closePersistentBox`
- `omniwrap://semantic/schema/HostedPersistentBoxClose`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-controluser` — discovery

Find the exact operation controlUser (POST /v1/admin/users) for Disable, ban, delete or re-enable a user. Cite exactly: operation:controlUser, auth:adminToken

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `controlUser`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/controlUser`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-getadminplans` — discovery

Find the exact operation getAdminPlans (GET /v1/admin/plans) for Plan catalog with admin controls. Cite exactly: operation:getAdminPlans, auth:adminToken

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `getAdminPlans`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/getAdminPlans`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-getauthgate` — discovery

Find the exact operation getAuthGate (GET /v1/auth/gate) for Registration gate state and waitlist count. Cite exactly: operation:getAuthGate

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `getAuthGate`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/operation/getAuthGate`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-listjobs` — discovery

Find the exact operation listJobs (GET /v1/jobs) for List the organization jobs. Cite exactly: operation:listJobs, auth:productSession

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `listJobs`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/listJobs`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-provisionpersistentbox` — discovery

Find the exact operation provisionPersistentBox (POST /v1/organizations/{organizationId}/persistent-boxes) for Provision a durable box from a configured operator offer. Cite exactly: operation:provisionPersistentBox, schema:HostedPersistentBoxRead, auth:productSession

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `provisionPersistentBox`
- schema: `HostedPersistentBoxRead`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/provisionPersistentBox`
- `omniwrap://semantic/schema/HostedPersistentBoxRead`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-readtelemetry` — discovery

Find the exact operation readTelemetry (GET /v1/admin/telemetry) for Read opt-in telemetry events. Cite exactly: operation:readTelemetry, auth:adminToken

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `readTelemetry`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/readTelemetry`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-requestaccess` — discovery

Find the exact operation requestAccess (POST /v1/waitlist) for Request beta access; one uniform answer, existing entries are never overwritten. Cite exactly: operation:requestAccess

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `requestAccess`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/operation/requestAccess`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-startpersistentbox` — discovery

Find the exact operation startPersistentBox (POST /v1/organizations/{organizationId}/persistent-boxes/{boxId}/start) for Start a retained hosted box. Cite exactly: operation:startPersistentBox, schema:HostedPersistentBoxRead, auth:productSession

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `startPersistentBox`
- schema: `HostedPersistentBoxRead`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/startPersistentBox`
- `omniwrap://semantic/schema/HostedPersistentBoxRead`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-syncobservedboxes` — discovery

Find the exact operation syncObservedBoxes (POST /v1/organizations/{organizationId}/observed-boxes/sync) for Replace one actor-owned client observation snapshot. Cite exactly: operation:syncObservedBoxes, schema:ObservedBox, auth:productSession

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `syncObservedBoxes`
- schema: `ObservedBox`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/syncObservedBoxes`
- `omniwrap://semantic/schema/ObservedBox`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `error-recovery-closehostedworkspace` — error-recovery

Which failure responses and error schemas apply to closeHostedWorkspace? Cite exactly: operation:closeHostedWorkspace, auth:productSession

Intent: Recover non-success response selectors and their declared error payloads.

Expected evidence:

- operation: `closeHostedWorkspace`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/closeHostedWorkspace`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `error-recovery-closepersistentbox` — error-recovery

Which failure responses and error schemas apply to closePersistentBox? Cite exactly: operation:closePersistentBox, auth:productSession

Intent: Recover non-success response selectors and their declared error payloads.

Expected evidence:

- operation: `closePersistentBox`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/closePersistentBox`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `error-recovery-controluser` — error-recovery

Which failure responses and error schemas apply to controlUser? Cite exactly: operation:controlUser, auth:adminToken

Intent: Recover non-success response selectors and their declared error payloads.

Expected evidence:

- operation: `controlUser`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/controlUser`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `error-recovery-getadminplans` — error-recovery

Which failure responses and error schemas apply to getAdminPlans? Cite exactly: operation:getAdminPlans, auth:adminToken

Intent: Recover non-success response selectors and their declared error payloads.

Expected evidence:

- operation: `getAdminPlans`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/getAdminPlans`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `error-recovery-listjobs` — error-recovery

Which failure responses and error schemas apply to listJobs? Cite exactly: operation:listJobs, auth:productSession

Intent: Recover non-success response selectors and their declared error payloads.

Expected evidence:

- operation: `listJobs`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/listJobs`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `error-recovery-provisionpersistentbox` — error-recovery

Which failure responses and error schemas apply to provisionPersistentBox? Cite exactly: operation:provisionPersistentBox, auth:productSession

Intent: Recover non-success response selectors and their declared error payloads.

Expected evidence:

- operation: `provisionPersistentBox`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/provisionPersistentBox`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `error-recovery-readtelemetry` — error-recovery

Which failure responses and error schemas apply to readTelemetry? Cite exactly: operation:readTelemetry, auth:adminToken

Intent: Recover non-success response selectors and their declared error payloads.

Expected evidence:

- operation: `readTelemetry`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/readTelemetry`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `error-recovery-requestaccess` — error-recovery

Which failure responses and error schemas apply to requestAccess? Cite exactly: operation:requestAccess

Intent: Recover non-success response selectors and their declared error payloads.

Expected evidence:

- operation: `requestAccess`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/operation/requestAccess`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-canceljob` — integration

Plan a correct SDK integration for cancelJob (POST /v1/jobs/{jobId}/cancel). Cite exactly: operation:cancelJob, auth:productSession

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `cancelJob`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/cancelJob`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-closehostedworkspace` — integration

Plan a correct SDK integration for closeHostedWorkspace (POST /v1/workspaces/{workspaceId}/close). Cite exactly: operation:closeHostedWorkspace, auth:productSession

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `closeHostedWorkspace`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/closeHostedWorkspace`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-closepersistentbox` — integration

Plan a correct SDK integration for closePersistentBox (POST /v1/organizations/{organizationId}/persistent-boxes/{boxId}/close). Cite exactly: operation:closePersistentBox, schema:HostedPersistentBoxClose, auth:productSession

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `closePersistentBox`
- schema: `HostedPersistentBoxClose`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/closePersistentBox`
- `omniwrap://semantic/schema/HostedPersistentBoxClose`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-controluser` — integration

Plan a correct SDK integration for controlUser (POST /v1/admin/users). Cite exactly: operation:controlUser, auth:adminToken

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `controlUser`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/controlUser`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-getadminplans` — integration

Plan a correct SDK integration for getAdminPlans (GET /v1/admin/plans). Cite exactly: operation:getAdminPlans, auth:adminToken

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `getAdminPlans`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/getAdminPlans`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-getauthgate` — integration

Plan a correct SDK integration for getAuthGate (GET /v1/auth/gate). Cite exactly: operation:getAuthGate

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `getAuthGate`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/operation/getAuthGate`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-listjobs` — integration

Plan a correct SDK integration for listJobs (GET /v1/jobs). Cite exactly: operation:listJobs, auth:productSession

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `listJobs`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/listJobs`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-provisionpersistentbox` — integration

Plan a correct SDK integration for provisionPersistentBox (POST /v1/organizations/{organizationId}/persistent-boxes). Cite exactly: operation:provisionPersistentBox, schema:HostedPersistentBoxRead, auth:productSession

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `provisionPersistentBox`
- schema: `HostedPersistentBoxRead`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/provisionPersistentBox`
- `omniwrap://semantic/schema/HostedPersistentBoxRead`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-readtelemetry` — integration

Plan a correct SDK integration for readTelemetry (GET /v1/admin/telemetry). Cite exactly: operation:readTelemetry, auth:adminToken

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `readTelemetry`
- authentication: `adminToken`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/adminToken`
- `omniwrap://semantic/operation/readTelemetry`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-requestaccess` — integration

Plan a correct SDK integration for requestAccess (POST /v1/waitlist). Cite exactly: operation:requestAccess

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `requestAccess`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/operation/requestAccess`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-startpersistentbox` — integration

Plan a correct SDK integration for startPersistentBox (POST /v1/organizations/{organizationId}/persistent-boxes/{boxId}/start). Cite exactly: operation:startPersistentBox, schema:HostedPersistentBoxRead, auth:productSession

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `startPersistentBox`
- schema: `HostedPersistentBoxRead`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/startPersistentBox`
- `omniwrap://semantic/schema/HostedPersistentBoxRead`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-syncobservedboxes` — integration

Plan a correct SDK integration for syncObservedBoxes (POST /v1/organizations/{organizationId}/observed-boxes/sync). Cite exactly: operation:syncObservedBoxes, schema:ObservedBox, auth:productSession

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `syncObservedBoxes`
- schema: `ObservedBox`
- authentication: `productSession`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/productSession`
- `omniwrap://semantic/operation/syncObservedBoxes`
- `omniwrap://semantic/schema/ObservedBox`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.
