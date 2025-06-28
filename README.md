# gren-turso

This package allows interfacing with both the [Turso Platform API](https://docs.turso.tech/api-reference/introduction) and the [libSQL remote protocal](https://docs.turso.tech/sdk/http/quickstart), which allows executing SQL statements for databases on Turso over HTTP.

## Turso Platform API

All modules related to the platform API are prefixed with `Platform` (i.e. `Turso.Platform.Database`), and deal with managing resources on Turso. For example, the `Turso.Platform.Groups` module allows adding, removing, or editing setting for groups within Turso.

To send queries to Turso, a `Turso.Platform.Connection` is required. Take a look at the `Turso.Platform` module for more information on how to construct a `Connection`.

The Turso platform API is not yet fully covered by this package. There is other functionality, such as managing your organizations users, that is not available. If you run into something that you need, please submit a ticket or add the functionality and submit a pull request!

## libSQL Remote Prototol (SQL over HTTP)

The libSQL remote protocol allows executing SQL queries over HTTP.

All modules related to the libSQL remote protocol are in the `Turso.Db` namespace. The `Turso.Db` module allows executing queries over HTTP, the `Turso.Db.Encode` allows encoding parameters for SQL queries, and the `Turso.Db.Decode` module allows decoding data resulting from queries.

To start sending queries to a Turso database, a `Turso.Db.Connection` is required. Take a look at the `Turso.Db` module for more information on how to construct a `Connection`.

## Tests

All functionality in this package is heavily tested. These tests can be found in the `integration_tests` directory in the source repository. See the `README.md` file in that folder for more information on how to run these tests.

Unit tests are located in the `tests` folder, and test the encoding and decoding functionality of database queries.
