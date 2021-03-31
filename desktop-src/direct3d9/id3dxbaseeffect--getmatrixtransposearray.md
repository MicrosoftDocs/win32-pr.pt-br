---
description: Obtém uma matriz de matrizes transpostas.
ms.assetid: fbfcb2e4-82ca-4f79-923e-35749c5b9586
title: 'Método ID3DXBaseEffect:: GetMatrixTransposeArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c5f3709a31067b82e9752a9e97db6f3a2a323a19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664108"
---
# <a name="id3dxbaseeffectgetmatrixtransposearray-method"></a><span data-ttu-id="95789-103">Método ID3DXBaseEffect:: GetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="95789-103">ID3DXBaseEffect::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="95789-104">Obtém uma matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="95789-104">Gets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="95789-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95789-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="95789-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95789-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95789-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95789-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95789-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="95789-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="95789-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="95789-109">Unique identifier.</span></span> <span data-ttu-id="95789-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="95789-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="95789-111">*pMatrix* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95789-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95789-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="95789-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="95789-113">Retorna uma matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="95789-113">Returns an array of transposed matrices.</span></span> <span data-ttu-id="95789-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="95789-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="95789-115">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="95789-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95789-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95789-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95789-117">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="95789-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95789-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95789-118">Return value</span></span>

<span data-ttu-id="95789-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95789-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95789-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95789-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95789-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="95789-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="95789-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="95789-122">Remarks</span></span>

<span data-ttu-id="95789-123">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="95789-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="95789-124">Se as matrizes de destino forem maiores do que as matrizes de origem, somente os componentes do canto superior esquerdo de cada matriz de destino serão preenchidos e os componentes da matriz de destino restantes serão definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="95789-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="95789-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95789-125">Requirements</span></span>



| <span data-ttu-id="95789-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="95789-126">Requirement</span></span> | <span data-ttu-id="95789-127">Valor</span><span class="sxs-lookup"><span data-stu-id="95789-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="95789-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95789-128">Header</span></span><br/>  | <dl> <span data-ttu-id="95789-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="95789-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="95789-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95789-130">Library</span></span><br/> | <dl> <span data-ttu-id="95789-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95789-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="95789-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="95789-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95789-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="95789-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="95789-134">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="95789-134">**SetMatrixTransposeArray**</span></span>](id3dxbaseeffect--setmatrixtransposearray.md)
</dt> </dl>

 

 
