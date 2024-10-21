# Undo-retweets
Remove all retweets on X

- open browser
- navigate to profile page. https://x.com/{yourusername}
- open developer tools. F12
- navigate to the console window
- paste the code below and hit enter
    
 <i>Note: it takes about 2 seconds per retweet</i>

```

setInterval(()=>{
    for (const d of document.querySelectorAll('button[data-testid="unretweet"]')){
        d.click()
        // click 'Undo Repost' to confirm
        document.querySelector('div[data-testid="unretweetConfirm"]').click()
    }
    window.scrollTo(0, document.body.scrollHeight)
}, 1000)

```
