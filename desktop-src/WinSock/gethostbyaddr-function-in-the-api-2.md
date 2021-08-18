---
description: A função gethostbyaddr usa a função WSALookupServiceBegin para consultar SVCID \_ INET \_ HOSTNAMEBYADDR como o GUID da classe de serviço.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Função gethostbyaddr na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac84d30ba919a4fc61456d5ca4772c12df786d89241e8249b57068b9aac3f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132319"
---
# <a name="gethostbyaddr-function-in-the-api"></a>Função gethostbyaddr na API

A [**função gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) usa a [**função WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ INET \_ HOSTNAMEBYADDR como o GUID da classe de serviço. O endereço do host é fornecido como uma cadeia de caracteres IPv4 decimnal pontilhada (por exemplo, "192.9.200.120") no membro *lpszServiceInstanceName* da estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passada para a **função WSALookupServiceBegin.** O32.dll Ws2 especifica LUP RETURN BLOB e o provedor de serviços de nome coloca uma estrutura HOSTENT no \_ \_ \_ blob (usando deslocamentos [](/windows/desktop/api/winsock/ns-winsock-hostent) em vez de ponteiros, conforme descrito acima). Os provedores de serviços de nomes também devem honrar esses outros \_ sinalizadores RETURN de \_ \* LUP. 

| Sinalizador              | Descrição                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ RETURN \_ NAME | Retorna o **membro \_ de nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) *em lpszServiceInstanceName*.                                                     |
| LUP \_ RETURN \_ ADDR | Retorna informações de endereçamento [**de HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas DE INFORMAÇÕES [**\_ CSADDR,**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) as informações de porta são padrão para zero. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes compatível para TCP/IP na API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolução de nomes independentes de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nomes](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
