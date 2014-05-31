# jQuery dragscrollable Plugin
## Copyright (c) 2009 Miquel Herrera

Adds the ability to manage elements scroll by dragging
one or more of its descendant elements. Options parameter
allow to specifically select which inner elements will
respond to the drag events.

### options properties:

**dragSelector**

> jquery selector to apply to each wrapped element to find which will be the dragging elements.
> Defaults to '>:first' which is the first child of scrollable element

**acceptPropagatedEvent**

> Will the dragging element accept propagated events? default is yes, a propagated mouse event
> on a inner element will be accepted and processed. If set to false, only events originated on the
> draggable elements will be processed.

**preventDefault**

> Prevents the event to propagate further effectivey dissabling other default actions. Defaults to true

###usage examples:

To add the scroll by drag to the element id=viewport when dragging its first child accepting any propagated events

`$('#viewport').dragscrollable();`

 To add the scroll by drag ability to any element div of class viewport when dragging its first descendant of class
 dragMe responding only to events originated on the '.dragMe' elements.

`$('div.viewport').dragscrollable({dragSelector:'.dragMe:first', acceptPropagatedEvent: false});`

 Notice that some 'viewports' could be nested within others but events
 would not interfere as acceptPropagatedEvent is set to false.

 