NO	第1階層	第2階層	第3階層	第4階層	第5階層	出力する内容	サンプル	備考	固定値？	電話帳	
6	BreadcrumbList										
7		@type				BreadcrumbList	BreadcrumbList		YES		
8		itemListElement						パンくずの数だけ、itemListElement を繰り返す			
9			@type			ListItem	ListItem		YES		
10			position				1	パンくず第1階層⇒1 , 第2階層⇒2 , 第3階層⇒3			
11			item								
12				@type		Thing	Thing		YES		
13				@id		http://haisha-yoyaku.jp/	http://haisha-yoyaku.jp/	パンくずURL			
14				name		歯医者・歯科トップページ	歯医者・歯科トップページ	パンくずリスト名称			
区切り											
区切り											
15	Dentist										
16		@type				Dentist	Dentist		YES		
17		aggregateRating						レーティング口コミが3件未満で総合レーティングが表示されない場合は、aggregateRating配下を削除　18/05/22 井上	YES		●
18			@type			AggregateRating	AggregateRating		YES		
19			bestRating			レーティングのMAX値	5	総合MAX値5を追加　18/05/22 井上	YES		●
20			ratingValue			レーティングスコア	4				
21			reviewCount			口コミ数	200	※口コミ数			
22			worstRating			レーティングのMIN値	0	総合MIN値0を追加　18/05/22 井上	YES		●
23		review						"レビューの数だけ、reviewを繰り返す　1/27ターニャ
aggregateRatingのみで問題なくなったので削除　18/05/22 井上"	YES		●
24			@type			Review	Review		YES		●
25			author			レーティングした人のニックネーム	矢島 義章				●
26			datePublished			レーティングした日	2016-12-17				●
27			description			口コミ内容	痛くなかったからよかった				●
28			reviewRating						YES		●
29				@type		Rating	Rating		YES		●
30				bestRating		レーティングのMAX値	5		YES		●
31				ratingValue		レーティングスコア	4				●
32				worstRating		レーティングのMIN値	1		YES		●
33			@type			Review	Review	投稿者2人目の場合	YES		●
34			author			レーティングした人のニックネーム	矢島 義子				●
35			datePublished			レーティングした日	2016-12-14				●
36			description			口コミ内容	丁寧な治療で助かりました。				●
37			reviewRating						YES		●
38				@type		Rating	Rating		YES		●
39				bestRating		レーティングのMAX値	5		YES		●
40				ratingValue		レーティングスコア	5				●
41				worstRating		レーティングのMIN値	1		YES		●
42			@type			Review	Review	投稿者3人目(口コミのみ投稿者)の場合　※表示されている口コミ数(上限3)まで繰り返す。	YES		●
43			author			レーティングした人のニックネーム	矢島 義男				●
44			datePublished			レーティングした日	2016-12-11				●
45			description			口コミ内容	また行きたい歯医者でした。				●
