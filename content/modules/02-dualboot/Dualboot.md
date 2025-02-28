[Retornar](index.md)
# Fazer o Dual Boot


Ao escolher esta opção é __fortemente recomendável__ que tenha feito uma cópia de segurança de tudo o que você não pode perder. Há uma possiblidade grande de perder dados.

<div style="border: 1px solidrgb(19, 20, 20); border-left-width: 5px; padding: 10px; background-color:rgb(175, 178, 181); border-radius: 5px;">
💡 <strong>Dica:</strong> Você tem o OneDrive pela sua conta Microsoft do INSPER (e-mail do aluno).<br><br>Se você usa Windows, a intergração com o OneDrive fuciona muito bem e mantém, automaticamente, uma cópia on-line dos seus arquivos e de suas configurações básicas (dependendo de como configurou).<br><br>Se você usa MacOS (A partir do Yosemite - 10.10 - 2014) a integração com o iCloud Drive funciona muito bem e mantém, automaticamente, uma cópia on-line
</div>
<br><br>
Antes de iniciar a instalação do Linux em dual boot, é necessário verificar se a criptografia de disco está ativada. Caso esteja, será preciso desativá-la para posteriormente desligar o Secure Boot na BIOS. Siga os passos abaixo para verificar e desativar a criptografia de disco no Windows:

	1.      Clique no botão Iniciar,
    2.	Acesse o Painel de Controle.
	3.	Vá até Sistema e Segurança.
	4.	Clique em Criptografia de Unidade de Disco BitLocker.
Na tela que aparecer, você poderá verificar se o BitLocker está ativado. Caso esteja, siga as instruções para desativá-lo:
<center>![](bitlocker/bitlocker.png)</center>
<br>

	•	Clique em Desativar BitLocker ao lado da unidade criptografada.
	•	Aguarde a descriptografia completa do disco antes de prosseguir.
<br>
Agora precisamos criar o pendrive de instalação do Ubuntu 22.04. Para este passo, você deve instalar o <strong>rufus</strong>. <br><br>

Você já baixou este arquivo no mesmo momento em que baixou o arquivo <strong>iso</strong> no início da atividade: [Arquivos](../../index.md#arquivos)

Após executar o arquivo, você verá um pedido de autorização de execução do windows:
<center>![](rufus/inst_rufus01.png)</center>
<br>
Clique em <strong>SIM</strong> e abrirá uma janela perguntando se quer buscar por atualizações:
<br><br>
<center>![](rufus/inst_rufus02.png)</center>
<br>
Clique em <strong>SIM</strong> novamente. Após verificar se existem atualizações, ele abrirá a tela principal do rufus:
<center>![](rufus/rufus.png)</center>
<br>
Nesta tela, você deve escolher as seguintes opções:<br>
- Device: O Pendrive em que gravará a instalação do Ubuntu;<br>
- Botão <strong>SELECT</strong>: Selecionar o arquivo .iso do Ubuntu que você baixou;<br>
- Partition Scheme: <strong>GPT</strong>;<br>
- Target System: <strong>UEFI</strong>.<br>
<br>
As demais opções, mantenha como padrão.
<br><br>

Agora clique em <strong>START (INICIAR)</strong>.

Após terminar, clique em <strong>close</strong> e desligue o computador <strong>com o pendrive conectado</strong>. Você deve reiniciar e entrar na BIOS para os próximos ajustes.
<br>


<div style="border: 1px solidrgb(19, 20, 20); border-left-width: 5px; padding: 10px; background-color:rgb(175, 178, 181); border-radius: 5px;">
💡 <strong>Dica:</strong> A próxima etapa (BIOS) faremos juntos para que não tenhamos problemas. Cada fabricante tem uma bios própria e veremos caso a caso.
</div>
<br>
Após desativar a criptografia, reinicie o computador e acesse as configurações da BIOS/UEFI para desabilitar o Secure Boot. O procedimento pode variar conforme o fabricante, mas geralmente envolve:

	1.	Reiniciar o computador enquanto mantém pressionada a tecla específica para acessar a BIOS (geralmente F2, DEL ou ESC).
	2.	Navegar até a aba de segurança ou inicialização (Security ou Boot).
	3.	Localizar a opção Secure Boot e defini-la como Disabled.
	4.	Salvar as alterações e sair da BIOS.
Com o Secure Boot desativado e o disco descriptografado, você estará pronto para iniciar a instalação do Linux em dual boot.
<br><br>
<div style="border: 1px solidrgb(19, 20, 20); border-left-width: 5px; padding: 10px; background-color:rgb(175, 178, 181); border-radius: 5px;">
💡 <strong>Dica:</strong> - Lembre-se de que as telas e nomes podem variar de acordo com a atualização e versão do seu windows.
</div>

Agora vamos iniciar o computador pelo pendrive. Para esta etapa, se for um notebook da <strong>DELL</strong> pressione repetidamente a tecla <strong>F12</strong> após ligar o computador, assim acessará o menu de boot do computador. Se for um computador de outra marca, é necessário saber como entrar no menu, mas é provavel que seja com <strong>F8 ou F10</strong> e se for um computador <strong>Thinkpad</strong> você deve precionar <strong>ENTER</strong> durante a inicialização quando ele mandar.

Após aparecer o menu, escolha o pendrive e tecle enter.

Próximo passo: [Instalação do Ubuntu](../03-ubuntu/Ubuntu.md)

