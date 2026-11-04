# RobotLens Releases

Official downloads of [RobotLens](https://robotlens.dev), a robotics studio for
Ubuntu 24.04 and ROS 2 Jazzy. This repository holds release files only; the
source code is not published.

Download the latest version from the
[Releases page](https://github.com/NarinderBrar/RobotLens-Releases/releases).

## What is RobotLens?

RobotLens brings your robot's topology, live data, 3D world, simulation, logs
and timeline into one native desktop workspace, so you spend less time
switching tools and more time solving the real problem. It works alongside the
ROS 2 tools you already use.

- **See the whole system:** a hierarchy and live node graph of nodes, topics,
  services, TF frames and robots, with one shared selection across every panel.
- **Visualize in 3D:** Vulkan rendering of URDF, SDF and MJCF robots, TF trees,
  joint motion, sensor data, maps, paths and markers.
- **Simulate and navigate:** built-in MuJoCo simulation, Nav2 profile and
  costmap generation, and 3D goal dispatch.
- **Edit scenes and projects:** a robot catalog, STL/DAE/OBJ/glTF mesh loading,
  transform gizmos, lights, cameras and full undo/redo.
- **Debug with evidence:** health findings, live `/diagnostics` and `/rosout`,
  message inspection, signal plots and topic recording and playback.
- **Stay in flow:** integrated build and interactive terminals, a project file
  explorer and Run/Stop controls for ROS launch files.
- **Ask the assistant:** an optional AI assistant that answers questions about
  the running system with cited evidence; the engineer stays in charge.

Learn more at [robotlens.dev](https://robotlens.dev).

## Requirements

- Ubuntu 24.04, 64-bit PC (amd64)
- The ROS 2 Jazzy apt repository
  ([setup guide](https://docs.ros.org/en/jazzy/Installation/Ubuntu-Install-Debs.html))

## Install

```bash
sudo apt update
sudo apt install ./robotlens_0.1.0_amd64.deb
robotlens
```

apt installs the required ROS and system libraries. To remove RobotLens:
`sudo apt remove robotlens`.

## Verify the download

Each release includes the package, a detached signature (`.asc`), a SHA-256
checksum and the RobotLens signing key.

```bash
sha256sum -c robotlens_0.1.0_amd64.sha256
gpg --import robotlens-signing-key.asc
gpg --verify robotlens_0.1.0_amd64.deb.asc robotlens_0.1.0_amd64.deb
```

The last command must report a good signature from
`RobotLens Release <robotlensworkspace@gmail.com>` with this fingerprint:

```text
C12C EF4A 49E7 83A1 2D6F  AD26 44E2 9058 8B60 7342
```

## Community

Questions, bug reports, feedback and showcases are welcome on the
[RobotLens Discord](https://discord.gg/Yaawrg3BbJ).

## License

RobotLens is free for personal, educational and non-commercial academic use.
Commercial use needs a separate license; see [robotlens.dev](https://robotlens.dev).
Full terms are in [LICENSE](LICENSE). Third-party notices are installed with the
package in `/usr/share/doc/robotlens/THIRD_PARTY_NOTICES.md`.

This repository is an official download source authorized by the copyright
holder. Please do not redistribute the package elsewhere.
