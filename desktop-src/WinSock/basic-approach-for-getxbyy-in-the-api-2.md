---
description: A maioria das funções getXbyY é convertida pelo Ws232.dll para uma sequência \_ WSALookupServiceBegin, WSALookupServiceNext e WSALookupServiceEnd que usa um de um conjunto de GUIDs especiais como a classe de serviço.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Abordagem básica para GetXbyY na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e6dd0e5569bd11de813e28eaec1ee04f6b5f206277f695cdb9aaab05ec4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322620"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Abordagem básica para GetXbyY na API

A maioria das funções **getXbyY** é convertida pelo Ws232.dll para uma sequência \_ [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa um de um conjunto de GUIDs especiais como a classe de serviço. Esses GUIDs identificam o tipo de **operação getXbyY** que está sendo emulada. A consulta é restrita a esses provedores de serviços de nome que suportam a \_ INET do AF. Sempre que uma função **getXbyY** retorna uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**SERVENT,**](/windows/desktop/api/winsock/ns-winsock-servent) o Ws232.dll especifica o sinalizador \_ LUP RETURN BLOB em \_ \_ **WSALookupServiceBegin** para que as informações desejadas sejam retornadas pelo provedor de serviços de nome. Essas estruturas devem ser ligeiramente modificadas, já que os ponteiros contidos em devem ser substituídos por deslocamentos relativos ao início dos dados do blob. Todos os valores referenciados por esses parâmetros de ponteiro devem, obviamente, estar completamente contidos no blob e todas as cadeias de caracteres são ASCII.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes compatível para TCP/IP na API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolução de nomes independentes de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nomes](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



