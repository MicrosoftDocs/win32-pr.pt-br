---
description: A estrutura WSAQUERYSET é usada para formar consultas para a função NSPLookupServiceBegin e usada para fornecer resultados de consulta para a função NSPLookupServiceNext.
ms.assetid: 017b5828-bc6e-42b7-aba7-21648b2dd707
title: Query-Related estruturas de dados na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcbd83ab427a6ec3f09c67f416fe5eb8d7ebaad165bf4e687dfd31dce882cda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569357"
---
# <a name="query-related-data-structures-in-the-spi"></a>Query-Related estruturas de dados na SPI

A [**estrutura WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) é usada para formar consultas para [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)e usada para fornecer resultados de consulta para [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext). É uma estrutura complexa porque contém ponteiros para várias outras estruturas, algumas das quais ainda referenciam outras estruturas. A relação entre **WSAQUERYSET** e as estruturas que ele referencia é ilustrada da seguinte forma:

![estruturas wsaqueryset](images/ovrvw3-2.png)

Dentro da [**estrutura WSAQUERYSET,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) a maioria dos membros é autoexplicativa, mas algumas explicações adicionais são óbvias. O **dwSize** será preenchido com sizeof( **WSAQUERYSET**) e pode ser usado por provedores de namespace para detectar e adaptar-se a diferentes versões da estrutura **WSAQUERYSET** que podem aparecer.

O **membro dwOutputFlags** é usado por um provedor de namespace para fornecer dados adicionais sobre os resultados da consulta. Para obter mais informações, [**consulte NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext).

A [**estrutura WSAECOMPARATOR referenciada**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) por **lpversion** é usada para a restrição de consulta e os resultados. Para consultas, o **membro dwVersion** indica a versão desejada do serviço. O **membro ecHow** é um tipo enumerado que especifica como a comparação será feita. As opções são COMP EQUALS, que exige que ocorra uma combinação exata na versão ou COMP NOTLESS, que especifica que o número de versão do serviço não seja menor que o valor \_ \_ de **dwVersion.**

A interpretação de **dwNameSpace** e **lpNSProviderId** depende de como a estrutura está sendo usada e é descrita mais detalhadamente nas descrições de função individuais que utilizam essa estrutura.

O **membro lpszContext** aplica-se a namespaces hierárquicos e especifica o ponto de partida de uma consulta ou o local dentro da hierarquia em que o serviço reside. As regras gerais são:

-   Um valor **null**, em branco ("") iniciará a pesquisa no contexto padrão.
-   Um valor de " \\ " inicia a pesquisa na parte superior do namespace.
-   Qualquer outro valor inicia a pesquisa no ponto designado.

Provedores que não suportam contenção poderão retornar um erro se algo diferente de "" ou \\ " " for especificado. Provedores que suportam contenção limitada, como grupos, devem aceitar "", \\ " ou um ponto designado. Os contextos são específicos do namespace. Se **dwNameSpace** for NS ALL, somente "" ou " deverá ser passado como o contexto porque eles são reconhecidos por todos \_ os \\ namespaces.

O **membro lpszQueryString** é usado para fornecer informações de consulta adicionais específicas do namespace, como uma cadeia de caracteres que descreve um nome de protocolo de transporte e serviço conhecido, como em "ftp/tcp".

A [**estrutura AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) referenciada por **lpafpProtocols** é usada apenas para fins de consulta e fornece uma lista de protocolos para restringir a consulta. Esses protocolos são representados como pares (família de endereços, protocolo), porque os valores de protocolo só têm significado dentro do contexto de uma família de endereços.

A matriz de [**estrutura \_ INFO CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) referenciada por **lpcsaBuffer** contém todas as informações necessárias para um serviço usar no estabelecimento de uma escuta ou um cliente a ser usado para estabelecer uma conexão com o serviço. Os **membros LocalAddr** **e RemoteAddr** contêm diretamente uma [**estrutura SOCKET \_ ADDRESS.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) Um serviço criaria um soquete usando a tupla (LocalAddr.lpSockaddr->sa \_ family, iSocketType, iProtocol). Ele vincularia o soquete a um endereço local usando LocalAddr.lpSockaddr e LocalAddr.lpSockaddrLength. O cliente cria seu soquete com a tupla (RemoteAddr.lpSockaddr->sa \_ family, iSocketType, iProtocol) e usa a combinação de RemoteAddr.lpSockaddr e RemoteAddr.lpSockaddrLength ao fazer uma conexão remota.

 

 
