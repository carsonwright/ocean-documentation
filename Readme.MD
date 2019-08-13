# Next In Line - Scheduling Assistant API (Ocean - Shark) Documentation

## Authenticate

| Request |                                                       |
|------| :-----                                           |
| Url | https://shark.nextinline.io/accounts/authenticate |
| Method | PUT |
| Body | ```{"value": "youradministratoremail@example.com", "password": "Here Is Your Password"}``` |

##### Example
```
curl -X PUT https://shark.nextinline.io/accounts/authenticate \
-d '{"value": "youradministratoremail@example.com", "password": "Here Is Your Password"}'
```

## Accounts
### Fetch Accounts
| Request     |         |
|------| :----- |
| Url | https://shark.nextinline.io/organizations/yourOrganizationID/accounts |
| Parameters | limit=number&search=value |
| Method | GET |

```
curl 'https://shark.nextinline.io/organizations/be7d846d-4409-4c47-a2e5-d2185a24d91f/accounts?limit=5&search=a' -H 'Accept: application/json, text/plain, */*' -H 'x-token: xI7RHW6iU6B7I3DsU4xb93IinRCefzaf'
```

## Appointments
### Fetch Appointments

| Request     |         |
|------| :----- |
| Url | https://shark.nextinline.io/organizations/yourOrganizationID/appointments |
| Method | GET |

##### Example
```
curl -X PUT https://shark.nextinline.io/organizations/be7d846d-4409-4c47-a2e5-d2185a24d91f/appointments
```


### Create Appointment

| Request     |         |
|------| :----- | 
| Url  | https://shark.nextinline.io/organizations/yourOrganizationID/appointments |
| Method | POST |
| Body | ```{"reason":"A Test For Next In Line","accountID":"theAccountID","patientID":"thePatientID","administratorID":"theDesiredAdministratorID","appointmentTypeID":"theAppointmentTypeID","startsAt":"2019-08-14T06:15:00-04:00","endsAt":"2019-08-14T06:45:00-04:00"}``` |

##### Example
```
curl -X POST https://shark.nextinline.io/organizations/be7d846d-4409-4c47-a2e5-d2185a24d91f/appointments \ 
-d '{"reason":"A Test For Next In Line","accountID":"4e47436e-2c1e-422b-b5ac-59a38f3df512","patientID":"efca9b46-47f8-4414-92ec-5bd7ce9d7a4f","administratorID":"5428e3a0-3ac9-4a36-bf7a-abc5141d223f","appointmentTypeID":"d793d9fd-8597-46aa-9313-d5b192b80ccb","startsAt":"2019-08-14T06:15:00-04:00","endsAt":"2019-08-14T06:45:00-04:00"}'
```