---
description: Considere os seguintes problemas importantes ao usar o recurso de AutoProxy do WinHTTP.
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: Problemas de AutoProxy no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc07ca7320fee028431ff0d89be78ee0b2dc4bb63e8191386808f0936c8a1518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052084"
---
# <a name="autoproxy-issues-in-winhttp"></a>Problemas de AutoProxy no WinHTTP

Considere os seguintes problemas importantes ao usar o recurso de AutoProxy do WinHTTP.

## <a name="only-one-proxy-server-is-currently-supported"></a>Atualmente há suporte para apenas um servidor proxy

Atualmente, o WinHTTP não dá suporte a configurações de proxy que especificam mais de um servidor proxy. Se [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) retornar uma estrutura de [**\_ \_ informações de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contém uma lista de servidores proxy, que o aplicativo então define no identificador de solicitação usando a opção de **\_ \_ proxy de opção WinHTTP** , o WinHTTP usará apenas o primeiro servidor proxy na lista. Se esse servidor proxy não estiver acessível, o WinHTTP não fará failover para nenhum dos outros servidores proxy na lista. Cabe ao aplicativo lidar com esse caso definindo a opção de **\_ \_ proxy de opção WinHTTP** novamente com o próximo servidor proxy na lista e reenviando a solicitação.

## <a name="security-risk-mitigation"></a>Mitigação de riscos de segurança

O processamento do arquivo de configuração automática do proxy requer a execução do código de script baixado. Algumas questões de segurança a considerar: se o servidor no qual o arquivo PAC reside foi comprometido, é possível que o código do script PAC seja mal-intencionado. Portanto, o WinHTTP usa as seguintes precauções para proteger o cliente:

1.  o código do script é impedido de instanciar quaisquer ActiveX objetos. Isso bloqueia uma grande quantidade de funcionalidades potencialmente perigosas, como a capacidade de acessar arquivos e executar e/s de rede.
2.  * * Windows Server 2003: * *[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) delega todo o processamento de WPAD a um serviço externo fora do processo, o serviço de descoberta automática de Proxy da Web do WinHTTP, que é executado na conta de usuário interna do serviço Local de baixo privilégio.

3.  **Windows XP com SP2 e Windows Server 2003:** Um script de PAC não tem permissão para ser executado por mais de 60 segundos, após o qual a execução do script é encerrada.

4.  **Windows XP com SP2 e Windows Server 2003:** O WinHTTP rejeita arquivos PAC maiores que 1 MB. Normalmente, um arquivo PAC típico não tem mais do que alguns quilobytes de tamanho.

lembre-se de que o processamento do código do script PAC requer o uso de COM, porque o WinHTTP usa o componente do Microsoft JScript para executar o script. Se o WinHTTP não puder delegar o processamento do protocolo WPAD a um serviço de descoberta de proxy da Web externo, fora do processo, o [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) carregará o tempo de execução com dentro do processo do aplicativo durante a chamada. Se o aplicativo em si já estiver usando COM, isso não deve ser uma preocupação.

## <a name="performance-considerations"></a>Considerações sobre desempenho

O processo de detecção automática pode ser lento, possivelmente desde vários segundos. As funções [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [WinHttpDetectAutoProxyConfigUrl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) estão bloqueando, funções síncronas. Pode ser que um mecanismo de detecção automática específico (como DHCP) seja muito mais lento do que o outro (como DNS). Se o tipo de detecção **automática de WinHTTP for \_ \_ \_ \_ DHCP** e **WinHTTP \_ tipo de detecção automática \_ \_ \_ de DNS \_** , os sinalizadores de autoria serão especificados, o WinHTTP usará o DHCP primeiro, de acordo com a especificação WPAD. Se nenhuma URL de PAC for descoberta emitindo uma solicitação DHCP, o WinHTTP tentará localizar o arquivo PAC em um endereço DNS conhecido.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) usa o parâmetro de identificador de sessão do WinHTTP para armazenar em cache o arquivo PAC e os resultados da detecção automática. É melhor usar o mesmo identificador de sessão para várias chamadas **WinHttpGetProxyForUrl** , se possível, para evitar a detecção repetida de URL de PAC e o download de arquivos. O arquivo PAC é armazenado em cache somente na memória e é Descartado quando o aplicativo fecha o identificador de sessão.

Devido ao impacto no desempenho do AutoProxy, é recomendável que somente aplicativos cliente ou serviços de desktop usem o recurso; os aplicativos baseados em servidor devem contar com o administrador do servidor usando o utilitário "ProxyCfg.exe".

 

 



