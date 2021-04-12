---
description: Divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Função D3DXMatrixDecompose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173153"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="82551-103">Função D3DXMatrixDecompose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="82551-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="82551-104">Divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.</span><span class="sxs-lookup"><span data-stu-id="82551-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="82551-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82551-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="82551-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82551-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82551-107">*pOutScale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82551-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82551-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="82551-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="82551-109">Ponteiro para a saída [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que contém fatores de dimensionamento aplicados ao longo dos eixos x, y e z.</span><span class="sxs-lookup"><span data-stu-id="82551-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="82551-110">*pOutRotation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82551-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82551-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="82551-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="82551-112">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que descreve a rotação.</span><span class="sxs-lookup"><span data-stu-id="82551-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="82551-113">*pOutTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82551-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82551-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="82551-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="82551-115">Ponteiro para o vetor D3DXVECTOR3 que descreve a tradução.</span><span class="sxs-lookup"><span data-stu-id="82551-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="82551-116">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82551-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82551-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="82551-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="82551-118">Ponteiro para uma matriz [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de entrada para decompor.</span><span class="sxs-lookup"><span data-stu-id="82551-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82551-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82551-119">Return value</span></span>

<span data-ttu-id="82551-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82551-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82551-121">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="82551-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="82551-122">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="82551-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="82551-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82551-123">Requirements</span></span>



| <span data-ttu-id="82551-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="82551-124">Requirement</span></span> | <span data-ttu-id="82551-125">Valor</span><span class="sxs-lookup"><span data-stu-id="82551-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82551-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82551-126">Header</span></span><br/>  | <dl> <span data-ttu-id="82551-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="82551-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="82551-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82551-128">Library</span></span><br/> | <dl> <span data-ttu-id="82551-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82551-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82551-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="82551-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82551-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="82551-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
