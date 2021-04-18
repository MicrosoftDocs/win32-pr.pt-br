---
title: Método ID3DX12PipelineParserCallbacks GSCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto do sombreador Geometry de um objeto que implementa essa interface.
ms.assetid: 0D8846C5-15E4-43EB-AA82-163BB514C5B7
keywords:
- Método GSCb
- Método GSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método GSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.GSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768e64ccdf06eccce731cafd0d40a9862b695e1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814558"
---
# <a name="id3dx12pipelineparsercallbacksgscb-method"></a><span data-ttu-id="98265-106">Método ID3DX12PipelineParserCallbacks:: GSCb</span><span class="sxs-lookup"><span data-stu-id="98265-106">ID3DX12PipelineParserCallbacks::GSCb method</span></span>

<span data-ttu-id="98265-107">Chama o retorno de chamada de subobjeto do sombreador Geometry de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="98265-107">Calls the geometry shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="98265-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98265-108">Syntax</span></span>


```C++
void GSCb(
  [ref] const D3D12_SHADER_BYTECODE &GS
);
```



## <a name="parameters"></a><span data-ttu-id="98265-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98265-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98265-110">*GS* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="98265-110">*GS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="98265-111">Tipo: **[**código de \_ \_ bytes do sombreador const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="98265-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="98265-112">Detalhes do subobjeto do sombreador Geometry analisado a partir de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="98265-112">Details of the geometry shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98265-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98265-113">Return value</span></span>

<span data-ttu-id="98265-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="98265-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="98265-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98265-115">Requirements</span></span>



| <span data-ttu-id="98265-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="98265-116">Requirement</span></span> | <span data-ttu-id="98265-117">Valor</span><span class="sxs-lookup"><span data-stu-id="98265-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="98265-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98265-118">Header</span></span><br/>  | <dl> <span data-ttu-id="98265-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="98265-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="98265-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98265-120">Library</span></span><br/> | <dl> <span data-ttu-id="98265-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98265-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="98265-122">DLL</span><span class="sxs-lookup"><span data-stu-id="98265-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="98265-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98265-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98265-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="98265-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98265-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="98265-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="98265-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="98265-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="98265-127">**\_Código de bytes do sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="98265-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





