var ASCDP=window.ASCDP||{};ASCDP.adS=ASCDP.adS||{},ASCDP.adS.addVideoAsset=e=>{let t=!1,a=!1,o=!1,i="pause",l="none",d=!1,n=ASCDP.pageSet,s=ASCDP.adS,r=s.adElts[e],c="data-state",p=r.crea1.creativeUrl.split("."),u=p[p.length-1],v=document.createElement("video"),y=()=>{v.paused||0===v.currentTime?(w.setAttribute(c,"play"),v.play().catch()):(w.setAttribute(c,"pause"),v.pause())},b=()=>{var e=s.getScrollTop(),t=s.getWinWidth()+document.body.getBoundingClientRect().left,t="responsive"===r.center?t*r.creas[0].factor:r.creas[0].height,e=(r.posY=s.calcY(r.adSlot,r.adSlot.offsetTop),e+s.getWinHeight()-t/2<r.posY||e>r.posY+t/2?0:1);e&&!v.ended?"pause"===w.getAttribute(c)&&r.play():"play"===w.getAttribute(c)&&r.play()},m=()=>{var e;"m3u8"!==u||v.canPlayType("application/vnd.apple.mpegurl")?(v.src=r.crea1.creativeUrl,r.crea1.options&&r.crea1.options.fallback&&(v.poster=r.crea1.options.fallback),t||r.hasPlayed?r.hasPlayed=!1:y()):window.Hls?Hls.isSupported()?((e=new Hls({maxBufferLength:4})).loadSource(r.crea1.creativeUrl),e.attachMedia(v),e.on(Hls.Events.MANIFEST_PARSED,function(){t||r.hasPlayed?r.hasPlayed=!1:y()})):(v.src=r.crea1.creativeUrl,t||r.hasPlayed?r.hasPlayed=!1:y()):setTimeout(m,50)};r.crea1.options&&(r.crea1.options.loop&&(a=!0),r.crea1.options.mute&&(o=!0),r.crea1.options.autoplay&&"mobile"!==n.connectionType&&(t=!0,o=!0,l="auto",i="play"),r.crea1.options.fallback)&&(v.poster=r.crea1.options.fallback,v.style.backgroundSize=r.crea1.width+"px "+r.crea1.height+"px",r.xtraCSS=r.xtraCSS||"",r.xtraCSS+=`#${e}_videoContentAd video {
                background-image: url('${r.crea1.options.fallback}');
                background-repeat: no-repeat;
            }`),"m3u8"!==u||v.canPlayType("application/vnd.apple.mpegurl")||s.loadModules(["hls"],null,"extensions"),v.id=e+"_video",v.style.width="100%",v.setAttribute("playsinline","true"),v.setAttribute("preload",l),v.autoplay=t,v.muted=o,v.loop=a,v.onclick=()=>{0<v.currentTime?window.open(r.crea1.clickUrl,r.crea1.clickUrlTarget):m()},v.onended=()=>{r.hasPlayed=!0,a||(d=!1,window.removeEventListener("scroll",r.playOnView,!1),w.setAttribute(c,"pause"),v.autoplay=!1,m(),w.style.visibility="hidden",S.style.display="block")};var h=document.createElement("div"),g=(h.id=e+"_videoContentAd",h.classList.add("media-item__video"),document.createElement("div"));g.id=e+"_videoBannerControls";let w=document.createElement("div"),C=(w.setAttribute("class","play"),w.setAttribute(c,i),w.onclick=y,document.createElement("div")),S=(C.setAttribute("class","sound"),C.setAttribute(c,"mute"),C.onclick=()=>{v.muted?(C.setAttribute(c,"loud"),v.muted=!1):(C.setAttribute(c,"mute"),v.muted=!0)},document.createElement("div"));return S.id="videoBoardPlay",S.onclick=()=>{S.style.display="none",o||C.setAttribute(c,"loud"),m(),w.style.visibility="visible"},S.style.cssText='background: url("https://www.asadcdn.com/adlib/img/play_circle.svg");background-size: cover; z-index: 500; position: absolute; display: block; width: 60px; height: 60px;margin: auto; left:0; right:0; top:0; bottom:0;',g.appendChild(w),g.appendChild(C),h.appendChild(g),h.appendChild(v),h.appendChild(S),m(),t?(S.style.display="none",window.addEventListener("scroll",b,!1)):(w.style.visibility="hidden",h.addEventListener("play",()=>{d||(d=!0,window.addEventListener("scroll",b,!1))},!1)),r.xtraCSS+=`#${e}_videoBannerControls {
            overflow-x: visible; position: absolute; left: 0; bottom: 0px; z-index: 10; width: 100%; height: 0;
        }
        #${e}_videoBannerControls > div {
            position: absolute; height: 30px; top: -30px;
        }
        #${e}_videoBannerControls .play[data-state='pause']{
            background: url(https://www.asadcdn.com/adlib/img/play_square.svg);
        }
        #${e}_videoBannerControls .play[data-state='play']{
            background: url(https://www.asadcdn.com/adlib/img/pause_square.svg);
        }
        #${e}_videoBannerControls .sound[data-state='loud']{
            background: url(https://www.asadcdn.com/adlib/img/sound_on.svg);
        }
        #${e}_videoBannerControls .sound[data-state='mute']{
            background: url(https://www.asadcdn.com/adlib/img/sound_off.svg);
        }
        #${e}_videoBannerControls .play{
            left: 0; width:30px;
        }
        #${e}_videoBannerControls .sound{
            right: 0; width:30px;
        }`,h};