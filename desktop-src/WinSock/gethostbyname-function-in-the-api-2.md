---
description: Função gethostbyname na API do Winsock.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Função gethostbyname na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090392"
---
# <a name="gethostbyname-function-in-the-api"></a>Função gethostbyname na API

A função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) usa a função [**WSALOOKUPSERVICEBEGIN**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ HOSTADDRBYNAME como o GUID de classe de serviço. O nome do host é fornecido no membro **lpszServiceInstanceName** na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passada para a função **WSALookupServiceBegin** . O \_32.dll Ws2 especifica Lup \_ blob de retorno \_ e o provedor de serviço de nome coloca uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima). Provedores de serviço de nome também devem respeitar esses outros \_ \_ \* sinalizadores de retorno de Lup.

| Sinalizador              | Descrição                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nome de retorno \_ | Retorna o membro do **\_ nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em *lpszServiceInstanceName*.                                                                                                                                           |
| \_endereço de retorno de Lup \_ | Retorna informações de endereçamento de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , as informações de porta são padronizadas como zero. Observe que essa rotina não resolve nomes de host que consistem em um endereço IPv4 pontilhado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
