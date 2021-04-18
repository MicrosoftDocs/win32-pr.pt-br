---
description: Obtém uma matriz de matrizes nontransposed.
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: 'Método ID3DXBaseEffect:: GetMatrixArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 242b3c42976f9bfe4ad8ecad4d965c473839ffdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786264"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a><span data-ttu-id="5f4df-103">Método ID3DXBaseEffect:: GetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="5f4df-103">ID3DXBaseEffect::GetMatrixArray method</span></span>

<span data-ttu-id="5f4df-104">Obtém uma matriz de matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="5f4df-104">Gets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f4df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f4df-105">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="5f4df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f4df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f4df-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f4df-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4df-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5f4df-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5f4df-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5f4df-109">Unique identifier.</span></span> <span data-ttu-id="5f4df-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5f4df-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f4df-111">*pMatrix* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5f4df-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4df-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f4df-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5f4df-113">Retorna uma matriz de matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="5f4df-113">Returns an array of nontransposed matrices.</span></span> <span data-ttu-id="5f4df-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="5f4df-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f4df-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5f4df-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4df-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f4df-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f4df-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="5f4df-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f4df-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f4df-118">Return value</span></span>

<span data-ttu-id="5f4df-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f4df-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f4df-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5f4df-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5f4df-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5f4df-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f4df-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f4df-122">Remarks</span></span>

<span data-ttu-id="5f4df-123">Uma matriz nontransposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="5f4df-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="5f4df-124">Se as matrizes de destino forem maiores do que as matrizes de origem, somente os componentes do canto superior esquerdo de cada matriz de destino serão preenchidos e os componentes da matriz de destino restantes serão definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="5f4df-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f4df-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f4df-125">Requirements</span></span>



| <span data-ttu-id="5f4df-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f4df-126">Requirement</span></span> | <span data-ttu-id="5f4df-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5f4df-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f4df-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f4df-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5f4df-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f4df-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5f4df-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f4df-130">Library</span></span><br/> | <dl> <span data-ttu-id="5f4df-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f4df-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5f4df-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f4df-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4df-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5f4df-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5f4df-134">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="5f4df-134">**SetMatrixArray**</span></span>](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
