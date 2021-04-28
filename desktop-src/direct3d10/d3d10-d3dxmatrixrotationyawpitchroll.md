---
description: Função D3DXMatrixRotationYawPitchRoll (D3DX10Math. h) – compila uma matriz com uma guinada, uma densidade e um rolo especificados.
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
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108944"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="1bda0-103">Função D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1bda0-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="1bda0-104">Cria uma matriz com uma guinada, pitch e roll especificados.</span><span class="sxs-lookup"><span data-stu-id="1bda0-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bda0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bda0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="1bda0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bda0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bda0-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1bda0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bda0-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bda0-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1bda0-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1bda0-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1bda0-110">*Guinada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1bda0-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bda0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bda0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bda0-112">Desvio em volta do eixo y, em radianos.</span><span class="sxs-lookup"><span data-stu-id="1bda0-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="1bda0-113">*Pitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1bda0-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bda0-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bda0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bda0-115">Inclinação em relação ao eixo x, em radianos.</span><span class="sxs-lookup"><span data-stu-id="1bda0-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="1bda0-116">*Rolar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1bda0-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bda0-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bda0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bda0-118">Sobreponha-se ao eixo z, em radianos.</span><span class="sxs-lookup"><span data-stu-id="1bda0-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bda0-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1bda0-119">Return value</span></span>

<span data-ttu-id="1bda0-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bda0-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1bda0-121">Ponteiro para uma estrutura D3DXMATRIX com a guinada, a densidade e o rolo especificados.</span><span class="sxs-lookup"><span data-stu-id="1bda0-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bda0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bda0-122">Remarks</span></span>

<span data-ttu-id="1bda0-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="1bda0-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1bda0-124">Dessa forma, a função D3DXMatrixRotationYawPitchRoll pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1bda0-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1bda0-125">A ordem das transformações é revertida primeiro, depois de pitch e depois da guinada.</span><span class="sxs-lookup"><span data-stu-id="1bda0-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="1bda0-126">Em relação ao eixo de coordenadas local do objeto, isso equivale à rotação em volta do eixo z, seguido pela rotação em volta do eixo x, seguido pela rotação em volta do eixo y, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="1bda0-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![ilustração de roll, pitch e guinada como rotações em volta dos três eixos](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="1bda0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bda0-128">Requirements</span></span>



| <span data-ttu-id="1bda0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bda0-129">Requirement</span></span> | <span data-ttu-id="1bda0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1bda0-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bda0-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bda0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1bda0-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bda0-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1bda0-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1bda0-133">Library</span></span><br/> | <dl> <span data-ttu-id="1bda0-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bda0-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bda0-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1bda0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bda0-136">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1bda0-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
