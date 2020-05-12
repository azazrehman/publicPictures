
Documentation for two modules:
- [common APIs](## puppeteerAPI.js File Documentation)
- [Common/Repetive Steps](## commonFunction.js File Documentation)

<a name="puppeteerAPI.js File Documentation"></a> 
## puppeteerAPI.js File Documentation

There are several checks and clicks used many times in our code. To avoid repetition of code, we created a separate file named "puppeteerAPI.js” having reusable functions.
 
Following are the functions of puppeteerAPI.js

- [Click on any Element](###click)
- [Click With Navigate](#clickWithNavigate)
- [Type a text](#typeText)
- [Should Exist Element](#shouldExist)
- [Click on XPATH element](#click_xPath)
- [Take Screen shot](#takeScreenShot)
- [loadUrl](#loadUrl)
- [getText](#getText)
- [getCount](#getCount)
- [pressKey](#pressKey)
- [downKey](#downKey)
- [upKey](#upKey)
- [shouldExistXPath](#shouldExistXPath)
- [shouldNotExist](#shouldNotExist)
- [doubleClick](#doubleClick)
- [isExist](#isExist)
- [setAttribute](#setAttribute)
- [selectValueFromDropDown](#selectValueFromDropDown)
- [waitForXPath](#waitForXPath)
- [wait Until Element is Invisible](#waitUntilElementInvisible)
----------------------------------
<a name="click"></a> 
### click 
 
Most commonly used action in puppeteer, This function will be used to click the elements
 
Parameters
 
    *page - page or a frame in which your selector exist which you want to click
    *selector - A selector which you want to click
    *button - the mouse button which you want to triger, default button is left 
    
<a name="clickWithNavigate"></a>    
### clickWithNavigate
 
Click in any element with single Promise Navigation
 
Parameters
 
    * page - page or a frame in which your selector exist which you want to click
    * selector - A selector which you want to click
    * button - the mouse button which you want to triger, default button is left
    
<a name="typeText"></a>     
### typeText
 
This function will be used to Type a text on Any input type Element
 
Parameters
 
    * page - page or a frame in which your selector exist and you want to type text in that
    * text - sequences of characters which you want to type
    * selector - A selector in which you want to type
    * myDelay - delay in typing the text on given selector, default delay is 80 milisecond
 
<a name="loadUrl"></a> 
### loadUrl
 
This will help to load url of any page.
 
Parameters
 
    * page - page or a frame in which your URL exist and you want to load
    * URL - that specific url you want to load

<a name="getText"></a> 
### getText
 
 "getText" function will be used to Get a text from DOM Element
 
Parameters:
 
      page - page or a frame in which your selector exist and you want to type text in that
      selector - A selector whose inside HTML text you want to retrieve

<a name="click_xPath"></a>
### click_xPath
 " click_xPath" will be used to Click on Any XPATH Element
 
Parameters:
 
       page - page or a frame in which your selector exist which you want to click
       selector - A XPATH selector which you want to click

<a name="getCount"></a>
### getCount
This function will Get Number of count of given Element
 
Parameters:
       *page - page or a frame in which your selector exist which you want to click
       *selector - A selector which you want to count
 
<a name="pressKey"></a>
### pressKey
Press Any key from Keyboard to Page or frame and release key
 
Parameters:
 
     *page - page or a frame in which your selector exist which you want to click
     *key - A key which u want to press like (1 or 2 or Tab etc)

<a name="downKey"></a>
### downKey
 This function will be used to Press and Hold Any key from Keyboard to Page or frame
 
 Parameters:
 
    *page - page or a frame in which your selector exist which you want to click
    *key - A key which u want to press and Hold like (Enter or Shift or Ctrl etc)

<a name="upKey"></a>
### upKey
This function will be used to Release Key Pressed by Keyboard on Page or frame
 
Parameters:
 
    * page - page or a frame in which your selector exist which you want to click
    * key - A key which u want to release like (Enter or Shift or Ctrl etc)

<a name="shouldExist"></a>
### shouldExist
"shouldExist" this will be used to make sure given element exist on a page or frame if not it throw error
 
Parameters:
 
    *page - page or a frame in which you check your selector exist
    *selector - A selector which u want to verify it exist on page or frame

<a name="shouldExistXPath"></a>
### shouldExistXPath
"shouldExistXPath" this will be  used to make sure given XPATH element exist on a page or frame if not it throw error
 
Parameters:
 
    *page - page or a frame where selector u want to findt
    *selector - A XPATH selector which u want to verify it exist on page or frame

<a name="shouldNotExist"></a>
### shouldNotExist
"shouldNotExist" this function will be used to make sure given element can't exist on a page or frame if exist return true
 
Parameters: 
 
    *page - page or a frame where selector u want to findt
    * selector - A  selector which u want to verify it not exist on page or frame
    * timeOut - timeOut Value to wait maximum for given selector

<a name="doubleClick"></a>
### doubleClick
"doubleClick" - Double click on given elemnnt reside on given page or frame
 
Parameters:
 
    *page - page or a frame where selector u want to findt
    *selector - A  selector on which u want to double click

<a name="isExist"></a> 
### isExist
<a name="isExist"></a>
"isExist" - Check Element is exist on page or not
 
Parameters:
 
    *page - page or a frame where selector u want to findt
    *selector - A  selector which u want to verify it exist or not on page or frame
    *timeOut - timeOut Value to wait maximum for given selector

<a name="setAttribute"></a>    
### setAttribute
 "setAttribute" - Set attribute on Element
 
 Parameters:
 
    *page - page or a frame where selector u want to findt
    *selector - A  selector which u want toadd attributes
    *attributeName - A  attribute name which u want to add
    *attributeValue - A attributeValue which u want to add in given new attribute

<a name="takeScreenShot"></a>
### takeScreenShot
"takeScreenShot" - Take screen shot of a Page while running tests
 
Parameters :
 
   *page - page or a frame whose screen shot u want to taken.

<a name="selectValueFromDropDown"></a>
### selectValueFromDropDown
 
This function will be used to select Value From DropDown menu
 
Parameter:
    *page - page or a frame where selector u want to findt
    *selectSelector - A dropdown select element
    *optionValue - an option value to select from options

<a name="waitForXPath"></a>
### waitForXPath
 
This function will be used to Wait for Element by XPATH in order to perform action on that
 
Parameter:
 
    *page - page or a frame where selector u want to wait
    *selector - A XPATH selector which u want wait for visible

<a name="waitUntilElementInvisible"></a>
### waitUntilElementInvisible
 
"waitUntilElementInvisible" -  Wait Until Specific Element Invisible or gone from a page or frame    
Parameters:
 
    *page - page or a frame where selector u want to findt
    *selector - A  selector whose u want to wait for disappear
    *maximumTime - maximum time which u want to wait the element

<a name="commonFunction.js File Documentation"></a> 
## commonFunction.js File Documentation
comming soon...

This is not the end. its just beginning :wink: