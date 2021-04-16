---
title: Método ID3DX12PipelineParserCallbacks InputLayoutCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de layout de entrada de um objeto que implementa essa interface.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Método InputLayoutCb
- Método InputLayoutCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método InputLayoutCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc28276ef893247577cf41de8f4aba5582c101d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765138"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a><span data-ttu-id="73431-106">Método ID3DX12PipelineParserCallbacks:: InputLayoutCb</span><span class="sxs-lookup"><span data-stu-id="73431-106">ID3DX12PipelineParserCallbacks::InputLayoutCb method</span></span>

<span data-ttu-id="73431-107">Chama o retorno de chamada de subobjeto de layout de entrada de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="73431-107">Calls the input layout subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="73431-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73431-108">Syntax</span></span>


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a><span data-ttu-id="73431-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73431-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73431-110">*InputLayout* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="73431-110">*InputLayout* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="73431-111">Tipo: **const [**D3D12 \_ layout de entrada \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span><span class="sxs-lookup"><span data-stu-id="73431-111">Type: **const [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span></span>

<span data-ttu-id="73431-112">Detalhes do subobjeto de layout de entrada analisado de um fluxo de estado de pipeline.</span><span class="sxs-lookup"><span data-stu-id="73431-112">Details of the input layout subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73431-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73431-113">Return value</span></span>

<span data-ttu-id="73431-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="73431-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="73431-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73431-115">Requirements</span></span>



| <span data-ttu-id="73431-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="73431-116">Requirement</span></span> | <span data-ttu-id="73431-117">Valor</span><span class="sxs-lookup"><span data-stu-id="73431-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="73431-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73431-118">Header</span></span><br/>  | <dl> <span data-ttu-id="73431-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="73431-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="73431-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73431-120">Library</span></span><br/> | <dl> <span data-ttu-id="73431-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73431-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="73431-122">DLL</span><span class="sxs-lookup"><span data-stu-id="73431-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="73431-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73431-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73431-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="73431-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73431-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="73431-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="73431-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="73431-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="73431-127">**D3D12 \_ de \_ layout de entrada \_ desc**</span><span class="sxs-lookup"><span data-stu-id="73431-127">**D3D12\_INPUT\_LAYOUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





