<div id="top"></div>

<div style="text-align:center"><img src="images/cover_image.jpg" /></div>

## 1. APIAssure

Is your API is out of control? Is testing getting harder? Then get APIAssure!
It's very easy to use!

### 1.1 Requirements

- Container: [Docker](https://www.docker.com/products/docker-desktop)
- Makefile: [Make](https://www.gnu.org/software/make/)
- Testing Framework: [Pytest](https://docs.pytest.org/en/7.2.x/)


## 2. Getting Started

1. Clone APIAssure.

```bash
git clone https://github.com/ErolGelbul/api_assure.git
```

2. Create secrets inside <secrets.ini>:

```bash
APP_URL=http://host.docker.internal:8080
ADMIN_USER=admin
ADMIN_PASSWORD=admin
```

3. Start development server:

```bash
make dev
```

## 3. Features

1. Logging
2. Automated end to end scenarios.
3. Pytest Fixtures

## 4. Components

### 4.1 utils.py

The build_request_headers function is used to build a dictionary containing the
necessary headers for making API requests, such as the Authorization and accept
headers. It can also include a Content-Type header if specified in the
function's arguments.

### 4.2 users.py (example)

> CRUD operation on Users.

The users.py file defines a Users class that provides methods for interacting
with the user-related endpoints of an API. The class contains the following
methods:


- get_all_users: Retrieves a list of all users.
- create_user: Creates a new user with a specified username, password, and role.
- get_current_user: Gets information about the currently authenticated user.
- delete_user: Deletes a user with a specified user ID.

These methods make HTTP requests to the API using the provided app_url,
access_token, and other necessary parameters. The build_request_headers function
from lib.utils is used to generate the required headers for each request. The
SESSION object from the config module is used to manage the HTTP requests.

### 4.3 conftest.py

Contains the login_as_admin Pytest fixture, which logs in
as an admin user and provides an access token for use in test functions. The
fixture has a session scope, meaning it's executed only once per test session.
To use this fixture, include it as a parameter in your test functions, which
will then have access to the admin user's access token.



## 5. Contributing

If you would like to add any extra features to the optimisation simulation, feel free to fork and create a pull request. Thank you!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- CONTACT -->
## 6. Contact

Erol Gelbul - [Website](http://www.erolgelbul.com)

Project Link: [APIAssure](https://github.com/ErolGelbul/APIAssure)

<p align="right">(<a href="#top">back to top</a>)</p>

