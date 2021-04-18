---
title: Método ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject (D3DX12. h)
description: Chama o retorno de chamada de erro de subobjeto duplicado de um objeto que implementa essa interface.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Método ErrorDuplicateSubobject
- Método ErrorDuplicateSubobject, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método ErrorDuplicateSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787653"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a><span data-ttu-id="1a15b-106">Método ID3DX12PipelineParserCallbacks:: ErrorDuplicateSubobject</span><span class="sxs-lookup"><span data-stu-id="1a15b-106">ID3DX12PipelineParserCallbacks::ErrorDuplicateSubobject method</span></span>

<span data-ttu-id="1a15b-107">Chama o retorno de chamada de erro de subobjeto duplicado de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="1a15b-107">Calls the duplicate subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a15b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a15b-108">Syntax</span></span>


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a><span data-ttu-id="1a15b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a15b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a15b-110">*Duplicatetype*</span><span class="sxs-lookup"><span data-stu-id="1a15b-110">*DuplicateType*</span></span> 
</dt> <dd>

<span data-ttu-id="1a15b-111">Tipo: **[ **\_ \_ \_ \_ tipo de subobjeto de estado de pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span><span class="sxs-lookup"><span data-stu-id="1a15b-111">Type: **[**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span></span>

<span data-ttu-id="1a15b-112">O tipo de subobjeto que foi duplicado.</span><span class="sxs-lookup"><span data-stu-id="1a15b-112">The subobject type that was duplicated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a15b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a15b-113">Return value</span></span>

<span data-ttu-id="1a15b-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="1a15b-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a15b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a15b-115">Requirements</span></span>



| <span data-ttu-id="1a15b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a15b-116">Requirement</span></span> | <span data-ttu-id="1a15b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1a15b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1a15b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a15b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1a15b-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a15b-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="1a15b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a15b-120">Library</span></span><br/> | <dl> <span data-ttu-id="1a15b-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a15b-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a15b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1a15b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a15b-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a15b-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a15b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a15b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a15b-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1a15b-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1a15b-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="1a15b-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="1a15b-127">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1a15b-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

