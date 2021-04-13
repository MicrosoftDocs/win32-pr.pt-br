---
description: A partir de provedores de serviços de telefonia do Windows 2000 que negociam uma versão do 3,0 ou posterior deve ter um provedor de serviços de mídia correspondente.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Comunicação do provedor de serviços de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297944"
---
# <a name="media-service-provider-communication"></a>Comunicação do provedor de serviços de mídia

A partir de provedores de serviços de telefonia do Windows 2000 que negociam uma versão do 3,0 ou posterior deve ter um provedor de serviços de mídia correspondente. A divisão precisa das responsabilidades operacionais é dependente da implementação. Por exemplo, um TSP pode usar o MSP correspondente para executar a determinação do tipo de mídia em uma sessão de entrada. No entanto, o TSP deve estar em conformidade com o TSPI, o que significa obter essa determinação do MSP e reportá-lo para a TAPI.

O TSPI fornece as seguintes funções e mensagens para permitir uma conexão virtual entre um TSP e um MSP:

-   [**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ lineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**QOSINFO de linha \_**](line-qosinfo.md)
-   [**SENDMSPDATA de linha \_**](line-sendmspdata.md)

 

 
