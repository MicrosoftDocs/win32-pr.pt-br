---
description: Obtém uma matriz de ponteiros para matrizes transpostas.
ms.assetid: b859ff2f-cf62-4619-b8be-b940fa0513b3
title: 'Método ID3DXBaseEffect:: GetMatrixTransposePointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e69c01395582691e6fdd0a695991ff1f726a362b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173183"
---
# <a name="id3dxbaseeffectgetmatrixtransposepointerarray-method"></a><span data-ttu-id="e4838-103">Método ID3DXBaseEffect:: GetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="e4838-103">ID3DXBaseEffect::GetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="e4838-104">Obtém uma matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="e4838-104">Gets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4838-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4838-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposePointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="e4838-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4838-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4838-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4838-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e4838-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e4838-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e4838-109">Unique identifier.</span></span> <span data-ttu-id="e4838-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e4838-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4838-111">*ppMatrix* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e4838-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4838-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e4838-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="e4838-113">Matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="e4838-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="e4838-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e4838-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4838-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="e4838-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4838-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4838-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4838-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="e4838-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4838-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4838-118">Return value</span></span>

<span data-ttu-id="e4838-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4838-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4838-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e4838-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e4838-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e4838-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4838-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4838-122">Remarks</span></span>

<span data-ttu-id="e4838-123">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="e4838-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="e4838-124">Se as matrizes de destino forem maiores do que as matrizes de origem, somente os componentes do canto superior esquerdo de cada matriz de destino serão preenchidos e os componentes da matriz de destino restantes serão definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="e4838-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4838-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4838-125">Requirements</span></span>



| <span data-ttu-id="e4838-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4838-126">Requirement</span></span> | <span data-ttu-id="e4838-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e4838-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4838-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4838-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e4838-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4838-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e4838-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4838-130">Library</span></span><br/> | <dl> <span data-ttu-id="e4838-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4838-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e4838-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4838-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4838-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e4838-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="e4838-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="e4838-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
