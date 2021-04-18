---
description: Define uma matriz de ponteiros para matrizes transpostas.
ms.assetid: 11a21077-eeee-4d52-ac16-41444e3eca4f
title: 'Método ID3DXBaseEffect:: SetMatrixTransposePointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1152deccdcadebe9f421fac6d7d5ce53c8d3e5f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802128"
---
# <a name="id3dxbaseeffectsetmatrixtransposepointerarray-method"></a><span data-ttu-id="fe763-103">Método ID3DXBaseEffect:: SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="fe763-103">ID3DXBaseEffect::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="fe763-104">Define uma matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="fe763-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe763-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe763-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="fe763-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe763-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe763-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe763-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe763-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fe763-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fe763-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="fe763-109">Unique identifier.</span></span> <span data-ttu-id="fe763-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fe763-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe763-111">*ppMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe763-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe763-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="fe763-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="fe763-113">Matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="fe763-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="fe763-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="fe763-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe763-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="fe763-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe763-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe763-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe763-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="fe763-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe763-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe763-118">Return value</span></span>

<span data-ttu-id="fe763-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe763-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe763-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe763-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe763-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fe763-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe763-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe763-122">Remarks</span></span>

<span data-ttu-id="fe763-123">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="fe763-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="fe763-124">Se as matrizes de destino forem menores do que as matrizes de origem, os componentes adicionais das matrizes de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="fe763-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe763-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe763-125">Requirements</span></span>



| <span data-ttu-id="fe763-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe763-126">Requirement</span></span> | <span data-ttu-id="fe763-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fe763-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe763-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe763-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fe763-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe763-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fe763-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe763-130">Library</span></span><br/> | <dl> <span data-ttu-id="fe763-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe763-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fe763-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe763-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe763-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fe763-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fe763-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="fe763-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
