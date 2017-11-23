WinSSHFS
========================

Fork of Asad Saeeduddin's WinSSHFS fork. Adds automatic ILmerge facilities so all assemblies are merged into a single executable.

CLI usage is:

```
SSHFS 1.0.0.0
Copyright c  2017

  -d, --drive-letter    Required. Drive letter to mount the remote SFTP path
                        under

  -r, --path            Required. Absolute path of directory to be mounted from
                        remote system

  -h, --host            Required. IP or hostname of remote host

  -p, --port            (Default: 22) SSH service port on remote server

  -u, --username        Required. Name of SSH user on remote system

  -x, --password        SSH user's password, if password-based or
                        keyboard-interactive auth should be attempted

  -k, --private-keys    SSH user's private key(s), if key-based auth should be
                        attempted
```

Prepare Git submodules
========================

```
git submodule update --init --recursive
```

Build Instructions
========================

CLI

```
nuget install
msbuild Sshfs\Sshfs.sln /p:Configuration=Release
```

Visual Studio

```
Install the Nuget dependencies using VS
Build the solution in Release mode
```


The CLI application will now be located at Sshfs\SSHFS.CLI\bin\Release\SSHFS.CLI.exe



