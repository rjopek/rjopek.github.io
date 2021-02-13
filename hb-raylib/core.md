---
layout: default
title: module core
permalink: core
---

> # **Function reference module: core**

## Window-related functions

#### InitWindow()
``` c
void InitWindow( int width, int height, const char *title );
```
Initialize window and OpenGL context

---

#### WindowShouldClose()
``` c
bool WindowShouldClose( void );
```
Check if KEY_ESCAPE pressed or Close icon pressed

---

#### CloseWindow()
``` c
void CloseWindow( void );
```
Close window and unload OpenGL context

---

#### IsWindowReady()
``` c
bool IsWindowReady( void );
```
Check if window has been initialized successfully

---

#### IsWindowMinimized()
``` c
bool IsWindowMinimized( void );
```
Check if window has been minimized (or lost focus)

---

#### IsWindowResized()
``` c
bool IsWindowResized( void );
```
Check if window has been resized

---

#### IsWindowHidden()
``` c
bool IsWindowHidden( void );
```
Check if window is currently hidden

---

#### IsWindowFullscreen()
``` c
bool IsWindowFullscreen( void );
```
Check if window is currently fullscreen

---

#### ToggleFullscreen()
``` c
void ToggleFullscreen( void );
```
Toggle fullscreen mode (only PLATFORM_DESKTOP)

---

#### UnhideWindow()
``` c
void UnhideWindow( void );
```
Show the window

---

#### HideWindow()
``` c
void HideWindow( void );
```
Hide the window

---

#### SetWindowIcon()
``` c
void SetWindowIcon( Image image );
```
Set icon for window (only PLATFORM_DESKTOP)

---

#### SetWindowTitle()
``` c
void SetWindowTitle( const char *title );
```
Set title for window (only PLATFORM_DESKTOP)

---

#### SetWindowPosition()
``` c
void SetWindowPosition( int x, int y );
```
Set window position on screen (only PLATFORM_DESKTOP)

---

#### SetWindowMonitor()
``` c
void SetWindowMonitor( int monitor );
```
Set monitor for the current window (fullscreen mode)

---

#### SetWindowMinSize()
``` c
void SetWindowMinSize( int width, int height );
```
Set window minimum dimensions (for FLAG_WINDOW_RESIZABLE)

---

#### SetWindowSize()
``` c
void SetWindowSize( int width, int height );
```
Set window dimensions

---

#### GetWindowHandle()
``` c
void *GetWindowHandle( void );
```
Get native window handle

---

#### GetScreenWidth()
``` c
int GetScreenWidth( void );
```
Get current screen width

---

#### GetScreenHeight()
``` c
int GetScreenHeight( void );
```
Get current screen height

---

#### GetMonitorCount()
``` c
int GetMonitorCount( void );
```
Get number of connected monitors

---

#### GetMonitorWidth()
``` c
int GetMonitorWidth( int monitor );
```
Get primary monitor width

---

#### GetMonitorHeight()
``` c
int GetMonitorHeight( int monitor );
```
Get primary monitor height

---

#### GetMonitorPhysicalWidth()
``` c
int GetMonitorPhysicalWidth( int monitor );
```
Get primary monitor physical width in millimetres

---

#### GetMonitorPhysicalHeight()
``` c
int GetMonitorPhysicalHeight( int monitor );
```
Get primary monitor physical height in millimetres

---

#### GetWindowPosition()
``` c
Vector2 GetWindowPosition( void );
```
Get window position XY on monitor

---

#### GetMonitorName()
``` c
const char *GetMonitorName( int monitor );
```
Get the human-readable, UTF-8 encoded name of the primary monitor

---

#### GetClipboardText()
``` c
const char *GetClipboardText( void );
```
Get clipboard text content

---

#### SetClipboardText()
``` c
void SetClipboardText( const char *text );
```
Set clipboard text content

---

## Cursor-related functions

#### ShowCursor()
``` c
void ShowCursor( void );
```
Shows cursor

---

#### HideCursor()
``` c
void HideCursor( void );
```
Hides cursor

---

#### IsCursorHidden()
``` c
bool IsCursorHidden( void );
```
Check if cursor is not visible

---

#### EnableCursor()
``` c
void EnableCursor( void );
```
Enables cursor (unlock cursor)

---

#### DisableCursor()
``` c
void DisableCursor( void );
```
Disables cursor (lock cursor)

---

## Drawing-related functions

#### ClearBackground()
``` c
void ClearBackground( Color color );
```
Set background color (framebuffer clear color)

---

#### BeginDrawing()
``` c
void BeginDrawing( void );
```
Setup canvas (framebuffer) to start drawing

---

#### EndDrawing()
``` c
void EndDrawing( void );
```
End canvas drawing and swap buffers (double buffering)

---

#### BeginMode2D()
``` c
void BeginMode2D( Camera2D camera );
```
Initialize 2D mode with custom camera (2D)

---

#### EndMode2D()
``` c
void EndMode2D( void );
```
Ends 2D mode with custom camera

---

#### BeginMode3D()
``` c
void BeginMode3D( Camera3D camera );
```
Initializes 3D mode with custom camera (3D)

---

#### EndMode3D()
``` c
void EndMode3D( void );
```
Ends 3D mode and returns to default 2D orthographic mode

---

#### BeginTextureMode()
``` c
void BeginTextureMode( RenderTexture2D target );
```
Initializes render texture for drawing

---

#### EndTextureMode()
``` c
void EndTextureMode( void );
```
Ends drawing to render texture

---

#### BeginScissorMode()
``` c
void BeginScissorMode( int x, int y, int width, int height );
```
Begin scissor mode (define screen area for following drawing)

---

#### EndScissorMode()
``` c
void EndScissorMode( void );
```
End scissor mode

---

## Screen-space-related functions

#### GetMouseRay()
``` c
Ray GetMouseRay( Vector2 mousePosition, Camera camera );
```
Returns a ray trace from mouse position

---

#### GetCameraMatrix()
``` c
Matrix GetCameraMatrix( Camera camera );
```
Returns camera transform matrix (view matrix)

---

#### GetCameraMatrix2D()
``` c
Matrix GetCameraMatrix2D( Camera2D camera );
```
Returns camera 2d transform matrix

---

#### GetWorldToScreen()
``` c
Vector2 GetWorldToScreen( Vector3 position, Camera camera );
```
Returns the screen space position for a 3d world space position

---

#### GetWorldToScreenEx()
``` c
Vector2 GetWorldToScreenEx( Vector3 position, Camera camera, int width, int height );
```
Returns size position for a 3d world space position

---

#### GetWorldToScreen2D()
``` c
Vector2 GetWorldToScreen2D( Vector2 position, Camera2D camera );
```
Returns the screen space position for a 2d camera world space position

---

#### GetScreenToWorld2D()
``` c
Vector2 GetScreenToWorld2D( Vector2 position, Camera2D camera );
```
Returns the world space position for a 2d camera screen space position

---

## Timing-related functions

#### SetTargetFPS()
``` c
void SetTargetFPS( int fps );
```
Set target FPS (maximum)

---

#### GetFPS()
``` c
int GetFPS( void );
```
Returns current FPS

---

#### GetFrameTime()
``` c
float GetFrameTime( void );
```
Returns time in seconds for last frame drawn

---

#### GetTime()
``` c
double GetTime( void );
```
Returns elapsed time in seconds since InitWindow()

---

## Color-related functions

#### ColorToInt()
``` c
int ColorToInt( Color color );
```
Returns hexadecimal value for a Color

---

#### ColorNormalize()
``` c
Vector4 ColorNormalize( Color color );
```
Returns color normalized as float [0..1]

---

#### ColorFromNormalized()
``` c
Color ColorFromNormalized( Vector4 normalized );
```
Returns color from normalized values [0..1]

---

#### ColorToHSV()
``` c
Vector3 ColorToHSV( Color color );
```
Returns HSV values for a Color

---

#### ColorFromHSV()
``` c
Color ColorFromHSV( Vector3 hsv );
```
Returns a Color from HSV values

---

#### GetColor()
``` c
Color GetColor( int hexValue );
```
Returns a Color struct from hexadecimal value

---

#### Fade()
``` c
Color Fade( Color color, float alpha );
```
Color fade-in or fade-out, alpha goes from 0.0f to 1.0f

---

## Misc. functions

#### SetConfigFlags()
``` c
void SetConfigFlags( unsigned int flags );
```
Setup window configuration flags (view FLAGS)

---

#### SetTraceLogLevel()
``` c
void SetTraceLogLevel( int logType );
```
Set the current threshold (minimum) log level

---

#### SetTraceLogExit()
``` c
void SetTraceLogExit( int logType );
```
Set the exit threshold (minimum) log level

---

#### SetTraceLogCallback()
``` c
void SetTraceLogCallback( TraceLogCallback callback );
```
Set a trace log callback to enable custom logging

---

#### TraceLog()
``` c
void TraceLog( int logType, const char *text, ... );
```
Show trace log messages (LOG_DEBUG, LOG_INFO, LOG_WARNING, LOG_ERROR)

---

#### TakeScreenshot()
``` c
void TakeScreenshot( const char *fileName );
```
Takes a screenshot of current screen (saved a .png)

---

#### GetRandomValue()
``` c
int GetRandomValue( int min, int max );
```
Returns a random value between min and max (both included)

---

## Files management functions

#### LoadFileData()
``` c
unsigned char *LoadFileData( const char *fileName, unsigned int *bytesRead );
```
Load file data as byte array (read)

---

#### SaveFileData()
``` c
void SaveFileData( const char *fileName, void *data, unsigned int bytesToWrite );
```
Save data to file from byte array (write)

---

#### LoadFileText()
``` c
char *LoadFileText( const char *fileName );
```
Load text data from file (read), returns a '\0' terminated string

---

#### SaveFileText()
``` c
void SaveFileText( const char *fileName, char *text );
```
Save text data to file (write), string must be '\0' terminated

---

#### FileExists()
``` c
bool FileExists( const char *fileName );
```
Check if file exists

---

#### IsFileExtension()
``` c
bool IsFileExtension( const char *fileName, const char *ext );
```
Check file extension

---

#### DirectoryExists()
``` c
bool DirectoryExists( const char *dirPath );
```
Check if a directory path exists

---

#### GetExtension()
``` c
const char *GetExtension( const char *fileName );
```
Get pointer to extension for a filename string

---

#### GetFileName()
``` c
const char *GetFileName( const char *filePath );
```
Get pointer to filename for a path string

---

#### GetFileNameWithoutExt()
``` c
const char *GetFileNameWithoutExt( const char *filePath );
```
Get filename string without extension (uses static string)

---

#### GetDirectoryPath()
``` c
const char *GetDirectoryPath( const char *filePath );
```
Get full path for a given fileName with path (uses static string)

---

#### GetPrevDirectoryPath()
``` c
const char *GetPrevDirectoryPath( const char *dirPath );
```
Get previous directory path for a given path (uses static string)

---

#### GetWorkingDirectory()
``` c
const char *GetWorkingDirectory( void );
```
Get current working directory (uses static string)

#### GetDirectoryFiles()
``` c
char **GetDirectoryFiles( const char *dirPath, int *count );
```
Get filenames in a directory path (memory should be freed)

---

#### ClearDirectoryFiles()
``` c
void ClearDirectoryFiles( void );
```
Clear directory files paths buffers (free memory)

---

#### ChangeDirectory()
``` c
bool ChangeDirectory( const char *dir );
```
Change working directory, returns true if success

---

#### IsFileDropped()
``` c
bool IsFileDropped( void );
```
Check if a file has been dropped into window

---

#### GetDroppedFiles()
``` c
char **GetDroppedFiles( int *count );
```
Get dropped files names (memory should be freed)

---

#### ClearDroppedFiles()
``` c
void ClearDroppedFiles( void );
```
Clear dropped files paths buffer (free memory)

----

#### GetFileModTime()
``` c
long GetFileModTime( const char *fileName );
```
Get file modification time (last write time)

---

#### CompressData()
``` c
unsigned char *CompressData( unsigned char *data, int dataLength, int *compDataLength );
```
Compress data (DEFLATE algorythm)

---

#### DecompressData()
``` c
unsigned char *DecompressData( unsigned char *compData, int compDataLength, int *dataLength );
```
Decompress data (DEFLATE algorythm)

---

## Persistent storage management

#### SaveStorageValue()
``` c
void SaveStorageValue( unsigned int position, int value );
```
Save integer value to storage file (to defined position)

---

#### LoadStorageValue()
``` c
int LoadStorageValue( unsigned int position );
```
Load integer value from storage file (from defined position)

---

#### OpenURL()
``` c
void OpenURL( const char *url );
```
Open URL with default system browser (if available)

---

> Input Handling Functions

## Input-related functions: keyb

#### IsKeyPressed()
``` c
bool IsKeyPressed( int key );
```
Detect if a key has been pressed once

---

#### IsKeyDown()
``` c
bool IsKeyDown( int key );
```
Detect if a key is being pressed

---

#### IsKeyReleased()
``` c
bool IsKeyReleased( int key );
```
Detect if a key has been released once

---

#### IsKeyUp()
``` c
bool IsKeyUp( int key );
```
Detect if a key is NOT being pressed

---

#### GetKeyPressed()
``` c
int GetKeyPressed( void );
```
Get latest key pressed

---

#### SetExitKey()
``` c
void SetExitKey( int key );
```
Set a custom key to exit program (default is ESC)

---

## Input-related functions: gamepads

#### IsGamepadAvailable()
``` c
bool IsGamepadAvailable( int gamepad );
```
Detect if a gamepad is available

---

#### IsGamepadName()
``` c
bool IsGamepadName( int gamepad, const char *name );
```
Check gamepad name (if available)

---

#### GetGamepadName()
``` c
const char *GetGamepadName( int gamepad );
```
Return gamepad internal name id

---

#### IsGamepadButtonPressed()
``` c
bool IsGamepadButtonPressed( int gamepad, int button );
```
Detect if a gamepad button has been pressed once

---

#### IsGamepadButtonDown()
``` c
bool IsGamepadButtonDown( int gamepad, int button );
```
Detect if a gamepad button is being pressed

---

#### IsGamepadButtonReleased()
``` c
bool IsGamepadButtonReleased( int gamepad, int button );
```
Detect if a gamepad button has been released once

---

#### IsGamepadButtonUp()
``` c
bool IsGamepadButtonUp( int gamepad, int button );
```
Detect if a gamepad button is NOT being pressed

---

### GetGamepadButtonPressed()
``` c
int GetGamepadButtonPressed( void );
```
Get the last gamepad button pressed

---

#### GetGamepadAxisCount()
``` c
int GetGamepadAxisCount( int gamepad );
```
Return gamepad axis count for a gamepad

---

#### GetGamepadAxisMovement()
``` c
float GetGamepadAxisMovement( int gamepad, int axis );
```
Return axis movement value for a gamepad axis

---

## Input-related functions: mouse

#### IsMouseButtonPressed()
``` c
bool IsMouseButtonPressed( int button );
```
Detect if a mouse button has been pressed once

---

#### IsMouseButtonDown()
``` c
bool IsMouseButtonDown( int button );
```
Detect if a mouse button is being pressed

---

#### IsMouseButtonReleased()
``` c
bool IsMouseButtonReleased( int button );
```
Detect if a mouse button has been released once

---

#### IsMouseButtonUp()
``` c
bool IsMouseButtonUp( int button );
```
Detect if a mouse button is NOT being pressed

---

#### GetMouseX()
``` c
int GetMouseX( void );
```
Returns mouse position X

---

#### GetMouseY()
``` c
int GetMouseY( void );
```
Returns mouse position Y

---

#### GetMousePosition()
```
Vector2 GetMousePosition( void );
```
Returns mouse position XY

---

#### SetMousePosition()
``` c
void SetMousePosition( int x, int y );
```
Set mouse position XY

---

#### SetMouseOffset()
``` c
void SetMouseOffset( int offsetX, int offsetY );
```
Set mouse offset

---

#### SetMouseScale()
``` c
void SetMouseScale( float scaleX, float scaleY );
```
Set mouse scaling

---

#### GetMouseWheelMove()
``` c
int GetMouseWheelMove( void );
```
Returns mouse wheel movement Y

---


## Input-related functions: touch

#### GetTouchX()
``` c
int GetTouchX( void );
```
Returns touch position X for touch point 0 (relative to screen size)

---

#### GetTouchY()
``` c
int GetTouchY( void );
```
Returns touch position Y for touch point 0 (relative to screen size)

---

#### GetTouchPosition()
``` c
Vector2 GetTouchPosition( int index );
```
Returns touch position XY for a touch point index (relative to screen size)

---

> Gestures and Touch Handling Functions (Module: gestures)

#### SetGesturesEnabled()
``` c
void SetGesturesEnabled( unsigned int gestureFlags );
```
Enable a set of gestures using flags

---

#### IsGestureDetected()
``` c
bool IsGestureDetected( int gesture );
```
Check if a gesture have been detected

---

#### GetGestureDetected()
``` c
int GetGestureDetected( void );
```
Get latest detected gesture

---

#### GetTouchPointsCount()
``` c
int GetTouchPointsCount( void );
```
Get touch points count

---

#### GetGestureHoldDuration()
``` c
float GetGestureHoldDuration( void );
```
Get gesture hold time in milliseconds

---

#### GetGestureDragVector()
``` c
Vector2 GetGestureDragVector( void );
```
Get gesture drag vector

---

#### GetGestureDragAngle()
``` c
float GetGestureDragAngle( void );
```
Get gesture drag angle

---

#### GetGesturePinchVector()
``` c
Vector2 GetGesturePinchVector( void );
```
Get gesture pinch delta

---

#### GetGesturePinchAngle()
``` c
float GetGesturePinchAngle( void );
```
Get gesture pinch angle

---

> Camera System Functions (Module: camera)

#### SetCameraMode()
``` c
void SetCameraMode( Camera camera, int mode );
```
Set camera mode (multiple camera modes available)

---

#### UpdateCamera()
``` c
void UpdateCamera( Camera *camera );
```
Update camera position for selected mode

---

#### SetCameraPanControl()
``` c
void SetCameraPanControl( int panKey );
```
Set camera pan key to combine with mouse movement (free camera)

---

#### SetCameraAltControl()
``` c
void SetCameraAltControl( int altKey );
```
Set camera alt key to combine with mouse movement (free camera)

---

#### SetCameraSmoothZoomControl()
``` c
void SetCameraSmoothZoomControl( int szKey );
```
Set camera smooth zoom key to combine with mouse (free camera)

---

#### SetCameraMoveControls()
``` c
void SetCameraMoveControls( int frontKey, int backKey, int rightKey, int leftKey, int upKey, int downKey );
```
Set camera move controls (1st person and 3rd person cameras)

---

> &copy; 2020 Rafał Jopek