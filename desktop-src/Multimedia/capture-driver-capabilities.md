---
title: Recursos do driver de captura
description: Recursos do driver de captura
ms.assetid: 6e74635e-9dac-419d-a264-08fee04ae7b7
keywords:
- WM_CAP_DRIVER_GET_CAPS mensagem
- macro capDriverGetCaps
- Estrutura CAPDRIVERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87fb4f9cb439229721b6c10aa6207af601f9ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005118"
---
# <a name="capture-driver-capabilities"></a><span data-ttu-id="8de17-106">Recursos do driver de captura</span><span class="sxs-lookup"><span data-stu-id="8de17-106">Capture Driver Capabilities</span></span>

<span data-ttu-id="8de17-107">Você pode recuperar os recursos de hardware do driver de captura conectado no momento usando a mensagem [**\_ \_ \_ obter \_ Caps do driver do WM Cap**](wm-cap-driver-get-caps.md) (ou a macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) ).</span><span class="sxs-lookup"><span data-stu-id="8de17-107">You can retrieve the hardware capabilities of the currently connected capture driver by using the [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message (or the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro).</span></span> <span data-ttu-id="8de17-108">Essa mensagem retorna os recursos do driver de captura e o hardware subjacente na estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="8de17-108">This message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

 

 




