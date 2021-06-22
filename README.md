# Script to build an software example from the [Arm ML embedded evaluation kit](https://review.mlplatform.org/plugins/gitiles/ml/ethos-u/ml-embedded-evaluation-kit/+/HEAD/docs/documentation.md#arm_ml-embedded-evaluation-kit)

Pull the docker image:
```bash
$ docker pull armsw/arm-tools:corstone-300-ml-eval-kit
```

Run using the run.sh script:
```bash
$ ./run.sh
```

# Passing the license server to the containers
To tell the containers where your FlexLM server is located use -e to pass an environment variable and insert your license server.

$ ./run.sh -e ARMLMD\_LICENSE\_FILE=7010@licenseserver


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

