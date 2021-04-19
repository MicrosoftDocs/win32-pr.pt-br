---
description: Define uma matriz de ponteiros para matrizes nontransposed.
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
ms.openlocfilehash: 4b29d4298d8ca52d2826cc780fb90d769c3337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784559"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="b3a82-103">Método ID3DXConstantTable:: SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="b3a82-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="b3a82-104">Define uma matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="b3a82-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3a82-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="b3a82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3a82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a82-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3a82-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a82-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b3a82-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b3a82-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="b3a82-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="b3a82-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3a82-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a82-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b3a82-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b3a82-112">Identificador exclusivo para uma matriz de matrizes constantes.</span><span class="sxs-lookup"><span data-stu-id="b3a82-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="b3a82-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b3a82-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3a82-114">*ppMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3a82-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a82-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="b3a82-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="b3a82-116">Matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="b3a82-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="b3a82-117">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b3a82-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3a82-118">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="b3a82-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a82-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3a82-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3a82-120">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="b3a82-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3a82-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3a82-121">Return value</span></span>

<span data-ttu-id="b3a82-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3a82-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3a82-123">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3a82-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b3a82-124">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b3a82-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3a82-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3a82-125">Remarks</span></span>

<span data-ttu-id="b3a82-126">Uma matriz nontransposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="b3a82-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a82-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3a82-127">Requirements</span></span>



| <span data-ttu-id="b3a82-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3a82-128">Requirement</span></span> | <span data-ttu-id="b3a82-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b3a82-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a82-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3a82-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b3a82-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3a82-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b3a82-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3a82-132">Library</span></span><br/> | <dl> <span data-ttu-id="b3a82-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3a82-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b3a82-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3a82-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a82-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b3a82-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
