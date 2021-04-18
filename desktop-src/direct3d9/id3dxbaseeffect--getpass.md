---
description: Obtém o identificador de uma passagem.
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'Método ID3DXBaseEffect:: getpass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104371016"
---
# <a name="id3dxbaseeffectgetpass-method"></a><span data-ttu-id="a6280-103">Método ID3DXBaseEffect:: getpass</span><span class="sxs-lookup"><span data-stu-id="a6280-103">ID3DXBaseEffect::GetPass method</span></span>

<span data-ttu-id="a6280-104">Obtém o identificador de uma passagem.</span><span class="sxs-lookup"><span data-stu-id="a6280-104">Gets the handle of a pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6280-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6280-105">Syntax</span></span>


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="a6280-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6280-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6280-107">*hTechnique* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6280-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6280-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a6280-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a6280-109">Identificador da técnica pai.</span><span class="sxs-lookup"><span data-stu-id="a6280-109">Handle of the parent technique.</span></span> <span data-ttu-id="a6280-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a6280-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6280-111">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a6280-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6280-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6280-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6280-113">Índice para a passagem.</span><span class="sxs-lookup"><span data-stu-id="a6280-113">Index for the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6280-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6280-114">Return value</span></span>

<span data-ttu-id="a6280-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a6280-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a6280-116">Retorna o identificador da passagem especificada dentro da técnica especificada ou **NULL** se o índice era inválido.</span><span class="sxs-lookup"><span data-stu-id="a6280-116">Returns the handle of the specified pass inside the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="a6280-117">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a6280-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6280-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6280-118">Requirements</span></span>



| <span data-ttu-id="a6280-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6280-119">Requirement</span></span> | <span data-ttu-id="a6280-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a6280-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6280-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6280-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a6280-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6280-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a6280-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6280-123">Library</span></span><br/> | <dl> <span data-ttu-id="a6280-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6280-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a6280-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6280-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6280-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a6280-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
