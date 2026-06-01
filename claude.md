


### 打包步骤

```shell
# web
cd app
pnpm i
pnpm build
cd ..

dotnet publish dy.net.csproj -c Release -o publish
cd publish
docker build -f .\Dockerfile -t registry.cn-hangzhou.aliyuncs.com/sijinhui/dysync .
docker push registry.cn-hangzhou.aliyuncs.com/sijinhui/dysync  
```