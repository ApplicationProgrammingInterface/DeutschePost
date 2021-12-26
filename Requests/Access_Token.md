
[Overview]: ..
[Endpoint]: Overview.html

<!--―――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――-->

**[🠔 Overview][Overview]**

---

## Access Token

**OAuth 2.0 Tokens** can be requested with different permissions ( `scopes` ).

---

### Retrieve

To request a **Token** you have to encode your **Credentials**.

`Authentication-Code`<br>
  ` = Base64( 'Client-Id' + ':' + 'Client-Secret' )`

<br>

##### Example

<table>
    <tr align='center'>
        <th>Id</th>
        <td><code>1932b677-269a-456c-825d-52b11e395419</code></td>
    </tr>
    <tr align='center'>
        <th>Secret</th>
        <td><code>71ebf780-f541-4d8b-a28e-f4663d90b006</code></td>
    </tr>
    <tr align='center'>
        <th>Authentication<br>Code</th>
        <td>
            <code>MTkzMmI2NzctMjY5YS00NTZjLTgyNWQtNTJi</code><br>
            <code>MTFlMzk1NDE5OjcxZWJmNzgwLWY1NDEtNGQ4</code><br>
            <code>Yi1hMjhlLWY0NjYzZDkwYjAwNg==</code>
        </td>
    </tr>
</table>

<br>

Now simply send a **GET** request to the <br>
**[Endpoint]** with the following properties:

<table>
    <tr align='center'>
        <th>Content-Type</th>
        <td><code>application/json</code></td>
    </tr>
    <tr align='center'>
        <th>Accept</th>
        <td><code></code></td>
    </tr>
    <tr align='center'>
        <th>Authorization<br>Code</th>
        <td><b>[ Authentication Code ]</b></td>
    </tr>
</table>

<br>

A ***successful*** response will be in the format of:

```json
{
    "access_token" : "hk7jh654g46hg4546..." ,
    "token_type"   : "Bearer" ,
    "expires_in"   : 18000 ,
    "scope"        : "dpilabel dpitracking"
}
```

`token_type`: <br>
  Type of the **OAuth 2.0 Token**, <br>
  not relevant, can be ignored.

`expires_in`: <br>
  Time in seconds, <br>
  default: `18000` ➔ `5 hours`.

`scope`: <br>
  What **API** access this token grants.


---

### Info



### Revoke
