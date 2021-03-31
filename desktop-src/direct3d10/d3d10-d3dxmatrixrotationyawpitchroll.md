---
description: Cria uma matriz com uma guinada, pitch e roll especificados.
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: Função D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d65242f49ee94394337f43555c3e154141e3b642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930722"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="625ff-103">Função D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="625ff-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="625ff-104">Cria uma matriz com uma guinada, pitch e roll especificados.</span><span class="sxs-lookup"><span data-stu-id="625ff-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="625ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="625ff-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="625ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="625ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="625ff-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="625ff-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="625ff-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="625ff-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="625ff-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="625ff-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="625ff-110">*Guinada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="625ff-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="625ff-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="625ff-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="625ff-112">Desvio em volta do eixo y, em radianos.</span><span class="sxs-lookup"><span data-stu-id="625ff-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="625ff-113">*Pitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="625ff-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="625ff-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="625ff-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="625ff-115">Inclinação em relação ao eixo x, em radianos.</span><span class="sxs-lookup"><span data-stu-id="625ff-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="625ff-116">*Rolar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="625ff-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="625ff-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="625ff-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="625ff-118">Sobreponha-se ao eixo z, em radianos.</span><span class="sxs-lookup"><span data-stu-id="625ff-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="625ff-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="625ff-119">Return value</span></span>

<span data-ttu-id="625ff-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="625ff-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="625ff-121">Ponteiro para uma estrutura D3DXMATRIX com a guinada, a densidade e o rolo especificados.</span><span class="sxs-lookup"><span data-stu-id="625ff-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="625ff-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="625ff-122">Remarks</span></span>

<span data-ttu-id="625ff-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="625ff-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="625ff-124">Dessa forma, a função D3DXMatrixRotationYawPitchRoll pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="625ff-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="625ff-125">A ordem das transformações é revertida primeiro, depois de pitch e depois da guinada.</span><span class="sxs-lookup"><span data-stu-id="625ff-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="625ff-126">Em relação ao eixo de coordenadas local do objeto, isso equivale à rotação em volta do eixo z, seguido pela rotação em volta do eixo x, seguido pela rotação em volta do eixo y, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="625ff-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![ilustração de roll, pitch e guinada como rotações em volta dos três eixos](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="625ff-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="625ff-128">Requirements</span></span>



| <span data-ttu-id="625ff-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="625ff-129">Requirement</span></span> | <span data-ttu-id="625ff-130">Valor</span><span class="sxs-lookup"><span data-stu-id="625ff-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="625ff-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="625ff-131">Header</span></span><br/>  | <dl> <span data-ttu-id="625ff-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="625ff-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="625ff-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="625ff-133">Library</span></span><br/> | <dl> <span data-ttu-id="625ff-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="625ff-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="625ff-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="625ff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="625ff-136">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="625ff-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
