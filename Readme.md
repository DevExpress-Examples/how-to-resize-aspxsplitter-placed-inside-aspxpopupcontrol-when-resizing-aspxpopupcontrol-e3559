<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/WebSite/Default.aspx) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
* [Default.aspx.cs](./CS/WebSite/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/WebSite/Default.aspx.vb))
<!-- default file list end -->
# How to resize ASPxSplitter placed inside ASPxPopupControl when resizing ASPxPopupControl
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e3559/)**
<!-- run online end -->


<p>At present, ASPxPopupControl does not have the built-in capability to resize nested controls when it's resizing. This example illustrates how to automatically resize controls places inside the popup. To accomplish this task, execute the following steps:</p><p>1. Set the <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxPopupControlASPxPopupControlBase_ScrollBarstopic"><u>ASPxPopupControl.ScrollBars</u></a> property to "Auto". This option will allow the popup control to evaluate the content width and height.</p><p>2. Handle the <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxPopupControlScriptsASPxClientPopupControlBase_AfterResizingtopic"><u>ASPxClientPopupControl.AfterResizing</u></a> event. In this event handler, call the <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxClassesScriptsASPxClientControl_AdjustControltopic"><u>AdjustControl</u></a> method for a desired control to force it to reevaluate its size.</p><p>3. Place the control into the <strong><div style="height: 100%; width: 100%; overflow: hidden"></strong> element. This element is necessary to overcome scrollbars that can be shown when ScrollBars="Auto" is set.</p>

<br/>


