l[![Go Report Card](https://goreportcard.com/badge/github.com/hostinger/fireactions)](https://goreportcard.com/report/github.com/hostinger/fireactions)

![Banner](docs/img/banner_violet.png)

Fireactions is an orchestrator for GitHub runners. BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure [Firecracker](https://firecracker-microvm.github.io/) based virtual machines.

> [!IMPORTANT]
> There's been multiple improvements with a lot of breaking changes. The current stable version is **v2.0.0**. Please use this version for production environments.

<!--
https://excalidraw.com/#json=GrJMj6LLYt39mgC0me7Di,C65TV9FhicnxNKgPeRhi3A
sequenceDiagram
    autonumber
    participant Fireactions
    participant Configuration file (YAML)
    participant Pool(s)
    participant Firecracker VM with GitHub runner
    participant GitHub

    Fireactions->>Configuration file (YAML): Load pools
    Fireactions->>Pool(s): Start pool(s)
    loop Ensure min amount of GitHub runners every 1s
        Pool(s)->>GitHub: Create JIT GitHub runner token
        Pool(s)->>Firecracker VM with GitHub runner: Start Firecracker VM
        Firecracker VM with GitHub runner->>GitHub: Run GitHub workflow job
        Firecracker VM with GitHub runner->>Pool(s): Exit (on workflow job finish)
    end
    GitHub->>Fireactions: Scale pool on workflow_job event
-->
![Architecture](docs/img/architecture.png)

Several key features:

- **Scalable**

  Pool based scaling approach. Fireactions always ensures the minimum amount of GitHub runners in the pool.

- **Ephemeral**

  Each virtual machine is created from scratch and destroyed after the job is finished, no state is preserved between jobs, just like with GitHub hosted runners.

- **Customizable**

  Define job labels and customize virtual machine resources to fit Your needs.

## Quickstart

bash
$ fireactions --help
BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure Firecracker based virtual machines.

# Molar Masses: "28.013,31.998,39.948
 --StartSwitch("-'1*");
    --End("*,-'1*);
** seqence: "*1*123*"
## Lï17īD D5 F7ßîœñ: " fusia energy Release ½MaVa²+½MbV²/b=ᐛD-D-fusia carrys 75% energy,
Bio-metric: PnPoe-mgh/kT
<=∞=><∞>
[FirebaseApp.AUTH()
[getauth()Firebaseapp][authdomain]measure ID

<!DOCTYPE html>
<html lang="en-US"> 
<head>
<meta charset="UTF-8"><meta http-equiv="Content-Type" content="text/html;charset=UTF-8">

<IEEE: 802.16: (wifi-max)wireless-communication
E:\/volume/medical>

• windows(DOS): [c:\>]
• OS_X(BASHSHELL): my-imac:/me$
• Linux(BASHSHELL)[root@myserver/]#

     function double (x)
{
    $y = 2*x;
    return $y;
}
    mac address: 00:0d:83:b1:c0:8e
    bits: 1010_1111
- bb74
- BB74
- IEEE-1394,FIREWIRE,HIGHSPEED:
<dir>
<1s>
  String: "1010" (s): i = 0

## <script>document.seraph_accel_usbpb=document.createElement;seraph_accel_izrbpb={add:function(b,a=10){void 0===this.a[a]&&(this.a[a]=[]);this.a[a].push(b)},a:{}}</script> 
<title>Energy Infrastructure &amp; Utility Services | Centuri</title> <meta 

## http-equiv="x-ua-compatible" content="ie=edge"> <meta name="viewport" content="width=device-width, initial-scale=1"> 

## <meta name="format-detection" content="telephone=no"> 

## <script async src="https://www.googletagmanager.com/gtag/js?id=G-YBBV48SHVE" type="o/js-lzl"></script> 

## <script type="o/js-lzl">
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());
      gtag('config', 'G-YBBV48SHVE');
          </script>

## <script type="o/js-lzl">(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
    new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
    j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
    'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
    })(window,document,'script','dataLayer','GTM-5LNVMH89');</script> 
<meta name="robots" content="index, follow, max-image-preview:large, max-snippet:-1, max-video-preview:-1"> 
<meta name="description" content="We are an infrastructure company that builds &amp; maintains energy networks for utilities, focusing on sustainable and clean energy solutions across North America."> 
<link rel="canonical" href="https://centuri.com/"> 
<meta property="og:locale" content="en_US"> <meta property="og:type" content="website"> <meta property="og:title" content="Energy Infrastructure &amp; Utility Services | Centuri"> 
<meta property="og:description" content="We are an infrastructure company that builds &amp; maintains energy networks for utilities, focusing on sustainable and clean energy solutions across North America."> <meta property="og:url" content="https://centuri.com/"> <meta property="og:site_name" content="Centuri"> <meta property="article:publisher" content="https://www.facebook.com/CenturiGroup"> <meta property="article:modified_time" content="2026-08-20T18:04:59+00:00"> <meta name="twitter:card" content="summary_large_image"> <meta name="twitter:site" content="@nextcenturi"> <script type="application/ld+json" class="yoast-schema-graph">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https://centuri.com/","url":"https:\/\/centuri.com/","name":"Energy Infrastructure & Utility Services | Centuri","isPartOf":{"@id":"https://centuri.com\/#website"},"about":{"@id":"https://centuri.com/#organization"},"datePublished":"2022-08-29T20:28:00+00:00","dateModified":"2026-08-20T18:04:59+00:00","description":"We are an infrastructure company that builds & maintains energy networks for utilities, focusing on sustainable and clean energy solutions across North America.","breadcrumb":{"@id":"https:\/\/centuri.com\/#breadcrumb"},"inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":
["https://centuri.com\/"]}]},{"@type":"BreadcrumbList","@id":"https://centuri.com/#breadcrumb","itemListElement":
[{"@type":"ListItem","position":1,"name":"Home"}]},
{"@type":"WebSite","@id":"https:\/\/centuri.com/#website","url":"https://centuri.com/","name":"Centuri","description":"Think Ahead","publisher":{"@id":"https:\/\/centuri.com\/#organization"},"potentialAction":[{"@type":"SearchAction","target":{"@type":"EntryPoint","urlTemplate":"https:\/\/centuri.com\/?s={search_term_string}"},"query-input":{"@type":"PropertyValueSpecification","valueRequired":true,"valueName":"search_term_string"}}],"inLanguage":"en-US"},{"@type":"Organization","@id":"https:\/\/centuri.com\/#organization","name":"Centuri","url":"https:\/\/centuri.com\/","logo":{"@type":"ImageObject","inLanguage":"en-US","@id":"https:\/\/centuri.com\/#\/schema\/logo\/image\/","url":"https:\/\/centuri.com\/wp-content\/uploads\/2022\/09\/Centuri-Primary-Logo-Horizontal.svg","contentUrl":"https:\/\/centuri.com\/wp-content\/uploads\/2022\/09\/Centuri-Primary-Logo-Horizontal.svg","width":175,"height":44,"caption":"Centuri"},"image":{"@id":"https:\/\/centuri.com\/#\/schema\/logo\/image\/"},"sameAs":["https:\/\/www.facebook.com\/CenturiGroup","https:\/\/x.com\/nextcenturi"]}]}</script> <link rel="alternate" title="oEmbed (JSON)" type="application/json+oembed" href="https://centuri.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fcenturi.com%2F"> <link rel="alternate" title="oEmbed (XML)" type="text/xml+oembed" href="https://centuri.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fcenturi.com%2F&amp;format=xml">       <script id="jquery-core-js" src="https://centuri.com/wp-includes/js/jquery/jquery.min.js?ver=3.7.1" type="o/js-lzl"></script> <link rel="https://api.w.org/" href="https://centuri.com/wp-json/"><link rel="alternate" title="JSON" type="application/json" href="https://centuri.com/wp-json/wp/v2/pages/5"><link rel="EditURI" type="application/rsd+xml" title="RSD" href="https://centuri.com/xmlrpc.php?rsd"> <link rel="shortlink" href="https://centuri.com/">  <script type="o/js-lzl">document.addEventListener('DOMContentLoaded', function () {
    document.querySelectorAll('button, a.button, .btn, [role="button"]').forEach(function (el) {
        el.addEventListener('click', function (e) {
            var target = el.getAttribute('href') || el.dataset.href || el.dataset.url;
            if (target) {
                e.preventDefault();
                window.location.href = target;
                return;
            }

            // If it's meant to submit a form
            var form = el.closest('form');
            if (form) {
                e.preventDefault();
                if (typeof form.requestSubmit === 'function') {
                    form.requestSubmit();
                } else {
                    form.submit();
                }
            }
        }, true);
    });
});

document.querySelectorAll('.menu-item-has-children > a').forEach(link => {

    link.onclick = function(e) {
        e.preventDefault();
        e.stopPropagation();

        const submenu = this.nextElementSibling;

        if (submenu.style.display === 'block') {
            submenu.style.display = 'none';
            this.setAttribute('aria-expanded', 'false');
        } else {
            submenu.style.display = 'block';
            this.setAttribute('aria-expanded', 'true');
        }

        return false;
    };

});

let timer;

document.querySelectorAll('.menu-item-has-children').forEach(item => {
    const submenu = item.querySelector('.sub-menu');
    if (!submenu) return;

    item.addEventListener('mouseenter', () => {
        clearTimeout(timer);
        submenu.style.display = 'block';
    });

    item.addEventListener('mouseleave', () => {
        timer = setTimeout(() => {
            submenu.style.display = 'none';
        }, 250); // Adjust 250–400ms if needed
    });

    submenu.addEventListener('mouseenter', () => {
        clearTimeout(timer);
        submenu.style.display = 'block';
    });
});
</script><script type="o/js-lzl">
function openPopup(e) {
  e.preventDefault(); // prevent default link behavior
  const url = e.currentTarget.href;
  window.open(
    url,
    'instagramPopup',
    'width=600,height=600,scrollbars=yes,resizable=yes',
  );
}
</script><script type="o/js-lzl">document.addEventListener('DOMContentLoaded', function () {
    // Get all the list items inside .data-area
    var listItems = document.querySelectorAll('.data-area li');
    
    // Loop through each item
    listItems.forEach(function(item) {
      var label = item.querySelector('.label');
      
      // Check the label content and adjust the width accordingly
      if (label) {
        if (label.textContent.trim() === 'Capabilities' || label.textContent.trim() === 'Capability') {
          item.style.width = '100%';  // Set width to 100% for Capabilities
        } else if (label.textContent.trim() === 'Completion') {
          item.style.width = '30%';   // Set width to 30% for Completion
        } else {
          item.style.width = 'auto';  // Default width for other items
        }
      }
    });
  });

</script><script type="o/js-lzl">document.addEventListener('DOMContentLoaded', function () {
    // Get all the list items inside .data-area
    var listItems = document.querySelectorAll('.single-project .data-area li');
    
    // Loop through each item
    listItems.forEach(function(item) {
      var label = item.querySelector('.label');
      
      // Check if the label text is "Company"
      if (label && label.textContent.trim() === 'Company') {
        item.style.display = 'none';  // Hide the item
      }
    });
  });
</script><link rel="icon" href="https://centuri.com/wp-content/uploads/2023/10/centuri-avatar-symbol-2x.webp" sizes="32x32"> <link rel="icon" href="https://centuri.com/wp-content/uploads/2023/10/centuri-avatar-symbol-2x.webp" sizes="192x192"> <link rel="apple-touch-icon" href="https://centuri.com/wp-content/uploads/2023/10/centuri-avatar-symbol-2x.webp"> <meta name="msapplication-TileImage" content="https://centuri.com/wp-content/uploads/2023/10/centuri-avatar-symbol-2x.webp">    <script src="https://static.elfsight.com/platform/platform.js" data-use-service-core defer></script> <noscript><style>.lzl{display:none!important;}</style></noscript><style>img.lzl,img.lzl-ing{opacity:0.01;}img.lzl-ed{transition:opacity .25s ease-in-out;}</style><style id="wp-img-auto-sizes-contain-inline-css">img:is([sizes=auto i],[sizes^="auto," i]){contain-intrinsic-size:3000px 1500px}</style><style id="classic-theme-styles-inline-css"></style><link id="classic-theme-styles-inline-css-nonCrit" rel="stylesheet/lzl-nc" href="/wp-content/cache/seraphinite-accelerator/s/m/d/css/2/0b/431ab6ecd62bdb35135b32eb9456a.100.css"><noscript lzl=""><link rel="stylesheet" href="/wp-content/cache/seraphinite-accelerator/s/m/d/css/2/0b/431ab6ecd62bdb35135b32eb9456a.100.css"></noscript><style id="global-styles-inline-css">:root{--wp--preset--aspect-ratio--square:1;--wp--preset--aspect-ratio--4-3:4/3;--wp--preset--aspect-ratio--3-4:3/4;--wp--preset--aspect-ratio--3-2:3/2;--wp--preset--aspect-ratio--2-3:2/3;--wp--preset--aspect-ratio--16-9:16/9;--wp--preset--aspect-ratio--9-16:9/16;--wp--preset--color--black:#000;--wp--preset--color--cyan-bluish-gray:#abb8c3;--wp--preset--color--white:#fff;--wp--preset--color--pale-pink:#f78da7;--wp--preset--color--vivid-red:#cf2e2e;--wp--preset--color--luminous-vivid-orange:#ff6900;--wp--preset--color--luminous-vivid-amber:#fcb900;--wp--preset--color--light-green-cyan:#7bdcb5;--wp--preset--color--vivid-green-cyan:#00d084;--wp--preset--color--pale-cyan-blue:#8ed1fc;--wp--preset--color--vivid-cyan-blue:#0693e3;--wp--preset--color--vivid-purple:#9b51e0;--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple:linear-gradient(135deg,#0693e3 0%,#9b51e0 100%);--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan:linear-gradient(135deg,#7adcb4 0%,#00d082 100%);--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange:linear-gradient(135deg,#fcb900 0%,#ff6900 100%);--wp--preset--gradient--luminous-vivid-orange-to-vivid-red:linear-gradient(135deg,#ff6900 0%,#cf2e2e 100%);--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray:linear-gradient(135deg,#eee 0%,#a9b8c3 100%);--wp--preset--gradient--cool-to-warm-spectrum:linear-gradient(135deg,#4aeadc 0%,#9778d1 20%,#cf2aba 40%,#ee2c82 60%,#fb6962 80%,#fef84c 100%);--wp--preset--gradient--blush-light-purple:linear-gradient(135deg,#ffceec 0%,#9896f0 100%);--wp--preset--gradient--blush-bordeaux:linear-gradient(135deg,#fecda5 0%,#fe2d2d 50%,#6b003e 100%);--wp--preset--gradient--luminous-dusk:linear-gradient(135deg,#ffcb70 0%,#c751c0 50%,#4158d0 100%);--wp--preset--gradient--pale-ocean:linear-gradient(135deg,#fff5cb 0%,#b6e3d4 50%,#33a7b5 100%);--wp--preset--gradient--electric-grass:linear-gradient(135deg,#caf880 0%,#71ce7e 100%);--wp--preset--gradient--midnight:linear-gradient(135deg,#020381 0%,#2874fc 100%);--wp--preset--font-size--small:13px;--wp--preset--font-size--medium:20px;--wp--preset--font-size--large:36px;--wp--preset--font-size--x-large:42px;--wp--preset--spacing--20:.44rem;--wp--preset--spacing--30:.67rem;--wp--preset--spacing--40:1rem;--wp--preset--spacing--50:1.5rem;--wp--preset--spacing--60:2.25rem;--wp--preset--spacing--70:3.38rem;--wp--preset--spacing--80:5.06rem;--wp--preset--shadow--natural:6px 6px 9px rgba(0,0,0,.2);--wp--preset--shadow--deep:12px 12px 50px rgba(0,0,0,.4);--wp--preset--shadow--sharp:6px 6px 0px rgba(0,0,0,.2);--wp--preset--shadow--outlined:6px 6px 0px -3px #fff,6px 6px #000;--wp--preset--shadow--crisp:6px 6px 0px #000}:where(body){margin:0}body{padding-top:0;padding-right:0;padding-bottom:0;padding-left:0}</style><link id="global-styles-inline-css-nonCrit" rel="stylesheet/lzl-nc" href="/wp-content/cache/seraphinite-accelerator/s/m/d/css/2/9f/4520c499f90d7265c0a9a6ecb2f11.174a.css"><noscript lzl=""><link rel="stylesheet" href="/wp-content/cache/seraphinite-accelerator/s/m/d/css/2/9f/4520c499f90d7265c0a9a6ecb2f11.174a.css"></noscript><style id="cff-css-crit" media="all">#cff{float:left;width:100%;margin:0 auto;padding:0;-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box}.cff-header .fa,.cff-header svg{margin:0 10px 0 0;padding:0}.cff-visual-header .cff-likes-box .cff-square-logo svg{width:18px;vertical-align:top}.cff-visual-header .cff-bio-info svg{display:inline-block;width:1em;vertical-align:middle;position:relative;top:-2px}.cff-posts-count svg{padding-right:3px}#cff .cff-post-desc,#cff h3,#cff h4,#cff h5,#cff h6,#cff p{float:left;width:100%;clear:both;padding:0;margin:5px 0;word-wrap:break-word}#cff .cff-share-tooltip a .fa,#cff .cff-share-tooltip a svg{font-size:16px;margin:0;padding:5px}#cff #cff-error-reason{display:none;padding:5px 0 0;clear:both}.sb-elementor-cta-img span svg{width:32px;fill:#257ab2;float:left!important}</style><link rel="stylesheet/lzl-nc" id="cff-css" href="https://centuri.com/wp-content/cache/seraphinite-accelerator/s/m/d/css/5/4c/8173b692035e7bad094c1c27cea29.646d.css" media="all"><noscript lzl=""><link rel="stylesheet" href="https://centuri.com/wp-content/cache/seraphinite-accelerator/s/m/d/css/5/4c/8173b692035e7bad094c1c27cea29.646d.css" media="all"></noscript><style id="sb-font-awesome-css-crit" media="all">@font-face{font-family:"FontAwesome";src:url("/wp-content/plugins/custom-facebook-feed/assets/css/../fonts/fontawesome-webfont.eot?v=4.7.0");src:url("/wp-content/plugins/custom-facebook-feed/assets/css/../fonts/fontawesome-webfont.eot?#iefix&v=4.7.0") format("embedded-opentype"),url("/wp-content/plugins/custom-facebook-feed/assets/css/../fonts/fontawesome-webfont.woff2?v=4.7.0") format("woff2"),url("/wp-content/plugins/custom-facebook-feed/assets/css/../fonts/fontawesome-webfont.woff?v=4.7.0") format("woff"),url("/wp-content/plugins/custom-facebook-feed/assets/css/../fonts/fontawesome-webfont.ttf?v=4.7.0") format("truetype"),url("/wp-content/plugins/custom-facebook-feed/assets/css/../fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular") format("svg");font-weight:400;font-style:normal;font-display:swap}@-webkit-keyframes fa-spin{0%{-webkit-transform:rotate(0deg);transform:rotate(0deg)}100%{-webkit-transform:rotate(359deg);transform:rotate(359deg)}}@keyframes fa-spin{0%{-webkit-transform:rotate(0deg);transform:rotate(0deg)}100%{-webkit-transform:rotate(359deg);transform:rotate(359deg)}}.sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0,0,0,0);border:0}</style><link rel="stylesheet/lzl-nc" id="sb-font-awesome-css" href="https://centuri.com/wp-content/cache/seraphinite-accelerator/s/m/d/css/8/33/f0795fc8d6e5fe5b063ca4f169e1d.6fa6.css" media="all"><noscript lzl=""><link rel="stylesheet" href="https://centuri.com/wp-content/cache/seraphinite-accelerator/s/m/d/css/8/33/f0795fc8d6e5fe5b063ca4f169e1d.6fa6.css" media="all"></noscript><style id="izi-main-css-crit" media="all">html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{margin:0;padding:0;border:0;font-size:100%;font:inherit;vertical-align:baseline}article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}body{line-height:1}ol,ul{list-style:none}.bg-black{background:#000}.row{box-sizing:border-box;display:flex;flex:0 1 auto;flex-direction:row;flex-wrap:wrap;margin-right:-1rem;margin-left:-1rem;width:auto}.col-xs,.col-xs-1,.col-xs-2,.col-xs-3,.col-xs-4,.col-xs-5,.col-xs-6,.col-xs-7,.col-xs-8,.col-xs-9,.col-xs-10,.col-xs-11,.col-xs-12{box-sizing:border-box;flex:0 0 auto;padding-right:1rem;padding-left:1rem}.col-xs-1{flex-basis:8.333%;max-width:8.333%}.col-xs-2{flex-basis:16.667%;max-width:16.667%}.col-xs-3{flex-basis:25%;max-width:25%}.col-xs-4{flex-basis:33.333%;max-width:33.333%}.col-xs-5{flex-basis:41.667%;max-width:41.667%}.col-xs-6{flex-basis:50%;max-width:50%}.col-xs-7{flex-basis:58.333%;max-width:58.333%}.col-xs-8{flex-basis:66.667%;max-width:66.667%}.col-xs-9{flex-basis:75%;max-width:75%}.col-xs-10{flex-basis:83.333%;max-width:83.333%}.col-xs-11{flex-basis:91.667%;max-width:91.667%}.col-xs-12{flex-basis:100%;max-width:100%}@media only screen and (min-width:769px){.col-sm,.col-sm-1,.col-sm-2,.col-sm-3,.col-sm-4,.col-sm-5,.col-sm-6,.col-sm-7,.col-sm-8,.col-sm-9,.col-sm-10,.col-sm-11,.col-sm-12{box-sizing:border-box;flex:0 0 auto;padding-right:1rem;padding-left:1rem}.col-sm-1{flex-basis:8.333%;max-width:8.333%}.col-sm-2{flex-basis:16.667%;max-width:16.667%}.col-sm-3{flex-basis:25%;max-width:25%}.col-sm-4{flex-basis:33.333%;max-width:33.333%}.col-sm-5{flex-basis:41.667%;max-width:41.667%}.col-sm-6{flex-basis:50%;max-width:50%}.col-sm-7{flex-basis:58.333%;max-width:58.333%}.col-sm-8{flex-basis:66.667%;max-width:66.667%}.col-sm-9{flex-basis:75%;max-width:75%}.col-sm-10{flex-basis:83.333%;max-width:83.333%}.col-sm-11{flex-basis:91.667%;max-width:91.667%}.col-sm-12{flex-basis:100%;max-width:100%}}@media only screen and (min-width:993px){.col-md,.col-md-1,.col-md-2,.col-md-3,.col-md-4,.col-md-5,.col-md-6,.col-md-7,.col-md-8,.col-md-9,.col-md-10,.col-md-11,.col-md-12{box-sizing:border-box;flex:0 0 auto;padding-right:1rem;padding-left:1rem}.col-md-1{flex-basis:8.333%;max-width:8.333%}.col-md-2{flex-basis:16.667%;max-width:16.667%}.col-md-3{flex-basis:25%;max-width:25%}.col-md-4{flex-basis:33.333%;max-width:33.333%}.col-md-5{flex-basis:41.667%;max-width:41.667%}.col-md-6{flex-basis:50%;max-width:50%}.col-md-7{flex-basis:58.333%;max-width:58.333%}.col-md-8{flex-basis:66.667%;max-width:66.667%}.col-md-9{flex-basis:75%;max-width:75%}.col-md-10{flex-basis:83.333%;max-width:83.333%}.col-md-11{flex-basis:91.667%;max-width:91.667%}.col-md-12{flex-basis:100%;max-width:100%}}.link,.editor-content a:not(.button),.content-editor a:not(.button),#tinymce a:not(.button){color:var(--theme-color--text-links-tile-headings-tile-border-hover-post-details);transition:250ms;font-weight:700;outline:1px solid transparent;outline-offset:2px}.link:hover,.editor-content a:hover:not(.button),.content-editor a:hover:not(.button),#tinymce a:hover:not(.button),.link:focus,.editor-content a:focus:not(.button),.content-editor a:focus:not(.button),#tinymce a:focus:not(.button){text-decoration:none;color:#000;outline:1px solid}.dark-background .link,.dark-background .editor-content a:not(.button),.editor-content .dark-background a:not(.button),.dark-background .content-editor a:not(.button),.content-editor .dark-background a:not(.button),.dark-background #tinymce a:not(.button),#tinym
```🔥
https://api.ip2location.io/?ip=127.0.0.1
{
    "ip": "127.0.0.1",
    "country_code": "-",
    "country_name": "-",
    "region_name": "-",
    "district": "-",
    "city_name": "-",
    "latitude": null,
    "longitude": null,
    "zip_code": "-",
    "time_zone": "-",
    "asn": "-",
    "as": "-",
    "as_info": {
        "as_number": "-",
        "as_name": "-",
        "as_domain": "-",
        "as_usage_type": "-",
        "as_cidr": "-"
    },
    "isp": "Loopback",
    "domain": "-",
    "net_speed": "-",
    "idd_code": "-",
    "area_code": "-",
    "weather_station_code": "-",
    "weather_station_name": "-",
    "mcc": "-",
    "mnc": "-",
    "mobile_brand": "-",
    "elevation": 0,
    "usage_type": "RSV",
    "address_type": "Unicast",
    "ads_category": "-",
    "ads_category_name": null,
    "continent": {
        "hemisphere": null,
        "translation": {
            "lang": "en",
            "value": null
        }
    },
    "country": {
        "name": "-",
        "alpha3_code": null,
        "numeric_code": null,
        "demonym": null,
        "flag": null,
        "capital": null,
        "total_area": 0,
        "population": 0,
        "currency": {
            "code": null,
            "name": null,
            "symbol": null
        },
        "language": {
            "code": null,
            "name": null
        },
        "tld": null,
        "translation": {
            "lang": "en",
            "value": null
        }
    },
    "region": {
        "name": "-",
        "code": null,
        "translation": {
            "lang": "en",
            "value": null
        }
    },
    "city": {
        "name": "-",
        "translation": {
            "lang": "en",
            "value": null
        }
    },
    "time_zone_info": {
        "olson": null,
        "current_time": "2026-10-02T11:14:08+08:00",
        "gmt_offset": 28800,
        "is_dst": false,
        "dst_start_date": null,
        "dst_end_date": null,
        "sunrise": "13:47",
        "sunset": "01:53"
    },
    "geotargeting": {
        "metro": null
    },
    "is_proxy": false,
    "fraud_score": 0,
    "proxy": {
        "last_seen": 0,
        "proxy_type": "-",
        "threat": "-",
        "provider": "-",
        "is_vpn": false,
        "is_tor": false,
        "is_data_center": false,
        "is_public_proxy": false,
        "is_web_proxy": false,
        "is_web_crawler": false,
        "is_ai_crawler": false,
        "is_residential_proxy": false,
        "is_consumer_privacy_network": false,
        "is_enterprise_private_network": false,
        "is_spammer": false,
        "is_scanner": false,
        "is_botnet": false,
        "is_bogon": false
    }
}
 NETORGFT20489500.onmicrosoft.comNETORGFT20489500.onmicrosoft.comHTTP/2 200 
expires: Thu, 19 Nov 1981 08:52:00 GMT
cache-control: no-store, no-cache, must-revalidate
pragma: no-cache
link: <https://yhwh.com/wp-json/>; rel="https://api.w.org/", <https://yhwh.com/wp-json/wp/v2/pages/6>; rel="alternate"; title="JSON"; type="application/json", <https://yhwh.com/>; rel=shortlink
set-cookie: PHPSESSID=32771a9e1a01996659da3a9f07909a56; path=/
vary: Accept-Encoding
content-type: text/html; charset=UTF-8
date: Fri, 02 Oct 2026 03:07:17 GMT
server: yhwh.com('https://api.ip2location.io/?ip=100.0.0.1')

{
    "ip": "100.0.0.1",
    "country_code": "US",
    "country_name": "United States of America",
    "region_name": "Massachusetts",
    "district": "Suffolk County",
    "city_name": "Boston",
    "latitude": 42.35848,
    "longitude": -71.06007,
    "zip_code": "02117",
    "time_zone": "-04:00",
    "asn": "701",
    "as": "Verizon Business",
    "as_info": {
        "as_number": "701",
        "as_name": "Verizon Business",
        "as_domain": "verizonenterprise.com",
        "as_usage_type": "ISP",
        "as_cidr": "100.0.0.0/16"
    },
    "isp": "Verizon Business",
    "domain": "verizonenterprise.com",
    "net_speed": "DSL",
    "idd_code": "1",
    "area_code": "617",
    "weather_station_code": "USMA0046",
    "weather_station_name": "Boston",
    "mcc": "311",
    "mnc": "480",
    "mobile_brand": "Verizon",
    "elevation": 15,
    "usage_type": "ISP",
    "address_type": "Unicast",
    "ads_category": "419",
    "ads_category_name": "Internet Service Providers",
    "continent": {
        "name": "North America",
        "code": "NA",
        "hemisphere": [
            "north",
            "west"
        ],
        "translation": {
            "lang": "en",
            "value": "North America"
        }
    },
    "country": {
        "name": "United States of America",
        "alpha3_code": "USA",
        "numeric_code": 840,
        "demonym": "Americans",
        "flag": "https://cdn.ip2location.io/assets/img/flags/us.png",
        "capital": "Washington, D.C.",
        "total_area": 9826675,
        "population": 339665118,
        "currency": {
            "code": "USD",
            "name": "United States Dollar",
            "symbol": "$"
        },
        "language": {
            "code": "EN",
            "name": "English"
        },
        "tld": "us",
        "translation": {
            "lang": "en",
            "value": "United States of America"
        }
    },
    "region": {
        "name": "Massachusetts",
        "code": "US-MA",
        "translation": {
            "lang": "en",
            "value": "Massachusetts"
        }
    },
    "city": {
        "name": "Boston",
        "translation": {
            "lang": "en",
            "value": "Boston"
        }
    },
    "time_zone_info": {
        "olson": "America/New_York",
        "current_time": "2026-10-01T23:14:48-04:00",
        "gmt_offset": -14400,
        "is_dst": true,
        "abbreviation": "EST",
        "dst_start_date": "2026-03-08",
        "dst_end_date": "2026-11-01",
        "sunrise": "06:42",
        "sunset": "18:27"
    },
    "geotargeting": {
        "metro": "506"
    },
    "is_proxy": false,
    "fraud_score": 0,
    "proxy": {
        "last_seen": 0,
        "proxy_type": "-",
        "threat": "-",
        "provider": "-",
        "is_vpn": false,
        "is_tor": false,
        "is_data_center": false,
        "is_public_proxy": false,
        "is_web_proxy": false,
        "is_web_crawler": false,
        "is_ai_crawler": false,
        "is_residential_proxy": false,
        "is_consumer_privacy_network": false,
        "is_enterprise_private_network": false,
        "is_spammer": false,
        "is_scanner": false,
        "is_botnet": false,
        "is_bogon": false
    }
}
 ns65.domaincontrol.com. 

dns.jomax.net. 2026082100 28800 7200 604800 600

v=spf1 include:secureserver.net

 -all127.255.255.255ns65.domaincontrol.com. dns.jomax.net. 2026082100 28800 7200 604800 600

#** ∆Y={0:ic<i|AL•(√P-√p(i):i/≤ic<iu
#** ∆L•√(p(iu)-√p(i|)ic>icu/ic<iμ
** ∆X•∆L•√(1/p(i){∆L•(⅛-√p(icu)
#** 0 crossing Tx.6.2.3
#** fo:=fg-fo(66.26),to(i):={+ic≥i
                        {oic<i(6.25

# = f(2)=2²-5×2+6=0&
 
# = f(4(=3²-5×3+6=0;

# = f(x)=x³+3x²-6x-8/4;

# = f3=x³+x²-6x-8÷4;

### Research.Gate.net
(seed),[XLS]_Represents paid>10,000-SSA Aegon],public Safty assets management

  ## Iteland ##

* X=f14.8176
* solution {x=0}
* solution {f14=1/8176}
* solution in Decimal {f14=0.0001223091977,
* dirivatives both sides respect 0=8176X
* differentiate both sides X1=8176f14
* integrating both sides respectto F14 
* f14x=4088f14²x;

** {3xq+4y+5z=6}
** {2x+3y+4z=5}
** {x+2y+3z=4}
** {2=4-x2y/3}

× √5.√2.4/2√5x

× √5.√2.2

× 5.x/✓√x/x.2

× vertical asymptotes: x=0
× horizontal asymptotes: y=0


Usage:
  fireactions [command]

Main application commands:
  server      Starts the server
  agent       Starts the agent and GitHub Actions runner inside the VM

Pool management commands:
  pools       Manage pools

Machine management commands:
  ps          List all running machines across all pools
  login       SSH into a running VM as root user
  logs        Stream logs from the fireactions-agent service inside a machine

Image management commands:
  image       Manage images

Additional Commands:
  version     Show version information
  help        Help about any command
  completion  Generate the autocompletion script for the specified shell

Flags:
  -h, --help      help for fireactions
  -v, --version   version for fireactions

Use "fireactions [command] --help" for more information about a command.
```

See the [Guide](https://fireactions.io/latest/) for installation and configuration instructions.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for more information on how to contribute to Fireactions.
```
 def rotation_matrix(theta):
    c, s = np.cos(theta), np.sin(theta)
    return np.array([[c, -s],
                     [s,  c]])

theta = np.pi / 4   # 45 degrees
R = rotation_matrix(theta)

# Apply to a vector
v = np.array([1.0, 0.0])
v_rotated = R @ v
print("Rotated vector:", v_rotated)# Computational basis
ket0 = np.array([1, 0], dtype=complex)
ket1 = np.array([0, 1], dtype=complex)

# Hadamard action
plus  = H @ ket0          # |+>
minus = H @ ket1          # |->

# X gate action
print("X|0> =", X @ ket0)   # should be |1>
print("X|1> =", X @ ket1)   # should be |0>def rc_current(t, E, R, tau):
    """i(t) = (E/R) * (1 - exp(-t/tau))"""
    return (E / R) * (1 - np.exp(-t / tau))

t = np.linspace(0, 5*0.01, 500)
i = rc_current(t, E=12, R=4.7, tau=0.01)# From one of your pages: X = (Y - 3) / 2
def final_result(Y):
    return (Y - 3) / 2

# Infinite series fragment ∑ X_n / n!
from math import factorial

def series_approx(X, terms=20):
    return sum(X**n / factorial(n) for n in range(terms))

// Rough translation of the control-flow notes
function applicationX(options) {
  // replace = option
  let value = options.replace || null;

  if (!value) {
    // ! # ! # end if  style guard
    return null;
  }

  // trusted-click-element + transform idea
  const transformed = U_transform(value);
  return transformed;
}
options.replace.

### <!doctype html3>

## <html3>
## <tr>
## <td>
## <th>

### IncomeQ3>Defined By $A$3 Absolute Cell Reference "enter",123".

### In Cell May Automatically Change To"$123.00".

### Press Tab Or Enter Or Click Outside The Cell.
Active Cell Is Formatted For Data Or A Text.
Text"1/2/3" 
### May Change To "01/02/2003".
Cell A20 May Contain
### A Formula That Produces The Result Of The Summation Of Cells A1-A25.
Cell 5 May Contain 
### A Formula That Averages All The Numbers In The B Column.
### AAAA.
# AAC videos "live" Or "on-the-fly".
Often Use H.264,HEVC,or VP9.
[#page:one#]

Molar Mass Advantage" "Nitrogen (N2) Oxygen (O2) Argon (Ar) Carbon_Dioxside (O2)