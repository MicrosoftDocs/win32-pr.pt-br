---
description: A consulta WSALookupServiceBegin usa SVCID \_ INET \_ SERVICEBYNAME como o GUID da classe de serviço.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: Funções getservbyname e getservbyport na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466966db2fc605b4043355746a1e606626e3d5d518452d1fab661dcfb68b3238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132159"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>Funções getservbyname e getservbyport na SPI

A [**consulta WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ INET \_ SERVICEBYNAME como o GUID da classe de serviço. O *parâmetro lpszServiceInstanceName* faz referência a uma cadeia de caracteres que indica o nome do serviço ou a porta de serviço e (opcionalmente) o protocolo de serviço. A formatação da cadeia de caracteres é ilustrada como ftp/tcp ou 21/tcp ou apenas ftp. A cadeia de caracteres não é sensível a minúsculas. A marca de barra, se presente, separa o identificador de protocolo da parte anterior da cadeia de caracteres. O Ws232.dll especificará LUP RETURN BLOB e o NSP colocará uma estrutura SERVENT no \_ \_ \_ blob (usando deslocamentos [](/windows/desktop/api/winsock/ns-winsock-servent) em vez de ponteiros, conforme descrito acima). Os NSPs também devem honrar esses outros \_ sinalizadores RETURN \_ \* LUP.



| Sinalizador              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ RETURN \_ NAME | Retorna o **membro \_ de nome** da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) *em lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                            |
| TIPO DE \_ RETORNO \_ LUP | Retorna GUID canônico em *lpServiceClassId* É entendido que um serviço identificado como ftp ou 21 pode estar em outra porta de acordo com as convenções estabelecidas localmente. O **membro \_ da porta** s da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicar onde o serviço pode ser contatado no ambiente local. O GUID canônico retornado quando LUP RETURN TYPE é definido deve ser um dos \_ \_ GUIDs predefinidos de svcs.h que corresponde ao número da porta indicado na estrutura **SERVENT.** |



 

 

 



