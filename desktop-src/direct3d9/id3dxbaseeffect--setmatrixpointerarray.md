---
description: Define uma matriz de ponteiros para matrizes nontransposed.
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'Método ID3DXBaseEffect:: SetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0f199c3db335dfc6b9966987678c07b4b3a22402
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930538"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="7228c-103">Método ID3DXBaseEffect:: SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="7228c-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="7228c-104">Define uma matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="7228c-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7228c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7228c-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="7228c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7228c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7228c-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7228c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7228c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7228c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7228c-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7228c-109">Unique identifier.</span></span> <span data-ttu-id="7228c-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7228c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7228c-111">*ppMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7228c-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7228c-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="7228c-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="7228c-113">Matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="7228c-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="7228c-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="7228c-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7228c-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="7228c-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7228c-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7228c-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7228c-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="7228c-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7228c-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7228c-118">Return value</span></span>

<span data-ttu-id="7228c-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7228c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7228c-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7228c-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7228c-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7228c-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7228c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7228c-122">Remarks</span></span>

<span data-ttu-id="7228c-123">Uma matriz nontransposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="7228c-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="7228c-124">Se as matrizes de destino forem menores do que as matrizes de origem, os componentes adicionais das matrizes de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="7228c-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7228c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7228c-125">Requirements</span></span>



| <span data-ttu-id="7228c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7228c-126">Requirement</span></span> | <span data-ttu-id="7228c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7228c-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7228c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7228c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7228c-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7228c-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7228c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7228c-130">Library</span></span><br/> | <dl> <span data-ttu-id="7228c-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7228c-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7228c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7228c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7228c-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7228c-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="7228c-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="7228c-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
