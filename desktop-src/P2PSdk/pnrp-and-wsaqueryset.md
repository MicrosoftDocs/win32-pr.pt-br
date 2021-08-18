---
description: O PNRP usa a estrutura WSAQUERYSET em conjunto com várias funções para facilitar a resolução de nomes e a enumeração de nomes e nuvens.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP e WSAQUERYSET (P2P.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbc635b0c1ca19cfaeeeb7f8b013aefad1e49e2141dd9715a36c0238e7be6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061348"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP e WSAQUERYSET

O PNRP usa a [**estrutura WSAQUERYSET**](winsock-nsp-reference-links.md) em conjunto com várias funções para facilitar a resolução de nomes e enumeração de nomes e nuvens.

Para definições completas das funções [**WSAQUERYSET**](winsock-nsp-reference-links.md) ou Windows Sockets, consulte suas respectivas definições na documentação da API Windows Sockets 2 no SDK da Plataforma.

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET e WSASetService

A [**função WSASetService**](winsock-nsp-reference-links.md) usa a estrutura **WSAQUERYSET** para registrar ou remover nomes de pares. A [página PNRP e WSASetService](pnrp-and-wsasetservice.md) descreve como usar a estrutura **WSAQUERYSET** com essa função.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET e WSALookupServiceBegin

A estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) é amplamente usada com as funções **WSALookupServiceBegin**, **WSALookupServiceNext** e **WSALookupServiceEnd.** Detalhes sobre como essas funções usam a **estrutura WSAQUERYSET** são detalhados nas seguintes páginas de referência:

-   [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                             |
| Versão<br/>                  | Windows XP com SP1 com o Pacote de Rede Avançado para Windows XP<br/>  |
| Cabeçalho<br/>                   | <dl> <dt>P2P.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




