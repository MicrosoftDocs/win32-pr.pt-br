---
title: Método ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de descrição de estado do rasterizador de um objeto que implementa essa interface.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Método RasterizerStateCb
- Método RasterizerStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método RasterizerStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772646"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a><span data-ttu-id="98567-106">Método ID3DX12PipelineParserCallbacks:: RasterizerStateCb</span><span class="sxs-lookup"><span data-stu-id="98567-106">ID3DX12PipelineParserCallbacks::RasterizerStateCb method</span></span>

<span data-ttu-id="98567-107">Chama o retorno de chamada de subobjeto de descrição de estado do rasterizador de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="98567-107">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="98567-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98567-108">Syntax</span></span>


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="98567-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98567-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98567-110">*RasterizerState* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="98567-110">*RasterizerState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="98567-111">Tipo: **const [**D3D12 \_ rasterizador \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span><span class="sxs-lookup"><span data-stu-id="98567-111">Type: **const [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span></span>

<span data-ttu-id="98567-112">Detalhes do subobjeto de descrição do estado do rasterizador analisado a partir de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="98567-112">Details of the rasterizer state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98567-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98567-113">Return value</span></span>

<span data-ttu-id="98567-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="98567-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="98567-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98567-115">Requirements</span></span>



| <span data-ttu-id="98567-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="98567-116">Requirement</span></span> | <span data-ttu-id="98567-117">Valor</span><span class="sxs-lookup"><span data-stu-id="98567-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="98567-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98567-118">Header</span></span><br/>  | <dl> <span data-ttu-id="98567-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="98567-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="98567-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98567-120">Library</span></span><br/> | <dl> <span data-ttu-id="98567-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98567-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="98567-122">DLL</span><span class="sxs-lookup"><span data-stu-id="98567-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="98567-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98567-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98567-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="98567-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98567-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="98567-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="98567-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="98567-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="98567-127">**D3D12 do \_ rasterizador \_ desc**</span><span class="sxs-lookup"><span data-stu-id="98567-127">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





