---
description: A estrutura WSAQUERYSET é usada para formar consultas para a função NSPLookupServiceBegin e usada para fornecer resultados de consulta para a função NSPLookupServiceNext.
ms.assetid: 017b5828-bc6e-42b7-aba7-21648b2dd707
title: Query-Related estruturas de dados no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ce5a7016bd2ad96f464137177036b470c64a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559705"
---
# <a name="query-related-data-structures-in-the-spi"></a>Query-Related estruturas de dados no SPI

A estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) é usada para formar consultas para [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)e é usada para fornecer resultados de consulta para [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext). É uma estrutura complexa porque contém ponteiros para várias outras estruturas, algumas das quais a referência ainda tem outras estruturas. A relação entre **WSAQUERYSET** e as estruturas referenciadas é ilustrada da seguinte maneira:

![estruturas WSAQUERYSET](images/ovrvw3-2.png)

Na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , a maioria dos membros é auto-explicativa, mas alguns merecem uma explicação adicional. O **dwSize** será preenchido com sizeof ( **WSAQUERYSET**) e pode ser usado por provedores de namespace para detectar e se adaptar a versões diferentes da estrutura **WSAQUERYSET** que podem aparecer.

O membro **dwOutputFlags** é usado por um provedor de namespace para fornecer dados adicionais sobre os resultados da consulta. Para obter mais informações, consulte [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext).

A estrutura [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) referenciada por **lpversion** é usada para a restrição de consulta e os resultados. Para consultas, o membro **DW** indica a versão desejada do serviço. O membro **ecHow** é um tipo enumerado que especifica como a comparação será feita. As opções são COMP \_ Equals, que requer que uma correspondência exata na versão ocorra, ou comp less, que \_ especifica que o número de versão do serviço não é menor que o valor de **DW**.

A interpretação de **dwNameSpace** e **lpNSProviderId** depende de como a estrutura está sendo usada e é descrita mais detalhadamente nas descrições de função individuais que utilizam essa estrutura.

O membro **lpszContext** se aplica a namespaces hierárquicos e especifica o ponto de partida de uma consulta ou o local dentro da hierarquia em que o serviço reside. As regras gerais são:

-   Um valor **nulo**, em branco (""), iniciará a pesquisa no contexto padrão.
-   Um valor de " \\ " inicia a pesquisa na parte superior do namespace.
-   Qualquer outro valor inicia a pesquisa no ponto designado.

Os provedores que não dão suporte à contenção poderão retornar um erro se algo diferente de "" ou " \\ " for especificado. Provedores que dão suporte a contenção limitada, como grupos, devem aceitar "", " \\ " ou um ponto designado. Contextos são específicos do namespace. Se **dwNameSpace** for NS \_ All, somente "" ou " \\ " deverá ser passado como o contexto porque eles são reconhecidos por todos os namespaces.

O membro **lpszQueryString** é usado para fornecer informações de consulta adicionais específicas de namespace, como uma cadeia de caracteres que descreve um serviço conhecido e um nome de protocolo de transporte, como em "FTP/TCP".

A estrutura [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) referenciada por **lpafpProtocols** é usada apenas para fins de consulta e fornece uma lista de protocolos para restringir a consulta. Esses protocolos são representados como pares (família de endereços, protocolo), pois os valores de protocolo só têm significado no contexto de uma família de endereços.

A matriz da estrutura de [**\_ informações do CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) referenciada por **lpcsaBuffer** contém todas as informações necessárias para que um serviço seja usado no estabelecimento de uma escuta ou um cliente para usar no estabelecimento de uma conexão com o serviço. Os membros **localaddr** e **RemoteAddr** contêm diretamente uma estrutura [**de \_ endereço de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) . Um serviço criaria um soquete usando a tupla (LocalAddr. lpSockaddr->\_ família SA, iSocketType, iProtocol). Ele ligaria o soquete a um endereço local usando LocalAddr. lpSockaddr e LocalAddr. lpSockaddrLength. O cliente cria seu soquete com a tupla (RemoteAddr. lpSockaddr->\_ família SA, iSocketType, iProtocol) e usa a combinação de RemoteAddr. lpSockAddr e RemoteAddr. lpSockaddrLength ao fazer uma conexão remota.

 

 
