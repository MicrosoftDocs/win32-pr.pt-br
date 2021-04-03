---
description: Define uma matriz de matrizes transpostas.
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: 'Método ID3DXTextureShader:: SetMatrixTransposeArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9efd0c81cef8a72880a9755ca40e4dd8b4950ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930572"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="84eb6-103">Método ID3DXTextureShader:: SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="84eb6-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="84eb6-104">Define uma matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="84eb6-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="84eb6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84eb6-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="84eb6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84eb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84eb6-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84eb6-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84eb6-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="84eb6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="84eb6-109">Identificador exclusivo para a matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="84eb6-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="84eb6-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="84eb6-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="84eb6-111">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84eb6-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84eb6-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="84eb6-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="84eb6-113">Matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="84eb6-113">Array of transposed matrices.</span></span> <span data-ttu-id="84eb6-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="84eb6-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="84eb6-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="84eb6-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84eb6-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84eb6-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84eb6-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="84eb6-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84eb6-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84eb6-118">Return value</span></span>

<span data-ttu-id="84eb6-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84eb6-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84eb6-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="84eb6-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="84eb6-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="84eb6-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="84eb6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="84eb6-122">Remarks</span></span>

<span data-ttu-id="84eb6-123">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="84eb6-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="84eb6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84eb6-124">Requirements</span></span>



| <span data-ttu-id="84eb6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="84eb6-125">Requirement</span></span> | <span data-ttu-id="84eb6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="84eb6-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84eb6-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84eb6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="84eb6-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="84eb6-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="84eb6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84eb6-129">Library</span></span><br/> | <dl> <span data-ttu-id="84eb6-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84eb6-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="84eb6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="84eb6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84eb6-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="84eb6-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
