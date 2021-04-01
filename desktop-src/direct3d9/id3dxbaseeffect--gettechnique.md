---
description: Obtém o identificador de uma técnica.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: 'Método ID3DXBaseEffect:: gettécnica (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f0c82c301a48eb939d182062240c4dba6d3fc63
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091999"
---
# <a name="id3dxbaseeffectgettechnique-method"></a><span data-ttu-id="6b140-103">Método ID3DXBaseEffect:: gettécnica</span><span class="sxs-lookup"><span data-stu-id="6b140-103">ID3DXBaseEffect::GetTechnique method</span></span>

<span data-ttu-id="6b140-104">Obtém o identificador de uma técnica.</span><span class="sxs-lookup"><span data-stu-id="6b140-104">Gets the handle of a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b140-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b140-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="6b140-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b140-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b140-107">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="6b140-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b140-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b140-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b140-109">Índice de técnica.</span><span class="sxs-lookup"><span data-stu-id="6b140-109">Technique index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b140-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b140-110">Return value</span></span>

<span data-ttu-id="6b140-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6b140-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6b140-112">Retorna o identificador da técnica especificada ou **NULL** se o índice era inválido.</span><span class="sxs-lookup"><span data-stu-id="6b140-112">Returns the handle of the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="6b140-113">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6b140-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b140-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b140-114">Requirements</span></span>



| <span data-ttu-id="6b140-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b140-115">Requirement</span></span> | <span data-ttu-id="6b140-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6b140-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b140-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b140-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6b140-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b140-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6b140-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b140-119">Library</span></span><br/> | <dl> <span data-ttu-id="6b140-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b140-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6b140-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b140-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b140-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6b140-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
