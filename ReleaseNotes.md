 ##更新履歴/説明
 
###20200903.39
（https://egg.5ch.net/test/read.cgi/software/1595715643/57）
 
・セルフ追っかけ再生  
　例：http://127.0.0.1:12345/m3u8/2/1200/index.m3u8  
　　現在のシーケンス番号から1200セグメント（リアルタイムの場合30分）戻ったところを再生  
  
・追加オプション  
　-nico-conv-seqno-start ＜num＞  
　　MP4への変換を指定したセグメント番号から開始する  
　-nico-conv-seqno-end ＜num＞  
　　MP4への変換を指定したセグメント番号で終了する  
　-nico-conv-force-concat  
　　MP4への変換で画質変更または抜けがあっても分割しないように設定  
　-nico-conv-force-concat=on  
　　(+) 上記を有効に設定  
　-nico-conv-force-concat=off  
　　(+) 上記を無効に設定(デフォルト)  
  
　-d2h  
　　[実験的] 録画済みのdb(.sqlite3)を視聴するためのHLSサーバを立てる(-db-to-hls)  
　　　開始シーケンス番号は（変換ではないが） -nico-conv-seqno-start で指定  
　　　　使用例：$ livedl lvXXXXXXXXX.sqlite3 -d2h -nico-hls-port 12345 -nico-conv-seqno-start 2780   
