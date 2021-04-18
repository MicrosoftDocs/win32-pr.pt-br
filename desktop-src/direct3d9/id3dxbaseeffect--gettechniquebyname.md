---
description: Obtém o identificador de uma técnica pesquisando seu nome.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'Método ID3DXBaseEffect:: GetTechniqueByName (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787762"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a><span data-ttu-id="6926f-103">Método ID3DXBaseEffect:: GetTechniqueByName</span><span class="sxs-lookup"><span data-stu-id="6926f-103">ID3DXBaseEffect::GetTechniqueByName method</span></span>

<span data-ttu-id="6926f-104">Obtém o identificador de uma técnica pesquisando seu nome.</span><span class="sxs-lookup"><span data-stu-id="6926f-104">Gets the handle of a technique by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6926f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6926f-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="6926f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6926f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6926f-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6926f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6926f-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6926f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6926f-109">Cadeia de caracteres que contém o nome da técnica.</span><span class="sxs-lookup"><span data-stu-id="6926f-109">String containing the technique name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6926f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6926f-110">Return value</span></span>

<span data-ttu-id="6926f-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6926f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6926f-112">Retorna o identificador da primeira técnica que tem o nome especificado ou **NULL** se o nome não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6926f-112">Returns the handle of the first technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="6926f-113">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6926f-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6926f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6926f-114">Requirements</span></span>



| <span data-ttu-id="6926f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6926f-115">Requirement</span></span> | <span data-ttu-id="6926f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6926f-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6926f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6926f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6926f-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6926f-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6926f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6926f-119">Library</span></span><br/> | <dl> <span data-ttu-id="6926f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6926f-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6926f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6926f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6926f-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6926f-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
