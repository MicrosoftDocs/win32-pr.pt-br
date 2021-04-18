---
title: Método ID3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto do tipo de topologia primitiva de um objeto que implementa essa interface.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Método PrimitiveTopologyTypeCb
- Método PrimitiveTopologyTypeCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método PrimitiveTopologyTypeCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780691"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a><span data-ttu-id="acd17-106">ID3DX12PipelineParserCallbacks: método rimitiveTopologyTypeCb de:P</span><span class="sxs-lookup"><span data-stu-id="acd17-106">ID3DX12PipelineParserCallbacks::PrimitiveTopologyTypeCb method</span></span>

<span data-ttu-id="acd17-107">Chama o retorno de chamada de subobjeto do tipo de topologia primitiva de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="acd17-107">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="acd17-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acd17-108">Syntax</span></span>


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a><span data-ttu-id="acd17-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acd17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd17-110">*PrimitiveTopologyType*</span><span class="sxs-lookup"><span data-stu-id="acd17-110">*PrimitiveTopologyType*</span></span> 
</dt> <dd>

<span data-ttu-id="acd17-111">Tipo: **[ **\_ tipo de \_ topologia \_ primitivo D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span><span class="sxs-lookup"><span data-stu-id="acd17-111">Type: **[**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span></span>

<span data-ttu-id="acd17-112">Detalhes do subobjeto do tipo de topologia primitiva analisado de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="acd17-112">Details of the primitive topology type subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acd17-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="acd17-113">Return value</span></span>

<span data-ttu-id="acd17-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="acd17-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="acd17-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acd17-115">Requirements</span></span>



| <span data-ttu-id="acd17-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="acd17-116">Requirement</span></span> | <span data-ttu-id="acd17-117">Valor</span><span class="sxs-lookup"><span data-stu-id="acd17-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="acd17-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="acd17-118">Header</span></span><br/>  | <dl> <span data-ttu-id="acd17-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="acd17-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="acd17-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="acd17-120">Library</span></span><br/> | <dl> <span data-ttu-id="acd17-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acd17-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="acd17-122">DLL</span><span class="sxs-lookup"><span data-stu-id="acd17-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="acd17-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acd17-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acd17-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="acd17-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd17-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="acd17-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="acd17-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="acd17-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="acd17-127">**\_Tipo de \_ topologia \_ primitivo D3D12**</span><span class="sxs-lookup"><span data-stu-id="acd17-127">**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





