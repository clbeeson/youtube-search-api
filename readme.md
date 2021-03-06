# Youtube Search API

Youtube Search API is an API for getting Youtube search results.

## Installation

```bash
npm install youtube-search-api
```

## Usage (import)

```node
var youtubesearchapi=require('youtube-search-api');
```
## GetListByKeywords (Promise)
```node
youtubesearchapi.GetListByKeyword("<keywords>",[playlist boolean])
```
GetListByKeywords Result
```node
{items:[],nextPage:{nextPageToken:"xxxxxxxx",nextPageContext:{}}}
```
"items" is the array from youtube, "nextPage" needs to pass when going to the next page. If playlist arg is true, will return ```type:'playlist'``` but the ```videos:[]``` property will not return the whole videos in the list, need to call ```GetPlaylistData``` to get real playlist's videos.
## NextPage (Promise)
```node
youtubesearchapi.NextPage(<nextPage from GetListByKeywords result>,[playlist boolean])
```
NextPage Result
```node
{items:[],nextPage:{nextPageToken:"xxxxxxxx",nextPageContext:{}}}
```

## Playlist with ID (Promise)
```node
youtubesearchapi.GetPlaylistData(<Playlist Id>)
```
Playlist Result
```node
{items:[],metadata:{}}
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## TODO
1. Live stream result

## License
[MIT](https://choosealicense.com/licenses/mit/)