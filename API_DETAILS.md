# Quick API Guide
More detailed Flickr API documentation is available [here](https://www.flickr.com/services/api/), however the following information should get you started for the exercise.

### Outline
- [Required info](#required-api-key-&-id)
- [Retrieve public photos](#retrieve-public-photos)
- [Constructing image url](#constructing-image-url)
- [Questions](#questions)

## Required Information
- Flickr API Key: `a5e95177da353f58113fd60296e1d250` (you can also use your own key)
- Nasa's user id: `24662369@N07`

## Retrieve public photos
Endpoint: `https://api.flickr.com/services/rest/?method=flickr.people.getPublicPhotos`

Requirements:
- `&api_key=APIKEY`
- `&user_id=USER_ID`

Optional Parameters
- `&format=json`
- `&nojsoncallback=1`

Full URL:  `https://api.flickr.com/services/rest/?method=flickr.people.getPublicPhotos&api_key=API_KEY&user_id=USER_ID&format=json&nojsoncallback=1`

Result:
```json
{ "photos": { "page": 1, "pages": 10, "perpage": 100, "total": "946",
    "photo": [
      { "id": "11738172576", "owner": "12218676@N04", "secret": "37d0aeb353", "server": "3803", "farm": 4, "title": "_IGP1164", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "11441822184", "owner": "12218676@N04", "secret": "e0d1cae3a7", "server": "3681", "farm": 4, "title": "picklr", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "9441833860", "owner": "12218676@N04", "secret": "1dc4d7677d", "server": "2893", "farm": 3, "title": "_PPP3369", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "9007662806", "owner": "12218676@N04", "secret": "9dcd741751", "server": "5341", "farm": 6, "title": "", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "8808596948", "owner": "12218676@N04", "secret": "13c838ba9f", "server": "5470", "farm": 6, "title": "_JSP0977", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "8678037785", "owner": "12218676@N04", "secret": "e6367640aa", "server": "8543", "farm": 9, "title": "bill-harveydent", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "8656077491", "owner": "12218676@N04", "secret": "710cd8fb32", "server": "8119", "farm": 9, "title": "bedroom", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "8656078775", "owner": "12218676@N04", "secret": "7bda42b650", "server": "8114", "farm": 9, "title": "beach-bicycle", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "8655982351", "owner": "12218676@N04", "secret": "727a4fc37a", "server": "8118", "farm": 9, "title": "jason-train-montreal", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "8655961073", "owner": "12218676@N04", "secret": "d3e7f84b9e", "server": "8109", "farm": 9, "title": "luce-rouge", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "8651896286", "owner": "12218676@N04", "secret": "4e0f724604", "server": "8382", "farm": 9, "title": "GoldstoneNoodleRestaurant", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "7058516875", "owner": "12218676@N04", "secret": "6366784d35", "server": "5232", "farm": 6, "title": "avec amour", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6873642443", "owner": "12218676@N04", "secret": "011b21d6cc", "server": "7065", "farm": 8, "title": "_IGP8001", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6854637221", "owner": "12218676@N04", "secret": "446a443e9c", "server": "7022", "farm": 8, "title": "_IGP7990", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6810113167", "owner": "12218676@N04", "secret": "c50635e979", "server": "7152", "farm": 8, "title": "_IGP8029", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6687720137", "owner": "12218676@N04", "secret": "c012c53df8", "server": "7172", "farm": 8, "title": "68540024", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6687692431", "owner": "12218676@N04", "secret": "1e87137612", "server": "7164", "farm": 8, "title": "68540018", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6601218563", "owner": "12218676@N04", "secret": "03a59515fe", "server": "7142", "farm": 8, "title": "68150004", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6601198767", "owner": "12218676@N04", "secret": "7e50ba44f3", "server": "7026", "farm": 8, "title": "68550011", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6562285537", "owner": "12218676@N04", "secret": "03b815840f", "server": "7149", "farm": 8, "title": "67200002-2", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6562252731", "owner": "12218676@N04", "secret": "f06b99755e", "server": "7172", "farm": 8, "title": "67200012-2", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6518977249", "owner": "12218676@N04", "secret": "26fb528af9", "server": "7035", "farm": 8, "title": "_IGP7738", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6506179111", "owner": "12218676@N04", "secret": "2930a78d5b", "server": "7003", "farm": 8, "title": "_IGP6080", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6506169835", "owner": "12218676@N04", "secret": "c1c62f36d7", "server": "7021", "farm": 8, "title": "_IGP6078", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6506079891", "owner": "12218676@N04", "secret": "f4ba4ac52b", "server": "7172", "farm": 8, "title": "_IGP5931", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6480613639", "owner": "12218676@N04", "secret": "af7f2697b6", "server": "7168", "farm": 8, "title": "_IGP7610", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6480596009", "owner": "12218676@N04", "secret": "30fded0293", "server": "7026", "farm": 8, "title": "_IGP7611", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6474073993", "owner": "12218676@N04", "secret": "e27865a62d", "server": "7020", "farm": 8, "title": "_IGP7528", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6444636497", "owner": "12218676@N04", "secret": "f35262aef1", "server": "7154", "farm": 8, "title": "_IGP7590", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6429080301", "owner": "12218676@N04", "secret": "84064f0ae2", "server": "7157", "farm": 8, "title": "_IGP7538", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6422058249", "owner": "12218676@N04", "secret": "4738c3fb59", "server": "7154", "farm": 8, "title": "_IGP7474", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6409425749", "owner": "12218676@N04", "secret": "be2c8e9170", "server": "6048", "farm": 7, "title": "_IGP7518", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6398036607", "owner": "12218676@N04", "secret": "824cfbb106", "server": "6213", "farm": 7, "title": "_IGP7169", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6398035859", "owner": "12218676@N04", "secret": "1539e0f212", "server": "6036", "farm": 7, "title": "_IGP7168", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6398023153", "owner": "12218676@N04", "secret": "fb80af1542", "server": "6094", "farm": 7, "title": "_IGP7170", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6338919752", "owner": "12218676@N04", "secret": "4903e0b9d7", "server": "6060", "farm": 7, "title": "60030002", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6306964928", "owner": "12218676@N04", "secret": "d695d62fec", "server": "6218", "farm": 7, "title": "_IGP7257", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6281586616", "owner": "12218676@N04", "secret": "7e4cf8017a", "server": "6102", "farm": 7, "title": "_IGP6707", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6265605610", "owner": "12218676@N04", "secret": "3db0e444e7", "server": "6101", "farm": 7, "title": "_IGP7230", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6248337242", "owner": "12218676@N04", "secret": "99e4ca4021", "server": "6234", "farm": 7, "title": "_IGP7082", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6248330434", "owner": "12218676@N04", "secret": "ac1c3da6f6", "server": "6053", "farm": 7, "title": "_IGP7147", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6247803087", "owner": "12218676@N04", "secret": "aa79b3a590", "server": "6160", "farm": 7, "title": "_IGP7063", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6212577763", "owner": "12218676@N04", "secret": "442665b373", "server": "6226", "farm": 7, "title": "_IGP6970", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6213088024", "owner": "12218676@N04", "secret": "857d2e972b", "server": "6036", "farm": 7, "title": "_IGP6968", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6212567657", "owner": "12218676@N04", "secret": "c794e3368d", "server": "6240", "farm": 7, "title": "_IGP6959", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6182736563", "owner": "12218676@N04", "secret": "f4e97e8f21", "server": "6174", "farm": 7, "title": "_IGP6759.jpg", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6183256552", "owner": "12218676@N04", "secret": "2559f5d99c", "server": "6152", "farm": 7, "title": "_IGP6750.jpg", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6101473728", "owner": "12218676@N04", "secret": "3885c041cf", "server": "6064", "farm": 7, "title": "_IGP6773", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6101473450", "owner": "12218676@N04", "secret": "0728bbc88e", "server": "6081", "farm": 7, "title": "_IGP6808", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6101473164", "owner": "12218676@N04", "secret": "a1635cac5c", "server": "6197", "farm": 7, "title": "_IGP6776", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6100926249", "owner": "12218676@N04", "secret": "a5a70b2dcd", "server": "6070", "farm": 7, "title": "_IGP6690", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "6101472306", "owner": "12218676@N04", "secret": "bca6af7965", "server": "6067", "farm": 7, "title": "_IGP6695", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5792156572", "owner": "12218676@N04", "secret": "ac08a2ee9a", "server": "2124", "farm": 3, "title": "for your eyes", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5752793527", "owner": "12218676@N04", "secret": "6e9920b54e", "server": "5146", "farm": 6, "title": "_IGP6411", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5752790427", "owner": "12218676@N04", "secret": "141a1548c0", "server": "3106", "farm": 4, "title": "_IGP6412", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5708392531", "owner": "12218676@N04", "secret": "ac515df0da", "server": "2537", "farm": 3, "title": "30940002", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5708899194", "owner": "12218676@N04", "secret": "4b737916b6", "server": "3346", "farm": 4, "title": "30940006-2", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5698224522", "owner": "12218676@N04", "secret": "50ff532dde", "server": "5270", "farm": 6, "title": "_IGP5811", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5691619308", "owner": "12218676@N04", "secret": "c376cb3c66", "server": "5188", "farm": 6, "title": "_IGP5813", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5691611010", "owner": "12218676@N04", "secret": "09322a716b", "server": "5306", "farm": 6, "title": "_IGP5824", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5691030937", "owner": "12218676@N04", "secret": "c4a90974e3", "server": "5301", "farm": 6, "title": "_IGP5823", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5654835687", "owner": "12218676@N04", "secret": "20312c26b8", "server": "5110", "farm": 6, "title": "_IGP5938", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5548900812", "owner": "12218676@N04", "secret": "f264e58b13", "server": "5064", "farm": 6, "title": "_IGP6008", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5412446692", "owner": "12218676@N04", "secret": "28f8ae1a08", "server": "5299", "farm": 6, "title": "_IGP5864", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5402740191", "owner": "12218676@N04", "secret": "06dc12c6ec", "server": "5018", "farm": 6, "title": "_IGP5830", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5403338572", "owner": "12218676@N04", "secret": "c5557fd5d8", "server": "5256", "farm": 6, "title": "_IGP5838", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5403338072", "owner": "12218676@N04", "secret": "0c7bfd6633", "server": "5018", "farm": 6, "title": "_IGP5837", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5402738371", "owner": "12218676@N04", "secret": "8ca4729837", "server": "5299", "farm": 6, "title": "_IGP5852", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5365870718", "owner": "12218676@N04", "secret": "cc91213a30", "server": "5050", "farm": 6, "title": "15940011", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5358244260", "owner": "12218676@N04", "secret": "f7cd3a369e", "server": "5082", "farm": 6, "title": "15940015-2", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5302662930", "owner": "12218676@N04", "secret": "db5dffef24", "server": "5005", "farm": 6, "title": "_IGP5636", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5300462742", "owner": "12218676@N04", "secret": "17375a9951", "server": "5163", "farm": 6, "title": "13010022", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5295520217", "owner": "12218676@N04", "secret": "66510f00b0", "server": "5244", "farm": 6, "title": "13010009", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5295407021", "owner": "12218676@N04", "secret": "c1def123ec", "server": "5246", "farm": 6, "title": "13010010", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5295999886", "owner": "12218676@N04", "secret": "6c451963d8", "server": "5123", "farm": 6, "title": "13010011", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5227572993", "owner": "12218676@N04", "secret": "f01aeccb2e", "server": "5085", "farm": 6, "title": "_IGP5427", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5188475574", "owner": "12218676@N04", "secret": "ba73826035", "server": "4021", "farm": 5, "title": "_IGP5240", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5188475384", "owner": "12218676@N04", "secret": "b67c1763f5", "server": "4148", "farm": 5, "title": "_IGP5241", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5183678540", "owner": "12218676@N04", "secret": "df9980368b", "server": "1291", "farm": 2, "title": "fomapan100-rodinal-tiffsbday-dyrageraldrobodance", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5155629520", "owner": "12218676@N04", "secret": "8cca7c425a", "server": "4129", "farm": 5, "title": "13010015", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5155628690", "owner": "12218676@N04", "secret": "25027c4a99", "server": "4067", "farm": 5, "title": "56230014", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5155019821", "owner": "12218676@N04", "secret": "3e81ca3bf2", "server": "1129", "farm": 2, "title": "img008", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5117938644", "owner": "12218676@N04", "secret": "34ae382e4c", "server": "4087", "farm": 5, "title": "56230016", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5117938382", "owner": "12218676@N04", "secret": "98b4e47179", "server": "1099", "farm": 2, "title": "56740015", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5117937940", "owner": "12218676@N04", "secret": "401b3f783e", "server": "1068", "farm": 2, "title": "56740009", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5117937620", "owner": "12218676@N04", "secret": "beac6db531", "server": "4132", "farm": 5, "title": "56740016", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "5117936936", "owner": "12218676@N04", "secret": "2c878765cd", "server": "1070", "farm": 2, "title": "56230009", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4994314241", "owner": "12218676@N04", "secret": "b503614c48", "server": "4110", "farm": 5, "title": "_IGP4894", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4994288727", "owner": "12218676@N04", "secret": "ed6222046a", "server": "4112", "farm": 5, "title": "_IGP4890", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4848418466", "owner": "12218676@N04", "secret": "57d749a50e", "server": "4130", "farm": 5, "title": "63080013", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4848409454", "owner": "12218676@N04", "secret": "28fe7de5f3", "server": "4126", "farm": 5, "title": "63080003", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4797781934", "owner": "12218676@N04", "secret": "1c46974d1b", "server": "4140", "farm": 5, "title": "_IGP4415-2", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4747807221", "owner": "12218676@N04", "secret": "6c920b4bc1", "server": "4142", "farm": 5, "title": "56230006", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4747789895", "owner": "12218676@N04", "secret": "99675c98de", "server": "4075", "farm": 5, "title": "68000013", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4714476015", "owner": "12218676@N04", "secret": "b81aacc1db", "server": "4022", "farm": 5, "title": "68000018", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4689172064", "owner": "12218676@N04", "secret": "5ee8d9ff11", "server": "4030", "farm": 5, "title": "68000001", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4673082800", "owner": "12218676@N04", "secret": "10c69b7480", "server": "4004", "farm": 5, "title": "63080009", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4672424167", "owner": "12218676@N04", "secret": "6318aa62d6", "server": "4069", "farm": 5, "title": "Dōmo-kun and fan girl", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4673038740", "owner": "12218676@N04", "secret": "76c1fcd21a", "server": "4066", "farm": 5, "title": "firm guy", "ispublic": 1, "isfriend": 0, "isfamily": 0 },
      { "id": "4667758971", "owner": "12218676@N04", "secret": "e58757a180", "server": "4065", "farm": 5, "title": "67220024", "ispublic": 1, "isfriend": 0, "isfamily": 0 }
    ] }, "stat": "ok" }
```

Note. API_KEY & USER_ID are placeholders. The API key will be provided to you, or you can create and use your own.

[API Documentation](https://www.flickr.com/services/api/flickr.people.getPublicPhotos.htm)

## Constructing image url
The following formats can be used to construct an image url.
```javascript
//  Formats:
//  https://farm{farm-id}.staticflickr.com/{server-id}/{id}_{secret}.jpg
//	or
//  https://farm{farm-id}.staticflickr.com/{server-id}/{id}_{secret}_[mstzb].jpg
//	or
//  https://farm{farm-id}.staticflickr.com/{server-id}/{id}_{o-secret}_o.(jpg|gif|png)

var sampleImgObj = { "id": "11738172576", "owner": "12218676@N04", "secret": "37d0aeb353", "server": "3803", "farm": 4, "title": "_IGP1164", "ispublic": 1, "isfriend": 0, "isfamily": 0 };
var urlDefault = 'https://farm' + sampleImgObj.farm + '.staticflickr.com/' + sampleImgObj.server + '/' + sampleImgObj.id + '_' + sampleImgObj.secret + '.jpg';
var urlLarge = 'https://farm' + sampleImgObj.farm + '.staticflickr.com/' + sampleImgObj.server + '/' + sampleImgObj.id + '_' + sampleImgObj.secret + '_b.jpg';

//(500px)   urlDefault = https://farm4.staticflickr.com/3803/11738172576_37d0aeb353.jpg
//(1024px)  urlLarge = https://farm4.staticflickr.com/3803/11738172576_37d0aeb353_b.jpg
```

**Note.** For `urlLarge` we used `_b` to grab a larger image url for the photo. However, this does not mean all photos are available in that size. Some photos are only available in certain sizes. [**flickr.photos.getSizes**](https://www.flickr.com/services/api/flickr.photos.getSizes.html) can be used to retrieve available sizes for a photo.

For more information please take a look at the official [documentation](https://www.flickr.com/services/api/misc.urls.html).

## Questions?
As always, if there's anything that's unclear or if you just have a general question, we're just an email away! :)


[Back to top.](#quick-api-guide)
