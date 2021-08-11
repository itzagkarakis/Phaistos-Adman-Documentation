# DISPLAY ADS

---

## Expanding-Creatives

---

1. ### Expandable(Expanding)-Creative

---

- #### Description

    ---

    Tο expanding creative είναι ένα display banner, το οποίο εμφανίζεται στο site, με διαστάσεις και σε θέση που ορίζονται απο τον Publisher.
Ο εκάστοτε χρήστης που παρακολουθεί τη διαφήμιση, έχει τη δυνατότητα με το πάτημα ενός expand κουμπιού, να μεγαλώσει το banner, αυξάνοντας ακαριαία τις διαστάσεις του (οι οποίες έχουν επίσης οριστεί απο τον Publisher). Τέλος, ο χρήστης μπορεί όποτε αυτός θελήσει, να επαναφέρει το banner στις αρχικές του διαστάσεις, απλά πατώντας ένα collapse button.

- #### Properties

    ---

    - &#9745; iframe: Creative iframe asset
    - &#9745; url: Destination Url ??? (could not find it in repo)
    - &#9745; width: Creative's width. Number or array [collapsed, expanded] eg: [300, 600]. When negative, it expands to left
    - &#9745; height: Creative's height. Number or array [collapsed, expanded] eg: [300, 600]. When negative, it expands to top
    - &#9745; offset: Object with top & left offset to adjuct the creative positioning to be visible in the collapsed state ??? (could not find it in repo)
    - &#9745; expand: Boolean. If true, it expands on mouseover. Default false
    - &#9745; collapse: Boolean. if true, it collapses on mouseout. Default false
    - &#9745; expandOnInit(only works in space not in iframe-creative): Boolean. Set true for pre-expanded creatives. Default true
    - &#9745; flow(only when expanded and only for the height): Boolean. If true, it pushes the page content (Pushdown). Default false
    - &#9745; zIndex: Number. Set zIndex level. Default 1999900

    - &#9744; (uid, placeholderRef, iframeRef,(enableMetrics, wmode in adman.js-old)) Exist in repo but not in docs???

- #### Events

    ---

    - &#9745; Supports the basic events callbacks just like the Rectangle Creative
    - &#9745; onExpand 
    - &#9745; onCollapse 

2. ### Expandable-Sticky-Creative

---

- #### Description

    ---

    Το expandable-sticky creative είναι ένα display banner, το οποίο εμφανίζεται στο site, με διαστάσεις ορισμένες απο τον Publisher. Συνήθως τοποθετείται ψηλά ή χαμηλά πάνω στη σελίδα, με διακριτικό τρόπο, έτσι ώστε να μην επηρεάζει άμεσα την πλοήγηση του χρήστη.
 Το Banner αυτό είναι clickable και μόλις ο χρήστης πατήσει σε οποιοδήποτε σημείο πάνω του, γίνεται fullscreen expand ένα layer, πάνω στο οποίο τοποθετείται ένα δεύτερο banner με τη διαφήμιση (διαστάσεων και θέσης ορισμένων απο τον Publisher).Επίσης τοποθετείται και ένα απλό close button, το οποίο μόλις πατηθεί επαναφέρει το χρήστη στην σελίδα που βρισκόταν πριν clickarei.

 - #### Properties

    ---

    - &#9745; teaser: Image URL for the teaser 
    - &#9745; banner: Image or Iframe (.html) URL for the main creative
    - &#9745; width: Number. Necessary when banner is Iframe. Default: 100vw (fullscreen) so the iframe needs to be responsive
    - &#9745; height: Number. Necessary when banner is Iframe. Default: 100vw (fullscreen) so the iframe needs to be responsive
    - &#9745; color: Object. Optional
        - teaser: background color for teaser banner. Default: rgba(0, 0, 0, 0.8)
        - banner: background color for the overlay, around banner. Default: rgba(0, 0, 0, 0.8)
    - &#9745; url: Destination Url
    - &#9745; position: top or bottom. Teaser banner position. Default: top
    - &#9745; closableTeaser: Boolean. Default true. If teaser should have close button
    - &#9744; (uid, placeholderRef, iframeRef, zindex, mode(*only click is working swipe, click), iframe) Exist in repo but not in docs???

- #### Events

    ---

    - onExpand ???
    - onCollapse ???

---

## Floating-Creatives

---

- ### Description

    ---

    Το floating creative είναι ένα display banner, το οποίο εμφανίζεται στο site, με διαστάσεις και σε θέση που ορίζονται απο τον Publisher. Παρουσιάζεται, πάνω απο το περιεχόμενο της σελίδας, κρύβοντας ότι βρίσκεται πίσω του.
Μπορεί να ενεργοποιηθεί με διάφορους τρόπους (π.χ με κάποιο click event, με απλό scrolling κ.α).
Απενεργοποιείται πατώντας ενα απλό exit button.

- ### Properties

    ---

    - &#9745; iframe or img: Creative asset
    - or wespace and host to render a webspace tag from the speficied ADMAN service
    - &#9745; url: Destination Url
    - &#9745; width: Creative's width (when i frame max is the iframe width. the rest is white space)
    - &#9745; height: Creative's height (when i frame max is the iframe height.the rest is white space)
    - &#9744; top
    - &#9744; bottom
    - &#9744; right
    - &#9744; left
    - scrolling: Boolean. If false, it will be fixed positioned. Default true
    - &#9745; overlay: Boolean. If true, an fullscreen overlay element will be displayed behind the creative. Default false
    - &#9745; overlay_color: String. Set the background color of the overlay element. Default rgba(255, 255, 255, 0.9)
    - &#9745; closer: Boolean or a Srting Url. If true, a default close button will be shown (Closer component). You may give a URL for closer button image. Default false
    - &#9745; responsive: Boolean. If true the creative will be resized (minimized) to fit in screen. Default false
    - &#9745; openInSameWindow: Boolean. If true link open in current tab of Browser, Default false. (Optional) (only in img-creative)
    - &#9744; (uid,placeholder,display, placeholderRef, iframeRef, children, closeCallback, show, setPublicApi, render, invokeEvent, interval(adman.js-old)) Exist in repo but not in docs???

- ### Events

    ---

    - &#9745; onClose

---

## Pushdown-Creatives

---

- ### Description

    ---

    To pushdown creative είναι ένα display banner, το οποίο εμφανίζεται στο site, με διαστάσεις που ορίζονται απο τον Publisher. Συνήθως εμφανίζεται "συρταρωτά" στην πάνω πλευρά του site, μόλις η σελίδα φορτώσει, σπρώχνοντας το περιεχόμενο της σελίδας προς τα κάτω. Η διάρκεια που θα παραμείνει στο σημείο, ορίζεται απο τον Publisher. Mόλις ο χρόνος αυτός περάσει, η διαφήμιση θα εξαφανιστεί με τον ίδιο τρόπο που εμφανίστηκε. Επίσης, ο χρήστης έχει τη δυνατότητα να την κλείσει, απλά πατώντας ενα exit button οποιαδήποτε στιγμή θελήσει.

 - ### Properties

    ---

    - &#9745; height: Number for the height of the creative (image or iframe) in pixels (only effective when number smaller than creative. if bigger then inserts white space)
    - &#9744; weight: Number for the height of the image if the creative has an image. in pixels. (not working)
    - &#9745; width: Number for the width of the creative (image or iframe) in pixels (only effective when number smaller than creative. if bigger then inserts white space)
    - &#9745; backgroundColor: Text. The background color. If the image,the iframe or the webspace don't cover the whole creative this is what will be visible. It can be Hex, rgb, or rgba
    - &#9745; img: Text for the url of the image
    - &#9745; iframe: Text for the url of the iframe
    - &#9744; (uid, placeholderRef, iframeRef, publicApi, url, color,&#9745; tranzition,&#9745; button, dataset,&#9745; secondsToClose) Exist in repo but not in docs???
    
    #### Providing webspace id

    - &#9745; webspace: webspace id
    - &#9745; host: Adman host service

    #### Header-bidding Props

    - sizes: Optional. Required when bidders set. Array of ad alternatives sizes for header-bidding eg. [[300, 250], [300, 600]]
    - bidders: Optional. Object with bidder name and adunit id for post-bidding
    - biddersQueue: Optional. Array of bidders (as above) for performing sequential header-biddings when bidders hasn't any won ad
    - sellerId: Seller id for Supply Chain object. Should correspond to current site entry seller_id found here https:www.phaistosnetworks.gr/_functions/SellersJson


- ### Events

    ---

    ?????????

---

## Rectangle(Flash)-Creatives

---

- ### Description

    ---

    Το rectangle creative είναι η απλούστερη μορρφή display banner διαφήμισης. Παίρνει θέση στο site καθώς και διαστάσεις από τον Publisher και αποτελεί απλά μία σταθερή σε θέση και μέγεθος διαφήμιση.

 - ### Properties

    ---

    - &#9745; iframe: Creative iframe asset
    - &#9745; url: Destination Url (could not find it in repo)
    - &#9745; width: Creative's width (effective when number smaller than iframe)
    - &#9745; height: Creative's height (effective when number smaller than iframe)
    - &#9744; htmlVars: Object with key - value additional Urls for tracking interactions (could not find it in repo)
    - &#9744; (uid, placeholderRef, iframeRef +(adman.js-old)) Exist in repo but not in docs???

- ### Events

    ---

    - &#9745; onInit
    - &#9745; onLoad
    - &#9745; onClick
    - &#9745; onOver
    - &#9745; onOut
    - &#9744; onYes: Fires when creative is visible
    - &#9744; onNo: Fires when creative isn't visible
    - &#9744; onSubmit: Fires when viewability is submitted

---

## Scroller-Creatives

---

- ### Description

    ---

    Το scroller creative είναι ένα display banner, το οποίο εμφανίζεται στο site, με διαστάσεις και σε θέση που ορίζονται απο τον Publisher.
 Όταν ο χρήστης κατά την πλοήγησή του στη σελίδα, φτάσει στο σημείο που έχει τοποθετηθεί το banner, τότε καθώς scrollarei βλέπει σταδιακά διαφορετικό μέρος της σταθερής διαφήμισης(στο εσωτερικό του banner, το οποίο περνάει πάνω απο το ad και λειτουργεί σαν παράθυρο).

 - ### Properties

    ---

    - &#9745; header: Text for header or false to disable it. Default: Advertisment
    - &#9745; footer: Text for footer or false to disable it. Default: Scroll to continue
    - &#9745; insertAfter or insertBefore or the Scroller ad will be placed inline after the currentScript
    - &#9745; fixedHeight: if true resize 50% creative. Default is false
    - &#9744; stayInFrame: if true window looks inside iframe. Default is false (could not find it in repo)???
    - &#9744; (uid, placeholderRef, iframeRef, setPublicApi, fallbacks, dataset) Exist in repo but not in docs???

    #### For Direct campaigns

    - &#9745; iframe: Creative iframe
    - &#9745; width: creative width. Default 100vw when iframe given (responsive)
    - &#9745; height: creative height. Default: 100vh when iframe given (responsive)
    - &#9745; url: Destination URL (could not find it in repo)??? (cursor pointer)

    #### Providing webspace id

    - &#9745; webspace: webspace id
    - &#9745; host: Adman host service

    #### Header-bidding Props

    - sizes: Optional. Required when bidders set. Array of ad alternatives sizes for header-bidding eg. [[300, 250], [300, 600]]
    - bidders: Optional. Object with bidder name and adunit id for post-bidding
    - biddersQueue: Optional. Array of bidders (as above) for performing sequential header-biddings when bidders hasn't any won ad
    - sellerId: Seller id for Supply Chain object. Should correspond to current site entry seller_id found here https:www.phaistosnetworks.gr/_functions/SellersJson

- ### Events

    ---

    ???????????


 ---

 ## Sidekick-Creatives

 ---

 - ### Description

    ---

    To sidekick creative είναι ένα display banner, το οποίο εμφανίζεται στο site, με διαστάσεις και σε θέση που ορίζονται απο τον Publisher. Εκτός απο τη διαφήμιση, περιέχει και ενα button το οποίο αν πατηθεί απο το χρήστη κάνει trigger ένα δεύτερο banner που εμφανίζεται στη σελίδα "συρταρωτά" και περιέχει display ή video διαφήμιση. Επίσης περιέχει και ένα exit button το οποίο μπορεί να clickarei ο χρήστης και να επαναφέρει τη σελίδα στην αρχική της μορφή.

- ### Properties

    ---

    - fixed: Object these attributes:

        - iframe: Creative iframe asset
        - url: Destination Url
        - width: Creative's width
        - height: Creative's height
    - slide: as above
    - (uid, placeholderRef, iframeRef, invokeEvent, expanded+ offset(adman.js-old)) Exist in repo but not in docs???

- ### Events

    ---

    ?????????

 ---

 ## Slider-Creatives

 ---

 - ### Description
    
    ---

    Το slider creative είναι ένα display banner, το οποίο εμφανίζεται στο site, με διαστάσεις ορισμένες απο τον Publisher. Συνήθως τοποθετείται ψηλά ή χαμηλά πάνω στη σελίδα, με διακριτικό τρόπο, έτσι ώστε να μην επηρεάζει άμεσα την πλοήγηση του χρήστη. Εκτός απο τη διαφήμιση, περιέχει και ενα button το οποίο αν πατηθεί απο το χρήστη, σε στέλνει "συρταρωτά" σε μία δεύτερη σελίδα. Εκεί υπάρχει νέο banner με display ή video διαφήμιση. Μέσω exit button επιστρέφουμε στην αρχική σελίδα.

  - ### Properties

    ---

    - fixed: Object these attributes:

        - iframe: Creative iframe asset
        - url: Destination Url
        - width: Creative's width
        - height: Creative's height
    - slide: as above
    - (uid, placeholderRef, iframeRef, invokeEvent, expanded) Exist in repo but not in docs???

- ### Events

    ---

    ?????????

 ---

 ## Sticky-Creatives

 ---

 - ### Description

    ---

    To sticky creative είναι ένα display banner, το οποίο εμφανίζεται στο site, με διαστάσεις και σε θέση που ορίζονται απο τον Publisher. Εμφανίζεται συνήθως "συρταρωτά", είτε απο το πλάι, είτε απο την πάνω, είτε απο την κάτω πλευρά του site. Σε οποιαδήποτε περίπτωση, κατά το scrolling, παραμένει "κολλημένο" στο σημείο που εμφανίστηκε.

    - ### Properties

    ---

    - &#9745; host: ADMAN service URL
    - &#9745; webspace: webspace id
    - &#9744; fallbacks: array of webspaces ids that are used in the fallback chain, webspace fetching another webspace with Openx creatives involved
    - &#9745; top: Number in pixels. If 0 it sticks to top
    - &#9745; bottom: Number in pixels. If 0 it sticks to bottom
    - &#9745; right: Number in pixels. If 0 it sticks to right
    - &#9745; left: Number in pixels. If 0 it sticks to left
    - &#9745; arrow: Boolean. Display or not the arrow button. Default true
    - &#9745; zIndex: Number. Set zIndex level. Default 2147483647
    - &#9745; closeTimeout: Number of seconds interval for closing the Sticky creative. Default 20
    - &#9745; closeOnCollapse: Boolean. Default false. If true, the creatives disappears after closing (throught arrow). If false, the arrow button will be still visible in order to be able to reveal the creative again (for the remaining time(closeTimeout) of the creative)
    - &#9744; events: array of events that will trigger the webspace call Default: ['scroll', 'touchstart', 'touchmove'] More options load, DOMContentLoaded For ASAP triggering webspace provide an empty array: []
    - &#9744; (uid, placeholderRef, setPublicApi, elementsToHide, responsive, invokeEvent) Exist in repo but not in docs???

    #### Header-bidding Props

    - sizes: Optional. Required when bidders set. Array of ad alternatives sizes for header-bidding eg. [[300, 250], [300, 600]]
    - bidders: Optional. Object with bidder name and adunit id for post-bidding
    - biddersQueue: Optional. Array of bidders (as above) for performing sequential header-biddings when bidders hasn't any won ad
    - sellerId: Seller id for Supply Chain object. Should correspond to current site entry seller_id found here https:www.phaistosnetworks.gr/_functions/SellersJson

 ---

 ## Skin-Creative

 ---

 - ### Description

    ---

    To skin creative "ντύνει" το site μας, προσθέτοντας στα πλάγια και (εφόσον επιθυμεί ο Publisher) πάνω απο το περιεχόμενο της σελίδας, banners στα οποία μπορεί να προστεθούν διαφημίσεις, οι οποίες θα ακολουθούν κατά το scrolling.

- ### Publisher-Properties

    ---

    - &#9745; contentWidth: 1300,  type: number || array | Content width of site
   multiple contentWidths
   contentWidth: [1300, {  default contentWidth will be 1300
      1200: 800,  on screen size 1200, contentWidth value will change to 800
      1000: 500   on screen size 1000, contentWidth value will change to 500
   }],
    - &#9745; followElement: 'nav',  type: string | Element to be followed on scroll
    - &#9745; followOffset: 100,  type: number | An offset to be added to the element we follow
    - &#9745; stopFollowing: {
    at: 100,  type: number | After X pixel to stop following the element asigned above,
    hold: 100,  type: number | After X stop following if hold is different than the top of the page assign number here
  },
    - &#9744; debug: false,  type: boolean | Enable to get logs
    - &#9744; alternatives: [
     ...
    {
      method: 'find',  type: string | will search for the element found at el attribute
      el: '#elem',  type: string ^
      options: {  object with every attr you want to be modified
        followElement: '.element',
        stopFollowing: {
          at: 300
        }
      }
    },
    {
      method: 'match',
      page: '/category/',  type: string | Will regex to match page href,
      options: {  object with every attr you want to be modified
        followElement: '.element',
        stopFollowing: {
          at: 300
        }
      }
    }
     ...
  ],
    styles: {  anything under the folder styles/index.js can be modified here
    'adman-skin': {  e.g. adman-skin or adman-skin-left
      zIndex: 5  use styles like you do on js
    },
  }

- ### Template-Properties

    ---

    - &#9745; top: 'obj.adman.gr/talos/2019/tempo/19698/top.gif'  top is currently not implemented. We expose it in order to use it on athinorama's callback.
    - &#9745; left: 'obj.adman.gr/talos/2019/tempo/19698/left.gif'
    - &#9745; right: 'obj.adman.gr/talos/2019/tempo/19698/right.gif'

            iframe example 
            top: 'obj.adman.gr/talos/2019/tempo/19392/gaming_top/index.html'
            left: 'obj.adman.gr/talos/2019/tempo/19392/gaming_left/index.html'
            right: 'obj.adman.gr/talos/2019/tempo/19392/gaming_right/index.html'

    - &#9745; click: '$DESTINATION'
    - &#9745; color: '#000',  background color behind images/iframes
    - &#9744; viewabilityWidth: 200,  if defined, a viewability box will be created with width
    - &#9744; viewabilityHeight: 500,  if defined (also requires viewabilityWidth), will override height for viewability box. If not declared, height of creative will be used
    - &#9745; responsive: true,  if true, skin sides will be resized base on the available space
    - &#9745; width: 400,  actual skin width
    - &#9745; height: 900,  actual skin height
    - &#9745; admanAdId: $ADMAN_AD_ID,  will always be like this (macro that returns instance id, used to measure viewability)

            beneficialWidth: 0.4,  minimum percent of skin width we need visible, default is width / 2


   - &#9745; publishers: {  e.g. override specs for localhost
    localhost: {  you can use the same object/options like the in Available publisher options section above
      followElement: '.element'
    }
  }

            define this object if you need to override or create object for a specific publisher

- ### Questions-skin

    - what is hideAt in template-properties at the repo skin example ???

 ---

 ## Interstitial-Creative ??????????????

 ---

  ---

 ## HBCreative-Creative ??????????????

 ---

 ---

 ## PostBid-Creative ??????????????

 ---

 ## Html5_sync-Creative ??????????????

 ---