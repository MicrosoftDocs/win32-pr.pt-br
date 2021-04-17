---
description: O PNRP usa a estrutura WSAQUERYSET em conjunto com várias funções para facilitar a resolução de nomes e a enumeração de nomes e nuvens.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP e WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770362"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP e WSAQUERYSET

O PNRP usa a estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) em conjunto com várias funções para facilitar a resolução de nomes e a enumeração de nomes e nuvens.

Para obter definições completas de funções do [**WSAQUERYSET**](winsock-nsp-reference-links.md) ou do Windows Sockets, consulte suas respectivas definições na documentação da API do Windows Sockets 2 no SDK da plataforma.

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET e WSASetService

A função [**WSASetService**](winsock-nsp-reference-links.md) usa a estrutura **WSAQUERYSET** para registrar ou remover nomes de par. A página [PNRP e WSASetService](pnrp-and-wsasetservice.md) descreve como usar a estrutura **WSAQUERYSET** com essa função.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET e WSALookupServiceBegin

A estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) é usada extensivamente com as funções **WSALookupServiceBegin**, **WSALookupServiceNext** e **WSALookupServiceEnd** . Detalhes sobre como essas funções usam a estrutura **WSAQUERYSET** são detalhados nas seguintes páginas de referência:

-   [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                             |
| Versão<br/>                  | Windows XP com SP1 com o Advanced Networking Pack para Windows XP<br/>  |
| parâmetro<br/>                   | <dl> <dt>P2P. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




