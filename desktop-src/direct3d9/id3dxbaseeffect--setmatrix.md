---
description: Define uma matriz não transposeda.
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'Método ID3DXBaseEffect:: setmatrix (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 39a5aed1d6321cf0599d212222fd967ee512e20e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506459"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="c0c00-103">Método ID3DXBaseEffect:: setmatrix</span><span class="sxs-lookup"><span data-stu-id="c0c00-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="c0c00-104">Define uma matriz não transposeda.</span><span class="sxs-lookup"><span data-stu-id="c0c00-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c00-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0c00-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="c0c00-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0c00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0c00-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0c00-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0c00-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c0c00-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c0c00-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c0c00-109">Unique identifier.</span></span> <span data-ttu-id="c0c00-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c0c00-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0c00-111">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0c00-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0c00-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0c00-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c0c00-113">Ponteiro para uma matriz nontransposed.</span><span class="sxs-lookup"><span data-stu-id="c0c00-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="c0c00-114">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c0c00-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0c00-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0c00-115">Return value</span></span>

<span data-ttu-id="c0c00-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0c00-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0c00-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0c00-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c0c00-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c0c00-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0c00-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0c00-119">Remarks</span></span>

<span data-ttu-id="c0c00-120">Uma matriz não transposed contém dados de linha principal.</span><span class="sxs-lookup"><span data-stu-id="c0c00-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="c0c00-121">Em outras palavras, cada vetor está contido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="c0c00-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="c0c00-122">Se a matriz de destino for menor do que a matriz de origem, os componentes adicionais da matriz de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="c0c00-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0c00-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0c00-123">Requirements</span></span>



| <span data-ttu-id="c0c00-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0c00-124">Requirement</span></span> | <span data-ttu-id="c0c00-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c0c00-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c00-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0c00-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c0c00-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0c00-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c0c00-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0c00-128">Library</span></span><br/> | <dl> <span data-ttu-id="c0c00-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0c00-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c0c00-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0c00-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0c00-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c0c00-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c0c00-132">**Getmatrix**</span><span class="sxs-lookup"><span data-stu-id="c0c00-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




