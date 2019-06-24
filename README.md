# oscp-ref
## 日本語
日本語では「なぜ」「何を目的にして実施するのか」をコメントとして書いています。

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
1. 権限昇格のための調査
	- Windows
		- 誰でもアクセス可能かつSystem権限で動作しているサービス
		- 権限が異様に高いプログラム
		- 脆弱性
	- Linux
		- 脆弱性
	- Unix（そのうち）
1. 権限昇格
	- Windows
	- Linux
	- Unix（そのうち）
1. システム、ネットワークに関する情報収集
	- Windows
	- Linux
	- Unix（そのうち）
	- Cloud(AWS, GCP等々からの情報収集)
1. ラテラルやポートフォワーディング（横に移る）
1. metasploit（これ一つで上のことをやる）
	- 情報収集
	- リモートエクスプロイト
	- 権限調査
	- 権限昇格
	- 対象システム・ネットワークの詳細情報収集
1. その他のmetasploitみたいに使える便利なツール群
	- PowerShell Empire
	- Cobalt Strike
	- PoshC2
	- dnscat2
	- p0wnedShell
	- Pupy Shell
	- Merlin
	- Nishang

## English
### Methodology and Strategy for OSCP lab and exam
1. Enumeration
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
1. Exploit to inside(Remote Exploit)
	- Windows
	- Linux
	- Unix(In the meantime)
1. Enumeration for Elevation
	- Windows
	- Linux
	- Unix(In the meantime)
1. Elevation of Privileges
	- Windows
	- Linux
	- Unix(for Real world)
1. Gathering the critical information
	- Windows
	- Linux
	- Unix(for Real world)
	- Cloud(AWS,GCP,etc...)
1. Lateral, Port Forwarding to next machine...
1. Metasploit(Just one machine)
	- enum
	- exploit to inside
	- enum for elevation
	- elevation of privileges
	- gathering the critical information
1. Other powerful tools like Metasploit
	- Powershell Empire
	- Cobalt Strike
	- PoshC2
	- dnscat2
	- p0wnedShell
	- Pupy Shell
	- Merlin
	- Nishang

