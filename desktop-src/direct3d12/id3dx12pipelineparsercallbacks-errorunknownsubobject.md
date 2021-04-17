---
title: Método ID3DX12PipelineParserCallbacks ErrorUnknownSubobject (D3DX12. h)
description: Chama o retorno de chamada de erro de subobjeto desconhecido de um objeto que implementa essa interface.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Método ErrorUnknownSubobject
- Método ErrorUnknownSubobject, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método ErrorUnknownSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812317"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a><span data-ttu-id="4714c-106">Método ID3DX12PipelineParserCallbacks:: ErrorUnknownSubobject</span><span class="sxs-lookup"><span data-stu-id="4714c-106">ID3DX12PipelineParserCallbacks::ErrorUnknownSubobject method</span></span>

<span data-ttu-id="4714c-107">Chama o retorno de chamada de erro de subobjeto desconhecido de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="4714c-107">Calls the unknown subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4714c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4714c-108">Syntax</span></span>


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a><span data-ttu-id="4714c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4714c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4714c-110">*Não knownTypevalue*</span><span class="sxs-lookup"><span data-stu-id="4714c-110">*UnknownTypeValue*</span></span> 
</dt> <dd>

<span data-ttu-id="4714c-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4714c-111">Type: **UINT**</span></span>

<span data-ttu-id="4714c-112">O tipo de subobjeto não reconhecido do subobjeto tentado.</span><span class="sxs-lookup"><span data-stu-id="4714c-112">The unrecognized subobject type of the attempted subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4714c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4714c-113">Return value</span></span>

<span data-ttu-id="4714c-114">Não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="4714c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4714c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4714c-115">Requirements</span></span>



| <span data-ttu-id="4714c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4714c-116">Requirement</span></span> | <span data-ttu-id="4714c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4714c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4714c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4714c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4714c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4714c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="4714c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4714c-120">Library</span></span><br/> | <dl> <span data-ttu-id="4714c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4714c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="4714c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4714c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4714c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4714c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4714c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4714c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4714c-125">Interfaces auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4714c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4714c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="4714c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





