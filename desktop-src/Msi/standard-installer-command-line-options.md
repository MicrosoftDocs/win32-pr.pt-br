---
Descrição: o programa executável que interpreta pacotes e instala produtos é Msiexec.exe. Observação: msiexec também define um nível de erro no retorno que corresponde aos códigos de erro do sistema. A tabela a seguir identifica as opções de linha de comando padrão para este programa. As opções de linha de comando não diferenciam maiúsculas de minúsculas. Windows instalador 2,0: as opções de linha de comando que são identificadas neste tópico estão disponíveis a partir do Windows Installer 3,0. as opções de Command-Line Windows Installer estão disponíveis com Windows Installer&\# 160; 3.0 e versões anteriores.
MS. AssetID: b1707c88-1cca-45ab-bb23-6002bfd5204e título: opções do instalador padrão Command-Line MS. tópico: artigo MS. Date: 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Opções de Command-Line do instalador padrão

O programa executável que interpreta pacotes e instala produtos é Msiexec.exe.

> [!Note]  
> Msiexec também define um nível de erro no retorno que corresponde aos [códigos de erro do sistema](../debug/system-error-codes.md).

 

A tabela a seguir identifica as opções de linha de comando padrão para este programa. As opções de linha de comando não diferenciam maiúsculas de minúsculas.

**Windows Installer 2,0:** as opções de linha de comando que são identificadas neste tópico estão disponíveis a partir do Windows Installer 3,0. as [opções de linha de comando](command-line-options.md) Windows Installer estão disponíveis com o Windows Installer 3,0 e versões anteriores.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Parâmetros</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/Help</strong></td>
<td> </td>
<td>Opção de ajuda e referência rápida. Exibe o uso correto do comando de instalação, incluindo uma lista de todos os comutadores e comportamentos. A descrição do uso pode ser exibida na interface do usuário. O uso incorreto de qualquer opção invoca essa opção de ajuda.<br/> Exemplo: <strong>msiexec/Help</strong><br/>
<blockquote>
[!Note]<br />
a opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Opção de exibição silenciosa. O instalador executa uma instalação sem exibir uma interface do usuário. Nenhum prompt, mensagem ou caixa de diálogo é exibido para o usuário. O usuário não pode cancelar a instalação. Use as opções de linha de comando <strong>/norestart</strong> ou <strong>/forcerestart</strong> padrão para controlar as reinicializações. Se nenhuma opção de reinicialização for especificada, o instalador reiniciará o computador sempre que necessário, sem exibir nenhum prompt ou aviso para o usuário.<br/> Exemplos: <br/> <strong>msiexec/pacote Application.msi/Quiet</strong><br/> <strong>Msiexec/Uninstall Application.msi/Quiet</strong><br/> <strong>Msiexec/Update msipatch. msp/Quiet</strong><br/> <strong>Msiexec/Uninstall msipatch. msp/pacote Application.msi/Quiet</strong><br/>
<blockquote>
[!Note]<br />
a opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/qn</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Passive</strong></td>
<td> </td>
<td>Opção de exibição passiva. O instalador exibe uma barra de progresso para o usuário que indica que uma instalação está em andamento, mas nenhum prompt ou mensagem de erro é exibido para o usuário. O usuário não pode cancelar a instalação. Use as opções de linha de comando <strong>/norestart</strong> ou <strong>/forcerestart</strong> padrão para controlar as reinicializações. Se nenhuma opção de reinicialização for especificada, o instalador reiniciará o computador sempre que necessário, sem exibir nenhum prompt ou aviso para o usuário. <br/> Exemplo: <strong>msiexec/pacote Application.msi/Passive</strong> <br/>
<blockquote>
[!Note]<br />
a opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/qb!-</strong> com <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S definida na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Nunca reinicie a opção. O instalador nunca reinicia o computador após a instalação.<br/> Exemplo: msiexec/pacote Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
o equivalente Windows Installer linha de comando foi <a href="reboot.md"><strong>reboot</strong></a>= ReallySuppress definido na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Sempre reinicie a opção. O instalador sempre reinicia o computador após cada instalação.<br/> Exemplo: msiexec/pacote Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
o equivalente Windows Installer linha de comando foi <a href="reboot.md"><strong>reboot</strong></a>= Force set na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Avisar antes da opção de reinicialização. Exibe uma mensagem informando que uma reinicialização é necessária para concluir a instalação e solicita ao usuário se o sistema deve ser reiniciado agora. Essa opção não pode ser usada junto com a opção <strong>/Quiet</strong> .<br/>
<blockquote>
[!Note]<br />
o equivalente Windows Installer linha de comando tem <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; definido na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Uninstall</strong></td>
<td><em>&lt;Package.msi|>de ProductCode </em></td>
<td>Opção desinstalar produto. Desinstala um produto.<br/>
<blockquote>
[!Note]<br />
a opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/x</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/Uninstall</strong></td>
<td><em>/pacote &lt;Package.msi | ProductCode>/Uninstall <Update1.msp | PatchGUID1> [; Update2. msp | PatchGUID2]</em></td>
<td>Desinstale a opção de atualização. Desinstala um patch de atualização.<br/>
<blockquote>
[!Note]<br />
a opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/i</strong> com <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= atualização1. msp | PatchGUID1[; Update2. msp | PatchGUID2] definido na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Opção de log. Grava informações de log em um arquivo de log no caminho existente especificado. O caminho para o local do arquivo de log já deve existir. O instalador não cria a estrutura de diretório para o arquivo de log.<br/> As informações a seguir são inseridas no log:<br/>
<ul>
<li>Mensagens de status</li>
<li>Avisos não fatais</li>
<li>Todas as mensagens de erro</li>
<li>Inicialização de ações</li>
<li>Registros específicos da ação</li>
<li>Solicitações do usuário</li>
<li>Parâmetros iniciais da interface do usuário</li>
<li>Informações de saída fatal ou de memória insuficiente</li>
<li>Mensagens de espaço em disco insuficiente</li>
<li>Propriedades do terminal</li>
</ul>
<blockquote>
[!Note]<br />
a opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/l *</strong>.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
para obter mais informações sobre todos os métodos que estão disponíveis para definir o modo de log, consulte <a href="normal-logging.md">log Normal</a> na seção <a href="windows-installer-logging.md">log de Windows Installer</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/pacote</strong></td>
<td><em>&lt;Package.msi|>de ProductCode </em></td>
<td>Instalar opção de produto. Instala ou configura um produto.<br/>
<blockquote>
[!Note]<br />
a opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/i</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Update</strong></td>
<td><em><Update1.msp>[; Update2. msp]</em></td>
<td>Opção instalar patches. Instala um ou vários patches. <br/>
<blockquote>
[!Note]<br />
o equivalente Windows Installer linha de comando tem <a href="patch.md"><strong>PATCH</strong></a> = [msipatch. msp] <; PatchGuid2> definido na linha de comando.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
