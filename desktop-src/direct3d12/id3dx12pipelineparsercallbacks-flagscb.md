---
title: Método ID3DX12PipelineParserCallbacks FlagsCb (D3DX12. h)
description: Chama o retorno de chamada do subobjeto flags de um objeto que implementa essa interface.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Método FlagsCb
- Método FlagsCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método FlagsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772520"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a><span data-ttu-id="f3ec7-106">Método ID3DX12PipelineParserCallbacks:: FlagsCb</span><span class="sxs-lookup"><span data-stu-id="f3ec7-106">ID3DX12PipelineParserCallbacks::FlagsCb method</span></span>

<span data-ttu-id="f3ec7-107">Chama o retorno de chamada do subobjeto flags de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="f3ec7-107">Calls the flags subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ec7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3ec7-108">Syntax</span></span>


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="f3ec7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3ec7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3ec7-110">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="f3ec7-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ec7-111">Tipo: **[ **\_ sinalizadores de \_ estado \_ do pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span><span class="sxs-lookup"><span data-stu-id="f3ec7-111">Type: **[**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span></span>

<span data-ttu-id="f3ec7-112">Detalhes do subobjeto flags analisado de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="f3ec7-112">Details of the flags subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3ec7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3ec7-113">Return value</span></span>

<span data-ttu-id="f3ec7-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="f3ec7-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ec7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3ec7-115">Requirements</span></span>



| <span data-ttu-id="f3ec7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3ec7-116">Requirement</span></span> | <span data-ttu-id="f3ec7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f3ec7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ec7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3ec7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f3ec7-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3ec7-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f3ec7-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3ec7-120">Library</span></span><br/> | <dl> <span data-ttu-id="f3ec7-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3ec7-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3ec7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f3ec7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="f3ec7-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3ec7-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ec7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3ec7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ec7-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f3ec7-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f3ec7-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="f3ec7-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="f3ec7-127">**\_Sinalizadores de \_ estado do pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="f3ec7-127">**D3D12\_PIPELINE\_STATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





