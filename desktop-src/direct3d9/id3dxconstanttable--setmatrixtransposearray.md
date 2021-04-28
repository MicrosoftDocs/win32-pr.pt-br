---
description: 'Método ID3DXConstantTable:: SetMatrixTransposeArray – define uma matriz de matrizes transpostas.'
ms.assetid: a67afc21-f43d-4dc5-b145-f3d66dd86dbb
title: 'Método ID3DXConstantTable:: SetMatrixTransposeArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0118c888adc52671a943b7b159bae80deca26a1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115044"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="5a56b-103">Método ID3DXConstantTable:: SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="5a56b-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="5a56b-104">Define uma matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="5a56b-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a56b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a56b-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="5a56b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a56b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a56b-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a56b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a56b-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5a56b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5a56b-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="5a56b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="5a56b-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a56b-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a56b-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5a56b-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5a56b-112">Identificador exclusivo para a matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="5a56b-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="5a56b-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5a56b-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a56b-114">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a56b-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a56b-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a56b-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5a56b-116">Matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="5a56b-116">Array of transposed matrices.</span></span> <span data-ttu-id="5a56b-117">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="5a56b-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a56b-118">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5a56b-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a56b-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a56b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a56b-120">Número de matrizes na matriz.</span><span class="sxs-lookup"><span data-stu-id="5a56b-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a56b-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a56b-121">Return value</span></span>

<span data-ttu-id="5a56b-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a56b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a56b-123">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a56b-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a56b-124">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5a56b-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a56b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a56b-125">Requirements</span></span>



| <span data-ttu-id="5a56b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a56b-126">Requirement</span></span> | <span data-ttu-id="5a56b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5a56b-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a56b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a56b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5a56b-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a56b-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5a56b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a56b-130">Library</span></span><br/> | <dl> <span data-ttu-id="5a56b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a56b-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5a56b-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5a56b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a56b-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="5a56b-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
