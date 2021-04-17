---
title: Estrutura de CD3DX12_DEFAULT (D3dx12. h)
description: Passa \_ o padrão D3D12 para um construtor para cada estrutura auxiliar. Essa estrutura é simplesmente usada como um mecanismo para definir parâmetros padrão em outras estruturas auxiliares.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Estrutura de CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105748071"
---
# <a name="cd3dx12_default-structure"></a><span data-ttu-id="b2b1a-105">\_Estrutura padrão CD3DX12</span><span class="sxs-lookup"><span data-stu-id="b2b1a-105">CD3DX12\_DEFAULT structure</span></span>

<span data-ttu-id="b2b1a-106">Passa \_ o padrão D3D12 para um construtor para cada estrutura auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-106">Passes D3D12\_DEFAULT into a constructor for each helper structure.</span></span> <span data-ttu-id="b2b1a-107">Essa estrutura é simplesmente usada como um mecanismo para definir parâmetros padrão em outras estruturas auxiliares.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-107">This structure is simply used as a mechanism to set default parameters on the other helper structures.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b1a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2b1a-108">Remarks</span></span>

<span data-ttu-id="b2b1a-109">Essa estrutura é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b2b1a-109">This struct is declared as follows:</span></span>

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

<span data-ttu-id="b2b1a-110">Passa \_ o padrão D3D12 para um construtor para cada struct auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b2b1a-110">Passes D3D12\_DEFAULT into a constructor for each helper struct.</span></span> <span data-ttu-id="b2b1a-111">Por exemplo, o Construtor a seguir é declarado em d3dx12. h:</span><span class="sxs-lookup"><span data-stu-id="b2b1a-111">For example, the following constructor is declared in d3dx12.h:</span></span>

<span data-ttu-id="b2b1a-112">\_ \_ Identificador do descritor de CPU CD3DX12 \_ ( \_ padrão CD3DX12) {PTR = 0;}</span><span class="sxs-lookup"><span data-stu-id="b2b1a-112">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT) { ptr = 0; }</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b1a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b1a-113">Requirements</span></span>



| <span data-ttu-id="b2b1a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b1a-114">Requirement</span></span> | <span data-ttu-id="b2b1a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b2b1a-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b1a-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2b1a-116">Header</span></span><br/> | <dl> <span data-ttu-id="b2b1a-117"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b1a-117"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b1a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2b1a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b1a-119">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="b2b1a-119">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





