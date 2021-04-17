---
description: Para facilitar a configuração das configurações de proxy, o WinHTTP 5,1 implementa o protocolo WPAD (descoberta automática de proxy da Web), também conhecido como AutoProxy.
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: Suporte ao WinHTTP AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26584bd0b1809f3866ed42adc7198275f40f991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782725"
---
# <a name="winhttp-autoproxy-support"></a>Suporte ao WinHTTP AutoProxy

Para facilitar a configuração das configurações de proxy, o WinHTTP 5,1 implementa o protocolo WPAD (descoberta automática de proxy da Web), também conhecido como AutoProxy.

## <a name="overview-of-autoproxy"></a>Visão geral do AutoProxy

Aplicativos e componentes que usam o WinHTTP para enviar solicitações HTTP devem garantir que a configuração de proxy esteja definida corretamente. A menos que o cliente tenha uma conexão direta com a Internet, uma solicitação HTTP normalmente deve ser enviada por um servidor proxy da Web que conecta a rede local do cliente à Internet (por exemplo, esse é geralmente o caso para clientes Web em uma LAN corporativa). Para aplicativos baseados em servidor, a configuração de proxy é normalmente gerenciada pelo administrador do servidor usando o utilitário ProxyCfg.exe do WinHTTP. O administrador do servidor sabe o nome do servidor proxy antecipadamente e usa ProxyCfg.exe para registrar essa configuração no registro em que o WinHTTP pode procurar. No entanto, exigir que os usuários finais da área de trabalho cliente configurem manualmente as configurações de proxy do WinHTTP é problemática. O usuário final pode não saber o nome do servidor proxy; exigir que o usuário final execute o utilitário de ProxyCfg.exe pode ser uma carga de suporte para uma organização. Para dar suporte a uma boa experiência de usuário, um aplicativo cliente habilitado para Web deve determinar a configuração de proxy sem intervenção do usuário.

Para facilitar a configuração das configurações de proxy para aplicativos baseados em WinHTTP, o WinHTTP agora implementa o [protocolo WPAD (descoberta automática de proxy da Web)](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01), geralmente chamado de *proxy* automático. Esse é o mesmo protocolo que os navegadores da Web implementam para descobrir automaticamente a configuração de proxy sem exigir que um usuário final especifique um servidor proxy manualmente. Esse recurso está disponível a partir do WinHTTP versão 5,1 no Windows 2000 Service Pack 3, Windows XP Service Pack 1 e Windows Server 2003. Observe que embora o Microsoft Internet Explorer e o Microsoft WinHTTP ofereçam suporte ao WPAD, a especificação nunca progrediu além do estágio "Internet-Draft" e expirou em maio de 2001.

O protocolo WPAD funciona da seguinte maneira:

1.  Usando os protocolos de rede DHCP e/ou DNS, a URL de um arquivo PAC (configuração automática de proxy) é descoberta. A URL identifica um arquivo PAC na rede local do cliente. O WinHTTP dá suporte apenas a URLs de PAC "http:" e "https:"; Ele não, por exemplo, dá suporte a URLS "file:".
2.  O arquivo PAC é baixado e, opcionalmente, armazenado em cache no computador do cliente. O arquivo PAC é um script executável que gera uma lista de um ou mais servidores proxy, dado um nome de host e uma URL de destino. O WinHTTP dá suporte apenas a arquivos PAC baseados em ECMAScript.
3.  Em cada solicitação HTTP, o código do script PAC é executado, com o nome do host e a URL da solicitação HTTP passada como parâmetros. O WinHTTP espera que o código do script PAC contenha uma função chamada **FindProxyForURL**, no formato:
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Essa função computa uma lista de um ou mais servidores proxy que podem ser usados pelo cliente HTTP para transmitir a solicitação. Se o script de PAC determinar que o cliente HTTP pode acessar o servidor de destino diretamente sem passar por um servidor proxy, ele indicará isso usando um valor de retorno especial.

## <a name="autoproxy-topics"></a>Tópicos de AutoProxy

-   [Funções de AutoProxy do WinHTTP](winhttp-autoproxy-api.md)
-   [Descoberta sem um arquivo de configuração automática](discovery-without-an-auto-config-file.md)
-   [Problemas de AutoProxy no WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Definindo as configurações de proxy do WinInet no WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [Cache de AutoProxy](autoproxy-cache.md)
-   [Formato de arquivo de configuração automática de extensões IPv6 para navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



