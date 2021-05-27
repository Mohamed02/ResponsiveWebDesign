RESPONSIVE WEB DESING


    REMOTE DEBUGGING: you use remote debugging by connecting your mobile to the desktop via usb cable for doign an inpect elment or opening dev tool bar.

    VIEWPORT: IT defines the area of the screen where the browser can render its content.


    HARDWARE PIXELS:
            WHen you buy a camera it will say it is a 100Mpixel camera. So here pixel means when a you captue an image with this camera, the image will have 100Mpixel
            that is in one sqmm area (not sure exactly the area) we have 100Mpixels. The higher the number of pixels the higher will be teh clarity of the image you captures

            here pixel is nothing but a small dot and the size of each pixel varies dependign on the camera you took the pic. for a poor clarity pic, the pixes size is larger, when compared
            to the good contrast image, which will have pixel size as smaller
            
            Hardware pixel is nothing but the pixel density.

            Similarty when you buy a laptop, as per the specification the screen resolution may for e.g 2200px. And your desktop resolution si 1400px.
            this means that the one with 2200pxels are packed in the laptop screen which makes the screen of good HD quality and displays high quqlity images perfcetly.

    DEVICE INDEPENDENT PIXELS:
            When it comes to browser rendering , browser uses a measuring unit called PIXELS, and this pixels is different from the HARDWARE PIXELS.
            that pixel is called Device Independent pixels. DIP is actually a unit of measurement

            on higher contrast devices , 1 Device Independent Pixel can hold 2 Hardware pixels or more

            where as in poor contrast devices or pictures, 1 DIP hold only part of the Hardware pixel. and it requires
            more than one DIP to hold a Hardware pixels

    VIEWPORT METATAG:

        When you dont define viewport tag, while rendering a page in a device with Hardware Pixels 1200px, then it will consider
        hardware pixels are DIP and it will consider it as a large screen and render the content as it renders in teh browser. and the user 
        has to pinch and zoom to see the content.

        IN contrast, when youd defin the viewport metatag and set the width as content width and if you had developed your page as RESPONSIVE
        then view port width will be mesured in terms of no of device Independent pixels and the page will be rendered in a way that it should 
        rendered in small devices.

    PIXEL RATIO:

        No of HARDWARE Pixels per DEVICE INDEPENDENT PIXEL

        A mobile screen has a resolution of 1920 x 1080 px with a device pixel ratio of 2. 
        What is the maximum width of a viewport in landscape mode measured in CSS pixels?

            960

        <meta name="viewport" content="width=device-width,initial-scalle=1">

        here width is set as the device-width in Device Independant pixels

        initial-scale as 1 , instructs the browser to establish 1:1 ration between Device Independent pixes and CSS Pixesl


    Why Mobile First Approach?

        When we start with developing content for small devices and moving up for larger devices, we can prioritize the contents so that we give required contents
        for mobile user and then show additional content for large devices.

        If it is otherway around, we will show all the contents on large devices and we strip down some contents to not to show it in mobile devices.
        this may result in we may skipping some of the important content on mobile devices.


    MEDIA QUERIES:
        IT helps to applies styles specifc to devices

        <link rel="stylesheet" media="screen and (min-width:500px)" href="over500.css">

        the above stylesheet will get applied only on devices with width 500px or more


        you can also apply media query on the stylesheet file as below

        @media screen and (min-width: 500px){
            body {
                    color: #F79420
            }
        }
         @media screen and (max-width: 500px){
            body {
                    font-size: 20px
            }
        }
        min-width is based on browser window and min-device-width is based on teh device width


    GRID

    Refer https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout

    FLEX BOX

            display:FLEX
            flex-wrap:wrap
            order: 4


    RESPONSIVE PATTERNS

        1. MOSTLY FLUID
        2. COLOUMN DROP
        3. LAYOUT SHIFTER
        4. OFF CANVAS

    COLOUMN DROP:

        here if we have three boxes ocupying equal spaces on the same line, when the width reduces, boxes will be dropped to the sencond row
        and for devices with smallest width , column appears one below one.


    MOSTLY FLUID :

    LAYOUT SHIFTER:
            In this arrangement of boxes are chagned thrugh flex box order when the viewport width is changed

    OFF CANVAS:
            In this the some of the elements are hidden on small devices on the nav drawer.



    RESPONSIVE IMAGES:
            Images can be made responsive with followign options
                1. Relative sizeing by setting width as percentage and max-width
                2. Use calc to calculate width.
                3. use units such as viewport hieight vh, vw, vmin,vmax
                4. Using Source set srcset attribute to load image appropriate to teh device resolution
    
    RESPONSIVE TABLES:

            A Table can be made responsive by hiding some of the tds on small devices or setting overflow as scroll.
