# oscp-ref
いろんなところにあるOSCPに関する資料、（実践的に）使えるコマンド等々ひたすら集めたrepository.  
診断とかペネトレをやってる or これからOSCPを取ろうと考えている人に役立つと良いなぁ.  
一応実案件でも役に立った場面のあったコマンドも載せている、かもしれない.

## 日本語
日本語では「なぜ」「何を目的にして実施するのか」を極力コメントとして記載.  

1. 情報収集（サービス・アカウント等）
	- 直接アクセス
		- ポートスキャン
			- クイック＆詳細チェック - 何が空いているのかを把握、確認ののち空いているポートに対してのみ詳細にチェック
		- 各ポートで動いているサービスの調査
			- サービスは？バージョンは？エクスプロイトコードは公開されていないか？
			- 設定ミスはされていないか？FTPであればanonymous login、HTTPであれば公開ディレクトリの不備など
			- ログインが必要なサービスでjoeアカウントが使用されていないか？
			- など。他に思いついたら追記する
		- 存在しそうなユーザ、パスワードの組み合わせを作成
			- HTMLパースなど
		- Cloud(AWS, GCP等々からの情報収集)
	- 公開情報からの収集（実際のRedTeamなどでやる）
		- そのうち
1. マシン内部への侵入（リモートエクスプロイト）
	- Windows
	- Linux
	- Unix（そのうち）
	- その他のフレームワーク(CMSとか)
1. システム、ネットワークに関する情報収集(PostExploitation)  
  ここでの情報を基に権限昇格、横展開を行っていく
	- Windows
	- Linux
	- Unix（そのうち）
	- Cloud(AWS, GCP等々からの情報収集)
1. 権限昇格
	- Windows
	- Linux
	- Unix（そのうち）
1. ラテラル: 横展開
	- Windows
	- Linux
	- Unix
1. ピボッティング: DMZなどへの横展開
	- Windows
	- Linux
	- Unix
1. Metasploit（これ一つで上のことをやる）
	- Remote Enumeration
	- RemoteExploit
	- PostExploitation
	- Persistence
	- Lateral
	- Pivoting
1. その他のMetasploitみたいに使える便利なツール群
	- Cobalt Strike
	- PowerShell Empire
	- PoshC2
	- dnscat2
	- p0wnedShell
	- Pupy Shell
	- Merlin
	- Nishang

## English
### Methodology and Strategy for OSCP lab and exam
1. Remote Enumeration
	- Active(Any)
		1. Scan port
			- Quick and Deep
		1. Search each port
			- vulnerable version?
			- miss configuration?
			- joe account?
			- etc...
		1. Create the list of user and password
			- Parse HTML
		1. Cloud
	- Passive(for Real world)
		- In the meantime
1. Remote Exploitation
	- Windows
	- Linux
	- Unix(In the meantime)
1. Post Exploitation
	- Windows
	- Linux
	- Unix(In the meantime)
	- Cloud(AWS,GCP,etc...)
1. Privilege Escalation
	- Windows
	- Linux
	- Unix(In the meantime)
1. Lateral Movement
	- Windows
	- Linux
	- Unix
1. Pivoting
	- Windows
	- Linux
	- Unix
1. Metasploit(Just one machine)
	- Remote Enumeration
	- Remote Exploitation
	- Post Exploitation
	- Privilege Escalation
	- Persistence
	- Lateral Movement
	- Pivoting
1. Other powerful tools
	- Cobalt Strike
	- Powershell Empire
	- PoshC2
	- dnscat2
	- p0wnedShell
	- Pupy Shell
	- Merlin
	- Nishang

