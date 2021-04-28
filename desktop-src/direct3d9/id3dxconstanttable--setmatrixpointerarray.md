---
description: 'Método ID3DXConstantTable:: SetMatrixPointerArray – define uma matriz de ponteiros para matrizes nontransposed.'
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: 'Método ID3DXConstantTable:: SetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd9505f82674efc822d4921d7116c8eab17198c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115064"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="042f9-103">Método ID3DXConstantTable:: SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="042f9-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="042f9-104">Define uma matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="042f9-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="042f9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="042f9-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="042f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="042f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="042f9-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="042f9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="042f9-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="042f9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="042f9-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="042f9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="042f9-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="042f9-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="042f9-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="042f9-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="042f9-112">Identificador exclusivo para uma matriz de matrizes constantes.</span><span class="sxs-lookup"><span data-stu-id="042f9-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="042f9-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="042f9-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="042f9-114">*ppMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="042f9-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="042f9-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="042f9-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="042f9-116">Matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="042f9-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="042f9-117">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="042f9-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="042f9-118">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="042f9-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="042f9-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="042f9-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="042f9-120">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="042f9-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="042f9-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="042f9-121">Return value</span></span>

<span data-ttu-id="042f9-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="042f9-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="042f9-123">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="042f9-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="042f9-124">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="042f9-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="042f9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="042f9-125">Remarks</span></span>

<span data-ttu-id="042f9-126">Uma matriz nontransposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="042f9-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="042f9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="042f9-127">Requirements</span></span>



| <span data-ttu-id="042f9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="042f9-128">Requirement</span></span> | <span data-ttu-id="042f9-129">Valor</span><span class="sxs-lookup"><span data-stu-id="042f9-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="042f9-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="042f9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="042f9-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="042f9-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="042f9-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="042f9-132">Library</span></span><br/> | <dl> <span data-ttu-id="042f9-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="042f9-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="042f9-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="042f9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="042f9-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="042f9-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
