---
layout: default
title: module shapes
permalink: shapes
---

> - # **Function reference module: shapes**

## Basic shapes drawing functions

#### DrawPixel()
``` c
void DrawPixel( int posX, int posY, Color color );
```
Draw a pixel

---

#### DrawPixelV()
``` c
void DrawPixelV(V ector2 position, Color color );
```
Draw a pixel (Vector version)

---

#### DrawLine()
``` c
void DrawLine( int startPosX, int startPosY, int endPosX, int endPosY, Color color );
```
Draw a line

---

#### DrawLineV()
``` c
void DrawLineV( Vector2 startPos, Vector2 endPos, Color color );
```
Draw a line (Vector version)

---

#### DrawLineEx()
``` c
void DrawLineEx( Vector2 startPos, Vector2 endPos, float thick, Color color );
```
Draw a line defining thickness

---

#### DrawLineBezier()
``` c
void DrawLineBezier( Vector2 startPos, Vector2 endPos, float thick, Color color );
```
Draw a line using cubic-bezier curves in-out

---

#### DrawLineStrip()
``` c
void DrawLineStrip( Vector2 *points, int numPoints, Color color );
```
Draw lines sequence

---

#### DrawCircle()
``` c
void DrawCircle( int centerX, int centerY, float radius, Color color );
```
Draw a color-filled circle

---

#### DrawCircleSector()
``` c
void DrawCircleSector( Vector2 center, float radius, int startAngle, int endAngle, int segments, Color color );
```
Draw a piece of a circle

---

#### DrawCircleSectorLines()
``` c
void DrawCircleSectorLines( Vector2 center, float radius, int startAngle, int endAngle, int segments, Color color );
```
Draw circle sector outline

---

#### DrawCircleGradient()
``` c
void DrawCircleGradient( int centerX, int centerY, float radius, Color color1, Color color2 );
```
Draw a gradient-filled circle

---

#### DrawCircleV()
``` c
void DrawCircleV( Vector2 center, float radius, Color color );
```
Draw a color-filled circle (Vector version)

---

#### DrawCircleLines()
``` c
void DrawCircleLines( int centerX, int centerY, float radius, Color color );
```
Draw circle outline

---

#### DrawEllipse()
``` c
void DrawEllipse( int centerX, int centerY, float radiusH, float radiusV, Color color );
```
Draw ellipse

---

#### DrawEllipseLines()
``` c
void DrawEllipseLines( int centerX, int centerY, float radiusH, float radiusV, Color color );
```
Draw ellipse outline

---

#### DrawRing()
``` c
void DrawRing( Vector2 center, float innerRadius, float outerRadius, int startAngle, int endAngle, int segments, Color color );
```
Draw ring

---

#### DrawRingLines()
``` c
void DrawRingLines( Vector2 center, float innerRadius, float outerRadius, int startAngle, int endAngle, int segments, Color color );
```
Draw ring outline

---

#### DrawRectangle()
``` c
void DrawRectangle( int posX, int posY, int width, int height, Color color );
```
Draw a color-filled rectangle

---

#### DrawRectangleV()
``` c
void DrawRectangleV( Vector2 position, Vector2 size, Color color );
```
Draw a color-filled rectangle (Vector version)

---

#### DrawRectangleRec()
``` c
void DrawRectangleRec( Rectangle rec, Color color );
```
Draw a color-filled rectangle

---

#### DrawRectanglePro()
``` c
void DrawRectanglePro( Rectangle rec, Vector2 origin, float rotation, Color color );
```
Draw a color-filled rectangle with pro parameters

---

#### DrawRectangleGradientV()
``` c
void DrawRectangleGradientV( int posX, int posY, int width, int height, Color color1, Color color2 );
```
Draw a vertical-gradient-filled rectangle

---

#### DrawRectangleGradientH()
``` c
void DrawRectangleGradientH( int posX, int posY, int width, int height, Color color1, Color color2 );
```
Draw a horizontal-gradient-filled rectangle

---

#### DrawRectangleGradientEx()
``` c
void DrawRectangleGradientEx( Rectangle rec, Color col1, Color col2, Color col3, Color col4 );
```
Draw a gradient-filled rectangle with custom vertex colors

---

#### DrawRectangleLines()
``` c
void DrawRectangleLines( int posX, int posY, int width, int height, Color color );
```
Draw rectangle outline

---

#### DrawRectangleLinesEx()
``` c
void DrawRectangleLinesEx( Rectangle rec, int lineThick, Color color );
```
Draw rectangle outline with extended parameters

---

#### DrawRectangleRounded()
``` c
void DrawRectangleRounded( Rectangle rec, float roundness, int segments, Color color );
```
Draw rectangle with rounded edges

---

#### DrawRectangleRoundedLines()
``` c
void DrawRectangleRoundedLines( Rectangle rec, float roundness, int segments, int lineThick, Color color );
```
Draw rectangle with rounded edges outline

---

#### DrawTriangle()
``` c
void DrawTriangle( Vector2 v1, Vector2 v2, Vector2 v3, Color color );
```
Draw a color-filled triangle (vertex in counter-clockwise order!)

---

#### DrawTriangleLines()
``` c
void DrawTriangleLines( Vector2 v1, Vector2 v2, Vector2 v3, Color color );
```
Draw triangle outline (vertex in counter-clockwise order!)

---

#### DrawTriangleFan()
``` c
void DrawTriangleFan( Vector2 *points, int numPoints, Color color );
```
Draw a triangle fan defined by points (first vertex is the center)

---

#### DrawTriangleStrip()
``` c
void DrawTriangleStrip( Vector2 *points, int pointsCount, Color color );
```
Draw a triangle strip defined by points

---

#### DrawPoly()
``` c
void DrawPoly( Vector2 center, int sides, float radius, float rotation, Color color );
```
Draw a regular polygon (Vector version)

---

#### DrawPolyLines()
``` c
void DrawPolyLines( Vector2 center, int sides, float radius, float rotation, Color color );
```
Draw a polygon outline of n sides

---

## Basic shapes collision detection functions

#### CheckCollisionRecs()
``` c
bool CheckCollisionRecs( Rectangle rec1, Rectangle rec2 );
```
Check collision between two rectangles

---

#### CheckCollisionCircles()
``` c
bool CheckCollisionCircles( Vector2 center1, float radius1, Vector2 center2, float radius2 );
```
Check collision between two circles

---

#### CheckCollisionCircleRec()
``` c
bool CheckCollisionCircleRec( Vector2 center, float radius, Rectangle rec );
```
Check collision between circle and rectangle

---

#### GetCollisionRec()
``` c
Rectangle GetCollisionRec( Rectangle rec1, Rectangle rec2 );
```
Get collision rectangle for two rectangles collision

---

#### CheckCollisionPointRec()
``` c
bool CheckCollisionPointRec( Vector2 point, Rectangle rec );
```
Check if point is inside rectangle

---

#### CheckCollisionPointCircle()
``` c
bool CheckCollisionPointCircle( Vector2 point, Vector2 center, float radius );
```
Check if point is inside circle

---

#### CheckCollisionPointTriangle()
``` c
bool CheckCollisionPointTriangle( Vector2 point, Vector2 p1, Vector2 p2, Vector2 p3 );
```
Check if point is inside a triangle

---

> &copy; 2020 Rafał Jopek