## Data enumeration with scapy

O Scapy é uma ferramenta de manipulação de pacotes de rede que permite criar, enviar, capturar e analisar pacotes de rede. A ferramenta é útil para testes de penetração, análise de tráfego de rede, análise de protocolos de rede, entre outros.

Executando:

```bash
scapy
```

Comando:

```bash
ans, unans = sr(IP(dst="<domain>/30", ttl=(1,6))/TCP())
```

Após parar a execução do comando, você pode visualizar alguns dados coletados dessa forma:

```bash
ans.make_table( lambda s, r: (s.dst, s.ttl, r.src))
```

Outro exemplo de coleta em mais de um domínio:

```bash
res, unans=traceroute(["www.google.com", "www.kali.org"],dport=[80, 443],maxttl=20, retry=2)
```





Esse comando envia pacotes TCP para o endereço IP especificado e captura as respostas. O comando `sr` envia pacotes e captura respostas, enquanto o comando `sr1` envia um pacote e captura a primeira resposta. O comando `ans, unans` captura as respostas e as não respondidas.