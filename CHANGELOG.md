# Changelog

All notable changes to `webklex/php-imap` will be documented in this file.

Updates should follow the [Keep a CHANGELOG](http://keepachangelog.com/) principles.

## [UNRELEASED]
### Fixed
- NaN

### Added
- NaN

### Affected Classes
- NaN

## [2.1.7] - 2020-10-03
### Fixed
- Fixed `Query::paginate()` (#13 #14 by [@Max13](https://github.com/Max13))

## [2.1.6] - 2020-10-02
### Fixed
- `Message::getAttributes()` hasn't returned all parameters

### Added
- Part number added to attachment
- `Client::getFolderByPath()` added (#12 by [@Max13](https://github.com/Max13))
- `Client::getFolderByName()` added (#12 by [@Max13](https://github.com/Max13))
- Throws exceptions if the authentication fails  (#11 by [@Max13](https://github.com/Max13))

### Affected Classes
- [Client::class](src/Client.php)

## [2.1.5] - 2020-09-30
### Fixed
- Wrong message content property reference fixed (#10)

## [2.1.4] - 2020-09-30
### Fixed
- Fix header extension values
- Part header detection method changed (#10)

### Affected Classes
- [Header::class](src/Header.php)
- [Part::class](src/Part.php)

## [2.1.3] - 2020-09-29
### Fixed
- Possible decoding problem fixed
- `Str::class` dependency removed from `Header::class`

### Affected Classes
- [Header::class](src/Header.php)

## [2.1.2] - 2020-09-28
### Fixed
- Dependency problem in `Attachement::getExtension()` fixed (#9)

### Affected Classes
- [Attachment::class](src/Attachment.php)

## [2.1.1] - 2020-09-23
### Fixed
- Missing default config parameter added

### Added
- Default account config fallback added

### Affected Classes
- [Client::class](src/Client.php)

## [2.1.0] - 2020-09-22
### Fixed
- Quota handling fixed

### Added
- Event system and callbacks added

### Affected Classes
- [Client::class](src/Client.php)
- [Folder::class](src/Folder.php)
- [Message::class](src/Message.php)

## [2.0.1] - 2020-09-20
### Fixed
- Carbon dependency fixed

## [2.0.0] - 2020-09-20
### Fixed
- Missing pagination item records fixed

### Added
- php-imap module replaced by direct socket communication
- Legacy support added
- IDLE support added
- oAuth support added
- Charset detection method updated
- Decoding fallback charsets added

### Affected Classes
- All

## [1.4.5] - 2019-01-23
### Fixed
- .csv attachement is not processed
- mail part structure property comparison changed to lowercase
- Replace helper functions for Laravel 6.0 #4 (@koenhoeijmakers)
- Date handling in Folder::appendMessage() fixed
- Carbon Exception Parse Data
- Convert sender name from non-utf8 to uf8 (@hwilok)
- Convert encoding of personal data struct

### Added
- Path prefix option added to Client::getFolder() method
- Attachment size handling added
- Find messages by custom search criteria

### Affected Classes
- [Query::class](src/Query/WhereQuery.php)
- [Mask::class](src/Support/Masks/Mask.php)
- [Attachment::class](src/Attachment.php)
- [Client::class](src/Client.php)
- [Folder::class](src/Folder.php)
- [Message::class](src/Message.php)

## [1.4.2.1] - 2019-07-03
### Fixed
- Error in Attachment::__construct #3
- Examples added

## [1.4.2] - 2019-07-02
### Fixed
- Pagination count total bug #213
- Changed internal message move and copy methods #210
- Query::since() query returning empty response #215
- Carbon Exception Parse Data #45
- Reading a blank body (text / html) but only from this sender #203
- Problem with Message::moveToFolder() and multiple moves #31
- Problem with encoding conversion #203
- Message null value attribute problem fixed
- Client connection path handling changed to be handled inside the calling method #31
- iconv(): error suppressor for //IGNORE added #184
- Typo Folder attribute fullName changed to full_name
- Query scope error fixed #153
- Replace embedded image with URL #151
- Fix sender name in non-latin emails sent from Gmail (#155)
- Fix broken non-latin characters in body in ASCII (us-ascii) charset #156
- Message::getMessageId() returns wrong value #197
- Message date validation extended #45 #192
- Removed "-i" from "iso-8859-8-i" in Message::parseBody #146

### Added
- Message::getFolder() method
- Create a fast count method for queries #216
- STARTTLS encryption alias added
- Mailbox fetching exception added #201
- Message::moveToFolder() fetches new Message::class afterwards #31
- Message structure accessor added #182
- Shadow Imap const class added #188
- Connectable "NOT" queries added
- Additional where methods added
- Message attribute handling changed
- Attachment attribute handling changed
- Message flag handling updated
- Message::getHTMLBody($callback) extended
- Masks added (take look at the examples for more information on masks)
- More examples added
- Query::paginate() method added
- Imap client timeout can be modified and read #186
- Decoder config options added #175
- Message search criteria "NOT" added #181
- Invalid message date exception added 
- Blade examples

### Breaking changes
- Message::moveToFolder() returns either a Message::class instance or null and not a boolean
- Folder::fullName is now Folder::full_name
- Attachment::image_src might no longer work as expected - use Attachment::getImageSrc() instead

### Affected Classes
- [Folder::class](src/Folder.php)
- [Client::class](src/Client.php)
- [Message::class](src/Message.php)
- [Attachment::class](src/Attachment.php)
- [Query::class](src/Query/Query.php)
- [WhereQuery::class](src/Query/WhereQuery.php)

## 0.0.3 - 2018-12-02
### Fixed
- Folder delimiter check added #137
- Config setting not getting loaded
- Date parsing updated

### Affected Classes
- [Folder::class](src/IMAP/Client.php)
- [Folder::class](src/IMAP/Message.php)

## 0.0.1 - 2018-08-13
### Added
- new php-imap package (fork from [webklex/laravel-imap](https://github.com/Webklex/laravel-imap))
