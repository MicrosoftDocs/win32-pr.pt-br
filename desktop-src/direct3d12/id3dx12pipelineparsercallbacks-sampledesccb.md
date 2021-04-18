---
title: Método ID3DX12PipelineParserCallbacks SampleDescCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de descrição de exemplo de um objeto que implementa essa interface.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Método SampleDescCb
- Método SampleDescCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método SampleDescCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802103"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a><span data-ttu-id="8f4ee-106">Método ID3DX12PipelineParserCallbacks:: SampleDescCb</span><span class="sxs-lookup"><span data-stu-id="8f4ee-106">ID3DX12PipelineParserCallbacks::SampleDescCb method</span></span>

<span data-ttu-id="8f4ee-107">Chama o retorno de chamada de subobjeto de descrição de exemplo de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="8f4ee-107">Calls the sample description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f4ee-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f4ee-108">Syntax</span></span>


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a><span data-ttu-id="8f4ee-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f4ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f4ee-110">*SampleDesc* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="8f4ee-110">*SampleDesc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8f4ee-111">Tipo: **const [**dxgi \_ amostra \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span><span class="sxs-lookup"><span data-stu-id="8f4ee-111">Type: **const [**DXGI\_SAMPLE\_DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span></span>

<span data-ttu-id="8f4ee-112">Detalhes do subobjeto de descrição de exemplo analisado a partir de um fluxo de estado de pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f4ee-112">Details of the sample description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f4ee-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f4ee-113">Return value</span></span>

<span data-ttu-id="8f4ee-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="8f4ee-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f4ee-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f4ee-115">Requirements</span></span>



| <span data-ttu-id="8f4ee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f4ee-116">Requirement</span></span> | <span data-ttu-id="8f4ee-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8f4ee-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8f4ee-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f4ee-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8f4ee-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f4ee-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8f4ee-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f4ee-120">Library</span></span><br/> | <dl> <span data-ttu-id="8f4ee-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f4ee-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8f4ee-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8f4ee-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8f4ee-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f4ee-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f4ee-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f4ee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f4ee-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8f4ee-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8f4ee-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8f4ee-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="8f4ee-127">**\_desc de exemplo de dxgi \_**</span><span class="sxs-lookup"><span data-stu-id="8f4ee-127">**DXGI\_SAMPLE\_DESC**</span></span>](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

