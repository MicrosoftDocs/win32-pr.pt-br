---
description: Crie o melhor dispositivo Direct3D e uma cadeia de permuta.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Função D3DX10CreateDeviceAndSwapChain (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298759"
---
# <a name="d3dx10createdeviceandswapchain-function"></a><span data-ttu-id="24304-103">Função D3DX10CreateDeviceAndSwapChain</span><span class="sxs-lookup"><span data-stu-id="24304-103">D3DX10CreateDeviceAndSwapChain function</span></span>

<span data-ttu-id="24304-104">Crie o melhor dispositivo Direct3D e uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="24304-104">Create the best Direct3D device and a swap chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="24304-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24304-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="24304-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24304-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24304-107">*pAdapter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24304-107">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24304-108">Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="24304-108">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="24304-109">Ponteiro para um [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span><span class="sxs-lookup"><span data-stu-id="24304-109">Pointer to a [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span></span>

</dd> <dt>

<span data-ttu-id="24304-110">*DriverType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24304-110">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24304-111">Tipo: **[ **\_ \_ tipo de driver d3d10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="24304-111">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="24304-112">O tipo de driver para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24304-112">The type of driver for the device.</span></span> <span data-ttu-id="24304-113">Consulte [**\_ \_ tipo de driver d3d10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span><span class="sxs-lookup"><span data-stu-id="24304-113">See [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span></span>

</dd> <dt>

<span data-ttu-id="24304-114">*Software* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24304-114">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24304-115">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24304-115">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24304-116">Um identificador para a DLL que implementa um rasterizador de software.</span><span class="sxs-lookup"><span data-stu-id="24304-116">A handle to the DLL that implements a software rasterizer.</span></span> <span data-ttu-id="24304-117">Deve ser **NULL** se o driverType for não software.</span><span class="sxs-lookup"><span data-stu-id="24304-117">Must be **NULL** if DriverType is non-software.</span></span> <span data-ttu-id="24304-118">O HMODULE de uma DLL pode ser obtido com [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)ou [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="24304-118">The HMODULE of a DLL can be obtained with [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa), or [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="24304-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="24304-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24304-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24304-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24304-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="24304-121">Optional.</span></span> <span data-ttu-id="24304-122">Sinalizadores de criação de dispositivo (consulte [**d3d10 \_ criar \_ \_ sinalizador de dispositivo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) que habilitam [camadas de API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="24304-122">Device creation flags (see [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="24304-123">Esses sinalizadores podem ser unificados ou juntos.</span><span class="sxs-lookup"><span data-stu-id="24304-123">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="24304-124">*pSwapChainDesc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24304-124">*pSwapChainDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24304-125">Tipo: a **[ **cadeia de permuta do dxgi \_ \_ \_ desc**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span><span class="sxs-lookup"><span data-stu-id="24304-125">Type: **[**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span></span>

<span data-ttu-id="24304-126">Descrição da cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="24304-126">Description of the swap chain.</span></span> <span data-ttu-id="24304-127">Consulte [**\_ desc de \_ cadeia \_ de permuta dxgi**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span><span class="sxs-lookup"><span data-stu-id="24304-127">See [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span></span>

</dd> <dt>

<span data-ttu-id="24304-128">*ppSwapChain* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="24304-128">*ppSwapChain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24304-129">Tipo: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span><span class="sxs-lookup"><span data-stu-id="24304-129">Type: **[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span></span>

<span data-ttu-id="24304-130">Endereço de um ponteiro para um [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="24304-130">Address of a pointer to an [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

</dd> <dt>

<span data-ttu-id="24304-131">*ppDevice* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="24304-131">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24304-132">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="24304-132">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="24304-133">Endereço de um ponteiro para uma [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) que receberá o dispositivo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="24304-133">Address of a pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) that will receive the newly created device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24304-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24304-134">Return value</span></span>

<span data-ttu-id="24304-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24304-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24304-136">Esse método retorna um dos seguintes [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="24304-136">This method returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="24304-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="24304-137">Remarks</span></span>

<span data-ttu-id="24304-138">Para criar o melhor dispositivo, esse método implementa mais de uma opção de criação de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24304-138">To create the best device, this method implements more than one device creation option.</span></span> <span data-ttu-id="24304-139">Primeiro, o método tenta criar um dispositivo 10,1 (e uma cadeia de permuta).</span><span class="sxs-lookup"><span data-stu-id="24304-139">First, the method attempts to create a 10.1 device (and swap chain).</span></span> <span data-ttu-id="24304-140">Se isso falhar, o método tentará criar um dispositivo 10,0.</span><span class="sxs-lookup"><span data-stu-id="24304-140">If that fails, the method attempts to create a 10.0 device.</span></span> <span data-ttu-id="24304-141">Se isso falhar, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="24304-141">If that fails, the method will fail.</span></span> <span data-ttu-id="24304-142">Se seu aplicativo precisar criar apenas um dispositivo 10,1 ou um dispositivo 10,0, use essas APIs em vez disso:</span><span class="sxs-lookup"><span data-stu-id="24304-142">If your application needs to create only a 10.1 device, or a 10.0 device only, use these APIs instead:</span></span>

-   <span data-ttu-id="24304-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) para criar um dispositivo Direct3D 10,0 (somente) e uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="24304-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) to create a Direct3D 10.0 (only) device and swap chain.</span></span>
-   <span data-ttu-id="24304-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) para criar um dispositivo Direct3D 10,1 (somente) e uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="24304-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) to create a Direct3D 10.1 (only) device and swap chain.</span></span>

<span data-ttu-id="24304-145">Esse método requer o Windows Vista Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="24304-145">This method requires Windows Vista Service Pack 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="24304-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24304-146">Requirements</span></span>



| <span data-ttu-id="24304-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="24304-147">Requirement</span></span> | <span data-ttu-id="24304-148">Valor</span><span class="sxs-lookup"><span data-stu-id="24304-148">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24304-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24304-149">Header</span></span><br/> | <dl> <span data-ttu-id="24304-150"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="24304-150"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24304-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="24304-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24304-152">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="24304-152">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
