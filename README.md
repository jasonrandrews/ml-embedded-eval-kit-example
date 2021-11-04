# [GitHub Codespaces](https://github.com/features/codespaces) and [Gitpod](https://gitpod.io)
## Software examples from the [Arm ML embedded evaluation kit](https://review.mlplatform.org/plugins/gitiles/ml/ethos-u/ml-embedded-evaluation-kit/+/HEAD/docs/documentation.md#arm_ml-embedded-evaluation-kit)

To get started open a GitHub Codespace or a [Gitpod workspace](https://gitpod.io/#https://github.com/jasonrandrews/ml-embedded-eval-kit-example) on this project!

The default compiler is gcc for the applications and it is pre-installed in the container. To use Arm Compiler 6 follow the instructions below. 

### Configure Flex license for Compiler 6 

To tell the GitHub Codespaces or Gitpod where your Flex server is located set an environment variable
```bash
$ export ARMLMD_LICENSE_FILE=/workspaces/ml-embedded-eval-kit-example/license.dat
```
You can also store the ARMLMD\_LICENSE\_FILE as a secret in Codespace. For more info check the [documentation about secrets](https://docs.github.com/en/codespaces/managing-your-codespaces/managing-encrypted-secrets-for-your-codespaces)

### Build the example software

```bash
$ ./build_software.sh
```

To change the numbers of MAC, for example to 64: 
```
$ ./build_software.sh -n 64
```

The default compiler is GNU gcc. To change to the Arm Compiler (armclang):
```
$ ./build_software.sh -t arm
```

### Run the software on the FVP

Default number of MACs and default compiler:

```bash
$ ./run.sh
```

To run using an application compiled with Arm Compiler:
```bash
$ ./run.sh -t arm
```

To change the number of MACs use the -n option:
```bash
$ ./run.sh -n 64
```

### From another shell, telnet to the FVP
```
$ telnet localhost 10500
```

Use the menu to run the application.

