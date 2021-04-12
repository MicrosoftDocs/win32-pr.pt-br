---
description: Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura pesquisando sua semântica com uma pesquisa que não diferencia maiúsculas de minúsculas.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'Método ID3DXBaseEffect:: GetParameterBySemantic (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298825"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a><span data-ttu-id="2e414-103">Método ID3DXBaseEffect:: GetParameterBySemantic</span><span class="sxs-lookup"><span data-stu-id="2e414-103">ID3DXBaseEffect::GetParameterBySemantic method</span></span>

<span data-ttu-id="2e414-104">Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura pesquisando sua semântica com uma pesquisa que não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2e414-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its semantic with a case-insensitive search.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e414-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e414-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a><span data-ttu-id="2e414-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e414-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e414-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e414-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e414-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2e414-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2e414-109">Identificador do parâmetro ou **nulo** para parâmetros de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2e414-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="2e414-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2e414-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e414-111">*pSemantic* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e414-111">*pSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e414-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e414-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e414-113">Cadeia de caracteres que contém o nome semântico.</span><span class="sxs-lookup"><span data-stu-id="2e414-113">String containing the semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e414-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e414-114">Return value</span></span>

<span data-ttu-id="2e414-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2e414-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2e414-116">Retorna o identificador do primeiro parâmetro que corresponde à semântica especificada ou **NULL** se a semântica não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="2e414-116">Returns the handle of the first parameter that matches the specified semantic, or **NULL** if the semantic was not found.</span></span> <span data-ttu-id="2e414-117">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2e414-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e414-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e414-118">Requirements</span></span>



| <span data-ttu-id="2e414-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e414-119">Requirement</span></span> | <span data-ttu-id="2e414-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2e414-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e414-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e414-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2e414-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e414-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2e414-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e414-123">Library</span></span><br/> | <dl> <span data-ttu-id="2e414-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e414-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2e414-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e414-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e414-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2e414-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
