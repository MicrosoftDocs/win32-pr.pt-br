---
description: Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'Método ID3DXBaseEffect:: getParameter (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012176"
---
# <a name="id3dxbaseeffectgetparameter-method"></a><span data-ttu-id="24e08-103">Método ID3DXBaseEffect:: getParameter</span><span class="sxs-lookup"><span data-stu-id="24e08-103">ID3DXBaseEffect::GetParameter method</span></span>

<span data-ttu-id="24e08-104">Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura.</span><span class="sxs-lookup"><span data-stu-id="24e08-104">Gets the handle of a top-level parameter or a structure member parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24e08-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="24e08-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24e08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24e08-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24e08-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24e08-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="24e08-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="24e08-109">Identificador do parâmetro ou **nulo** para parâmetros de nível superior.</span><span class="sxs-lookup"><span data-stu-id="24e08-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="24e08-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="24e08-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="24e08-111">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="24e08-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24e08-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24e08-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24e08-113">Índice de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="24e08-113">Parameter index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24e08-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24e08-114">Return value</span></span>

<span data-ttu-id="24e08-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="24e08-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="24e08-116">Retorna o identificador do parâmetro especificado ou **NULL** se o índice era inválido.</span><span class="sxs-lookup"><span data-stu-id="24e08-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="24e08-117">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="24e08-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24e08-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24e08-118">Requirements</span></span>



| <span data-ttu-id="24e08-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="24e08-119">Requirement</span></span> | <span data-ttu-id="24e08-120">Valor</span><span class="sxs-lookup"><span data-stu-id="24e08-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="24e08-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24e08-121">Header</span></span><br/>  | <dl> <span data-ttu-id="24e08-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e08-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="24e08-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24e08-123">Library</span></span><br/> | <dl> <span data-ttu-id="24e08-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24e08-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="24e08-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="24e08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e08-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="24e08-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
