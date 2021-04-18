---
description: As funções getservbyname e getservbyport usam a função WSALookupServiceBegin para consultar SVCID \_ inet \_ SERVICEBYNAME como o GUID de classe de serviço.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funções getservbyname e getservbyport na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771432"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>Funções getservbyname e getservbyport na API

As funções [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usam a função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ SERVICEBYNAME como o GUID de classe de serviço. O membro *lpszServiceInstanceName* na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passado para a função **WSALookupServiceBegin** faz referência a uma cadeia de caracteres para indicar o nome do serviço ou a porta de serviço e (opcionalmente) o protocolo de serviço. A formatação da cadeia de caracteres é ilustrada como FTP ou TCP ou 21/TCP ou apenas FTP. A cadeia de caracteres não diferencia maiúsculas de minúsculas. A barra, se presente, separa o identificador de protocolo da parte anterior da cadeia de caracteres. O \_32.dll Ws2 especificará Lup \_ blob de retorno \_ e o provedor de namespace irá posicionar uma estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima). Provedores de namespace também devem respeitar esses \_ outros \_ \* sinalizadores de retorno de Lup.

| Sinalizador              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nome de retorno \_ | Retorna o membro do **\_ nome de s** da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) em *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_tipo de retorno Lup \_ | Retorna o GUID canônico em *lpServiceClassId* é entendido que um serviço identificado como FTP ou 21 pode estar em outra porta de acordo com as convenções estabelecidas localmente. O parâmetro da **\_ porta s** da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicar onde o serviço pode ser contatado no ambiente local. O GUID canônico retornado quando o \_ tipo de retorno Lup \_ está definido deve ser um dos GUIDs predefinidos de SVCS. h que corresponde ao número da porta indicado na estrutura **SERVENT** . |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



