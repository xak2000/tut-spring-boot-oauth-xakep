# Login

As user:

```
curl crizcroz-android:crizcroz-android-secret@localhost:8080/oauth/token -d grant_type=password -d username=user -d password=user-secret
```

As dealer:

```
curl crizcroz-android:crizcroz-android-secret@localhost:8080/oauth/token -d grant_type=password -d username=dealer -d password=dealer-secret
```

Example output

```
{
    "access_token":"517d80d5-7f08-42f4-8865-857a8e675f2f",
    "token_type":"bearer",
    "refresh_token":"3ff534dc-462b-48f5-b474-5dd49b7d1360",
    "expires_in":43145,
    "scope":"read write"
}
```

# Refresh token

```
curl crizcroz-android:crizcroz-android-secret@localhost:8080/oauth/token -d grant_type=refresh_token -d refresh_token=1419a1bb-f4fe-4b3d-94a9-5d0dc0b87a55
```

# Make API request

```
curl localhost:8081/user?access_token=517d80d5-7f08-42f4-8865-857a8e675f2f
```
