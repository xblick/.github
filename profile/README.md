
# Durchblick

Durchblick (`xblick`) is a framework for camera streams and perception nodes on one PC or several. Programs exchange images through shared memory and GPU memory on the same PC, and compressed over the network between PCs. It is built on [Zenoh](https://zenoh.io) and follows the message models of ROS 2.

## Start

```bash
pip install "xblick[cam]"
xblick router &
xblick cam                 # choose a webcam from the list
xblick view                # choose the stream; it opens in the browser
```

A first model on that camera, on the CPU: [xblick-yolox](https://github.com/xblick/xblick-yolox).

## Repositories

| Repository | What it is | Needs |
| --- | --- | --- |
| [xblick](https://github.com/xblick/xblick) | The core: streams, rings, the `xblick` command, the terminal interface | Linux |
| [xblick-relay](https://github.com/xblick/xblick-relay) | Brings streams from other PCs into the rings of this PC | Linux; a GPU optional |

**Cameras**

| Repository | Camera |
| --- | --- |
| `xblick cam` in the core | Webcams, capture cards, RTSP and HTTP streams |
| [xblick-azure-kinect](https://github.com/xblick/xblick-azure-kinect) | Azure Kinect, with body tracking |
| [xblick-roboception](https://github.com/xblick/xblick-roboception) | Roboception rc_visard |

**Models**

| Repository | Model | Result | Computes on | Terms of the model |
| --- | --- | --- | --- | --- |
| [xblick-yolox](https://github.com/xblick/xblick-yolox) | YOLOX | 2D detections | CPU or GPU | see its README |
| [xblick-rtdetrv4](https://github.com/xblick/xblick-rtdetrv4) | RT-DETRv4 | 2D detections | CPU or GPU | see its README |
| [xblick-sam3](https://github.com/xblick/xblick-sam3) | SAM 3.1 | Instance masks for words | GPU | SAM License |
| [xblick-tapnext](https://github.com/xblick/xblick-tapnext) | TAPNext++ | Point tracks | GPU | Apache-2.0 |
| [xblick-vjepa2](https://github.com/xblick/xblick-vjepa2) | V-JEPA 2 | Video features and actions | GPU | MIT |
| [xblick-gem-x](https://github.com/xblick/xblick-gem-x) | GEM-X | Body pose | GPU | see its README |
| [xblick-nemo](https://github.com/xblick/xblick-nemo) | NeMO | Object poses | GPU | non-commercial parts |
| [xblick-boxer](https://github.com/xblick/xblick-boxer) | Boxer | 3D boxes | GPU | non-commercial |

## Documentation

- [Install and a first stream](https://github.com/xblick/xblick/blob/main/docs/getting-started/install.md)
- [All documentation](https://github.com/xblick/xblick/blob/main/docs/README.md)
- [Changes](https://github.com/xblick/xblick/blob/main/CHANGELOG.md), [issues](https://github.com/xblick/xblick/issues)

## Origin

Durchblick was started by David Schneider at the [Computer Vision for Human-Computer Interaction Lab (cv:hci)](https://cvhci.iar.kit.edu) at KIT and is developed further in cooperation with the [High Performance Humanoid Technologies Lab (H2T)](https://h2t.iar.kit.edu) at KIT.
