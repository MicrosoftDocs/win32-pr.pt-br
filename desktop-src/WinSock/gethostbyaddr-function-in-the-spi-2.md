---
description: A consulta WSALookupServiceBegin usa SVCID \_ inet \_ HOSTNAMEBYADDR como o GUID de classe de serviço.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Função GetHostbyaddr no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501695"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Função GetHostbyaddr no SPI

A consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ HOSTNAMEBYADDR como o GUID de classe de serviço. O endereço do host é fornecido em *lpszServiceInstanceName* como uma cadeia de caracteres de endereço IPv4 com pontos decimais (por exemplo, 192.9.200.120). O *\_32.dllWs2* especifica Lup \_ blob de retorno \_ e o NSP coloca uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima). NSPs também deve respeitar esses outros \_ \_ \* sinalizadores de retorno de Lup.



| Sinalizador              | Descrição                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nome de retorno \_ | Retorna o membro do **\_ nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em *lpszServiceInstanceName*.                                                     |
| \_endereço de retorno de Lup \_ | Retorna informações de endereçamento de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , as informações de porta são padronizadas como zero. |



 

 

 
