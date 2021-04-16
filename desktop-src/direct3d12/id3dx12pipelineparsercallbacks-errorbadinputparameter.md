---
title: Método ID3DX12PipelineParserCallbacks ErrorBadInputParameter (D3DX12. h)
description: Chama o retorno de chamada de erro de parâmetro de entrada inadequado de um objeto que implementa essa interface.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Método ErrorBadInputParameter
- Método ErrorBadInputParameter, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método ErrorBadInputParameter
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808208"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a><span data-ttu-id="b8230-106">Método ID3DX12PipelineParserCallbacks:: ErrorBadInputParameter</span><span class="sxs-lookup"><span data-stu-id="b8230-106">ID3DX12PipelineParserCallbacks::ErrorBadInputParameter method</span></span>

<span data-ttu-id="b8230-107">Chama o retorno de chamada de erro de parâmetro de entrada inadequado de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="b8230-107">Calls the bad input parameter error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8230-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8230-108">Syntax</span></span>


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b8230-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8230-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8230-110">*ParameterIndex*</span><span class="sxs-lookup"><span data-stu-id="b8230-110">*ParameterIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="b8230-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b8230-111">Type: **UINT**</span></span>

<span data-ttu-id="b8230-112">A posição do parâmetro que contém entrada inadequada.</span><span class="sxs-lookup"><span data-stu-id="b8230-112">The position of the parameter that contains bad input.</span></span> <span data-ttu-id="b8230-113">O parâmetro mais à esquerda está na posição 1, não na posição 0.</span><span class="sxs-lookup"><span data-stu-id="b8230-113">The left-most parameter is at position 1, not position 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8230-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8230-114">Return value</span></span>

<span data-ttu-id="b8230-115">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="b8230-115">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8230-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8230-116">Requirements</span></span>



| <span data-ttu-id="b8230-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8230-117">Requirement</span></span> | <span data-ttu-id="b8230-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b8230-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8230-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8230-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b8230-120"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8230-120"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b8230-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8230-121">Library</span></span><br/> | <dl> <span data-ttu-id="b8230-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8230-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8230-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b8230-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8230-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8230-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8230-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8230-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8230-126">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b8230-126">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b8230-127">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b8230-127">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





