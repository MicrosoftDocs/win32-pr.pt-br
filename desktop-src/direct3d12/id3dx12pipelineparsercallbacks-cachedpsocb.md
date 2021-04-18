---
title: Método ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto PSO (objeto de estado de pipeline) armazenado em cache de um objeto que implementa essa interface.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Método CachedPSOCb
- Método CachedPSOCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método CachedPSOCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807899"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a><span data-ttu-id="40a5b-106">Método ID3DX12PipelineParserCallbacks:: CachedPSOCb</span><span class="sxs-lookup"><span data-stu-id="40a5b-106">ID3DX12PipelineParserCallbacks::CachedPSOCb method</span></span>

<span data-ttu-id="40a5b-107">Chama o retorno de chamada de subobjeto PSO (objeto de estado de pipeline) armazenado em cache de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="40a5b-107">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a5b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40a5b-108">Syntax</span></span>


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a><span data-ttu-id="40a5b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40a5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a5b-110">*CachedPSO* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="40a5b-110">*CachedPSO* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="40a5b-111">Tipo: **const [**D3D12 \_ estado de \_ pipeline \_ armazenado em cache**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span><span class="sxs-lookup"><span data-stu-id="40a5b-111">Type: **const [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span></span>

<span data-ttu-id="40a5b-112">Detalhes do subobjeto de PSO (objeto de estado do Pipeline) em cache analisado a partir de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="40a5b-112">Details of the cached PSO (Pipeline State Object) subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a5b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40a5b-113">Return value</span></span>

<span data-ttu-id="40a5b-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="40a5b-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a5b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40a5b-115">Requirements</span></span>



| <span data-ttu-id="40a5b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a5b-116">Requirement</span></span> | <span data-ttu-id="40a5b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="40a5b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="40a5b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40a5b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="40a5b-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a5b-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="40a5b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40a5b-120">Library</span></span><br/> | <dl> <span data-ttu-id="40a5b-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40a5b-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="40a5b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="40a5b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="40a5b-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40a5b-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a5b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="40a5b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a5b-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="40a5b-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="40a5b-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="40a5b-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="40a5b-127">**\_Estado de pipeline armazenado em cache D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40a5b-127">**D3D12\_CACHED\_PIPELINE\_STATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





