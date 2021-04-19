---
description: Gera uma declaração de vértice de saída da declaração de entrada. A declaração de saída destina-se ao uso pelas funções de mosaico de malha.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: Função D3DXGenerateOutputDecl (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798166"
---
# <a name="d3dxgenerateoutputdecl-function"></a><span data-ttu-id="68a84-104">Função D3DXGenerateOutputDecl</span><span class="sxs-lookup"><span data-stu-id="68a84-104">D3DXGenerateOutputDecl function</span></span>

<span data-ttu-id="68a84-105">Gera uma declaração de vértice de saída da declaração de entrada.</span><span class="sxs-lookup"><span data-stu-id="68a84-105">Generates an output vertex declaration from the input declaration.</span></span> <span data-ttu-id="68a84-106">A declaração de saída destina-se ao uso pelas funções de mosaico de malha.</span><span class="sxs-lookup"><span data-stu-id="68a84-106">The output declaration is intended for use by the mesh tessellation functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a84-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68a84-107">Syntax</span></span>


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="68a84-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68a84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a84-109">*pOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68a84-109">*pOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68a84-110">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span><span class="sxs-lookup"><span data-stu-id="68a84-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="68a84-111">Ponteiro para a declaração de vértice de saída.</span><span class="sxs-lookup"><span data-stu-id="68a84-111">Pointer to the output vertex declaration.</span></span> <span data-ttu-id="68a84-112">Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="68a84-112">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="68a84-113">*pInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68a84-113">*pInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68a84-114">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="68a84-114">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="68a84-115">Ponteiro para a declaração de vértice de entrada.</span><span class="sxs-lookup"><span data-stu-id="68a84-115">Pointer to the input vertex declaration.</span></span> <span data-ttu-id="68a84-116">Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="68a84-116">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a84-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68a84-117">Return value</span></span>

<span data-ttu-id="68a84-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68a84-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68a84-119">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="68a84-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="68a84-120">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="68a84-120">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="68a84-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68a84-121">Requirements</span></span>



| <span data-ttu-id="68a84-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="68a84-122">Requirement</span></span> | <span data-ttu-id="68a84-123">Valor</span><span class="sxs-lookup"><span data-stu-id="68a84-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68a84-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68a84-124">Header</span></span><br/>  | <dl> <span data-ttu-id="68a84-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="68a84-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="68a84-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68a84-126">Library</span></span><br/> | <dl> <span data-ttu-id="68a84-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68a84-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68a84-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="68a84-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a84-129">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="68a84-129">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




