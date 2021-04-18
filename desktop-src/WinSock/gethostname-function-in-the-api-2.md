---
description: A função GetHostName usa a função WSALookupServiceBegin para consultar o \_ nome de host SVCID como o GUID de classe de serviço.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Função GetHostName na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787745"
---
# <a name="gethostname-function-in-the-api"></a>Função GetHostName na API

A função [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) usa a função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar o \_ nome de host SVCID como o GUID de classe de serviço. Se o membro **lpszServiceInstanceName** da estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passado para a função **WSALookupServiceBegin** for **nulo** ou fizer referência a uma cadeia de caracteres **nula** (ou seja. ""), o host local deve ser resolvido. Caso contrário, ocorrerá uma pesquisa em um nome de host especificado. Para fins de emulação de **GetHostName** , o \_32.dll Ws2 especifica um ponteiro **nulo** para o membro **lpszServiceInstanceName** e especifica Lup \_ nome de retorno \_ para que o nome do host seja retornado no membro **lpszServiceInstanceName** . Se um aplicativo usar essa consulta e especificar \_ \_ o endereço de retorno de Lup, então ele será fornecido em uma estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . A \_ ação de blob de retorno Lup \_ é indefinida para esta consulta. As informações de porta são padronizadas para zero, a menos que o membro **lpszQueryString** da estrutura **WSAQUERYSET** passada para a função **WSALOOKUPSERVICEBEGIN** referencie um serviço como FTP. nesse caso, o endereço de transporte completo do serviço indicado é fornecido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
