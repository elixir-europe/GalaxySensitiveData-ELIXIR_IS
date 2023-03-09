# ELIXIR: Strengthen Data Management in Galaxy
### WP2: Sensitive Data Accessing and Processing in Galaxy

Encryption is usually performed at the file system level, encrypting the whole volume (or partition) attached to the server hosting Galaxy. This approach does not easily fit into a user-level encryption strategy, as it requires that the privacy of users’ data can safely be entrusted to the Galaxy instance administrator(s) and also does not provide proper separation of data between users. This approach is still fine for small- to medium-sized private instances.

Adding support for data encryption at the user level requires a change of approach that needs to be carefully explored since it would require some substantial adaptation to the way Galaxy manages user data, including when used as input for tools and workflows. It will be crucial to design a secure solution for the management of dataset access privileges, for both end-users and computational nodes (e.g. for making sure that the user data can only be decrypted in certain locations - related to task 1.3). We will build on the Crypt4GH standard which allows the content of a data file to be read while it remains encrypted. 
During the Implementation Study, we will explore the possibility of introducing a secure user-level data encryption strategy into Galaxy, also considering the needs of Pulsar, and provide a proof-of-concept implementation of this feature in Galaxy. 

### Proof-of-concept implementation

This repository centralizes the software and documents produced as part of WP2:

- https://github.com/elixir-europe/galaxy-is-wp2
- https://github.com/elixir-europe/GalaxySensitiveData-IS_py-recryptor
