# Aqui eu vou postar coisas que eu faço depois de instalar o windows, literamente.  💻 <br />
 <br />
#Recomendo fazer com o computador fora da internet, as atualizações automáticas podem e vão atrapalhar!  <br />
 <br />
1 - Baixar o app Shutp10 e ativar as config recomendadas <br />
2 - Abrir o powershell como admin e colar o seguinte comando -> iwr -useb https://christitus.com/win | iex <br />
Vamos usar a ferramenta do christitus para automatizar muitas coisas que se for fazer de forma manual, levaria um bom tempo!  <br />
Com a ferramenta aberta, ir em tweaks - standard e run tweaks! Depoisir na seção update e clicar em Security recomended settings! Só isso! Recomendo visitar o site para mais detahes: <br />
https://christitus.com/windows-tool/ <br />
3 - Ir em painel de controle - opções de desempenho - propriedades do sistema: <br />
Peek <br />
     Mostrar miniaturas no lugar de icones <br />
     Mostrar sombras sob janelas <br />
     Usar fontes de tela com cantos arredondados <br />
     Usar sombras subjacentespara rotulos de íconas na área de trabalho <br />
 <br />
 <br />
4 - Configuraçoes via regedit para deixar o sistema mais responsivo!  <br />
 <br />
Ir em: <br />
Computador\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile <br />
 <br />
Mudar valor da chave SystemResponsiveness (1) hexadecimal <br />
 <br />
Computador\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games <br />
Mudar a chave Gpu Priority (8) <br />
Mudar a chave Priority (6) <br />
Mudar a chave Scleduling Category (High) <br />
Mudar a chave SFIO Priority (High) <br />
 <br />
Desativar o algoritimo de nagle (Obrigatóro para quem joga online!) <br />
Computador\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces <br />
Abrir o cmd e -> ipconfig | findstr /C:IPv4 <br />
De volta no regedir, clicar com o direito em localizar e colar o ip p mostrar a interface qual está vinculada no registro, exemplo --> {9fe23c16-2cba-4489-ad0d-6027fe154caf} <br />
Criar as variavels TcpAckFrequency e  TCPNoDelay <br />
 <br />
TcpAckFrequency dword 32 bits (1) <br />
TCPNoDelay dword (1) <br />
 <br />
5 - Macetes para se fazer na bios (Usando uma placa mãe da ASUS como exemplo!) <br />
 <br />
Ativar XMP na bios   <br />
Abobe 4g enable <br />
Sr iov enable  <br />
Rebar enable  <br />
global c state control disable <br />
Cppc e cpc prefered cores disable = Advanced > AMD CBS > NBIO Common Options > SMU Common Options :) <br />
