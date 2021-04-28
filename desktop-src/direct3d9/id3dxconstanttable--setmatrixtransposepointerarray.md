---
description: 'Método ID3DXConstantTable:: SetMatrixTransposePointerArray – define uma matriz de ponteiros para matrizes transpostas.'
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'Método ID3DXConstantTable:: SetMatrixTransposePointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fefb5a0b62174499a4631f2fe8020c25a3a8efa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115034"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="2ef73-103">Método ID3DXConstantTable:: SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="2ef73-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="2ef73-104">Define uma matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="2ef73-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef73-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ef73-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="2ef73-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ef73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef73-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ef73-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef73-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2ef73-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2ef73-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="2ef73-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="2ef73-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ef73-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef73-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2ef73-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2ef73-112">Identificador exclusivo para a matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="2ef73-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="2ef73-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2ef73-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ef73-114">*ppMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ef73-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef73-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="2ef73-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="2ef73-116">Matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="2ef73-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="2ef73-117">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2ef73-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ef73-118">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="2ef73-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef73-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ef73-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ef73-120">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="2ef73-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef73-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2ef73-121">Return value</span></span>

<span data-ttu-id="2ef73-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ef73-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ef73-123">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ef73-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ef73-124">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2ef73-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef73-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ef73-125">Remarks</span></span>

<span data-ttu-id="2ef73-126">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="2ef73-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef73-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ef73-127">Requirements</span></span>



| <span data-ttu-id="2ef73-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ef73-128">Requirement</span></span> | <span data-ttu-id="2ef73-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2ef73-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef73-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ef73-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2ef73-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef73-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2ef73-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ef73-132">Library</span></span><br/> | <dl> <span data-ttu-id="2ef73-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ef73-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2ef73-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2ef73-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef73-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2ef73-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
