---
description: Define uma matriz de matrizes nontransposed.
ms.assetid: 008de62c-3a36-4499-8a0b-9075756395e9
title: 'Método ID3DXBaseEffect:: SetMatrixArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c48dcb3288930a9170c932f335a4b20c258acbb4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298470"
---
# <a name="id3dxbaseeffectsetmatrixarray-method"></a><span data-ttu-id="c8b36-103">Método ID3DXBaseEffect:: SetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="c8b36-103">ID3DXBaseEffect::SetMatrixArray method</span></span>

<span data-ttu-id="c8b36-104">Define uma matriz de matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="c8b36-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b36-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8b36-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c8b36-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8b36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b36-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c8b36-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b36-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c8b36-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c8b36-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c8b36-109">Unique identifier.</span></span> <span data-ttu-id="c8b36-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c8b36-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b36-111">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c8b36-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b36-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8b36-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8b36-113">Matriz de matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="c8b36-113">Array of nontransposed matrices.</span></span> <span data-ttu-id="c8b36-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c8b36-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b36-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="c8b36-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b36-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8b36-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8b36-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="c8b36-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b36-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8b36-118">Return value</span></span>

<span data-ttu-id="c8b36-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8b36-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8b36-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c8b36-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c8b36-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c8b36-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8b36-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8b36-122">Remarks</span></span>

<span data-ttu-id="c8b36-123">Uma matriz nontransposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="c8b36-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="c8b36-124">Se as matrizes de destino forem menores do que as matrizes de origem, os componentes adicionais das matrizes de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="c8b36-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b36-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8b36-125">Requirements</span></span>



| <span data-ttu-id="c8b36-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b36-126">Requirement</span></span> | <span data-ttu-id="c8b36-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c8b36-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b36-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8b36-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c8b36-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b36-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c8b36-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8b36-130">Library</span></span><br/> | <dl> <span data-ttu-id="c8b36-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8b36-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c8b36-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8b36-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b36-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c8b36-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c8b36-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="c8b36-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
