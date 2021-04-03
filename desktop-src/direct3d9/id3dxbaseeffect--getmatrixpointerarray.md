---
description: Obtém uma matriz de ponteiros para matrizes nontransposed.
ms.assetid: ee9f752d-a06a-43a3-b4ce-d1d585ba8c08
title: 'Método ID3DXBaseEffect:: GetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a841c321e641b74841a76432eab8b016f396f61a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930747"
---
# <a name="id3dxbaseeffectgetmatrixpointerarray-method"></a><span data-ttu-id="30ffa-103">Método ID3DXBaseEffect:: GetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="30ffa-103">ID3DXBaseEffect::GetMatrixPointerArray method</span></span>

<span data-ttu-id="30ffa-104">Obtém uma matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="30ffa-104">Gets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ffa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30ffa-105">Syntax</span></span>


```C++
HRESULT GetMatrixPointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="30ffa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30ffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ffa-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30ffa-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ffa-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="30ffa-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="30ffa-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="30ffa-109">Unique identifier.</span></span> <span data-ttu-id="30ffa-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="30ffa-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="30ffa-111">*ppMatrix* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="30ffa-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30ffa-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="30ffa-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="30ffa-113">Matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="30ffa-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="30ffa-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="30ffa-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="30ffa-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="30ffa-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ffa-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30ffa-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30ffa-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="30ffa-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ffa-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30ffa-118">Return value</span></span>

<span data-ttu-id="30ffa-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30ffa-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30ffa-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30ffa-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30ffa-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="30ffa-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="30ffa-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="30ffa-122">Remarks</span></span>

<span data-ttu-id="30ffa-123">Uma matriz nontransposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="30ffa-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="30ffa-124">Se as matrizes de destino forem maiores do que as matrizes de origem, somente os componentes do canto superior esquerdo de cada matriz de destino serão preenchidos e os componentes da matriz de destino restantes serão definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="30ffa-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ffa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30ffa-125">Requirements</span></span>



| <span data-ttu-id="30ffa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="30ffa-126">Requirement</span></span> | <span data-ttu-id="30ffa-127">Valor</span><span class="sxs-lookup"><span data-stu-id="30ffa-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ffa-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30ffa-128">Header</span></span><br/>  | <dl> <span data-ttu-id="30ffa-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="30ffa-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="30ffa-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30ffa-130">Library</span></span><br/> | <dl> <span data-ttu-id="30ffa-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30ffa-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="30ffa-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ffa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ffa-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="30ffa-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="30ffa-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="30ffa-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
