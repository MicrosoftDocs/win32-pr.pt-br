---
description: 'Método ID3DXTextureShader:: SetMatrixTransposePointerArray – define uma matriz de ponteiros para matrizes transpostas.'
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: 'Método ID3DXTextureShader:: SetMatrixTransposePointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 46e04c8c86bd0cdf7acea44872d00ad19f620ee6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090144"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="c0843-103">Método ID3DXTextureShader:: SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="c0843-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="c0843-104">Define uma matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="c0843-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0843-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0843-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c0843-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0843-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0843-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0843-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0843-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c0843-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c0843-109">Identificador exclusivo para a matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="c0843-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="c0843-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c0843-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0843-111">*ppMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0843-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0843-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="c0843-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="c0843-113">Matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="c0843-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="c0843-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c0843-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0843-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="c0843-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0843-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0843-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0843-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="c0843-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0843-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c0843-118">Return value</span></span>

<span data-ttu-id="c0843-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0843-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0843-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0843-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c0843-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c0843-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0843-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0843-122">Remarks</span></span>

<span data-ttu-id="c0843-123">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="c0843-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0843-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0843-124">Requirements</span></span>



| <span data-ttu-id="c0843-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0843-125">Requirement</span></span> | <span data-ttu-id="c0843-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c0843-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0843-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0843-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c0843-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0843-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c0843-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0843-129">Library</span></span><br/> | <dl> <span data-ttu-id="c0843-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0843-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c0843-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c0843-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0843-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c0843-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
