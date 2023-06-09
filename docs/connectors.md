Connectors provide standard interfaces for interacting with external calendar servers and other means
of persisting calendar and resource data.

## Overview

The default Connectors include support for local storage and DAV-compliant servers (i.e. CalDAV or 
CardDAV). A Connector instance is configured with an associated virtual path, which allows you to
configure multiple instances of the same Connector type.

### Local Storage

The default connector uses local file-based storage for managing your data. The benefits of this
connector include:

* Zero configuration default means you can use it immediately
* It's fast for creating new data
* Data is stored locally so less need to secure transports and connectivity with external systems

### CalDAV/CardDAV Server

The DAV connector is compliant with these popular standards for accessing and managing calendar and
resource data. The benefits of this connector include:

* Connectivity to existing calendaring systems such as Google, Radicale, Baikal, Zoho, etc.
* You can directly manipulate your calendars and contacts but continue to use your favourite clients

## Enable a Connector instance

Each connector instance is associated with a virtual path. For example the default connector using
local storage is configured with the following path:

    /local

To create a new local storage instance you would need to use a different path:

    coucal connector local /sandbox

If a connector does not yet have any instances you can omit the path to use the default path:

    coucal connector dav -host=dav.example.com # will use the default path of /dav


## Disable a Connector instance

TBD.
