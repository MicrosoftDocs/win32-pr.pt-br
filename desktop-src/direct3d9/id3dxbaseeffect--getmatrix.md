---
description: Obtém uma matriz nontransposed.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'Método ID3DXBaseEffect:: getmatrix (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780258"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a><span data-ttu-id="2334d-103">Método ID3DXBaseEffect:: getmatrix</span><span class="sxs-lookup"><span data-stu-id="2334d-103">ID3DXBaseEffect::GetMatrix method</span></span>

<span data-ttu-id="2334d-104">Obtém uma matriz nontransposed.</span><span class="sxs-lookup"><span data-stu-id="2334d-104">Gets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2334d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2334d-105">Syntax</span></span>


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="2334d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2334d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2334d-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2334d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2334d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2334d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2334d-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2334d-109">Unique identifier.</span></span> <span data-ttu-id="2334d-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2334d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2334d-111">*pMatrix* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2334d-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2334d-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2334d-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2334d-113">Retorna uma matriz nontransposed.</span><span class="sxs-lookup"><span data-stu-id="2334d-113">Returns a nontransposed matrix.</span></span> <span data-ttu-id="2334d-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2334d-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2334d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2334d-115">Return value</span></span>

<span data-ttu-id="2334d-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2334d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2334d-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2334d-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2334d-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2334d-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2334d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2334d-119">Remarks</span></span>

<span data-ttu-id="2334d-120">Uma matriz nontransposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="2334d-120">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="2334d-121">Se a matriz de destino for maior que a matriz de origem, somente os componentes do canto superior esquerdo da matriz de destino serão preenchidos e os componentes restantes serão definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="2334d-121">If the destination matrix is larger than the source matrix, only the upper-left components of the destination matrix will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2334d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2334d-122">Requirements</span></span>



| <span data-ttu-id="2334d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2334d-123">Requirement</span></span> | <span data-ttu-id="2334d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2334d-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2334d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2334d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2334d-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2334d-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2334d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2334d-127">Library</span></span><br/> | <dl> <span data-ttu-id="2334d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2334d-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2334d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2334d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2334d-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2334d-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="2334d-131">**Setmatrix**</span><span class="sxs-lookup"><span data-stu-id="2334d-131">**SetMatrix**</span></span>](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




