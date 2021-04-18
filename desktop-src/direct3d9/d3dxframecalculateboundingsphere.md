---
description: Computa a esfera delimitadora de todas as malhas na hierarquia de quadros.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: Função D3DXFrameCalculateBoundingSphere (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810804"
---
# <a name="d3dxframecalculateboundingsphere-function"></a><span data-ttu-id="9cd17-103">Função D3DXFrameCalculateBoundingSphere</span><span class="sxs-lookup"><span data-stu-id="9cd17-103">D3DXFrameCalculateBoundingSphere function</span></span>

<span data-ttu-id="9cd17-104">Computa a esfera delimitadora de todas as malhas na hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="9cd17-104">Computes the bounding sphere of all the meshes in the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd17-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cd17-105">Syntax</span></span>


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a><span data-ttu-id="9cd17-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cd17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cd17-107">*pFrameRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cd17-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd17-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="9cd17-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="9cd17-109">Ponteiro para o nó raiz.</span><span class="sxs-lookup"><span data-stu-id="9cd17-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="9cd17-110">*pObjectCenter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9cd17-110">*pObjectCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd17-111">Tipo: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="9cd17-111">Type: **[**LPD3DXVECTOR3**](d3dxvector3.md)**</span></span>

<span data-ttu-id="9cd17-112">Retorna o centro da esfera delimitadora.</span><span class="sxs-lookup"><span data-stu-id="9cd17-112">Returns the center of the bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="9cd17-113">*pObjectRadius* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9cd17-113">*pObjectRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd17-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9cd17-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9cd17-115">Retorna o raio da esfera delimitadora.</span><span class="sxs-lookup"><span data-stu-id="9cd17-115">Returns the radius of the bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cd17-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cd17-116">Return value</span></span>

<span data-ttu-id="9cd17-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9cd17-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9cd17-118">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9cd17-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9cd17-119">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9cd17-119">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd17-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cd17-120">Requirements</span></span>



| <span data-ttu-id="9cd17-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd17-121">Requirement</span></span> | <span data-ttu-id="9cd17-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9cd17-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd17-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cd17-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9cd17-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cd17-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9cd17-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cd17-125">Library</span></span><br/> | <dl> <span data-ttu-id="9cd17-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cd17-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9cd17-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cd17-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd17-128">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="9cd17-128">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
