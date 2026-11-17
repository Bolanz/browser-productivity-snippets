# Browser Productivity Snippets 🚀

A personal collection of lightweight JavaScript bookmarklets and browser console snippets designed to speed up daily web browsing, research, and repetitive tasks.

## Included Snippets

### 1. Extract All Links on a Page
Run this in your browser console (`F12` -> Console) or save it as a bookmarklet to quickly list all URLs on the current webpage:

```javascript
javascript:(function(){const links=Array.from(document.querySelectorAll('a')).map(a=>a.href).filter(href=>href.startsWith('http'));console.log([...new Set(links)].join('\n'));alert('Copied/Logged ' + new Set(links).size + ' unique links to Console!');})();
