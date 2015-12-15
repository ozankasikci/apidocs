---
category: User
path: '/-/api/user/create'
title: 'Create User'
type: 'POST'

---

This method allows API consumers to create new users for their Koding teams.

### Authentication

* The headers must include a **valid authentication token**.
```Authentication: Bearer {TOKEN}```


### Parameters

* **email** (_required_)
  * should be a valid email address, must not be used before.

* **username** (_required when there is no suggestedUsername_)
  * should be between 4-25 characters, can contain lowercase alphanumerics and dashes

* **suggestedUsername** (_required when there is no username_)
  * should be between 4-15 characters, can contain lowercase alphanumerics and dashes

* **firstName** (_optional_)

* **lastName** (_optional_)

### Response

**If succeeds**, returns the username of the newly created user.
```{
  data : {
    username : 'username'
  }
}```

For error responses, see the [error responses documentation](#/error-responses).