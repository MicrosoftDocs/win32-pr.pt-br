---
description: Função D3DXMatrixDecompose (D3dx9math. h) – divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Função D3DXMatrixDecompose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aaaa1059c4ffeafa453694d9c348656c856decaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098184"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="7c7b8-103">Função D3DXMatrixDecompose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7c7b8-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="7c7b8-104">Divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.</span><span class="sxs-lookup"><span data-stu-id="7c7b8-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c7b8-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="7c7b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c7b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c7b8-107">*pOutScale* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7c7b8-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7b8-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c7b8-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7c7b8-109">Ponteiro para a saída [**D3DXVECTOR3**](d3dxvector3.md) que contém fatores de dimensionamento aplicados ao longo dos eixos x, y e z.</span><span class="sxs-lookup"><span data-stu-id="7c7b8-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="7c7b8-110">*pOutRotation* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7c7b8-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7b8-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c7b8-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7c7b8-112">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que descreve a rotação.</span><span class="sxs-lookup"><span data-stu-id="7c7b8-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="7c7b8-113">*pOutTranslation* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7c7b8-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7b8-114">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c7b8-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7c7b8-115">Ponteiro para o vetor [**D3DXVECTOR3**](d3dxvector3.md) que descreve a tradução.</span><span class="sxs-lookup"><span data-stu-id="7c7b8-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="7c7b8-116">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c7b8-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7b8-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c7b8-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c7b8-118">Ponteiro para uma matriz [**D3DXMATRIX**](d3dxmatrix.md) de entrada para decompor.</span><span class="sxs-lookup"><span data-stu-id="7c7b8-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c7b8-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7c7b8-119">Return value</span></span>

<span data-ttu-id="7c7b8-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c7b8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c7b8-121">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c7b8-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7c7b8-122">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7c7b8-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c7b8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c7b8-123">Requirements</span></span>



| <span data-ttu-id="7c7b8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c7b8-124">Requirement</span></span> | <span data-ttu-id="7c7b8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7c7b8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c7b8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c7b8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7c7b8-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c7b8-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7c7b8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c7b8-128">Library</span></span><br/> | <dl> <span data-ttu-id="7c7b8-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c7b8-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c7b8-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7c7b8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c7b8-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="7c7b8-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




