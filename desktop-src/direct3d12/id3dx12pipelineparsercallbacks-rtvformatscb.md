---
title: Método ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de matriz de formato de destino de renderização de um objeto que implementa essa interface.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Método RTVFormatsCb
- Método RTVFormatsCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método RTVFormatsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790388"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a><span data-ttu-id="9ca52-106">Método ID3DX12PipelineParserCallbacks:: RTVFormatsCb</span><span class="sxs-lookup"><span data-stu-id="9ca52-106">ID3DX12PipelineParserCallbacks::RTVFormatsCb method</span></span>

<span data-ttu-id="9ca52-107">Chama o retorno de chamada de subobjeto de matriz de formato de destino de renderização de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="9ca52-107">Calls the render target format array subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca52-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ca52-108">Syntax</span></span>


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a><span data-ttu-id="9ca52-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ca52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ca52-110">*RTVFormats* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="9ca52-110">*RTVFormats* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9ca52-111">Tipo: **[**matriz de \_ \_ formato \_ const D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span><span class="sxs-lookup"><span data-stu-id="9ca52-111">Type: **const [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span></span>

<span data-ttu-id="9ca52-112">Detalhes do subobjeto de matriz de formato de destino de renderização analisado de um fluxo de estado de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ca52-112">Details of the render target format array subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ca52-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ca52-113">Return value</span></span>

<span data-ttu-id="9ca52-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="9ca52-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca52-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ca52-115">Requirements</span></span>



| <span data-ttu-id="9ca52-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ca52-116">Requirement</span></span> | <span data-ttu-id="9ca52-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9ca52-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca52-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ca52-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9ca52-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ca52-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="9ca52-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ca52-120">Library</span></span><br/> | <dl> <span data-ttu-id="9ca52-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ca52-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ca52-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9ca52-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ca52-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ca52-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca52-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ca52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca52-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9ca52-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="9ca52-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="9ca52-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="9ca52-127">**\_Matriz de \_ formato D3D12 RT \_**</span><span class="sxs-lookup"><span data-stu-id="9ca52-127">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





