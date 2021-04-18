---
description: Sinalizadores para opções de criação de recursos e superfície.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813594"
---
# <a name="dxgi_usage"></a><span data-ttu-id="20f89-103">uso de DXGI \_</span><span class="sxs-lookup"><span data-stu-id="20f89-103">DXGI\_USAGE</span></span>

<span data-ttu-id="20f89-104">Sinalizadores para opções de criação de recursos e superfície.</span><span class="sxs-lookup"><span data-stu-id="20f89-104">Flags for surface and resource creation options.</span></span>



| <span data-ttu-id="20f89-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="20f89-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="20f89-106">Description</span><span class="sxs-lookup"><span data-stu-id="20f89-106">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <span data-ttu-id="20f89-107"><dt>**Dxgi \_ \_ \_**</dt> <dt>1L <<  de buffer de fundo de uso (2 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="20f89-107"><dt>**DXGI\_USAGE\_BACK\_BUFFER**</dt> <dt>1L << (2 + 4)</dt></span></span> </dl>                             | <span data-ttu-id="20f89-108">A superfície ou o recurso é usado como um buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="20f89-108">The surface or resource is used as a back buffer.</span></span> <span data-ttu-id="20f89-109">Você não precisa passar o **\_ buffer de \_ fundo \_ de uso de dxgi** ao criar uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="20f89-109">You don’t need to pass **DXGI\_USAGE\_BACK\_BUFFER** when you create a swap chain.</span></span> <span data-ttu-id="20f89-110">Mas você pode determinar se um recurso pertence a uma cadeia de permuta ao chamar [**IDXGIResource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) e obter **o \_ \_ \_ buffer de fundo de uso de dxgi**.</span><span class="sxs-lookup"><span data-stu-id="20f89-110">But you can determine whether a resource belongs to a swap chain when you call [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) and get **DXGI\_USAGE\_BACK\_BUFFER**.</span></span><br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <span data-ttu-id="20f89-111"><dt>**Dxgi \_ \_Descartar uso \_ no 1L \_ presente**</dt> <dt> <<  (5 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="20f89-111"><dt>**DXGI\_USAGE\_DISCARD\_ON\_PRESENT**</dt> <dt>1L << (5 + 4)</dt></span></span> </dl>       | <span data-ttu-id="20f89-112">Esse sinalizador é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="20f89-112">This flag is for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <span data-ttu-id="20f89-113"><dt>**Dxgi \_ 1L \_ \_ somente leitura de uso**</dt> <dt> <<  (4 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="20f89-113"><dt>**DXGI\_USAGE\_READ\_ONLY**</dt> <dt>1L << (4 + 4)</dt></span></span> </dl>                                   | <span data-ttu-id="20f89-114">Use a superfície ou o recurso para leitura apenas.</span><span class="sxs-lookup"><span data-stu-id="20f89-114">Use the surface or resource for reading only.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <span data-ttu-id="20f89-115"><dt>**Dxgi \_ 1L <<  de \_ \_ \_ saída de destino de renderização de uso**</dt> <dt>(1 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="20f89-115"><dt>**DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT**</dt> <dt>1L << (1 + 4)</dt></span></span> </dl> | <span data-ttu-id="20f89-116">Use a superfície ou o recurso como um destino de renderização de saída.</span><span class="sxs-lookup"><span data-stu-id="20f89-116">Use the surface or resource as an output render target.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <span data-ttu-id="20f89-117"><dt>**Dxgi \_ <<  \_ de \_ entrada do sombreador de uso**</dt> <dt>1L (0 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="20f89-117"><dt>**DXGI\_USAGE\_SHADER\_INPUT**</dt> <dt>1L << (0 + 4)</dt></span></span> </dl>                          | <span data-ttu-id="20f89-118">Use a superfície ou o recurso como uma entrada para um sombreador.</span><span class="sxs-lookup"><span data-stu-id="20f89-118">Use the surface or resource as an input to a shader.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <span data-ttu-id="20f89-119"><dt>**Dxgi \_ 1L \_ compartilhado de uso**</dt> <dt> <<  (3 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="20f89-119"><dt>**DXGI\_USAGE\_SHARED**</dt> <dt>1L << (3 + 4)</dt></span></span> </dl>                                             | <span data-ttu-id="20f89-120">Compartilhe a superfície ou o recurso.</span><span class="sxs-lookup"><span data-stu-id="20f89-120">Share the surface or resource.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <span data-ttu-id="20f89-121"><dt>**Dxgi \_ 1L de \_ \_ acesso não ordenado de uso**</dt> <dt> <<  (6 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="20f89-121"><dt>**DXGI\_USAGE\_UNORDERED\_ACCESS**</dt> <dt>1L << (6 + 4)</dt></span></span> </dl>              | <span data-ttu-id="20f89-122">Use a superfície ou o recurso para acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="20f89-122">Use the surface or resource for unordered access.</span></span><br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="20f89-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="20f89-123">Remarks</span></span>

<span data-ttu-id="20f89-124">Cada sinalizador é definido como um inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="20f89-124">Each flag is defined as an unsigned integer.</span></span>

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

<span data-ttu-id="20f89-125">Essas opções de sinalizador são usadas em uma chamada para o método [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)ou [**IDXGIFactory2:: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) para descrever as opções de uso da superfície e de acesso da CPU para o buffer de fundo de uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="20f89-125">These flag options are used in a call to the [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow), or [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method to describe the surface usage and CPU access options for the back buffer of a swap chain.</span></span> <span data-ttu-id="20f89-126">Você não pode usar **o \_ uso \_ de dxgi compartilhado**, **\_ \_ descarte \_ de uso de dxgi em diante \_** e os valores de **\_ uso \_ \_ somente leitura de dxgi** como entrada para criar uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="20f89-126">You can't use the **DXGI\_USAGE\_SHARED**, **DXGI\_USAGE\_DISCARD\_ON\_PRESENT**, and **DXGI\_USAGE\_READ\_ONLY** values as input to create a swap chain.</span></span> <span data-ttu-id="20f89-127">No entanto, DXGI pode definir o **\_ \_ descarte \_ de uso de dxgi no \_ momento** e o **uso de dxgi \_ \_ \_ somente leitura** para alguns dos buffers de fundo da cadeia de troca em nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="20f89-127">However, DXGI can set **DXGI\_USAGE\_DISCARD\_ON\_PRESENT** and **DXGI\_USAGE\_READ\_ONLY** for some of the swap chain's back buffers on the application's behalf.</span></span> <span data-ttu-id="20f89-128">Você pode chamar o método [**IDXGIResource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) para recuperar o uso desses buffers de fundo.</span><span class="sxs-lookup"><span data-stu-id="20f89-128">You can call the [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) method to retrieve the usage of these back buffers.</span></span> <span data-ttu-id="20f89-129">A cadeia de permuta só dá suporte ao valor de **\_ \_ \_ nenhum acesso da CPU dxgi** no **\_ campo de \_ acesso \_ à CPU dxgi** da parte do **\_ uso de dxgi**.</span><span class="sxs-lookup"><span data-stu-id="20f89-129">Swap chain's only support the **DXGI\_CPU\_ACCESS\_NONE** value in the **DXGI\_CPU\_ACCESS\_FIELD** part of **DXGI\_USAGE**.</span></span>

<span data-ttu-id="20f89-130">Essas opções de sinalizador também são usadas pelo método [**IDXGIDevice:: CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .</span><span class="sxs-lookup"><span data-stu-id="20f89-130">These flag options are also used by the [**IDXGIDevice::CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f89-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20f89-131">Requirements</span></span>



| <span data-ttu-id="20f89-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="20f89-132">Requirement</span></span> | <span data-ttu-id="20f89-133">Valor</span><span class="sxs-lookup"><span data-stu-id="20f89-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="20f89-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20f89-134">Header</span></span><br/> | <dl> <span data-ttu-id="20f89-135"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="20f89-135"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f89-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="20f89-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f89-137">Constantes DXGI</span><span class="sxs-lookup"><span data-stu-id="20f89-137">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




