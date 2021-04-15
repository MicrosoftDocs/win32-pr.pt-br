---
description: A maioria das funções getXbyY são convertidas pelo \_32.dll Ws2 para uma sequência WSALookupServiceBegin, WSALookupServiceNext e WSALookupServiceEnd que usa um conjunto de GUIDs especiais como a classe de serviço.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Abordagem básica para GetXbyY na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501707"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Abordagem básica para GetXbyY na API

A maioria das funções **getXbyY** são convertidas pelo \_32.dll Ws2 para uma sequência [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa um conjunto de GUIDs especiais como a classe de serviço. Essas GUIDs identificam o tipo de operação **getXbyY** que está sendo emulada. A consulta é restrita a esses provedores de serviços de nomes que dão suporte ao inet da AF \_ . Sempre que uma função **getXbyY** retorna uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , o ws2 \_32.dll especifica o \_ sinalizador de retorno de blob Lup \_ em **WSALookupServiceBegin** para que as informações desejadas sejam retornadas pelo provedor de serviços de nome. Essas estruturas devem ser ligeiramente modificadas, pois os ponteiros contidos em devem ser substituídos por deslocamentos que são relativos ao início dos dados do blob. É claro que todos os valores referenciados por esses parâmetros de ponteiro devem estar completamente contidos no BLOB, e todas as cadeias de caracteres são ASCII.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



