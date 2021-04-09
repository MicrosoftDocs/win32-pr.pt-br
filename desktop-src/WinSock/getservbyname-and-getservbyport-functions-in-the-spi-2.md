---
description: A consulta WSALookupServiceBegin usa SVCID \_ inet \_ SERVICEBYNAME como o GUID de classe de serviço.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: Funções getservbyname e getservbyport no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd910dc7ab478c262bd5ca6c480dc3ec58e1b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090390"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>Funções getservbyname e getservbyport no SPI

A consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ SERVICEBYNAME como o GUID de classe de serviço. O parâmetro *lpszServiceInstanceName* faz referência a uma cadeia de caracteres que indica o nome do serviço ou a porta de serviço e (opcionalmente) o protocolo de serviço. A formatação da cadeia de caracteres é ilustrada como FTP/TCP ou 21/TCP ou apenas FTP. A cadeia de caracteres não diferencia maiúsculas de minúsculas. A barra, se presente, separa o identificador de protocolo da parte anterior da cadeia de caracteres. O \_32.dll Ws2 especificará Lup \_ blob de retorno \_ e o NSP coloca uma estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima). NSPs também deve respeitar esses outros \_ \_ \* sinalizadores de retorno de Lup.



| Sinalizador              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nome de retorno \_ | Retorna o membro do **\_ nome de s** da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) em *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_tipo de retorno Lup \_ | Retorna o GUID canônico em *lpServiceClassId* é entendido que um serviço identificado como FTP ou 21 pode estar em outra porta de acordo com as convenções estabelecidas localmente. O membro da **\_ porta s** da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicar onde o serviço pode ser contatado no ambiente local. O GUID canônico retornado quando o \_ tipo de retorno Lup \_ está definido deve ser um dos GUIDs predefinidos de SVCS. h que corresponde ao número da porta indicado na estrutura **SERVENT** . |



 

 

 



