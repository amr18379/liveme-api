# LiveMe API Reference

** This document is under constant construction and will change periodically **

### getUserInfo

**Syntax:** getUserInfo(userid)

**Parameters:**
*userid* - The User ID of an account.

**Returns:** Object containing all avaialble information on the userid provided if found.

### getVideoInfo

**Syntax:** getVideoInfo(videoid)

**Parameters:**
*videoid* - The Video ID of a video.

**Returns:** Objects containing details on the video with the id of videoid and the user account that posted it.

### getUserReplays

**Syntax:** getUserReplays(userid, page, count)

**Parameters:**
*userid* - The User ID of an account.
*page* - What page to start listing results from (Must be at least 1.)
*count* - How many to list or fetch per page of results.

**Returns:** An array of Objects each describing a video posted by the user still available for replay.

### getChatHistoryForVideo

**Syntax:** getChatHistoryForVideo(chat_url)

**Parameters:**
*chat_url* - The chat url for a video, can be found in the returned data from either **getVideoInfo** or **getUserReplays**.

***Returns:** Returns an array of Objects each describing a message posted.

### performSearch

**Syntax:** performSearch(query, page, count, type, country) 

**Parameters:**
*query* - Containing what to search for, depending on type of search.  Can be a partial or full User's name or a hashtag.
*page* - What page to start listing results from (Must be at least 1.)
*count* - How many to list or fetch per page of results.
*type* - Set to 1 if searching by User's name, or 2 if performing a hashtag search.
*country* - (Optional) The country code you would like to limit your search to.

**Returns:** An array of Objects with minimal information.
