Repository to store generated PKI for HAB secure boot

To generate ca certs for HABv4 signing, ensure you have your own
key_pass.txt, and serial in keys folder, and run the following command.

For pre imx-cst v3.1.1 version
`$ .\hab4_pki_tree.sh -existing-ca n -use-ecc n -kl 2048 -duration 5 -num-srk 4 -srk-ca y`

For post imx-cst v3.4.0 version
`$ .\hab4_pki_tree.sh -existing-ca n -kt rsa -kl 2048 -duration 5 -num-srk 4 -srk-ca y`

Contents of key_pass.txt and serial
key_pass.txt: (default is test, test)
`!mysecretkey`
`!mysecretkey`

serial: (default is 12345678)
`20260101`
