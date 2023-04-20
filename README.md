**Practical task for William Reed**

***Test URL:** https://wrextdesign.william-reed.com/tests/practical/index.html*

**Overview:**
You are working on implementing the Adobe Datalayer on the above URL. To finish the implementation, you will need to:
1. Write a javascript function that counts the words of the article only (not the comments) and updates DataLayer.article_data.word_count accordingly.
2. Understand why DataLayer.journey_data.is_mobile isn't working and fix as appropriate.
3. Declare DataLayer.article_data.original_article as true when window.location.href matches the content of DataLayer.journey_data.canonical_url

**Pointers:**
- The datalayer is stored under a javascript variable named DataLayer
-  DataLayer.article_data.word_count should return an integer.



**Discussion :**

1. Without editing the HTML, and adding for example an `<article>` tag, querySelectorAll was used and selected all the elements that typically make up the content of the article. The node list elements used the regex expression in the split function to account for extra white space in the text when splitting it into words ,ensuring accuracy,

2. `DataLayer.journey_data.is_mobile` was not working because the function declaration needs to be moved above the invocation of `mobileCheck()`

3. Here the URL is parsed into seperate components and then checked, it is a more robust way than simply comparing strings because the string might have a trailing slash or some other encoded character which will throw the comparison out incorrectly.
