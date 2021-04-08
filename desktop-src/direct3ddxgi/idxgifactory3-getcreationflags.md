---
description: Obtém os sinalizadores que foram usados quando um objeto de infraestrutura gráfica do Microsoft DirectX (DXGI) foi criado.
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
title: 'Método IDXGIFactory3:: GetCreationFlags'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDXGIFactory3.GetCreationFlags
api_type:
- COM
api_location:
- dxgi1_3.h
ms.openlocfilehash: 56d1f35ea5a4ce26a0d9ccb5ee0d79035f74a0ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087207"
---
# <a name="idxgifactory3getcreationflags-method"></a><span data-ttu-id="17408-103">Método IDXGIFactory3:: GetCreationFlags</span><span class="sxs-lookup"><span data-stu-id="17408-103">IDXGIFactory3::GetCreationFlags method</span></span>

<span data-ttu-id="17408-104">Obtém os sinalizadores que foram usados quando um objeto de infraestrutura gráfica do Microsoft DirectX (DXGI) foi criado.</span><span class="sxs-lookup"><span data-stu-id="17408-104">Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.</span></span>

## <a name="syntax"></a><span data-ttu-id="17408-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17408-105">Syntax</span></span>


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a><span data-ttu-id="17408-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17408-106">Parameters</span></span>

<span data-ttu-id="17408-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="17408-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17408-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17408-108">Return value</span></span>

<span data-ttu-id="17408-109">Os sinalizadores de criação.</span><span class="sxs-lookup"><span data-stu-id="17408-109">The creation flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="17408-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="17408-110">Remarks</span></span>

<span data-ttu-id="17408-111">O método **GetCreationFlags** retorna sinalizadores que foram passados para a [**função CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) ou criados implicitamente por [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)ou [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="17408-111">The **GetCreationFlags** method returns flags that were passed to the [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) function, or were implicitly constructed by [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice), or [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="see-also"></a><span data-ttu-id="17408-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="17408-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17408-113">**IDXGIFactory3**</span><span class="sxs-lookup"><span data-stu-id="17408-113">**IDXGIFactory3**</span></span>](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
