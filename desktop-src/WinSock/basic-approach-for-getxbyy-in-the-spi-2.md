---
description: A maioria das funções GetXbyY são convertidas por Ws2 \_32.dll em uma sequência WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd que usa um conjunto de GUIDs especiais como a classe de serviço.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Abordagem básica para GetXbyY no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827123"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Abordagem básica para GetXbyY no SPI

A maioria das funções **GetXbyY** são convertidas por Ws2 \_32.dll em uma sequência [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa um conjunto de GUIDs especiais como a classe de serviço. Essas GUIDs identificam o tipo de operação **GetXbyY** que está sendo emulada. A consulta é restrita a essas NSPs que dão suporte ao inet da AF \_ . Sempre que uma função **GetXbyY** retorna uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , o ws2 \_32.dll especificará o \_ sinalizador de retorno de blob Lup \_ em **WSALookupServiceBegin** para que as informações desejadas sejam retornadas pelo NSP. Essas estruturas devem ser ligeiramente modificadas, pois os ponteiros contidos em devem ser substituídos por deslocamentos que são relativos ao início dos dados do blob. É claro que todos os valores referenciados por esses membros de ponteiro devem estar completamente contidos no BLOB, e todas as cadeias de caracteres são ASCII.

 

 



