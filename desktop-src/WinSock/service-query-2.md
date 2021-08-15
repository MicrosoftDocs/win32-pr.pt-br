---
description: Nomeia a consulta de serviço Windows Soquetes (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Consulta de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5452c94c3768cbff387b0125fe183a3026f7ab6c64d90325341ce5f2a9366de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740415"
---
# <a name="service-query"></a>Consulta de serviço

-   [**Nsplookupservicebegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**Nsplookupservicenext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**Nsplookupserviceend**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Uma consulta de serviço de nome envolve uma série de chamadas: [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), seguida por uma ou mais chamadas para [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) e terminando com uma chamada para [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) aceita uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como entrada para definir os parâmetros de consulta junto com um conjunto de sinalizadores para fornecer controle adicional sobre a operação de pesquisa. Ele retorna um alça de consulta que é usado nas chamadas subsequentes para **NSPLookupServiceNext** e **NSPLookupServiceEnd**.

O cliente spi do namespace invoca [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) para obter resultados da consulta, com os resultados fornecidos em um buffer [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecido pelo cliente. O cliente continua a chamar **NSPLookupServiceNext** até que o código de erro WSA E NO MORE seja retornado, indicando que todos os resultados \_ \_ foram \_ recuperados. Em seguida, a pesquisa é encerrada por uma chamada para [**NSPLookupServiceEnd.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend) A **função NSPLookupServiceEnd** também pode ser usada para cancelar um **NSPLookupServiceNext** pendente quando chamado de outro thread.

No Windows Sockets 2, códigos de erro conflitantes são definidos para WSAENOMORE (10102) e WSA \_ E \_ NO MORE \_ (10110). O código de erro WSAENOMORE será removido em uma versão futura e somente o WSA \_ E \_ NO MORE \_ permanecerá. Os provedores de namespace devem alternar para usar o código de erro WSA E NO MORE assim que possível para manter a compatibilidade com a maior variedade \_ \_ possível de \_ aplicativos.

 

 



