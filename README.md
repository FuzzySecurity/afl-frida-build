# Afl++ Frida Mode Build

This playbook automates building an `Afl++ Frida-Mode` toolchain for `MAC Arm64`. Pull requests are welcome to expand the playbook to other architectures.

You can adjust which `platform version` and `afl release tag` you want to build for by adjusting the variables at the top of the playbook.

```yml
---
- name: AFL++ Frida-Mode MAC ARM64 Build
  hosts: localhost
  gather_facts: yes
  vars:
    ANDROID_PLATFORM: 31 # Platform version to build for
    AFL_TAG: "latest"    # Use "latest" or set to specific tag (e.g. "v4.08c")
```

#### Running the playbook

```
ansible-playbook fuzz-build.yml
```

https://github.com/FuzzySecurity/afl-frida-build/assets/10997340/1b21a19a-e18a-4fc5-82b8-8fb8356bb45e


#### Background context

You can read this post to understand more about where this need comes from.

- Fuzzing Redux, leveraging AFL++ Frida-Mode on Android native libraries - [here](#)
