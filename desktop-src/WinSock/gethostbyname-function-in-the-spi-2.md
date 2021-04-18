---
description: Função gethostbyname no SPI do Winsock.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Função gethostbyname no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793904"
---
# <a name="gethostbyname-function-in-the-spi"></a>Função gethostbyname no SPI

A consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ HOSTADDRBYNAME como o GUID de classe de serviço. O nome do host é fornecido em *lpszServiceInstanceName*. O *\_32.dllWs2* especifica Lup \_ blob de retorno \_ e o NSP coloca uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima). NSPs também deve respeitar esses outros \_ \_ \* sinalizadores de retorno de Lup.



| Sinalizador              | Descrição                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nome de retorno \_ | Retorna o membro do **\_ nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em *lpszServiceInstanceName*.                                                                                                                                                            |
| \_endereço de retorno de Lup \_ | Retorna informações de endereçamento de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , as informações de porta são padronizadas como zero. Observe que essa rotina não resolve nomes de host que consistem em uma cadeia de caracteres de endereço IPv4 de decimal pontilhado. |



 

 

 
