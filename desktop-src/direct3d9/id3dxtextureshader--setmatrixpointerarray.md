---
description: Define uma matriz de ponteiros para matrizes não transpostas.
ms.assetid: 5ad83abd-1895-4838-85b5-c437c23a3d91
title: 'Método ID3DXTextureShader:: SetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bde5250ae8ceeab7522b9df15c99070e9471608
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298548"
---
# <a name="id3dxtextureshadersetmatrixpointerarray-method"></a><span data-ttu-id="2a639-103">Método ID3DXTextureShader:: SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="2a639-103">ID3DXTextureShader::SetMatrixPointerArray method</span></span>

<span data-ttu-id="2a639-104">Define uma matriz de ponteiros para matrizes não transpostas.</span><span class="sxs-lookup"><span data-stu-id="2a639-104">Sets an array of pointers to non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a639-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a639-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2a639-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a639-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a639-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a639-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a639-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2a639-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2a639-109">Identificador exclusivo para uma matriz de matrizes constantes.</span><span class="sxs-lookup"><span data-stu-id="2a639-109">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="2a639-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="2a639-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a639-111">*ppMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a639-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a639-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="2a639-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="2a639-113">Matriz de ponteiros para matrizes não transpostas.</span><span class="sxs-lookup"><span data-stu-id="2a639-113">Array of pointers to non-transposed matrices.</span></span> <span data-ttu-id="2a639-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2a639-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a639-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="2a639-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a639-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a639-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a639-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="2a639-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a639-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a639-118">Return value</span></span>

<span data-ttu-id="2a639-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a639-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a639-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2a639-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2a639-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2a639-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a639-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a639-122">Remarks</span></span>

<span data-ttu-id="2a639-123">Uma matriz não transposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="2a639-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a639-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a639-124">Requirements</span></span>



| <span data-ttu-id="2a639-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a639-125">Requirement</span></span> | <span data-ttu-id="2a639-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2a639-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a639-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a639-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2a639-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a639-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2a639-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a639-129">Library</span></span><br/> | <dl> <span data-ttu-id="2a639-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a639-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2a639-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a639-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a639-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2a639-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
