---
description: Consulta de serviço de nome no Windows Sockets (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Consulta de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010822"
---
# <a name="service-query"></a>Consulta de serviço

-   [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Uma consulta de serviço de nome envolve uma série de chamadas: [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), seguida por uma ou mais chamadas para [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) e terminando com uma chamada para [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como entrada para definir os parâmetros de consulta junto com um conjunto de sinalizadores para fornecer controle adicional sobre a operação de pesquisa. Ele retorna um identificador de consulta que é usado nas chamadas subsequentes para **NSPLookupServiceNext** e **NSPLookupServiceEnd**.

O cliente SPI do namespace invoca [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) para obter os resultados da consulta, com os resultados fornecidos em um buffer [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecido pelo cliente. O cliente continua a chamar **NSPLookupServiceNext** até que o código de erro WSA \_ E \_ não \_ mais seja retornado, indicando que todos os resultados foram recuperados. Em seguida, a pesquisa é encerrada por uma chamada para [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). A função **NSPLookupServiceEnd** também pode ser usada para cancelar um **NSPLookupServiceNext** pendente no momento quando chamado de outro thread.

No Windows Sockets 2, códigos de erro conflitantes são definidos para WSAENOMORE (10102) e WSA \_ e \_ não \_ mais (10110). O código de erro WSAENOMORE será removido em uma versão futura e somente o WSA \_ e \_ não \_ será mais mantido. Provedores de namespace devem alternar para o uso do WSA \_ E \_ não \_ mais código de erro assim que possível para manter a compatibilidade com a maior variedade possível de aplicativos.

 

 



