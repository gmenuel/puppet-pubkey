# Reference

<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

### Defined types

#### Public Defined types

* [`pubkey::ssh`](#pubkey--ssh): Generate ssh key pair and exports public ssh key

#### Private Defined types

* `pubkey::keygen`: Internal class to validate detected parameters

### Data types

* [`Pubkey::Type`](#Pubkey--Type)

## Defined types

### <a name="pubkey--ssh"></a>`pubkey::ssh`

Exports public ssh key to Puppetserver

#### Examples

##### 

```puppet
pubkey::ssh { 'john_rsa': }
```

#### Parameters

The following parameters are available in the `pubkey::ssh` defined type:

* [`user`](#-pubkey--ssh--user)
* [`type`](#-pubkey--ssh--type)
* [`home`](#-pubkey--ssh--home)
* [`prefix`](#-pubkey--ssh--prefix)
* [`comment`](#-pubkey--ssh--comment)
* [`size`](#-pubkey--ssh--size)
* [`tags`](#-pubkey--ssh--tags)
* [`export_key`](#-pubkey--ssh--export_key)
* [`path`](#-pubkey--ssh--path)
* [`hostname`](#-pubkey--ssh--hostname)
* [`separator`](#-pubkey--ssh--separator)

##### <a name="-pubkey--ssh--user"></a>`user`

Data type: `Optional[String[1]]`

account name under which we will store the ssh key

Default value: `undef`

##### <a name="-pubkey--ssh--type"></a>`type`

Data type: `Optional[Pubkey::Type]`

ssh key type one of: 'dsa', 'rsa', 'ecdsa', 'ed25519', 'ecdsa-sk', 'ed25519-sk'

Default value: `undef`

##### <a name="-pubkey--ssh--home"></a>`home`

Data type: `Optional[Stdlib::UnixPath]`

user's home directory, assuming .ssh is located in $HOME/.ssh

Default value: `undef`

##### <a name="-pubkey--ssh--prefix"></a>`prefix`

Data type: `Optional[String[1]]`

custom key file prefix for the ssh key file (default: 'id')

Default value: `undef`

##### <a name="-pubkey--ssh--comment"></a>`comment`

Data type: `Optional[String[1]]`

ssh key's comment

Default value: `undef`

##### <a name="-pubkey--ssh--size"></a>`size`

Data type: `Optional[Integer]`

number of bits for generated ssh key

Default value: `undef`

##### <a name="-pubkey--ssh--tags"></a>`tags`

Data type: `Optional[Array[String]]`

optional tags added to the exported key

Default value: `undef`

##### <a name="-pubkey--ssh--export_key"></a>`export_key`

Data type: `Boolean`

whether export the generated key (default: true)

Default value: `true`

##### <a name="-pubkey--ssh--path"></a>`path`

Data type: `Stdlib::AbsolutePath`

standard unix path to look for ssh-keygen

Default value: `$facts['path']`

##### <a name="-pubkey--ssh--hostname"></a>`hostname`

Data type: `String`

that will be part of exported resource

Default value: `$facts['networking']['fqdn']`

##### <a name="-pubkey--ssh--separator"></a>`separator`

Data type: `String[1]`

A character for user and type auto-detection (default: '_')

Default value: `'_'`

## Data types

### <a name="Pubkey--Type"></a>`Pubkey::Type`

The Pubkey::Type data type.

Alias of `Enum['dsa', 'rsa', 'ecdsa', 'ed25519', 'ecdsa-sk', 'ed25519-sk']`
