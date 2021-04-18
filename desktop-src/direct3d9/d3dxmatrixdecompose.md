---
description: Divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.
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
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781589"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="f71af-103">Função D3DXMatrixDecompose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f71af-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="f71af-104">Divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.</span><span class="sxs-lookup"><span data-stu-id="f71af-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f71af-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f71af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f71af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f71af-107">*pOutScale* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f71af-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f71af-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f71af-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f71af-109">Ponteiro para a saída [**D3DXVECTOR3**](d3dxvector3.md) que contém fatores de dimensionamento aplicados ao longo dos eixos x, y e z.</span><span class="sxs-lookup"><span data-stu-id="f71af-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="f71af-110">*pOutRotation* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f71af-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f71af-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f71af-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f71af-112">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que descreve a rotação.</span><span class="sxs-lookup"><span data-stu-id="f71af-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="f71af-113">*pOutTranslation* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f71af-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f71af-114">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f71af-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f71af-115">Ponteiro para o vetor [**D3DXVECTOR3**](d3dxvector3.md) que descreve a tradução.</span><span class="sxs-lookup"><span data-stu-id="f71af-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="f71af-116">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f71af-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f71af-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f71af-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f71af-118">Ponteiro para uma matriz [**D3DXMATRIX**](d3dxmatrix.md) de entrada para decompor.</span><span class="sxs-lookup"><span data-stu-id="f71af-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f71af-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f71af-119">Return value</span></span>

<span data-ttu-id="f71af-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f71af-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f71af-121">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f71af-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f71af-122">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f71af-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f71af-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f71af-123">Requirements</span></span>



| <span data-ttu-id="f71af-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f71af-124">Requirement</span></span> | <span data-ttu-id="f71af-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f71af-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f71af-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f71af-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f71af-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71af-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f71af-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f71af-128">Library</span></span><br/> | <dl> <span data-ttu-id="f71af-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f71af-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f71af-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f71af-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71af-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f71af-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




