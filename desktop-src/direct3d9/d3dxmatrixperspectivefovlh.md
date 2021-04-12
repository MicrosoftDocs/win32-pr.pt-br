---
description: Cria uma matriz de projeção de perspectiva à esquerda com base em um campo de visão.
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: Função D3DXMatrixPerspectiveFovLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91b25a2e319236485c2c290b55acb94954a4791d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173123"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a><span data-ttu-id="f0fcb-103">Função D3DXMatrixPerspectiveFovLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f0fcb-103">D3DXMatrixPerspectiveFovLH function (D3dx9math.h)</span></span>

<span data-ttu-id="f0fcb-104">Cria uma matriz de projeção de perspectiva à esquerda com base em um campo de visão.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0fcb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0fcb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="f0fcb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0fcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0fcb-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f0fcb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0fcb-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0fcb-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0fcb-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0fcb-110">*fovy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0fcb-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0fcb-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0fcb-112">Campo de exibição na direção y, em radianos.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f0fcb-113">*Aspecto* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0fcb-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0fcb-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0fcb-115">Taxa de proporção, definida como exibir largura de espaço dividida por altura.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="f0fcb-116">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0fcb-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0fcb-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0fcb-118">Valor Z do plano de exibição próximo.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="f0fcb-119">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0fcb-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0fcb-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0fcb-121">Z-valor do plano de exibição distante.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0fcb-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0fcb-122">Return value</span></span>

<span data-ttu-id="f0fcb-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0fcb-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0fcb-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de projeção de perspectiva do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0fcb-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0fcb-125">Remarks</span></span>

<span data-ttu-id="f0fcb-126">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="f0fcb-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f0fcb-127">Dessa forma, a função **D3DXMatrixPerspectiveFovLH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-127">In this way, the **D3DXMatrixPerspectiveFovLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f0fcb-128">Para alterar o eixo de taxa de proporção, use a fórmula de cálculo: fovy = 2 \* Math. ATAN (Math. tan (fovy \* 0,5)/Aspect).</span><span class="sxs-lookup"><span data-stu-id="f0fcb-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="f0fcb-129">Como alternativa, adicione as variáveis de taxa de proporção X e Y na estrutura para dimensionar o espaço de exibição vertical: fovy = 2 \* Math. ATAN (Math. tan (fovy \* 0,5)/aspectity), Aspect = aspectX \* aspecto Y.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="f0fcb-130">Essa função computa a matriz retornada, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="f0fcb-130">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="f0fcb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0fcb-131">Requirements</span></span>



| <span data-ttu-id="f0fcb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0fcb-132">Requirement</span></span> | <span data-ttu-id="f0fcb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f0fcb-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0fcb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0fcb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f0fcb-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0fcb-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f0fcb-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0fcb-136">Library</span></span><br/> | <dl> <span data-ttu-id="f0fcb-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0fcb-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0fcb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0fcb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0fcb-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f0fcb-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f0fcb-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="f0fcb-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="f0fcb-142">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-142">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="f0fcb-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="f0fcb-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="f0fcb-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
