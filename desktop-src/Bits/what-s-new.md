---
title: Novidade (BITS)
description: A tabela a seguir identifica o que há de novo para cada versão do Serviço de Transferência Inteligente em Segundo Plano (BITS).
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- o que há de novo BITS
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b171a1d8cede9e3fd49ac81ab47ffb09f72b6200
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008681"
---
# <a name="whats-new-bits"></a>Novidade (BITS)

Desde sua primeira versão como parte do Windows XP, a Serviço de Transferência Inteligente em Segundo Plano (BITS) foi constantemente aprimorada, adicionando controles mais poderosos para o desenvolvedor e o administrador controlar e gerenciar downloads. Um conjunto avançado de cmdlets do PowerShell foi adicionado; Ele pode se conectar a mais tipos de servidores HTTP; é mais cuidadoso na largura de banda da rede e nos custos do usuário do que nunca. 

A tabela a seguir identifica o que há de novo para cada versão do Serviço de Transferência Inteligente em Segundo Plano (BITS).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versão</th>
<th>Descrição dos recursos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versão 10,3</td>
<td>Novos recursos:<br/>
<ul>
<li>Adição de <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> para marcar cabeçalhos HTTP como somente gravação e para definir um retorno de chamada de validação de certificado do servidor.</li>
<li>O BITS reterá sua identidade de serviço quando for criado por outro serviço do sistema.</li>
<li>O BITS continuará a transferir arquivos no modo de espera conectado, desde que o dispositivo esteja conectado.</li>
</ul>
O BITS versão 10,3 está incluído no Windows 10 maio 2019 atualização (10,0; Build 18362) e posterior.
</td>
</tr>
<tr class="even">
<td>Versão 10,2</td>
<td>Novos recursos:<br/>
<ul>
<li><a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> adicionado para alterar o método http para downloads de http.</li>
<li>O BITS agora usa a ordem de proxy padrão para ser mais consistente com o restante do sistema.</li>
<li>É mais fácil para os programadores definirem a configuração de proxy do BITS para cenários empresariais.</li>
<li>O BITS agora tem mais cuidado de energia e dá suporte à [espera moderna](/windows-hardware/design/device-experiences/modern-standby).</li>
<li>O BITS agora oferece suporte a [políticas](/windows/client-management/mdm/policy-configuration-service-provider) de MDM (Mobile Device Manager), além de [diretivas de grupo](./group-policies).</li>
</ul>
O BITS versão 10,2 está incluído na atualização de 10 de outubro de 2018 do Windows (10.0; Build 17763) e posterior.
</td>
</tr>
<tr class="odd">
<td>Versão 10,1</td>
<td>Novos recursos:<br/>
<ul>
<li>Adição de <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> e <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> para habilitar cenários de acesso aleatório para downloads de http.</li>
<li>Adicionado <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> e <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> à enumeração <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> para ajustar os comportamentos de download e notificação, respectivamente.</li>
</ul>
O BITS versão 10,1 está incluído na atualização do Windows 10 Creator e posterior.
</td>
</tr>
<tr class="even">
<td>Versão 5.0</td>
<td>Novos recursos:<br/>
<ul>
<li>Adicionada a interface <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> , que adiciona métodos genéricos para obter e definir propriedades de trabalho do bits para os métodos herdados da interface <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> .<br/> Para obter informações sobre como usar a nova interface <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> , consulte <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">como controlar se um trabalho do bits tem permissão para baixar em uma conexão cara</a> e <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">como obter o último conjunto de cabeçalhos HTTP recebido para cada arquivo em um trabalho de download do bits</a>.<br/></li>
<li>Adicionada a União de <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> e a <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>e as enumerações de <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> . Para obter exemplos de uso, consulte os tópicos de instruções acima.</li>
<li>Adicionada a interface <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> , que adiciona métodos para obter e definir propriedades genéricas em objetos BackgroundCopyFile para os métodos herdados da interface <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> . A adição de propriedades genéricas tornará possível aprimorar os recursos do BackgroundCopyFile no futuro sem a necessidade de criar uma nova interface.</li>
<li>A primeira Propriedade genérica exposta por <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> é a propriedade <strong>HttpResponseHeaders</strong> .</li>
<li>Adicionada a União de <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> e a enumeração <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> .</li>
</ul>
O BITS versão 5,0 está incluído nos sistemas operacionais Windows Server 2012 e Windows 8, em que a versão do% windir% \System32\QMgr.dll é &quot; 7.7. xxxx. xxxx &quot; .<br/> Os recursos a seguir foram adicionados aos BITS no Windows 10<br/>
<ul>
<li>No Windows 10, versão 1607, é possível usar as APIs COM do BITS e os cmdlets do PowerShell do BITS (quando disponíveis) em uma sessão remota do PowerShell. Isso é especialmente útil ao administrar versões do Windows Server 2016 que não têm nenhum recurso de logon local. Os trabalhos BITS iniciados por meio de sessões remotas do PowerShell são executados no contexto da conta do usuário da sessão e somente avançarão quando houver pelo menos uma sessão de logon local ativa ou uma sessão remota do PowerShell associada à conta do usuário. Considere usar sessões remotas do PowerShell persistentes (consulte <a href="/powershell/module/microsoft.powershell.core/new-pssession">New-PSSession</a>) para transferências de execução longa.</li>
<li>No Windows 10, versão 1607, agora é possível que um proprietário do trabalho do BITS defina tokens auxiliares sem ser um administrador, desde que o token auxiliar não tenha recursos de administrador. Isso reduz a superfície de vulnerabilidade de download em segundo plano ou de ferramentas de atualização, permitindo sua execução com a conta NetworkService com menos privilégios, em vez de uma conta com privilégios administrativos.</li>
</ul>
O BITS versão 5,0 também está incluído no Windows 10, em que a versão do% windir% \System32\QMgr.dll é &quot; 7.8. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versão 4.0</td>
<td>Novos recursos:<br/>
<ul>
<li>O cache de pares agora usa o Windows BranchCache. Esse novo modelo de cache de pares substitui o modelo usado para o BITS versão 3,0. Para obter mais informações, consulte <a href="peer-caching.md">cache de pares</a>.</li>
<li>Adicionou um modelo de acesso a recursos mais flexível que permite que os aplicativos associem um par de tokens de segurança a um trabalho de transferência do BITS. Para obter mais informações, consulte <a href="helper-tokens-for-bits-transfer-jobs.md">tokens auxiliares para trabalhos de transferência do bits</a>.</li>
<li>Adicionado o <a href="bits-compact-server.md">bits Compact Server</a>, que é um servidor de arquivos http/https autônomo que fornece a capacidade de transferir um número limitado de arquivos grandes de forma assíncrona entre computadores.</li>
<li>Maior limitação de largura de banda granular. Para obter mais informações, consulte <a href="group-policies.md">políticas de grupo</a>.</li>
</ul>
O BITS versão 4,0 está incluído nos sistemas operacionais Windows Server 2008 R2 e Windows 7.<br/> Você também pode baixar o BITS 4,0 para Windows Server 2008 com Service Pack 2 (SP2), Windows Vista com Service Pack 1 (SP1) e Windows Vista com Service Pack 2 (SP2). Para obter informações sobre como baixar BITS 4,0, consulte <a href="https://support.microsoft.com/kb/968929">KB968929</a>.<br/> A versão de% windir% \System32\QMgr.dll é &quot; 7.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versão 3.0</td>
<td>Novos recursos:<br/>
<ul>
<li>Adicionado <a href="peer-caching.md">cache de sistemas pares</a> , que permite baixar conteúdo de pares e também fornecer conteúdo a pares em uma rede de domínio.</li>
<li><a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">Notificação</a> adicionada para quando um arquivo é baixado.</li>
<li>Acesso adicionado ao <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">arquivo temporário</a> enquanto o download está em andamento.</li>
<li>Adicionada a capacidade de controlar <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">redirecionamentos</a>de http.</li>
<li>Adição de mais <a href="group-policies.md">políticas de grupo</a> para controlar o cache de pares e limitar os tempos de download.</li>
<li>Adição de eventos de diagnóstico e solução de problemas ao log de eventos do sistema.</li>
<li>Adicionado suporte para UAC ( <a href="user-account-control-and-bits.md">controle de conta de usuário</a> ).</li>
<li>No Windows Vista e superior, o tipo de inicialização BITS padrão é de início automático atrasado.</li>
</ul>
<blockquote>
[!Note]<br />
O BITS agora usa políticas de grupo para limitar o número de trabalhos e arquivos que você pode criar. Isso pode afetar os aplicativos que atualmente criam um grande número de trabalhos ou adicionar um grande número de arquivos a um trabalho.
</blockquote>
<br/> <br/> O BITS versão 3,0 está incluído nos sistemas operacionais Windows Server 2008 e Windows Vista. <br/> A versão de% windir% \System32\QMgr.dll é &quot; 7.0. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versão 2,5</td>
<td>Suporte adicionado para cabeçalhos HTTP personalizados, autenticação de cliente baseada em certificado para transportes HTTP seguros e IPv6. Também foi adicionado o uso de contadores de IGD (dispositivo de gateway de Internet) para calcular com mais precisão a <a href="network-bandwidth.md">largura de banda</a>disponível.<br/> Os recursos do BITS 2,5 estão disponíveis nos sistemas operacionais Windows Server 2008, Windows Vista e Windows XP com Service Pack 3 (SP3). <br/> Você também pode baixar o BITS 2,5 para Windows Server 2003 com Service Pack 2 (SP2), Windows Server 2003 com Service Pack 1 (SP1) e Windows XP com Service Pack 2 (SP2). Para baixar o BITS 2,5, vá para o <a href="https://www.microsoft.com/download/details.aspx?id=4933">centro de download da Microsoft</a> e instale o KB923845.<br/> A versão de% windir% \System32\QMgr.dll é &quot; 6.7. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versão 2,0</td>
<td>Adição de suporte para a execução de downloads simultâneos em primeiro plano, usando caminhos de protocolo SMB para nomes remotos, baixando intervalos de um arquivo, alterando o prefixo ou o nome completo de um nome remoto e limitando o uso de largura de banda do cliente. A política JobInactivityTimeout agora está localizada em configuração do computador, Modelos Administrativos, rede, Serviço de Transferência Inteligente em Segundo Plano (BITS).<br/> O BITS versão 2,0 está incluído no Windows XP com SP2 e no Windows Server 2003 com SP1. Você também pode baixar o BITS 2,0 para o Windows Server 2003 e o Windows XP. Para baixar o BITS 2,0, vá para o <a href="https://www.microsoft.com/download/details.aspx?id=19031">centro de download da Microsoft</a> e instale o KB842773.<br/> A versão de% windir% \System32\QMgr.dll é &quot; 6.6. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versão 1.5</td>
<td>Adição de upload e upload – capacidade de resposta, execução de linha de comando para eventos e credenciais explícitas e credenciais de proxy.<br/> A partir do BITS 1,5, os usuários com um <a href="/windows/win32/secauthz/restricted-tokens">token restrito</a> não podem criar ou modificar trabalhos.<br/> O BITS versão 1,5 está incluído no Windows Server 2003. Um redistribuível está disponível para o Windows XP no <a href="https://www.microsoft.com/download/details.aspx?id=22250">centro de download da Microsoft</a>.<br/> A versão de% windir% \System32\QMgr.dll é &quot; 6.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versão 1,2</td>
<td>Mesma funcionalidade da versão 1,0. Contém atualizações e aprimoramentos internos.<br/> O BITS versão 1,2 está incluído no Windows XP com Service Pack 1 (SP1).<br/> A versão de% windir% \System32\QMgr.dll é &quot; 6.2. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versão 1.0</td>
<td>Versão inicial. Fornece downloads priorizados, restritos e assíncronos em segundo plano ou em primeiro plano. Os downloads são retomados automaticamente após a reinicialização do computador e a desconexão de rede.<br/> O BITS versão 1,0 está incluído no Windows XP.<br/> A versão de% windir% \System32\QMgr.dll é &quot; 6.0. xxxx. xxxx &quot; .<br/></td>
</tr>
</tbody>
</table>

Para liberar recursos em seu programa com base em recursos de BITS, use QueryInterface em (por exemplo) seu objeto de trabalho para ver se o objeto de trabalho permite que você crie a versão necessária. Como alternativa, consulte [determinando a versão do bits em um computador](./determining-the-version-of-bits-on-a-computer.md) para converter o número de versão QMgr.dll na versão bits.

## <a name="version-103"></a>Versão 10,3

As seguintes interfaces foram adicionadas para esta versão
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
     [ **IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>Versão 10,2

As seguintes interfaces foram adicionadas para esta versão
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>Versão 10,1

As seguintes interfaces foram adicionadas para esta versão
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

As constantes a seguir foram adicionadas para uso com a [enumeração BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id).

-   **\_ \_ propriedade de trabalho \_ do bits sob o \_ modo de demanda \_**
-   **\_intervalo de \_ notificação mínimo da propriedade de trabalho do bits \_ \_ \_ \_ MS**


## <a name="version-50"></a>Versão 5.0

As seguintes interfaces foram adicionadas para esta versão:

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>Versão 4.0

As seguintes interfaces foram adicionadas para esta versão:

-   [**IBitsToken**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>Versão 3.0

As seguintes interfaces foram adicionadas para esta versão:

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**IBitsPeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**IBitsPeerCacheAdministration**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**IBitsPeerCacheRecord**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**IEnumBitsPeerCacheRecords**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**IEnumBitsPeers**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

As constantes a seguir foram adicionadas para uso com o método [**IBackgroundCopyJobHttpOptions:: SetSecurityFlags**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) :

-   **\_política de \_ redirecionamento http BG \_ \_ permitir \_ silencioso**
-   **\_política de \_ redirecionamento http BG \_ \_ permitir \_ relatório**
-   **\_política de \_ redirecionamento http BG não \_ \_ permitir**
-   **\_máscara de \_ política de redirecionamento de http BG \_ \_**
-   **\_ \_ política de redirecionamento http BG \_ \_ permitir \_ https \_ para \_ http**

## <a name="version-25"></a>Versão 2,5

A interface e a enumeração a seguir foram adicionadas para a versão 2,5:

-   [**IBackgroundCopyJobHttpOptions**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**\_local de \_ armazenamento de certificado BG \_**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>Versão 2,0

As seguintes interfaces, estrutura e tópicos foram adicionados para a versão 2,0:

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**\_intervalo de arquivos BG \_**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [Políticas de grupo](group-policies.md)

Para obter informações sobre downloads simultâneos em primeiro plano, consulte a seção comentários para [**\_ \_ prioridade de trabalho BG**](/windows/win32/api/Bits/ne-bits-bg_job_priority).

Para obter informações sobre como usar o protocolo SMB, consulte [**BG \_ File \_ info**](/windows/win32/api/Bits/ns-bits-bg_file_info).

## <a name="version-15"></a>Versão 1.5

As seguintes interfaces e tópicos foram adicionados para a versão 1,5:

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [Recuperando a resposta de um trabalho de Upload-Reply](retrieving-the-reply-from-an-upload-reply-job.md)
-   [Registrando para executar um programa](registering-to-execute-a-program.md)
-   [Configurações do servidor BITS para trabalhos de carregamento](bits-server-settings-for-upload-jobs.md)
-   [Configurando o servidor para carregamentos](setting-up-the-server-for-uploads.md)
-   [Usando cabeçalhos de solicitação/resposta de notificação do BITS](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>Atualizando versões do BITS
 
Você pode baixar o BITS 4,0 para Windows Server 2008 com Service Pack 2 (SP2), Windows Vista com Service Pack 1 (SP1) e Windows Vista com Service Pack 2 (SP2). Para obter informações sobre como baixar BITS 4,0, consulte [KB968929](https://support.microsoft.com/kb/968929).
