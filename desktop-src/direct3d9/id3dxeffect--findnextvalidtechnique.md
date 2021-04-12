---
description: Pesquisa a próxima técnica válida, começando na técnica após a técnica especificada.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'Método ID3DXEffect:: FindNextValidTechnique (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370963"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a><span data-ttu-id="299e1-103">Método ID3DXEffect:: FindNextValidTechnique</span><span class="sxs-lookup"><span data-stu-id="299e1-103">ID3DXEffect::FindNextValidTechnique method</span></span>

<span data-ttu-id="299e1-104">Pesquisa a próxima técnica válida, começando na técnica após a técnica especificada.</span><span class="sxs-lookup"><span data-stu-id="299e1-104">Searches for the next valid technique, starting at the technique after the specified technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="299e1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="299e1-105">Syntax</span></span>


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="299e1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="299e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="299e1-107">*hTechnique* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="299e1-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="299e1-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="299e1-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="299e1-109">Identificador exclusivo para uma técnica.</span><span class="sxs-lookup"><span data-stu-id="299e1-109">Unique identifier to a technique.</span></span> <span data-ttu-id="299e1-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="299e1-110">See [Handles (Direct3D 9)](handles.md).</span></span> <span data-ttu-id="299e1-111">Especifique **NULL** para esse parâmetro para localizar a primeira técnica válida.</span><span class="sxs-lookup"><span data-stu-id="299e1-111">Specify **NULL** for this parameter to find the first valid technique.</span></span>

</dd> <dt>

<span data-ttu-id="299e1-112">*pTechnique* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="299e1-112">*pTechnique* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="299e1-113">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span><span class="sxs-lookup"><span data-stu-id="299e1-113">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span></span>

<span data-ttu-id="299e1-114">Ponteiro para um identificador para a próxima técnica.</span><span class="sxs-lookup"><span data-stu-id="299e1-114">Pointer to an identifier for the next technique.</span></span> <span data-ttu-id="299e1-115">**NULL** será retornado se esta for a última técnica.</span><span class="sxs-lookup"><span data-stu-id="299e1-115">**NULL** is returned if this is the last technique.</span></span> <span data-ttu-id="299e1-116">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="299e1-116">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="299e1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="299e1-117">Return value</span></span>

<span data-ttu-id="299e1-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="299e1-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="299e1-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="299e1-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="299e1-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="299e1-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="299e1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="299e1-121">Requirements</span></span>



| <span data-ttu-id="299e1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="299e1-122">Requirement</span></span> | <span data-ttu-id="299e1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="299e1-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="299e1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="299e1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="299e1-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="299e1-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="299e1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="299e1-126">Library</span></span><br/> | <dl> <span data-ttu-id="299e1-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="299e1-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="299e1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="299e1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299e1-129">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="299e1-129">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="299e1-130">**D3DXTECHNIQUE \_ desc**</span><span class="sxs-lookup"><span data-stu-id="299e1-130">**D3DXTECHNIQUE\_DESC**</span></span>](d3dxtechnique-desc.md)
</dt> <dt>

[<span data-ttu-id="299e1-131">**ID3DXEffect::ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="299e1-131">**ID3DXEffect::ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




