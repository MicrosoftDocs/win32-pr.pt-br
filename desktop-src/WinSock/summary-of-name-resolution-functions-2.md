---
description: 'As funções de resolução de nomes podem ser agrupadas em três categorias: instalação de serviço, consultas de cliente e auxiliar (com macros).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Resumo das funções de resolução de nomes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647124"
---
# <a name="summary-of-name-resolution-functions"></a>Resumo das funções de resolução de nomes

As funções de resolução de nomes podem ser agrupadas em três categorias: instalação de serviço, consultas de cliente e auxiliar (com macros). As seções a seguir identificam as funções em cada categoria e descrevem brevemente o uso pretendido. As estruturas de dados-chave também são descritas.

## <a name="service-installation"></a>Instalação do serviço

-   [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

Quando a classe de serviço necessária ainda não existir, um aplicativo usará [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) para instalar uma nova classe de serviço fornecendo um nome de classe de serviço, um GUID para o identificador de classe de serviço e uma série de estruturas [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Essas estruturas são específicas para um namespace específico e fornecem valores comuns, como números de porta TCP recomendados ou identificadores SAP do NetWare. Uma classe de serviço pode ser removida chamando [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) e fornecendo o GUID correspondente ao identificador de classe.

Quando existe uma classe de serviço, as instâncias específicas de um serviço podem ser instaladas ou removidas por meio do [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea). Essa função usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como um parâmetro de entrada junto com um código de operação e sinalizadores de operação. O código da operação indica se o serviço está sendo instalado ou removido. A estrutura **WSAQUERYSET** fornece todas as informações relevantes sobre o serviço, incluindo o identificador de classe de serviço, o nome do serviço (para essa instância), o identificador de namespace aplicável e as informações de protocolo e um conjunto de endereços de transporte no qual o serviço escuta. Os serviços devem invocar **WSASetService** quando forem inicializados para anunciar sua presença em namespaces dinâmicos.

## <a name="client-query"></a>Consulta do cliente

-   [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

A função [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) permite que um aplicativo descubra quais namespaces são acessíveis por meio de instalações de resolução de nome do Winsock. Ele também permite que um aplicativo determine se um determinado namespace tem suporte por mais de um provedor de namespace e para descobrir o identificador do provedor para qualquer provedor de namespace específico. Usando um identificador de provedor, o aplicativo pode restringir uma operação de consulta a um provedor de namespace especificado.

Namespace do Winsock – as operações de consulta envolvem uma série de chamadas: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), seguidas por uma ou mais chamadas para [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) e terminando com uma chamada para [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). **WSALookupServiceBegin** usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como entrada para definir os parâmetros de consulta junto com um conjunto de sinalizadores para fornecer controle adicional sobre a operação de pesquisa. Ele retorna um identificador de consulta que é usado nas chamadas subsequentes para **WSALookupServiceNext** e **WSALookupServiceEnd**.

O aplicativo invoca [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) para obter os resultados da consulta, com os resultados fornecidos em um buffer [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecido pelo aplicativo. O aplicativo continua chamando **WSALookupServiceNext** até que o código de erro WSA \_ E \_ não \_ mais seja retornado, indicando que todos os resultados foram recuperados. Em seguida, a pesquisa é encerrada por uma chamada para [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). A função **WSALookupServiceEnd** também pode ser usada para cancelar um **WSALookupServiceNext** pendente no momento quando chamado de outro thread.

No Windows Sockets 2, códigos de erro conflitantes são definidos para WSAENOMORE (10102) e WSA \_ e \_ não \_ mais (10110). O código de erro WSAENOMORE será removido em uma versão futura e somente o WSA \_ e \_ não \_ será mais mantido. No entanto, para o Windows Sockets 2, os aplicativos devem verificar WSAENOMORE e WSA e \_ \_ não \_ mais a maior compatibilidade possível com provedores de namespace que usam um deles.

## <a name="helper-functions"></a>Funções auxiliares

-   [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [**WSAGetServiceClassInfo**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

As funções auxiliares de resolução de nomes incluem uma função para recuperar um nome de classe de serviço dado um identificador de classe de serviço, um par de funções usadas para converter um endereço de transporte entre uma estrutura [**SOCKADDR**](sockaddr-2.md) e uma representação de cadeia de caracteres ASCII, uma função para recuperar as informações de esquema de classe de serviço para uma determinada classe de serviço e um conjunto de macros para mapear serviços bem

As seguintes macros do Winsock2. h auxiliam no mapeamento entre classes de serviço bem conhecidas e esses namespaces:

| Macro                                                                                                            | Descrição                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| SVCID \_ TCP (porta) SVCID \_ UDP (porta)<br/> SVCID \_ NetWare (tipo de objeto)<br/>                              | Dada uma porta para TCP/IP ou UDP/IP ou o tipo de objeto no caso do NetWare, retorna o GUID (número da porta na ordem do host). |
| IS \_ SVCID \_ TCP (GUID) é \_ SVCID \_ UDP (GUID)<br/> é \_ SVCID \_ NetWare (GUID)<br/>                          | Retornará **true** se o GUID estiver dentro do intervalo permitido.                                                                |
| SET \_ TCP \_ SVCID (GUID, porta) Set \_ UDP \_ SVCID (GUID, porta)<br/>                                                | Inicializa uma estrutura de GUID com o equivalente de GUID para um número de porta TCP ou UDP (o número da porta deve estar na ordem do host).    |
| PORTA \_ da \_ \_ porta TCP (GUID) SVCID \_ do \_ SVCID \_ UDP (GUID)<br/> SAPId \_ da \_ SVCID \_ NetWare (GUID)<br/> | Retorna a porta ou o tipo de objeto associado ao GUID (número da porta na ordem do host).                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[Estruturas de dados de resolução de nomes](name-resolution-data-structures-2.md)
</dt> <dt>

[Modelo de resolução de nomes](name-resolution-model-2.md)
</dt> <dt>

[Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




