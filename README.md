# CPU Tracker X

CPU Tracker X is a professional-grade telemetry overlay for Windows, designed to provide real-time hardware monitoring data in a non-intrusive, customizable desktop interface. Built using .NET 8.0 and WPF, it leverages the LibreHardwareMonitor library to deliver accurate performance statistics for workstations and gaming systems.

## Key Features

### Hardware Telemetry
*   **CPU Monitoring**: Real-time tracking of total CPU load, individual core statistics, and package temperatures.
*   **GPU Monitoring**: Support for NVIDIA, AMD, and Intel graphics processors, providing load, temperature, and VRAM utilization metrics.
*   **Memory Analysis**: Continuous monitoring of system RAM load.
*   **Storage Activity**: Live tracking of disk read and write activity percentages.
*   **Network Performance**: Real-time throughput reporting for upload and download speeds, along with network latency (Ping) monitoring.
*   **Performance Metrics**: Precise FPS and Frametime tracking using ETW (Event Tracing for Windows).

### Advanced Customization
*   **Dynamic Styling**: Full control over color palettes for every individual metric, allowing for seamless integration with any desktop aesthetic.
*   **Typography and Transparency**: Support for custom system fonts and adjustable background opacity levels.
*   **Intelligent Positioning**: Snap-to-edge functionality for all four corners of the screen, or manual "Unlocked" positioning for precise placement.
*   **Global Hotkeys**: Custom keyboard shortcuts (e.g., Ctrl+Shift+O) to toggle the overlay visibility instantly.

### User Interface
*   **Minimalist Design**: A borderless, transparent overlay that sits above or behind other windows based on user preference.
*   **System Integration**: Runs silently in the system tray with an integrated context menu for quick settings access.
*   **Automation**: Option to launch automatically on Windows startup.

## Requirements

*   **Operating System**: Windows 10 or Windows 11.
*   **Runtime**: .NET 8.0 Desktop Runtime.
*   **Permissions**: Administrator privileges are required to access low-level hardware sensors through the driver interface.

## Installation

1.  Download the latest release executable.
2.  Ensure .NET 8.0 is installed on your system.
3.  Execute `CpuGpuOverlay.exe` as Administrator.

## Configuration

Settings are managed through a dedicated graphical interface accessible via:
*   Right-clicking the System Tray icon and selecting **Settings**.
*   Clicking the Settings icon on the overlay (visible when hovering over the window).

Configuration data is persisted in a `settings.json` file located in the application directory.

## Technical Architecture

CPU Tracker X is architected for low overhead and high precision:
*   **Framework**: Windows Presentation Foundation (WPF) with .NET 8.0.
*   **Hardware Abstraction**: Utilizes `LibreHardwareMonitorLib` for multi-vendor hardware sensor support.
*   **Performance Tracking**: Employs `Microsoft.Diagnostics.Tracing.TraceEvent` for low-latency kernel-level performance monitoring.
*   **Configuration**: JSON-based asynchronous persistence for application state.

## License

This project is intended for personal and professional hardware monitoring. Please refer to the specific license terms of the utilized libraries (LibreHardwareMonitor and TraceEvent) for third-party compliance.
