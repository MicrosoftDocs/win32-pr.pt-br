---
description: Para facilitar a configuração de configurações de proxy, o WinHTTP 5.1 implementa o protocolo WPAD (Descoberta Automática de Proxy Web), também conhecido como autoproxy.
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: Suporte ao WinHTTP AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f6a07645fd7d8bcd401bf399d2a9f525499c4d3a725e49b9d170c067092f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614076"
---
# <a name="winhttp-autoproxy-support"></a>Suporte ao WinHTTP AutoProxy

Para facilitar a configuração de configurações de proxy, o WinHTTP 5.1 implementa o protocolo WPAD (Descoberta Automática de Proxy Web), também conhecido como autoproxy.

## <a name="overview-of-autoproxy"></a>Visão geral do AutoProxy

Aplicativos e componentes que usam WinHTTP para enviar solicitações HTTP devem garantir que a configuração de proxy seja definida corretamente. A menos que o cliente tenha uma conexão direta com a Internet, uma solicitação HTTP normalmente deve ser enviada por meio de um servidor proxy Web que conecta a rede local do cliente à Internet (por exemplo, esse geralmente é o caso para clientes Web em uma LAN corporativa). Para aplicativos baseados em servidor, a configuração de proxy normalmente é gerenciada pelo administrador do servidor usando o utilitário ProxyCfg.exe WinHTTP. O administrador do servidor sabe o nome do servidor proxy com antecedência e usa ProxyCfg.exe para registrar essa configuração no Registro em que o WinHTTP pode procurar. No entanto, exigir que os usuários finais da área de trabalho cliente configurem manualmente as configurações de proxy WinHTTP é problemático. O usuário final pode não saber o nome do servidor proxy; exigir que o usuário final execute o utilitário ProxyCfg.exe pode ser uma carga de suporte para uma organização. Para dar suporte a uma boa experiência do usuário, um aplicativo cliente habilitado para a Web deve determinar a configuração de proxy sem intervenção do usuário.

Para facilitar a definição das configurações de proxy para aplicativos baseados em WinHTTP, o WinHTTP agora implementa o protocolo [WPAD (Descoberta](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01)Automática de Proxy Web), geralmente chamado de reprodução *automática.* Esse é o mesmo protocolo que os navegadores da Web implementam para descobrir automaticamente a configuração de proxy sem exigir que um usuário final especifique um servidor proxy manualmente. Esse recurso está disponível a partir do WinHTTP versão 5.1 no Windows 2000 Service Pack 3, Windows XP Service Pack 1 e Windows Server 2003. Observe que, embora o Microsoft Internet Explorer e o Microsoft WinHTTP deem suporte ao WPAD, a especificação nunca progrediu além do estágio "Rascunho da Internet" e expirou em maio de 2001.

O protocolo WPAD funciona da seguinte forma:

1.  Usando os protocolos de rede DHCP e/ou DNS, a URL de um arquivo PAC (Configuração Automática de Proxy) é descoberta. A URL identifica um arquivo PAC na rede local do cliente. O WinHTTP dá suporte apenas a URLs pac "http:" e "https:"; ele não dá suporte, por exemplo, a URLs "file:".
2.  O arquivo PAC é baixado e, opcionalmente, armazenado em cache no computador do cliente. O arquivo PAC é um script executável que gera uma lista de um ou mais servidores proxy, considerando um nome de host de destino e uma URL. O WinHTTP dá suporte apenas a arquivos PAC baseados em ECMAScript.
3.  Em cada solicitação HTTP, o código de script PAC é executado, com o nome do host e a URL da solicitação HTTP passados como parâmetros. WinHTTP espera que o código de script PAC contenha uma função chamada **FindProxyForURL,** no formato:
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Essa função calcula uma lista de um ou mais servidores proxy que podem ser usados pelo cliente HTTP para transmitir a solicitação. Se o script PAC determinar que o cliente HTTP pode acessar o servidor de destino diretamente sem passar por um servidor proxy, ele indicará isso usando um valor de retorno especial.

## <a name="autoproxy-topics"></a>Tópicos do AutoProxy

-   [Funções WinHTTP AutoProxy](winhttp-autoproxy-api.md)
-   [Descoberta sem um arquivo de configuração automática](discovery-without-an-auto-config-file.md)
-   [Problemas de AutoProxy no WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Definindo configurações de proxy do WinInet no WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [AutoProxy Cache](autoproxy-cache.md)
-   [Extensões IPv6 para o formato de arquivo de configuração automática do navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



