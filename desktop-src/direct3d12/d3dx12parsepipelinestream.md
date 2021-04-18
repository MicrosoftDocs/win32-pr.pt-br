---
title: Função D3DX12ParsePipelineStream (D3dx12. h)
description: Analisa uma descrição de fluxo de estado de pipeline, chamando um retorno de chamada definido pelo usuário para cada instância de subobjeto analisada.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- Função D3DX12ParsePipelineStream
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814596"
---
# <a name="d3dx12parsepipelinestream-function"></a><span data-ttu-id="fb413-104">Função D3DX12ParsePipelineStream</span><span class="sxs-lookup"><span data-stu-id="fb413-104">D3DX12ParsePipelineStream function</span></span>

<span data-ttu-id="fb413-105">Analisa uma descrição de fluxo de estado de pipeline, chamando um retorno de chamada definido pelo usuário para cada instância de subobjeto analisada.</span><span class="sxs-lookup"><span data-stu-id="fb413-105">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb413-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb413-106">Syntax</span></span>


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a><span data-ttu-id="fb413-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb413-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb413-108">*Desc* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="fb413-108">*Desc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fb413-109">Tipo: **const [**D3D12 \_ pipeline \_ State \_ Stream \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span><span class="sxs-lookup"><span data-stu-id="fb413-109">Type: **const [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span></span>

<span data-ttu-id="fb413-110">A descrição do fluxo de estado do pipeline para analisar.</span><span class="sxs-lookup"><span data-stu-id="fb413-110">The pipeline state stream description to parse.</span></span>

</dd> <dt>

<span data-ttu-id="fb413-111">*pCallbacks*</span><span class="sxs-lookup"><span data-stu-id="fb413-111">*pCallbacks*</span></span> 
</dt> <dd>

<span data-ttu-id="fb413-112">Tipo: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb413-112">Type: **[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span></span>

<span data-ttu-id="fb413-113">Uma estrutura que especifica os retornos de chamada a serem chamados para cada tipo de subobjeto e retornos de chamada adicionais para chamar no caso de um erro de análise.</span><span class="sxs-lookup"><span data-stu-id="fb413-113">A structure that specifies the callbacks to call for each subobject type and additional callbacks to call in the event of a parsing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb413-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb413-114">Return value</span></span>

<span data-ttu-id="fb413-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb413-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb413-116">Esse método retorna um erro HRESULT Success (**S \_ OK** ou **E \_ INVALIDARG** se um tipo de subobjeto desconhecido for encontrado, se a descrição do fluxo estiver vazia, nula ou contiver subobjetos duplicados (incluindo subobjetos derivados) ou se *pCallbacks* for nulo.</span><span class="sxs-lookup"><span data-stu-id="fb413-116">This method returns an HRESULT success (**S\_OK** or **E\_INVALIDARG** error if an unknown subobject type is encountered, if the stream description is empty, null, or contains duplicate subobjects (including derived subobjects), or if *pCallbacks* is null.</span></span> <span data-ttu-id="fb413-117">Em cada caso em que E \_ INVALIDARG é retornado, um retorno de chamada correspondente é chamado primeiro.</span><span class="sxs-lookup"><span data-stu-id="fb413-117">In each case that E\_INVALIDARG is returned, a corresponding callback is first called.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb413-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb413-118">Requirements</span></span>



| <span data-ttu-id="fb413-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb413-119">Requirement</span></span> | <span data-ttu-id="fb413-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fb413-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb413-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb413-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fb413-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb413-122"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="fb413-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb413-123">Library</span></span><br/> | <dl> <span data-ttu-id="fb413-124"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb413-124"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb413-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fb413-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb413-126"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb413-126"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb413-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb413-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb413-128">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="fb413-128">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





