---
description: Retorna o número de elementos na declaração de vértice.
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: Função D3DXGetDeclLength (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5576b4b86d5238d4942e09d605f695c66136799a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105766420"
---
# <a name="d3dxgetdecllength-function"></a><span data-ttu-id="d92e8-103">Função D3DXGetDeclLength</span><span class="sxs-lookup"><span data-stu-id="d92e8-103">D3DXGetDeclLength function</span></span>

<span data-ttu-id="d92e8-104">Retorna o número de elementos na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="d92e8-104">Returns the number of elements in the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d92e8-105">Syntax</span></span>


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a><span data-ttu-id="d92e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d92e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d92e8-107">*pDecl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d92e8-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92e8-108">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="d92e8-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="d92e8-109">Um ponteiro para a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="d92e8-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="d92e8-110">Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="d92e8-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d92e8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d92e8-111">Return value</span></span>

<span data-ttu-id="d92e8-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d92e8-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d92e8-113">O número de elementos na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="d92e8-113">The number of elements in the vertex declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d92e8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d92e8-114">Requirements</span></span>



| <span data-ttu-id="d92e8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d92e8-115">Requirement</span></span> | <span data-ttu-id="d92e8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d92e8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d92e8-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d92e8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d92e8-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d92e8-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d92e8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d92e8-119">Library</span></span><br/> | <dl> <span data-ttu-id="d92e8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d92e8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d92e8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d92e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92e8-122">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="d92e8-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
