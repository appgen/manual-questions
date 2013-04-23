Manual app questions
================
Here we copy answers to the following questions

* __What__ are you making?
* __Why__ are you making it?
* What do you __need__ help with?

Each directory within the present directory contains to the three answers for
a particular entity (app, person, company, department, &c.), in files named
`what`, `why` and `need`. The directory name is used as a unique identifier.

The following search finds LinkedIn InMails and creates directories for them.

    notmuch show from:hit-reply@linkedin.com |
    sed -n 's/.*id:\([^ ]*\) .*/\1/p' |
    xargs mkdir
