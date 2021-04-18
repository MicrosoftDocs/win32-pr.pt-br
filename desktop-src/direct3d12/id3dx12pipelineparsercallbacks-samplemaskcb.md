---
title: Método ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de máscara de exemplo de um objeto que implementa essa interface.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Método SampleMaskCb
- Método SampleMaskCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método SampleMaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791281"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a><span data-ttu-id="9a65f-106">Método ID3DX12PipelineParserCallbacks:: SampleMaskCb</span><span class="sxs-lookup"><span data-stu-id="9a65f-106">ID3DX12PipelineParserCallbacks::SampleMaskCb method</span></span>

<span data-ttu-id="9a65f-107">Chama o retorno de chamada de subobjeto de máscara de exemplo de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="9a65f-107">Calls the sample mask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a65f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a65f-108">Syntax</span></span>


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a><span data-ttu-id="9a65f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a65f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a65f-110">*SampleMask*</span><span class="sxs-lookup"><span data-stu-id="9a65f-110">*SampleMask*</span></span> 
</dt> <dd>

<span data-ttu-id="9a65f-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9a65f-111">Type: **UINT**</span></span>

<span data-ttu-id="9a65f-112">Detalhes do subobjeto de máscara de exemplo analisado de um fluxo de estado de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a65f-112">Details of the sample mask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a65f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a65f-113">Return value</span></span>

<span data-ttu-id="9a65f-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="9a65f-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a65f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a65f-115">Requirements</span></span>



| <span data-ttu-id="9a65f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a65f-116">Requirement</span></span> | <span data-ttu-id="9a65f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9a65f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9a65f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a65f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9a65f-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a65f-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="9a65f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a65f-120">Library</span></span><br/> | <dl> <span data-ttu-id="9a65f-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a65f-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="9a65f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9a65f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a65f-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a65f-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a65f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a65f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a65f-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9a65f-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="9a65f-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="9a65f-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





