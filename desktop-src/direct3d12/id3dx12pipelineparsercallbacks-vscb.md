---
title: Método ID3DX12PipelineParserCallbacks VSCb (D3DX12. h)
description: Chama o retorno de chamada do subobjeto do sombreador de vértice de um objeto que implementa essa interface.
ms.assetid: 65A185B7-C790-4254-A3C5-EBBE9C38CA4E
keywords:
- Método VSCb
- Método VSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método VSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.VSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef9ab27b2f9fd4b93190e2eea453397de297013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765029"
---
# <a name="id3dx12pipelineparsercallbacksvscb-method"></a><span data-ttu-id="5fe8a-106">Método ID3DX12PipelineParserCallbacks:: VSCb</span><span class="sxs-lookup"><span data-stu-id="5fe8a-106">ID3DX12PipelineParserCallbacks::VSCb method</span></span>

<span data-ttu-id="5fe8a-107">Chama o retorno de chamada do subobjeto do sombreador de vértice de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-107">Calls the vertex shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fe8a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fe8a-108">Syntax</span></span>


```C++
void VSCb(
  [ref] const D3D12_SHADER_BYTECODE &VS
);
```



## <a name="parameters"></a><span data-ttu-id="5fe8a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fe8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fe8a-110">*Vs* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="5fe8a-110">*VS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe8a-111">Tipo: **[**código de \_ \_ bytes do sombreador const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="5fe8a-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="5fe8a-112">Detalhes do subobjeto do sombreador de vértice analisado a partir de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-112">Details of the vertex shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fe8a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fe8a-113">Return value</span></span>

<span data-ttu-id="5fe8a-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe8a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fe8a-115">Requirements</span></span>



| <span data-ttu-id="5fe8a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fe8a-116">Requirement</span></span> | <span data-ttu-id="5fe8a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5fe8a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe8a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fe8a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5fe8a-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fe8a-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5fe8a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fe8a-120">Library</span></span><br/> | <dl> <span data-ttu-id="5fe8a-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fe8a-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5fe8a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5fe8a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5fe8a-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fe8a-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fe8a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fe8a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe8a-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5fe8a-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5fe8a-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="5fe8a-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="5fe8a-127">**\_Código de bytes do sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5fe8a-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





