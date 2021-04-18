---
description: O terminal CAudioCaptureTerminal é derivado de CSingleFilterTerminal e implementa um terminal de captura de áudio estático para dispositivos Wave usando o filtro Wave do DirectShow. A maioria dos MSPs não precisará substituir a implementação desse terminal.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: CAudioCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781053"
---
# <a name="caudiocaptureterminal"></a><span data-ttu-id="e4a9b-104">CAudioCaptureTerminal</span><span class="sxs-lookup"><span data-stu-id="e4a9b-104">CAudioCaptureTerminal</span></span>

<span data-ttu-id="e4a9b-105">O terminal **CAudioCaptureTerminal** é derivado de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa um terminal de captura de áudio estático para dispositivos Wave usando o filtro Wave do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e4a9b-105">The **CAudioCaptureTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio capture terminal for wave devices using the DirectShow wavein filter.</span></span> <span data-ttu-id="e4a9b-106">A maioria dos MSPs não precisará substituir a implementação desse terminal.</span><span class="sxs-lookup"><span data-stu-id="e4a9b-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="e4a9b-107">Definido em MSPtmac. h.</span><span class="sxs-lookup"><span data-stu-id="e4a9b-107">Defined in MSPtmac.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a9b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4a9b-108">Remarks</span></span>

<span data-ttu-id="e4a9b-109">Os métodos de balanceamento [**Put \_**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**obter \_ balanceamento**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioCaptureTerminal** não são implementados e retornarão e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e4a9b-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioCaptureTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



