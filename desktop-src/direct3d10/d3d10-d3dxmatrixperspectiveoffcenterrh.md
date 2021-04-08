---
description: Cria uma matriz de projeção de perspectiva personalizada para o lado direito.
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: Função D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54fc98658d5466acd69d3245af7488c40cd352c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012157"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="ab456-103">Função D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ab456-103">D3DXMatrixPerspectiveOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="ab456-104">Cria uma matriz de projeção de perspectiva personalizada para o lado direito.</span><span class="sxs-lookup"><span data-stu-id="ab456-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab456-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab456-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="ab456-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab456-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab456-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ab456-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab456-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab456-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab456-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="ab456-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ab456-110">*l* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ab456-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab456-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab456-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab456-112">Valor x mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="ab456-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="ab456-113">*r* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ab456-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab456-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab456-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab456-115">Valor x máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="ab456-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="ab456-116">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ab456-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab456-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab456-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab456-118">Valor y mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="ab456-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="ab456-119">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ab456-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab456-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab456-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab456-121">Valor y máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="ab456-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="ab456-122">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab456-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab456-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab456-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab456-124">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="ab456-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="ab456-125">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab456-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab456-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab456-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab456-127">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="ab456-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab456-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab456-128">Return value</span></span>

<span data-ttu-id="ab456-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab456-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab456-130">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de projeção de perspectiva de mão com o lado direito personalizada.</span><span class="sxs-lookup"><span data-stu-id="ab456-130">Pointer to a D3DXMATRIX structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab456-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab456-131">Remarks</span></span>

<span data-ttu-id="ab456-132">Todos os parâmetros da função D3DXMatrixPerspectiveOffCenterRH são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="ab456-132">All the parameters of the D3DXMatrixPerspectiveOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="ab456-133">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="ab456-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="ab456-134">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="ab456-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ab456-135">Dessa forma, a função D3DXMatrixPerspectiveOffCenterRH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="ab456-135">In this way, the D3DXMatrixPerspectiveOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ab456-136">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="ab456-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="ab456-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab456-137">Requirements</span></span>



| <span data-ttu-id="ab456-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab456-138">Requirement</span></span> | <span data-ttu-id="ab456-139">Valor</span><span class="sxs-lookup"><span data-stu-id="ab456-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab456-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab456-140">Header</span></span><br/>  | <dl> <span data-ttu-id="ab456-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab456-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ab456-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab456-142">Library</span></span><br/> | <dl> <span data-ttu-id="ab456-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab456-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab456-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab456-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab456-145">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="ab456-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
