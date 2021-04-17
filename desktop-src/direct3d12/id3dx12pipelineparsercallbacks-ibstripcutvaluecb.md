---
title: Método ID3DX12PipelineParserCallbacks IBStripCutValueCb (D3DX12. h)
description: Chama o retorno de chamada da faixa do buffer de índice-recortar valor do subobjeto de um objeto que implementa essa interface.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Método IBStripCutValueCb
- Método IBStripCutValueCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método IBStripCutValueCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798272"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a><span data-ttu-id="8bbac-106">Método ID3DX12PipelineParserCallbacks:: IBStripCutValueCb</span><span class="sxs-lookup"><span data-stu-id="8bbac-106">ID3DX12PipelineParserCallbacks::IBStripCutValueCb method</span></span>

<span data-ttu-id="8bbac-107">Chama o retorno de chamada da faixa do buffer de índice-recortar valor do subobjeto de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="8bbac-107">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bbac-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bbac-108">Syntax</span></span>


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a><span data-ttu-id="8bbac-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bbac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bbac-110">*IBStripCutValue*</span><span class="sxs-lookup"><span data-stu-id="8bbac-110">*IBStripCutValue*</span></span> 
</dt> <dd>

<span data-ttu-id="8bbac-111">Tipo: **[ **\_ valor de \_ \_ \_ recorte \_ da faixa de buffer do índice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span><span class="sxs-lookup"><span data-stu-id="8bbac-111">Type: **[**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span></span>

<span data-ttu-id="8bbac-112">Detalhes da faixa do buffer de índice – recortar valor do subobjeto analisado de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8bbac-112">Details of the index buffer strip-cut value subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bbac-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8bbac-113">Return value</span></span>

<span data-ttu-id="8bbac-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="8bbac-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bbac-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bbac-115">Requirements</span></span>



| <span data-ttu-id="8bbac-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bbac-116">Requirement</span></span> | <span data-ttu-id="8bbac-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8bbac-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8bbac-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8bbac-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8bbac-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bbac-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8bbac-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bbac-120">Library</span></span><br/> | <dl> <span data-ttu-id="8bbac-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bbac-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8bbac-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8bbac-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8bbac-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bbac-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bbac-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bbac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bbac-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8bbac-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8bbac-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8bbac-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="8bbac-127">**\_Valor de \_ \_ \_ recorte de faixa de buffer de índice D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8bbac-127">**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





