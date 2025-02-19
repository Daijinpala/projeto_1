# Parte teórica

1) Cite 3 exemplos de
distribuição linux.
- **Ubuntu**:<br><br>O Ubuntu é um sistema operacional moderno e seguro, amplamente utilizado por milhões de pessoas e preferido por desenvolvedores profissionais. Ele oferece os aplicativos, bibliotecas e ferramentas mais recentes, sendo uma plataforma essencial para IDEs, desenvolvimento de jogos e IA/ML. Com aplicativos essenciais como Firefox, Chrome, Discord, Steam e OBS Studio, o Ubuntu atende às necessidades diárias de navegação, mensagens, jogos e criação de conteúdo. Priorizando privacidade e segurança, ele inclui atualizações regulares e recursos de proteção integrados. Além disso, o Ubuntu Pro oferece integração com ferramentas empresariais, conformidade e patches de segurança estendidos. Totalmente de código aberto, o Ubuntu é gratuito e sustentado por uma comunidade global de desenvolvedores voluntários. <br><br>
- **Debian**: <br><br>O Debian é um sistema operacional livre e de código aberto, também baseado no Linux, conhecido por sua estabilidade, confiabilidade e compromisso com os princípios do software livre. Ele é desenvolvido por uma comunidade global de voluntários e é a base para muitas outras distribuições Linux, incluindo o Ubuntu. <br><br>
- **Arch linux**: <br><br> O Arch Linux é uma distribuição Linux leve, flexível e altamente personalizável, conhecida por sua filosofia "Keep It Simple, Stupid" (KISS) e por ser uma distribuição "rolling release". Isso significa que ele é atualizado continuamente, sem a necessidade de grandes atualizações de versão, garantindo que os usuários sempre tenham acesso aos softwares mais recentes. <br>

2) O que é IP FIXO e sua função.<br>

O IP fixo é um endereço único e permanente(enquanto for pago claro…), a função dele em suma é:

- Ser vinculado permanente a um dispositivo
- Facilitar a localização do usuário/máquina na rede.

3) O que faz o comando ls -la?<br>

Listagem de arquivos detalhado, mostrando arquivos ocultos no diretório.​

- ls -a: lista os arquivos e diretórios no diretório atual, incluindo os arquivos ocultos.
- ls -l: lista os arquivos e diretórios no diretório atual em um formato detalhado.
- ls -la: junção das duas anteriores.

> [!TIP]
> 	Exemplo:<br>-rw-r--r-- 1 user user 1234 Feb 17 11:20 .bashrc<br>-rw-r--r-- 1 user user 5678 Feb 17 11:25 arquivo

4) o que acontece se eu executar o
comando "shutdown -r -f -t 0" sem ser
root
e sem sudo?<br>

**shutdown:** Este é o comando principal que é usado para desligar ou reiniciar o sistema.

**-r:** Esta opção indica que o sistema deve ser reiniciado (restart).<br>
**-f:** Esta opção força o fechamento de aplicativos em execução sem aviso prévio. Isso significa que qualquer programa aberto será fechado imediatamente, o que pode resultar na perda de dados não salvos.<br>
**-t 0:** Esta opção define o tempo de espera antes de executar a ação, em segundos. O valor 0 significa que a ação será executada imediatamente, sem atraso.<br>

**Mensagem de erro ou acesso negado,  pois precisa estar no root e no sudo pois o -f encera todos os aplicativos que estão em execução o que necessitaria que o usuario tenha as permissões de super usuario.**



>### Documentação oficial:<br> [Ubuntu](https://help.ubuntu.com/stable/ubuntu-help/?_ga=2.163188468.972084809.1739989151-389520051.1739989151&_gl=1*1r5uf6h*_gcl_au*OTI2MDQzNjI1LjE3Mzk5ODkxNTI.)<br>[Debian](https://www.debian.org/doc/index.pt.html)<br>[Arch linux](https://wiki.archlinux.org/title/Main_page)