---
title: Método ID3DX12PipelineParserCallbacks NodemaskCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto nodemask de um objeto que implementa essa interface.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Método NodemaskCb
- Método NodemaskCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método NodemaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812089"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a><span data-ttu-id="d091f-106">Método ID3DX12PipelineParserCallbacks:: NodemaskCb</span><span class="sxs-lookup"><span data-stu-id="d091f-106">ID3DX12PipelineParserCallbacks::NodemaskCb method</span></span>

<span data-ttu-id="d091f-107">Chama o retorno de chamada de subobjeto nodemask de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="d091f-107">Calls the nodemask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d091f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d091f-108">Syntax</span></span>


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a><span data-ttu-id="d091f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d091f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d091f-110">*Nodemask*</span><span class="sxs-lookup"><span data-stu-id="d091f-110">*Nodemask*</span></span> 
</dt> <dd>

<span data-ttu-id="d091f-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d091f-111">Type: **UINT**</span></span>

<span data-ttu-id="d091f-112">Detalhes do subobjeto nodemask analisado de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="d091f-112">Details of the nodemask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d091f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d091f-113">Return value</span></span>

<span data-ttu-id="d091f-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="d091f-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d091f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d091f-115">Requirements</span></span>



| <span data-ttu-id="d091f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d091f-116">Requirement</span></span> | <span data-ttu-id="d091f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d091f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d091f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d091f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d091f-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d091f-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d091f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d091f-120">Library</span></span><br/> | <dl> <span data-ttu-id="d091f-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d091f-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d091f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d091f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d091f-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d091f-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d091f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d091f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d091f-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d091f-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d091f-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d091f-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





