---
description: A partir Windows provedores de serviços de telefonia do 2000 que negociam uma versão 3.0 ou posterior devem ter um provedor de serviços de mídia correspondente.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Comunicação do Provedor de Serviços de Mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3797d02c67fc86ebfb44ff9e0e7b2c85cd1604206a58f1d8f5c3ca293599e92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404816"
---
# <a name="media-service-provider-communication"></a>Comunicação do Provedor de Serviços de Mídia

A partir Windows provedores de serviços de telefonia do 2000 que negociam uma versão 3.0 ou posterior devem ter um provedor de serviços de mídia correspondente. A divisão precisa das responsabilidades operacionais depende da implementação. Por exemplo, um TSP pode usar o MSP correspondente para executar a determinação do tipo de mídia em uma sessão de entrada. No entanto, o TSP deve estar em conformidade com o TSPI, o que significa obter essa determinação do MSP e reportá-la à TAPI.

O TSPI fornece as seguintes funções e mensagens para permitir uma conexão virtual entre um TSP e um MSP:

-   [**Linha \_ TSPICloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**Linha \_ TSPICreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**Linha \_ TSPIMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**Linha \_ TSPIReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**LINE \_ QOSINFO**](line-qosinfo.md)
-   [**LINE \_ SENDMSPDATA**](line-sendmspdata.md)

 

 
