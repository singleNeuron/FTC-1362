# ftc_app
FTC Android Studio project to create FTC Robot Controller app.

This is the FTC SDK that can be used to create an FTC Robot Controller app, with custom op modes.
The FTC Robot Controller app is designed to work in conjunction with the FTC Driver Station app.
The FTC Driver Station app is available through Google Play.

To use this SDK, download/clone the entire project to your local computer.

*** Important note regarding the repository size ***:  this repository is large and it can take a long time and a lot of space to clone the entire repository. If you would like to save time and space, there are some options that you can choose to download only the most current version of the Android project folder.

If you are a git user, you can use the --depth command line argument to only clone the most current version of the repository:

  git clone --depth=1 https://github.com/ftctechnh/ftc_app.git

Or, if you prefer, you can use the "Download Zip" button available through the main repository page.  You can also download the project folder (as a .zip or .tar.gz archive file) from the Downloads subsection of the Releases page for this repository.

Use Android Studio to import the folder  ("Import project (Eclipse ADT, Gradle, etc.)").

The Javadoc reference documentation for the FTC SDK is now available online.  Visit the following URL to view the FTC SDK documentation as a live website:

http://ftctechnh.github.io/ftc_app/doc/javadoc/index.html

Documentation for the FTC SDK is also included with this repository.  There is a subfolder called "doc" which contains several subfolders:

 * The folder "apk" contains the .apk files for the FTC Driver Station and FTC Robot Controller apps.
 * The folder "javadoc" contains the JavaDoc user documentation for the FTC SDK.
 * The folder "tutorial" contains PDF files that help teach the basics of using the FTC SDK.

For technical questions regarding the SDK, please visit the FTC Technology forum:

  http://ftcforum.usfirst.org/forumdisplay.php?156-FTC-Technology

**************************************************************************************

Version 3.00 (built on 17.04.13)

*** Use this version of the software at YOUR OWN RISK!!! ***

This software is being released as an "alpha" version.  Use this version at your own risk!

This pre-release software contains SIGNIFICANT changes, including changes to the Wi-Fi Direct pairing mechanism, rewrites of the I2C sensor classes, changes to the USB/FTDI layer, and the introduction of support for the REV Robotics Expansion Hub and the REV Robotics color-range-light sensor.  These changes were implemented to improve the reliability and resiliency of the FTC control system.

Please note, however, that version 3.00 is considered "alpha" code.  This code is being released so that the FIRST community will have an opportunity to test the new REV Expansion Hub electronics module when it becomes available in May.  The developers do not recommend using this code for critical applications (i.e., competition use).

*** Use this version of the software at YOUR OWN RISK!!! ***

Changes include:
 * Major rework of sensor-related infrastructure.  Includes rewriting sensor classes to implement synchronous I2C communication.
 * Fix to reset Autonomous timer back to 30 seconds.
 * Implementation of specific motor profiles for approved 12V motors (includes Tetrix, AndyMark, Matrix and REV models).
 * Modest improvements to enhance Wi-Fi P2P pairing.
 * Fixes telemetry log addition race.
 * Publishes all the sources (not just a select few).
 * Includes Block programming improvements
    - Addition of optimized Vuforia blocks.
    - Auto scrollbar to projects and sounds pages.
    - Fixed blocks paste bug.
    - Blocks execute after while-opModeIsActive loop (to allow for cleanup before exiting op mode).
    - Added gyro integratedZValue block.
    - Fixes bug with projects page for Firefox browser.
    - Added IsSpeaking block to AndroidTextToSpeech.  
 * Implements support for the REV Robotics Expansion Hub
    - Implements support for integral REV IMU (physically installed on I2C bus 0, uses same Bosch BNO055 9 axis absolute orientation sensor as Adafruit 9DOF abs orientation sensor).
    - Implements support for REV color/range/light sensor.
    - Provides support to update Expansion Hub firmware through FTC SDK.
    - Detects REV firmware version and records in log file.
    - Includes support for REV Control Hub (note that the REV Control Hub is not yet approved for FTC use).
    - Implements FTC Blocks programming support for REV Expansion Hub and sensor hardware.
    - Detects and alerts when I2C device disconnect.
    
**************************************************************************************

Version 2.62 (built on 17.01.07)
  * Added null pointer check before calling modeToByte() in finishModeSwitchIfNecessary method for ModernRoboticsUsbDcMotorController class.
  * Changes to enhance Modern Robotics USB protocol robustness.

**************************************************************************************

Version 2.61 (released on 16.12.19)
  * Blocks Programming mode changes:
     - Fix to correct issue when an exception was thrown because an OpticalDistanceSensor object appears twice in the hardware map (the second time as a LightSensor).

**************************************************************************************

Version 2.6 (released on 16.12.16)
  * Fixes for Gyro class:
     - Improve (decrease) sensor refresh latency.
     - fix isCalibrating issues.
  * Blocks Programming mode changes:
     - Blocks now ignores a device in the configuration xml if the name is empty. Other devices work in configuration work fine.
     
**************************************************************************************

Version 2.5 (internal release on released on 16.12.13)
  * Blocks Programming mode changes:
     - Added blocks support for AdafruitBNO055IMU.
     - Added Download Op Mode button to FtcBocks.html.
     - Added support for copying blocks in one OpMode and pasting them in an other OpMode. The clipboard content is stored on the phone, so the programming mode server must be running.
     - Modified Utilities section of the toolbox.
     - In Programming Mode, display information about the active connections.
     - Fixed paste location when workspace has been scrolled.
     - Added blocks support for the android Accelerometer.
     - Fixed issue where Blocks Upload Op Mode truncated name at first dot.
     - Added blocks support for Android SoundPool.
     - Added type safety to blocks for Acceleration.
     - Added type safety to blocks for AdafruitBNO055IMU.Parameters.
     - Added type safety to blocks for AnalogInput.
     - Added type safety to blocks for AngularVelocity.
     - Added type safety to blocks for Color.
     - Added type safety to blocks for ColorSensor.
     - Added type safety to blocks for CompassSensor.
     - Added type safety to blocks for CRServo.
     - Added type safety to blocks for DigitalChannel.
     - Added type safety to blocks for ElapsedTime.
     - Added type safety to blocks for Gamepad.
     - Added type safety to blocks for GyroSensor.
     - Added type safety to blocks for IrSeekerSensor.
     - Added type safety to blocks for LED.
     - Added type safety to blocks for LightSensor.
     - Added type safety to blocks for LinearOpMode.
     - Added type safety to blocks for MagneticFlux.
     - Added type safety to blocks for MatrixF.     
     - Added type safety to blocks for MrI2cCompassSensor.
     - Added type safety to blocks for MrI2cRangeSensor.
     - Added type safety to blocks for OpticalDistanceSensor.
     - Added type safety to blocks for Orientation.
     - Added type safety to blocks for Position.
     - Added type safety to blocks for Quaternion.
     - Added type safety to blocks for Servo.
     - Added type safety to blocks for ServoController.
     - Added type safety to blocks for Telemetry.
     - Added type safety to blocks for Temperature.
     - Added type safety to blocks for TouchSensor.
     - Added type safety to blocks for UltrasonicSensor.
     - Added type safety to blocks for VectorF.
     - Added type safety to blocks for Velocity.
     - Added type safety to blocks for VoltageSensor.
     - Added type safety to blocks for VuforiaLocalizer.Parameters.
     - Added type safety to blocks for VuforiaTrackable.
     - Added type safety to blocks for VuforiaTrackables.
     - Added type safety to blocks for enums in AdafruitBNO055IMU.Parameters.
     - Added type safety to blocks for AndroidAccelerometer, AndroidGyroscope, AndroidOrientation, and AndroidTextToSpeech.

**************************************************************************************

Version 2.4 (released on 16.11.13)
  * Fix to avoid crashing for nonexistent resources.
  * Blocks Programming mode changes:
     - Added blocks to support OpenGLMatrix, MatrixF, and VectorF.
     - Added blocks to support AngleUnit, AxesOrder, AxesReference, CameraDirection, CameraMonitorFeedback, DistanceUnit, and TempUnit.
     - Added blocks to support Acceleration.
     - Added blocks to support LinearOpMode.getRuntime.
     - Added blocks to support MagneticFlux and Position.
     - Fixed typos.
     - Made blocks for ElapsedTime more consistent with other objects.
     - Added blocks to support Quaternion, Velocity, Orientation, AngularVelocity.
     - Added blocks to support VuforiaTrackables, VuforiaTrackable, VuforiaLocalizer, VuforiaTrackableDefaultListener.
     - Fixed a few blocks.
     - Added type checking to new blocks.
     - Updated to latest blockly.
     - Added default variable blocks to navigation and matrix blocks.
     - Fixed toolbox entry for openGLMatrix_rotation_withAxesArgs.
     - When user downloads Blocks-generated op mode, only the .blk file is downloaded.
     - When user uploads Blocks-generated op mode (.blk file), Javascript code is auto generated.
     - Added DbgLog support.
     - Added logging when a blocks file is read/written.
     - Fixed bug to properly render blocks even if missing devices from configuration file.
     - Added support for additional characters (not just alphanumeric) for the block file names (for download and upload).
     - Added support for OpMode flavor (“Autonomous” or “TeleOp”) and group.
  * Changes to Samples to prevent tutorial issues.
  * Incorporated suggested changes from public pull 216 (“Replace .. paths”).
  * Remove Servo Glitches when robot stopped.
  * if user hits “Cancels” when editing a configuration file, clears the unsaved changes and reverts to original unmodified configuration.
  * Added log info to help diagnose why the Robot Controller app was terminated (for example, by watch dog function).
  * Added ability to transfer log from the controller.
  * Fixed inconsistency for AngularVelocity
  * Limit unbounded growth of data for telemetry.  If user does not call telemetry.update() for LinearOpMode in a timely manner, data added for telemetry might get lost if size limit is exceeded.

**************************************************************************************

Version 2.35 (released on 16.10.06)
  * Blockly programming mode - Removed unnecesary idle() call from blocks for new project.

**************************************************************************************

Version 2.30 (released on 16.10.05)
  * Blockly programming mode:
     - Mechanism added to save Blockly op modes from Programming Mode Server onto local device
     - To avoid clutter, blocks are displayed in categorized folders
     - Added support for DigitalChannel
     - Added support for ModernRoboticsI2cCompassSensor
     - Added support for ModernRoboticsI2cRangeSensor
     - Added support for VoltageSensor
     - Added support for AnalogInput
     - Added support for AnalogOutput
     - Fix for CompassSensor setMode block
  * Vuforia
     - Fix deadlock / make camera data available while Vuforia is running.
     - Update to Vuforia 6.0.117 (recommended by Vuforia and Google to close security loophole). 
  * Fix for autonomous 30 second timer bug (where timer was in effect, even though it appeared to have timed out).
  * opModeIsActive changes to allow cleanup after op mode is stopped (with enforced 2 second safety timeout).
  * Fix to avoid reading i2c twice.
  * Updated sample Op Modes.
  * Improved logging and fixed intermittent freezing.
  * Added digital I/O sample.
  * Cleaned up device names in sample op modes to be consistent with Pushbot guide.
  * Fix to allow use of IrSeekerSensorV3.

**************************************************************************************

Version 2.20 (released on 16.09.08)
  * Support for Modern Robotics Compass Sensor.
  * Support for Modern Robotics Range Sensor.
  * Revise device names for Pushbot templates to match the names used in Pushbot guide.
  * Fixed bug so that IrSeekerSensorV3 device is accessible as IrSeekerSensor in hardwareMap.
  * Modified computer vision code to require an individual Vuforia license (per legal requirement from PTC).
  * Minor fixes.
  * Blockly enhancements:
     - Support for Voltage Sensor.
     - Support for Analog Input.
     - Support for Analog Output.
     - Support for Light Sensor.
     - Support for Servo Controller.

**************************************************************************************

Version 2.10 (released on 16.09.03)
 * Support for Adafruit IMU.
 * Improvements to ModernRoboticsI2cGyro class
    - Block on reset of z axis.
    - isCalibrating() returns true while gyro is calibration.
 * Updated sample gyro program.
 * Blockly enhancements
    - support for android.graphics.Color.
    - added support for ElapsedTime.
    - improved look and legibility of blocks.
    - support for compass sensor.
    - support for ultrasonic sensor.
    - support for IrSeeker.
    - support for LED.
    - support for color sensor.
    - support for CRServo
    - prompt user to configure robot before using programming mode.
 * Provides ability to disable audio cues.
 * various bug fixes and improvements.

**************************************************************************************

Version 2.00 (released on 16.08.19)
 * This is the new release for the upcoming 2016-2017 FIRST Tech Challenge Season.
 * Channel change is enabled in the FTC Robot Controller app for Moto G 2nd and 3rd Gen phones.
 * Users can now use annotations to register/disable their Op Modes.
 * Changes in the Android SDK, JDK and build tool requirements (minsdk=19, java 1.7, build tools 23.0.3).
 * Standardized units in analog input.
 * Cleaned up code for existing analog sensor classes.
 * setChannelMode and getChannelMode were REMOVED from the DcMotorController class.  This is important - we no longer set the motor modes through the motor controller.
 * setMode and getMode were added to the DcMotor class.  
 * ContinuousRotationServo class has been added to the FTC SDK.
 * Range.clip() method has been overloaded so it can support this operation for int, short and byte integers.
 * Some changes have been made (new methods added) on how a user can access items from the hardware map.
 * Users can now set the zero power behavior for a DC motor so that the motor will brake or float when power is zero.
 * Prototype Blockly Programming Mode has been added to FTC Robot Controller.  Users can place the Robot Controller into this mode, and then use a device (such as a laptop) that has a Javascript enabled browser to write Blockly-based Op Modes directly onto the Robot Controller.
 * Users can now configure the robot remotely through the FTC Driver Station app.
 * Android Studio project supports Android Studio 2.1.x and compile SDK Version 23 (Marshmallow).
 * Vuforia Computer Vision SDK integrated into FTC SDK.  Users can use sample vision targets to get localization information on a standard FTC field.
 * Project structure has been reorganized so that there is now a TeamCode package that users can use to place their local/custom Op Modes into this package.
 * Inspection function has been integrated into the FTC Robot Controller and Driver Station Apps (Thanks Team HazMat… 9277 & 10650!).
 * Audio cues have been incorporated into FTC SDK.
 * Swap mechanism added to FTC Robot Controller configuration activity.  For example, if you have two motor controllers on a robot, and you misidentified them in your configuration file, you can use the Swap button to swap the devices within the configuration file (so you do not have to manually re-enter in the configuration info for the two devices).
 * Fix mechanism added to all user to replace an electronic module easily.  For example, suppose a servo controller dies on your robot. You replace the broken module with a new module, which has a different serial number from the original servo controller.  You can use the Fix button to automatically reconfigure your configuration file to use the serial number of the new module.
 * Improvements made to fix resiliency and responsiveness of the system.
 * For LinearOpMode the user now must for a telemetry.update() to update the telemetry data on the driver station.  This update() mechanism ensures that the driver station gets the updated data properly and at the same time.
 * The Auto Configure function of the Robot Controller is now template based.  If there is a commonly used robot configuration, a template can be created so that the Auto Configure mechanism can be used to quickly configure a robot of this type.
 * The logic to detect a runaway op mode (both in the LinearOpMode and OpMode types) and to abort the run, then auto recover has been improved/implemented.
 * Fix has been incorporated so that Logitech F310 gamepad mappings will be correct for Marshmallow users.

**************************************************************************************

Release 16.07.08

 * For the ftc_app project, the gradle files have been modified to support Android Studio 2.1.x.



**************************************************************************************

Release 16.03.30

 * For the MIT App Inventor, the design blocks have new icons that better represent the function of each design component.
 * Some changes were made to the shutdown logic to ensure the robust shutdown of some of our USB services.
 * A change was made to LinearOpMode so as to allow a given instance to be executed more than once, which is required for the App Inventor.
 * Javadoc improved/updated.

**************************************************************************************

Release 16.03.09

 * Changes made to make the FTC SDK synchronous (significant change!)
    - waitOneFullHardwareCycle() and waitForNextHardwareCycle() are no longer needed and have been deprecated.
    - runOpMode() (for a LinearOpMode) is now decoupled from the system's hardware read/write thread.
    - loop() (for an OpMode) is now decoupled from the system's hardware read/write thread.
    - Methods are synchronous.
    - For example, if you call setMode(DcMotorController.RunMode.RESET_ENCODERS) for a motor, the encoder is guaranteed to be reset when the method call is complete.
    - For legacy module (NXT compatible), user no longer has to toggle between read and write modes when reading from or writing to a legacy device.
 * Changes made to enhance reliability/robustness during ESD event.
 * Changes made to make code thread safe.
 * Debug keystore added so that user-generated robot controller APKs will all use the same signed key (to avoid conflicts if a team has multiple developer laptops for example).
 * Firmware version information for Modern Robotics modules are now logged.
 * Changes made to improve USB comm reliability and robustness.
 * Added support for voltage indicator for legacy (NXT-compatible) motor controllers.
 * Changes made to provide auto stop capabilities for op modes.
    - A LinearOpMode class will stop when the statements in runOpMode() are complete.  User does not have to push the stop button on the driver station.
    - If an op mode is stopped by the driver station, but there is a run away/uninterruptible thread persisting, the app will log an error message then force itself to crash to stop the runaway thread.
 * Driver Station UI modified to display lowest measured voltage below current voltage (12V battery).
 * Driver Station UI modified to have color background for current voltage (green=good, yellow=caution, red=danger, extremely low voltage).
 * javadoc improved (edits and additional classes).
 * Added app build time to About activity for driver station and robot controller apps.
 * Display local IP addresses on Driver Station About activity.
 * Added I2cDeviceSynchImpl.
 * Added I2cDeviceSync interface.
 * Added seconds() and milliseconds() to ElapsedTime for clarity.
 * Added getCallbackCount() to I2cDevice.
 * Added missing clearI2cPortActionFlag.
 * Added code to create log messages while waiting for LinearOpMode shutdown.
 * Fix so Wifi Direct Config activity will no longer launch multiple times.
 * Added the ability to specify an alternate i2c address in software for the Modern Robotics gyro.
 
**************************************************************************************

Release 16.02.09

 * Improved battery checker feature so that voltage values get refreshed regularly (every 250 msec) on Driver Station (DS) user interface.
 * Improved software so that Robot Controller (RC) is much more resilient and “self-healing” to USB disconnects:
    - If user attempts to start/restart RC with one or more module missing, it will display a warning but still start up.
    - When running an op mode, if one or more modules gets disconnected, the RC & DS will display warnings,and robot will keep on working in spite of the missing module(s).
    - If a disconnected module gets physically reconnected the RC will auto detect the module and the user will regain control of the recently connected module.
    - Warning messages are more helpful (identifies the type of module that’s missing plus its USB serial number).   
 * Code changes to fix the null gamepad reference when users try to reference the gamepads in the init() portion of their op mode.
 * NXT light sensor output is now properly scaled.  Note that teams might have to readjust their light threshold values in their op modes.
 * On DS user interface, gamepad icon for a driver will disappear if the matching gamepad is disconnected or if that gamepad gets designated as a different driver.
 * Robot Protocol (ROBOCOL) version number info is displayed in About screen on RC and DS apps.
 * Incorporated a display filter on pairing screen to filter out devices that don’t use the “<TEAM NUMBER>-“ format. This filter can be turned off to show all WiFi Direct devices.
 * Updated text in License file.
 * Fixed formatting error in OpticalDistanceSensor.toString().
 * Fixed issue on with a blank (“”) device name that would disrupt WiFi Direct Pairing.
 * Made a change so that the WiFi info and battery info can be displayed more quickly on the DS upon connecting to RC.
 * Improved javadoc generation.
 * Modified code to make it easier to support language localization in the future.

**************************************************************************************

Release 16.01.04

 * Updated compileSdkVersion for apps
 * Prevent Wifi from entering power saving mode
 * removed unused import from driver station
 * Corrrected "Dead zone" joystick code.
 * LED.getDeviceName and .getConnectionInfo() return null
 * apps check for ROBOCOL_VERSION mismatch
 * Fix for Telemetry also has off-by-one errors in its data string sizing / short size limitations error
 * User telemetry output is sorted.
 * added formatting variants to DbgLog and RobotLog APIs
 * code modified to allow for a long list of op mode names.
 * changes to improve thread safety of RobocolDatagramSocket
 * Fix for "missing hardware leaves robot controller disconnected from driver station" error
 * fix for "fast tapping of Init/Start causes problems" (toast is now only instantiated on UI thread).
 * added some log statements for thread life cycle.
 * moved gamepad reset logic inside of initActiveOpMode() for robustness
 * changes made to mitigate risk of race conditions on public methods.
 * changes to try and flag when WiFi Direct name contains non-printable characters.
 * fix to correct race condition between .run() and .close() in ReadWriteRunnableStandard.
 * updated FTDI driver
 * made ReadWriteRunnableStanard interface public.
 * fixed off-by-one errors in Command constructor
 * moved specific hardware implmentations into their own package.
 * moved specific gamepad implemnatations to the hardware library.
 * changed LICENSE file to new BSD version.
 * fixed race condition when shutting down Modern Robotics USB devices.
 * methods in the ColorSensor classes have been synchronized.
 * corrected isBusy() status to reflect end of motion.
 * corrected "back" button keycode.
 * the notSupported() method of the GyroSensor class was changed to protected (it should not be public).


**************************************************************************************

Release 15.11.04.001

 * Added Support for Modern Robotics Gyro.
  - The GyroSensor class now supports the MR Gyro Sensor.
  - Users can access heading data (about Z axis)
  - Users can also access raw gyro data (X, Y, & Z axes).
  - Example MRGyroTest.java op mode included.
 * Improved error messages
  - More descriptive error messages for exceptions in user code.
 * Updated DcMotor API
 * Enable read mode on new address in setI2cAddress
 * Fix so that driver station app resets the gamepads when switching op modes.
 * USB-related code changes to make USB comm more responsive and to display more explicit error messages.
  - Fix so that USB will recover properly if the USB bus returns garbage data.
  - Fix USB initializtion race condition.
  - Better error reporting during FTDI open.
  - More explicit messages during USB failures.
  - Fixed bug so that USB device is closed if event loop teardown method was not called.
 * Fixed timer UI issue
 * Fixed duplicate name UI bug (Legacy Module configuration).
 * Fixed race condition in EventLoopManager.
 * Fix to keep references stable when updating gamepad.
 * For legacy Matrix motor/servo controllers removed necessity of appending "Motor" and "Servo" to controller names.
 * Updated HT color sensor driver to use constants from ModernRoboticsUsbLegacyModule class.
 * Updated MR color sensor driver to use constants from ModernRoboticsUsbDeviceInterfaceModule class. 
 * Correctly handle I2C Address change in all color sensors
 * Updated/cleaned up op modes.
  - Updated comments in LinearI2cAddressChange.java example op mode.
  - Replaced the calls to "setChannelMode" with "setMode" (to match the new of the DcMotor  method).
  - Removed K9AutoTime.java op mode.
  - Added MRGyroTest.java op mode (demonstrates how to use MR Gyro Sensor).
  - Added MRRGBExample.java op mode (demonstrates how to use MR Color Sensor).
  - Added HTRGBExample.java op mode (demonstrates how to use HT legacy color sensor).
  - Added MatrixControllerDemo.java (demonstrates how to use legacy Matrix controller).
 * Updated javadoc documentation.
 * Updated release .apk files for Robot Controller and Driver Station apps.

T. Eng
November 5, 2015
 
**************************************************************************************

Release 15.10.06.002

 * Added support for Legacy Matrix 9.6V motor/servo controller.
 * Cleaned up build.gradle file.
 * Minor UI and bug fixes for driver station and robot controller apps.
 * Throws error if Ultrasonic sensor (NXT) is not configured for legacy module port 4 or 5.

T. Eng
October 6, 2015

**************************************************************************************

In this latest version of the FTC SDK (20150803_001) the following changes should be noted:

 * New user interfaces for FTC Driver Station and FTC Robot Controller apps.
 * An init() method is added to the OpMode class.
   - For this release, init() is triggered right before the start() method.
   - Eventually, the init() method will be triggered when the user presses an "INIT" button on driver station.
   - The init() and loop() methods are now required (i.e., need to be overridden in the user's op mode).
   - The start() and stop() methods are optional.
 * A new LinearOpMode class is introduced.
   - Teams can use the LinearOpMode mode to create a linear (not event driven) program model.
   - Teams can use blocking statements like Thread.sleep() within a linear op mode.
 * The API for the Legacy Module and Core Device Interface Module have been updated.
   - Support for encoders with the Legacy Module is now working.
 * The hardware loop has been updated for better performance.


T. Eng
August 3, 2015