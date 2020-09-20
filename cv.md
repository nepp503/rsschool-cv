1. **Vitali Siniak**
2. **Tel.:** *+421905957362*, **e-mail**: *nepp503@gmail.com*
3. Hi, my name is Vitali. I'm 26. Right now I'm working in Slovakia as Junior PLM Consultant. My main responsibility is to provide support and change our PLM software according to customer needs. These changes I make in Java code in XML files. My main goal right now is to gain as much experience as I can, to learn and become a high skill developer. I'm a very good learner, I'm very responsible and I adapt fast. To prove that right now I have a different project in my company. We develop web-app and I work on this project as frontend developer, so I had to learn fast and adapt to new project and its needs. Also I'm not afraid of challanges so I was able to move to Slovakia from Belarus according to family situation and its a new country for me, but I was able to adapt here and find a job. Its very important for me that I have a very smart people around me so I could learn from them. And I wish that my abilities as hard-worker and good-learner will help me to become a great developer.  
4. Java Core, Java EE, JSP, Tomcat Aplication Server, OOP, Git, HTML, CSS, JS, jQuery, Kendo UI, MySQL, BitBucket, English as a second language.  
5. Here are some latest examples of my code on project [GOMAN] (https://goman.sk):
```
      var global_WindowID = {MAIN_WINDOW_ID};
      var global_WindowObjectID = {MAIN_OBJECT_ID};
      var global_WindowItemID = {MAIN_ITEM_ID};
      var global_WindowParameters = [];
      var currentPage = {};

      var global_ReportObjects = [];

      <!— BEGIN: parameter —>
      global_WindowParameters["{PARAMETER_NAME}"] = "{PARAMETER_VALUE}";
      <!— END: parameter —>

      <!— BEGIN: standardwnd —>
      $(document).ready(function () {

      var splitter = $("#appMainSpliter-{MAIN_WINDOW_ID}").kendoSplitter({
      orientation: "vertical",
      panes: [
      { collapsible: true,size: "100%", xmin:"250px", size: "{MAIN_HEIGTH}px", xsize: "500px",collapsed: false ,scrollable: true },
      { collapsible: true, xsize: "250px",collapsed: {COLLAPS_RELSPLIT} }
      ]
      }).data("kendoSplitter");

      var tsobjectsMainView = $("#appMainViewsTabs-{MAIN_WINDOW_ID}").kendoTabStrip({
      animation: { open: { duration: 0} },
      activate: function(e) {
      var previousPage;
      globalHistory.length > 0 ? previousPage = globalHistory[globalHistory.length-historyIndex] : previousPage = undefined;
      currentPage = {
      windowId: {MAIN_WINDOW_ID},
      itemId: {MAIN_ITEM_ID},
      mainView: e.item.offsetParent.id,
      mainTab: e.item.getAttribute('aria-controls'),
      relView: $("#appRelationViewsTabs-{MAIN_WINDOW_ID}").length == 0 ? undefined : $("#appRelationViewsTabs-{MAIN_WINDOW_ID}").get(0).id,
      relTab: $("#appRelationViewsTabs-{MAIN_WINDOW_ID}").find(".k-content.k-state-active").length == 0 ?
      ($("#appRelationViewsTabs-{MAIN_WINDOW_ID}").find(".k-content").get(0) == undefined ? undefined : $("#appRelationViewsTabs-{MAIN_WINDOW_ID}").find(".k-content").get(0).id) :
      $("#appRelationViewsTabs-{MAIN_WINDOW_ID}").find(".k-content.k-state-active").get(0).id
      };
      if(!buttonWasClickedForMainTab){
      if(!checkTypeOfPreviousPage(currentPage, previousPage)){
      addToHistory(currentPage);
      }
      }
      buttonWasClickedForMainTab = false;
      }
      }).data('kendoTabStrip');

      var tsobjectsRelView =$("#appRelationViewsTabs-{MAIN_WINDOW_ID}").kendoTabStrip({
      animation: { open: { duration: 0} },
      select: onSelectRelTab,
      activate: function(e) {
      var previousPage;
      globalHistory.length > 0 ? previousPage = globalHistory[globalHistory.length-1] : previousPage = undefined;
      currentPage = {
      windowId: {MAIN_WINDOW_ID},
      itemId: {MAIN_ITEM_ID},
      mainView: $("#appMainViewsTabs-{MAIN_WINDOW_ID}").get(0).id,
      mainTab: $("#appMainViewsTabs-{MAIN_WINDOW_ID}").find(".k-content.k-state-active").length == 0 ?
      ($("#appMainViewsTabs-{MAIN_WINDOW_ID}").find(".k-content").get(0) == undefined ? undefined : $("#appMainViewsTabs-{MAIN_WINDOW_ID}").find(".k-content").get(0).id) :
      $("#appMainViewsTabs-{MAIN_WINDOW_ID}").find(".k-content.k-state-active").get(0).id,
      relView: e.item.offsetParent.id,
      relTab: e.item.getAttribute('aria-controls')
      };
      if(!buttonWasClickedForRelTab){
      if(!checkTypeOfPreviousPage(currentPage, previousPage)){
      addToHistory(currentPage);
      }
      }
      buttonWasClickedForRelTab = false;
      }
      }).data("kendoTabStrip");
      <!— BEGIN: viewtab —>
      tsobjectsMainView.append(
      [{
      text: "<span class=\"k-icon k-icon-24 k-i-folder\"></span>" + "{VIEW_TITLE}",
      encoded: false,
      contentUrl:

      "./app/view.php?forwindowid={MAIN_WINDOW_ID}&viewid={MAIN_VIEW_ID}&mainview=true&autobind={AUTO_BIND}&itemobjectid={MAIN_OBJECT_ID}&itemid={MAIN_ITEM_ID}&viewrelations={REL_RELATIONS}&addtorelateddatasource=true&{ADD_URL_PARAMS}"
      }]
      );
      <!— END: viewtab —>

      if(buttonWasClickedForMainTab){
      tsobjectsMainView.select('li[aria-controls='+globalHistory[globalHistory.length-historyIndex].mainTab+']');
      }else{
      tsobjectsMainView.select(0);
      }

      <!— BEGIN: viewtabrel —>
      tsobjectsRelView.append(
      [{
      text: "<span class=\"k-icon k-icon-24 k-i-folder\"></span>" + "{VIEW_TITLE}",
      encoded: false,
      contentUrl:"./app/view.php?forwindowid={MAIN_WINDOW_ID}&viewid={REL_VIEW_ID}&mainview=false&autobind={AUTO_BIND}&itemobjectid={MAIN_OBJECT_ID}&itemid={MAIN_ITEM_ID}&viewrelations={REL_RELATIONS}&addtorelateddatasource=true"
      }]
      );
      <!— END: viewtabrel —>

      if(buttonWasClickedForRelTab && globalHistory[globalHistory.length-historyIndex].relTab != undefined){
      tsobjectsRelView.select('li[aria-controls='+globalHistory[globalHistory.length-historyIndex].relTab+']');
      }else{
      tsobjectsRelView.select(0);
      }

      <!— BEGIN: hidesplitterrel —>
      splitter.remove(".k-pane:last");
      <!— END: hidesplitterrel —>

      });
 ```
