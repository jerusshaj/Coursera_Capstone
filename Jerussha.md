```
import requests
```


```
#link of the website through which we are going to scrape the data
url = 'https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M'
website_url = requests.get(url).text
```


```
from bs4 import BeautifulSoup
```


```
#view how the tags are nested in the document
soup = BeautifulSoup(website_url,'lxml')
print(soup.prettify())
```

    <!DOCTYPE html>
    <html class="client-nojs" dir="ltr" lang="en">
     <head>
      <meta charset="utf-8"/>
      <title>
       List of postal codes of Canada: M - Wikipedia
      </title>
      <script>
       document.documentElement.className="client-js";RLCONF={"wgBreakFrames":!1,"wgSeparatorTransformTable":["",""],"wgDigitTransformTable":["",""],"wgDefaultDateFormat":"dmy","wgMonthNames":["","January","February","March","April","May","June","July","August","September","October","November","December"],"wgRequestId":"3ad865cd-79b8-49be-b442-e7b7797acd3d","wgCSPNonce":!1,"wgCanonicalNamespace":"","wgCanonicalSpecialPageName":!1,"wgNamespaceNumber":0,"wgPageName":"List_of_postal_codes_of_Canada:_M","wgTitle":"List of postal codes of Canada: M","wgCurRevisionId":979555370,"wgRevisionId":979555370,"wgArticleId":539066,"wgIsArticle":!0,"wgIsRedirect":!1,"wgAction":"view","wgUserName":null,"wgUserGroups":["*"],"wgCategories":["Articles with short description","Short description is different from Wikidata","Communications in Ontario","Postal codes in Canada","Toronto","Ontario-related lists"],"wgPageContentLanguage":"en","wgPageContentModel":"wikitext","wgRelevantPageName":
    "List_of_postal_codes_of_Canada:_M","wgRelevantArticleId":539066,"wgIsProbablyEditable":!0,"wgRelevantPageIsProbablyEditable":!0,"wgRestrictionEdit":[],"wgRestrictionMove":[],"wgMediaViewerOnClick":!0,"wgMediaViewerEnabledByDefault":!0,"wgPopupsReferencePreviews":!1,"wgPopupsConflictsWithNavPopupGadget":!1,"wgVisualEditor":{"pageLanguageCode":"en","pageLanguageDir":"ltr","pageVariantFallbacks":"en"},"wgMFDisplayWikibaseDescriptions":{"search":!0,"nearby":!0,"watchlist":!0,"tagline":!1},"wgWMESchemaEditAttemptStepOversample":!1,"wgULSCurrentAutonym":"English","wgNoticeProject":"wikipedia","wgCentralAuthMobileDomain":!1,"wgEditSubmitButtonLabelPublish":!0,"wgULSPosition":"interlanguage","wgWikibaseItemId":"Q3248240"};RLSTATE={"ext.globalCssJs.user.styles":"ready","site.styles":"ready","noscript":"ready","user.styles":"ready","ext.globalCssJs.user":"ready","user":"ready","user.options":"loading","ext.cite.styles":"ready","skins.vector.styles.legacy":"ready",
    "jquery.tablesorter.styles":"ready","ext.visualEditor.desktopArticleTarget.noscript":"ready","ext.uls.interlanguage":"ready","ext.wikimediaBadges":"ready","wikibase.client.init":"ready"};RLPAGEMODULES=["ext.cite.ux-enhancements","site","mediawiki.page.ready","jquery.tablesorter","skins.vector.legacy.js","ext.gadget.ReferenceTooltips","ext.gadget.charinsert","ext.gadget.extra-toolbar-buttons","ext.gadget.refToolbar","ext.gadget.switcher","ext.centralauth.centralautologin","mmv.head","mmv.bootstrap.autostart","ext.popups","ext.visualEditor.desktopArticleTarget.init","ext.visualEditor.targetLoader","ext.eventLogging","ext.wikimediaEvents","ext.navigationTiming","ext.uls.compactlinks","ext.uls.interface","ext.cx.eventlogging.campaigns","ext.quicksurveys.init","ext.centralNotice.geoIP","ext.centralNotice.startUp"];
      </script>
      <script>
       (RLQ=window.RLQ||[]).push(function(){mw.loader.implement("user.options@1hzgi",function($,jQuery,require,module){/*@nomin*/mw.user.tokens.set({"patrolToken":"+\\","watchToken":"+\\","csrfToken":"+\\"});
    });});
      </script>
      <link href="/w/load.php?lang=en&amp;modules=ext.cite.styles%7Cext.uls.interlanguage%7Cext.visualEditor.desktopArticleTarget.noscript%7Cext.wikimediaBadges%7Cjquery.tablesorter.styles%7Cskins.vector.styles.legacy%7Cwikibase.client.init&amp;only=styles&amp;skin=vector" rel="stylesheet"/>
      <script async="" src="/w/load.php?lang=en&amp;modules=startup&amp;only=scripts&amp;raw=1&amp;skin=vector">
      </script>
      <meta content="" name="ResourceLoaderDynamicStyles"/>
      <link href="/w/load.php?lang=en&amp;modules=site.styles&amp;only=styles&amp;skin=vector" rel="stylesheet"/>
      <meta content="MediaWiki 1.36.0-wmf.18" name="generator"/>
      <meta content="origin" name="referrer"/>
      <meta content="origin-when-crossorigin" name="referrer"/>
      <meta content="origin-when-cross-origin" name="referrer"/>
      <link href="//upload.wikimedia.org" rel="preconnect"/>
      <link href="//en.m.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M" media="only screen and (max-width: 720px)" rel="alternate"/>
      <link href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=edit" rel="alternate" title="Edit this page" type="application/x-wiki"/>
      <link href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=edit" rel="edit" title="Edit this page"/>
      <link href="/static/apple-touch/wikipedia.png" rel="apple-touch-icon"/>
      <link href="/static/favicon/wikipedia.ico" rel="shortcut icon"/>
      <link href="/w/opensearch_desc.php" rel="search" title="Wikipedia (en)" type="application/opensearchdescription+xml"/>
      <link href="//en.wikipedia.org/w/api.php?action=rsd" rel="EditURI" type="application/rsd+xml"/>
      <link href="//creativecommons.org/licenses/by-sa/3.0/" rel="license"/>
      <link href="https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M" rel="canonical"/>
      <link href="//login.wikimedia.org" rel="dns-prefetch"/>
      <link href="//meta.wikimedia.org" rel="dns-prefetch"/>
     </head>
     <body class="mediawiki ltr sitedir-ltr mw-hide-empty-elt ns-0 ns-subject mw-editable page-List_of_postal_codes_of_Canada_M rootpage-List_of_postal_codes_of_Canada_M skin-vector action-view skin-vector-legacy">
      <div class="noprint" id="mw-page-base">
      </div>
      <div class="noprint" id="mw-head-base">
      </div>
      <div class="mw-body" id="content" role="main">
       <a id="top">
       </a>
       <div class="mw-body-content" id="siteNotice">
        <!-- CentralNotice -->
       </div>
       <div class="mw-indicators mw-body-content">
       </div>
       <h1 class="firstHeading" id="firstHeading" lang="en">
        List of postal codes of Canada: M
       </h1>
       <div class="mw-body-content" id="bodyContent">
        <div class="noprint" id="siteSub">
         From Wikipedia, the free encyclopedia
        </div>
        <div id="contentSub">
        </div>
        <div id="contentSub2">
        </div>
        <div id="jump-to-nav">
        </div>
        <a class="mw-jump-link" href="#mw-head">
         Jump to navigation
        </a>
        <a class="mw-jump-link" href="#searchInput">
         Jump to search
        </a>
        <div class="mw-content-ltr" dir="ltr" id="mw-content-text" lang="en">
         <div class="mw-parser-output">
          <div class="shortdescription nomobile noexcerpt noprint searchaux" style="display:none">
           Wikipedia list article
          </div>
          <p>
           This is a list of
           <a href="/wiki/Postal_codes_in_Canada" title="Postal codes in Canada">
            postal codes in Canada
           </a>
           where the first letter is M. Postal codes beginning with M are located within the city of
           <a href="/wiki/Toronto" title="Toronto">
            Toronto
           </a>
           in the province of
           <a href="/wiki/Ontario" title="Ontario">
            Ontario
           </a>
           . Only the first three characters are listed, corresponding to the Forward Sortation Area.
          </p>
          <p>
           <a href="/wiki/Canada_Post" title="Canada Post">
            Canada Post
           </a>
           provides a free postal code look-up tool on its website,
           <sup class="reference" id="cite_ref-1">
            <a href="#cite_note-1">
             [1]
            </a>
           </sup>
           via its
           <a href="/wiki/Mobile_app" title="Mobile app">
            applications
           </a>
           for such
           <a class="mw-redirect" href="/wiki/Smartphones" title="Smartphones">
            smartphones
           </a>
           as the
           <a href="/wiki/IPhone" title="IPhone">
            iPhone
           </a>
           and
           <a href="/wiki/BlackBerry" title="BlackBerry">
            BlackBerry
           </a>
           ,
           <sup class="reference" id="cite_ref-2">
            <a href="#cite_note-2">
             [2]
            </a>
           </sup>
           and sells hard-copy directories and
           <a href="/wiki/CD-ROM" title="CD-ROM">
            CD-ROMs
           </a>
           . Many vendors also sell validation tools, which allow customers to properly match addresses and postal codes. Hard-copy directories can also be consulted in all post offices, and some libraries.
          </p>
          <h2>
           <span class="mw-headline" id="Toronto_-_103_FSAs">
            <a href="/wiki/Toronto" title="Toronto">
             Toronto
            </a>
            - 103
            <a href="/wiki/Postal_codes_in_Canada#Forward_sortation_areas" title="Postal codes in Canada">
             FSAs
            </a>
           </span>
           <span class="mw-editsection">
            <span class="mw-editsection-bracket">
             [
            </span>
            <a href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=edit&amp;section=1" title="Edit section: Toronto - 103 FSAs">
             edit
            </a>
            <span class="mw-editsection-bracket">
             ]
            </span>
           </span>
          </h2>
          <p>
           Note: There are no rural FSAs in Toronto, hence no postal codes should start with M0. However, the postal code M0R 8T0 is assigned to an
           <a href="/wiki/Amazon_(company)" title="Amazon (company)">
            Amazon
           </a>
           warehouse in Mississauga, suggesting that Canada Post may have reserved the M0 FSA for high volume addresses.
          </p>
          <table class="wikitable sortable">
           <tbody>
            <tr>
             <th>
              Postal Code
             </th>
             <th>
              Borough
             </th>
             <th>
              Neighbourhood
             </th>
            </tr>
            <tr>
             <td>
              M1A
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M2A
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3A
             </td>
             <td>
              North York
             </td>
             <td>
              Parkwoods
             </td>
            </tr>
            <tr>
             <td>
              M4A
             </td>
             <td>
              North York
             </td>
             <td>
              Victoria Village
             </td>
            </tr>
            <tr>
             <td>
              M5A
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Regent Park, Harbourfront
             </td>
            </tr>
            <tr>
             <td>
              M6A
             </td>
             <td>
              North York
             </td>
             <td>
              Lawrence Manor, Lawrence Heights
             </td>
            </tr>
            <tr>
             <td>
              M7A
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Queen's Park, Ontario Provincial Government
             </td>
            </tr>
            <tr>
             <td>
              M8A
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9A
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              Islington Avenue, Humber Valley Village
             </td>
            </tr>
            <tr>
             <td>
              M1B
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Malvern, Rouge
             </td>
            </tr>
            <tr>
             <td>
              M2B
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3B
             </td>
             <td>
              North York
             </td>
             <td>
              Don Mills
             </td>
            </tr>
            <tr>
             <td>
              M4B
             </td>
             <td>
              East York
             </td>
             <td>
              Parkview Hill, Woodbine Gardens
             </td>
            </tr>
            <tr>
             <td>
              M5B
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Garden District, Ryerson
             </td>
            </tr>
            <tr>
             <td>
              M6B
             </td>
             <td>
              North York
             </td>
             <td>
              Glencairn
             </td>
            </tr>
            <tr>
             <td>
              M7B
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8B
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9B
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              West Deane Park, Princess Gardens, Martin Grove, Islington, Cloverdale
             </td>
            </tr>
            <tr>
             <td>
              M1C
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Rouge Hill, Port Union, Highland Creek
             </td>
            </tr>
            <tr>
             <td>
              M2C
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3C
             </td>
             <td>
              North York
             </td>
             <td>
              Don Mills
             </td>
            </tr>
            <tr>
             <td>
              M4C
             </td>
             <td>
              East York
             </td>
             <td>
              Woodbine Heights
             </td>
            </tr>
            <tr>
             <td>
              M5C
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              St. James Town
             </td>
            </tr>
            <tr>
             <td>
              M6C
             </td>
             <td>
              York
             </td>
             <td>
              Humewood-Cedarvale
             </td>
            </tr>
            <tr>
             <td>
              M7C
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8C
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9C
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              Eringate, Bloordale Gardens, Old Burnhamthorpe, Markland Wood
             </td>
            </tr>
            <tr>
             <td>
              M1E
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Guildwood, Morningside, West Hill
             </td>
            </tr>
            <tr>
             <td>
              M2E
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3E
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4E
             </td>
             <td>
              East Toronto
             </td>
             <td>
              The Beaches
             </td>
            </tr>
            <tr>
             <td>
              M5E
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Berczy Park
             </td>
            </tr>
            <tr>
             <td>
              M6E
             </td>
             <td>
              York
             </td>
             <td>
              Caledonia-Fairbanks
             </td>
            </tr>
            <tr>
             <td>
              M7E
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8E
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9E
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1G
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Woburn
             </td>
            </tr>
            <tr>
             <td>
              M2G
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3G
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4G
             </td>
             <td>
              East York
             </td>
             <td>
              Leaside
             </td>
            </tr>
            <tr>
             <td>
              M5G
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Central Bay Street
             </td>
            </tr>
            <tr>
             <td>
              M6G
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Christie
             </td>
            </tr>
            <tr>
             <td>
              M7G
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8G
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9G
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1H
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Cedarbrae
             </td>
            </tr>
            <tr>
             <td>
              M2H
             </td>
             <td>
              North York
             </td>
             <td>
              Hillcrest Village
             </td>
            </tr>
            <tr>
             <td>
              M3H
             </td>
             <td>
              North York
             </td>
             <td>
              Bathurst Manor, Wilson Heights, Downsview North
             </td>
            </tr>
            <tr>
             <td>
              M4H
             </td>
             <td>
              East York
             </td>
             <td>
              Thorncliffe Park
             </td>
            </tr>
            <tr>
             <td>
              M5H
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Richmond, Adelaide, King
             </td>
            </tr>
            <tr>
             <td>
              M6H
             </td>
             <td>
              West Toronto
             </td>
             <td>
              Dufferin, Dovercourt Village
             </td>
            </tr>
            <tr>
             <td>
              M7H
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8H
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9H
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1J
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Scarborough Village
             </td>
            </tr>
            <tr>
             <td>
              M2J
             </td>
             <td>
              North York
             </td>
             <td>
              Fairview, Henry Farm, Oriole
             </td>
            </tr>
            <tr>
             <td>
              M3J
             </td>
             <td>
              North York
             </td>
             <td>
              Northwood Park, York University
             </td>
            </tr>
            <tr>
             <td>
              M4J
             </td>
             <td>
              East York
             </td>
             <td>
              East Toronto, Broadview North (Old East York)
             </td>
            </tr>
            <tr>
             <td>
              M5J
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Harbourfront East, Union Station, Toronto Islands
             </td>
            </tr>
            <tr>
             <td>
              M6J
             </td>
             <td>
              West Toronto
             </td>
             <td>
              Little Portugal, Trinity
             </td>
            </tr>
            <tr>
             <td>
              M7J
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8J
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9J
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1K
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Kennedy Park, Ionview, East Birchmount Park
             </td>
            </tr>
            <tr>
             <td>
              M2K
             </td>
             <td>
              North York
             </td>
             <td>
              Bayview Village
             </td>
            </tr>
            <tr>
             <td>
              M3K
             </td>
             <td>
              North York
             </td>
             <td>
              Downsview
             </td>
            </tr>
            <tr>
             <td>
              M4K
             </td>
             <td>
              East Toronto
             </td>
             <td>
              The Danforth West, Riverdale
             </td>
            </tr>
            <tr>
             <td>
              M5K
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Toronto Dominion Centre, Design Exchange
             </td>
            </tr>
            <tr>
             <td>
              M6K
             </td>
             <td>
              West Toronto
             </td>
             <td>
              Brockton, Parkdale Village, Exhibition Place
             </td>
            </tr>
            <tr>
             <td>
              M7K
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8K
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9K
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1L
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Golden Mile, Clairlea, Oakridge
             </td>
            </tr>
            <tr>
             <td>
              M2L
             </td>
             <td>
              North York
             </td>
             <td>
              York Mills, Silver Hills
             </td>
            </tr>
            <tr>
             <td>
              M3L
             </td>
             <td>
              North York
             </td>
             <td>
              Downsview
             </td>
            </tr>
            <tr>
             <td>
              M4L
             </td>
             <td>
              East Toronto
             </td>
             <td>
              India Bazaar, The Beaches West
             </td>
            </tr>
            <tr>
             <td>
              M5L
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Commerce Court, Victoria Hotel
             </td>
            </tr>
            <tr>
             <td>
              M6L
             </td>
             <td>
              North York
             </td>
             <td>
              North Park, Maple Leaf Park, Upwood Park
             </td>
            </tr>
            <tr>
             <td>
              M7L
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8L
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9L
             </td>
             <td>
              North York
             </td>
             <td>
              Humber Summit
             </td>
            </tr>
            <tr>
             <td>
              M1M
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Cliffside, Cliffcrest, Scarborough Village West
             </td>
            </tr>
            <tr>
             <td>
              M2M
             </td>
             <td>
              North York
             </td>
             <td>
              Willowdale, Newtonbrook
             </td>
            </tr>
            <tr>
             <td>
              M3M
             </td>
             <td>
              North York
             </td>
             <td>
              Downsview
             </td>
            </tr>
            <tr>
             <td>
              M4M
             </td>
             <td>
              East Toronto
             </td>
             <td>
              Studio District
             </td>
            </tr>
            <tr>
             <td>
              M5M
             </td>
             <td>
              North York
             </td>
             <td>
              Bedford Park, Lawrence Manor East
             </td>
            </tr>
            <tr>
             <td>
              M6M
             </td>
             <td>
              York
             </td>
             <td>
              Del Ray, Mount Dennis, Keelsdale and Silverthorn
             </td>
            </tr>
            <tr>
             <td>
              M7M
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8M
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9M
             </td>
             <td>
              North York
             </td>
             <td>
              Humberlea, Emery
             </td>
            </tr>
            <tr>
             <td>
              M1N
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Birch Cliff, Cliffside West
             </td>
            </tr>
            <tr>
             <td>
              M2N
             </td>
             <td>
              North York
             </td>
             <td>
              Willowdale, Willowdale East
             </td>
            </tr>
            <tr>
             <td>
              M3N
             </td>
             <td>
              North York
             </td>
             <td>
              Downsview
             </td>
            </tr>
            <tr>
             <td>
              M4N
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              Lawrence Park
             </td>
            </tr>
            <tr>
             <td>
              M5N
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              Roselawn
             </td>
            </tr>
            <tr>
             <td>
              M6N
             </td>
             <td>
              York
             </td>
             <td>
              Runnymede, The Junction North
             </td>
            </tr>
            <tr>
             <td>
              M7N
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8N
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9N
             </td>
             <td>
              York
             </td>
             <td>
              Weston
             </td>
            </tr>
            <tr>
             <td>
              M1P
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Dorset Park, Wexford Heights, Scarborough Town Centre
             </td>
            </tr>
            <tr>
             <td>
              M2P
             </td>
             <td>
              North York
             </td>
             <td>
              York Mills West
             </td>
            </tr>
            <tr>
             <td>
              M3P
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4P
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              Davisville North
             </td>
            </tr>
            <tr>
             <td>
              M5P
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              Forest Hill North &amp; West, Forest Hill Road Park
             </td>
            </tr>
            <tr>
             <td>
              M6P
             </td>
             <td>
              West Toronto
             </td>
             <td>
              High Park, The Junction South
             </td>
            </tr>
            <tr>
             <td>
              M7P
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8P
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9P
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              Westmount
             </td>
            </tr>
            <tr>
             <td>
              M1R
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Wexford, Maryvale
             </td>
            </tr>
            <tr>
             <td>
              M2R
             </td>
             <td>
              North York
             </td>
             <td>
              Willowdale, Willowdale West
             </td>
            </tr>
            <tr>
             <td>
              M3R
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4R
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              North Toronto West,  Lawrence Park
             </td>
            </tr>
            <tr>
             <td>
              M5R
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              The Annex, North Midtown, Yorkville
             </td>
            </tr>
            <tr>
             <td>
              M6R
             </td>
             <td>
              West Toronto
             </td>
             <td>
              Parkdale, Roncesvalles
             </td>
            </tr>
            <tr>
             <td>
              M7R
             </td>
             <td>
              Mississauga
             </td>
             <td>
              Canada Post Gateway Processing Centre
             </td>
            </tr>
            <tr>
             <td>
              M8R
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9R
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              Kingsview Village, St. Phillips, Martin Grove Gardens, Richview Gardens
             </td>
            </tr>
            <tr>
             <td>
              M1S
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Agincourt
             </td>
            </tr>
            <tr>
             <td>
              M2S
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3S
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4S
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              Davisville
             </td>
            </tr>
            <tr>
             <td>
              M5S
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              University of Toronto, Harbord
             </td>
            </tr>
            <tr>
             <td>
              M6S
             </td>
             <td>
              West Toronto
             </td>
             <td>
              Runnymede, Swansea
             </td>
            </tr>
            <tr>
             <td>
              M7S
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8S
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9S
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1T
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Clarks Corners, Tam O'Shanter, Sullivan
             </td>
            </tr>
            <tr>
             <td>
              M2T
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3T
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4T
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              Moore Park, Summerhill East
             </td>
            </tr>
            <tr>
             <td>
              M5T
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Kensington Market, Chinatown, Grange Park
             </td>
            </tr>
            <tr>
             <td>
              M6T
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M7T
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8T
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M9T
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1V
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Milliken, Agincourt North, Steeles East, L'Amoreaux East
             </td>
            </tr>
            <tr>
             <td>
              M2V
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3V
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4V
             </td>
             <td>
              Central Toronto
             </td>
             <td>
              Summerhill West, Rathnelly, South Hill, Forest Hill SE, Deer Park
             </td>
            </tr>
            <tr>
             <td>
              M5V
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              CN Tower, King and Spadina, Railway Lands, Harbourfront West, Bathurst Quay, South Niagara, Island airport
             </td>
            </tr>
            <tr>
             <td>
              M6V
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M7V
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8V
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              New Toronto, Mimico South, Humber Bay Shores
             </td>
            </tr>
            <tr>
             <td>
              M9V
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              South Steeles, Silverstone, Humbergate, Jamestown, Mount Olive, Beaumond Heights, Thistletown, Albion Gardens
             </td>
            </tr>
            <tr>
             <td>
              M1W
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Steeles West, L'Amoreaux West
             </td>
            </tr>
            <tr>
             <td>
              M2W
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3W
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4W
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Rosedale
             </td>
            </tr>
            <tr>
             <td>
              M5W
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Stn A PO Boxes
             </td>
            </tr>
            <tr>
             <td>
              M6W
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M7W
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8W
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              Alderwood, Long Branch
             </td>
            </tr>
            <tr>
             <td>
              M9W
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              Northwest, West Humber - Clairville
             </td>
            </tr>
            <tr>
             <td>
              M1X
             </td>
             <td>
              Scarborough
             </td>
             <td>
              Upper Rouge
             </td>
            </tr>
            <tr>
             <td>
              M2X
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3X
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4X
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              St. James Town, Cabbagetown
             </td>
            </tr>
            <tr>
             <td>
              M5X
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              First Canadian Place, Underground city
             </td>
            </tr>
            <tr>
             <td>
              M6X
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M7X
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8X
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              The Kingsway, Montgomery Road, Old Mill North
             </td>
            </tr>
            <tr>
             <td>
              M9X
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1Y
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M2Y
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3Y
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4Y
             </td>
             <td>
              Downtown Toronto
             </td>
             <td>
              Church and Wellesley
             </td>
            </tr>
            <tr>
             <td>
              M5Y
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M6Y
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M7Y
             </td>
             <td>
              East Toronto
             </td>
             <td>
              Business reply mail Processing Centre, South Central Letter Processing Plant Toronto
             </td>
            </tr>
            <tr>
             <td>
              M8Y
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              Old Mill South, King's Mill Park, Sunnylea, Humber Bay, Mimico NE, The Queensway East, Royal York South East, Kingsway Park South East
             </td>
            </tr>
            <tr>
             <td>
              M9Y
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M1Z
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M2Z
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M3Z
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M4Z
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M5Z
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M6Z
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M7Z
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
            <tr>
             <td>
              M8Z
             </td>
             <td>
              Etobicoke
             </td>
             <td>
              Mimico NW, The Queensway West, South of Bloor, Kingsway Park South West, Royal York South West
             </td>
            </tr>
            <tr>
             <td>
              M9Z
             </td>
             <td>
              Not assigned
             </td>
             <td>
              Not assigned
             </td>
            </tr>
           </tbody>
          </table>
          <h2>
           <span id="Most_populated_FSAs.5B3.5D">
           </span>
           <span class="mw-headline" id="Most_populated_FSAs[3]">
            Most populated FSAs
            <sup class="reference" id="cite_ref-statcan_3-0">
             <a href="#cite_note-statcan-3">
              [3]
             </a>
            </sup>
           </span>
           <span class="mw-editsection">
            <span class="mw-editsection-bracket">
             [
            </span>
            <a href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=edit&amp;section=2" title="Edit section: Most populated FSAs[3]">
             edit
            </a>
            <span class="mw-editsection-bracket">
             ]
            </span>
           </span>
          </h2>
          <ol>
           <li>
            M1B, 65,129
           </li>
           <li>
            M2N, 60,124
           </li>
           <li>
            M1V, 55,250
           </li>
           <li>
            M9V, 55,159
           </li>
           <li>
            M2J, 54,391
           </li>
          </ol>
          <h2>
           <span id="Least_populated_FSAs.5B3.5D">
           </span>
           <span class="mw-headline" id="Least_populated_FSAs[3]">
            Least populated FSAs
            <sup class="reference" id="cite_ref-statcan_3-1">
             <a href="#cite_note-statcan-3">
              [3]
             </a>
            </sup>
           </span>
           <span class="mw-editsection">
            <span class="mw-editsection-bracket">
             [
            </span>
            <a href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=edit&amp;section=3" title="Edit section: Least populated FSAs[3]">
             edit
            </a>
            <span class="mw-editsection-bracket">
             ]
            </span>
           </span>
          </h2>
          <ol>
           <li>
            M5K, 5
           </li>
           <li>
            M5L, 5
           </li>
           <li>
            M5W, 5
           </li>
           <li>
            M5X, 5
           </li>
           <li>
            M7A, 5
           </li>
          </ol>
          <h2>
           <span class="mw-headline" id="References">
            References
           </span>
           <span class="mw-editsection">
            <span class="mw-editsection-bracket">
             [
            </span>
            <a href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=edit&amp;section=4" title="Edit section: References">
             edit
            </a>
            <span class="mw-editsection-bracket">
             ]
            </span>
           </span>
          </h2>
          <div class="mw-references-wrap">
           <ol class="references">
            <li id="cite_note-1">
             <span class="mw-cite-backlink">
              <b>
               <a href="#cite_ref-1">
                ^
               </a>
              </b>
             </span>
             <span class="reference-text">
              <cite class="citation web cs1" id="CITEREFCanada_Post">
               Canada Post.
               <a class="external text" href="https://www.canadapost.ca/cpotools/apps/fpc/personal/findByCity?execution=e2s1" rel="nofollow">
                "Canada Post - Find a Postal Code"
               </a>
               <span class="reference-accessdate">
                . Retrieved
                <span class="nowrap">
                 9 November
                </span>
                2008
               </span>
               .
              </cite>
              <span class="Z3988" title="ctx_ver=Z39.88-2004&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Abook&amp;rft.genre=unknown&amp;rft.btitle=Canada+Post+-+Find+a+Postal+Code&amp;rft.au=Canada+Post&amp;rft_id=https%3A%2F%2Fwww.canadapost.ca%2Fcpotools%2Fapps%2Ffpc%2Fpersonal%2FfindByCity%3Fexecution%3De2s1&amp;rfr_id=info%3Asid%2Fen.wikipedia.org%3AList+of+postal+codes+of+Canada%3A+M">
              </span>
              <style data-mw-deduplicate="TemplateStyles:r982806391">
               .mw-parser-output cite.citation{font-style:inherit}.mw-parser-output .citation q{quotes:"\"""\"""'""'"}.mw-parser-output .id-lock-free a,.mw-parser-output .citation .cs1-lock-free a{background:linear-gradient(transparent,transparent),url("//upload.wikimedia.org/wikipedia/commons/6/65/Lock-green.svg")right 0.1em center/9px no-repeat}.mw-parser-output .id-lock-limited a,.mw-parser-output .id-lock-registration a,.mw-parser-output .citation .cs1-lock-limited a,.mw-parser-output .citation .cs1-lock-registration a{background:linear-gradient(transparent,transparent),url("//upload.wikimedia.org/wikipedia/commons/d/d6/Lock-gray-alt-2.svg")right 0.1em center/9px no-repeat}.mw-parser-output .id-lock-subscription a,.mw-parser-output .citation .cs1-lock-subscription a{background:linear-gradient(transparent,transparent),url("//upload.wikimedia.org/wikipedia/commons/a/aa/Lock-red-alt-2.svg")right 0.1em center/9px no-repeat}.mw-parser-output .cs1-subscription,.mw-parser-output .cs1-registration{color:#555}.mw-parser-output .cs1-subscription span,.mw-parser-output .cs1-registration span{border-bottom:1px dotted;cursor:help}.mw-parser-output .cs1-ws-icon a{background:linear-gradient(transparent,transparent),url("//upload.wikimedia.org/wikipedia/commons/4/4c/Wikisource-logo.svg")right 0.1em center/12px no-repeat}.mw-parser-output code.cs1-code{color:inherit;background:inherit;border:none;padding:inherit}.mw-parser-output .cs1-hidden-error{display:none;font-size:100%}.mw-parser-output .cs1-visible-error{font-size:100%}.mw-parser-output .cs1-maint{display:none;color:#33aa33;margin-left:0.3em}.mw-parser-output .cs1-subscription,.mw-parser-output .cs1-registration,.mw-parser-output .cs1-format{font-size:95%}.mw-parser-output .cs1-kern-left,.mw-parser-output .cs1-kern-wl-left{padding-left:0.2em}.mw-parser-output .cs1-kern-right,.mw-parser-output .cs1-kern-wl-right{padding-right:0.2em}.mw-parser-output .citation .mw-selflink{font-weight:inherit}
              </style>
             </span>
            </li>
            <li id="cite_note-2">
             <span class="mw-cite-backlink">
              <b>
               <a href="#cite_ref-2">
                ^
               </a>
              </b>
             </span>
             <span class="reference-text">
              <cite class="citation web cs1">
               <a class="external text" href="https://web.archive.org/web/20110519093024/http://www.canadapost.ca/cpo/mc/personal/tools/mobileapp/default.jsf" rel="nofollow">
                "Mobile Apps"
               </a>
               . Canada Post. Archived from
               <a class="external text" href="http://www.canadapost.ca/cpo/mc/personal/tools/mobileapp/default.jsf" rel="nofollow">
                the original
               </a>
               on 2011-05-19.
              </cite>
              <span class="Z3988" title="ctx_ver=Z39.88-2004&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Abook&amp;rft.genre=unknown&amp;rft.btitle=Mobile+Apps&amp;rft.pub=Canada+Post&amp;rft_id=http%3A%2F%2Fwww.canadapost.ca%2Fcpo%2Fmc%2Fpersonal%2Ftools%2Fmobileapp%2Fdefault.jsf&amp;rfr_id=info%3Asid%2Fen.wikipedia.org%3AList+of+postal+codes+of+Canada%3A+M">
              </span>
              <link href="mw-data:TemplateStyles:r982806391" rel="mw-deduplicated-inline-style"/>
             </span>
            </li>
            <li id="cite_note-statcan-3">
             <span class="mw-cite-backlink">
              ^
              <a href="#cite_ref-statcan_3-0">
               <sup>
                <i>
                 <b>
                  a
                 </b>
                </i>
               </sup>
              </a>
              <a href="#cite_ref-statcan_3-1">
               <sup>
                <i>
                 <b>
                  b
                 </b>
                </i>
               </sup>
              </a>
             </span>
             <span class="reference-text">
              <cite class="citation web cs1">
               <a class="external text" href="http://www12.statcan.ca/english/census06/data/popdwell/Table.cfm?T=1201&amp;SR=1&amp;S=0&amp;O=A&amp;RPP=9999&amp;PR=0&amp;CMA=0" rel="nofollow">
                "2006 Census of Population"
               </a>
               . 15 October 2008.
              </cite>
              <span class="Z3988" title="ctx_ver=Z39.88-2004&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Abook&amp;rft.genre=unknown&amp;rft.btitle=2006+Census+of+Population&amp;rft.date=2008-10-15&amp;rft_id=http%3A%2F%2Fwww12.statcan.ca%2Fenglish%2Fcensus06%2Fdata%2Fpopdwell%2FTable.cfm%3FT%3D1201%26SR%3D1%26S%3D0%26O%3DA%26RPP%3D9999%26PR%3D0%26CMA%3D0&amp;rfr_id=info%3Asid%2Fen.wikipedia.org%3AList+of+postal+codes+of+Canada%3A+M">
              </span>
              <link href="mw-data:TemplateStyles:r982806391" rel="mw-deduplicated-inline-style"/>
             </span>
            </li>
           </ol>
          </div>
          <table class="navbox">
           <tbody>
            <tr>
             <td style="width:36px; text-align:center">
              <a class="image" href="/wiki/File:Flag_of_Canada.svg" title="Flag of Canada">
               <img alt="Flag of Canada" data-file-height="600" data-file-width="1200" decoding="async" height="18" src="//upload.wikimedia.org/wikipedia/en/thumb/c/cf/Flag_of_Canada.svg/36px-Flag_of_Canada.svg.png" srcset="//upload.wikimedia.org/wikipedia/en/thumb/c/cf/Flag_of_Canada.svg/54px-Flag_of_Canada.svg.png 1.5x, //upload.wikimedia.org/wikipedia/en/thumb/c/cf/Flag_of_Canada.svg/72px-Flag_of_Canada.svg.png 2x" width="36"/>
              </a>
             </td>
             <th class="navbox-title" style="font-size:110%">
              <a href="/wiki/Postal_codes_in_Canada" title="Postal codes in Canada">
               Canadian postal codes
              </a>
             </th>
             <td style="width:36px; text-align:center">
              <a class="image" href="/wiki/File:Canadian_postal_district_map_(without_legends).svg">
               <img alt="Canadian postal district map (without legends).svg" data-file-height="846" data-file-width="1000" decoding="async" height="18" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Canadian_postal_district_map_%28without_legends%29.svg/21px-Canadian_postal_district_map_%28without_legends%29.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Canadian_postal_district_map_%28without_legends%29.svg/32px-Canadian_postal_district_map_%28without_legends%29.svg.png 1.5x, //upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Canadian_postal_district_map_%28without_legends%29.svg/43px-Canadian_postal_district_map_%28without_legends%29.svg.png 2x" width="21"/>
              </a>
             </td>
            </tr>
            <tr>
             <td colspan="3" style="text-align:center; font-size: 100%;">
              <table cellspacing="0" style="background-color: #F8F8F8;" width="100%">
               <tbody>
                <tr>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Newfoundland_and_Labrador" title="Newfoundland and Labrador">
                   NL
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Nova_Scotia" title="Nova Scotia">
                   NS
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Prince_Edward_Island" title="Prince Edward Island">
                   PE
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/New_Brunswick" title="New Brunswick">
                   NB
                  </a>
                 </td>
                 <td colspan="3" style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Quebec" title="Quebec">
                   QC
                  </a>
                 </td>
                 <td colspan="5" style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Ontario" title="Ontario">
                   ON
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Manitoba" title="Manitoba">
                   MB
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Saskatchewan" title="Saskatchewan">
                   SK
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Alberta" title="Alberta">
                   AB
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/British_Columbia" title="British Columbia">
                   BC
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Nunavut" title="Nunavut">
                   NU
                  </a>
                  /
                  <a href="/wiki/Northwest_Territories" title="Northwest Territories">
                   NT
                  </a>
                 </td>
                 <td style="text-align:center; border:1px solid #aaa;">
                  <a href="/wiki/Yukon" title="Yukon">
                   YT
                  </a>
                 </td>
                </tr>
                <tr>
                 <td align="center" style="border: 1px solid #FF0000; background-color: #FFE0E0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_A" title="List of postal codes of Canada: A">
                   A
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #FF4000; background-color: #FFE8E0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_B" title="List of postal codes of Canada: B">
                   B
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #FF8000; background-color: #FFF0E0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_C" title="List of postal codes of Canada: C">
                   C
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #FFC000; background-color: #FFF8E0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_E" title="List of postal codes of Canada: E">
                   E
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #FFFF00; background-color: #FFFFE0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_G" title="List of postal codes of Canada: G">
                   G
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #C0FF00; background-color: #F8FFE0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_H" title="List of postal codes of Canada: H">
                   H
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #80FF00; background-color: #F0FFE0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_J" title="List of postal codes of Canada: J">
                   J
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #00FF00; background-color: #E0FFE0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_K" title="List of postal codes of Canada: K">
                   K
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #00FF80; background-color: #E0FFF0; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_L" title="List of postal codes of Canada: L">
                   L
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #E0FFF8; background-color: #00FFC0; font-size: 135%; color: black;" width="5%">
                  <a class="mw-selflink selflink">
                   M
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #00FFE0; background-color: #E0FFFC; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_N" title="List of postal codes of Canada: N">
                   N
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #00FFFF; background-color: #E0FFFF; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_P" title="List of postal codes of Canada: P">
                   P
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #00C0FF; background-color: #E0F8FF; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_R" title="List of postal codes of Canada: R">
                   R
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #0080FF; background-color: #E0F0FF; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_S" title="List of postal codes of Canada: S">
                   S
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #0040FF; background-color: #E0E8FF; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_T" title="List of postal codes of Canada: T">
                   T
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #0000FF; background-color: #E0E0FF; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_V" title="List of postal codes of Canada: V">
                   V
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #A000FF; background-color: #E8E0FF; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_X" title="List of postal codes of Canada: X">
                   X
                  </a>
                 </td>
                 <td align="center" style="border: 1px solid #FF00FF; background-color: #FFE0FF; font-size: 135%;" width="5%">
                  <a href="/wiki/List_of_postal_codes_of_Canada:_Y" title="List of postal codes of Canada: Y">
                   Y
                  </a>
                 </td>
                </tr>
               </tbody>
              </table>
             </td>
            </tr>
           </tbody>
          </table>
          <!-- 
    NewPP limit report
    Parsed by mw1411
    Cached time: 20201206200326
    Cache expiry: 2592000
    Dynamic content: false
    Complications: [vary‐revision‐sha1]
    CPU time usage: 0.196 seconds
    Real time usage: 0.264 seconds
    Preprocessor visited node count: 281/1000000
    Post‐expand include size: 10828/2097152 bytes
    Template argument size: 275/2097152 bytes
    Highest expansion depth: 8/40
    Expensive parser function count: 0/500
    Unstrip recursion depth: 1/20
    Unstrip post‐expand size: 9622/5000000 bytes
    Lua time usage: 0.105/10.000 seconds
    Lua memory usage: 3007528/52428800 bytes
    Number of Wikibase entities loaded: 0/400
    -->
          <!--
    Transclusion expansion time report (%,ms,calls,template)
    100.00%  206.854      1 -total
     55.27%  114.327      3 Template:Cite_web
     37.30%   77.148      1 Template:Short_description
     21.01%   43.458      1 Template:Pagetype
      9.36%   19.361      2 Template:Main_other
      7.34%   15.185      1 Template:SDcat
      2.72%    5.622      1 Template:Canadian_postal_codes
    -->
          <!-- Saved in parser cache with key enwiki:pcache:idhash:539066-0!canonical and timestamp 20201206200326 and revision id 979555370. Serialized with JSON.
     -->
         </div>
         <noscript>
          <img alt="" height="1" src="//en.wikipedia.org/wiki/Special:CentralAutoLogin/start?type=1x1" style="border: none; position: absolute;" title="" width="1"/>
         </noscript>
         <div class="printfooter">
          Retrieved from "
          <a dir="ltr" href="https://en.wikipedia.org/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;oldid=979555370">
           https://en.wikipedia.org/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;oldid=979555370
          </a>
          "
         </div>
        </div>
        <div class="catlinks" data-mw="interface" id="catlinks">
         <div class="mw-normal-catlinks" id="mw-normal-catlinks">
          <a href="/wiki/Help:Category" title="Help:Category">
           Categories
          </a>
          :
          <ul>
           <li>
            <a href="/wiki/Category:Communications_in_Ontario" title="Category:Communications in Ontario">
             Communications in Ontario
            </a>
           </li>
           <li>
            <a href="/wiki/Category:Postal_codes_in_Canada" title="Category:Postal codes in Canada">
             Postal codes in Canada
            </a>
           </li>
           <li>
            <a href="/wiki/Category:Toronto" title="Category:Toronto">
             Toronto
            </a>
           </li>
           <li>
            <a href="/wiki/Category:Ontario-related_lists" title="Category:Ontario-related lists">
             Ontario-related lists
            </a>
           </li>
          </ul>
         </div>
         <div class="mw-hidden-catlinks mw-hidden-cats-hidden" id="mw-hidden-catlinks">
          Hidden categories:
          <ul>
           <li>
            <a href="/wiki/Category:Articles_with_short_description" title="Category:Articles with short description">
             Articles with short description
            </a>
           </li>
           <li>
            <a href="/wiki/Category:Short_description_is_different_from_Wikidata" title="Category:Short description is different from Wikidata">
             Short description is different from Wikidata
            </a>
           </li>
          </ul>
         </div>
        </div>
       </div>
      </div>
      <div id="mw-data-after-content">
       <div class="read-more-container">
       </div>
      </div>
      <div id="mw-navigation">
       <h2>
        Navigation menu
       </h2>
       <div id="mw-head">
        <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
        <nav aria-labelledby="p-personal-label" class="mw-portlet mw-portlet-personal vector-menu" id="p-personal" role="navigation">
         <h3 id="p-personal-label">
          <span>
           Personal tools
          </span>
         </h3>
         <div class="vector-menu-content">
          <ul class="vector-menu-content-list">
           <li id="pt-anonuserpage">
            Not logged in
           </li>
           <li id="pt-anontalk">
            <a accesskey="n" href="/wiki/Special:MyTalk" title="Discussion about edits from this IP address [n]">
             Talk
            </a>
           </li>
           <li id="pt-anoncontribs">
            <a accesskey="y" href="/wiki/Special:MyContributions" title="A list of edits made from this IP address [y]">
             Contributions
            </a>
           </li>
           <li id="pt-createaccount">
            <a href="/w/index.php?title=Special:CreateAccount&amp;returnto=List+of+postal+codes+of+Canada%3A+M" title="You are encouraged to create an account and log in; however, it is not mandatory">
             Create account
            </a>
           </li>
           <li id="pt-login">
            <a accesskey="o" href="/w/index.php?title=Special:UserLogin&amp;returnto=List+of+postal+codes+of+Canada%3A+M" title="You're encouraged to log in; however, it's not mandatory. [o]">
             Log in
            </a>
           </li>
          </ul>
         </div>
        </nav>
        <div id="left-navigation">
         <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
         <nav aria-labelledby="p-namespaces-label" class="mw-portlet mw-portlet-namespaces vector-menu vector-menu-tabs" id="p-namespaces" role="navigation">
          <h3 id="p-namespaces-label">
           <span>
            Namespaces
           </span>
          </h3>
          <div class="vector-menu-content">
           <ul class="vector-menu-content-list">
            <li class="selected" id="ca-nstab-main">
             <a accesskey="c" href="/wiki/List_of_postal_codes_of_Canada:_M" title="View the content page [c]">
              Article
             </a>
            </li>
            <li id="ca-talk">
             <a accesskey="t" href="/wiki/Talk:List_of_postal_codes_of_Canada:_M" rel="discussion" title="Discuss improvements to the content page [t]">
              Talk
             </a>
            </li>
           </ul>
          </div>
         </nav>
         <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
         <nav aria-labelledby="p-variants-label" class="mw-portlet mw-portlet-variants emptyPortlet vector-menu vector-menu-dropdown" id="p-variants" role="navigation">
          <input aria-labelledby="p-variants-label" class="vector-menu-checkbox" type="checkbox"/>
          <h3 id="p-variants-label">
           <span>
            Variants
           </span>
          </h3>
          <div class="vector-menu-content">
           <ul class="vector-menu-content-list">
           </ul>
          </div>
         </nav>
        </div>
        <div id="right-navigation">
         <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
         <nav aria-labelledby="p-views-label" class="mw-portlet mw-portlet-views vector-menu vector-menu-tabs" id="p-views" role="navigation">
          <h3 id="p-views-label">
           <span>
            Views
           </span>
          </h3>
          <div class="vector-menu-content">
           <ul class="vector-menu-content-list">
            <li class="selected" id="ca-view">
             <a href="/wiki/List_of_postal_codes_of_Canada:_M">
              Read
             </a>
            </li>
            <li id="ca-edit">
             <a accesskey="e" href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=edit" title="Edit this page [e]">
              Edit
             </a>
            </li>
            <li id="ca-history">
             <a accesskey="h" href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=history" title="Past revisions of this page [h]">
              View history
             </a>
            </li>
           </ul>
          </div>
         </nav>
         <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
         <nav aria-labelledby="p-cactions-label" class="mw-portlet mw-portlet-cactions emptyPortlet vector-menu vector-menu-dropdown" id="p-cactions" role="navigation">
          <input aria-labelledby="p-cactions-label" class="vector-menu-checkbox" type="checkbox"/>
          <h3 id="p-cactions-label">
           <span>
            More
           </span>
          </h3>
          <div class="vector-menu-content">
           <ul class="vector-menu-content-list">
           </ul>
          </div>
         </nav>
         <div id="p-search" role="search">
          <h3>
           <label for="searchInput">
            Search
           </label>
          </h3>
          <form action="/w/index.php" id="searchform">
           <div data-search-loc="header-navigation" id="simpleSearch">
            <input accesskey="f" autocapitalize="sentences" id="searchInput" name="search" placeholder="Search Wikipedia" title="Search Wikipedia [f]" type="search"/>
            <input name="title" type="hidden" value="Special:Search"/>
            <input class="searchButton mw-fallbackSearchButton" id="mw-searchButton" name="fulltext" title="Search Wikipedia for this text" type="submit" value="Search"/>
            <input class="searchButton" id="searchButton" name="go" title="Go to a page with this exact name if it exists" type="submit" value="Go"/>
           </div>
          </form>
         </div>
        </div>
       </div>
       <div id="mw-panel">
        <div id="p-logo" role="banner">
         <a class="mw-wiki-logo" href="/wiki/Main_Page" title="Visit the main page">
         </a>
        </div>
        <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
        <nav aria-labelledby="p-navigation-label" class="mw-portlet mw-portlet-navigation vector-menu vector-menu-portal portal portal-first" id="p-navigation" role="navigation">
         <h3 id="p-navigation-label">
          <span>
           Navigation
          </span>
         </h3>
         <div class="vector-menu-content">
          <ul class="vector-menu-content-list">
           <li id="n-mainpage-description">
            <a accesskey="z" href="/wiki/Main_Page" title="Visit the main page [z]">
             Main page
            </a>
           </li>
           <li id="n-contents">
            <a href="/wiki/Wikipedia:Contents" title="Guides to browsing Wikipedia">
             Contents
            </a>
           </li>
           <li id="n-currentevents">
            <a href="/wiki/Portal:Current_events" title="Articles related to current events">
             Current events
            </a>
           </li>
           <li id="n-randompage">
            <a accesskey="x" href="/wiki/Special:Random" title="Visit a randomly selected article [x]">
             Random article
            </a>
           </li>
           <li id="n-aboutsite">
            <a href="/wiki/Wikipedia:About" title="Learn about Wikipedia and how it works">
             About Wikipedia
            </a>
           </li>
           <li id="n-contactpage">
            <a href="//en.wikipedia.org/wiki/Wikipedia:Contact_us" title="How to contact Wikipedia">
             Contact us
            </a>
           </li>
           <li id="n-sitesupport">
            <a href="https://donate.wikimedia.org/wiki/Special:FundraiserRedirector?utm_source=donate&amp;utm_medium=sidebar&amp;utm_campaign=C13_en.wikipedia.org&amp;uselang=en" title="Support us by donating to the Wikimedia Foundation">
             Donate
            </a>
           </li>
          </ul>
         </div>
        </nav>
        <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
        <nav aria-labelledby="p-interaction-label" class="mw-portlet mw-portlet-interaction vector-menu vector-menu-portal portal" id="p-interaction" role="navigation">
         <h3 id="p-interaction-label">
          <span>
           Contribute
          </span>
         </h3>
         <div class="vector-menu-content">
          <ul class="vector-menu-content-list">
           <li id="n-help">
            <a href="/wiki/Help:Contents" title="Guidance on how to use and edit Wikipedia">
             Help
            </a>
           </li>
           <li id="n-introduction">
            <a href="/wiki/Help:Introduction" title="Learn how to edit Wikipedia">
             Learn to edit
            </a>
           </li>
           <li id="n-portal">
            <a href="/wiki/Wikipedia:Community_portal" title="The hub for editors">
             Community portal
            </a>
           </li>
           <li id="n-recentchanges">
            <a accesskey="r" href="/wiki/Special:RecentChanges" title="A list of recent changes to Wikipedia [r]">
             Recent changes
            </a>
           </li>
           <li id="n-upload">
            <a href="/wiki/Wikipedia:File_Upload_Wizard" title="Add images or other media for use on Wikipedia">
             Upload file
            </a>
           </li>
          </ul>
         </div>
        </nav>
        <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
        <nav aria-labelledby="p-tb-label" class="mw-portlet mw-portlet-tb vector-menu vector-menu-portal portal" id="p-tb" role="navigation">
         <h3 id="p-tb-label">
          <span>
           Tools
          </span>
         </h3>
         <div class="vector-menu-content">
          <ul class="vector-menu-content-list">
           <li id="t-whatlinkshere">
            <a accesskey="j" href="/wiki/Special:WhatLinksHere/List_of_postal_codes_of_Canada:_M" title="List of all English Wikipedia pages containing links to this page [j]">
             What links here
            </a>
           </li>
           <li id="t-recentchangeslinked">
            <a accesskey="k" href="/wiki/Special:RecentChangesLinked/List_of_postal_codes_of_Canada:_M" rel="nofollow" title="Recent changes in pages linked from this page [k]">
             Related changes
            </a>
           </li>
           <li id="t-upload">
            <a accesskey="u" href="/wiki/Wikipedia:File_Upload_Wizard" title="Upload files [u]">
             Upload file
            </a>
           </li>
           <li id="t-specialpages">
            <a accesskey="q" href="/wiki/Special:SpecialPages" title="A list of all special pages [q]">
             Special pages
            </a>
           </li>
           <li id="t-permalink">
            <a href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;oldid=979555370" title="Permanent link to this revision of this page">
             Permanent link
            </a>
           </li>
           <li id="t-info">
            <a href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;action=info" title="More information about this page">
             Page information
            </a>
           </li>
           <li id="t-cite">
            <a href="/w/index.php?title=Special:CiteThisPage&amp;page=List_of_postal_codes_of_Canada%3A_M&amp;id=979555370&amp;wpFormIdentifier=titleform" title="Information on how to cite this page">
             Cite this page
            </a>
           </li>
           <li id="t-wikibase">
            <a accesskey="g" href="https://www.wikidata.org/wiki/Special:EntityPage/Q3248240" title="Structured data on this page hosted by Wikidata [g]">
             Wikidata item
            </a>
           </li>
          </ul>
         </div>
        </nav>
        <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
        <nav aria-labelledby="p-coll-print_export-label" class="mw-portlet mw-portlet-coll-print_export vector-menu vector-menu-portal portal" id="p-coll-print_export" role="navigation">
         <h3 id="p-coll-print_export-label">
          <span>
           Print/export
          </span>
         </h3>
         <div class="vector-menu-content">
          <ul class="vector-menu-content-list">
           <li id="coll-download-as-rl">
            <a href="/w/index.php?title=Special:DownloadAsPdf&amp;page=List_of_postal_codes_of_Canada%3A_M&amp;action=show-download-screen" title="Download this page as a PDF file">
             Download as PDF
            </a>
           </li>
           <li id="t-print">
            <a accesskey="p" href="/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;printable=yes" title="Printable version of this page [p]">
             Printable version
            </a>
           </li>
          </ul>
         </div>
        </nav>
        <!-- Please do not use role attribute as CSS selector, it is deprecated. -->
        <nav aria-labelledby="p-lang-label" class="mw-portlet mw-portlet-lang vector-menu vector-menu-portal portal" id="p-lang" role="navigation">
         <h3 id="p-lang-label">
          <span>
           Languages
          </span>
         </h3>
         <div class="vector-menu-content">
          <ul class="vector-menu-content-list">
           <li class="interlanguage-link interwiki-fr">
            <a class="interlanguage-link-target" href="https://fr.wikipedia.org/wiki/Liste_des_codes_postaux_canadiens_d%C3%A9butant_par_M" hreflang="fr" lang="fr" title="Liste des codes postaux canadiens débutant par M – French">
             Français
            </a>
           </li>
          </ul>
          <div class="after-portlet after-portlet-lang">
           <span class="wb-langlinks-edit wb-langlinks-link">
            <a class="wbc-editpage" href="https://www.wikidata.org/wiki/Special:EntityPage/Q3248240#sitelinks-wikipedia" title="Edit interlanguage links">
             Edit links
            </a>
           </span>
          </div>
         </div>
        </nav>
       </div>
      </div>
      <footer class="mw-footer" id="footer" role="contentinfo">
       <ul id="footer-info">
        <li id="footer-info-lastmod">
         This page was last edited on 21 September 2020, at 11:54
         <span class="anonymous-show">
          (UTC)
         </span>
         .
        </li>
        <li id="footer-info-copyright">
         Text is available under the
         <a href="//en.wikipedia.org/wiki/Wikipedia:Text_of_Creative_Commons_Attribution-ShareAlike_3.0_Unported_License" rel="license">
          Creative Commons Attribution-ShareAlike License
         </a>
         <a href="//creativecommons.org/licenses/by-sa/3.0/" rel="license" style="display:none;">
         </a>
         ;
    additional terms may apply.  By using this site, you agree to the
         <a href="//foundation.wikimedia.org/wiki/Terms_of_Use">
          Terms of Use
         </a>
         and
         <a href="//foundation.wikimedia.org/wiki/Privacy_policy">
          Privacy Policy
         </a>
         . Wikipedia® is a registered trademark of the
         <a href="//www.wikimediafoundation.org/">
          Wikimedia Foundation, Inc.
         </a>
         , a non-profit organization.
        </li>
       </ul>
       <ul id="footer-places">
        <li id="footer-places-privacy">
         <a class="extiw" href="https://foundation.wikimedia.org/wiki/Privacy_policy" title="wmf:Privacy policy">
          Privacy policy
         </a>
        </li>
        <li id="footer-places-about">
         <a href="/wiki/Wikipedia:About" title="Wikipedia:About">
          About Wikipedia
         </a>
        </li>
        <li id="footer-places-disclaimer">
         <a href="/wiki/Wikipedia:General_disclaimer" title="Wikipedia:General disclaimer">
          Disclaimers
         </a>
        </li>
        <li id="footer-places-contact">
         <a href="//en.wikipedia.org/wiki/Wikipedia:Contact_us">
          Contact Wikipedia
         </a>
        </li>
        <li id="footer-places-mobileview">
         <a class="noprint stopMobileRedirectToggle" href="//en.m.wikipedia.org/w/index.php?title=List_of_postal_codes_of_Canada:_M&amp;mobileaction=toggle_view_mobile">
          Mobile view
         </a>
        </li>
        <li id="footer-places-developers">
         <a href="https://www.mediawiki.org/wiki/Special:MyLanguage/How_to_contribute">
          Developers
         </a>
        </li>
        <li id="footer-places-statslink">
         <a href="https://stats.wikimedia.org/#/en.wikipedia.org">
          Statistics
         </a>
        </li>
        <li id="footer-places-cookiestatement">
         <a href="https://foundation.wikimedia.org/wiki/Cookie_statement">
          Cookie statement
         </a>
        </li>
       </ul>
       <ul class="noprint" id="footer-icons">
        <li id="footer-copyrightico">
         <a href="https://wikimediafoundation.org/">
          <img alt="Wikimedia Foundation" height="31" loading="lazy" src="/static/images/footer/wikimedia-button.png" srcset="/static/images/footer/wikimedia-button-1.5x.png 1.5x, /static/images/footer/wikimedia-button-2x.png 2x" width="88"/>
         </a>
        </li>
        <li id="footer-poweredbyico">
         <a href="https://www.mediawiki.org/">
          <img alt="Powered by MediaWiki" height="31" loading="lazy" src="/static/images/footer/poweredby_mediawiki_88x31.png" srcset="/static/images/footer/poweredby_mediawiki_132x47.png 1.5x, /static/images/footer/poweredby_mediawiki_176x62.png 2x" width="88"/>
         </a>
        </li>
       </ul>
       <div style="clear: both;">
       </div>
      </footer>
      <script>
       (RLQ=window.RLQ||[]).push(function(){mw.config.set({"wgPageParseReport":{"limitreport":{"cputime":"0.196","walltime":"0.264","ppvisitednodes":{"value":281,"limit":1000000},"postexpandincludesize":{"value":10828,"limit":2097152},"templateargumentsize":{"value":275,"limit":2097152},"expansiondepth":{"value":8,"limit":40},"expensivefunctioncount":{"value":0,"limit":500},"unstrip-depth":{"value":1,"limit":20},"unstrip-size":{"value":9622,"limit":5000000},"entityaccesscount":{"value":0,"limit":400},"timingprofile":["100.00%  206.854      1 -total"," 55.27%  114.327      3 Template:Cite_web"," 37.30%   77.148      1 Template:Short_description"," 21.01%   43.458      1 Template:Pagetype","  9.36%   19.361      2 Template:Main_other","  7.34%   15.185      1 Template:SDcat","  2.72%    5.622      1 Template:Canadian_postal_codes"]},"scribunto":{"limitreport-timeusage":{"value":"0.105","limit":"10.000"},"limitreport-memusage":{"value":3007528,"limit":52428800}},"cachereport":{"origin":"mw1411","timestamp":"20201206200326","ttl":2592000,"transientcontent":false}}});});
      </script>
      <script type="application/ld+json">
       {"@context":"https:\/\/schema.org","@type":"Article","name":"List of postal codes of Canada: M","url":"https:\/\/en.wikipedia.org\/wiki\/List_of_postal_codes_of_Canada:_M","sameAs":"http:\/\/www.wikidata.org\/entity\/Q3248240","mainEntity":"http:\/\/www.wikidata.org\/entity\/Q3248240","author":{"@type":"Organization","name":"Contributors to Wikimedia projects"},"publisher":{"@type":"Organization","name":"Wikimedia Foundation, Inc.","logo":{"@type":"ImageObject","url":"https:\/\/www.wikimedia.org\/static\/images\/wmf-hor-googpub.png"}},"datePublished":"2004-03-20T10:02:13Z","dateModified":"2020-09-21T11:54:47Z","headline":"Wikimedia list article"}
      </script>
      <script>
       (RLQ=window.RLQ||[]).push(function(){mw.config.set({"wgBackendResponseTime":157,"wgHostname":"mw1265"});});
      </script>
     </body>
    </html>



```
my_table = soup.find('table',{'class':'wikitable sortable'})
print(my_table)
```

    <table class="wikitable sortable">
    <tbody><tr>
    <th>Postal Code
    </th>
    <th>Borough
    </th>
    <th>Neighbourhood
    </th></tr>
    <tr>
    <td>M1A
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M2A
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3A
    </td>
    <td>North York
    </td>
    <td>Parkwoods
    </td></tr>
    <tr>
    <td>M4A
    </td>
    <td>North York
    </td>
    <td>Victoria Village
    </td></tr>
    <tr>
    <td>M5A
    </td>
    <td>Downtown Toronto
    </td>
    <td>Regent Park, Harbourfront
    </td></tr>
    <tr>
    <td>M6A
    </td>
    <td>North York
    </td>
    <td>Lawrence Manor, Lawrence Heights
    </td></tr>
    <tr>
    <td>M7A
    </td>
    <td>Downtown Toronto
    </td>
    <td>Queen's Park, Ontario Provincial Government
    </td></tr>
    <tr>
    <td>M8A
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9A
    </td>
    <td>Etobicoke
    </td>
    <td>Islington Avenue, Humber Valley Village
    </td></tr>
    <tr>
    <td>M1B
    </td>
    <td>Scarborough
    </td>
    <td>Malvern, Rouge
    </td></tr>
    <tr>
    <td>M2B
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3B
    </td>
    <td>North York
    </td>
    <td>Don Mills
    </td></tr>
    <tr>
    <td>M4B
    </td>
    <td>East York
    </td>
    <td>Parkview Hill, Woodbine Gardens
    </td></tr>
    <tr>
    <td>M5B
    </td>
    <td>Downtown Toronto
    </td>
    <td>Garden District, Ryerson
    </td></tr>
    <tr>
    <td>M6B
    </td>
    <td>North York
    </td>
    <td>Glencairn
    </td></tr>
    <tr>
    <td>M7B
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8B
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9B
    </td>
    <td>Etobicoke
    </td>
    <td>West Deane Park, Princess Gardens, Martin Grove, Islington, Cloverdale
    </td></tr>
    <tr>
    <td>M1C
    </td>
    <td>Scarborough
    </td>
    <td>Rouge Hill, Port Union, Highland Creek
    </td></tr>
    <tr>
    <td>M2C
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3C
    </td>
    <td>North York
    </td>
    <td>Don Mills
    </td></tr>
    <tr>
    <td>M4C
    </td>
    <td>East York
    </td>
    <td>Woodbine Heights
    </td></tr>
    <tr>
    <td>M5C
    </td>
    <td>Downtown Toronto
    </td>
    <td>St. James Town
    </td></tr>
    <tr>
    <td>M6C
    </td>
    <td>York
    </td>
    <td>Humewood-Cedarvale
    </td></tr>
    <tr>
    <td>M7C
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8C
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9C
    </td>
    <td>Etobicoke
    </td>
    <td>Eringate, Bloordale Gardens, Old Burnhamthorpe, Markland Wood
    </td></tr>
    <tr>
    <td>M1E
    </td>
    <td>Scarborough
    </td>
    <td>Guildwood, Morningside, West Hill
    </td></tr>
    <tr>
    <td>M2E
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3E
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4E
    </td>
    <td>East Toronto
    </td>
    <td>The Beaches
    </td></tr>
    <tr>
    <td>M5E
    </td>
    <td>Downtown Toronto
    </td>
    <td>Berczy Park
    </td></tr>
    <tr>
    <td>M6E
    </td>
    <td>York
    </td>
    <td>Caledonia-Fairbanks
    </td></tr>
    <tr>
    <td>M7E
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8E
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9E
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1G
    </td>
    <td>Scarborough
    </td>
    <td>Woburn
    </td></tr>
    <tr>
    <td>M2G
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3G
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4G
    </td>
    <td>East York
    </td>
    <td>Leaside
    </td></tr>
    <tr>
    <td>M5G
    </td>
    <td>Downtown Toronto
    </td>
    <td>Central Bay Street
    </td></tr>
    <tr>
    <td>M6G
    </td>
    <td>Downtown Toronto
    </td>
    <td>Christie
    </td></tr>
    <tr>
    <td>M7G
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8G
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9G
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1H
    </td>
    <td>Scarborough
    </td>
    <td>Cedarbrae
    </td></tr>
    <tr>
    <td>M2H
    </td>
    <td>North York
    </td>
    <td>Hillcrest Village
    </td></tr>
    <tr>
    <td>M3H
    </td>
    <td>North York
    </td>
    <td>Bathurst Manor, Wilson Heights, Downsview North
    </td></tr>
    <tr>
    <td>M4H
    </td>
    <td>East York
    </td>
    <td>Thorncliffe Park
    </td></tr>
    <tr>
    <td>M5H
    </td>
    <td>Downtown Toronto
    </td>
    <td>Richmond, Adelaide, King
    </td></tr>
    <tr>
    <td>M6H
    </td>
    <td>West Toronto
    </td>
    <td>Dufferin, Dovercourt Village
    </td></tr>
    <tr>
    <td>M7H
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8H
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9H
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1J
    </td>
    <td>Scarborough
    </td>
    <td>Scarborough Village
    </td></tr>
    <tr>
    <td>M2J
    </td>
    <td>North York
    </td>
    <td>Fairview, Henry Farm, Oriole
    </td></tr>
    <tr>
    <td>M3J
    </td>
    <td>North York
    </td>
    <td>Northwood Park, York University
    </td></tr>
    <tr>
    <td>M4J
    </td>
    <td>East York
    </td>
    <td>East Toronto, Broadview North (Old East York)
    </td></tr>
    <tr>
    <td>M5J
    </td>
    <td>Downtown Toronto
    </td>
    <td>Harbourfront East, Union Station, Toronto Islands
    </td></tr>
    <tr>
    <td>M6J
    </td>
    <td>West Toronto
    </td>
    <td>Little Portugal, Trinity
    </td></tr>
    <tr>
    <td>M7J
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8J
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9J
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1K
    </td>
    <td>Scarborough
    </td>
    <td>Kennedy Park, Ionview, East Birchmount Park
    </td></tr>
    <tr>
    <td>M2K
    </td>
    <td>North York
    </td>
    <td>Bayview Village
    </td></tr>
    <tr>
    <td>M3K
    </td>
    <td>North York
    </td>
    <td>Downsview
    </td></tr>
    <tr>
    <td>M4K
    </td>
    <td>East Toronto
    </td>
    <td>The Danforth West, Riverdale
    </td></tr>
    <tr>
    <td>M5K
    </td>
    <td>Downtown Toronto
    </td>
    <td>Toronto Dominion Centre, Design Exchange
    </td></tr>
    <tr>
    <td>M6K
    </td>
    <td>West Toronto
    </td>
    <td>Brockton, Parkdale Village, Exhibition Place
    </td></tr>
    <tr>
    <td>M7K
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8K
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9K
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1L
    </td>
    <td>Scarborough
    </td>
    <td>Golden Mile, Clairlea, Oakridge
    </td></tr>
    <tr>
    <td>M2L
    </td>
    <td>North York
    </td>
    <td>York Mills, Silver Hills
    </td></tr>
    <tr>
    <td>M3L
    </td>
    <td>North York
    </td>
    <td>Downsview
    </td></tr>
    <tr>
    <td>M4L
    </td>
    <td>East Toronto
    </td>
    <td>India Bazaar, The Beaches West
    </td></tr>
    <tr>
    <td>M5L
    </td>
    <td>Downtown Toronto
    </td>
    <td>Commerce Court, Victoria Hotel
    </td></tr>
    <tr>
    <td>M6L
    </td>
    <td>North York
    </td>
    <td>North Park, Maple Leaf Park, Upwood Park
    </td></tr>
    <tr>
    <td>M7L
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8L
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9L
    </td>
    <td>North York
    </td>
    <td>Humber Summit
    </td></tr>
    <tr>
    <td>M1M
    </td>
    <td>Scarborough
    </td>
    <td>Cliffside, Cliffcrest, Scarborough Village West
    </td></tr>
    <tr>
    <td>M2M
    </td>
    <td>North York
    </td>
    <td>Willowdale, Newtonbrook
    </td></tr>
    <tr>
    <td>M3M
    </td>
    <td>North York
    </td>
    <td>Downsview
    </td></tr>
    <tr>
    <td>M4M
    </td>
    <td>East Toronto
    </td>
    <td>Studio District
    </td></tr>
    <tr>
    <td>M5M
    </td>
    <td>North York
    </td>
    <td>Bedford Park, Lawrence Manor East
    </td></tr>
    <tr>
    <td>M6M
    </td>
    <td>York
    </td>
    <td>Del Ray, Mount Dennis, Keelsdale and Silverthorn
    </td></tr>
    <tr>
    <td>M7M
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8M
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9M
    </td>
    <td>North York
    </td>
    <td>Humberlea, Emery
    </td></tr>
    <tr>
    <td>M1N
    </td>
    <td>Scarborough
    </td>
    <td>Birch Cliff, Cliffside West
    </td></tr>
    <tr>
    <td>M2N
    </td>
    <td>North York
    </td>
    <td>Willowdale, Willowdale East
    </td></tr>
    <tr>
    <td>M3N
    </td>
    <td>North York
    </td>
    <td>Downsview
    </td></tr>
    <tr>
    <td>M4N
    </td>
    <td>Central Toronto
    </td>
    <td>Lawrence Park
    </td></tr>
    <tr>
    <td>M5N
    </td>
    <td>Central Toronto
    </td>
    <td>Roselawn
    </td></tr>
    <tr>
    <td>M6N
    </td>
    <td>York
    </td>
    <td>Runnymede, The Junction North
    </td></tr>
    <tr>
    <td>M7N
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8N
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9N
    </td>
    <td>York
    </td>
    <td>Weston
    </td></tr>
    <tr>
    <td>M1P
    </td>
    <td>Scarborough
    </td>
    <td>Dorset Park, Wexford Heights, Scarborough Town Centre
    </td></tr>
    <tr>
    <td>M2P
    </td>
    <td>North York
    </td>
    <td>York Mills West
    </td></tr>
    <tr>
    <td>M3P
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4P
    </td>
    <td>Central Toronto
    </td>
    <td>Davisville North
    </td></tr>
    <tr>
    <td>M5P
    </td>
    <td>Central Toronto
    </td>
    <td>Forest Hill North &amp; West, Forest Hill Road Park
    </td></tr>
    <tr>
    <td>M6P
    </td>
    <td>West Toronto
    </td>
    <td>High Park, The Junction South
    </td></tr>
    <tr>
    <td>M7P
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8P
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9P
    </td>
    <td>Etobicoke
    </td>
    <td>Westmount
    </td></tr>
    <tr>
    <td>M1R
    </td>
    <td>Scarborough
    </td>
    <td>Wexford, Maryvale
    </td></tr>
    <tr>
    <td>M2R
    </td>
    <td>North York
    </td>
    <td>Willowdale, Willowdale West
    </td></tr>
    <tr>
    <td>M3R
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4R
    </td>
    <td>Central Toronto
    </td>
    <td>North Toronto West,  Lawrence Park
    </td></tr>
    <tr>
    <td>M5R
    </td>
    <td>Central Toronto
    </td>
    <td>The Annex, North Midtown, Yorkville
    </td></tr>
    <tr>
    <td>M6R
    </td>
    <td>West Toronto
    </td>
    <td>Parkdale, Roncesvalles
    </td></tr>
    <tr>
    <td>M7R
    </td>
    <td>Mississauga
    </td>
    <td>Canada Post Gateway Processing Centre
    </td></tr>
    <tr>
    <td>M8R
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9R
    </td>
    <td>Etobicoke
    </td>
    <td>Kingsview Village, St. Phillips, Martin Grove Gardens, Richview Gardens
    </td></tr>
    <tr>
    <td>M1S
    </td>
    <td>Scarborough
    </td>
    <td>Agincourt
    </td></tr>
    <tr>
    <td>M2S
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3S
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4S
    </td>
    <td>Central Toronto
    </td>
    <td>Davisville
    </td></tr>
    <tr>
    <td>M5S
    </td>
    <td>Downtown Toronto
    </td>
    <td>University of Toronto, Harbord
    </td></tr>
    <tr>
    <td>M6S
    </td>
    <td>West Toronto
    </td>
    <td>Runnymede, Swansea
    </td></tr>
    <tr>
    <td>M7S
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8S
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9S
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1T
    </td>
    <td>Scarborough
    </td>
    <td>Clarks Corners, Tam O'Shanter, Sullivan
    </td></tr>
    <tr>
    <td>M2T
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3T
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4T
    </td>
    <td>Central Toronto
    </td>
    <td>Moore Park, Summerhill East
    </td></tr>
    <tr>
    <td>M5T
    </td>
    <td>Downtown Toronto
    </td>
    <td>Kensington Market, Chinatown, Grange Park
    </td></tr>
    <tr>
    <td>M6T
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M7T
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8T
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M9T
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1V
    </td>
    <td>Scarborough
    </td>
    <td>Milliken, Agincourt North, Steeles East, L'Amoreaux East
    </td></tr>
    <tr>
    <td>M2V
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3V
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4V
    </td>
    <td>Central Toronto
    </td>
    <td>Summerhill West, Rathnelly, South Hill, Forest Hill SE, Deer Park
    </td></tr>
    <tr>
    <td>M5V
    </td>
    <td>Downtown Toronto
    </td>
    <td>CN Tower, King and Spadina, Railway Lands, Harbourfront West, Bathurst Quay, South Niagara, Island airport
    </td></tr>
    <tr>
    <td>M6V
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M7V
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8V
    </td>
    <td>Etobicoke
    </td>
    <td>New Toronto, Mimico South, Humber Bay Shores
    </td></tr>
    <tr>
    <td>M9V
    </td>
    <td>Etobicoke
    </td>
    <td>South Steeles, Silverstone, Humbergate, Jamestown, Mount Olive, Beaumond Heights, Thistletown, Albion Gardens
    </td></tr>
    <tr>
    <td>M1W
    </td>
    <td>Scarborough
    </td>
    <td>Steeles West, L'Amoreaux West
    </td></tr>
    <tr>
    <td>M2W
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3W
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4W
    </td>
    <td>Downtown Toronto
    </td>
    <td>Rosedale
    </td></tr>
    <tr>
    <td>M5W
    </td>
    <td>Downtown Toronto
    </td>
    <td>Stn A PO Boxes
    </td></tr>
    <tr>
    <td>M6W
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M7W
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8W
    </td>
    <td>Etobicoke
    </td>
    <td>Alderwood, Long Branch
    </td></tr>
    <tr>
    <td>M9W
    </td>
    <td>Etobicoke
    </td>
    <td>Northwest, West Humber - Clairville
    </td></tr>
    <tr>
    <td>M1X
    </td>
    <td>Scarborough
    </td>
    <td>Upper Rouge
    </td></tr>
    <tr>
    <td>M2X
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3X
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4X
    </td>
    <td>Downtown Toronto
    </td>
    <td>St. James Town, Cabbagetown
    </td></tr>
    <tr>
    <td>M5X
    </td>
    <td>Downtown Toronto
    </td>
    <td>First Canadian Place, Underground city
    </td></tr>
    <tr>
    <td>M6X
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M7X
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8X
    </td>
    <td>Etobicoke
    </td>
    <td>The Kingsway, Montgomery Road, Old Mill North
    </td></tr>
    <tr>
    <td>M9X
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1Y
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M2Y
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3Y
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4Y
    </td>
    <td>Downtown Toronto
    </td>
    <td>Church and Wellesley
    </td></tr>
    <tr>
    <td>M5Y
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M6Y
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M7Y
    </td>
    <td>East Toronto
    </td>
    <td>Business reply mail Processing Centre, South Central Letter Processing Plant Toronto
    </td></tr>
    <tr>
    <td>M8Y
    </td>
    <td>Etobicoke
    </td>
    <td>Old Mill South, King's Mill Park, Sunnylea, Humber Bay, Mimico NE, The Queensway East, Royal York South East, Kingsway Park South East
    </td></tr>
    <tr>
    <td>M9Y
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M1Z
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M2Z
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M3Z
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M4Z
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M5Z
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M6Z
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M7Z
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr>
    <tr>
    <td>M8Z
    </td>
    <td>Etobicoke
    </td>
    <td>Mimico NW, The Queensway West, South of Bloor, Kingsway Park South West, Royal York South West
    </td></tr>
    <tr>
    <td>M9Z
    </td>
    <td>Not assigned
    </td>
    <td>Not assigned
    </td></tr></tbody></table>



```
#finding all tags that start with td
links = my_table.findAll('td')
links[0]
```




    <td>M1A
    </td>




```
#loop over them to extract (Postcode, Borough, neighborhood)
Postcodes = [] 
Boroughs = [] 
neighborhoods = []

i = 0

for word in links:
  if i%3 == 0:
    Postcodes.append(word.get_text().strip())
    
  elif i%3 == 1:
    Boroughs.append(word.get_text().strip())
  
  elif i%3 == 2:
    neighborhoods.append(word.get_text().strip())
  i+=1
Boroughs
```




    ['Not assigned',
     'Not assigned',
     'North York',
     'North York',
     'Downtown Toronto',
     'North York',
     'Downtown Toronto',
     'Not assigned',
     'Etobicoke',
     'Scarborough',
     'Not assigned',
     'North York',
     'East York',
     'Downtown Toronto',
     'North York',
     'Not assigned',
     'Not assigned',
     'Etobicoke',
     'Scarborough',
     'Not assigned',
     'North York',
     'East York',
     'Downtown Toronto',
     'York',
     'Not assigned',
     'Not assigned',
     'Etobicoke',
     'Scarborough',
     'Not assigned',
     'Not assigned',
     'East Toronto',
     'Downtown Toronto',
     'York',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Scarborough',
     'Not assigned',
     'Not assigned',
     'East York',
     'Downtown Toronto',
     'Downtown Toronto',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Scarborough',
     'North York',
     'North York',
     'East York',
     'Downtown Toronto',
     'West Toronto',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Scarborough',
     'North York',
     'North York',
     'East York',
     'Downtown Toronto',
     'West Toronto',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Scarborough',
     'North York',
     'North York',
     'East Toronto',
     'Downtown Toronto',
     'West Toronto',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Scarborough',
     'North York',
     'North York',
     'East Toronto',
     'Downtown Toronto',
     'North York',
     'Not assigned',
     'Not assigned',
     'North York',
     'Scarborough',
     'North York',
     'North York',
     'East Toronto',
     'North York',
     'York',
     'Not assigned',
     'Not assigned',
     'North York',
     'Scarborough',
     'North York',
     'North York',
     'Central Toronto',
     'Central Toronto',
     'York',
     'Not assigned',
     'Not assigned',
     'York',
     'Scarborough',
     'North York',
     'Not assigned',
     'Central Toronto',
     'Central Toronto',
     'West Toronto',
     'Not assigned',
     'Not assigned',
     'Etobicoke',
     'Scarborough',
     'North York',
     'Not assigned',
     'Central Toronto',
     'Central Toronto',
     'West Toronto',
     'Mississauga',
     'Not assigned',
     'Etobicoke',
     'Scarborough',
     'Not assigned',
     'Not assigned',
     'Central Toronto',
     'Downtown Toronto',
     'West Toronto',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Scarborough',
     'Not assigned',
     'Not assigned',
     'Central Toronto',
     'Downtown Toronto',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Scarborough',
     'Not assigned',
     'Not assigned',
     'Central Toronto',
     'Downtown Toronto',
     'Not assigned',
     'Not assigned',
     'Etobicoke',
     'Etobicoke',
     'Scarborough',
     'Not assigned',
     'Not assigned',
     'Downtown Toronto',
     'Downtown Toronto',
     'Not assigned',
     'Not assigned',
     'Etobicoke',
     'Etobicoke',
     'Scarborough',
     'Not assigned',
     'Not assigned',
     'Downtown Toronto',
     'Downtown Toronto',
     'Not assigned',
     'Not assigned',
     'Etobicoke',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Downtown Toronto',
     'Not assigned',
     'Not assigned',
     'East Toronto',
     'Etobicoke',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Not assigned',
     'Etobicoke',
     'Not assigned']




```
len(neighborhoods) == len(Boroughs) == len(Postcodes)
```




    True




```
import pandas as pd
```


```
df = pd.DataFrame()
df['Postalcodes'] = Postcodes
df['Borough'] = Boroughs
df['neighborhood'] = neighborhoods
df[df['Postalcodes']== 'M1R']
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postalcodes</th>
      <th>Borough</th>
      <th>neighborhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>108</th>
      <td>M1R</td>
      <td>Scarborough</td>
      <td>Wexford, Maryvale</td>
    </tr>
  </tbody>
</table>
</div>




```
indexes = []
for index, row in df.iterrows():
  if row['Borough'] == 'Not assigned':
    indexes.append(index)
    continue
  elif row['neighborhood'] == 'Not assigned':
    row['neighborhood'] == row['Borough']
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postalcodes</th>
      <th>Borough</th>
      <th>neighborhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1A</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M2A</td>
      <td>Not assigned</td>
      <td>Not assigned</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Regent Park, Harbourfront</td>
    </tr>
  </tbody>
</table>
</div>




```
df.drop(indexes, inplace=True)
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postalcodes</th>
      <th>Borough</th>
      <th>neighborhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Regent Park, Harbourfront</td>
    </tr>
    <tr>
      <th>5</th>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Manor, Lawrence Heights</td>
    </tr>
    <tr>
      <th>6</th>
      <td>M7A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park, Ontario Provincial Government</td>
    </tr>
  </tbody>
</table>
</div>




```
df1 = df.groupby('Postalcodes')['neighborhood'].apply(', '.join).reset_index()
df1.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postalcodes</th>
      <th>neighborhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Malvern, Rouge</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Rouge Hill, Port Union, Highland Creek</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Guildwood, Morningside, West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```
df = pd.merge( df[['Postalcodes','Borough']], df1[['Postalcodes','neighborhood']], on='Postalcodes')
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postalcodes</th>
      <th>Borough</th>
      <th>neighborhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Regent Park, Harbourfront</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Manor, Lawrence Heights</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M7A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park, Ontario Provincial Government</td>
    </tr>
  </tbody>
</table>
</div>




```
df.shape
```




    (103, 3)




```
!wget -O geospatial_data.csv 'http://cocl.us/Geospatial_data'
```

    --2020-12-12 04:49:46--  http://cocl.us/Geospatial_data
    Resolving cocl.us (cocl.us)... 169.63.96.176, 169.63.96.194
    Connecting to cocl.us (cocl.us)|169.63.96.176|:80... connected.
    HTTP request sent, awaiting response... 301 Moved Permanently
    Location: https://cocl.us/Geospatial_data [following]
    --2020-12-12 04:49:46--  https://cocl.us/Geospatial_data
    Connecting to cocl.us (cocl.us)|169.63.96.176|:443... connected.
    HTTP request sent, awaiting response... 301 Moved Permanently
    Location: https://ibm.box.com/shared/static/9afzr83pps4pwf2smjjcf1y5mvgb18rr.csv [following]
    --2020-12-12 04:49:47--  https://ibm.box.com/shared/static/9afzr83pps4pwf2smjjcf1y5mvgb18rr.csv
    Resolving ibm.box.com (ibm.box.com)... 107.152.26.197
    Connecting to ibm.box.com (ibm.box.com)|107.152.26.197|:443... connected.
    HTTP request sent, awaiting response... 301 Moved Permanently
    Location: /public/static/9afzr83pps4pwf2smjjcf1y5mvgb18rr.csv [following]
    --2020-12-12 04:49:47--  https://ibm.box.com/public/static/9afzr83pps4pwf2smjjcf1y5mvgb18rr.csv
    Reusing existing connection to ibm.box.com:443.
    HTTP request sent, awaiting response... 301 Moved Permanently
    Location: https://ibm.ent.box.com/public/static/9afzr83pps4pwf2smjjcf1y5mvgb18rr.csv [following]
    --2020-12-12 04:49:47--  https://ibm.ent.box.com/public/static/9afzr83pps4pwf2smjjcf1y5mvgb18rr.csv
    Resolving ibm.ent.box.com (ibm.ent.box.com)... 107.152.29.201
    Connecting to ibm.ent.box.com (ibm.ent.box.com)|107.152.29.201|:443... connected.
    HTTP request sent, awaiting response... 302 Found
    Location: https://public.boxcloud.com/d/1/b1!VX_3jOuvAZ8nIes1FpAtDrMb73XxkiatTedLRjL_bzq8u0kIvH-bBI8ZEpEEhR9K89uxqO3n3KdmGil-7__jk-f-LTz2rqEBruZhYpPeI8Mfeaoi0Akhkt0hA9KKHJg6s9nYaDfIPohe3_3ASqwUVKMd4sG-42M_Q-EQ01tyhKRUxamJx41ZMKNzgV7qoMo6dvTO8CoGeQa3MWftGHXI0Pe9QwEQH0Rk65BPsWiaDxWDcbgZMc9TcmM32zh9XnCaAFaVH_80w2zwWkNyu2oSomrNXfA0NDSV7hfVJ9-W-cmzrfzbm7uFZ2ye7cdKztcEo4oolKP2DETchiB-VjFTbOS7_ngkdwk4XhOA-94FcWD8LHIdMVz8rKFjgjYX6CEob6JYPvs-96wSif4zDKDeulT7OSR37FEK6v30xTdEiPZGNAoWbzcCToWa-JdDSX5MbVZsoUu6L1WrNc5DAihxTqHf6Zi92oOBML7Xp41OHNr-uSc0grl8K6_ugaUW_R_lTqq9PB5Ccuhi4FlZ5Qth035zX8Uq5BwjpNmodNKAt6gbTUjqm49vjwFlyBmf7MubJ9EeASA9F75pPqHnEcNLmNz6EozbKJST37Gl9iTdJsLejdoOLrIzwUeb4wHRansIUAVa3EO4yzYh1OTf7spjKonm_9Swky7D5AmkZnaHLoJuQf-dP-1IvH590csKZg8EsCFZeyXrGmcnTxSul7RmLFYd5kQXctVpugIfC2g7skP1LM1cMpcId0J3IriZol2P7hlDZu3pwNMIEC9XGvQQnj2cmsU4ZVfkB8PgYjQrbOHv7qGUYoh4Wa19j6S_dmoW9SUUMKWnKL9XfnlGLwVx_WBkFCTsgh3fe81V_Ug6_cQLmJeEidSBuKb0ij8TO5HsaOEM4NMHeq3-xoVeceQ53Wb_kIByPPPID4V2vIc3XoCvx6Hd8vEAKYT6HqVeS1PjyufRB7LI9KP6J0HfCWoH-QvWObObO4wiELYhLej8Ugwjf0WDWyFXwyrhghJa2A_32N4CRWBs64VecTDp37OnmQkEquDCTVq-5_OgmgP7jklxIj7Ck8sUOAoeplDaSx0SX_Z1PVWqdI13LULq6YKkjBmvQDS5UcMxlrkmFa1hielqO2-kbJsZqLPliesNwYD1SeMlcZK8MCSURV9SKfE-9EoLSYHLcAwYxUT0h9A0EfJ90chF6oBpcuHAjQhgZ1YwCTIuJvNMgmfTN6qOERaVWek_0R21bHgPS9BnYyq1GRzvB1YFJlaGpN4LW_wMU8f__kPhVPh0EYfAV59XjbEejfomUBei_2GzzeCQ6NAuaJwo40o6sTdwr6oLqoAmRR2iIrIVbwWUAMFsou44Qb6IRBeNG0UbHbpYUXwKxXAWEUqBxrajXlJizG2tSlIkRZVPmAbAYL3fwEdA6xrgXFL-KfH3g_UO01n4td5OIcdZWjtTgQUxNVLKARBA0kQXk_EAVmIGJWvxLVd5FA../download [following]
    --2020-12-12 04:49:48--  https://public.boxcloud.com/d/1/b1!VX_3jOuvAZ8nIes1FpAtDrMb73XxkiatTedLRjL_bzq8u0kIvH-bBI8ZEpEEhR9K89uxqO3n3KdmGil-7__jk-f-LTz2rqEBruZhYpPeI8Mfeaoi0Akhkt0hA9KKHJg6s9nYaDfIPohe3_3ASqwUVKMd4sG-42M_Q-EQ01tyhKRUxamJx41ZMKNzgV7qoMo6dvTO8CoGeQa3MWftGHXI0Pe9QwEQH0Rk65BPsWiaDxWDcbgZMc9TcmM32zh9XnCaAFaVH_80w2zwWkNyu2oSomrNXfA0NDSV7hfVJ9-W-cmzrfzbm7uFZ2ye7cdKztcEo4oolKP2DETchiB-VjFTbOS7_ngkdwk4XhOA-94FcWD8LHIdMVz8rKFjgjYX6CEob6JYPvs-96wSif4zDKDeulT7OSR37FEK6v30xTdEiPZGNAoWbzcCToWa-JdDSX5MbVZsoUu6L1WrNc5DAihxTqHf6Zi92oOBML7Xp41OHNr-uSc0grl8K6_ugaUW_R_lTqq9PB5Ccuhi4FlZ5Qth035zX8Uq5BwjpNmodNKAt6gbTUjqm49vjwFlyBmf7MubJ9EeASA9F75pPqHnEcNLmNz6EozbKJST37Gl9iTdJsLejdoOLrIzwUeb4wHRansIUAVa3EO4yzYh1OTf7spjKonm_9Swky7D5AmkZnaHLoJuQf-dP-1IvH590csKZg8EsCFZeyXrGmcnTxSul7RmLFYd5kQXctVpugIfC2g7skP1LM1cMpcId0J3IriZol2P7hlDZu3pwNMIEC9XGvQQnj2cmsU4ZVfkB8PgYjQrbOHv7qGUYoh4Wa19j6S_dmoW9SUUMKWnKL9XfnlGLwVx_WBkFCTsgh3fe81V_Ug6_cQLmJeEidSBuKb0ij8TO5HsaOEM4NMHeq3-xoVeceQ53Wb_kIByPPPID4V2vIc3XoCvx6Hd8vEAKYT6HqVeS1PjyufRB7LI9KP6J0HfCWoH-QvWObObO4wiELYhLej8Ugwjf0WDWyFXwyrhghJa2A_32N4CRWBs64VecTDp37OnmQkEquDCTVq-5_OgmgP7jklxIj7Ck8sUOAoeplDaSx0SX_Z1PVWqdI13LULq6YKkjBmvQDS5UcMxlrkmFa1hielqO2-kbJsZqLPliesNwYD1SeMlcZK8MCSURV9SKfE-9EoLSYHLcAwYxUT0h9A0EfJ90chF6oBpcuHAjQhgZ1YwCTIuJvNMgmfTN6qOERaVWek_0R21bHgPS9BnYyq1GRzvB1YFJlaGpN4LW_wMU8f__kPhVPh0EYfAV59XjbEejfomUBei_2GzzeCQ6NAuaJwo40o6sTdwr6oLqoAmRR2iIrIVbwWUAMFsou44Qb6IRBeNG0UbHbpYUXwKxXAWEUqBxrajXlJizG2tSlIkRZVPmAbAYL3fwEdA6xrgXFL-KfH3g_UO01n4td5OIcdZWjtTgQUxNVLKARBA0kQXk_EAVmIGJWvxLVd5FA../download
    Resolving public.boxcloud.com (public.boxcloud.com)... 107.152.29.200
    Connecting to public.boxcloud.com (public.boxcloud.com)|107.152.29.200|:443... connected.
    HTTP request sent, awaiting response... 200 OK
    Length: 2891 (2.8K) [text/csv]
    Saving to: ‘geospatial_data.csv’
    
    geospatial_data.csv 100%[===================>]   2.82K  --.-KB/s    in 0s      
    
    2020-12-12 04:49:48 (51.6 MB/s) - ‘geospatial_data.csv’ saved [2891/2891]
    



```
geospatial_data = pd.read_csv('geospatial_data.csv')
geospatial_data.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postal Code</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>43.806686</td>
      <td>-79.194353</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>43.784535</td>
      <td>-79.160497</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>43.763573</td>
      <td>-79.188711</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>43.770992</td>
      <td>-79.216917</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>43.773136</td>
      <td>-79.239476</td>
    </tr>
  </tbody>
</table>
</div>




```
geospatial_data = geospatial_data.rename(columns={"Postal Code": "Postalcodes"}, errors="raise")
geospatial_data.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postalcodes</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>43.806686</td>
      <td>-79.194353</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>43.784535</td>
      <td>-79.160497</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>43.763573</td>
      <td>-79.188711</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>43.770992</td>
      <td>-79.216917</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>43.773136</td>
      <td>-79.239476</td>
    </tr>
  </tbody>
</table>
</div>




```
#merge both tables together
df = df.merge(geospatial_data, on='Postalcodes')
                                                        
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postalcodes</th>
      <th>Borough</th>
      <th>neighborhood</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M3A</td>
      <td>North York</td>
      <td>Parkwoods</td>
      <td>43.753259</td>
      <td>-79.329656</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M4A</td>
      <td>North York</td>
      <td>Victoria Village</td>
      <td>43.725882</td>
      <td>-79.315572</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M5A</td>
      <td>Downtown Toronto</td>
      <td>Regent Park, Harbourfront</td>
      <td>43.654260</td>
      <td>-79.360636</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M6A</td>
      <td>North York</td>
      <td>Lawrence Manor, Lawrence Heights</td>
      <td>43.718518</td>
      <td>-79.464763</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M7A</td>
      <td>Downtown Toronto</td>
      <td>Queen's Park, Ontario Provincial Government</td>
      <td>43.662301</td>
      <td>-79.389494</td>
    </tr>
  </tbody>
</table>
</div>




```
print('The dataframe has {} boroughs and {} neighborhoods.'.format(
        len(df['Borough'].unique()),
        df.shape[0]
    )
)
```

    The dataframe has 10 boroughs and 103 neighborhoods.



```
import json
!pip install geopy
from geopy.geocoders import Nominatim
!pip install folium==0.5.0
import folium
```

    Requirement already satisfied: geopy in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (2.0.0)
    Requirement already satisfied: geographiclib<2,>=1.49 in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from geopy) (1.50)
    Requirement already satisfied: folium==0.5.0 in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (0.5.0)
    Requirement already satisfied: branca in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from folium==0.5.0) (0.4.1)
    Requirement already satisfied: jinja2 in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from folium==0.5.0) (2.11.2)
    Requirement already satisfied: six in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from folium==0.5.0) (1.15.0)
    Requirement already satisfied: requests in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from folium==0.5.0) (2.24.0)
    Requirement already satisfied: MarkupSafe>=0.23 in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from jinja2->folium==0.5.0) (1.1.1)
    Requirement already satisfied: chardet<4,>=3.0.2 in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from requests->folium==0.5.0) (3.0.4)
    Requirement already satisfied: idna<3,>=2.5 in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from requests->folium==0.5.0) (2.9)
    Requirement already satisfied: certifi>=2017.4.17 in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from requests->folium==0.5.0) (2020.12.5)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in /opt/conda/envs/Python-3.7-main/lib/python3.7/site-packages (from requests->folium==0.5.0) (1.25.9)



```
address = 'Toronto'

geolocator = Nominatim(user_agent="t_explorer")
location = geolocator.geocode(address)
latitude = location.latitude
longitude = location.longitude
print('The geograpical coordinate of Toronto are {}, {}.'.format(latitude, longitude))
```

    The geograpical coordinate of Toronto are 43.6534817, -79.3839347.



```
map_toronto = folium.Map(location=[latitude, longitude], zoom_start=11)

# add markers to map
for lat, lng, label in zip(df['Latitude'], df['Longitude'], df['neighborhood']):
    label = folium.Popup(label, parse_html=True)
    folium.CircleMarker(
        [lat, lng],
        radius=5,
        popup=label,
        color='blue',
        fill=True,
        fill_color='#3186cc',
        fill_opacity=0.7,
        parse_html=False).add_to(map_toronto)  
    
map_toronto
```




<div style="width:100%;"><div style="position:relative;width:100%;height:0;padding-bottom:60%;"><span style="color:#565656">Make this Notebook Trusted to load map: File -> Trust Notebook</span><iframe src="about:blank" style="position:absolute;width:100%;height:100%;left:0;top:0;border:none !important;" data-html=PCFET0NUWVBFIGh0bWw+CjxoZWFkPiAgICAKICAgIDxtZXRhIGh0dHAtZXF1aXY9ImNvbnRlbnQtdHlwZSIgY29udGVudD0idGV4dC9odG1sOyBjaGFyc2V0PVVURi04IiAvPgogICAgPHNjcmlwdD5MX1BSRUZFUl9DQU5WQVMgPSBmYWxzZTsgTF9OT19UT1VDSCA9IGZhbHNlOyBMX0RJU0FCTEVfM0QgPSBmYWxzZTs8L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL2Nkbi5qc2RlbGl2ci5uZXQvbnBtL2xlYWZsZXRAMS4yLjAvZGlzdC9sZWFmbGV0LmpzIj48L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL2FqYXguZ29vZ2xlYXBpcy5jb20vYWpheC9saWJzL2pxdWVyeS8xLjExLjEvanF1ZXJ5Lm1pbi5qcyI+PC9zY3JpcHQ+CiAgICA8c2NyaXB0IHNyYz0iaHR0cHM6Ly9tYXhjZG4uYm9vdHN0cmFwY2RuLmNvbS9ib290c3RyYXAvMy4yLjAvanMvYm9vdHN0cmFwLm1pbi5qcyI+PC9zY3JpcHQ+CiAgICA8c2NyaXB0IHNyYz0iaHR0cHM6Ly9jZG5qcy5jbG91ZGZsYXJlLmNvbS9hamF4L2xpYnMvTGVhZmxldC5hd2Vzb21lLW1hcmtlcnMvMi4wLjIvbGVhZmxldC5hd2Vzb21lLW1hcmtlcnMuanMiPjwvc2NyaXB0PgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL2Nkbi5qc2RlbGl2ci5uZXQvbnBtL2xlYWZsZXRAMS4yLjAvZGlzdC9sZWFmbGV0LmNzcyIvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL21heGNkbi5ib290c3RyYXBjZG4uY29tL2Jvb3RzdHJhcC8zLjIuMC9jc3MvYm9vdHN0cmFwLm1pbi5jc3MiLz4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9tYXhjZG4uYm9vdHN0cmFwY2RuLmNvbS9ib290c3RyYXAvMy4yLjAvY3NzL2Jvb3RzdHJhcC10aGVtZS5taW4uY3NzIi8+CiAgICA8bGluayByZWw9InN0eWxlc2hlZXQiIGhyZWY9Imh0dHBzOi8vbWF4Y2RuLmJvb3RzdHJhcGNkbi5jb20vZm9udC1hd2Vzb21lLzQuNi4zL2Nzcy9mb250LWF3ZXNvbWUubWluLmNzcyIvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL2NkbmpzLmNsb3VkZmxhcmUuY29tL2FqYXgvbGlicy9MZWFmbGV0LmF3ZXNvbWUtbWFya2Vycy8yLjAuMi9sZWFmbGV0LmF3ZXNvbWUtbWFya2Vycy5jc3MiLz4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9yYXdnaXQuY29tL3B5dGhvbi12aXN1YWxpemF0aW9uL2ZvbGl1bS9tYXN0ZXIvZm9saXVtL3RlbXBsYXRlcy9sZWFmbGV0LmF3ZXNvbWUucm90YXRlLmNzcyIvPgogICAgPHN0eWxlPmh0bWwsIGJvZHkge3dpZHRoOiAxMDAlO2hlaWdodDogMTAwJTttYXJnaW46IDA7cGFkZGluZzogMDt9PC9zdHlsZT4KICAgIDxzdHlsZT4jbWFwIHtwb3NpdGlvbjphYnNvbHV0ZTt0b3A6MDtib3R0b206MDtyaWdodDowO2xlZnQ6MDt9PC9zdHlsZT4KICAgIAogICAgICAgICAgICA8c3R5bGU+ICNtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUgewogICAgICAgICAgICAgICAgcG9zaXRpb24gOiByZWxhdGl2ZTsKICAgICAgICAgICAgICAgIHdpZHRoIDogMTAwLjAlOwogICAgICAgICAgICAgICAgaGVpZ2h0OiAxMDAuMCU7CiAgICAgICAgICAgICAgICBsZWZ0OiAwLjAlOwogICAgICAgICAgICAgICAgdG9wOiAwLjAlOwogICAgICAgICAgICAgICAgfQogICAgICAgICAgICA8L3N0eWxlPgogICAgICAgIAo8L2hlYWQ+Cjxib2R5PiAgICAKICAgIAogICAgICAgICAgICA8ZGl2IGNsYXNzPSJmb2xpdW0tbWFwIiBpZD0ibWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1IiA+PC9kaXY+CiAgICAgICAgCjwvYm9keT4KPHNjcmlwdD4gICAgCiAgICAKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGJvdW5kcyA9IG51bGw7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgdmFyIG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSA9IEwubWFwKAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgJ21hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NScsCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICB7Y2VudGVyOiBbNDMuNjUzNDgxNywtNzkuMzgzOTM0N10sCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICB6b29tOiAxMSwKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIG1heEJvdW5kczogYm91bmRzLAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgbGF5ZXJzOiBbXSwKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIHdvcmxkQ29weUp1bXA6IGZhbHNlLAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgY3JzOiBMLkNSUy5FUFNHMzg1NwogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICB9KTsKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHRpbGVfbGF5ZXJfMjFmYTcyZmFmODA0NDBkYmFjZGE2MjU4YzI1NWM2ODEgPSBMLnRpbGVMYXllcigKICAgICAgICAgICAgICAgICdodHRwczovL3tzfS50aWxlLm9wZW5zdHJlZXRtYXAub3JnL3t6fS97eH0ve3l9LnBuZycsCiAgICAgICAgICAgICAgICB7CiAgImF0dHJpYnV0aW9uIjogbnVsbCwKICAiZGV0ZWN0UmV0aW5hIjogZmFsc2UsCiAgIm1heFpvb20iOiAxOCwKICAibWluWm9vbSI6IDEsCiAgIm5vV3JhcCI6IGZhbHNlLAogICJzdWJkb21haW5zIjogImFiYyIKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2RiNDNkMmY3MjJhZjQzZjdhYzIwYmE2OWRlOWU1NDM1ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzUzMjU4NiwtNzkuMzI5NjU2NV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8zOTE2MjM0NmM4YjU0YTY4OTBhNWIxY2UwNDk2ZDcwMiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8zYmM2NGZkOGRkODg0NGY4OGZmOGVhNzQ0ZjY2MDc4OSA9ICQoJzxkaXYgaWQ9Imh0bWxfM2JjNjRmZDhkZDg4NDRmODhmZjhlYTc0NGY2NjA3ODkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlBhcmt3b29kczwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMzkxNjIzNDZjOGI1NGE2ODkwYTViMWNlMDQ5NmQ3MDIuc2V0Q29udGVudChodG1sXzNiYzY0ZmQ4ZGQ4ODQ0Zjg4ZmY4ZWE3NDRmNjYwNzg5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2RiNDNkMmY3MjJhZjQzZjdhYzIwYmE2OWRlOWU1NDM1LmJpbmRQb3B1cChwb3B1cF8zOTE2MjM0NmM4YjU0YTY4OTBhNWIxY2UwNDk2ZDcwMik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9lNmViNWU5ZWUzYmM0OWQ3YjMxMDJmMmY1Y2ViMTJmYiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcyNTg4MjI5OTk5OTk5NSwtNzkuMzE1NTcxNTk5OTk5OThdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYzAyMGM0OTEwZDUyNDQyMWE1YjEyZmRmZWVlYWVmOWQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNWQxMmYwNGFiNTNiNDhlNzlmNjVlZDExMmFjMTZlMDYgPSAkKCc8ZGl2IGlkPSJodG1sXzVkMTJmMDRhYjUzYjQ4ZTc5ZjY1ZWQxMTJhYzE2ZTA2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5WaWN0b3JpYSBWaWxsYWdlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9jMDIwYzQ5MTBkNTI0NDIxYTViMTJmZGZlZWVhZWY5ZC5zZXRDb250ZW50KGh0bWxfNWQxMmYwNGFiNTNiNDhlNzlmNjVlZDExMmFjMTZlMDYpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfZTZlYjVlOWVlM2JjNDlkN2IzMTAyZjJmNWNlYjEyZmIuYmluZFBvcHVwKHBvcHVwX2MwMjBjNDkxMGQ1MjQ0MjFhNWIxMmZkZmVlZWFlZjlkKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2Y1MzI3YWQ1NDk4ZDQyZDZiZjhjOTg5N2M2NGNlMzBjID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjU0MjU5OSwtNzkuMzYwNjM1OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8wZjY2NGUwNGY3ZTY0MWY0ODU1YzVhNTZiMmYxMjIyMCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8zNDA0OTM3NmI0ZmE0NjNiYmUyYmM5YjRhMzIzYTM3MSA9ICQoJzxkaXYgaWQ9Imh0bWxfMzQwNDkzNzZiNGZhNDYzYmJlMmJjOWI0YTMyM2EzNzEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlJlZ2VudCBQYXJrLCBIYXJib3VyZnJvbnQ8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzBmNjY0ZTA0ZjdlNjQxZjQ4NTVjNWE1NmIyZjEyMjIwLnNldENvbnRlbnQoaHRtbF8zNDA0OTM3NmI0ZmE0NjNiYmUyYmM5YjRhMzIzYTM3MSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9mNTMyN2FkNTQ5OGQ0MmQ2YmY4Yzk4OTdjNjRjZTMwYy5iaW5kUG9wdXAocG9wdXBfMGY2NjRlMDRmN2U2NDFmNDg1NWM1YTU2YjJmMTIyMjApOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZWM2YzkyMzlkYTM0NDEwZDgzMjBmOTMxZjI2NjVhMjYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MTg1MTc5OTk5OTk5OTYsLTc5LjQ2NDc2MzI5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2RkZTVmZTFhMmJmZDQ0YTE5ZTNhNTE3OTZkYzNkOTk3ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2Q0YjhjODcwZDhkZTQ2NDdhNjVhNDRhZmNlMmQwN2Y4ID0gJCgnPGRpdiBpZD0iaHRtbF9kNGI4Yzg3MGQ4ZGU0NjQ3YTY1YTQ0YWZjZTJkMDdmOCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TGF3cmVuY2UgTWFub3IsIExhd3JlbmNlIEhlaWdodHM8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2RkZTVmZTFhMmJmZDQ0YTE5ZTNhNTE3OTZkYzNkOTk3LnNldENvbnRlbnQoaHRtbF9kNGI4Yzg3MGQ4ZGU0NjQ3YTY1YTQ0YWZjZTJkMDdmOCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9lYzZjOTIzOWRhMzQ0MTBkODMyMGY5MzFmMjY2NWEyNi5iaW5kUG9wdXAocG9wdXBfZGRlNWZlMWEyYmZkNDRhMTllM2E1MTc5NmRjM2Q5OTcpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNzBkYzY5NjkzYTVkNDA3MTk1ZDQ0NWQ4MjJjYTE4YTMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NjIzMDE1LC03OS4zODk0OTM4XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzgxZDM2MjU0NTkwYTQ1OTRiNjdkYTU2MmJhMTliZTI5ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2ZmZWUxZGJkNWE2YjRiMTViNWEzMzllZTNiMzIzNTYxID0gJCgnPGRpdiBpZD0iaHRtbF9mZmVlMWRiZDVhNmI0YjE1YjVhMzM5ZWUzYjMyMzU2MSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+UXVlZW4mIzM5O3MgUGFyaywgT250YXJpbyBQcm92aW5jaWFsIEdvdmVybm1lbnQ8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzgxZDM2MjU0NTkwYTQ1OTRiNjdkYTU2MmJhMTliZTI5LnNldENvbnRlbnQoaHRtbF9mZmVlMWRiZDVhNmI0YjE1YjVhMzM5ZWUzYjMyMzU2MSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl83MGRjNjk2OTNhNWQ0MDcxOTVkNDQ1ZDgyMmNhMThhMy5iaW5kUG9wdXAocG9wdXBfODFkMzYyNTQ1OTBhNDU5NGI2N2RhNTYyYmExOWJlMjkpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMTZhMzQxNTMxOTI3NGYwYmI3MTVhOWM0ZmRhYmM3MTkgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42Njc4NTU2LC03OS41MzIyNDI0MDAwMDAwMl0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8zODFmZWJhMjUwZGM0ZDhkODc1YzE1OTZiNmRhNDRjNCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84ZTFiNTc4N2VjNDA0YTY4ODcwNzIyOGQ1YzBhY2Y4NyA9ICQoJzxkaXYgaWQ9Imh0bWxfOGUxYjU3ODdlYzQwNGE2ODg3MDcyMjhkNWMwYWNmODciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPklzbGluZ3RvbiBBdmVudWUsIEh1bWJlciBWYWxsZXkgVmlsbGFnZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMzgxZmViYTI1MGRjNGQ4ZDg3NWMxNTk2YjZkYTQ0YzQuc2V0Q29udGVudChodG1sXzhlMWI1Nzg3ZWM0MDRhNjg4NzA3MjI4ZDVjMGFjZjg3KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzE2YTM0MTUzMTkyNzRmMGJiNzE1YTljNGZkYWJjNzE5LmJpbmRQb3B1cChwb3B1cF8zODFmZWJhMjUwZGM0ZDhkODc1YzE1OTZiNmRhNDRjNCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9hYTA1ODU5MWM3ZTg0NTZlYmU5ZTdjOTU4ZjE5ZDMzOSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjgwNjY4NjI5OTk5OTk5NiwtNzkuMTk0MzUzNDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMDc1MzEwMWZkZDcyNGJmOGJiNWFlNzk3YTQ3YTJiN2UgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYTQwNjk2ZWI2MDlkNGQ1YWE5NmNhMmY3MGZmMGE3YjkgPSAkKCc8ZGl2IGlkPSJodG1sX2E0MDY5NmViNjA5ZDRkNWFhOTZjYTJmNzBmZjBhN2I5IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5NYWx2ZXJuLCBSb3VnZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMDc1MzEwMWZkZDcyNGJmOGJiNWFlNzk3YTQ3YTJiN2Uuc2V0Q29udGVudChodG1sX2E0MDY5NmViNjA5ZDRkNWFhOTZjYTJmNzBmZjBhN2I5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2FhMDU4NTkxYzdlODQ1NmViZTllN2M5NThmMTlkMzM5LmJpbmRQb3B1cChwb3B1cF8wNzUzMTAxZmRkNzI0YmY4YmI1YWU3OTdhNDdhMmI3ZSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl83MmY4NzUyMDc5Yjc0NGY4ODFmYjZhYjIzNTA2MWUxOCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc0NTkwNTc5OTk5OTk5NiwtNzkuMzUyMTg4XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzJjZmNkNGE2MThmMTQxMWVhZTJhY2M0MjNkZWE3MjA1ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2E1ODI1OTdlYmJhZDQ3MDFiYWY1MzlhMzRiMzZiNTAyID0gJCgnPGRpdiBpZD0iaHRtbF9hNTgyNTk3ZWJiYWQ0NzAxYmFmNTM5YTM0YjM2YjUwMiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RG9uIE1pbGxzPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8yY2ZjZDRhNjE4ZjE0MTFlYWUyYWNjNDIzZGVhNzIwNS5zZXRDb250ZW50KGh0bWxfYTU4MjU5N2ViYmFkNDcwMWJhZjUzOWEzNGIzNmI1MDIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNzJmODc1MjA3OWI3NDRmODgxZmI2YWIyMzUwNjFlMTguYmluZFBvcHVwKHBvcHVwXzJjZmNkNGE2MThmMTQxMWVhZTJhY2M0MjNkZWE3MjA1KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzIxMzI3MzdiOTk1NTRmMzhhMWYxZTJmOWM0YjE0NDdhID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzA2Mzk3MiwtNzkuMzA5OTM3XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2ZkMjA0ZTk4ZTkyNTQwNTViMjE1ZDgzNDY0MWY4ODVkID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2I0MzhjMWQ4NDAxMTRhZTg4YjRiNTc0OTg2YTQ3MjZlID0gJCgnPGRpdiBpZD0iaHRtbF9iNDM4YzFkODQwMTE0YWU4OGI0YjU3NDk4NmE0NzI2ZSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+UGFya3ZpZXcgSGlsbCwgV29vZGJpbmUgR2FyZGVuczwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZmQyMDRlOThlOTI1NDA1NWIyMTVkODM0NjQxZjg4NWQuc2V0Q29udGVudChodG1sX2I0MzhjMWQ4NDAxMTRhZTg4YjRiNTc0OTg2YTQ3MjZlKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzIxMzI3MzdiOTk1NTRmMzhhMWYxZTJmOWM0YjE0NDdhLmJpbmRQb3B1cChwb3B1cF9mZDIwNGU5OGU5MjU0MDU1YjIxNWQ4MzQ2NDFmODg1ZCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8xYTU1OWU5YjQxYTk0NGY3YjdlZWI0ZGZlNGViMmZjOCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY1NzE2MTgsLTc5LjM3ODkzNzA5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzdiNDgxYjdiOTFlYTQyMzZiZDFlM2Y0YzQ5OTA0M2E5ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2QzNzQ0NmQ0NzAzYzRiN2Q5YmMxNTRjNDYwMGE2M2U3ID0gJCgnPGRpdiBpZD0iaHRtbF9kMzc0NDZkNDcwM2M0YjdkOWJjMTU0YzQ2MDBhNjNlNyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+R2FyZGVuIERpc3RyaWN0LCBSeWVyc29uPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF83YjQ4MWI3YjkxZWE0MjM2YmQxZTNmNGM0OTkwNDNhOS5zZXRDb250ZW50KGh0bWxfZDM3NDQ2ZDQ3MDNjNGI3ZDliYzE1NGM0NjAwYTYzZTcpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMWE1NTllOWI0MWE5NDRmN2I3ZWViNGRmZTRlYjJmYzguYmluZFBvcHVwKHBvcHVwXzdiNDgxYjdiOTFlYTQyMzZiZDFlM2Y0YzQ5OTA0M2E5KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2MwZjZiYTYzMTdkOTRiNzQ5ODE1MTg2YjE2NWU0MDc0ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzA5NTc3LC03OS40NDUwNzI1OTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8zNWNmNjZhOGQ2MGE0NzE1YWRiZWY3YzRjNmUzZGM4YSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84NWE2ZDA3OTUyZWM0NGE1YjBjOWFhNDI3OTg3YjcwNSA9ICQoJzxkaXYgaWQ9Imh0bWxfODVhNmQwNzk1MmVjNDRhNWIwYzlhYTQyNzk4N2I3MDUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkdsZW5jYWlybjwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMzVjZjY2YThkNjBhNDcxNWFkYmVmN2M0YzZlM2RjOGEuc2V0Q29udGVudChodG1sXzg1YTZkMDc5NTJlYzQ0YTViMGM5YWE0Mjc5ODdiNzA1KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2MwZjZiYTYzMTdkOTRiNzQ5ODE1MTg2YjE2NWU0MDc0LmJpbmRQb3B1cChwb3B1cF8zNWNmNjZhOGQ2MGE0NzE1YWRiZWY3YzRjNmUzZGM4YSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8xNzBjOGY5NDFmZDI0YWUxODIzOTNkMDdlZGU1MjA1YiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY1MDk0MzIsLTc5LjU1NDcyNDQwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2VkOGJhODFiZWRjNjQ3Mzg4YzkzOTMwZGRiNTFjMTk4ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzRlNDUxN2U0OTI2NTQ1MWZhNWU2ZGUxZWI3ZmYwNjU3ID0gJCgnPGRpdiBpZD0iaHRtbF80ZTQ1MTdlNDkyNjU0NTFmYTVlNmRlMWViN2ZmMDY1NyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V2VzdCBEZWFuZSBQYXJrLCBQcmluY2VzcyBHYXJkZW5zLCBNYXJ0aW4gR3JvdmUsIElzbGluZ3RvbiwgQ2xvdmVyZGFsZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZWQ4YmE4MWJlZGM2NDczODhjOTM5MzBkZGI1MWMxOTguc2V0Q29udGVudChodG1sXzRlNDUxN2U0OTI2NTQ1MWZhNWU2ZGUxZWI3ZmYwNjU3KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzE3MGM4Zjk0MWZkMjRhZTE4MjM5M2QwN2VkZTUyMDViLmJpbmRQb3B1cChwb3B1cF9lZDhiYTgxYmVkYzY0NzM4OGM5MzkzMGRkYjUxYzE5OCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl80YjFiZWNiZjNkZmY0ZWI0YjM5MzNkZmJmODQxZGI5NyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc4NDUzNTEsLTc5LjE2MDQ5NzA5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzUxYTQ1YjBhZmM3ODQ5NmQ4NDliMDA4OGMyZjkyMzQ1ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzgyMzEwNzM3N2ZmOTQzOWViZjhjMDIzMDRlYjRjNDVkID0gJCgnPGRpdiBpZD0iaHRtbF84MjMxMDczNzdmZjk0MzllYmY4YzAyMzA0ZWI0YzQ1ZCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Um91Z2UgSGlsbCwgUG9ydCBVbmlvbiwgSGlnaGxhbmQgQ3JlZWs8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzUxYTQ1YjBhZmM3ODQ5NmQ4NDliMDA4OGMyZjkyMzQ1LnNldENvbnRlbnQoaHRtbF84MjMxMDczNzdmZjk0MzllYmY4YzAyMzA0ZWI0YzQ1ZCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl80YjFiZWNiZjNkZmY0ZWI0YjM5MzNkZmJmODQxZGI5Ny5iaW5kUG9wdXAocG9wdXBfNTFhNDViMGFmYzc4NDk2ZDg0OWIwMDg4YzJmOTIzNDUpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOGM2M2YwNGE4MjcxNDNlZGEwOTE5NjhlZGUyNTk4ZTMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MjU4OTk3MDAwMDAwMSwtNzkuMzQwOTIzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2YxZjMxYjM5ZDJlNDQxYWNiZGJkZmViOWNiY2M1M2U0ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzM4MGMyM2I4YmVjNDRkMjg4NTVjOTQ3NjY0MDExNDQ1ID0gJCgnPGRpdiBpZD0iaHRtbF8zODBjMjNiOGJlYzQ0ZDI4ODU1Yzk0NzY2NDAxMTQ0NSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RG9uIE1pbGxzPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9mMWYzMWIzOWQyZTQ0MWFjYmRiZGZlYjljYmNjNTNlNC5zZXRDb250ZW50KGh0bWxfMzgwYzIzYjhiZWM0NGQyODg1NWM5NDc2NjQwMTE0NDUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOGM2M2YwNGE4MjcxNDNlZGEwOTE5NjhlZGUyNTk4ZTMuYmluZFBvcHVwKHBvcHVwX2YxZjMxYjM5ZDJlNDQxYWNiZGJkZmViOWNiY2M1M2U0KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzUyNjM1NTJhMzY2YzQxODBhMzIwY2M5NTNmMTY3Yzg4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjk1MzQzOTAwMDAwMDA1LC03OS4zMTgzODg3XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzMyOWQ1MDA0MmQxOTQ2ZGRhYjk0YTY2ODZlNzJiZTc0ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzhhMGM0NTUzNmM1NTQwYjU4NzdkMTQxZjY2YzZlNThhID0gJCgnPGRpdiBpZD0iaHRtbF84YTBjNDU1MzZjNTU0MGI1ODc3ZDE0MWY2NmM2ZTU4YSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V29vZGJpbmUgSGVpZ2h0czwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMzI5ZDUwMDQyZDE5NDZkZGFiOTRhNjY4NmU3MmJlNzQuc2V0Q29udGVudChodG1sXzhhMGM0NTUzNmM1NTQwYjU4NzdkMTQxZjY2YzZlNThhKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzUyNjM1NTJhMzY2YzQxODBhMzIwY2M5NTNmMTY3Yzg4LmJpbmRQb3B1cChwb3B1cF8zMjlkNTAwNDJkMTk0NmRkYWI5NGE2Njg2ZTcyYmU3NCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9jNDViY2QyYzU3OGQ0OTQ3YTA4MzYyZWMxZjI3ZGNhZiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY1MTQ5MzksLTc5LjM3NTQxNzldLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfNGI2MzMzNGI1OTcyNGM4YWIwNGEwMzVlNGNmMTJmYmYgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNWViZWExMGZmMzY3NDM3ODllNmVjN2Q0ZjdmYzcyMjAgPSAkKCc8ZGl2IGlkPSJodG1sXzVlYmVhMTBmZjM2NzQzNzg5ZTZlYzdkNGY3ZmM3MjIwIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5TdC4gSmFtZXMgVG93bjwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNGI2MzMzNGI1OTcyNGM4YWIwNGEwMzVlNGNmMTJmYmYuc2V0Q29udGVudChodG1sXzVlYmVhMTBmZjM2NzQzNzg5ZTZlYzdkNGY3ZmM3MjIwKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2M0NWJjZDJjNTc4ZDQ5NDdhMDgzNjJlYzFmMjdkY2FmLmJpbmRQb3B1cChwb3B1cF80YjYzMzM0YjU5NzI0YzhhYjA0YTAzNWU0Y2YxMmZiZik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9iMjkyZWM1OTI3Mjg0Y2IyOWJkNWIzOWVhMGMyNDk3YiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY5Mzc4MTMsLTc5LjQyODE5MTQwMDAwMDAyXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzA1ZDdjNGJjMjM3YzQ5MjhiNzc3MmMzN2M3ZjgxOWQzID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2M2NDgyMTI3ZTc4YTQ1NjdhYjJhZWY5NmI4NDEzMWUyID0gJCgnPGRpdiBpZD0iaHRtbF9jNjQ4MjEyN2U3OGE0NTY3YWIyYWVmOTZiODQxMzFlMiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+SHVtZXdvb2QtQ2VkYXJ2YWxlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8wNWQ3YzRiYzIzN2M0OTI4Yjc3NzJjMzdjN2Y4MTlkMy5zZXRDb250ZW50KGh0bWxfYzY0ODIxMjdlNzhhNDU2N2FiMmFlZjk2Yjg0MTMxZTIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYjI5MmVjNTkyNzI4NGNiMjliZDViMzllYTBjMjQ5N2IuYmluZFBvcHVwKHBvcHVwXzA1ZDdjNGJjMjM3YzQ5MjhiNzc3MmMzN2M3ZjgxOWQzKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzQ3NjI1Y2I2MzU4ODQxNWRhNGRhYzE0Y2M3OTcwOWNhID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjQzNTE1MiwtNzkuNTc3MjAwNzk5OTk5OTldLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfM2Q2ZjEzYzY4NjM1NDRiNjgwOWQ1ZTM3ZTlmN2RiZTQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMzdhZDhkYmMxZDlhNDgzOTg0ZDZmODE4MzI0NGQyOTQgPSAkKCc8ZGl2IGlkPSJodG1sXzM3YWQ4ZGJjMWQ5YTQ4Mzk4NGQ2ZjgxODMyNDRkMjk0IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5FcmluZ2F0ZSwgQmxvb3JkYWxlIEdhcmRlbnMsIE9sZCBCdXJuaGFtdGhvcnBlLCBNYXJrbGFuZCBXb29kPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8zZDZmMTNjNjg2MzU0NGI2ODA5ZDVlMzdlOWY3ZGJlNC5zZXRDb250ZW50KGh0bWxfMzdhZDhkYmMxZDlhNDgzOTg0ZDZmODE4MzI0NGQyOTQpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNDc2MjVjYjYzNTg4NDE1ZGE0ZGFjMTRjYzc5NzA5Y2EuYmluZFBvcHVwKHBvcHVwXzNkNmYxM2M2ODYzNTQ0YjY4MDlkNWUzN2U5ZjdkYmU0KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2FkMmVkNjA1YmJlMzQwZWNhNmJkOTVkNzdlMDMzN2NlID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzYzNTcyNiwtNzkuMTg4NzExNV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF81MzA0OThmM2RkOWY0MGM4YWE1NWYyZmZjOTY4NWI3YiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF83MjU0YjczZWVhYTg0MjJjYTQ1YmNlYzRlMDY4ZDVlNSA9ICQoJzxkaXYgaWQ9Imh0bWxfNzI1NGI3M2VlYWE4NDIyY2E0NWJjZWM0ZTA2OGQ1ZTUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkd1aWxkd29vZCwgTW9ybmluZ3NpZGUsIFdlc3QgSGlsbDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNTMwNDk4ZjNkZDlmNDBjOGFhNTVmMmZmYzk2ODViN2Iuc2V0Q29udGVudChodG1sXzcyNTRiNzNlZWFhODQyMmNhNDViY2VjNGUwNjhkNWU1KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2FkMmVkNjA1YmJlMzQwZWNhNmJkOTVkNzdlMDMzN2NlLmJpbmRQb3B1cChwb3B1cF81MzA0OThmM2RkOWY0MGM4YWE1NWYyZmZjOTY4NWI3Yik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl80YmM2MTZjMDcyZDE0ZGM4ODgxM2VkMGNmYzBhNzE2MCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY3NjM1NzM5OTk5OTk5LC03OS4yOTMwMzEyXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzljOGNmYWUzYjRkYTRjZjI5ZGEzYWI5ZDIyMGI4MjczID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzI2YWJlZmI0MDhjMjQ2ZTFhNDI4MTFkNTQ4NWFiMjNiID0gJCgnPGRpdiBpZD0iaHRtbF8yNmFiZWZiNDA4YzI0NmUxYTQyODExZDU0ODVhYjIzYiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+VGhlIEJlYWNoZXM8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzljOGNmYWUzYjRkYTRjZjI5ZGEzYWI5ZDIyMGI4MjczLnNldENvbnRlbnQoaHRtbF8yNmFiZWZiNDA4YzI0NmUxYTQyODExZDU0ODVhYjIzYik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl80YmM2MTZjMDcyZDE0ZGM4ODgxM2VkMGNmYzBhNzE2MC5iaW5kUG9wdXAocG9wdXBfOWM4Y2ZhZTNiNGRhNGNmMjlkYTNhYjlkMjIwYjgyNzMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZjY2YjVmNGQzMTQ1NGI0NGJiMDMzYWE0OWFmNTY3Y2IgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDQ3NzA3OTk5OTk5OTYsLTc5LjM3MzMwNjRdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfODQ3YmVjODE4Mzk0NDNhMmI5MTcxYzU3ODllYTdlNWYgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYjljZDU4OWMwMzQ3NDEzODgyYjRjZjQ5ZTk5OTRjYWIgPSAkKCc8ZGl2IGlkPSJodG1sX2I5Y2Q1ODljMDM0NzQxMzg4MmI0Y2Y0OWU5OTk0Y2FiIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5CZXJjenkgUGFyazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfODQ3YmVjODE4Mzk0NDNhMmI5MTcxYzU3ODllYTdlNWYuc2V0Q29udGVudChodG1sX2I5Y2Q1ODljMDM0NzQxMzg4MmI0Y2Y0OWU5OTk0Y2FiKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2Y2NmI1ZjRkMzE0NTRiNDRiYjAzM2FhNDlhZjU2N2NiLmJpbmRQb3B1cChwb3B1cF84NDdiZWM4MTgzOTQ0M2EyYjkxNzFjNTc4OWVhN2U1Zik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl81ZmQ5OTkyMWU0NzA0ZjJhYjkxYzIxNGMwMjNhZjUwNSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY4OTAyNTYsLTc5LjQ1MzUxMl0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF84ZTNiNjlhYWNkOWQ0NTljYWZiYjYzOTEwYTQyMGMwMiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8yNDYyZmNmNmM2NGI0NGNlYmQwZDAwNWVlNjVhMDUxMyA9ICQoJzxkaXYgaWQ9Imh0bWxfMjQ2MmZjZjZjNjRiNDRjZWJkMGQwMDVlZTY1YTA1MTMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNhbGVkb25pYS1GYWlyYmFua3M8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzhlM2I2OWFhY2Q5ZDQ1OWNhZmJiNjM5MTBhNDIwYzAyLnNldENvbnRlbnQoaHRtbF8yNDYyZmNmNmM2NGI0NGNlYmQwZDAwNWVlNjVhMDUxMyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl81ZmQ5OTkyMWU0NzA0ZjJhYjkxYzIxNGMwMjNhZjUwNS5iaW5kUG9wdXAocG9wdXBfOGUzYjY5YWFjZDlkNDU5Y2FmYmI2MzkxMGE0MjBjMDIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOGI3OTIxZjJjNTZhNDZkMTg2Mjg2ZTc4YzdhMDk5NWYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43NzA5OTIxLC03OS4yMTY5MTc0MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF85ZWY5ODc3OWQ3NjQ0ZWJjYWRlODgwNzYzNzI4NjU4NCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8yZWUwZGNkYjU1YWE0MzNiYjBmYzgzNjQ4MWEwNWQyMyA9ICQoJzxkaXYgaWQ9Imh0bWxfMmVlMGRjZGI1NWFhNDMzYmIwZmM4MzY0ODFhMDVkMjMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPldvYnVybjwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfOWVmOTg3NzlkNzY0NGViY2FkZTg4MDc2MzcyODY1ODQuc2V0Q29udGVudChodG1sXzJlZTBkY2RiNTVhYTQzM2JiMGZjODM2NDgxYTA1ZDIzKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzhiNzkyMWYyYzU2YTQ2ZDE4NjI4NmU3OGM3YTA5OTVmLmJpbmRQb3B1cChwb3B1cF85ZWY5ODc3OWQ3NjQ0ZWJjYWRlODgwNzYzNzI4NjU4NCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9lNWEzNWExMjMwYTg0N2M0YmE0MzQzZGYxYzg3NTJhZCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcwOTA2MDQsLTc5LjM2MzQ1MTddLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMWVmZDA2MjllZTRiNDQwMzllZjA3NjE2MDMxMjBmNDIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNDllYWMxMjFhMWEzNGIzYzk2NjNkNTVhY2RlZTZiZTUgPSAkKCc8ZGl2IGlkPSJodG1sXzQ5ZWFjMTIxYTFhMzRiM2M5NjYzZDU1YWNkZWU2YmU1IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5MZWFzaWRlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8xZWZkMDYyOWVlNGI0NDAzOWVmMDc2MTYwMzEyMGY0Mi5zZXRDb250ZW50KGh0bWxfNDllYWMxMjFhMWEzNGIzYzk2NjNkNTVhY2RlZTZiZTUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfZTVhMzVhMTIzMGE4NDdjNGJhNDM0M2RmMWM4NzUyYWQuYmluZFBvcHVwKHBvcHVwXzFlZmQwNjI5ZWU0YjQ0MDM5ZWYwNzYxNjAzMTIwZjQyKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzMzOTU1ODdmNWRmNjQ5MTdhMmExNDgyMGYxOGI1ZDg0ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjU3OTUyNCwtNzkuMzg3MzgyNl0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8zM2NiZjAyMTdkNjE0MWM5OGM4NzEwOTc3NGE4YWVmOCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9iZjhhZDVhYmQ0ZmU0N2Y2YTVjMGMyMzhmMGYwMTQ1OSA9ICQoJzxkaXYgaWQ9Imh0bWxfYmY4YWQ1YWJkNGZlNDdmNmE1YzBjMjM4ZjBmMDE0NTkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNlbnRyYWwgQmF5IFN0cmVldDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMzNjYmYwMjE3ZDYxNDFjOThjODcxMDk3NzRhOGFlZjguc2V0Q29udGVudChodG1sX2JmOGFkNWFiZDRmZTQ3ZjZhNWMwYzIzOGYwZjAxNDU5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzMzOTU1ODdmNWRmNjQ5MTdhMmExNDgyMGYxOGI1ZDg0LmJpbmRQb3B1cChwb3B1cF8zM2NiZjAyMTdkNjE0MWM5OGM4NzEwOTc3NGE4YWVmOCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9iYjAzZjk0MGEwOTI0Mzk3OTQ3ODYyZmE2YjM0ZDdhYSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY2OTU0MiwtNzkuNDIyNTYzN10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF81MzQyYjZjYTA3YWY0NTJiYjhmZWUyZTZkNGNjNjZjYyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9lOTQ2NjIzM2UyZGE0OTM0OGY5MDY3ZTlkZjEyYTc5YSA9ICQoJzxkaXYgaWQ9Imh0bWxfZTk0NjYyMzNlMmRhNDkzNDhmOTA2N2U5ZGYxMmE3OWEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNocmlzdGllPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF81MzQyYjZjYTA3YWY0NTJiYjhmZWUyZTZkNGNjNjZjYy5zZXRDb250ZW50KGh0bWxfZTk0NjYyMzNlMmRhNDkzNDhmOTA2N2U5ZGYxMmE3OWEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYmIwM2Y5NDBhMDkyNDM5Nzk0Nzg2MmZhNmIzNGQ3YWEuYmluZFBvcHVwKHBvcHVwXzUzNDJiNmNhMDdhZjQ1MmJiOGZlZTJlNmQ0Y2M2NmNjKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzM5ZWJmNDA0ZTc3OTQyNGViNzNlZGY2ZTAxYWQ3MjA0ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzczMTM2LC03OS4yMzk0NzYwOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF84Y2Q0NjIzNWQyY2M0MGQ2OWZiMmJhZTdjNTMxYjEzMiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9hOGQ4ZjNkNDUzMDA0YWI5YjA3NzczMDI1ZDhmMWVjNyA9ICQoJzxkaXYgaWQ9Imh0bWxfYThkOGYzZDQ1MzAwNGFiOWIwNzc3MzAyNWQ4ZjFlYzciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNlZGFyYnJhZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfOGNkNDYyMzVkMmNjNDBkNjlmYjJiYWU3YzUzMWIxMzIuc2V0Q29udGVudChodG1sX2E4ZDhmM2Q0NTMwMDRhYjliMDc3NzMwMjVkOGYxZWM3KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzM5ZWJmNDA0ZTc3OTQyNGViNzNlZGY2ZTAxYWQ3MjA0LmJpbmRQb3B1cChwb3B1cF84Y2Q0NjIzNWQyY2M0MGQ2OWZiMmJhZTdjNTMxYjEzMik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9hYjM4YzZmNjI4M2M0Y2YyODQyMmQwZjBlOWFkYTJmMSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjgwMzc2MjIsLTc5LjM2MzQ1MTddLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYTcxNDAxMzU3NjljNGZjOWE4OTM4Mzc0MTU1YWMxNjggPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNmY3ZWQxZWQwMmIyNGJjOWIxZTBjODI1MmU0ZjY2MDkgPSAkKCc8ZGl2IGlkPSJodG1sXzZmN2VkMWVkMDJiMjRiYzliMWUwYzgyNTJlNGY2NjA5IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5IaWxsY3Jlc3QgVmlsbGFnZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfYTcxNDAxMzU3NjljNGZjOWE4OTM4Mzc0MTU1YWMxNjguc2V0Q29udGVudChodG1sXzZmN2VkMWVkMDJiMjRiYzliMWUwYzgyNTJlNGY2NjA5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2FiMzhjNmY2MjgzYzRjZjI4NDIyZDBmMGU5YWRhMmYxLmJpbmRQb3B1cChwb3B1cF9hNzE0MDEzNTc2OWM0ZmM5YTg5MzgzNzQxNTVhYzE2OCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8zNzYxODhmNzU5MmU0NzBiYmYyNmYyZmM0Y2ZiODRmMSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc1NDMyODMsLTc5LjQ0MjI1OTNdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYTRiM2I0YmFhMDVjNDMxOWJlNGEyMzgwMzc4Y2FjNjIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMjY0NTEyMWRlNzI4NGI4YWE4MTgxNjZlMWE1YTQ0NGYgPSAkKCc8ZGl2IGlkPSJodG1sXzI2NDUxMjFkZTcyODRiOGFhODE4MTY2ZTFhNWE0NDRmIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5CYXRodXJzdCBNYW5vciwgV2lsc29uIEhlaWdodHMsIERvd25zdmlldyBOb3J0aDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfYTRiM2I0YmFhMDVjNDMxOWJlNGEyMzgwMzc4Y2FjNjIuc2V0Q29udGVudChodG1sXzI2NDUxMjFkZTcyODRiOGFhODE4MTY2ZTFhNWE0NDRmKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzM3NjE4OGY3NTkyZTQ3MGJiZjI2ZjJmYzRjZmI4NGYxLmJpbmRQb3B1cChwb3B1cF9hNGIzYjRiYWEwNWM0MzE5YmU0YTIzODAzNzhjYWM2Mik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl82ODIyZjA4ZWVhNjk0ZGRkYjY2MGNlMWJhYzM3ZmU5YSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcwNTM2ODksLTc5LjM0OTM3MTkwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzZiYzJhOGUxN2YzYTQwNzhhMDI4NTllMDNjMzJlOWIyID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2RlNWIyN2M3ZGYxZDQ2MTQ4ODU1ZDgwNDk0NzZmYmE5ID0gJCgnPGRpdiBpZD0iaHRtbF9kZTViMjdjN2RmMWQ0NjE0ODg1NWQ4MDQ5NDc2ZmJhOSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+VGhvcm5jbGlmZmUgUGFyazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNmJjMmE4ZTE3ZjNhNDA3OGEwMjg1OWUwM2MzMmU5YjIuc2V0Q29udGVudChodG1sX2RlNWIyN2M3ZGYxZDQ2MTQ4ODU1ZDgwNDk0NzZmYmE5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzY4MjJmMDhlZWE2OTRkZGRiNjYwY2UxYmFjMzdmZTlhLmJpbmRQb3B1cChwb3B1cF82YmMyYThlMTdmM2E0MDc4YTAyODU5ZTAzYzMyZTliMik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl85OTUzYWYyZDk3Mzg0MjgxYWJmOTcyYTgxYWNhNDdiNiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY1MDU3MTIwMDAwMDAxLC03OS4zODQ1Njc1XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzNiYzc5ODU3NTM2ZjQ2NjBiNDM5YzAwZmFmYWI4ZmJhID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzkxNjBhNjVkZjFlYjQwMmQ5OWRiNWRmYjhjMzZhMmJiID0gJCgnPGRpdiBpZD0iaHRtbF85MTYwYTY1ZGYxZWI0MDJkOTlkYjVkZmI4YzM2YTJiYiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+UmljaG1vbmQsIEFkZWxhaWRlLCBLaW5nPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8zYmM3OTg1NzUzNmY0NjYwYjQzOWMwMGZhZmFiOGZiYS5zZXRDb250ZW50KGh0bWxfOTE2MGE2NWRmMWViNDAyZDk5ZGI1ZGZiOGMzNmEyYmIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOTk1M2FmMmQ5NzM4NDI4MWFiZjk3MmE4MWFjYTQ3YjYuYmluZFBvcHVwKHBvcHVwXzNiYzc5ODU3NTM2ZjQ2NjBiNDM5YzAwZmFmYWI4ZmJhKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzQ3MjhhODQ2YmRlNjRiMjFiNjMyYzM3MGQ1NDk1NmI4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjY5MDA1MTAwMDAwMDEsLTc5LjQ0MjI1OTNdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfZjNlNjNhNGUzOTcyNDNiZGI4ZThlZDQ5NDU2MjJlYTkgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfODdjMGJhNDU5NTI2NGI1ZDhjNGIwYjJkN2RkMjMzNDIgPSAkKCc8ZGl2IGlkPSJodG1sXzg3YzBiYTQ1OTUyNjRiNWQ4YzRiMGIyZDdkZDIzMzQyIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5EdWZmZXJpbiwgRG92ZXJjb3VydCBWaWxsYWdlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9mM2U2M2E0ZTM5NzI0M2JkYjhlOGVkNDk0NTYyMmVhOS5zZXRDb250ZW50KGh0bWxfODdjMGJhNDU5NTI2NGI1ZDhjNGIwYjJkN2RkMjMzNDIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNDcyOGE4NDZiZGU2NGIyMWI2MzJjMzcwZDU0OTU2YjguYmluZFBvcHVwKHBvcHVwX2YzZTYzYTRlMzk3MjQzYmRiOGU4ZWQ0OTQ1NjIyZWE5KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2I3NzUxMjY2N2RlYTRkZTA4MzBmYmQ4Mzg1MjM2ZDU4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzQ0NzM0MiwtNzkuMjM5NDc2MDk5OTk5OTldLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMzQ0MzIwNzdjZDEyNGZjNjhlMjJjZDg3MGJlNzExNzkgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNjZkOTdjMTg4ZWI5NGI2YTk4Nzc5NjIzMGNiOTgzNGMgPSAkKCc8ZGl2IGlkPSJodG1sXzY2ZDk3YzE4OGViOTRiNmE5ODc3OTYyMzBjYjk4MzRjIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5TY2FyYm9yb3VnaCBWaWxsYWdlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8zNDQzMjA3N2NkMTI0ZmM2OGUyMmNkODcwYmU3MTE3OS5zZXRDb250ZW50KGh0bWxfNjZkOTdjMTg4ZWI5NGI2YTk4Nzc5NjIzMGNiOTgzNGMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYjc3NTEyNjY3ZGVhNGRlMDgzMGZiZDgzODUyMzZkNTguYmluZFBvcHVwKHBvcHVwXzM0NDMyMDc3Y2QxMjRmYzY4ZTIyY2Q4NzBiZTcxMTc5KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2IzMGQ0YmYzYzU4ODRlNmI5ZWUxOTNlNDJhY2VlYWE0ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzc4NTE3NSwtNzkuMzQ2NTU1N10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8wZjRjMjYzYmRhZDQ0ZjQ4YjViY2UyMDJmZGE1ZjkwMiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF81N2Y1MWE3Y2IwNzM0MmNmYWZlZDBkNzA1ODIzMDlkNiA9ICQoJzxkaXYgaWQ9Imh0bWxfNTdmNTFhN2NiMDczNDJjZmFmZWQwZDcwNTgyMzA5ZDYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkZhaXJ2aWV3LCBIZW5yeSBGYXJtLCBPcmlvbGU8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzBmNGMyNjNiZGFkNDRmNDhiNWJjZTIwMmZkYTVmOTAyLnNldENvbnRlbnQoaHRtbF81N2Y1MWE3Y2IwNzM0MmNmYWZlZDBkNzA1ODIzMDlkNik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9iMzBkNGJmM2M1ODg0ZTZiOWVlMTkzZTQyYWNlZWFhNC5iaW5kUG9wdXAocG9wdXBfMGY0YzI2M2JkYWQ0NGY0OGI1YmNlMjAyZmRhNWY5MDIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOGVkNTFlZWY5NDgzNDQxZDg2MGU3ODlkNjQwNjg1ZDkgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43Njc5ODAzLC03OS40ODcyNjE5MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iYTQyYzY1YzRkMjE0MDU0YjcwMGVhMDRlNzFhN2FmYSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9kYjYyZTJmNzA4ODc0ODVkYmU3NzY4YzUxMTZlMDQ1MiA9ICQoJzxkaXYgaWQ9Imh0bWxfZGI2MmUyZjcwODg3NDg1ZGJlNzc2OGM1MTE2ZTA0NTIiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk5vcnRod29vZCBQYXJrLCBZb3JrIFVuaXZlcnNpdHk8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2JhNDJjNjVjNGQyMTQwNTRiNzAwZWEwNGU3MWE3YWZhLnNldENvbnRlbnQoaHRtbF9kYjYyZTJmNzA4ODc0ODVkYmU3NzY4YzUxMTZlMDQ1Mik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84ZWQ1MWVlZjk0ODM0NDFkODYwZTc4OWQ2NDA2ODVkOS5iaW5kUG9wdXAocG9wdXBfYmE0MmM2NWM0ZDIxNDA1NGI3MDBlYTA0ZTcxYTdhZmEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZTdmOGU3NjFlNTczNGNmMGJjZmFmYjExYWZiZjk5ZDUgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42ODUzNDcsLTc5LjMzODEwNjVdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfNjFlMjliMTE1ZDFjNGQzZmE1ODI2MWJiMGUzODI3N2MgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMDVjNTMxNzg0OTdhNDE4MDhlMTA2MTk5YjI1MWJkMDYgPSAkKCc8ZGl2IGlkPSJodG1sXzA1YzUzMTc4NDk3YTQxODA4ZTEwNjE5OWIyNTFiZDA2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5FYXN0IFRvcm9udG8sIEJyb2FkdmlldyBOb3J0aCAoT2xkIEVhc3QgWW9yayk8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzYxZTI5YjExNWQxYzRkM2ZhNTgyNjFiYjBlMzgyNzdjLnNldENvbnRlbnQoaHRtbF8wNWM1MzE3ODQ5N2E0MTgwOGUxMDYxOTliMjUxYmQwNik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9lN2Y4ZTc2MWU1NzM0Y2YwYmNmYWZiMTFhZmJmOTlkNS5iaW5kUG9wdXAocG9wdXBfNjFlMjliMTE1ZDFjNGQzZmE1ODI2MWJiMGUzODI3N2MpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNGVmMDYzMmY2OWQ3NGMyOTllMDdiMjE4NjNkNzk2YjggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDA4MTU3LC03OS4zODE3NTIyOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iZWY4ZTY1OTFmYzU0YWE2OGNlZDQwZTE3YmIwYmRjOCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF83NDFiMzIzMjUyZDU0YTc2OGVjN2M0NDEzN2EwOTRkOSA9ICQoJzxkaXYgaWQ9Imh0bWxfNzQxYjMyMzI1MmQ1NGE3NjhlYzdjNDQxMzdhMDk0ZDkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkhhcmJvdXJmcm9udCBFYXN0LCBVbmlvbiBTdGF0aW9uLCBUb3JvbnRvIElzbGFuZHM8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2JlZjhlNjU5MWZjNTRhYTY4Y2VkNDBlMTdiYjBiZGM4LnNldENvbnRlbnQoaHRtbF83NDFiMzIzMjUyZDU0YTc2OGVjN2M0NDEzN2EwOTRkOSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl80ZWYwNjMyZjY5ZDc0YzI5OWUwN2IyMTg2M2Q3OTZiOC5iaW5kUG9wdXAocG9wdXBfYmVmOGU2NTkxZmM1NGFhNjhjZWQ0MGUxN2JiMGJkYzgpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYzZjMDFlMmRkMzM3NDFlYmJhNTYyYTQxMGZkNmFmODUgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDc5MjY3MDAwMDAwMDYsLTc5LjQxOTc0OTddLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMjg3MTVmYzMwMTcxNGJkNGI3YjY3N2NmNGJkZmJkNWQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMmRmMDJmNTA5NTIyNGRiNTk5M2ZmMjNiNDA0M2E4MzcgPSAkKCc8ZGl2IGlkPSJodG1sXzJkZjAyZjUwOTUyMjRkYjU5OTNmZjIzYjQwNDNhODM3IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5MaXR0bGUgUG9ydHVnYWwsIFRyaW5pdHk8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzI4NzE1ZmMzMDE3MTRiZDRiN2I2NzdjZjRiZGZiZDVkLnNldENvbnRlbnQoaHRtbF8yZGYwMmY1MDk1MjI0ZGI1OTkzZmYyM2I0MDQzYTgzNyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9jNmMwMWUyZGQzMzc0MWViYmE1NjJhNDEwZmQ2YWY4NS5iaW5kUG9wdXAocG9wdXBfMjg3MTVmYzMwMTcxNGJkNGI3YjY3N2NmNGJkZmJkNWQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZDMxMDAyMTNjNmE3NGQ4ZTg3MmI2NDQ5NDM3NGU1ODggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43Mjc5MjkyLC03OS4yNjIwMjk0MDAwMDAwMl0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF81NjAwNzVkYmE3NWM0MjY2ODQ0MDgxODg5MmVmMmJkMSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8yMGY5NTJjZmUyNjk0ZjBlOGY3ZjBjMWYyNDc5NmVmYyA9ICQoJzxkaXYgaWQ9Imh0bWxfMjBmOTUyY2ZlMjY5NGYwZThmN2YwYzFmMjQ3OTZlZmMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPktlbm5lZHkgUGFyaywgSW9udmlldywgRWFzdCBCaXJjaG1vdW50IFBhcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzU2MDA3NWRiYTc1YzQyNjY4NDQwODE4ODkyZWYyYmQxLnNldENvbnRlbnQoaHRtbF8yMGY5NTJjZmUyNjk0ZjBlOGY3ZjBjMWYyNDc5NmVmYyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9kMzEwMDIxM2M2YTc0ZDhlODcyYjY0NDk0Mzc0ZTU4OC5iaW5kUG9wdXAocG9wdXBfNTYwMDc1ZGJhNzVjNDI2Njg0NDA4MTg4OTJlZjJiZDEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMDY1MWY2MGQ1ZjhlNDkzZWE4NWQzZTQyMWZkMzgzODAgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43ODY5NDczLC03OS4zODU5NzVdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMWI4MGUwZTE0NjI1NGRmN2I4NjcyMGYzZmZlOWFmOGQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMmQzZjhmYTc3MTI5NDAzNDk4NDk3ZWRiOGI5OGVlOWQgPSAkKCc8ZGl2IGlkPSJodG1sXzJkM2Y4ZmE3NzEyOTQwMzQ5ODQ5N2VkYjhiOThlZTlkIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5CYXl2aWV3IFZpbGxhZ2U8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzFiODBlMGUxNDYyNTRkZjdiODY3MjBmM2ZmZTlhZjhkLnNldENvbnRlbnQoaHRtbF8yZDNmOGZhNzcxMjk0MDM0OTg0OTdlZGI4Yjk4ZWU5ZCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8wNjUxZjYwZDVmOGU0OTNlYTg1ZDNlNDIxZmQzODM4MC5iaW5kUG9wdXAocG9wdXBfMWI4MGUwZTE0NjI1NGRmN2I4NjcyMGYzZmZlOWFmOGQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOTdhN2IwZDIzYTI2NDcwOTk2MDM1MmVhZmZlMzU1YWIgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43Mzc0NzMyMDAwMDAwMDQsLTc5LjQ2NDc2MzI5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzUyNDEwMzU0MWNmNjRmZTBhODE3YzE5Njg3ZjZhYzBkID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2I3ZWQwZDFmYWY5YjQ4ODRiMGYxZWI2MzBmM2IxODc0ID0gJCgnPGRpdiBpZD0iaHRtbF9iN2VkMGQxZmFmOWI0ODg0YjBmMWViNjMwZjNiMTg3NCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RG93bnN2aWV3PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF81MjQxMDM1NDFjZjY0ZmUwYTgxN2MxOTY4N2Y2YWMwZC5zZXRDb250ZW50KGh0bWxfYjdlZDBkMWZhZjliNDg4NGIwZjFlYjYzMGYzYjE4NzQpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfOTdhN2IwZDIzYTI2NDcwOTk2MDM1MmVhZmZlMzU1YWIuYmluZFBvcHVwKHBvcHVwXzUyNDEwMzU0MWNmNjRmZTBhODE3YzE5Njg3ZjZhYzBkKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzYzMjFhMmRkZTU3NTQ1NGM4YmE5MzhjYzU3ODc2MGE4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjc5NTU3MSwtNzkuMzUyMTg4XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2RjOWZkNWI0YmY0YTRhZDk4YjM5M2FiNDYxYTM3YTdlID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzVlNmU3MTI1MTE4YzQxNzc4ZjhiMDY1Y2FiNjI1NWJhID0gJCgnPGRpdiBpZD0iaHRtbF81ZTZlNzEyNTExOGM0MTc3OGY4YjA2NWNhYjYyNTViYSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+VGhlIERhbmZvcnRoIFdlc3QsIFJpdmVyZGFsZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZGM5ZmQ1YjRiZjRhNGFkOThiMzkzYWI0NjFhMzdhN2Uuc2V0Q29udGVudChodG1sXzVlNmU3MTI1MTE4YzQxNzc4ZjhiMDY1Y2FiNjI1NWJhKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzYzMjFhMmRkZTU3NTQ1NGM4YmE5MzhjYzU3ODc2MGE4LmJpbmRQb3B1cChwb3B1cF9kYzlmZDViNGJmNGE0YWQ5OGIzOTNhYjQ2MWEzN2E3ZSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9iNTM5N2I2NTAyNTk0NGVlODUxM2QxNWQxZmUwZDc4MCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY0NzE3NjgsLTc5LjM4MTU3NjQwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2RhN2MyM2FkYTNmMjQ3NTM4ZTk2NzQ2N2ZjMDhhYzYzID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzI0MjQ3ODMxMjlkNjQ4MzdiY2M5MDFiNGU0Yjc5MTFhID0gJCgnPGRpdiBpZD0iaHRtbF8yNDI0NzgzMTI5ZDY0ODM3YmNjOTAxYjRlNGI3OTExYSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+VG9yb250byBEb21pbmlvbiBDZW50cmUsIERlc2lnbiBFeGNoYW5nZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfZGE3YzIzYWRhM2YyNDc1MzhlOTY3NDY3ZmMwOGFjNjMuc2V0Q29udGVudChodG1sXzI0MjQ3ODMxMjlkNjQ4MzdiY2M5MDFiNGU0Yjc5MTFhKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2I1Mzk3YjY1MDI1OTQ0ZWU4NTEzZDE1ZDFmZTBkNzgwLmJpbmRQb3B1cChwb3B1cF9kYTdjMjNhZGEzZjI0NzUzOGU5Njc0NjdmYzA4YWM2Myk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9hYjFjZGM5MGZhMmM0OGQ1YTc1MjFkNjdkMmUzMjg0OSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjYzNjg0NzIsLTc5LjQyODE5MTQwMDAwMDAyXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzFkNzQ2MzQ3N2U4NDQxMTA4OTk5ZWM0MjA0ZTAxMGZjID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzI5YmUxZTI5ZTZkMTQzMTg4NDZkZmMwNTc2OTQ0Y2U1ID0gJCgnPGRpdiBpZD0iaHRtbF8yOWJlMWUyOWU2ZDE0MzE4ODQ2ZGZjMDU3Njk0NGNlNSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QnJvY2t0b24sIFBhcmtkYWxlIFZpbGxhZ2UsIEV4aGliaXRpb24gUGxhY2U8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzFkNzQ2MzQ3N2U4NDQxMTA4OTk5ZWM0MjA0ZTAxMGZjLnNldENvbnRlbnQoaHRtbF8yOWJlMWUyOWU2ZDE0MzE4ODQ2ZGZjMDU3Njk0NGNlNSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9hYjFjZGM5MGZhMmM0OGQ1YTc1MjFkNjdkMmUzMjg0OS5iaW5kUG9wdXAocG9wdXBfMWQ3NDYzNDc3ZTg0NDExMDg5OTllYzQyMDRlMDEwZmMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMzA1ZjNiMTgzMDI4NGE4NDlhNzAxYWY2NTdhNjM3OWIgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MTExMTE3MDAwMDAwMDQsLTc5LjI4NDU3NzJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfZmMxNDQxNTU2YWE1NGZjOTgzNWUwMWQzMzZhZWI4ZTIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZTZhMTllODZhOWJlNDAwMzk1ZTAxY2VlYjM1MzFkOTEgPSAkKCc8ZGl2IGlkPSJodG1sX2U2YTE5ZTg2YTliZTQwMDM5NWUwMWNlZWIzNTMxZDkxIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Hb2xkZW4gTWlsZSwgQ2xhaXJsZWEsIE9ha3JpZGdlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9mYzE0NDE1NTZhYTU0ZmM5ODM1ZTAxZDMzNmFlYjhlMi5zZXRDb250ZW50KGh0bWxfZTZhMTllODZhOWJlNDAwMzk1ZTAxY2VlYjM1MzFkOTEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMzA1ZjNiMTgzMDI4NGE4NDlhNzAxYWY2NTdhNjM3OWIuYmluZFBvcHVwKHBvcHVwX2ZjMTQ0MTU1NmFhNTRmYzk4MzVlMDFkMzM2YWViOGUyKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzc2ZGFiZDBlNjNhYzRlYWZiN2QwZDUxODhjOTg3MTEzID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzU3NDkwMiwtNzkuMzc0NzE0MDk5OTk5OTldLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYjVlNmE5Y2UxZWFjNDQ4NGIzYmU2ZDRlMTllNWYxNDkgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfODkzZDRiYWJhMzQwNGY4ZWFhNDI3MDg4YzUwZDhiMTIgPSAkKCc8ZGl2IGlkPSJodG1sXzg5M2Q0YmFiYTM0MDRmOGVhYTQyNzA4OGM1MGQ4YjEyIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Zb3JrIE1pbGxzLCBTaWx2ZXIgSGlsbHM8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2I1ZTZhOWNlMWVhYzQ0ODRiM2JlNmQ0ZTE5ZTVmMTQ5LnNldENvbnRlbnQoaHRtbF84OTNkNGJhYmEzNDA0ZjhlYWE0MjcwODhjNTBkOGIxMik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl83NmRhYmQwZTYzYWM0ZWFmYjdkMGQ1MTg4Yzk4NzExMy5iaW5kUG9wdXAocG9wdXBfYjVlNmE5Y2UxZWFjNDQ4NGIzYmU2ZDRlMTllNWYxNDkpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZTdjZTVhMGVhNmY3NDU5Yjk2NGM5MWFjMGJiODAyZTAgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MzkwMTQ2LC03OS41MDY5NDM2XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2MxZDk5ZWUzZDJjYTQwNzU4Y2FjM2Q5Yzk2NWJlNmUxID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzg0ZjNlOGI1MzJkODQxYmZhZWM3Y2U5MzQwZTU3OGVlID0gJCgnPGRpdiBpZD0iaHRtbF84NGYzZThiNTMyZDg0MWJmYWVjN2NlOTM0MGU1NzhlZSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RG93bnN2aWV3PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9jMWQ5OWVlM2QyY2E0MDc1OGNhYzNkOWM5NjViZTZlMS5zZXRDb250ZW50KGh0bWxfODRmM2U4YjUzMmQ4NDFiZmFlYzdjZTkzNDBlNTc4ZWUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfZTdjZTVhMGVhNmY3NDU5Yjk2NGM5MWFjMGJiODAyZTAuYmluZFBvcHVwKHBvcHVwX2MxZDk5ZWUzZDJjYTQwNzU4Y2FjM2Q5Yzk2NWJlNmUxKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2FlZjVkMGIzYTczYjQxMzhiMmNiYzMyYzI2YTM5MDQzID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjY4OTk4NSwtNzkuMzE1NTcxNTk5OTk5OThdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYzg5NzdmMTMzNmU2NDhmNzk1MTFhY2IwYzIzMDc0MzIgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNzhjNWY5ZDBjMzliNGRiYzk3ZDI2ZTdhNGM2MGQzM2YgPSAkKCc8ZGl2IGlkPSJodG1sXzc4YzVmOWQwYzM5YjRkYmM5N2QyNmU3YTRjNjBkMzNmIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5JbmRpYSBCYXphYXIsIFRoZSBCZWFjaGVzIFdlc3Q8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2M4OTc3ZjEzMzZlNjQ4Zjc5NTExYWNiMGMyMzA3NDMyLnNldENvbnRlbnQoaHRtbF83OGM1ZjlkMGMzOWI0ZGJjOTdkMjZlN2E0YzYwZDMzZik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9hZWY1ZDBiM2E3M2I0MTM4YjJjYmMzMmMyNmEzOTA0My5iaW5kUG9wdXAocG9wdXBfYzg5NzdmMTMzNmU2NDhmNzk1MTFhY2IwYzIzMDc0MzIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMzg5ZmUxYTE2MzQyNGQ0OTg5MThmMGQzZjIyYWE3NmEgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDgxOTg1LC03OS4zNzk4MTY5MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9jNTI1M2U5N2ZmMmU0Y2UyOTA5YjgyOGRjZTRlOTlmYiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8xY2FlMWZhMjZhYTc0MmU0YjU5ODc2ODU1YjMzNTQ4ZiA9ICQoJzxkaXYgaWQ9Imh0bWxfMWNhZTFmYTI2YWE3NDJlNGI1OTg3Njg1NWIzMzU0OGYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNvbW1lcmNlIENvdXJ0LCBWaWN0b3JpYSBIb3RlbDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfYzUyNTNlOTdmZjJlNGNlMjkwOWI4MjhkY2U0ZTk5ZmIuc2V0Q29udGVudChodG1sXzFjYWUxZmEyNmFhNzQyZTRiNTk4NzY4NTViMzM1NDhmKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzM4OWZlMWExNjM0MjRkNDk4OTE4ZjBkM2YyMmFhNzZhLmJpbmRQb3B1cChwb3B1cF9jNTI1M2U5N2ZmMmU0Y2UyOTA5YjgyOGRjZTRlOTlmYik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl85MjRhYjIyNGM1OTc0ZDY2OTBkOGNmOTI4ZGRmYTY2NyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcxMzc1NjIwMDAwMDAwNiwtNzkuNDkwMDczOF0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9mNTgzNzNjYmY1MmI0NTFlOGQ1MTQxMzliMjgwZTYyMiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9lY2FiYmFjNmQwZmU0NzI0YTRjZTJiNjg0NjlkMmNkZiA9ICQoJzxkaXYgaWQ9Imh0bWxfZWNhYmJhYzZkMGZlNDcyNGE0Y2UyYjY4NDY5ZDJjZGYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk5vcnRoIFBhcmssIE1hcGxlIExlYWYgUGFyaywgVXB3b29kIFBhcms8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2Y1ODM3M2NiZjUyYjQ1MWU4ZDUxNDEzOWIyODBlNjIyLnNldENvbnRlbnQoaHRtbF9lY2FiYmFjNmQwZmU0NzI0YTRjZTJiNjg0NjlkMmNkZik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl85MjRhYjIyNGM1OTc0ZDY2OTBkOGNmOTI4ZGRmYTY2Ny5iaW5kUG9wdXAocG9wdXBfZjU4MzczY2JmNTJiNDUxZThkNTE0MTM5YjI4MGU2MjIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNzIxNTBlYWVjNzJkNDI0NWExNzRhYmYxNmUxMjVkYjEgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43NTYzMDMzLC03OS41NjU5NjMyOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9lNTMzYWY2YTQxYWY0ODMzODI3YjAyZTc1NzFhMmQ5YyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF82YjkwMTNlY2Y4M2U0MDM4ODA3MjMwYjU3MDA0MmFmYSA9ICQoJzxkaXYgaWQ9Imh0bWxfNmI5MDEzZWNmODNlNDAzODgwNzIzMGI1NzAwNDJhZmEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkh1bWJlciBTdW1taXQ8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2U1MzNhZjZhNDFhZjQ4MzM4MjdiMDJlNzU3MWEyZDljLnNldENvbnRlbnQoaHRtbF82YjkwMTNlY2Y4M2U0MDM4ODA3MjMwYjU3MDA0MmFmYSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl83MjE1MGVhZWM3MmQ0MjQ1YTE3NGFiZjE2ZTEyNWRiMS5iaW5kUG9wdXAocG9wdXBfZTUzM2FmNmE0MWFmNDgzMzgyN2IwMmU3NTcxYTJkOWMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNGZhNGM1MDI0NmExNDkwMjgyMzY5ZmNkMjU3Nzg5OWEgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MTYzMTYsLTc5LjIzOTQ3NjA5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2RmZjI5MTBhYjAzNjRmZjI5MjFhMWE5NDlmZmJhYmIyID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2MxOGQxYWQ0YmU3ZTQyZTBhNTI3MjY1MDU1YWY0N2VhID0gJCgnPGRpdiBpZD0iaHRtbF9jMThkMWFkNGJlN2U0MmUwYTUyNzI2NTA1NWFmNDdlYSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Q2xpZmZzaWRlLCBDbGlmZmNyZXN0LCBTY2FyYm9yb3VnaCBWaWxsYWdlIFdlc3Q8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2RmZjI5MTBhYjAzNjRmZjI5MjFhMWE5NDlmZmJhYmIyLnNldENvbnRlbnQoaHRtbF9jMThkMWFkNGJlN2U0MmUwYTUyNzI2NTA1NWFmNDdlYSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl80ZmE0YzUwMjQ2YTE0OTAyODIzNjlmY2QyNTc3ODk5YS5iaW5kUG9wdXAocG9wdXBfZGZmMjkxMGFiMDM2NGZmMjkyMWExYTk0OWZmYmFiYjIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMGJhN2U5ZmZlZjk3NGRiYzgxZmVlNjM1YTkyOGVhM2IgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43ODkwNTMsLTc5LjQwODQ5Mjc5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzJmMzYwMWQ4OWY5YzQ4MDJiMzI3ZTNiMzU0MjJiZGYwID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzIyZTcxOWRiYjQxMjQzZmY5MzQxZDQ0NjBiMGNmOTZiID0gJCgnPGRpdiBpZD0iaHRtbF8yMmU3MTlkYmI0MTI0M2ZmOTM0MWQ0NDYwYjBjZjk2YiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V2lsbG93ZGFsZSwgTmV3dG9uYnJvb2s8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzJmMzYwMWQ4OWY5YzQ4MDJiMzI3ZTNiMzU0MjJiZGYwLnNldENvbnRlbnQoaHRtbF8yMmU3MTlkYmI0MTI0M2ZmOTM0MWQ0NDYwYjBjZjk2Yik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8wYmE3ZTlmZmVmOTc0ZGJjODFmZWU2MzVhOTI4ZWEzYi5iaW5kUG9wdXAocG9wdXBfMmYzNjAxZDg5ZjljNDgwMmIzMjdlM2IzNTQyMmJkZjApOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfOTFkZGE0ZTA5ZDI5NGZjYTg4MzE2YjM0ZjExZDJlM2EgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43Mjg0OTY0LC03OS40OTU2OTc0MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF82YTRkMTRiMmY3ZjE0MTY4ODhlYTA2YjQwYzA4ZWJjZiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8yMDcxOTY4ZTU5MzQ0NjI3OTEzZWU2YjBjMGFmOTIwOCA9ICQoJzxkaXYgaWQ9Imh0bWxfMjA3MTk2OGU1OTM0NDYyNzkxM2VlNmIwYzBhZjkyMDgiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRvd25zdmlldzwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNmE0ZDE0YjJmN2YxNDE2ODg4ZWEwNmI0MGMwOGViY2Yuc2V0Q29udGVudChodG1sXzIwNzE5NjhlNTkzNDQ2Mjc5MTNlZTZiMGMwYWY5MjA4KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzkxZGRhNGUwOWQyOTRmY2E4ODMxNmIzNGYxMWQyZTNhLmJpbmRQb3B1cChwb3B1cF82YTRkMTRiMmY3ZjE0MTY4ODhlYTA2YjQwYzA4ZWJjZik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9kYjkzNzJmOGNjOTE0YzY2YjI2MWM5MjdmOWIzNjc3ZSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY1OTUyNTUsLTc5LjM0MDkyM10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9jYjg1MjhkNmNlOGU0M2YzODg1ODBjZGFkYzE1ZWNmMyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9kNGI3MGVmMTE0N2Q0ZjIwYTBkNTg4NzhmYmNhZTQyNSA9ICQoJzxkaXYgaWQ9Imh0bWxfZDRiNzBlZjExNDdkNGYyMGEwZDU4ODc4ZmJjYWU0MjUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlN0dWRpbyBEaXN0cmljdDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfY2I4NTI4ZDZjZThlNDNmMzg4NTgwY2RhZGMxNWVjZjMuc2V0Q29udGVudChodG1sX2Q0YjcwZWYxMTQ3ZDRmMjBhMGQ1ODg3OGZiY2FlNDI1KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2RiOTM3MmY4Y2M5MTRjNjZiMjYxYzkyN2Y5YjM2NzdlLmJpbmRQb3B1cChwb3B1cF9jYjg1MjhkNmNlOGU0M2YzODg1ODBjZGFkYzE1ZWNmMyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl80NzZlMWRiOGExMzA0MDg0YmZkZDJjMDk1NDAyYWI1NyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjczMzI4MjUsLTc5LjQxOTc0OTddLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfOWU0NDNhNjI4ZWFkNDYyOWJlOTkzYTFhOTVmMzRlMjggPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMjgwNGMwZGRhYmRmNDYxYjhmM2Q1ZjBkNjBlYzU1NmYgPSAkKCc8ZGl2IGlkPSJodG1sXzI4MDRjMGRkYWJkZjQ2MWI4ZjNkNWYwZDYwZWM1NTZmIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5CZWRmb3JkIFBhcmssIExhd3JlbmNlIE1hbm9yIEVhc3Q8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzllNDQzYTYyOGVhZDQ2MjliZTk5M2ExYTk1ZjM0ZTI4LnNldENvbnRlbnQoaHRtbF8yODA0YzBkZGFiZGY0NjFiOGYzZDVmMGQ2MGVjNTU2Zik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl80NzZlMWRiOGExMzA0MDg0YmZkZDJjMDk1NDAyYWI1Ny5iaW5kUG9wdXAocG9wdXBfOWU0NDNhNjI4ZWFkNDYyOWJlOTkzYTFhOTVmMzRlMjgpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYjBkZjA1YmQxYThiNDNjMWIyYTNkOWQzMzgxOTA3N2EgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42OTExMTU4LC03OS40NzYwMTMyOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF82MDMzZDE0N2YzMzQ0OGU0OWUxMjc2NzAxNjE2ZmY0NiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84YzIwYzUyYzJlMmE0YzZmYWM1YjBjZGU5Yzc3OThjNiA9ICQoJzxkaXYgaWQ9Imh0bWxfOGMyMGM1MmMyZTJhNGM2ZmFjNWIwY2RlOWM3Nzk4YzYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRlbCBSYXksIE1vdW50IERlbm5pcywgS2VlbHNkYWxlIGFuZCBTaWx2ZXJ0aG9ybjwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNjAzM2QxNDdmMzM0NDhlNDllMTI3NjcwMTYxNmZmNDYuc2V0Q29udGVudChodG1sXzhjMjBjNTJjMmUyYTRjNmZhYzViMGNkZTljNzc5OGM2KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2IwZGYwNWJkMWE4YjQzYzFiMmEzZDlkMzM4MTkwNzdhLmJpbmRQb3B1cChwb3B1cF82MDMzZDE0N2YzMzQ0OGU0OWUxMjc2NzAxNjE2ZmY0Nik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9jZmI1MTMxN2Y4ZWY0OGU5OTE3YmUwMjM1ODg4ZWFjOSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcyNDc2NTksLTc5LjUzMjI0MjQwMDAwMDAyXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2IwMTZjOWY3ZDQ3MTQ0OTU4NzkxMzRhOTA5ZmE3ZmVmID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2M4ZDA4Mzc2OTFmODQwNWM5ZmQ4OWRjNjM0ZmRlOGM5ID0gJCgnPGRpdiBpZD0iaHRtbF9jOGQwODM3NjkxZjg0MDVjOWZkODlkYzYzNGZkZThjOSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+SHVtYmVybGVhLCBFbWVyeTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfYjAxNmM5ZjdkNDcxNDQ5NTg3OTEzNGE5MDlmYTdmZWYuc2V0Q29udGVudChodG1sX2M4ZDA4Mzc2OTFmODQwNWM5ZmQ4OWRjNjM0ZmRlOGM5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2NmYjUxMzE3ZjhlZjQ4ZTk5MTdiZTAyMzU4ODhlYWM5LmJpbmRQb3B1cChwb3B1cF9iMDE2YzlmN2Q0NzE0NDk1ODc5MTM0YTkwOWZhN2ZlZik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8yNThlY2UxNmRmNTA0YzhlOGViNDU2OTQ3Y2UyZGQyOCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY5MjY1NzAwMDAwMDAwNCwtNzkuMjY0ODQ4MV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8yYTZiNjNhMDljMmY0MjVkYWVjZGUyODk2NDZiYTYyNyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF85YzY2ODY0MjQ0ZTk0MzVmYmRmYmE2MTJhZTM4ZWIxOSA9ICQoJzxkaXYgaWQ9Imh0bWxfOWM2Njg2NDI0NGU5NDM1ZmJkZmJhNjEyYWUzOGViMTkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkJpcmNoIENsaWZmLCBDbGlmZnNpZGUgV2VzdDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMmE2YjYzYTA5YzJmNDI1ZGFlY2RlMjg5NjQ2YmE2Mjcuc2V0Q29udGVudChodG1sXzljNjY4NjQyNDRlOTQzNWZiZGZiYTYxMmFlMzhlYjE5KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzI1OGVjZTE2ZGY1MDRjOGU4ZWI0NTY5NDdjZTJkZDI4LmJpbmRQb3B1cChwb3B1cF8yYTZiNjNhMDljMmY0MjVkYWVjZGUyODk2NDZiYTYyNyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8zODY4YzhjNDM3ZWI0N2ZhOWMxMzljNGJlNjdmNGY2MCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc3MDExOTksLTc5LjQwODQ5Mjc5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzM0NDVkZjhhYzc3MDRlMjFhODRjNjVlNzZmYzRiMDA1ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzVkMDYwOWNhYjY0ZTRjNTBiNGZhZWJmMDZiOGY3OTAzID0gJCgnPGRpdiBpZD0iaHRtbF81ZDA2MDljYWI2NGU0YzUwYjRmYWViZjA2YjhmNzkwMyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V2lsbG93ZGFsZSwgV2lsbG93ZGFsZSBFYXN0PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8zNDQ1ZGY4YWM3NzA0ZTIxYTg0YzY1ZTc2ZmM0YjAwNS5zZXRDb250ZW50KGh0bWxfNWQwNjA5Y2FiNjRlNGM1MGI0ZmFlYmYwNmI4Zjc5MDMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMzg2OGM4YzQzN2ViNDdmYTljMTM5YzRiZTY3ZjRmNjAuYmluZFBvcHVwKHBvcHVwXzM0NDVkZjhhYzc3MDRlMjFhODRjNjVlNzZmYzRiMDA1KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzhkMDYwYzFmOWM0ZTQ5M2JiZjViMTI0MjMxMjY2MTdhID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzYxNjMxMywtNzkuNTIwOTk5NDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYzNhZTFkZjQ4YmJlNDFiZWIzMjZiNGQ2ZjgyYTI3NzUgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMzQzOTQ2YjdhYWFmNDQxMTlkODRmNWFjMGJmNDhlNGYgPSAkKCc8ZGl2IGlkPSJodG1sXzM0Mzk0NmI3YWFhZjQ0MTE5ZDg0ZjVhYzBiZjQ4ZTRmIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Eb3duc3ZpZXc8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2MzYWUxZGY0OGJiZTQxYmViMzI2YjRkNmY4MmEyNzc1LnNldENvbnRlbnQoaHRtbF8zNDM5NDZiN2FhYWY0NDExOWQ4NGY1YWMwYmY0OGU0Zik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84ZDA2MGMxZjljNGU0OTNiYmY1YjEyNDIzMTI2NjE3YS5iaW5kUG9wdXAocG9wdXBfYzNhZTFkZjQ4YmJlNDFiZWIzMjZiNGQ2ZjgyYTI3NzUpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZjNkOTgxNDQyZDNiNGQzNThhMDk2ZDdmODFlMDYyYzggPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MjgwMjA1LC03OS4zODg3OTAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzg3MTRiNmE5YzE0ZjRmYmY5N2IxYWE1MzUyYjI1OWY3ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2I0MzEwZTlkMmE2YzQ5Mjg5MzVhZmZhNTRlOGRiNWFjID0gJCgnPGRpdiBpZD0iaHRtbF9iNDMxMGU5ZDJhNmM0OTI4OTM1YWZmYTU0ZThkYjVhYyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TGF3cmVuY2UgUGFyazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfODcxNGI2YTljMTRmNGZiZjk3YjFhYTUzNTJiMjU5Zjcuc2V0Q29udGVudChodG1sX2I0MzEwZTlkMmE2YzQ5Mjg5MzVhZmZhNTRlOGRiNWFjKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2YzZDk4MTQ0MmQzYjRkMzU4YTA5NmQ3ZjgxZTA2MmM4LmJpbmRQb3B1cChwb3B1cF84NzE0YjZhOWMxNGY0ZmJmOTdiMWFhNTM1MmIyNTlmNyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9lNTZkZWQ5OWU2ZmE0ZWJmYjRhMTE3N2VlZmI1MDY1YyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcxMTY5NDgsLTc5LjQxNjkzNTU5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2RmZWU1NjFhY2E5ODRkNjU4Mzg5YzM0ZmMyODZmY2IwID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzg4NjdlMzYzMjM2ODQzOTg4ODlhMWFkOWMzNzZjMjBmID0gJCgnPGRpdiBpZD0iaHRtbF84ODY3ZTM2MzIzNjg0Mzk4ODg5YTFhZDljMzc2YzIwZiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Um9zZWxhd248L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2RmZWU1NjFhY2E5ODRkNjU4Mzg5YzM0ZmMyODZmY2IwLnNldENvbnRlbnQoaHRtbF84ODY3ZTM2MzIzNjg0Mzk4ODg5YTFhZDljMzc2YzIwZik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9lNTZkZWQ5OWU2ZmE0ZWJmYjRhMTE3N2VlZmI1MDY1Yy5iaW5kUG9wdXAocG9wdXBfZGZlZTU2MWFjYTk4NGQ2NTgzODljMzRmYzI4NmZjYjApOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMzAxYjdmYmMxNjM2NDNkMTk3YjU4YzRlZTlhODQxOGYgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NzMxODUyOTk5OTk5OSwtNzkuNDg3MjYxOTAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfY2Q1OTRhYmNkM2ZjNDU4MDgwM2YzMTBjMTRkNjQ5MjQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYWZkM2IzNDc3MGMzNGExZTg3YWU5OGE2N2RkNjVlZDQgPSAkKCc8ZGl2IGlkPSJodG1sX2FmZDNiMzQ3NzBjMzRhMWU4N2FlOThhNjdkZDY1ZWQ0IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5SdW5ueW1lZGUsIFRoZSBKdW5jdGlvbiBOb3J0aDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfY2Q1OTRhYmNkM2ZjNDU4MDgwM2YzMTBjMTRkNjQ5MjQuc2V0Q29udGVudChodG1sX2FmZDNiMzQ3NzBjMzRhMWU4N2FlOThhNjdkZDY1ZWQ0KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzMwMWI3ZmJjMTYzNjQzZDE5N2I1OGM0ZWU5YTg0MThmLmJpbmRQb3B1cChwb3B1cF9jZDU5NGFiY2QzZmM0NTgwODAzZjMxMGMxNGQ2NDkyNCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9iMmQ5NjQ4MTI5MTc0MTA0YTkxMzk4YWQ2OTdiOTc3MyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcwNjg3NiwtNzkuNTE4MTg4NDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYTA5YTIyZmJiYTQ3NDRkNDkzZGZhYWE0ZTk5N2UzYTMgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfOGI2MmMyMjg5OTFhNDg4M2FlMGNmNGQyMmJiYjFjZGYgPSAkKCc8ZGl2IGlkPSJodG1sXzhiNjJjMjI4OTkxYTQ4ODNhZTBjZjRkMjJiYmIxY2RmIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5XZXN0b248L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2EwOWEyMmZiYmE0NzQ0ZDQ5M2RmYWFhNGU5OTdlM2EzLnNldENvbnRlbnQoaHRtbF84YjYyYzIyODk5MWE0ODgzYWUwY2Y0ZDIyYmJiMWNkZik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9iMmQ5NjQ4MTI5MTc0MTA0YTkxMzk4YWQ2OTdiOTc3My5iaW5kUG9wdXAocG9wdXBfYTA5YTIyZmJiYTQ3NDRkNDkzZGZhYWE0ZTk5N2UzYTMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNWVkYTk2M2RmOGUzNGYyYmJmNTdiMjg2OGRiYjdkYWMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43NTc0MDk2LC03OS4yNzMzMDQwMDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9jNGZlMzU5Y2VkMTQ0NDllYjVlMzZkNWY4MDA0NGE5NyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF80Njc4NGYwNTI0OTg0MjczODUwOTE1MzI3MmEwNTYxMSA9ICQoJzxkaXYgaWQ9Imh0bWxfNDY3ODRmMDUyNDk4NDI3Mzg1MDkxNTMyNzJhMDU2MTEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRvcnNldCBQYXJrLCBXZXhmb3JkIEhlaWdodHMsIFNjYXJib3JvdWdoIFRvd24gQ2VudHJlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9jNGZlMzU5Y2VkMTQ0NDllYjVlMzZkNWY4MDA0NGE5Ny5zZXRDb250ZW50KGh0bWxfNDY3ODRmMDUyNDk4NDI3Mzg1MDkxNTMyNzJhMDU2MTEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNWVkYTk2M2RmOGUzNGYyYmJmNTdiMjg2OGRiYjdkYWMuYmluZFBvcHVwKHBvcHVwX2M0ZmUzNTljZWQxNDQ0OWViNWUzNmQ1ZjgwMDQ0YTk3KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzRhNmMyYTYxZmNlYjRlOWY5NzM4ODAxMzViNTRhNDUyID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzUyNzU4Mjk5OTk5OTk2LC03OS40MDAwNDkzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzc4MmQ1NDZkMmEzODRjMGI5Mjk1YTRhNGQ1OTBkYWViID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzVhNWE4NmRmYmFjYzQ0Zjg5YWUxYTg4YTdiMmJlNDkyID0gJCgnPGRpdiBpZD0iaHRtbF81YTVhODZkZmJhY2M0NGY4OWFlMWE4OGE3YjJiZTQ5MiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+WW9yayBNaWxscyBXZXN0PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF83ODJkNTQ2ZDJhMzg0YzBiOTI5NWE0YTRkNTkwZGFlYi5zZXRDb250ZW50KGh0bWxfNWE1YTg2ZGZiYWNjNDRmODlhZTFhODhhN2IyYmU0OTIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNGE2YzJhNjFmY2ViNGU5Zjk3Mzg4MDEzNWI1NGE0NTIuYmluZFBvcHVwKHBvcHVwXzc4MmQ1NDZkMmEzODRjMGI5Mjk1YTRhNGQ1OTBkYWViKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2U3MzBhZDcwNTZlNTRkYjg5OGU5NjU4ZTE3NjFjYmY0ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzEyNzUxMSwtNzkuMzkwMTk3NV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF82MTk4YmMzZTkzNmQ0YWEyYTJmZDBkMDMxNDhmNmJiMCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF85YTNlNzc0Mjk4YTM0NzQ1OGUzOTE3NWNiMzVhMzhhMyA9ICQoJzxkaXYgaWQ9Imh0bWxfOWEzZTc3NDI5OGEzNDc0NThlMzkxNzVjYjM1YTM4YTMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkRhdmlzdmlsbGUgTm9ydGg8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzYxOThiYzNlOTM2ZDRhYTJhMmZkMGQwMzE0OGY2YmIwLnNldENvbnRlbnQoaHRtbF85YTNlNzc0Mjk4YTM0NzQ1OGUzOTE3NWNiMzVhMzhhMyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9lNzMwYWQ3MDU2ZTU0ZGI4OThlOTY1OGUxNzYxY2JmNC5iaW5kUG9wdXAocG9wdXBfNjE5OGJjM2U5MzZkNGFhMmEyZmQwZDAzMTQ4ZjZiYjApOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNjQ3M2JjZWZkMGEyNDYyNGIyN2YyY2JjM2EzZmU0YmIgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42OTY5NDc2LC03OS40MTEzMDcyMDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF82OWZiY2FlMmEyNjg0MjEwYTIxOGJiMjU5Y2QxYWZmZCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9lYTEyM2ZmZDhiOTU0ZWYyODZkMTVhYmI5YTU1Mzc0OCA9ICQoJzxkaXYgaWQ9Imh0bWxfZWExMjNmZmQ4Yjk1NGVmMjg2ZDE1YWJiOWE1NTM3NDgiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkZvcmVzdCBIaWxsIE5vcnRoICZhbXA7IFdlc3QsIEZvcmVzdCBIaWxsIFJvYWQgUGFyazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNjlmYmNhZTJhMjY4NDIxMGEyMThiYjI1OWNkMWFmZmQuc2V0Q29udGVudChodG1sX2VhMTIzZmZkOGI5NTRlZjI4NmQxNWFiYjlhNTUzNzQ4KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzY0NzNiY2VmZDBhMjQ2MjRiMjdmMmNiYzNhM2ZlNGJiLmJpbmRQb3B1cChwb3B1cF82OWZiY2FlMmEyNjg0MjEwYTIxOGJiMjU5Y2QxYWZmZCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9kNGRkOWIwNDBiNGQ0ZTBhYTkxNzBhZDQwOWU5NWViZCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY2MTYwODMsLTc5LjQ2NDc2MzI5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzNhZDA5MzgwOWUxZTQwMzZiYmQ5YTkzYmZiYmRmZDZhID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2RiNTE5OWRlMDJlMjQyYWRhNGE1MzAwYzBkMjhmOThhID0gJCgnPGRpdiBpZD0iaHRtbF9kYjUxOTlkZTAyZTI0MmFkYTRhNTMwMGMwZDI4Zjk4YSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+SGlnaCBQYXJrLCBUaGUgSnVuY3Rpb24gU291dGg8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzNhZDA5MzgwOWUxZTQwMzZiYmQ5YTkzYmZiYmRmZDZhLnNldENvbnRlbnQoaHRtbF9kYjUxOTlkZTAyZTI0MmFkYTRhNTMwMGMwZDI4Zjk4YSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9kNGRkOWIwNDBiNGQ0ZTBhYTkxNzBhZDQwOWU5NWViZC5iaW5kUG9wdXAocG9wdXBfM2FkMDkzODA5ZTFlNDAzNmJiZDlhOTNiZmJiZGZkNmEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNWEzMWMxMGU5ZjJlNDhkNWIzZDNjZTUwYmIxZmRkNzcgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42OTYzMTksLTc5LjUzMjI0MjQwMDAwMDAyXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2IxNzViNDJhYWUxNTQzMWI5YTFhYzAyOGEwYTU5YjAyID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2EzOGRmMmI3Mjg5NjQ2MDE5NDhhYzdmYjk2ZGRiODc4ID0gJCgnPGRpdiBpZD0iaHRtbF9hMzhkZjJiNzI4OTY0NjAxOTQ4YWM3ZmI5NmRkYjg3OCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V2VzdG1vdW50PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iMTc1YjQyYWFlMTU0MzFiOWExYWMwMjhhMGE1OWIwMi5zZXRDb250ZW50KGh0bWxfYTM4ZGYyYjcyODk2NDYwMTk0OGFjN2ZiOTZkZGI4NzgpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNWEzMWMxMGU5ZjJlNDhkNWIzZDNjZTUwYmIxZmRkNzcuYmluZFBvcHVwKHBvcHVwX2IxNzViNDJhYWUxNTQzMWI5YTFhYzAyOGEwYTU5YjAyKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzJhNjA5NjdhNzRkZjRkZWY5YTdiMDM0NmM2MmZmMzNiID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzUwMDcxNTAwMDAwMDA0LC03OS4yOTU4NDkxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzk4ODFhMThlOGYwOTQ5ZDc4NWRlYTNiNGU1MzQxODQ4ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzEwMmNlNjYxNGEzNTRiMDA5MWQzM2Q0MjMyNWUwOTk0ID0gJCgnPGRpdiBpZD0iaHRtbF8xMDJjZTY2MTRhMzU0YjAwOTFkMzNkNDIzMjVlMDk5NCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V2V4Zm9yZCwgTWFyeXZhbGU8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzk4ODFhMThlOGYwOTQ5ZDc4NWRlYTNiNGU1MzQxODQ4LnNldENvbnRlbnQoaHRtbF8xMDJjZTY2MTRhMzU0YjAwOTFkMzNkNDIzMjVlMDk5NCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8yYTYwOTY3YTc0ZGY0ZGVmOWE3YjAzNDZjNjJmZjMzYi5iaW5kUG9wdXAocG9wdXBfOTg4MWExOGU4ZjA5NDlkNzg1ZGVhM2I0ZTUzNDE4NDgpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfY2UwY2YyZmQ0NGE5NGY2M2JiM2UzMjBlMTUyYjA0NGMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43ODI3MzY0LC03OS40NDIyNTkzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzdjZGZiOWRhMjQ1MjRhNDFiNTFmZmM1OTJmMTQ2ZTIzID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2MzODYxNjcwMzhhNTQwNzk5OWQ2NGViY2I3NDg5Y2IyID0gJCgnPGRpdiBpZD0iaHRtbF9jMzg2MTY3MDM4YTU0MDc5OTlkNjRlYmNiNzQ4OWNiMiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+V2lsbG93ZGFsZSwgV2lsbG93ZGFsZSBXZXN0PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF83Y2RmYjlkYTI0NTI0YTQxYjUxZmZjNTkyZjE0NmUyMy5zZXRDb250ZW50KGh0bWxfYzM4NjE2NzAzOGE1NDA3OTk5ZDY0ZWJjYjc0ODljYjIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfY2UwY2YyZmQ0NGE5NGY2M2JiM2UzMjBlMTUyYjA0NGMuYmluZFBvcHVwKHBvcHVwXzdjZGZiOWRhMjQ1MjRhNDFiNTFmZmM1OTJmMTQ2ZTIzKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2JkNzFkMGU0NzBkNTQ3MTI4NTAzODQ5ZDM5MzRlMzQ4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzE1MzgzNCwtNzkuNDA1Njc4NDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfNTIwZDNhZjc4NDY5NDZiZTg3MTI3YWViYTc3ZWY0OTggPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMTc5YWU3ZDc3ZWIzNGE4ZDg5YjY5OTk0NTVjNmJkNmIgPSAkKCc8ZGl2IGlkPSJodG1sXzE3OWFlN2Q3N2ViMzRhOGQ4OWI2OTk5NDU1YzZiZDZiIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Ob3J0aCBUb3JvbnRvIFdlc3QsICBMYXdyZW5jZSBQYXJrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF81MjBkM2FmNzg0Njk0NmJlODcxMjdhZWJhNzdlZjQ5OC5zZXRDb250ZW50KGh0bWxfMTc5YWU3ZDc3ZWIzNGE4ZDg5YjY5OTk0NTVjNmJkNmIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYmQ3MWQwZTQ3MGQ1NDcxMjg1MDM4NDlkMzkzNGUzNDguYmluZFBvcHVwKHBvcHVwXzUyMGQzYWY3ODQ2OTQ2YmU4NzEyN2FlYmE3N2VmNDk4KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzg3ZGQyYTNiMDVmZTQ0ZmI5NjFiNmFkNmJlODI3M2Y4ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjcyNzA5NywtNzkuNDA1Njc4NDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfNWJkMDQxMzdkNGVhNDA1MWE1OTU4ZTJiNTRiYWIwODEgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNGEyZmEzOWQ4YjQ4NDYyYmFkOWRkN2QzMDBkMmZiNjYgPSAkKCc8ZGl2IGlkPSJodG1sXzRhMmZhMzlkOGI0ODQ2MmJhZDlkZDdkMzAwZDJmYjY2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5UaGUgQW5uZXgsIE5vcnRoIE1pZHRvd24sIFlvcmt2aWxsZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNWJkMDQxMzdkNGVhNDA1MWE1OTU4ZTJiNTRiYWIwODEuc2V0Q29udGVudChodG1sXzRhMmZhMzlkOGI0ODQ2MmJhZDlkZDdkMzAwZDJmYjY2KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzg3ZGQyYTNiMDVmZTQ0ZmI5NjFiNmFkNmJlODI3M2Y4LmJpbmRQb3B1cChwb3B1cF81YmQwNDEzN2Q0ZWE0MDUxYTU5NThlMmI1NGJhYjA4MSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9jMzZmNTAzZjc3Yjk0MjA4OGQxNDY0MmEzZmQ3MWZjYSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY0ODk1OTcsLTc5LjQ1NjMyNV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF83NzEwZDVhN2M1ZGU0MzNhYWRiMjAyNWEyODZmOWQxYiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8yYTMxMzFlM2VhMmI0M2NjOWIyOTIxOWE0YjM5MzczMCA9ICQoJzxkaXYgaWQ9Imh0bWxfMmEzMTMxZTNlYTJiNDNjYzliMjkyMTlhNGIzOTM3MzAiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlBhcmtkYWxlLCBSb25jZXN2YWxsZXM8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzc3MTBkNWE3YzVkZTQzM2FhZGIyMDI1YTI4NmY5ZDFiLnNldENvbnRlbnQoaHRtbF8yYTMxMzFlM2VhMmI0M2NjOWIyOTIxOWE0YjM5MzczMCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9jMzZmNTAzZjc3Yjk0MjA4OGQxNDY0MmEzZmQ3MWZjYS5iaW5kUG9wdXAocG9wdXBfNzcxMGQ1YTdjNWRlNDMzYWFkYjIwMjVhMjg2ZjlkMWIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMTA4MjY1MjUxNGY0NGE1ODgyZjE2YmI1NjU2YzBiNTQgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42MzY5NjU2LC03OS42MTU4MTg5OTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8zNjMzZWFkYmRjYjY0ZDVjOTNhMjMyM2UzNThkMjg4YSA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF80ZmI2OGFjOTE3M2Q0ZTA4YjE4NWFkZTc2ZmJjNmU0NCA9ICQoJzxkaXYgaWQ9Imh0bWxfNGZiNjhhYzkxNzNkNGUwOGIxODVhZGU3NmZiYzZlNDQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNhbmFkYSBQb3N0IEdhdGV3YXkgUHJvY2Vzc2luZyBDZW50cmU8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzM2MzNlYWRiZGNiNjRkNWM5M2EyMzIzZTM1OGQyODhhLnNldENvbnRlbnQoaHRtbF80ZmI2OGFjOTE3M2Q0ZTA4YjE4NWFkZTc2ZmJjNmU0NCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8xMDgyNjUyNTE0ZjQ0YTU4ODJmMTZiYjU2NTZjMGI1NC5iaW5kUG9wdXAocG9wdXBfMzYzM2VhZGJkY2I2NGQ1YzkzYTIzMjNlMzU4ZDI4OGEpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMGJhNmFjMGQwYmY3NDZmNGEwYzg1NTgxZDMxMTQ2NjMgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42ODg5MDU0LC03OS41NTQ3MjQ0MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8xYjQyM2I0Y2VkODA0YWIwYWYyMTEzNzBhZjRiNWNlMCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF82NmM2NjFmNDRlMmI0MDVjYmY1NTFmZmFlMGY1ZTNlOSA9ICQoJzxkaXYgaWQ9Imh0bWxfNjZjNjYxZjQ0ZTJiNDA1Y2JmNTUxZmZhZTBmNWUzZTkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPktpbmdzdmlldyBWaWxsYWdlLCBTdC4gUGhpbGxpcHMsIE1hcnRpbiBHcm92ZSBHYXJkZW5zLCBSaWNodmlldyBHYXJkZW5zPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8xYjQyM2I0Y2VkODA0YWIwYWYyMTEzNzBhZjRiNWNlMC5zZXRDb250ZW50KGh0bWxfNjZjNjYxZjQ0ZTJiNDA1Y2JmNTUxZmZhZTBmNWUzZTkpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMGJhNmFjMGQwYmY3NDZmNGEwYzg1NTgxZDMxMTQ2NjMuYmluZFBvcHVwKHBvcHVwXzFiNDIzYjRjZWQ4MDRhYjBhZjIxMTM3MGFmNGI1Y2UwKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzcxMTYzZGE4NGNjNjRjMzU4ZWZkYWZlNmQ0MmNiNmMxID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzk0MjAwMywtNzkuMjYyMDI5NDAwMDAwMDJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMzYzM2MzZWE1MTQ5NDgyOTkxMzRmNTA1YTc5MmU4ZTcgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNTczYTNjYzBhN2JkNDAyN2I5NTI3MTYyMzEzOGYwYzYgPSAkKCc8ZGl2IGlkPSJodG1sXzU3M2EzY2MwYTdiZDQwMjdiOTUyNzE2MjMxMzhmMGM2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5BZ2luY291cnQ8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzM2MzNjM2VhNTE0OTQ4Mjk5MTM0ZjUwNWE3OTJlOGU3LnNldENvbnRlbnQoaHRtbF81NzNhM2NjMGE3YmQ0MDI3Yjk1MjcxNjIzMTM4ZjBjNik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl83MTE2M2RhODRjYzY0YzM1OGVmZGFmZTZkNDJjYjZjMS5iaW5kUG9wdXAocG9wdXBfMzYzM2MzZWE1MTQ5NDgyOTkxMzRmNTA1YTc5MmU4ZTcpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfZmQ2YzNmYjRlMGQ1NGMyN2FlNDc3ZWI1ZmU2Y2Q5YzcgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My43MDQzMjQ0LC03OS4zODg3OTAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzJjNDQ3ZDVmMjFlZjQ3MTFiNjI3ZmQxNjRhYjdjZDZmID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzc3MGM1YTRiMjc1NjQ2ZDVhNjIyODk1NWM3MDhiMGM4ID0gJCgnPGRpdiBpZD0iaHRtbF83NzBjNWE0YjI3NTY0NmQ1YTYyMjg5NTVjNzA4YjBjOCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+RGF2aXN2aWxsZTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMmM0NDdkNWYyMWVmNDcxMWI2MjdmZDE2NGFiN2NkNmYuc2V0Q29udGVudChodG1sXzc3MGM1YTRiMjc1NjQ2ZDVhNjIyODk1NWM3MDhiMGM4KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2ZkNmMzZmI0ZTBkNTRjMjdhZTQ3N2ViNWZlNmNkOWM3LmJpbmRQb3B1cChwb3B1cF8yYzQ0N2Q1ZjIxZWY0NzExYjYyN2ZkMTY0YWI3Y2Q2Zik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8yODY3MjhjMmY2Y2Q0MzA0YWVhNmE4ZGE2MzJhYTMzNSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY2MjY5NTYsLTc5LjQwMDA0OTNdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMTllMzEzNDcyMTUyNDg5YmI0ZmJmNmY5MDBjZWE1MzQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYjY2ODcwZjE1YzQxNDFmMjljYzk2ZjI0MGI5NmJkMTIgPSAkKCc8ZGl2IGlkPSJodG1sX2I2Njg3MGYxNWM0MTQxZjI5Y2M5NmYyNDBiOTZiZDEyIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Vbml2ZXJzaXR5IG9mIFRvcm9udG8sIEhhcmJvcmQ8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzE5ZTMxMzQ3MjE1MjQ4OWJiNGZiZjZmOTAwY2VhNTM0LnNldENvbnRlbnQoaHRtbF9iNjY4NzBmMTVjNDE0MWYyOWNjOTZmMjQwYjk2YmQxMik7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl8yODY3MjhjMmY2Y2Q0MzA0YWVhNmE4ZGE2MzJhYTMzNS5iaW5kUG9wdXAocG9wdXBfMTllMzEzNDcyMTUyNDg5YmI0ZmJmNmY5MDBjZWE1MzQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMDVlMTMwMTNmODNlNDkwMmE4YTYzOWNkNjg5YzFhMjUgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NTE1NzA2LC03OS40ODQ0NDk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2JkNWY5NGMzOGQwZTQ5NmRiMTdlMDljOWQ1ZDM1M2E4ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzFmZGRlNWFkOWYxZDQ0ZGY4MjdkYmM2Yzc0MTc3YzVhID0gJCgnPGRpdiBpZD0iaHRtbF8xZmRkZTVhZDlmMWQ0NGRmODI3ZGJjNmM3NDE3N2M1YSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+UnVubnltZWRlLCBTd2Fuc2VhPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iZDVmOTRjMzhkMGU0OTZkYjE3ZTA5YzlkNWQzNTNhOC5zZXRDb250ZW50KGh0bWxfMWZkZGU1YWQ5ZjFkNDRkZjgyN2RiYzZjNzQxNzdjNWEpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMDVlMTMwMTNmODNlNDkwMmE4YTYzOWNkNjg5YzFhMjUuYmluZFBvcHVwKHBvcHVwX2JkNWY5NGMzOGQwZTQ5NmRiMTdlMDljOWQ1ZDM1M2E4KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzczNTI3Yjk1NjA2MTQxYTY4NmFlNTRkMDFmZTc4YmFjID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzgxNjM3NSwtNzkuMzA0MzAyMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF84OGExZmE1ZWJmNzE0M2RhYThkNmE4OTM1YTU2NzkwMCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8wMmM2YjY4YjFkMTY0N2ZiYWY0ZTM0NWIzMzdhZGE2MCA9ICQoJzxkaXYgaWQ9Imh0bWxfMDJjNmI2OGIxZDE2NDdmYmFmNGUzNDViMzM3YWRhNjAiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNsYXJrcyBDb3JuZXJzLCBUYW0gTyYjMzk7U2hhbnRlciwgU3VsbGl2YW48L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzg4YTFmYTVlYmY3MTQzZGFhOGQ2YTg5MzVhNTY3OTAwLnNldENvbnRlbnQoaHRtbF8wMmM2YjY4YjFkMTY0N2ZiYWY0ZTM0NWIzMzdhZGE2MCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl83MzUyN2I5NTYwNjE0MWE2ODZhZTU0ZDAxZmU3OGJhYy5iaW5kUG9wdXAocG9wdXBfODhhMWZhNWViZjcxNDNkYWE4ZDZhODkzNWE1Njc5MDApOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfM2Y3ZDE3NTkyMzUzNDU1MWE3OTc4OWMzODc1ZTEzYzkgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42ODk1NzQzLC03OS4zODMxNTk5MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iOGJjNmZiNTMwODg0YzBkYTMzOWU4YjVjMTEyZTAxZCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9hOTg4M2NjOWUyOGM0ZDMwOTAyMTE0OWJkOGJmZDA4MSA9ICQoJzxkaXYgaWQ9Imh0bWxfYTk4ODNjYzllMjhjNGQzMDkwMjExNDliZDhiZmQwODEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk1vb3JlIFBhcmssIFN1bW1lcmhpbGwgRWFzdDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfYjhiYzZmYjUzMDg4NGMwZGEzMzllOGI1YzExMmUwMWQuc2V0Q29udGVudChodG1sX2E5ODgzY2M5ZTI4YzRkMzA5MDIxMTQ5YmQ4YmZkMDgxKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzNmN2QxNzU5MjM1MzQ1NTFhNzk3ODljMzg3NWUxM2M5LmJpbmRQb3B1cChwb3B1cF9iOGJjNmZiNTMwODg0YzBkYTMzOWU4YjVjMTEyZTAxZCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8zM2ZjYmQwM2NmNWE0NWE3OTY2YWJlOGRhNjNmNTI2YSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY1MzIwNTcsLTc5LjQwMDA0OTNdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfNTU0MTBmMDc0NGQ0NDE5Mzg2YWM2MmFjYWE2YzAxZDcgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfZWYzNmQxYmUxNWY1NGFjZmJlNjk5YTBmNWM4MzU4MDQgPSAkKCc8ZGl2IGlkPSJodG1sX2VmMzZkMWJlMTVmNTRhY2ZiZTY5OWEwZjVjODM1ODA0IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5LZW5zaW5ndG9uIE1hcmtldCwgQ2hpbmF0b3duLCBHcmFuZ2UgUGFyazwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNTU0MTBmMDc0NGQ0NDE5Mzg2YWM2MmFjYWE2YzAxZDcuc2V0Q29udGVudChodG1sX2VmMzZkMWJlMTVmNTRhY2ZiZTY5OWEwZjVjODM1ODA0KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzMzZmNiZDAzY2Y1YTQ1YTc5NjZhYmU4ZGE2M2Y1MjZhLmJpbmRQb3B1cChwb3B1cF81NTQxMGYwNzQ0ZDQ0MTkzODZhYzYyYWNhYTZjMDFkNyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl80OGMzNTA5NWI1YjM0NjFhODQzMWQ3MTFiY2QwNDk3OSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjgxNTI1MjIsLTc5LjI4NDU3NzJdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfZjBlOWIxZmQ1MzljNDliNGIwMGY4NjZjNGI3ZjgwODkgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYWM4MTUxOWIxOWMyNDcyZmJmM2E3NTg3ZDg4ZWJkM2EgPSAkKCc8ZGl2IGlkPSJodG1sX2FjODE1MTliMTljMjQ3MmZiZjNhNzU4N2Q4OGViZDNhIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5NaWxsaWtlbiwgQWdpbmNvdXJ0IE5vcnRoLCBTdGVlbGVzIEVhc3QsIEwmIzM5O0Ftb3JlYXV4IEVhc3Q8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2YwZTliMWZkNTM5YzQ5YjRiMDBmODY2YzRiN2Y4MDg5LnNldENvbnRlbnQoaHRtbF9hYzgxNTE5YjE5YzI0NzJmYmYzYTc1ODdkODhlYmQzYSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl80OGMzNTA5NWI1YjM0NjFhODQzMWQ3MTFiY2QwNDk3OS5iaW5kUG9wdXAocG9wdXBfZjBlOWIxZmQ1MzljNDliNGIwMGY4NjZjNGI3ZjgwODkpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfNTc3OGYwNjE2MjQ3NGNhNzllMTc3ZGVmOGY5MGY4NmQgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42ODY0MTIyOTk5OTk5OSwtNzkuNDAwMDQ5M10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF80YzRhMDA2NWMyYjg0YTU1OThjOGZiZDBjN2YxNzlmMiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8zMzA4MzQzOTYyZGE0Y2M2YjEyZWRlMjE0ODE3YWIwNCA9ICQoJzxkaXYgaWQ9Imh0bWxfMzMwODM0Mzk2MmRhNGNjNmIxMmVkZTIxNDgxN2FiMDQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlN1bW1lcmhpbGwgV2VzdCwgUmF0aG5lbGx5LCBTb3V0aCBIaWxsLCBGb3Jlc3QgSGlsbCBTRSwgRGVlciBQYXJrPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF80YzRhMDA2NWMyYjg0YTU1OThjOGZiZDBjN2YxNzlmMi5zZXRDb250ZW50KGh0bWxfMzMwODM0Mzk2MmRhNGNjNmIxMmVkZTIxNDgxN2FiMDQpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNTc3OGYwNjE2MjQ3NGNhNzllMTc3ZGVmOGY5MGY4NmQuYmluZFBvcHVwKHBvcHVwXzRjNGEwMDY1YzJiODRhNTU5OGM4ZmJkMGM3ZjE3OWYyKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzhmYWVkMGY0NmEwYzQxOGY4NDUyMTQ5ODk5NDliNTk2ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjI4OTQ2NywtNzkuMzk0NDE5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF81NjE4OTkxYjYzYjI0MTQyYTdhOTM3NDk2ZTU4ODQ1NiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8yZmY3MzBjYjJlYTQ0MDZjOTBlYjk1ODViODJmYzk2YyA9ICQoJzxkaXYgaWQ9Imh0bWxfMmZmNzMwY2IyZWE0NDA2YzkwZWI5NTg1YjgyZmM5NmMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNOIFRvd2VyLCBLaW5nIGFuZCBTcGFkaW5hLCBSYWlsd2F5IExhbmRzLCBIYXJib3VyZnJvbnQgV2VzdCwgQmF0aHVyc3QgUXVheSwgU291dGggTmlhZ2FyYSwgSXNsYW5kIGFpcnBvcnQ8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzU2MTg5OTFiNjNiMjQxNDJhN2E5Mzc0OTZlNTg4NDU2LnNldENvbnRlbnQoaHRtbF8yZmY3MzBjYjJlYTQ0MDZjOTBlYjk1ODViODJmYzk2Yyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl84ZmFlZDBmNDZhMGM0MThmODQ1MjE0OTg5OTQ5YjU5Ni5iaW5kUG9wdXAocG9wdXBfNTYxODk5MWI2M2IyNDE0MmE3YTkzNzQ5NmU1ODg0NTYpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfYTY0Yjg1MTA1YjhiNDE1ZDhjNjA5YzkyYjhlYmQ2NTUgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42MDU2NDY2LC03OS41MDEzMjA3MDAwMDAwMV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9kODEyYzE0NjUyNGI0NWVlOWMwMTAxMmY3NDhjNjRlNiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84ODkzOGMxNjIwN2M0MWQ0YWUzYzQzNGEyNTVhZjBlZCA9ICQoJzxkaXYgaWQ9Imh0bWxfODg5MzhjMTYyMDdjNDFkNGFlM2M0MzRhMjU1YWYwZWQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk5ldyBUb3JvbnRvLCBNaW1pY28gU291dGgsIEh1bWJlciBCYXkgU2hvcmVzPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9kODEyYzE0NjUyNGI0NWVlOWMwMTAxMmY3NDhjNjRlNi5zZXRDb250ZW50KGh0bWxfODg5MzhjMTYyMDdjNDFkNGFlM2M0MzRhMjU1YWYwZWQpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYTY0Yjg1MTA1YjhiNDE1ZDhjNjA5YzkyYjhlYmQ2NTUuYmluZFBvcHVwKHBvcHVwX2Q4MTJjMTQ2NTI0YjQ1ZWU5YzAxMDEyZjc0OGM2NGU2KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzI5ZWI3OGVlMDEwOTQ2ZGNhZTZkMzNhNDYyYmQxYTYxID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNzM5NDE2Mzk5OTk5OTk2LC03OS41ODg0MzY5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzE2ZWE2ZGQ1YWFhZDQzZWNiMWQ2N2NkMjkxNzMyODNmID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2E3ODJhOTQ5NzgzNDQwNTZiOTk5ZGJlY2YyNTU3MmI4ID0gJCgnPGRpdiBpZD0iaHRtbF9hNzgyYTk0OTc4MzQ0MDU2Yjk5OWRiZWNmMjU1NzJiOCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+U291dGggU3RlZWxlcywgU2lsdmVyc3RvbmUsIEh1bWJlcmdhdGUsIEphbWVzdG93biwgTW91bnQgT2xpdmUsIEJlYXVtb25kIEhlaWdodHMsIFRoaXN0bGV0b3duLCBBbGJpb24gR2FyZGVuczwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMTZlYTZkZDVhYWFkNDNlY2IxZDY3Y2QyOTE3MzI4M2Yuc2V0Q29udGVudChodG1sX2E3ODJhOTQ5NzgzNDQwNTZiOTk5ZGJlY2YyNTU3MmI4KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzI5ZWI3OGVlMDEwOTQ2ZGNhZTZkMzNhNDYyYmQxYTYxLmJpbmRQb3B1cChwb3B1cF8xNmVhNmRkNWFhYWQ0M2VjYjFkNjdjZDI5MTczMjgzZik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl85MjMwYjM4ZDJkMjk0ZWMzYjJkZWE2YmVkZjcyM2ZjMSA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjc5OTUyNTIwMDAwMDAwNSwtNzkuMzE4Mzg4N10sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF83OGU2NTc5NmQ5NTc0M2NhOTllZTg0MzYzM2VkOWNhMCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF8xYjAyODIxNGMxMjQ0ZWY5ODBkZWYyODIzYWQ0ZTI2ZSA9ICQoJzxkaXYgaWQ9Imh0bWxfMWIwMjgyMTRjMTI0NGVmOTgwZGVmMjgyM2FkNGUyNmUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlN0ZWVsZXMgV2VzdCwgTCYjMzk7QW1vcmVhdXggV2VzdDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNzhlNjU3OTZkOTU3NDNjYTk5ZWU4NDM2MzNlZDljYTAuc2V0Q29udGVudChodG1sXzFiMDI4MjE0YzEyNDRlZjk4MGRlZjI4MjNhZDRlMjZlKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzkyMzBiMzhkMmQyOTRlYzNiMmRlYTZiZWRmNzIzZmMxLmJpbmRQb3B1cChwb3B1cF83OGU2NTc5NmQ5NTc0M2NhOTllZTg0MzYzM2VkOWNhMCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl9kMGZkNmIxNTI5ZTA0YzU4YTAyNTYzNDQ5MzlhMGNlMiA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY3OTU2MjYsLTc5LjM3NzUyOTQwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzliZjg3ZmJjMWVkZTQ1YjRiZTllYzA4MTkwOWRmZjQ0ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzEwOTZlMjE5ZWNlZDRhNDJhNzU5ZDAyMzBiZTk2ZTc5ID0gJCgnPGRpdiBpZD0iaHRtbF8xMDk2ZTIxOWVjZWQ0YTQyYTc1OWQwMjMwYmU5NmU3OSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Um9zZWRhbGU8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzliZjg3ZmJjMWVkZTQ1YjRiZTllYzA4MTkwOWRmZjQ0LnNldENvbnRlbnQoaHRtbF8xMDk2ZTIxOWVjZWQ0YTQyYTc1OWQwMjMwYmU5NmU3OSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgY2lyY2xlX21hcmtlcl9kMGZkNmIxNTI5ZTA0YzU4YTAyNTYzNDQ5MzlhMGNlMi5iaW5kUG9wdXAocG9wdXBfOWJmODdmYmMxZWRlNDViNGJlOWVjMDgxOTA5ZGZmNDQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIGNpcmNsZV9tYXJrZXJfMWRkNmRlMzgxMTEyNDExYmI5NGNlYTUwOThiZWQxNGQgPSBMLmNpcmNsZU1hcmtlcigKICAgICAgICAgICAgICAgIFs0My42NDY0MzUyLC03OS4zNzQ4NDU5OTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9hZmYyODZkZWRhMjc0NDc4OWE4MmM5ZTdjZTYxYTAwYyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84NWRjN2E1MWYwNTI0MGYzOTRjZTU0NjdkZmU0ZGM4YiA9ICQoJzxkaXYgaWQ9Imh0bWxfODVkYzdhNTFmMDUyNDBmMzk0Y2U1NDY3ZGZlNGRjOGIiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlN0biBBIFBPIEJveGVzPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9hZmYyODZkZWRhMjc0NDc4OWE4MmM5ZTdjZTYxYTAwYy5zZXRDb250ZW50KGh0bWxfODVkYzdhNTFmMDUyNDBmMzk0Y2U1NDY3ZGZlNGRjOGIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMWRkNmRlMzgxMTEyNDExYmI5NGNlYTUwOThiZWQxNGQuYmluZFBvcHVwKHBvcHVwX2FmZjI4NmRlZGEyNzQ0Nzg5YTgyYzllN2NlNjFhMDBjKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2I2M2ZiYzM2MGRkYzRmNTU5NTNiZjMxODRlMzllZTFiID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjAyNDEzNzAwMDAwMDEsLTc5LjU0MzQ4NDA5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzYwYTlkZmY1ZGExMjQzMzM5YWQ0YTU4MDBkYjg0Y2JhID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2JiZDQ4YmQ5MDc4ZDRjZTlhYzU0MWIxOTFjNTExZjFmID0gJCgnPGRpdiBpZD0iaHRtbF9iYmQ0OGJkOTA3OGQ0Y2U5YWM1NDFiMTkxYzUxMWYxZiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QWxkZXJ3b29kLCBMb25nIEJyYW5jaDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNjBhOWRmZjVkYTEyNDMzMzlhZDRhNTgwMGRiODRjYmEuc2V0Q29udGVudChodG1sX2JiZDQ4YmQ5MDc4ZDRjZTlhYzU0MWIxOTFjNTExZjFmKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyX2I2M2ZiYzM2MGRkYzRmNTU5NTNiZjMxODRlMzllZTFiLmJpbmRQb3B1cChwb3B1cF82MGE5ZGZmNWRhMTI0MzMzOWFkNGE1ODAwZGI4NGNiYSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl82OGY1ZTkyMmM2YjU0NDkwYTAzZmFlOTgxYTk5NDA3NyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjcwNjc0ODI5OTk5OTk5NCwtNzkuNTk0MDU0NF0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9iZDBiMTY1ZDMzZDQ0ZDViYmUxYzY0ZDEwZWE4MDU3ZCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9hMmJjMjViZjViOGE0OGRlYmEwNGIzODljMzVjNThiYiA9ICQoJzxkaXYgaWQ9Imh0bWxfYTJiYzI1YmY1YjhhNDhkZWJhMDRiMzg5YzM1YzU4YmIiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk5vcnRod2VzdCwgV2VzdCBIdW1iZXIgLSBDbGFpcnZpbGxlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9iZDBiMTY1ZDMzZDQ0ZDViYmUxYzY0ZDEwZWE4MDU3ZC5zZXRDb250ZW50KGh0bWxfYTJiYzI1YmY1YjhhNDhkZWJhMDRiMzg5YzM1YzU4YmIpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNjhmNWU5MjJjNmI1NDQ5MGEwM2ZhZTk4MWE5OTQwNzcuYmluZFBvcHVwKHBvcHVwX2JkMGIxNjVkMzNkNDRkNWJiZTFjNjRkMTBlYTgwNTdkKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzE0ZWU5YmExM2JjZjRkM2FiNmNkYTdkNjMzZjRmZjY3ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuODM2MTI0NzAwMDAwMDA2LC03OS4yMDU2MzYwOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF81ZTVkYjlhMTBlYTM0OTI0YTk3OTE0OThiNWQzZGYzNiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9kYzIyNDliOTRlMTE0NjQxODMzYzEwNGM3ZmJlM2JmNyA9ICQoJzxkaXYgaWQ9Imh0bWxfZGMyMjQ5Yjk0ZTExNDY0MTgzM2MxMDRjN2ZiZTNiZjciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlVwcGVyIFJvdWdlPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF81ZTVkYjlhMTBlYTM0OTI0YTk3OTE0OThiNWQzZGYzNi5zZXRDb250ZW50KGh0bWxfZGMyMjQ5Yjk0ZTExNDY0MTgzM2MxMDRjN2ZiZTNiZjcpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMTRlZTliYTEzYmNmNGQzYWI2Y2RhN2Q2MzNmNGZmNjcuYmluZFBvcHVwKHBvcHVwXzVlNWRiOWExMGVhMzQ5MjRhOTc5MTQ5OGI1ZDNkZjM2KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzFiMDljMDBiYTQ0NDQxMmQ4YTQzN2ZmMjg0YjUzMWVmID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjY3OTY3LC03OS4zNjc2NzUzXSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzBiOWZjODA2YzgyYjRiZDM4NjIxNDU0MDljZjUxMmU3ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzNmMzA1MjFkYjFkNDRlM2RhNjEzYjAyZjUwZGQ3ZmI4ID0gJCgnPGRpdiBpZD0iaHRtbF8zZjMwNTIxZGIxZDQ0ZTNkYTYxM2IwMmY1MGRkN2ZiOCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+U3QuIEphbWVzIFRvd24sIENhYmJhZ2V0b3duPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8wYjlmYzgwNmM4MmI0YmQzODYyMTQ1NDA5Y2Y1MTJlNy5zZXRDb250ZW50KGh0bWxfM2YzMDUyMWRiMWQ0NGUzZGE2MTNiMDJmNTBkZDdmYjgpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfMWIwOWMwMGJhNDQ0NDEyZDhhNDM3ZmYyODRiNTMxZWYuYmluZFBvcHVwKHBvcHVwXzBiOWZjODA2YzgyYjRiZDM4NjIxNDU0MDljZjUxMmU3KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2I2ZTE0NDk0NjFkMDQzYmFhZDMxOTgyOWViNzBjNTk1ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjQ4NDI5MiwtNzkuMzgyMjgwMl0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF80NTJlM2U2NmQ5ZDc0ODUyOTE0ZGJmODNkMTFkNjZlNyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84YWIyMmUwM2Q3YWI0ZWU5OGExMDY1YjgxNDllMWY5YyA9ICQoJzxkaXYgaWQ9Imh0bWxfOGFiMjJlMDNkN2FiNGVlOThhMTA2NWI4MTQ5ZTFmOWMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkZpcnN0IENhbmFkaWFuIFBsYWNlLCBVbmRlcmdyb3VuZCBjaXR5PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF80NTJlM2U2NmQ5ZDc0ODUyOTE0ZGJmODNkMTFkNjZlNy5zZXRDb250ZW50KGh0bWxfOGFiMjJlMDNkN2FiNGVlOThhMTA2NWI4MTQ5ZTFmOWMpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYjZlMTQ0OTQ2MWQwNDNiYWFkMzE5ODI5ZWI3MGM1OTUuYmluZFBvcHVwKHBvcHVwXzQ1MmUzZTY2ZDlkNzQ4NTI5MTRkYmY4M2QxMWQ2NmU3KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyX2FmZDI0MDAxYmRiNDRjMzM5N2I4YzJiYjM0NWQ4NzRkID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjUzNjUzNjAwMDAwMDA1LC03OS41MDY5NDM2XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzlkOTYxMmUwZWRlYjQyOGI5NTc3ZTQ4MWVhODA5MWY3ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2U1ODRkNGViYjYzNzRhYzE5MmMzYzZlNDA4YjFlYmM2ID0gJCgnPGRpdiBpZD0iaHRtbF9lNTg0ZDRlYmI2Mzc0YWMxOTJjM2M2ZTQwOGIxZWJjNiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+VGhlIEtpbmdzd2F5LCBNb250Z29tZXJ5IFJvYWQsIE9sZCBNaWxsIE5vcnRoPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF85ZDk2MTJlMGVkZWI0MjhiOTU3N2U0ODFlYTgwOTFmNy5zZXRDb250ZW50KGh0bWxfZTU4NGQ0ZWJiNjM3NGFjMTkyYzNjNmU0MDhiMWViYzYpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfYWZkMjQwMDFiZGI0NGMzMzk3YjhjMmJiMzQ1ZDg3NGQuYmluZFBvcHVwKHBvcHVwXzlkOTYxMmUwZWRlYjQyOGI5NTc3ZTQ4MWVhODA5MWY3KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzRhYTIxNWU3ZDRjMDQ2YmE4NTE0NDEwY2Q3OThlNjQ1ID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjY1ODU5OSwtNzkuMzgzMTU5OTAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMTJjYjY2N2FhNzVmNDM1Yjg3MzVjMjNiYzgzNWZhZjUgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMGM4ZTBmNDI5YWE1NGY1ZjkwNWM5MzIyM2EzMzBkZjEgPSAkKCc8ZGl2IGlkPSJodG1sXzBjOGUwZjQyOWFhNTRmNWY5MDVjOTMyMjNhMzMwZGYxIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5DaHVyY2ggYW5kIFdlbGxlc2xleTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMTJjYjY2N2FhNzVmNDM1Yjg3MzVjMjNiYzgzNWZhZjUuc2V0Q29udGVudChodG1sXzBjOGUwZjQyOWFhNTRmNWY5MDVjOTMyMjNhMzMwZGYxKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzRhYTIxNWU3ZDRjMDQ2YmE4NTE0NDEwY2Q3OThlNjQ1LmJpbmRQb3B1cChwb3B1cF8xMmNiNjY3YWE3NWY0MzViODczNWMyM2JjODM1ZmFmNSk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl8zMjgxM2M3YWVjOTY0YmJmOWQ0YWJhYjAyZjM2MTM5MCA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjY2Mjc0MzksLTc5LjMyMTU1OF0sCiAgICAgICAgICAgICAgICB7CiAgImJ1YmJsaW5nTW91c2VFdmVudHMiOiB0cnVlLAogICJjb2xvciI6ICJibHVlIiwKICAiZGFzaEFycmF5IjogbnVsbCwKICAiZGFzaE9mZnNldCI6IG51bGwsCiAgImZpbGwiOiB0cnVlLAogICJmaWxsQ29sb3IiOiAiIzMxODZjYyIsCiAgImZpbGxPcGFjaXR5IjogMC43LAogICJmaWxsUnVsZSI6ICJldmVub2RkIiwKICAibGluZUNhcCI6ICJyb3VuZCIsCiAgImxpbmVKb2luIjogInJvdW5kIiwKICAib3BhY2l0eSI6IDEuMCwKICAicmFkaXVzIjogNSwKICAic3Ryb2tlIjogdHJ1ZSwKICAid2VpZ2h0IjogMwp9CiAgICAgICAgICAgICAgICApLmFkZFRvKG1hcF9kYzU3NmIwNmRlOWM0NDQwOGJiMDZkZmRkNzEyMWY2NSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9jZjdkZTRkMzdkYWY0ZjllYmExZDc4ZjY2MGYyNGQ4OCA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9jNGU0MzhkY2ExMzk0ZjdkODhkNmFmMWY1YzQyMWI2NyA9ICQoJzxkaXYgaWQ9Imh0bWxfYzRlNDM4ZGNhMTM5NGY3ZDg4ZDZhZjFmNWM0MjFiNjciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkJ1c2luZXNzIHJlcGx5IG1haWwgUHJvY2Vzc2luZyBDZW50cmUsIFNvdXRoIENlbnRyYWwgTGV0dGVyIFByb2Nlc3NpbmcgUGxhbnQgVG9yb250bzwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfY2Y3ZGU0ZDM3ZGFmNGY5ZWJhMWQ3OGY2NjBmMjRkODguc2V0Q29udGVudChodG1sX2M0ZTQzOGRjYTEzOTRmN2Q4OGQ2YWYxZjVjNDIxYjY3KTsKICAgICAgICAgICAgCgogICAgICAgICAgICBjaXJjbGVfbWFya2VyXzMyODEzYzdhZWM5NjRiYmY5ZDRhYmFiMDJmMzYxMzkwLmJpbmRQb3B1cChwb3B1cF9jZjdkZTRkMzdkYWY0ZjllYmExZDc4ZjY2MGYyNGQ4OCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgY2lyY2xlX21hcmtlcl82OTAyODA0ZDczNzE0ZTE1OWNlODFiMDE2ZTViM2RiYyA9IEwuY2lyY2xlTWFya2VyKAogICAgICAgICAgICAgICAgWzQzLjYzNjI1NzksLTc5LjQ5ODUwOTA5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHsKICAiYnViYmxpbmdNb3VzZUV2ZW50cyI6IHRydWUsCiAgImNvbG9yIjogImJsdWUiLAogICJkYXNoQXJyYXkiOiBudWxsLAogICJkYXNoT2Zmc2V0IjogbnVsbCwKICAiZmlsbCI6IHRydWUsCiAgImZpbGxDb2xvciI6ICIjMzE4NmNjIiwKICAiZmlsbE9wYWNpdHkiOiAwLjcsCiAgImZpbGxSdWxlIjogImV2ZW5vZGQiLAogICJsaW5lQ2FwIjogInJvdW5kIiwKICAibGluZUpvaW4iOiAicm91bmQiLAogICJvcGFjaXR5IjogMS4wLAogICJyYWRpdXMiOiA1LAogICJzdHJva2UiOiB0cnVlLAogICJ3ZWlnaHQiOiAzCn0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2RjNTc2YjA2ZGU5YzQ0NDA4YmIwNmRmZGQ3MTIxZjY1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzNjZjQ4YjE3YmI5YzQ3MTFiMDE3MDU1ZTlhNTQ3MGFlID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2Q5NjZhMzU2MzM4NTQyMGM4ODY4Yzc0OTgxNDliOTk3ID0gJCgnPGRpdiBpZD0iaHRtbF9kOTY2YTM1NjMzODU0MjBjODg2OGM3NDk4MTQ5Yjk5NyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+T2xkIE1pbGwgU291dGgsIEtpbmcmIzM5O3MgTWlsbCBQYXJrLCBTdW5ueWxlYSwgSHVtYmVyIEJheSwgTWltaWNvIE5FLCBUaGUgUXVlZW5zd2F5IEVhc3QsIFJveWFsIFlvcmsgU291dGggRWFzdCwgS2luZ3N3YXkgUGFyayBTb3V0aCBFYXN0PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8zY2Y0OGIxN2JiOWM0NzExYjAxNzA1NWU5YTU0NzBhZS5zZXRDb250ZW50KGh0bWxfZDk2NmEzNTYzMzg1NDIwYzg4NjhjNzQ5ODE0OWI5OTcpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfNjkwMjgwNGQ3MzcxNGUxNTljZTgxYjAxNmU1YjNkYmMuYmluZFBvcHVwKHBvcHVwXzNjZjQ4YjE3YmI5YzQ3MTFiMDE3MDU1ZTlhNTQ3MGFlKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBjaXJjbGVfbWFya2VyXzNjYzA0MjNlNmJlNTQ0OWNhMDczNjJhNmU0N2EwZDliID0gTC5jaXJjbGVNYXJrZXIoCiAgICAgICAgICAgICAgICBbNDMuNjI4ODQwOCwtNzkuNTIwOTk5NDAwMDAwMDFdLAogICAgICAgICAgICAgICAgewogICJidWJibGluZ01vdXNlRXZlbnRzIjogdHJ1ZSwKICAiY29sb3IiOiAiYmx1ZSIsCiAgImRhc2hBcnJheSI6IG51bGwsCiAgImRhc2hPZmZzZXQiOiBudWxsLAogICJmaWxsIjogdHJ1ZSwKICAiZmlsbENvbG9yIjogIiMzMTg2Y2MiLAogICJmaWxsT3BhY2l0eSI6IDAuNywKICAiZmlsbFJ1bGUiOiAiZXZlbm9kZCIsCiAgImxpbmVDYXAiOiAicm91bmQiLAogICJsaW5lSm9pbiI6ICJyb3VuZCIsCiAgIm9wYWNpdHkiOiAxLjAsCiAgInJhZGl1cyI6IDUsCiAgInN0cm9rZSI6IHRydWUsCiAgIndlaWdodCI6IDMKfQogICAgICAgICAgICAgICAgKS5hZGRUbyhtYXBfZGM1NzZiMDZkZTljNDQ0MDhiYjA2ZGZkZDcxMjFmNjUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMzJlMjYyNWNhMzU5NDlmNWI5ZGMwMDg5MmUxNTA2ODEgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYWUwMzdlZWYxOWZlNDQ0NjhkZmZiZTFkYTQyODYwODYgPSAkKCc8ZGl2IGlkPSJodG1sX2FlMDM3ZWVmMTlmZTQ0NDY4ZGZmYmUxZGE0Mjg2MDg2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5NaW1pY28gTlcsIFRoZSBRdWVlbnN3YXkgV2VzdCwgU291dGggb2YgQmxvb3IsIEtpbmdzd2F5IFBhcmsgU291dGggV2VzdCwgUm95YWwgWW9yayBTb3V0aCBXZXN0PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8zMmUyNjI1Y2EzNTk0OWY1YjlkYzAwODkyZTE1MDY4MS5zZXRDb250ZW50KGh0bWxfYWUwMzdlZWYxOWZlNDQ0NjhkZmZiZTFkYTQyODYwODYpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIGNpcmNsZV9tYXJrZXJfM2NjMDQyM2U2YmU1NDQ5Y2EwNzM2MmE2ZTQ3YTBkOWIuYmluZFBvcHVwKHBvcHVwXzMyZTI2MjVjYTM1OTQ5ZjViOWRjMDA4OTJlMTUwNjgxKTsKCiAgICAgICAgICAgIAogICAgICAgIAo8L3NjcmlwdD4= onload="this.contentDocument.open();this.contentDocument.write(atob(this.getAttribute('data-html')));this.contentDocument.close();" allowfullscreen webkitallowfullscreen mozallowfullscreen></iframe></div></div>


