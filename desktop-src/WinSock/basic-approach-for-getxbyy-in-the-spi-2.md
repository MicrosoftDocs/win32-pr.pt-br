---
description: A maioria das funções GetXbyY são convertidas por Ws2 \_32.dll em uma sequência WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd que usa um conjunto de GUIDs especiais como a classe de serviço.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Abordagem básica para GetXbyY no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba707747dd6082bfa6c8b3c4dd3c19e8d6ce968359745947227ee464d97f984f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560520"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Abordagem básica para GetXbyY no SPI

A maioria das funções **GetXbyY** são convertidas por Ws2 \_32.dll em uma sequência [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa um conjunto de GUIDs especiais como a classe de serviço. Essas GUIDs identificam o tipo de operação **GetXbyY** que está sendo emulada. A consulta é restrita a essas NSPs que dão suporte ao inet da AF \_ . Sempre que uma função **GetXbyY** retorna uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , o ws2 \_32.dll especificará o \_ sinalizador de retorno de blob Lup \_ em **WSALookupServiceBegin** para que as informações desejadas sejam retornadas pelo NSP. Essas estruturas devem ser ligeiramente modificadas, pois os ponteiros contidos em devem ser substituídos por deslocamentos que são relativos ao início dos dados do blob. É claro que todos os valores referenciados por esses membros de ponteiro devem estar completamente contidos no BLOB, e todas as cadeias de caracteres são ASCII.

 

 



