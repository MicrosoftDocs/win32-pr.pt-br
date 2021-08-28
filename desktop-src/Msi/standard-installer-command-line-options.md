---
description: o programa executável que interpreta pacotes e instala produtos é Msiexec.exe. Observe que o Msiexec também define um nível de erro no retorno que corresponde aos Códigos de Erro do Sistema. A tabela a seguir identifica as opções de linha de comando padrão para este programa. As opções de linha de comando não são sensíveis a maiúsculas e minúsculas. Windows Instalador 2.0: as opções de linha de comando identificadas neste tópico estão disponíveis a partir do Windows Installer 3.0. As Windows do Command-Line estão disponíveis com o Windows Installer&\# 160;3.0 e versões anteriores.
ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e título: Standard Installer Command-Line Options ms.topic: article ms.date: 31/05/2018
---

# <a name="standard-installer-command-line-options"></a>Opções de Command-Line Standard Installer

O programa executável que interpreta pacotes e instala produtos é Msiexec.exe.

> [!Note]  
> O Msiexec também define um nível de erro no retorno que corresponde aos Códigos [de Erro do Sistema](../debug/system-error-codes.md).

 

A tabela a seguir identifica as opções de linha de comando padrão para este programa. As opções de linha de comando não são sensíveis a maiúsculas e minúsculas.

**Windows Instalador 2.0:** As opções de linha de comando identificadas neste tópico estão disponíveis a partir do Windows Installer 3.0. As Windows de [Linha](command-line-options.md) de Comando do Instalador do Windows estão disponíveis com o Windows Installer 3.0 e versões anteriores.



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
<td><strong>/help</strong></td>
<td> </td>
<td>Opção de ajuda e referência rápida. Exibe o uso correto do comando de instalação, incluindo uma lista de todas as opções e comportamento. A descrição do uso pode ser exibida na interface do usuário. O uso incorreto de qualquer opção invoca essa opção de ajuda.<br/> Exemplo: <strong>msiexec /help</strong><br/>
<blockquote>
[!Note]<br />
A opção Windows linha de comando do <a href="command-line-options.md">instalador</a> equivalente é <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Opção de exibição silenciosa. O instalador executa uma instalação sem exibir uma interface do usuário. Nenhum prompt, mensagens ou caixas de diálogo são exibidos para o usuário. O usuário não pode cancelar a instalação. Use as opções de linha de <strong>comando padrão /norestart</strong> ou <strong>/forcerestart</strong> para controlar reinicializações. Se nenhuma opção de reinicialização for especificada, o instalador reiniciará o computador sempre que necessário sem exibir nenhum aviso ou prompt para o usuário.<br/> Exemplos: <br/> <strong>msiexec /package Application.msi /quiet</strong><br/> <strong>Msiexec /uninstall Application.msi /quiet</strong><br/> <strong>Msiexec /update msipatch.msp /quiet</strong><br/> <strong>Msiexec /uninstall msipatch.msp /package Application.msi/quiet</strong><br/>
<blockquote>
[!Note]<br />
A opção Windows linha de comando do <a href="command-line-options.md">instalador</a> equivalente é <strong>/qn</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Opção de exibição passiva. O instalador exibe uma barra de progresso para o usuário que indica que uma instalação está em andamento, mas nenhuma mensagem de erro ou prompt é exibida para o usuário. O usuário não pode cancelar a instalação. Use as opções de linha de <strong>comando padrão /norestart</strong> ou <strong>/forcerestart</strong> para controlar reinicializações. Se nenhuma opção de reinicialização for especificada, o instalador reiniciará o computador sempre que necessário sem exibir nenhum aviso ou prompt para o usuário. <br/> Exemplo: <strong>msiexec /package Application.msi /passive</strong> <br/>
<blockquote>
[!Note]<br />
A opção Windows linha de comando do <a href="command-line-options.md">instalador</a> equivalente é <strong>/qb!-</strong> com <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S definido na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Opção Nunca reiniciar. O instalador nunca reinicia o computador após a instalação.<br/> Exemplo: msiexec /package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
A linha Windows comando do instalador equivalente tem <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress definido na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Sempre reinicie a opção. O instalador sempre reinicia o computador após cada instalação.<br/> Exemplo: msiexec /package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
A linha Windows comando do instalador equivalente tem <a href="reboot.md"><strong>REBOOT</strong></a>=Force definido na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Prompt antes de reiniciar a opção. Exibe uma mensagem de que uma reinicialização é necessária para concluir a instalação e pergunta ao usuário se o sistema deve ser reiniciado agora. Essa opção não pode ser usada junto com a <strong>opção /quiet.</strong><br/>
<blockquote>
[!Note]<br />
O equivalente Windows linha de comando do Instalador tem <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; definido na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Opção de desinstalar o produto. Desinstala um produto.<br/>
<blockquote>
[!Note]<br />
A opção Windows linha de comando do <a href="command-line-options.md">instalador</a> equivalente é <strong>/x.</strong>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/uninstall</strong></td>
<td><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1> [; Update2.msp | PatchGUID2]</em></td>
<td>Opção de atualização de desinstalação. Desinstala um patch de atualização.<br/>
<blockquote>
[!Note]<br />
A opção Windows linha de <a href="command-line-options.md">comando</a> do instalador equivalente é <strong>/I</strong> com <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[; Update2.msp | PatchGUID2] definido na linha de comando.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Opção de log. Grava informações de log em um arquivo de log no caminho existente especificado. O caminho para o local do arquivo de log já deve existir. O instalador não cria a estrutura de diretório para o logfile.<br/> As seguintes informações são inseridas no log:<br/>
<ul>
<li>Mensagens de status</li>
<li>Avisos nãofatais</li>
<li>Todas as mensagens de erro</li>
<li>Iniciar ações</li>
<li>Registros específicos da ação</li>
<li>Solicitações do usuário</li>
<li>Parâmetros iniciais da interface do usuário</li>
<li>Informações de saída fatais ou sem memória</li>
<li>Mensagens de espaço fora do disco</li>
<li>Propriedades do terminal</li>
</ul>
<blockquote>
[!Note]<br />
A opção Windows linha de comando <a href="command-line-options.md">do instalador</a> equivalente <strong>é /L*.</strong>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Para obter mais informações sobre todos os métodos disponíveis para definir o modo de registro em log, consulte Registro em log <a href="normal-logging.md">normal</a> na seção registro em log do <a href="windows-installer-logging.md">Windows Instalador.</a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Opção Instalar produto. Instala ou configura um produto.<br/>
<blockquote>
[!Note]<br />
A opção Windows linha de comando do <a href="command-line-options.md">instalador</a> equivalente é <strong>/I</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/update</strong></td>
<td><em><Update1.msp>[; Update2.msp]</em></td>
<td>Opção Instalar patches. Instala um ou vários patches. <br/>
<blockquote>
[!Note]<br />
A linha de Windows do instalador equivalente tem <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<; PatchGuid2> definido na linha de comando.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
