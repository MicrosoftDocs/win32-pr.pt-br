---
description: Obtém o identificador de uma passagem procurando seu nome.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'Método ID3DXBaseEffect:: GetPassByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780662"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a><span data-ttu-id="3ebb5-103">Método ID3DXBaseEffect:: GetPassByName</span><span class="sxs-lookup"><span data-stu-id="3ebb5-103">ID3DXBaseEffect::GetPassByName method</span></span>

<span data-ttu-id="3ebb5-104">Obtém o identificador de uma passagem procurando seu nome.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-104">Gets the handle of a pass by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ebb5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ebb5-105">Syntax</span></span>


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="3ebb5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ebb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ebb5-107">*hTechnique* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ebb5-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ebb5-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3ebb5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3ebb5-109">Identificador da técnica pai.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-109">Handle of the parent technique.</span></span> <span data-ttu-id="3ebb5-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3ebb5-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ebb5-111">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ebb5-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ebb5-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ebb5-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ebb5-113">Cadeia de caracteres que contém o nome da passagem.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-113">String containing the pass name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ebb5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ebb5-114">Return value</span></span>

<span data-ttu-id="3ebb5-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3ebb5-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3ebb5-116">Retorna o identificador da primeira passagem dentro da técnica especificada que tem o nome especificado ou **nulo** se o nome não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-116">Returns the handle of the first pass inside the specified technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="3ebb5-117">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3ebb5-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ebb5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ebb5-118">Requirements</span></span>



| <span data-ttu-id="3ebb5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ebb5-119">Requirement</span></span> | <span data-ttu-id="3ebb5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3ebb5-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ebb5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ebb5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3ebb5-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ebb5-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3ebb5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ebb5-123">Library</span></span><br/> | <dl> <span data-ttu-id="3ebb5-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ebb5-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3ebb5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ebb5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ebb5-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3ebb5-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
