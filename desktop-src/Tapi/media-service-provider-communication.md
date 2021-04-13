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
# <a name="media-service-provider-communication"></a><span data-ttu-id="67455-103">Comunicação do provedor de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="67455-103">Media Service Provider Communication</span></span>

<span data-ttu-id="67455-104">A partir de provedores de serviços de telefonia do Windows 2000 que negociam uma versão do 3,0 ou posterior deve ter um provedor de serviços de mídia correspondente.</span><span class="sxs-lookup"><span data-stu-id="67455-104">Starting with Windows 2000 telephony service providers that negotiate a version of 3.0 or later must have a matching media service provider.</span></span> <span data-ttu-id="67455-105">A divisão precisa das responsabilidades operacionais é dependente da implementação.</span><span class="sxs-lookup"><span data-stu-id="67455-105">The precise division of operational responsibilities is implementation dependent.</span></span> <span data-ttu-id="67455-106">Por exemplo, um TSP pode usar o MSP correspondente para executar a determinação do tipo de mídia em uma sessão de entrada.</span><span class="sxs-lookup"><span data-stu-id="67455-106">For example, a TSP might use the matching MSP to perform media type determination on an incoming session.</span></span> <span data-ttu-id="67455-107">No entanto, o TSP deve estar em conformidade com o TSPI, o que significa obter essa determinação do MSP e reportá-lo para a TAPI.</span><span class="sxs-lookup"><span data-stu-id="67455-107">However, the TSP must conform to the TSPI, which means getting that determination from the MSP and reporting it to TAPI.</span></span>

<span data-ttu-id="67455-108">O TSPI fornece as seguintes funções e mensagens para permitir uma conexão virtual entre um TSP e um MSP:</span><span class="sxs-lookup"><span data-stu-id="67455-108">TSPI provides the following functions and messages to allow a virtual connection between a TSP and an MSP:</span></span>

-   [<span data-ttu-id="67455-109">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="67455-109">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="67455-110">**TSPI \_ lineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="67455-110">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="67455-111">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="67455-111">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="67455-112">**TSPI \_ lineReceiveMSPData**</span><span class="sxs-lookup"><span data-stu-id="67455-112">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="67455-113">**QOSINFO de linha \_**</span><span class="sxs-lookup"><span data-stu-id="67455-113">**LINE\_QOSINFO**</span></span>](line-qosinfo.md)
-   [<span data-ttu-id="67455-114">**SENDMSPDATA de linha \_**</span><span class="sxs-lookup"><span data-stu-id="67455-114">**LINE\_SENDMSPDATA**</span></span>](line-sendmspdata.md)

 

 
