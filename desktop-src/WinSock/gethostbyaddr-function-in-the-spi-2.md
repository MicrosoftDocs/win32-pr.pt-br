---
description: A consulta WSALookupServiceBegin usa SVCID \_ INET \_ HOSTNAMEBYADDR como o GUID da classe de serviço.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Função gethostbyaddr na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e343bcd66b7b1482f14a07239ae73710fd789486633219952696406dd8f1bd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132309"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Função gethostbyaddr na SPI

A [**consulta WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ INET \_ HOSTNAMEBYADDR como o GUID da classe de serviço. O endereço do host é fornecido em *lpszServiceInstanceName* como uma cadeia de caracteres de endereço IPv4 decimal pontilhada (por exemplo, 192.9.200.120). O *Ws2 \_32.dll* especifica LUP RETURN BLOB e o NSP coloca uma estrutura HOSTENT no \_ \_ blob (usando deslocamentos [](/windows/desktop/api/winsock/ns-winsock-hostent) em vez de ponteiros, conforme descrito acima). Os NSPs também devem honrar esses outros \_ sinalizadores RETURN \_ \* LUP.



| Sinalizador              | Descrição                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ RETURN \_ NAME | Retorna o **membro \_ de nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) *em lpszServiceInstanceName*.                                                     |
| LUP \_ RETURN \_ ADDR | Retorna informações de endereçamento [**de HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas DE INFORMAÇÕES [**\_ CSADDR,**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) as informações de porta são padrão para zero. |



 

 

 
