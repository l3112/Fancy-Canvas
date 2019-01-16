# Fancy-Canvas
Also from Wes Bos' JavaScript30. The hue code only works in certain places.
CanvasBasic is the single-color one.
CanvasFancy is the multi-hued one.

Look at this nifty canvas! There’s a canvas element, with width and height. It’s set at 800 for both, default, but I want to make it wider. (Which we do so , with window.innerWidth)

The context is what we’re drawing on, not the actual canvas (ctx) and ask for the context.

There are contexts for stroke style, linejoin, and line cap (which gives us that round tube-y brush)

let drawing false means you only draw when the mouse press is down; *down, true*, *up, false*

last coordinates = 0 —— a starting x and y

draw function takes an event, listening for the mouse move so it will draw (it’s logged)
stop function when the mouse isn’t down.

Eventlistener for mousedown
mouseout is when you move the mouse out of the canvas, it’s also read as a ‘not pressed down’

offset values come from the event that’s happening.

check the lasts so that things don’t just start from the point, or where you just stopped (check mousedown), so update your last x and last y

you can change the linewidth

ctx.strokestyle = `hsl(${hue}, 100%, 50%)`;
defining this stroke style with the other ctx elements before the function strangely doesn’t work.
