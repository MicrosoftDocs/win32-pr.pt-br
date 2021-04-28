---
description: 'Método ID3DXBaseEffect:: SetMatrixTranspose – define uma matriz transposeda.'
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: 'Método ID3DXBaseEffect:: SetMatrixTranspose (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 384d4a7ed5e1b769218b9290ed6cc0f7f060bd66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107394"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="055ef-103">Método ID3DXBaseEffect:: SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="055ef-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="055ef-104">Define uma matriz transposeda.</span><span class="sxs-lookup"><span data-stu-id="055ef-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="055ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="055ef-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="055ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="055ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="055ef-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="055ef-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="055ef-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="055ef-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="055ef-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="055ef-109">Unique identifier.</span></span> <span data-ttu-id="055ef-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="055ef-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="055ef-111">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="055ef-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="055ef-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="055ef-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="055ef-113">Ponteiro para uma matriz transpoda.</span><span class="sxs-lookup"><span data-stu-id="055ef-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="055ef-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="055ef-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="055ef-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="055ef-115">Return value</span></span>

<span data-ttu-id="055ef-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="055ef-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="055ef-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="055ef-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="055ef-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="055ef-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="055ef-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="055ef-119">Remarks</span></span>

<span data-ttu-id="055ef-120">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="055ef-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="055ef-121">Se a matriz de destino for menor do que a matriz de origem, os componentes adicionais da matriz de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="055ef-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="055ef-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="055ef-122">Requirements</span></span>



| <span data-ttu-id="055ef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="055ef-123">Requirement</span></span> | <span data-ttu-id="055ef-124">Valor</span><span class="sxs-lookup"><span data-stu-id="055ef-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="055ef-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="055ef-125">Header</span></span><br/>  | <dl> <span data-ttu-id="055ef-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="055ef-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="055ef-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="055ef-127">Library</span></span><br/> | <dl> <span data-ttu-id="055ef-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="055ef-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="055ef-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="055ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="055ef-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="055ef-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="055ef-131">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="055ef-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




