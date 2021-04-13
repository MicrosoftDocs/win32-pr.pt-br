---
description: Obtém uma matriz transposeda.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: 'Método ID3DXBaseEffect:: GetMatrixTranspose (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f52a7b528a7853278f5e1b902c3907e8d48fa40f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298827"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a><span data-ttu-id="537f3-103">Método ID3DXBaseEffect:: GetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="537f3-103">ID3DXBaseEffect::GetMatrixTranspose method</span></span>

<span data-ttu-id="537f3-104">Obtém uma matriz transposeda.</span><span class="sxs-lookup"><span data-stu-id="537f3-104">Gets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="537f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="537f3-105">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="537f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="537f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="537f3-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="537f3-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="537f3-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="537f3-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="537f3-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="537f3-109">Unique identifier.</span></span> <span data-ttu-id="537f3-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="537f3-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="537f3-111">*pMatrix* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="537f3-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="537f3-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="537f3-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="537f3-113">Retorna uma matriz transposeda.</span><span class="sxs-lookup"><span data-stu-id="537f3-113">Returns a transposed matrix.</span></span> <span data-ttu-id="537f3-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="537f3-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="537f3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="537f3-115">Return value</span></span>

<span data-ttu-id="537f3-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="537f3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="537f3-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="537f3-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="537f3-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="537f3-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="537f3-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="537f3-119">Remarks</span></span>

<span data-ttu-id="537f3-120">Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="537f3-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="537f3-121">Se a matriz de destino for maior que a matriz de origem, somente os elementos do canto superior esquerdo da matriz de destino serão preenchidos e os componentes da matriz de destino restantes serão definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="537f3-121">If the destination matrix is larger than the source matrix, only the upper-left elements of the destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="537f3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="537f3-122">Requirements</span></span>



| <span data-ttu-id="537f3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="537f3-123">Requirement</span></span> | <span data-ttu-id="537f3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="537f3-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="537f3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="537f3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="537f3-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="537f3-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="537f3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="537f3-127">Library</span></span><br/> | <dl> <span data-ttu-id="537f3-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="537f3-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="537f3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="537f3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537f3-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="537f3-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="537f3-131">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="537f3-131">**SetMatrixTranspose**</span></span>](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




