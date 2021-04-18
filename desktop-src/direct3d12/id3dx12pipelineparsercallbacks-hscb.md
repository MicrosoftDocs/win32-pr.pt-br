---
title: Método ID3DX12PipelineParserCallbacks HSCb (D3DX12. h)
description: Chama o retorno de chamada do subobjeto do sombreador envoltória de um objeto que implementa essa interface.
ms.assetid: B2967E7F-391F-4A76-A087-E0B925018EE3
keywords:
- Método HSCb
- Método HSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método HSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.HSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7d351e0b3827087cb51c38af173badd28d698c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105795446"
---
# <a name="id3dx12pipelineparsercallbackshscb-method"></a><span data-ttu-id="7500c-106">Método ID3DX12PipelineParserCallbacks:: HSCb</span><span class="sxs-lookup"><span data-stu-id="7500c-106">ID3DX12PipelineParserCallbacks::HSCb method</span></span>

<span data-ttu-id="7500c-107">Chama o retorno de chamada do subobjeto do sombreador envoltória de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="7500c-107">Calls the hull shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7500c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7500c-108">Syntax</span></span>


```C++
void HSCb(
  [ref] const D3D12_SHADER_BYTECODE &HS
);
```



## <a name="parameters"></a><span data-ttu-id="7500c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7500c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7500c-110">*HS* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="7500c-110">*HS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7500c-111">Tipo: **[**código de \_ \_ bytes do sombreador const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="7500c-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="7500c-112">Detalhes do subobjeto do sombreador envoltória analisado de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="7500c-112">Details of the hull shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7500c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7500c-113">Return value</span></span>

<span data-ttu-id="7500c-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="7500c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7500c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7500c-115">Requirements</span></span>



| <span data-ttu-id="7500c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7500c-116">Requirement</span></span> | <span data-ttu-id="7500c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7500c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7500c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7500c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7500c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7500c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="7500c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7500c-120">Library</span></span><br/> | <dl> <span data-ttu-id="7500c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7500c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="7500c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7500c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7500c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7500c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7500c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7500c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7500c-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7500c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7500c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="7500c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="7500c-127">**\_Código de bytes do sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7500c-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





