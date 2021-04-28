---
description: 'Método ID3DXConstantTable:: SetMatrixTranspose – define uma matriz transposeda.'
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: 'Método ID3DXConstantTable:: SetMatrixTranspose (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06cc989a14da6f2fe84d30f7f5d7d9fc35acd3bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115054"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="47f01-103">Método ID3DXConstantTable:: SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="47f01-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="47f01-104">Define uma matriz transposeda.</span><span class="sxs-lookup"><span data-stu-id="47f01-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47f01-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="47f01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47f01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f01-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47f01-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f01-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="47f01-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="47f01-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="47f01-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="47f01-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47f01-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f01-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="47f01-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="47f01-112">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="47f01-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="47f01-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="47f01-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="47f01-114">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47f01-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f01-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="47f01-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="47f01-116">Ponteiro para uma matriz transpoda.</span><span class="sxs-lookup"><span data-stu-id="47f01-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="47f01-117">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="47f01-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f01-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="47f01-118">Return value</span></span>

<span data-ttu-id="47f01-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47f01-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47f01-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47f01-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="47f01-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="47f01-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f01-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47f01-122">Requirements</span></span>



| <span data-ttu-id="47f01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="47f01-123">Requirement</span></span> | <span data-ttu-id="47f01-124">Valor</span><span class="sxs-lookup"><span data-stu-id="47f01-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f01-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47f01-125">Header</span></span><br/>  | <dl> <span data-ttu-id="47f01-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="47f01-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="47f01-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47f01-127">Library</span></span><br/> | <dl> <span data-ttu-id="47f01-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47f01-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="47f01-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="47f01-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f01-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="47f01-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
