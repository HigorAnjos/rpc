all:
	rpcgen -C simp.x	
	gcc -c *.c
	gcc -o client simpclient.o simp_clnt.o simp_xdr.o -lnsl
	gcc -o server simpservice.o simp_svc.o simp_xdr.o -lrpcsvc -lnsl
	./server &

# ./client 127.0.0.1 5 5