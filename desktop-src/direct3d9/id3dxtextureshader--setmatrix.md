---
description: 'Método ID3DXTextureShader:: setmatrix – define uma matriz não transposeda.'
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: 'Método ID3DXTextureShader:: setmatrix (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15ba6b289ad106a8fad4a932b9c5d01e0a52dc18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090214"
---
# <a name="id3dxtextureshadersetmatrix-method"></a><span data-ttu-id="54a18-103">Método ID3DXTextureShader:: setmatrix</span><span class="sxs-lookup"><span data-stu-id="54a18-103">ID3DXTextureShader::SetMatrix method</span></span>

<span data-ttu-id="54a18-104">Define uma matriz não transposeda.</span><span class="sxs-lookup"><span data-stu-id="54a18-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a18-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54a18-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="54a18-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54a18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a18-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="54a18-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a18-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="54a18-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="54a18-109">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="54a18-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="54a18-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="54a18-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="54a18-111">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="54a18-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a18-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="54a18-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54a18-113">Ponteiro para uma matriz não transposeda.</span><span class="sxs-lookup"><span data-stu-id="54a18-113">Pointer to a non-transposed matrix.</span></span> <span data-ttu-id="54a18-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="54a18-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a18-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="54a18-115">Return value</span></span>

<span data-ttu-id="54a18-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54a18-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54a18-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54a18-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="54a18-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="54a18-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a18-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="54a18-119">Remarks</span></span>

<span data-ttu-id="54a18-120">Uma matriz não transposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="54a18-120">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="54a18-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54a18-121">Requirements</span></span>



| <span data-ttu-id="54a18-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="54a18-122">Requirement</span></span> | <span data-ttu-id="54a18-123">Valor</span><span class="sxs-lookup"><span data-stu-id="54a18-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a18-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54a18-124">Header</span></span><br/>  | <dl> <span data-ttu-id="54a18-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="54a18-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="54a18-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54a18-126">Library</span></span><br/> | <dl> <span data-ttu-id="54a18-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54a18-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="54a18-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="54a18-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a18-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="54a18-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




