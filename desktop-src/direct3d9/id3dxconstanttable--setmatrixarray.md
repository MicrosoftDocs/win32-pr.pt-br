---
description: Define uma matriz de matrizes nontransposed.
ms.assetid: f36b8e8a-c22f-41e6-acb1-6298291b002f
title: 'Método ID3DXConstantTable:: SetMatrixArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 48dd85975ac58dd26d4194584ce5fbebe26da2a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760589"
---
# <a name="id3dxconstanttablesetmatrixarray-method"></a><span data-ttu-id="7c4a7-103">Método ID3DXConstantTable:: SetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="7c4a7-103">ID3DXConstantTable::SetMatrixArray method</span></span>

<span data-ttu-id="7c4a7-104">Define uma matriz de matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c4a7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c4a7-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="7c4a7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c4a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c4a7-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c4a7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c4a7-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7c4a7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7c4a7-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="7c4a7-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c4a7-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c4a7-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7c4a7-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7c4a7-112">Identificador exclusivo para a matriz de matrizes constantes.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-112">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="7c4a7-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7c4a7-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c4a7-114">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c4a7-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c4a7-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c4a7-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c4a7-116">Matriz de matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-116">Array of nontransposed matrices.</span></span> <span data-ttu-id="7c4a7-117">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="7c4a7-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c4a7-118">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="7c4a7-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c4a7-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c4a7-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c4a7-120">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c4a7-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c4a7-121">Return value</span></span>

<span data-ttu-id="7c4a7-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c4a7-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c4a7-123">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c4a7-124">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4a7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c4a7-125">Requirements</span></span>



| <span data-ttu-id="7c4a7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c4a7-126">Requirement</span></span> | <span data-ttu-id="7c4a7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7c4a7-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4a7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c4a7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7c4a7-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4a7-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7c4a7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c4a7-130">Library</span></span><br/> | <dl> <span data-ttu-id="7c4a7-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c4a7-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7c4a7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c4a7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4a7-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="7c4a7-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
