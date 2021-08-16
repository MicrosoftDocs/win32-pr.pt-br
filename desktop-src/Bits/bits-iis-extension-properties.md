---
title: Propriedades de extensão do IIS do BITS
description: Serviço de Transferência Inteligente em Segundo Plano (BITS) usa uma ISAPI para estender o IIS para dar suporte a trabalhos de carregamento.
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- BITS de propriedades de extensão do IIS do BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c81d57114a23a07c5f952a9cb33399644f5cbed8bbf67cccf802a1c996b72b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835164"
---
# <a name="bits-iis-extension-properties"></a>Propriedades de extensão do IIS do BITS

Serviço de Transferência Inteligente em Segundo Plano (BITS) usa uma ISAPI para estender o IIS para dar suporte a [**trabalhos de carregamento**](/windows/win32/api/bits/ne-bits-bg_job_type). A tabela a seguir lista as propriedades que o BITS adiciona à metabase do IIS para o componente do diretório virtual. O BITS usa essas propriedades para determinar como carregar os arquivos. As propriedades de extensão do IIS do BITS são herdáveis, exceto para **BITSUploadEnabled**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BITSUploadEnabled</strong> Tipo de dados: <strong>booliano</strong><br/></td>
<td>Indica se os carregamentos do BITS estão habilitados no diretório virtual. Se a configuração não estiver presente ou for 0, os carregamentos do BITS serão desabilitados.<br/> Trata-se de uma propriedade somente leitura. Para definir essa propriedade, chame o método <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>EnableBITSUploads</strong></a> ou <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>DisableBITSUploads</strong></a> da interface <a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>IBITSExtensionSetup</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><strong>BITSSessionTimeout</strong> Tipo de dados: <strong>DWORD</strong><br/></td>
<td>Número de segundos em que a conexão será mantida se nenhum progresso for fazer upload do arquivo; o temporizador é redefinido quando o andamento é realizado. O BITS fechará a conexão se o tempo limite for atingido e limpará os dados associados à sessão.<br/> Definir um tempo limite de sessão curto pode ser um problema para trabalhos de resposta de upload porque a resposta só é baixada quando o usuário está conectado e conectado à rede. É possível que a sessão expire até que a resposta seja baixada; nesse caso, a sessão é cancelada e o arquivo de resposta é excluído.<br/> Observe que o BITS cancelará o trabalho se o valor de Política de Grupo <a href="/windows/win32/bits/group-policies">JobInactivityTimeout</a> (o padrão é 90 dias) for atingido, independentemente dessa configuração.<br/> O valor padrão é 1.209.600 (14 dias).<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSMaximumUploadSize</strong> Tipo de dados: <strong>cadeia de caracteres</strong><br/></td>
<td>Número máximo de bytes que podem ser carregados por trabalho. Especifique o número máximo de bytes como uma cadeia de caracteres decimal; o valor da cadeia de caracteres deve ser menor ou igual a &quot; 1844674407370955 &quot; . Uma cadeia de caracteres vazia é a mesma que especificar &quot; 1844674407370955 &quot; .<br/> O valor padrão é uma cadeia de caracteres vazia.<br/>
<blockquote>
[!Note]<br />
No IIS 7, o limite de upload padrão é 30 milhões bytes. O valor da propriedade <strong>BITSMaximumUploadSize</strong> não pode exceder o limite do IIS. Para obter detalhes e informações sobre como alterar o padrão do IIS, consulte <a href="https://support.microsoft.com//kb/942074">KB942074</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSServerNotificationType</strong> Tipo de dados: <strong>DWORD</strong><br/></td>
<td>Especifica como enviar o arquivo de upload para o aplicativo de servidor. Os valores possíveis são: 0, 1 e 2.<br/> Um valor de 0 significa que o arquivo não é enviado para o aplicativo de servidor. O BITS coloca o arquivo de carregamento no diretório especificado no nome remoto (o nome remoto especificado quando você <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile">adicionou o arquivo</a> ao trabalho) sem notificar o aplicativo de servidor. Se o arquivo existir atualmente no diretório de destino, ele será substituído pelo arquivo de carregamento.<br/> Um valor de 1 significa que o BITS passa o local do arquivo de carregamento para o aplicativo de servidor especificado na propriedade <strong>BITSServerNotificationURL</strong> . O aplicativo de servidor processa o arquivo e gera um arquivo de resposta, se necessário. Por padrão, o BITS remove os arquivos de upload e de resposta do servidor depois de receber a resposta do aplicativo de servidor. Para que o BITS Copie o arquivo de upload para o local especificado pelo nome do arquivo remoto no trabalho, inclua o cabeçalho <a href="/windows/win32/bits/notification-protocol-for-server-applications">bits-Copy-file-to-Destination</a> em sua resposta. Se você não incluir o cabeçalho e quiser salvar os arquivos de upload e de resposta, deverá copiar os arquivos de upload e de resposta em um novo local antes de responder.<br/> Um valor de 2 significa que o BITS passa o arquivo de carregamento no corpo da solicitação para o aplicativo de servidor especificado na propriedade <strong>BITSServerNotificationURL</strong> . O aplicativo de servidor processa o arquivo e retorna a resposta no corpo da resposta, se necessário.<br/> Para obter detalhes sobre os cabeçalhos de solicitação e resposta, consulte <a href="/windows/win32/bits/notification-protocol-for-server-applications">protocolo de notificação para aplicativos de servidor</a>.<br/> O aplicativo de servidor deve fornecer uma resposta em cinco minutos. Se o aplicativo do servidor não responder em cinco minutos, o trabalho entrará no estado de erro transitório. Quando o <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>intervalo de repetição</strong></a> expirar, o servidor bits enviará outra notificação para o aplicativo de servidor (o aplicativo de servidor deve ser gravado para lidar com notificações duplicadas). <strong>BITS 1,5:</strong> O tempo limite de notificação é de 30 segundos.<br/> <br/> O valor padrão é 0.<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSServerNotificationURL</strong> Tipo de dados: <strong>cadeia de caracteres</strong><br/></td>
<td>Opcional. Contém a URL do aplicativo de servidor para o qual o BITS publica o arquivo de carregamento. Você deve especificar uma URL se o valor da propriedade <strong>BITSServerNotificationType</strong> for 1 ou 2. A URL é limitada a 2.200 caracteres, não incluindo o terminador nulo. A URL deve ser uma URL HTTP; O BITS não oferece suporte a URLs de notificação HTTPS.<br/> Se a URL não estiver disponível no momento do carregamento, o BITS tentará o upload novamente até que a URL de notificação exista ou até que o período de repetição expire.<br/> Observe que, se o nome remoto especificado no trabalho contiver uma cadeia de caracteres de consulta, a cadeia de caracteres de consulta será anexada à URL que você especificar. Por exemplo, se o nome remoto contiver https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 e você especificar a configuração <strong>BITSServerNotificationURL</strong> como https://otherserver/myvdir2/bag.asp , a URL para a qual o bits é Postado https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 .<br/> Se a URL original for https://myserver/myvdir/file.txt e a URL de notificação for myasp. asp, o bits usará http//meuservidor/MyVDir/myasp. asp como a URL de notificação.<br/> Se a parte do caminho e do nome do arquivo da URL contiver caracteres Unicode que não são comuns à página de código no cliente e no servidor, a conversão da URL falhará no servidor e o trabalho do BITS será colocado no estado de erro. Se a parte do servidor da URL contiver caracteres Unicode, você deverá codificar a parte do servidor usando <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">nomes de domínio internacionalizados</a> (IDN).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSHostId</strong> Tipo de dados: <strong>cadeia de caracteres</strong><br/></td>
<td>Defina essa propriedade se a instalação do servidor for uma web farm que não usa armazenamento compartilhado.<br/> Especifique o nome do servidor ou o endereço IP do servidor ao qual se conectar novamente depois que o processo de carregamento for interrompido. Normalmente, você especifica o nome do servidor que está configurando. A URL é limitada a 300 caracteres, não incluindo o terminador nulo.<br/> Se você não especificar essa propriedade e o processo de carregamento for interrompido, será possível que o BITS retome o trabalho em outro servidor no farm. No entanto, o servidor anterior ainda contém o arquivo de carregamento parcial antes da interrupção. O BITS remove o arquivo parcial após o <strong>BITSSessionTimeout</strong> expirar.<br/>
<blockquote>
[!Note]<br />
Não use a propriedade <strong>BITSHostId</strong> se o SSL for usado em um Web farm que usa o NLB (balanceamento de carga de rede) ou nomes DNS com vários endereços IP, a menos que você inclua o nome do cluster e os nomes de servidor individuais no certificado. (Se o nome do servidor especificado em <strong>BITSHostId</strong> não corresponder ao nome comum no certificado, o trabalho falhará.) Em vez disso, para o NLB, defina o parâmetro <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">Affinity</a> como <strong>single</strong> para garantir que o cliente se comunique com o mesmo servidor no futuro.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSHostIdFallbackTimeout</strong> Tipo de dados: <strong>DWORD</strong><br/></td>
<td>Número de segundos em que o cliente BITS tenta se reconectar ao nome do servidor <strong>BITSHostId</strong> antes de reverter para o nome de host especificado no nome do arquivo remoto do trabalho. O temporizador começa quando o BITS não consegue se conectar ao servidor <strong>BITSHostId</strong> . O temporizador é redefinido quando o cliente se conecta com êxito ao servidor.<br/> Observe que o valor de tempo limite sem progresso do trabalho (consulte <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>método ibackgroundcopyjob:: SetNoProgressTimeout</strong></a>) deve ser maior que esse valor de tempo limite. Caso contrário, o trabalho falhará antes de o valor de tempo limite de fallback expirar.<br/> Defina essa propriedade somente se você definir a propriedade <strong>BITSHostId</strong> .<br/> O valor padrão é 86.400 (1 dia).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSAllowOverwrites</strong> Tipo de dados: <strong>inteiro</strong><br/></td>
<td>Indica se um arquivo de carregamento pode substituir um arquivo existente com o mesmo nome. O arquivo de carregamento substitui o arquivo existente se <strong>BITSAllowOverwrites</strong> for 1.<br/> O valor padrão é 0.<br/> <strong>IIS 6,0:</strong> Você pode definir essa propriedade somente de um script, não pode defini-la usando a página de propriedades de extensão do BITS na interface do usuário do IIS.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUseDefault</strong> Tipo de dados: <strong>booliano</strong><br/></td>
<td>Indica se a tarefa de limpeza usa as agendas padrão. Por padrão, a tarefa de limpeza é executada a cada 12 horas.<br/> Defina como 1 para usar o agendamento padrão; caso contrário, 0 para especificar uma agenda.<br/> Para especificar uma agenda, use as propriedades <strong>BITSCleanupCount</strong> e <strong>BITSCleanupUnits</strong> .<br/> A tarefa de limpeza limpa o diretório virtual excluindo os trabalhos que não foram modificados dentro do período de tempo limite da sessão (consulte <strong>BITSSessionTimeout</strong>).<br/> O padrão é 1 usar o agendamento padrão.<br/> <strong>IIS 6,0:</strong> Sem suporte.<br/></td>
</tr>
<tr class="even">
<td><strong>BITSCleanupCount</strong> Tipo de dados: <strong>inteiro</strong><br/></td>
<td>Especifica o intervalo a aguardar entre a execução da tarefa de limpeza. O intervalo que você pode especificar depende das unidades. Para obter possíveis valores de intervalo, consulte a propriedade <strong>BITSCleanupUnits</strong> .<br/> Essa propriedade será ignorada se <strong>BITSCleanupUseDefault</strong> for 0.<br/> <strong>IIS 6,0:</strong> Sem suporte.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUnits</strong> Tipo de dados: <strong>inteiro</strong><br/></td>
<td>Especifica as unidades para o intervalo de limpeza especificado na propriedade <strong>BITSCleanupCount</strong> . Essa propriedade será ignorada se <strong>BITSCleanupUseDefault</strong> for 0.<br/> Os valores possíveis são:<dl> 0: as unidades são minutos. Os valores possíveis são 1 a 60.<br />
1: as unidades são horas. Esse é o padrão. Os valores possíveis são 1 a 24.<br />
2: as unidades são dias. Os valores possíveis são 1 a 360.<br />
</dl> <br/> <strong>IIS 6,0:</strong> Sem suporte.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSNumberOfSessionsLimit</strong> Tipo de dados: <strong>inteiro</strong><br/></td>
<td>Limita o número de sessões de carregamento que podem existir simultaneamente para um usuário. Se o número de sessões de um usuário for maior que esse limite, quando a tarefa de limpeza for executada, as sessões mais recentes serão excluídas até que o número de sessões do usuário esteja abaixo do limite.<br/> O padrão é 50 sessões.<br/> <strong>IIS 6,0:</strong> Sem suporte.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSSessionLimitEnable</strong> Tipo de dados: <strong>booliano</strong><br/></td>
<td>Indica se o BITS limita o número de sessões de carregamento por usuário. Se a configuração não estiver presente ou for 0, o limite será desabilitado.<br/> Para especificar o limite, defina a propriedade <strong>BITSNumberOfSessionsLimit</strong> .<br/> O padrão é 1.<br/> <strong>IIS 6,0:</strong> Sem suporte.<br/> <br/></td>
</tr>
</tbody>
</table>



 

o exemplo a seguir mostra como definir as propriedades de extensão do IIS do BITS usando Windows Host de Script. Se o diretório virtual apontar para um compartilhamento remoto, defina também as propriedades de **UNCPassword** do **UNCUserName** e do IIS.


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

// Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



 

