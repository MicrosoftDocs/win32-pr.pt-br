---
description: As funções getservbyname e getservbyport usam a função WSALookupServiceBegin para consultar SVCID \_ INET SERVICEBYNAME como o GUID da classe \_ de serviço.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funções getservbyname e getservbyport na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e5d7cc9b1811eef98cc6d337abc3230ea46bd537a19969a4b412473e671b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132209"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>Funções getservbyname e getservbyport na API

As [**funções getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usam a função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ INET SERVICEBYNAME como o GUID da classe \_ de serviço. O membro *lpszServiceInstanceName* na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passado para a função **WSALookupServiceBegin** faz referência a uma cadeia de caracteres para indicar o nome do serviço ou a porta de serviço e (opcionalmente) o protocolo de serviço. A formatação da cadeia de caracteres é ilustrada como FTP ou TCP ou 21/TCP ou apenas FTP. A cadeia de caracteres não é sensível a minúsculas. A marca de barra, se presente, separa o identificador de protocolo da parte anterior da cadeia de caracteres. O Ws232.dll especificará LUP RETURN BLOB e o provedor de namespace colocará uma estrutura SERVENT no \_ \_ \_ blob (usando deslocamentos [](/windows/desktop/api/winsock/ns-winsock-servent) em vez de ponteiros, conforme descrito acima). Os provedores de namespace também devem honrar esses outros sinalizadores \_ RETURN de LUP. \_ \*

| Sinalizador              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ RETURN \_ NAME | Retorna o **membro \_ de nome** da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) *em lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                               |
| TIPO DE \_ RETORNO \_ LUP | Retorna GUID canônico em *lpServiceClassId* É entendido que um serviço identificado como FTP ou 21 pode estar em outra porta de acordo com as convenções estabelecidas localmente. O **parâmetro \_ de** porta s da [**estrutura SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicar onde o serviço pode ser contatado no ambiente local. O GUID canônico retornado quando LUP RETURN TYPE é definido deve ser um dos \_ \_ GUIDs predefinidos de Svcs.h que corresponde ao número da porta indicado na estrutura **SERVENT.** |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes compatível para TCP/IP na API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolução de nomes independentes de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nomes](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



