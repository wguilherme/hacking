### Introdução ao Nessus

O Nessus é uma ferramenta de varredura de vulnerabilidades que é usada para identificar, quantificar e priorizar as vulnerabilidades de segurança em sistemas operacionais, aplicações e hardware. O Nessus foi desenvolvido pela Tenable Network Security e é uma das ferramentas de segurança mais populares.

- Install .deb package from [Tenable](https://www.tenable.com/downloads/nessus)
- Start the service `/bin/systemctl start nessusd.service`
- Access the web interface at `https://localhost:8834`


Enable system service to start on boot:
```bash
systemctl enable nessusd.service
systemctl status nessusd.service
```

