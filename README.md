golang版的淘宝客(tbk)SDK



## API示例

###  [taobao.tbk.tpwd.create( 淘宝客-公用-淘口令生成 )](https://open.taobao.com/api.htm?docId=31127&docType=2)

```go
func TestTaobaoTbkTpwdCreate(t *testing.T) {
	var topClient *top.Client = top.NewClient(AppKey, AppSecret)

	var api = top.NewTaobaoTbkTpwdCreate()
	api.SetParam("text", "长度大于5个字符")
	api.SetParam("url", "https://uland.taobao.com/")

	d, err := topClient.Run(api)

	fmt.Println(">>>>>>", string(d), err)
}
```