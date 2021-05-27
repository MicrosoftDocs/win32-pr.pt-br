---
title: O dispositivo D1112 deve ser DX11
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: O dispositivo associado à superfície DXGI deve ser um dispositivo D3D11.
keywords:
- O dispositivo D1112 deve ser DX11 Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 68408c56710589def033c34d20d9bac81e8d4947
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549881"
---
# <a name="d1112-device-must-be-dx11"></a><span data-ttu-id="2f770-104">D1112: o dispositivo deve ser DX11</span><span class="sxs-lookup"><span data-stu-id="2f770-104">D1112: Device Must Be DX11</span></span>

<span data-ttu-id="2f770-105">O dispositivo associado à superfície DXGI deve ser um dispositivo D3D11.</span><span class="sxs-lookup"><span data-stu-id="2f770-105">The device associated with the DXGI surface must be a D3D11 device.</span></span>



| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="2f770-106">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="2f770-106">Error Level</span></span> | <span data-ttu-id="2f770-107">Aviso</span><span class="sxs-lookup"><span data-stu-id="2f770-107">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="2f770-108">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="2f770-108">Possible Causes</span></span>

<span data-ttu-id="2f770-109">Houve uma tentativa de usar [**o CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) com uma superfície DXGI criada por um dispositivo não Direct3D11.</span><span class="sxs-lookup"><span data-stu-id="2f770-109">There was an attempt to use the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) with a DXGI surface created by a non-Direct3D11 device.</span></span>

 

 




