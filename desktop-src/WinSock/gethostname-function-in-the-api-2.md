---
description: A função gethostname usa a função WSALookupServiceBegin para consultar SVCID \_ HOSTNAME como o GUID da classe de serviço.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Função gethostname na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec72c7eab46ccb9988dc166d8121304850ea49e2488901496e5c0377a395a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132269"
---
# <a name="gethostname-function-in-the-api"></a>Função gethostname na API

A [**função gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) usa a [**função WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ HOSTNAME como o GUID da classe de serviço. Se **o membro lpszServiceInstanceName** da estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passado para a **função WSALookupServiceBegin** for **NULL** ou referenciar uma cadeia de caracteres **NULL** (ou seja, . ""), o host local deve ser resolvido. Caso contrário, ocorrerá uma olhada em um nome de host especificado. Para fins de emulação **gethostname,** o Ws232.dll especifica um ponteiro NULL para o membro lpszServiceInstanceName e especifica lUP RETURN NAME para que o nome do host seja retornado no membro \_   \_ \_ **lpszServiceInstanceName.** Se um aplicativo usar essa consulta e especificar LUP RETURN ADDR, o endereço do host será fornecido em uma \_ \_ estrutura [**CSADDR \_ INFO.**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) A ação LUP \_ RETURN \_ BLOB é indefinida para essa consulta. As informações de porta são padrão como zero, a menos que o membro **lpszQueryString** da estrutura **WSAQUERYSET** passado para a função **WSALookupServiceBegin** faça referência a um serviço como FTP, caso em que o endereço de transporte completo do serviço indicado é fornecido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes compatível para TCP/IP na API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolução de nomes independentes de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nomes](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
