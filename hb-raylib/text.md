---
layout: default
title: module text
permalink: text
---

> # **Function reference module: text**

## Font loading/unloading functions

#### GetFontDefault()
``` c
Font GetFontDefault( void );
```
Get the default Font

---

### LoadFont()
``` c
Font LoadFont( const char *fileName );
```
Load font from file into GPU memory (VRAM)

---

#### LoadFontEx()
``` c
Font LoadFontEx( const char *fileName, int fontSize, int *fontChars, int charsCount );
```
Load font from file with extended parameters

---

#### LoadFontFromImage()
``` c
Font LoadFontFromImage( Image image, Color key, int firstChar );
```
Load font from Image (XNA style)

---

#### LoadFontData()
``` c
CharInfo *LoadFontData( const char *fileName, int fontSize, int *fontChars, int charsCount, int type );
```
Load font data for further use

---

#### GenImageFontAtlas()
``` c
Image GenImageFontAtlas( const CharInfo *chars, Rectangle **recs, int charsCount, int fontSize, int padding, int packMethod );
```
Generate image font atlas using chars info

---

#### UnloadFont()
``` c
void UnloadFont( Font font );
```
Unload Font from GPU memory (VRAM)

---

## Text drawing functions

#### DrawFPS()
``` c
void DrawFPS( int posX, int posY );
```
Shows current FPS

---
#### DrawText()
``` c
void DrawText( const char *text, int posX, int posY, int fontSize, Color color );
```
Draw text (using default font)

---

#### DrawTextEx()
``` c
void DrawTextEx( Font font, const char *text, Vector2 position, float fontSize, float spacing, Color tint );
```
Draw text using font and additional parameters

---

#### DrawTextRec()
``` c
void DrawTextRec( Font font, const char *text, Rectangle rec, float fontSize, float spacing, bool wordWrap, Color tint );
```
Draw text using font inside rectangle limits

---

#### DrawTextRecEx()
``` c
void DrawTextRecEx( Font font, const char *text, Rectangle rec, float fontSize, float spacing, bool wordWrap, Color tint, int selectStart, int selectLength, olor selectTint, Color selectBackTint );
```
Draw text using font inside rectangle limits with support for text selection

---

#### DrawTextCodepoint()
``` c
void DrawTextCodepoint( Font font, int codepoint, Vector2 position, float scale, Color tint );
```
Draw one character (codepoint)

---

## Text misc. functions

#### MeasureText()
``` c
int MeasureText( const char *text, int fontSize );
```
Measure string width for default font

---

#### MeasureTextEx()
``` c
Vector2 MeasureTextEx( Font font, const char *text, float fontSize, float spacing );
```
Measure string size for Font

---

#### GetGlyphIndex()
``` c
int GetGlyphIndex( Font font, int codepoint );
```
Get index position for a unicode character on font

---

## Text strings management functions (no utf8 strings, only byte chars)
> NOTE: Some strings allocate memory internally for returned strings, just be careful!

#### TextCopy()
``` c
int TextCopy( char *dst, const char *src );
```
Copy one string to another, returns bytes copied

---

#### TextIsEqual()
``` c
bool TextIsEqual( const char *text1, const char *text2 );
```
Check if two text string are equal

---

#### TextLength()
``` c
unsigned int TextLength( const char *text );
```
Get text length, checks for '\0' ending

---

#### TextFormat()
``` c
const char *TextFormat( const char *text, ... );
```
Text formatting with variables (sprintf style)

---

#### TextSubtext()
``` c
const char *TextSubtext( const char *text, int position, int length );
```
Get a piece of a text string

---

#### TextReplace()
``` c
char *TextReplace( char *text, const char *replace, const char *by );
```
Replace text string (memory must be freed!)

---

#### TextInsert()
``` c
char *TextInsert( const char *text, const char *insert, int position );
```
Insert text in a position (memory must be freed!)

---

#### TextJoin()
``` c
const char *TextJoin( const char **textList, int count, const char *delimiter );
```
Join text strings with delimiter

---

### TextSplit()
``` c
const char **TextSplit( const char *text, char delimiter, int *count );
```
Split text into multiple strings

---

#### TextAppend()
``` c
void TextAppend( char *text, const char *append, int *position );
```
Append text at specific position and move cursor!

---

#### TextFindIndex()
``` c
int TextFindIndex( const char *text, const char *find );
```
Find first text occurrence within a string

---

#### TextToUpper()
``` c
const char *TextToUpper( const char *text );
```
Get upper case version of provided string

---

#### TextToLower()
``` c
const char *TextToLower( const char *text );
```
Get lower case version of provided string

---

#### TextToPascal()
``` c
const char *TextToPascal( const char *text );
```
Get Pascal case notation version of provided string

---

#### TextToInteger()
``` c
int TextToInteger( const char *text );
```
Get integer value from text (negative values not supported)

---

#### TextToUtf8()
``` c
char *TextToUtf8( int *codepoints, int length );
```
Encode text codepoint into utf8 text (memory must be freed!)

---

## UTF8 text strings management functions

#### GetCodepoints()
``` c
int *GetCodepoints( const char *text, int *count );
```
Get all codepoints in a string, codepoints count returned by parameters

---

#### GetCodepointsCount()
``` c
int GetCodepointsCount( const char *text );
```
Get total number of characters (codepoints) in a UTF8 encoded string

---

#### GetNextCodepoint()
``` c
int GetNextCodepoint( const char *text, int *bytesProcessed );
```
Returns next codepoint in a UTF8 encoded string; 0x3f('?') is returned on failure

---

#### CodepointToUtf8()
``` c
const char *CodepointToUtf8( int codepoint, int *byteLength );
```
Encode codepoint into utf8 text (char array length returned as parameter)

---
