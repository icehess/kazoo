### Users

#### About Users

#### Schema

Schema for a user



Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`call_forward.direct_calls_only` | Determines if the calls that are not directly sent to the device should be forwarded | `boolean()` | `false` | `false`
`call_forward.enabled` | Determines if the call forwarding should be used | `boolean()` | `false` | `false`
`call_forward.failover` | Enable the call-forwarding parameters if the device is offline | `boolean()` | `false` | `false`
`call_forward.ignore_early_media` | The option to determine if early media from the call forwarded number should ignored | `boolean()` | `true` | `false`
`call_forward.keep_caller_id` | Determines if the caller id is kept when the call is forwarded, if not the devices caller id is used | `boolean()` | `true` | `false`
`call_forward.number` | The number to forward calls to | `string(0..35)` |   | `false`
`call_forward.require_keypress` | Determines if the callee is prompted to press 1 to accept the call | `boolean()` | `true` | `false`
`call_forward.substitute` | Determines if the call forwarding replaces the device | `boolean()` | `true` | `false`
`call_forward` | The device call forward parameters | `object()` |   | `false`
`call_recording` |   | `object()` |   | `false`
`call_restriction` | Device level call restrictions for each available number classification | `object()` | `{}` | `false`
`call_waiting` |   | [#/definitions/call_waiting](#call_waiting) |   | `false`
`caller_id` | The device caller ID parameters | `object()` | `{}` | `false`
`contact_list.exclude` | If set to true the device is excluded from the contact list | `boolean()` |   | `false`
`contact_list` | Contect List Parameters | `object()` | `{}` | `false`
`dial_plan` | A list of rules used to modify dialed numbers | `object()` | `{}` | `false`
`directories` | Provides the mappings for what directory the user is a part of (the key), and what callflow (the value) to invoke if the user is selected by the caller. | `object()` |   | `false`
`do_not_disturb.enabled` | Is do-not-disturb enabled for this user? | `boolean()` |   | `false`
`do_not_disturb` | DND Parameters | `object()` |   | `false`
`email` | The email of the user | `string(1..254)` |   | `false`
`enabled` | Determines if the user is currently enabled | `boolean()` | `true` | `false`
`feature_level` | The user level for assigning feature sets | `string()` |   | `false`
`first_name` | The first name of the user | `string(1..128)` |   | `true`
`formatters` |   | `object()` |   | `false`
`hotdesk.enabled` | Determines if the user has hotdesking enabled | `boolean()` | `false` | `false`
`hotdesk.id` | The users hotdesk id | `string(0..15)` |   | `false`
`hotdesk.keep_logged_in_elsewhere` | Determines if user should be able to login to multiple phones simultaneously | `boolean()` | `false` | `false`
`hotdesk.pin` | The users hotdesk pin number | `string(4..15)` |   | `false`
`hotdesk.require_pin` | Determines if user requires a pin to change the hotdesk state | `boolean()` | `false` | `false`
`hotdesk` | The user hotdesk parameters | `object()` | `{}` | `false`
`language` | The language for this user | `string()` |   | `false`
`last_name` | The last name of the user | `string(1..128)` |   | `true`
`media.audio.codecs.[]` |   | `string()` |   | `false`
`media.audio.codecs` | A list of audio codecs the device supports | `array(string('OPUS' | 'CELT@32000h' | 'G7221@32000h' | 'G7221@16000h' | 'G722' | 'speex@32000h' | 'speex@16000h' | 'PCMU' | 'PCMA' | 'G729' | 'GSM' | 'CELT@48000h' | 'CELT@64000h' | 'G722_16' | 'G722_32' | 'CELT_48' | 'CELT_64' | 'Speex' | 'speex'))` |   | `false`
`media.audio` | The audio media parameters | `object()` | `{}` | `false`
`media.bypass_media` | Default bypass media mode (The string type is deprecated, please use this as a boolean) | `boolean() | string('true' | 'false' | 'auto')` |   | `false`
`media.encryption.enforce_security` | Is Encryption Enabled? | `boolean()` | `false` | `false`
`media.encryption.methods.[]` |   | `string()` |   | `false`
`media.encryption.methods` | Supported Encryption Types | `array(string('zrtp' | 'srtp'))` | `[]` | `false`
`media.encryption` | Encryption Parameters | `object()` | `{}` | `false`
`media.fax_option` | Is T.38 Supported? | `boolean()` |   | `false`
`media.ignore_early_media` | The option to determine if early media from the device should always be ignored | `boolean()` |   | `false`
`media.progress_timeout` | The progress timeout to apply to the device (seconds) | `integer()` |   | `false`
`media.video.codecs.[]` |   | `string()` |   | `false`
`media.video.codecs` | A list of video codecs the device supports | `array(string('H261' | 'H263' | 'H264' | 'VP8'))` | `[]` | `false`
`media.video` | The video media parameters | `object()` | `{}` | `false`
`media` | The device media parameters | `object()` | `{}` | `false`
`metaflows` | The device metaflow parameters | [#/definitions/metaflows](#metaflows) |   | `false`
`music_on_hold.media_id` | The ID of a media object that should be used as the music on hold | `string(0..128)` |   | `false`
`music_on_hold` | The music on hold parameters used if not a property of the device owner | `object()` | `{}` | `false`
`password` | The GUI login password | `string()` |   | `false`
`presence_id` | Static presence ID (used instead of SIP username) | `string()` |   | `false`
`priv_level` | The privilege level of the user | `string('user' | 'admin')` | `user` | `false`
`profile` | User's profile data | `object()` | `{}` | `false`
`pronounced_name.media_id` | The ID of a media object that should be used as the music on hold | `string(0..128)` |   | `false`
`pronounced_name` | Name pronounced by user to introduce himself to conference members | `object()` |   | `false`
`require_password_update` | UI flag that the user should update their password. | `boolean()` | `false` | `false`
`ringtones.external` | The alert info SIP header added when the call is from internal sources | `string(0..256)` |   | `false`
`ringtones.internal` | The alert info SIP header added when the call is from external sources | `string(0..256)` |   | `false`
`ringtones` | Ringtone Parameters | `object()` | `{}` | `false`
`timezone` | User's timezone | `string()` |   | `false`
`username` | The GUI login username - alpha-numeric, dashes, at symbol, periods, plusses, and underscores allowed | `string(1..256)` |   | `false`
`verified` | Determines if the user has been verified | `boolean()` | `false` | `false`
`vm_to_email_enabled` | Determines if the user would like voicemails emailed to them | `boolean()` | `true` | `false`
`voicemail.notify.callback` |   | [#/definitions/notify.callback](#notifycallback) |   | `false`
`voicemail.notify` |   | `object()` |   | `false`
`voicemail` |   | `object()` |   | `false`

##### call_recording

endpoint recording settings


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`any` |   | [#/definitions/call_recording.source](#call_recordingsource) |   | `false`
`inbound` |   | [#/definitions/call_recording.source](#call_recordingsource) |   | `false`
`outbound` |   | [#/definitions/call_recording.source](#call_recordingsource) |   | `false`

##### call_recording.parameters


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`enabled` | is recording enabled | `boolean()` |   | `false`
`format` | What format to store the recording on disk | `string('mp3' | 'wav')` |   | `false`
`record_min_sec` | The minimum length, in seconds, the recording must be to be considered successful. Otherwise it is deleted | `integer()` |   | `false`
`record_on_answer` | Recording should start on answer | `boolean()` |   | `false`
`record_on_bridge` | Recording should start on bridge | `boolean()` |   | `false`
`record_sample_rate` | What sampling rate to use on the recording | `integer()` |   | `false`
`time_limit` | Time limit, in seconds, for the recording | `integer()` |   | `false`
`url` | The URL to use when sending the recording for storage | `string()` |   | `false`

##### call_recording.source


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`any` |   | [#/definitions/call_recording.parameters](#call_recordingparameters) |   | `false`
`offnet` |   | [#/definitions/call_recording.parameters](#call_recordingparameters) |   | `false`
`onnet` |   | [#/definitions/call_recording.parameters](#call_recordingparameters) |   | `false`

##### call_waiting

Parameters for server-side call waiting


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`enabled` | Determines if server side call waiting is enabled/disabled | `boolean()` |   | `false`

##### caller_id

Defines caller ID settings based on the type of call being made


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`emergency.name` | The caller id name for the object type | `string(0..35)` |   | `false`
`emergency.number` | The caller id name for the object type | `string(0..35)` |   | `false`
`emergency` | The caller ID used when a resource is flagged as 'emergency' | `object()` |   | `false`
`external.name` | The caller id name for the object type | `string(0..35)` |   | `false`
`external.number` | The caller id name for the object type | `string(0..35)` |   | `false`
`external` | The default caller ID used when dialing external numbers | `object()` |   | `false`
`internal.name` | The caller id name for the object type | `string(0..35)` |   | `false`
`internal.number` | The caller id name for the object type | `string(0..35)` |   | `false`
`internal` | The default caller ID used when dialing internal extensions | `object()` |   | `false`

##### dialplans

Permit local dialing by converting the dialed number to a routable form


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`system.[]` |   | `string()` |   | `false`
`system` | List of system dial plans | `array(string())` |   | `false`

##### formatters

Schema for request formatters


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`^[[:alnum:]_]+$` | Key to match in the route request JSON | `array([#/definitions/formatters.format_options](#formattersformat_options)) | [#/definitions/formatters.format_options](#formattersformat_options)` |   | `false`

##### formatters.format_options

Schema for formatter options


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`direction` | Only apply the formatter on the relevant request direction | `string('inbound' | 'outbound' | 'both')` |   | `false`
`match_invite_format` | Applicable on fields with SIP URIs. Will format the username portion to match the invite format of the outbound request. | `boolean()` |   | `false`
`prefix` | Prepends value against the result of a successful regex match | `string()` |   | `false`
`regex` | Matches against the value, with optional capture group | `string()` |   | `false`
`strip` | If set to true, the field will be stripped from the payload | `boolean()` |   | `false`
`suffix` | Appends value against the result of a successful regex match | `string()` |   | `false`
`value` | Replaces the current value with the static value defined | `string()` |   | `false`

##### metaflow

A metaflow node defines a module to execute, data to provide to that module, and one or more children to branch to


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children./.+/` |   | [#/definitions/metaflow](#metaflow) |   | `false`
`children` | Children metaflows | `object()` |   | `false`
`data` | The data/arguments of the metaflow module | `object()` |   | `false`
`module` | The name of the metaflow module to execute at this node | `string(1..64)` |   | `true`

##### metaflows

Actions applied to a call outside of the normal callflow, initiated by the caller(s)


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`binding_digit` | What DTMF will trigger the collection and analysis of the subsequent DTMF sequence | `string('1' | '2' | '3' | '4' | '5' | '6' | '7' | '8' | '9' | '0' | '*' | '#')` | `*` | `false`
`digit_timeout` | How long to wait between DTMF presses before processing the collected sequence (milliseconds) | `integer()` |   | `false`
`listen_on` | Which leg(s) of the call to listen for DTMF | `string('both' | 'self' | 'peer')` |   | `false`
`numbers./^[0-9]+$/` |   | [#/definitions/metaflow](#metaflow) |   | `false`
`numbers` | A list of static numbers with their flows | `object()` |   | `false`
`patterns./.+/` |   | [#/definitions/metaflow](#metaflow) |   | `false`
`patterns` | A list of patterns with their flows | `object()` |   | `false`

##### notify.callback

Schema for a callback options


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`attempts` | How many attempts without answer will system do | `integer()` |   | `false`
`disabled` | Determines if the system will call to callback number | `boolean()` |   | `false`
`interval_s` | How long will system wait between call back notification attempts | `integer()` |   | `false`
`number` | Number for callback notifications about new messages | `string()` |   | `false`
`schedule` | Schedules interval between callbacks | `array(integer())` |   | `false`
`timeout_s` | How long will system wait for answer to callback | `integer()` |   | `false`

##### profile

Defines user extended properties


Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`addresses.[].address` | To specify the address | `string()` |   | `false`
`addresses.[].types` | To specify types of the address | `array()` |   | `false`
`addresses` | To specify the components of the addresses | `array(object())` |   | `false`
`assistant` | To specify the user's assistant | `string()` |   | `false`
`birthday` | To specify the birth date of the user | `string()` |   | `false`
`nicknames.[]` |   | `string()` |   | `false`
`nicknames` | To specify the text corresponding to the nickname of the user | `array(string())` |   | `false`
`note` | To specify supplemental information or a comment that is associated with the user | `string()` |   | `false`
`role` | To specify the function or part played in a particular situation by the user | `string()` |   | `false`
`sort-string` | To specify the family name or given name text to be used for national-language-specific sorting of the FN and N types | `string()` |   | `false`
`title` | To specify the position or job of the user | `string()` |   | `false`



#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users
```

#### Create

> PUT /v2/accounts/{ACCOUNT_ID}/users

```shell
curl -v -X PUT \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users
```

#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}
```

#### Change

> POST /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}

```shell
curl -v -X POST \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}
```

#### Patch

> PATCH /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}

```shell
curl -v -X PATCH \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}
```

#### Remove

> DELETE /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}

```shell
curl -v -X DELETE \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}
```

#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/vcard

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/vcard
```

#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo
```

#### Change

> POST /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo

```shell
curl -v -X POST \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo
```

#### Remove

> DELETE /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo

```shell
curl -v -X DELETE \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo
```

#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/quickcall/{PHONE_NUMBER}

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/quickcall/{PHONE_NUMBER}
```

