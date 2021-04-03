---
description: Determina se um parâmetro é usado pela técnica.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'Método ID3DXEffect:: IsParameterUsed (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6cbe4783a9ad5b618f05941eae08af4c15be0512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091947"
---
# <a name="id3dxeffectisparameterused-method"></a><span data-ttu-id="df70f-103">Método ID3DXEffect:: IsParameterUsed</span><span class="sxs-lookup"><span data-stu-id="df70f-103">ID3DXEffect::IsParameterUsed method</span></span>

<span data-ttu-id="df70f-104">Determina se um parâmetro é usado pela técnica.</span><span class="sxs-lookup"><span data-stu-id="df70f-104">Determines if a parameter is used by the technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="df70f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df70f-105">Syntax</span></span>


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="df70f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df70f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df70f-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df70f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df70f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="df70f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="df70f-109">Identificador exclusivo para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="df70f-109">Unique identifier for the parameter.</span></span> <span data-ttu-id="df70f-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="df70f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="df70f-111">*hTechnique* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df70f-111">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df70f-112">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="df70f-112">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="df70f-113">Identificador exclusivo da técnica.</span><span class="sxs-lookup"><span data-stu-id="df70f-113">Unique identifier for the technique.</span></span> <span data-ttu-id="df70f-114">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="df70f-114">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df70f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df70f-115">Return value</span></span>

<span data-ttu-id="df70f-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df70f-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df70f-117">Retornará **true** se o parâmetro estiver sendo usado e retornará **false** se o parâmetro não estiver sendo usado.</span><span class="sxs-lookup"><span data-stu-id="df70f-117">Returns **TRUE** if the parameter is being used and returns **FALSE** if the parameter is not being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="df70f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df70f-118">Requirements</span></span>



| <span data-ttu-id="df70f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="df70f-119">Requirement</span></span> | <span data-ttu-id="df70f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="df70f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="df70f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df70f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="df70f-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="df70f-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="df70f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df70f-123">Library</span></span><br/> | <dl> <span data-ttu-id="df70f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df70f-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="df70f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="df70f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df70f-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="df70f-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
