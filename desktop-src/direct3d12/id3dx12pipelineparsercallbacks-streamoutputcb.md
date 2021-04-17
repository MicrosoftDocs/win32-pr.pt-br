---
title: Método ID3DX12PipelineParserCallbacks StreamOutputCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de descrição de saída de fluxo de um objeto que implementa essa interface.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Método StreamOutputCb
- Método StreamOutputCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método StreamOutputCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791341"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a><span data-ttu-id="b6c6b-106">Método ID3DX12PipelineParserCallbacks:: StreamOutputCb</span><span class="sxs-lookup"><span data-stu-id="b6c6b-106">ID3DX12PipelineParserCallbacks::StreamOutputCb method</span></span>

<span data-ttu-id="b6c6b-107">Chama o retorno de chamada de subobjeto de descrição de saída de fluxo de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="b6c6b-107">Calls the stream output description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c6b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6c6b-108">Syntax</span></span>


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a><span data-ttu-id="b6c6b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6c6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c6b-110">*StreamOutput* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="b6c6b-110">*StreamOutput* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c6b-111">Tipo: **const [**D3D12 \_ saída de fluxo \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span><span class="sxs-lookup"><span data-stu-id="b6c6b-111">Type: **const [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span></span>

<span data-ttu-id="b6c6b-112">Detalhes do subobjeto de descrição de saída do fluxo analisado a partir de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6c6b-112">Details of the stream output description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c6b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6c6b-113">Return value</span></span>

<span data-ttu-id="b6c6b-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="b6c6b-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c6b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6c6b-115">Requirements</span></span>



| <span data-ttu-id="b6c6b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c6b-116">Requirement</span></span> | <span data-ttu-id="b6c6b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b6c6b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c6b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6c6b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b6c6b-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c6b-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b6c6b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6c6b-120">Library</span></span><br/> | <dl> <span data-ttu-id="b6c6b-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6c6b-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6c6b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b6c6b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b6c6b-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6c6b-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c6b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6c6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c6b-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b6c6b-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b6c6b-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b6c6b-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b6c6b-127">**\_Desc de \_ saída de fluxo D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b6c6b-127">**D3D12\_STREAM\_OUTPUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





