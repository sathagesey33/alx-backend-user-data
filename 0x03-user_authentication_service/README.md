#0x03. User authentication service
##About

### A session based user authentication API
Files

    app.py: API entry point
    auth.py: authentication model
    db.py: database model
    user.py: user model
    main.py: end-to-end integration tests

#### Setup

$ pip3 install -r requirements.txt

Run

$ flask run

Routes

    GET /: returns logout message when user is logged out
    GET /profile returns email of logged in user
    POST /users: creates new user (Form data: email, password)
    POST /sessions: logs in existing user(Form data: email, password)
    POST /reset_password: returns password reset token (Form data: email)
    PUT /reset_password: updates existing user's password (Form data: email, new_password, reset_token)
    DELETE /sessions: logs out user
