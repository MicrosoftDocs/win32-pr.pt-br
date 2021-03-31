---
description: Define uma matriz transposeda.
ms.assetid: 5339a9de-528f-4404-880b-73964192b766
title: 'Método ID3DXTextureShader:: SetMatrixTranspose (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf5507d935d2fea1b6210624e70344a2c4a1da81
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930612"
---
# <a name="id3dxtextureshadersetmatrixtranspose-method"></a><span data-ttu-id="92bfc-103">Método ID3DXTextureShader:: SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="92bfc-103">ID3DXTextureShader::SetMatrixTranspose method</span></span>

<span data-ttu-id="92bfc-104">Define uma matriz transposeda.</span><span class="sxs-lookup"><span data-stu-id="92bfc-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="92bfc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92bfc-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="92bfc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92bfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92bfc-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92bfc-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92bfc-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="92bfc-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="92bfc-109">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="92bfc-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="92bfc-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="92bfc-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="92bfc-111">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92bfc-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92bfc-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="92bfc-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="92bfc-113">Ponteiro para uma matriz transpoda.</span><span class="sxs-lookup"><span data-stu-id="92bfc-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="92bfc-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="92bfc-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92bfc-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92bfc-115">Return value</span></span>

<span data-ttu-id="92bfc-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92bfc-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92bfc-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="92bfc-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="92bfc-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="92bfc-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="92bfc-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="92bfc-119">Remarks</span></span>

<span data-ttu-id="92bfc-120">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="92bfc-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="92bfc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92bfc-121">Requirements</span></span>



| <span data-ttu-id="92bfc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="92bfc-122">Requirement</span></span> | <span data-ttu-id="92bfc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="92bfc-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92bfc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92bfc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="92bfc-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="92bfc-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="92bfc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92bfc-126">Library</span></span><br/> | <dl> <span data-ttu-id="92bfc-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92bfc-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="92bfc-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="92bfc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92bfc-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="92bfc-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




