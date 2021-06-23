# [GitHub Codespaces](https://github.com/features/codespaces) and [Gitpod](https://gitpod.io)
## Software example from the [Arm ML embedded evaluation kit](https://review.mlplatform.org/plugins/gitiles/ml/ethos-u/ml-embedded-evaluation-kit/+/HEAD/docs/documentation.md#arm_ml-embedded-evaluation-kit)

### To get started open a GitHub Codespace or a [Gitpod workspace](https://gitpod.io/#https://github.com/jasonrandrews/ml-embedded-eval-kit-example) on this project!

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

### Run the software on the FVP
```bash
$ FVP_Corstone_SSE-300_Ethos-U55 -f FVP_config.txt -a ml-embedded-evaluation-kit/build/bin/ethos-u-img_class.axf
```

### From another shell, telnet to the FVP
```
$ telnet localhost 10500
```

Use the menu to run the application.

