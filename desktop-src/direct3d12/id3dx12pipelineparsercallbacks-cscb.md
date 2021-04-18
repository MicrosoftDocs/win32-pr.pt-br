---
title: Método ID3DX12PipelineParserCallbacks CSCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto do sombreador de computação de um objeto que implementa essa interface.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Método CSCb
- Método CSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método CSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813728"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a><span data-ttu-id="7069c-106">Método ID3DX12PipelineParserCallbacks:: CSCb</span><span class="sxs-lookup"><span data-stu-id="7069c-106">ID3DX12PipelineParserCallbacks::CSCb method</span></span>

<span data-ttu-id="7069c-107">Chama o retorno de chamada de subobjeto do sombreador de computação de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="7069c-107">Calls the compute shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7069c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7069c-108">Syntax</span></span>


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a><span data-ttu-id="7069c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7069c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7069c-110">*Cs* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="7069c-110">*CS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7069c-111">Tipo: **[**código de \_ \_ bytes do sombreador const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="7069c-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="7069c-112">Detalhes do subobjeto do sombreador de computação analisado a partir de um fluxo de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="7069c-112">Details of the compute shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7069c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7069c-113">Return value</span></span>

<span data-ttu-id="7069c-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="7069c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7069c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7069c-115">Requirements</span></span>



| <span data-ttu-id="7069c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7069c-116">Requirement</span></span> | <span data-ttu-id="7069c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7069c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7069c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7069c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7069c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7069c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="7069c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7069c-120">Library</span></span><br/> | <dl> <span data-ttu-id="7069c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7069c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="7069c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7069c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7069c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7069c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7069c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7069c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7069c-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7069c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7069c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="7069c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="7069c-127">**\_Código de bytes do sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7069c-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





