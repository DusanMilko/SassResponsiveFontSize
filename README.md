Responsive Font Size
==================

Responsive Font Size Sass plugin using screen widths and automatic media querie generation

### Install

Install Sass, required for this plugin

Import the scss file into your main scss and add location of the file example: libs or partials

```
@import "LOCATION/responsive-font-size";
```

### Usage Example

In where you define your global variables

```
$xsmall-screen: 320px; // Mobile
$small-screen: 768px; // Tablet
$medium-screen: 940px; // Tablet Landscape
$large-screen: 1280px; // Small Desktop
$xlarge-screen: 1440px; // Large Desktop
```

In any class use:

> The font in the example goes from 12px on mobile devices to 15 right before it hits tablet, then on tablet uses 12 and goes up to 20 for desktop t a rate of 0.8em( every 0.8 ems its adjusts )

```
@include responsive-font-size (
  $min-font-size: em-calc(12), // Font size at smallest width
  $minbreak-font-size: em-calc(15), // Font size at medium break
  $maxbreak-font-size: em-calc(12), // Font size at other end of medium break
  $max-font-size: em-calc(20), // Font size at largest width
  $min-screen-width: $xsmall-screen, // Variable/value of small width
  $break-screen-width: $small-screen, // Variable/value of medium (breakpoint) width
  $max-screen-width: $xlarge-screen, // Variable/value of largest width 
  $font-size-step: 0.8em // Points of changes, the smaller = more css/more changes/smoother scaling of size
);
```

### Browser Support

---
> Works with browsers that support media queries. Basically everything except ie6,7,8. You can use a polyfill or shim to make media queries work in ie8.

---
