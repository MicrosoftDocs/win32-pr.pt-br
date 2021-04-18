---
title: Função D3DX12GetBaseSubobjectType (D3dx12. h)
description: Retorna o tipo de subobjeto que corresponde à classe base do tipo de subobjeto passado.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- Função D3DX12GetBaseSubobjectType
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771477"
---
# <a name="d3dx12getbasesubobjecttype-function"></a><span data-ttu-id="d85e0-104">Função D3DX12GetBaseSubobjectType</span><span class="sxs-lookup"><span data-stu-id="d85e0-104">D3DX12GetBaseSubobjectType function</span></span>

<span data-ttu-id="d85e0-105">Retorna o tipo de subobjeto que corresponde à classe base do tipo de subobjeto passado.</span><span class="sxs-lookup"><span data-stu-id="d85e0-105">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d85e0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d85e0-106">Syntax</span></span>


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a><span data-ttu-id="d85e0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d85e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d85e0-108">*Subobjecttype*</span><span class="sxs-lookup"><span data-stu-id="d85e0-108">*SubobjectType*</span></span> 
</dt> <dd>

<span data-ttu-id="d85e0-109">Tipo: **\_ \_ \_ \_ tipo de subobjeto de estado de pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="d85e0-109">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="d85e0-110">Um valor de enumeração que especifica o tipo de subobjeto no qual você está interessado.</span><span class="sxs-lookup"><span data-stu-id="d85e0-110">An enumeration value that specifies the subobject type that you're interested in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d85e0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d85e0-111">Return value</span></span>

<span data-ttu-id="d85e0-112">Tipo: **\_ \_ \_ \_ tipo de subobjeto de estado de pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="d85e0-112">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="d85e0-113">Se *subobjecttype* corresponder a um tipo de dados de subobjeto derivado de outro tipo de dados de subobjeto, o tipo de subobjeto do tipo de dados de subobjeto base será retornado; caso contrário, o tipo de subobjeto passado é retornado.</span><span class="sxs-lookup"><span data-stu-id="d85e0-113">If *SubobjectType* corresponds to a subobject data type that is derived from another subobject data type, the subobject type of the base subobject data type is returned; otherwise, the passed-in subobject type is returned.</span></span> <span data-ttu-id="d85e0-114">Por exemplo, se **D3D12 \_ \_ profundidade de \_ tipo de subobjeto \_ \_ \_ STENCIL1** for passado, o **\_ \_ \_ \_ \_ \_ estêncil profundidade de tipo de subobjeto do estado do pipeline D3D12** será retornado.</span><span class="sxs-lookup"><span data-stu-id="d85e0-114">For example, if **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** is passed in, then **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="d85e0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d85e0-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d85e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d85e0-116">Requirements</span></span>



| <span data-ttu-id="d85e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d85e0-117">Requirement</span></span> | <span data-ttu-id="d85e0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d85e0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d85e0-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d85e0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d85e0-120"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d85e0-120"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d85e0-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d85e0-121">Library</span></span><br/> | <dl> <span data-ttu-id="d85e0-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d85e0-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d85e0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d85e0-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="d85e0-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d85e0-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d85e0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d85e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d85e0-126">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="d85e0-126">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





