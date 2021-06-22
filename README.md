# GitHub Codespaces
# Software example from the [Arm ML embedded evaluation kit](https://review.mlplatform.org/plugins/gitiles/ml/ethos-u/ml-embedded-evaluation-kit/+/HEAD/docs/documentation.md#arm_ml-embedded-evaluation-kit)

# Start GitHub Codespaces on this GitHub Project

# Arm Compiler 6 requires a FlexLM license to operate
To tell the GitHub Codespace where your FlexLM server set an environment variable
```bash
$ export ARMLMD\_LICENSE\_FILE=7010@licenseserver
```
You can also store the ARMLMD\_LICENSE\_FILE as a secret in Codespace. For more info check the [documentation about secrets](https://docs.github.com/en/codespaces/managing-your-codespaces/managing-encrypted-secrets-for-your-codespaces)

# Build the example software
```bash
$ ./build_software.sh
```

# Run the software on the FVP
```bash
$ FVP_Corstone_SSE-300_Ethos-U55 
```

# From another shell, telnet to the FVP
```
$ telnet localhost 10500
```

Use the menu to run the application.

