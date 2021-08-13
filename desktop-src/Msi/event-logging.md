---
description: Windows Os eventos fornecem uma maneira padrão e centralizada para aplicativos (e o sistema operacional) para registrar eventos importantes de software e hardware.
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: log de eventos (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c1aa4808727a220ec104cb3e7bfdff2741dcb2366ca1468288a082baab813b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636920"
---
# <a name="event-logging-windows-installer"></a>log de eventos (Windows Installer)

[Windows eventos](../events/windows-events.md) fornece uma maneira padrão e centralizada para aplicativos (e o sistema operacional) para registrar eventos importantes de software e hardware. O serviço de log de eventos armazena eventos de várias fontes em uma única coleção chamada *log de eventos*. antes do Windows Vista, você usaria o [rastreamento de eventos para Windows](../etw/event-tracing-portal.md) (ETW) ou [log de eventos](../eventlog/event-logging.md) para registrar eventos. Windows o Vista introduziu um novo modelo de eventos que unifica o ETW e a API de [Log de eventos Windows](../wes/windows-event-log.md) .

O instalador também grava entradas no log de eventos. Esses eventos de registro, como os seguintes:

-   Êxito ou falha da instalação; remoção ou reparo de um produto.
-   Erros que ocorrem durante a configuração do produto.
-   Detecção de dados de configuração corrompidos.

Se uma grande quantidade de informações for gravada, o arquivo de log de eventos poderá ficar cheio e o instalador exibirá a mensagem "o arquivo de log do aplicativo está cheio".

O instalador pode gravar as entradas a seguir no log de eventos. Todas as mensagens de log de eventos têm uma ID de evento exclusiva. Todos os erros gerais criados na [tabela de erros](error-table.md) que são retornados para uma instalação que falha são registrados no log de eventos do aplicativo com uma ID de mensagem igual ao erro + 10.000. Por exemplo, o número do erro na tabela de erros para uma instalação concluída com êxito é 1707. A instalação bem-sucedida é registrada no log de eventos do aplicativo com uma ID de mensagem 11707 (1707 + 10.000).

para obter informações sobre como habilitar o log detalhado no computador de um usuário ao solucionar problemas de implantação, consulte [práticas recomendadas de Windows Installer](windows-installer-best-practices.md).



<table>
<thead>
<tr class="header">
<th>ID do evento</th>
<th>Mensagem</th>
<th>Comentários</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1001</td>
<td>Falha na detecção do produto ' %1 ', recurso ' %2 ' durante a solicitação do componente ' %3 '</td>
<td>Uma mensagem de aviso. Para obter detalhes, consulte <a href="searching-for-a-broken-feature-or-component.md">pesquisando um recurso ou componente desfeito</a>.</td>
</tr>
<tr class="even">
<td>1002</td>
<td>Valor inesperado ou ausente (nome: ' %1 ', valor: ' %2 ') na chave ' %3 '</td>
<td>Mensagem de erro de que havia um valor inesperado ou ausente.</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>Subchave inesperada ou ausente ' %1 ' na chave ' %2 '</td>
<td>Mensagem de erro informando que havia uma subchave inesperada ou ausente.</td>
</tr>
<tr class="even">
<td>1004</td>
<td>falha na detecção do produto ' %1 ', recurso ' %2 ', componente ' %3 ' <strong>observação:</strong> começando com Windows Installer versão 2,0, esta mensagem é: falha na detecção do produto ' %1 ', recurso ' %2 ', componente ' %3 '. O recurso ' %4 ' não existe.<br/></td>
<td>Uma mensagem de aviso. Consulte também <a href="searching-for-a-broken-feature-or-component.md">procurando um componente ou recurso desfeito</a>.</td>
</tr>
<tr class="odd">
<td>1005</td>
<td>A operação de instalação iniciou uma reinicialização</td>
<td>Mensagem informativa de que a instalação iniciou uma reinicialização do sistema.</td>
</tr>
<tr class="even">
<td>1006</td>
<td>Não é possível executar a verificação da assinatura digital para o gabinete ' %1 '. WinVerifyTrust não está disponível no computador.</td>
<td>Mensagem de aviso. Um gabinete foi criado na <a href="msidigitalsignature-table.md">tabela MsiDigitalSignature</a> para ter uma verificação de <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>WinVerifyTrust</strong></a> executada. Esta ação não pôde ser executada porque o computador não tem as DLLs de criptografia corretas instaladas.</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>A instalação de %1 não é permitida pela política de restrição de software. a Windows Installer permite apenas a execução de itens sem restrições. O nível de autorização retornado pela política de restrição de software era %2.</td>
<td>Uma mensagem de erro indicando que o administrador configurou a diretiva de restrição de software para não permitir essa instalação.</td>
</tr>
<tr class="even">
<td>1008</td>
<td>A instalação de %1 não é permitida devido a um erro no processamento da diretiva de restrição de software. O objeto não pode ser confiável.</td>
<td>Uma mensagem de erro indicando que houve problemas ao tentar verificar o pacote de acordo com a diretiva de restrição de software.</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>esta versão do Windows não oferece suporte à implantação de pacotes de 64 bits. O script ' %1 ' é para um pacote de 64 bits.</td>
<td>Mensagem de erro indicando que os scripts para pacotes de 64 bits só podem ser executados em um computador de 64 bits.</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{Relatório de exceções não tratado}</td>
<td>Mensagem de erro para uma exceção sem tratamento, este é o relatório.</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows Informações de proxy do instalador não registradas corretamente</td>
<td>Mensagem de erro informando que as informações de proxy não foram registradas corretamente.</td>
</tr>
<tr class="even">
<td>1015</td>
<td>Falha ao conectar ao servidor. Erro:% d</td>
<td>Mensagem informativa que a instalação falhou ao se conectar ao servidor.</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>Falha na detecção do produto ' %1 ', recurso ' %2 ', componente ' %3 '. O recurso ' %4 ' em um componente de execução de origem não pôde ser localizado porque nenhuma fonte válida e acessível foi encontrada.</td>
<td>Mensagem de aviso. Para obter mais informações, consulte <a href="searching-for-a-broken-feature-or-component.md">pesquisando um recurso ou componente desfeito</a>.</td>
</tr>
<tr class="even">
<td>1017</td>
<td>O SID do usuário foi alterado de ' %1 ' para ' %2 ', mas o aplicativo gerenciado e as chaves de dados do usuário não podem ser atualizadas. Erro = ' %3 '.</td>
<td>Mensagem de erro indicando que ocorreu um erro ao tentar atualizar o registro do usuário após a alteração do SID do usuário.</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>Não é possível instalar o aplicativo ' %1 ' porque ele não é compatível com esta versão do Windows.</td>
<td>Mensagem de erro indicando que a instalação é incompatível com a versão atualmente em execução do Windows. Contate o fabricante do software que está sendo instalado para uma atualização.</td>
</tr>
<tr class="even">
<td>1019</td>
<td>Produto: %1-a atualização ' %2 ' foi removida com êxito.</td>
<td>Mensagem informativa de que o instalador removeu a atualização. <strong>Windows Installer 2,0:</strong> Não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>Produto: %1-a atualização ' %2 ' não pôde ser removida. Código de erro %3. Informações adicionais estão disponíveis no arquivo de log %4.</td>
<td>Mensagem de erro indicando que o instalador não pôde remover a atualização. Informações adicionais estão disponíveis no arquivo de log. <strong>Windows Installer 2,0:</strong> Não disponível.<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>Produto: %1-a atualização ' %2 ' não pôde ser removida. Código de erro %3.</td>
<td>Mensagem de erro indicando que o instalador não pôde remover a atualização. Para obter informações sobre como ativar o registro em log, consulte <a href="windows-installer-best-practices.md">habilitar o log detalhado no computador do usuário ao solucionar problemas de implantação.</a> <strong>Windows Installer 2,0:</strong> Não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>Produto: %1-atualização ' %2 ' instalada com êxito.</td>
<td>Mensagem informativa que o instalador instalou a atualização com êxito. <strong>Windows Installer 2,0:</strong> Não disponível.<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>Produto: %1-a atualização ' %2 ' não pôde ser instalada. Código de erro %3. Informações adicionais estão disponíveis no arquivo de log %4.</td>
<td>Mensagem de erro indicando que o instalador não pôde instalar a atualização. Informações adicionais estão disponíveis no arquivo de log. <strong>Windows Installer 2,0:</strong> Não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1024</td>
<td>Produto: %1-a atualização ' %2 ' não pôde ser instalada. Código de erro %3.</td>
<td>Mensagem de erro indicando que o instalador não pôde instalar a atualização. Para obter informações sobre como ativar o logon, consulte <a href="windows-installer-best-practices.md">habilitar o log detalhado no computador do usuário ao solucionar problemas de implantação.</a> <strong>Windows Installer 2,0:</strong> Não disponível.<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>Produto: %1. O arquivo %2 está sendo usado pelo seguinte processo: nome: %3, ID %4.</td>
<td><strong>Windows Installer 2,0:</strong> Não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows O instalador determinou que sua chave de registro de dados de configuração não foi protegida corretamente. O proprietário da chave deve ser um sistema local ou Builtin\Administrators. A chave existente será excluída e recriada com as configurações de segurança apropriadas.</td>
<td>Mensagem de aviso. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows O instalador determinou que uma subchave do registro %1 em seus dados de configuração não foi protegida corretamente. O proprietário da chave deve ser um sistema local ou Builtin\Administrators. A subchave existente e todo o seu conteúdo serão excluídos.</td>
<td>Mensagem de aviso. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows O instalador determinou que sua pasta de cache de dados de configuração não foi protegida corretamente. O proprietário da chave deve ser um sistema local ou Builtin\Administrators. A pasta existente será excluída e recriada com as configurações de segurança apropriadas.</td>
<td>mensagem de aviso<strong><a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anterior</a>:</strong> não disponível.<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>Produto: %1. Reinicialização necessária.</td>
<td>Mensagem de aviso indicatiing que uma reinicialização do sistema é necessária para concluir a instalação e a reinicialização foi adiada para um momento posterior. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>Produto: %1. o aplicativo tentou instalar uma versão mais recente do arquivo de Windows protegido %2. Talvez seja necessário atualizar o sistema operacional para que esse aplicativo funcione corretamente. (Versão do pacote: %3, versão protegida do sistema operacional: %4).</td>
<td>mensagem de aviso indicando que a instalação tentou substituir um arquivo crítico protegido por <a href="windows-resource-protection-on-windows-vista.md">Proteção de Recursos do Windows</a>. Uma atualização do sistema operacional pode ser necessária para usar este aplicativo. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>Produto: %1. O assembly ' %2 ' do componente ' %3 ' está em uso.</td>
<td>Mensagem de aviso indicando que a instalação tentou atualizar um assembly em uso no momento. O sistema deve ser reiniciado para concluir a atualização desse assembly. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>Ocorreu um erro ao atualizar as variáveis de ambiente atualizadas durante a instalação de ' %1 '.</td>
<td>Mensagem de aviso indicando que alguns usuários que fizeram logon no computador podem precisar fazer logoff e logon novamente para concluir a atualização de variáveis de ambiente. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/></td>
</tr>
<tr class="even">
<td>1046</td>
<td>Produto: %1. Versão: %2. Idioma: %3. Instalação concluída com o status: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>NomeDoProduto</strong></a> , campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/> Campo 5- <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e anteriores</a>:</strong> Campo 5 não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>Produto: %1. Versão: %2. Idioma: %3. Remoção concluída com o status: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>NomeDoProduto</strong></a> , campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/> Campo 5- <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e anteriores</a>:</strong> Campo 5 não disponível.<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>Produto: %1. Versão: %2. Idioma: %3. Alteração de configuração concluída com o status: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>NomeDoProduto</strong></a> , campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 5- <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e anteriores</a>:</strong> Campo 5 não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>Produto: %1. Versão: %2. Idioma: %3. Atualização: %4. Instalação da atualização concluída com o status: %5. Fabricante: %6.</td>
<td>Campo 1- <a href="productname.md"><strong>NomeDoProduto</strong></a> , campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 4-este é o nome amigável do usuário se a <a href="msipatchmetadata-table.md">tabela MsiPatchMetadata</a> estiver presente no pacote de patch. Caso contrário, esse é o GUID de código de patch do patch.<br/> Campo 5-status da instalação da atualização.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e anteriores</a>:</strong> Não disponível.<br/> Campo 6- <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e anteriores</a>:</strong> Campo 6 não disponível.<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>Produto: %1. Versão: %2. Idioma: %3. Atualização: %4. Remoção da atualização concluída com status: %5. Fabricante: %6.</td>
<td>Campo 1 – <a href="productname.md"><strong>Campo ProductName</strong></a> 2 – <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3 – <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 4 – esse é o nome amigável se a <a href="msipatchmetadata-table.md">Tabela MsiPatchMetadata</a> estiver presente no pacote de patch. Caso contrário, esse é o GUID do código de patch do patch.<br/> Campo 5 – Status da remoção da atualização.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Instalador 3.1 e anterior:</a></strong> Não disponível.<br/> Campo 6 – <a href="manufacturer.md"> <strong>Fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Instalador 4.5 e anteriores:</a></strong> Campo 6 não disponível.<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>Produto: %1. Versão: %2. Idioma: %3. É necessário reiniciar. Tipo de reinicialização: %4. Motivo da reinicialização: %5. Fabricante: %6.</td>
<td>Campo 1 – <a href="productname.md"><strong>Campo ProductName</strong></a> 2 – <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3 – <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <dl> Campo 4 – uma constante que indica o tipo de reinicialização: <br/> <dl> <strong>msirbRebootImmediate</strong> (1) – Houve uma reinicialização imediata do computador.<br />
<strong>msirbRebootDeferred</strong> (2) – um usuário ou administrador adiou uma reinicialização necessária do computador usando a interface do usuário ou <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress.<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbRebootUndeterminedReason</strong> (0)– Reinicialização necessária por um motivo não especificado.<br />
<strong>msirbRebootInUseFilesReason</strong> (1)- Foi necessária uma reinicialização para substituir os arquivos em uso.<br />
<strong>msirbRebootScheduleRebootReason</strong> (2)- O pacote contém uma <a href="schedulereboot-action.md">ação ScheduleReboot.</a><br />
<strong>msirbRebootForceRebootReason</strong> (3)- O pacote contém uma <a href="forcereboot-action.md">ação ForceReboot.</a><br />
<strong>msirbRebootCustomActionReason</strong> (4)- Uma ação personalizada chamada <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>função MsiSetMode.</strong></a><br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Instalador 3.1 e anterior:</a></strong> Não disponível.<br/> Campo 6 – <a href="manufacturer.md"> <strong>Fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Instalador 4.5 e anteriores:</a></strong> Campo 6 não disponível.<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>O instalador encontrou um erro inesperado ao instalar esse pacote. Isso pode indicar um problema com este pacote. O código de erro é [1]. {{Os argumentos são: [2], [3], [4]}}</td>
<td>Mensagem de erro indicando que ocorreu um erro interno. O texto dessa mensagem baseia-se no texto escrito para o erro 5 na tabela Erro.</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>Produto [2] – Operação de instalação concluída com êxito</td>
<td>Mensagem informando que a instalação do produto foi bem-sucedida.</td>
</tr>
<tr class="even">
<td>11708</td>
<td>Produto [2] – Falha na operação de instalação</td>
<td>Mensagem de erro de que a instalação do produto falhou.</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>Produto [2] – Configuração concluída com êxito.</td>
<td>Mensagem informando que a configuração do produto foi bem-sucedida.</td>
</tr>
</tbody>
</table>



 

Você pode importar cadeias de caracteres de erros localizados para eventos em seu banco de dados usando Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). O SDK inclui cadeias de caracteres de recurso localizadas para cada um dos idiomas listados na seção [Localizando as tabelas Error e ActionText.](localizing-the-error-and-actiontext-tables.md) Se as cadeias de caracteres de erro correspondentes a eventos não são populadas, o instalador carrega cadeias de caracteres localizadas para o idioma especificado pela [**propriedade ProductLanguage.**](productlanguage.md)

 

 
