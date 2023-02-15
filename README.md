## Install go-grpc:
```
go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
```
## Export the path to the go-grpc binaries:
```
open ~/.zshrc
export PATH="$PATH:$(go env GOPATH)/bin"
source ~/.zshrc
```

## Generate the gRPC code:
```
cd chapter-00/helloworld
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative pb/helloworld.proto
```

## Run the server:
```
go run server/main.go
```

## Run the client:
```
go run client/main.go Codetoanbug
```

## Output:
```
2021/10/03 22:00:00 Greeting: Hello Codetoanbug
```
Hope this helps.

## License
The code in this repository is licensed under the [MIT license](https://opensource.org/licenses/MIT)
See LICENSE for details.