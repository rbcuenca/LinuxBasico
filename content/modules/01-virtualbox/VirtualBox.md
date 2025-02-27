# Instalação do VirtualBox

## Iniciando a Instalação

- Vamos dividir este tópico em dois. Clique no sistema operacional que você usa para acessar o conjunto de instruções correto:


<p style="text-align:center;">
  <a href="#instalação-no-windows">WINDOWS</a>
</p>
<p style="text-align:center;">
  <a href="#instalação-no-macos">MACOS</a>
</p>

<div style="border: 1px solidrgb(19, 20, 20); border-left-width: 5px; padding: 10px; background-color:rgb(175, 178, 181); border-radius: 5px;">
💡 <strong>Dica:</strong> Pergunte em TODAS dúvidas!!!
</div>

---

- Se você já instalou o VirtualBox, pode seguir para a [Instalação do Linux](#preparando-a-instalação-do-linux-ubuntu-2204)
---

### Instalação no Windows
- Neste exemplo estamos usando o Windos 11 24h2 e o instalador do link mostrado na primeira página.
- Dê um duplo clique no arquivo que você baixou e siga a instalação.

<center>
![](Windows/inst00.png)
![](Windows/inst01.png)
![](Windows/inst02.png)
![](Windows/inst03.png)
![](Windows/inst04.png)
![](Windows/inst05.png)
![](Windows/inst06.png)
![](Windows/inst07.png)
![](Windows/inst08.png)

</center>

<p style="text-align:right;">
  <a href="#preparando-a-instalação-do-linux-ubuntu-2204">Preparando a Instalação do Linux</a>
</p>

### Instalação no MacOS
- Neste exemplo estamos usando MacOS Ventura e o instalador do link mostrado na primeira página.
- Após o download, execute o arquivo de extenção dmg. Ele montará um disco virtual com a instalação do VirtualBox.

<center>
![](MacOS/instMac00.png)
![](MacOS/instMac01.png)
![](MacOS/instMac02.png)
![](MacOS/instMac03.png)
![](MacOS/instMac04.png)

<p style="text-align:center;">Nos últimos momentos da instalação, aparecerá este aviso no canto superior direito, basta fechar.</p>
![](MacOS/instMac05.png)
<br>

</center>

### Preparando a Instalação do Linux Ubuntu 22.04

- A partir deste ponto, tanto a instalação no Windows como no Linux os passos serão os mesmos. Estaremos usando as imagens da instalação no Windows por ser o SO mais utilizado, se você está usando MacOS e tiver dúvidas **PERGUNTE** a sua dúvida é muito importante para todos!!

---

<p style="text-align:center;">Com o VirtualBox aberto, você deve clicar em NOVO:</p>

<center>![](vm/inst09.png)</center>

<p style="text-align:center;">Na tela que abrir, você dará o nome da Máquina Virtual e o caminho. Em seguida os campos de:</p>
<p style="text-align:center;">Imagem ISO :<strong>Selecione o arquivo de Imagem ISO que você baixou. Encontrado nos links na pagina inicial desta atividade.</strong></p>
<p style="text-align:center;">Tipo :<strong>Linux;</strong></p>
<p style="text-align:center;">Subtipo :<strong>Ubuntu;</strong></p>
<p style="text-align:center;">Versão :<strong>Ubuntu (64-bit);</strong></p>

<center>![](vm/inst10.png)</center>

<p style="text-align:center;">Clique em Próximo</p><br><br>


<p style="text-align:center;">Agora escolha quanto do seu hardware ficará "dedicado" à máquina virtual.</p>
<p style="text-align:center;">Usualmente ele recomenda o mínimo necessário para o sistema funcionar, é extremamente recomendável que dedique um pouco mais do hardware. Em situações do dia a dia é interessante, oa menos, metade dos seus núcleos e metade de sua memória RAM. Mas <strong>cuidado</strong> para não entrar na área em <strong>vermelho</strong>, se deixar pouco recurso para o sistema operacional da máuqina, você travará o seu computador assim que iniciar a máquina virtual.</p>

<center>![](vm/inst11.png)</center>

<p style="text-align:center;">Clique em Próximo</p><br><br>
<center>![](vm/inst12.png)</center>

<p style="text-align:center;">Chegou o momento de dizer o tamnho do seu disco virtual.</p>
<p style="text-align:center;">Não recomendo deixar menos de 40G. Não há necessidade para <strong>pânico</strong> pois a alocação deste disco é dinâmica, você não ficará com todo o espaço "preso" neste aruivo. Para isso é só <strong> não clicar</strong> no checkbox.</p>

<p style="text-align:center;">Clique em Próximo</p><br><br>
<center>![](vm/inst13.png)</center>

<p style="text-align:center;">Sumário</p>
<p style="text-align:center;">Nesta tela você poderá revisar tudo o que escolheu e finalizar a configuração da sua máquina virtual, clicando em Finalizar.</p><br>
<p style="text-align:center;">Os próximos passos serão os mesmos para as máquinas virtuais e a instalação diretamente no computador.</p>

Próximo passo: [Instalação do Ubuntu](modules/03-ubuntu/Ubuntu.md)