# LDPlayer Automation Manager

A professional Python application for automating Facebook interactions using LDPlayer emulators. This tool provides automated scrolling and Reels posting capabilities with a modern GUI interface.

## cd D:\Application\Automation-LDPlayer-v1\src python app.py

## Features

- **Facebook Automation**: Automated scrolling and Reels posting
- **Multi-Device Management**: Control multiple LDPlayer instances simultaneously
- **Performance Monitoring**: Track success rates, task durations, and system metrics
- **Content Queue Management**: Organize and manage video content for posting
- **Task Scheduling**: Schedule automated tasks with flexible timing options
- **Backup & Restore**: Save and restore application settings and data
- **Modern GUI**: Clean, professional interface with real-time status updates

## Project Structure

```
src/
├── app.py                 # Main entry point
├── gui/                   # Graphical User Interface
│   ├── __init__.py
│   ├── ld_manager_app.py  # Main application window
│   ├── main_window.py     # Automation control window
│   └── checkbox_treeview.py # Enhanced treeview with checkboxes
├── core/                  # Core business logic
│   ├── __init__.py
│   ├── emulator.py        # LDPlayer control and management
│   ├── managers.py        # Account, content, and task management
│   └── task_handlers.py   # Facebook automation task handlers
└── utils/                 # Utility modules
    ├── __init__.py
    ├── app_utils.py       # General application utilities
    ├── error_handler.py   # Enhanced error handling
    ├── performance_monitor.py # Performance tracking
    ├── rate_limiter.py    # Rate limiting functionality
    ├── activity_randomizer.py # Randomization utilities
    └── toast.py           # Toast notification system
```

## Installation

1. **Prerequisites**:
   - Python 3.8+
   - LDPlayer installed and configured
   - uiautomator2 (optional, for enhanced automation)

2. **Install Dependencies**:
   ```bash
   pip install tkinter uiautomator2 psutil
   ```

3. **Run the Application**:
   ```bash
   cd src
   python app.py
   ```

## Usage

### Basic Operation

1. **Launch the Application**:
   ```bash
   python app.py
   ```

2. **Configure Settings**:
   - Set parallel LD instances
   - Configure boot delays and task durations
   - Choose task type (Facebook Active or Post Reels)

3. **Select Devices**:
   - Use the device table to select LDPlayer instances
   - Check/uncheck devices for batch operations

4. **Start Automation**:
   - Click "Start Automation" to begin tasks
   - Monitor progress in the activity log

### Task Types

#### Facebook Active (Scrolling)
- Automates natural scrolling behavior on Facebook
- Configurable intensity and duration
- Includes random delays for human-like behavior

#### Post Reels
- Automatically posts videos to Facebook Reels
- Uses content queue for video management
- Handles Facebook permission dialogs
- Supports captions and hashtags

### Advanced Features

#### Content Management
- Add videos individually or load entire folders
- Automatic caption and hashtag generation
- Queue management with usage tracking

#### Scheduling
- Daily or weekly task scheduling
- Configurable repeat intervals
- Automatic execution at specified times

#### Performance Monitoring
- Real-time analytics dashboard
- Success rate tracking
- Task duration monitoring
- System resource usage

## Configuration

Settings are automatically saved to `./config/setting.json`:

```json
{
  "parallel_ld": 2,
  "boot_delay": 10,
  "task_duration": 15,
  "max_videos": 2,
  "start_same_time": false,
  "use_content_queue": true
}
```

## Troubleshooting

### Common Issues

1. **LDPlayer Not Detected**:
   - Ensure LDPlayer is installed and running
   - Check administrator privileges for console access
   - Verify LDPlayer path in emulator configuration

2. **ADB Connection Issues**:
   - Restart ADB server: `adb kill-server && adb start-server`
   - Check device connections: `adb devices`
   - Verify emulator ports are available

3. **Import Errors**:
   - Ensure all dependencies are installed
   - Check Python path includes project directory
   - Verify package structure is intact

### Logs and Debugging

- Check the activity log in the GUI for real-time information
- Console output provides additional debugging information
- Performance reports available in Tools menu

## Development

### Adding New Features

1. **GUI Components**: Add to `gui/` package
2. **Business Logic**: Implement in `core/` package
3. **Utilities**: Place in `utils/` package

### Code Style

- Follow PEP 8 conventions
- Use type hints where appropriate
- Include docstrings for classes and methods
- Maintain separation of concerns

## License

This project is provided as-is for educational and personal use.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## Support

For issues and questions:
1. Check the troubleshooting section
2. Review the activity logs
3. Ensure all prerequisites are met
4. Test with minimal configuration first