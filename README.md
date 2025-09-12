# Instructions
1. Refresh the "websites" page of which the file you want to download is stored
2. open up the pdf so it is visible
3. load all the pages (by scrolling up or down it a couple of times)
4. Open your developer console and paste the script below or in main.js


Paste it into ChatGPT or Gemini, ask it to tell you what it does if you are worried if it is a virus or smth

## How it works
yo momma

### Script
```
(async()=>{async function e(){if(window.jspdf&&window.jspdf.jsPDF)return window.jspdf.jsPDF;await new Promise((e,t)=>{const n=document.createElement("script");n.src="https://cdn.jsdelivr.net/npm/jspdf@2.5.1/dist/jspdf.umd.min.js",n.onload=e,n.onerror=t,document.head.appendChild(n)});return window.jspdf.jsPDF}const t=await e(),n=Array.from(document.getElementsByTagName("img")).filter(e=>/^blob:/.test(e.src)&&e.naturalWidth>0&&e.naturalHeight>0);if(0===n.length)return console.warn("No images found to export.");let a=new t({unit:"mm",format:"a4",orientation:"p"});function r(e,n,r,o){const i=n>r?"l":"p";if(o){const n=a.internal.pageSize.getWidth()>a.internal.pageSize.getHeight();if("l"===i&&!n||"p"===i&&n)a=new t({unit:"mm",format:"a4",orientation:i})}else a.addPage(void 0,i);let d=a.internal.pageSize.getWidth(),l=a.internal.pageSize.getHeight(),u=10,c=d-2*u,m=l-2*u,f=e=>25.4*e/96,g=f(n),s=f(r),h=Math.min(c/g,m/s,1),p=g*h,w=s*h,v=(d-p)/2,E=(l-w)/2;a.addImage(e,"PNG",v,E,p,w,void 0,"FAST")}function o(e){const t=e.naturalWidth,n=e.naturalHeight,a=document.createElement("canvas");a.width=t;a.height=n;const r=a.getContext("2d");return r.drawImage(e,0,0,t,n),a.toDataURL("image/png")}let i=!1;for(let e=0;e<n.length;e++){const t=n[e];try{const n=o(t);r(n,t.naturalWidth,t.naturalHeight,!i),i=!0}catch(e){console.warn("Skipped one image:",t.src,e)}}a.save("download.pdf")})();
```
