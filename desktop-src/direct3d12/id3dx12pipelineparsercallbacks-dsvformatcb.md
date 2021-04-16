---
title: Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) (DSV)
description: Chama o retorno de chamada de subobjeto de formato de valor de estêncil de profundidade de um objeto que implementa essa interface.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
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
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187907"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a><span data-ttu-id="5d6f6-106">Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) para o valor de estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="5d6f6-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h) for depth stencil value</span></span>

<span data-ttu-id="5d6f6-107">Chama o retorno de chamada de subobjeto de formato de valor de estêncil de profundidade de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="5d6f6-107">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6f6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d6f6-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="5d6f6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d6f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d6f6-110">*DepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="5d6f6-110">*DepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6f6-111">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5d6f6-111">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5d6f6-112">Detalhes do subobjeto formato do valor do estêncil de profundidade analisado de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d6f6-112">Details of the depth stencil value format subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d6f6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d6f6-113">Return value</span></span>

<span data-ttu-id="5d6f6-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="5d6f6-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d6f6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d6f6-115">Requirements</span></span>



| <span data-ttu-id="5d6f6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d6f6-116">Requirement</span></span> | <span data-ttu-id="5d6f6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5d6f6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6f6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d6f6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5d6f6-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d6f6-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5d6f6-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d6f6-120">Library</span></span><br/> | <dl> <span data-ttu-id="5d6f6-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d6f6-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5d6f6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5d6f6-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d6f6-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d6f6-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d6f6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d6f6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6f6-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5d6f6-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5d6f6-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="5d6f6-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="5d6f6-127">**\_formato dxgi**</span><span class="sxs-lookup"><span data-stu-id="5d6f6-127">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

