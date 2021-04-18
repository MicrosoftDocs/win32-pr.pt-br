---
title: Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de estado de estêncil de profundidade de um objeto que implementa essa interface.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Método DepthStencilStateCb
- Método DepthStencilStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763496"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a><span data-ttu-id="e6d15-106">Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)</span><span class="sxs-lookup"><span data-stu-id="e6d15-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h)</span></span>

<span data-ttu-id="e6d15-107">Chama o retorno de chamada de subobjeto de estado de estêncil de profundidade de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="e6d15-107">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d15-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6d15-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="e6d15-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6d15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d15-110">*DepthStencilState* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="e6d15-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d15-111">Tipo: **const [**D3D12 \_ de \_ estêncil \_ de profundidade desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span><span class="sxs-lookup"><span data-stu-id="e6d15-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span></span>

<span data-ttu-id="e6d15-112">Detalhes do subobjeto de estado de estêncil de profundidade analisado de um fluxo de estado de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6d15-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d15-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6d15-113">Return value</span></span>

<span data-ttu-id="e6d15-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="e6d15-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d15-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6d15-115">Requirements</span></span>



| <span data-ttu-id="e6d15-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d15-116">Requirement</span></span> | <span data-ttu-id="e6d15-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e6d15-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d15-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6d15-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e6d15-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6d15-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="e6d15-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6d15-120">Library</span></span><br/> | <dl> <span data-ttu-id="e6d15-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6d15-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6d15-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e6d15-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6d15-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6d15-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6d15-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6d15-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d15-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e6d15-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e6d15-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="e6d15-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="e6d15-127">**Desc. de estêncil de profundidade de D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e6d15-127">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





