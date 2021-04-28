---
description: 'Método ID3DXBaseEffect:: SetMatrixTransposeArray – define uma matriz de matrizes transpostas.'
ms.assetid: 5dc65424-b0cd-490d-900e-60b9f7536ace
title: 'Método ID3DXBaseEffect:: SetMatrixTransposeArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7f145dc45f053e208f7890c8afdac6422ecde13
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097504"
---
# <a name="id3dxbaseeffectsetmatrixtransposearray-method"></a><span data-ttu-id="9aba9-103">Método ID3DXBaseEffect:: SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="9aba9-103">ID3DXBaseEffect::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="9aba9-104">Define uma matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="9aba9-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aba9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aba9-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="9aba9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aba9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aba9-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aba9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aba9-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9aba9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9aba9-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="9aba9-109">Unique identifier.</span></span> <span data-ttu-id="9aba9-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="9aba9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9aba9-111">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aba9-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aba9-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9aba9-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9aba9-113">Matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="9aba9-113">Array of transposed matrices.</span></span> <span data-ttu-id="9aba9-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="9aba9-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="9aba9-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="9aba9-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aba9-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aba9-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aba9-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="9aba9-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aba9-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9aba9-118">Return value</span></span>

<span data-ttu-id="9aba9-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9aba9-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9aba9-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9aba9-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9aba9-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9aba9-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aba9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aba9-122">Remarks</span></span>

<span data-ttu-id="9aba9-123">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="9aba9-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="9aba9-124">Se as matrizes de destino forem menores do que as matrizes de origem, os componentes adicionais das matrizes de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="9aba9-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aba9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aba9-125">Requirements</span></span>



| <span data-ttu-id="9aba9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aba9-126">Requirement</span></span> | <span data-ttu-id="9aba9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9aba9-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aba9-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aba9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9aba9-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aba9-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9aba9-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9aba9-130">Library</span></span><br/> | <dl> <span data-ttu-id="9aba9-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aba9-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9aba9-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9aba9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aba9-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="9aba9-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="9aba9-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="9aba9-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
