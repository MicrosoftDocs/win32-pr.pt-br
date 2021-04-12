---
description: Obtém o identificador de uma função procurando seu nome.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'Método ID3DXBaseEffect:: GetFunctionByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298831"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a><span data-ttu-id="7c1ec-103">Método ID3DXBaseEffect:: GetFunctionByName</span><span class="sxs-lookup"><span data-stu-id="7c1ec-103">ID3DXBaseEffect::GetFunctionByName method</span></span>

<span data-ttu-id="7c1ec-104">Obtém o identificador de uma função procurando seu nome.</span><span class="sxs-lookup"><span data-stu-id="7c1ec-104">Gets the handle of a function by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c1ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c1ec-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="7c1ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c1ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c1ec-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c1ec-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c1ec-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c1ec-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c1ec-109">Cadeia de caracteres que contém o nome da função.</span><span class="sxs-lookup"><span data-stu-id="7c1ec-109">String containing the function name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c1ec-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c1ec-110">Return value</span></span>

<span data-ttu-id="7c1ec-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7c1ec-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7c1ec-112">Retorna o identificador da função especificada ou **NULL** se o nome não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="7c1ec-112">Returns the handle of the specified function, or **NULL** if the name was not found.</span></span> <span data-ttu-id="7c1ec-113">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7c1ec-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1ec-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c1ec-114">Requirements</span></span>



| <span data-ttu-id="7c1ec-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c1ec-115">Requirement</span></span> | <span data-ttu-id="7c1ec-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7c1ec-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1ec-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c1ec-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7c1ec-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c1ec-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7c1ec-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c1ec-119">Library</span></span><br/> | <dl> <span data-ttu-id="7c1ec-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c1ec-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7c1ec-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c1ec-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1ec-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7c1ec-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
