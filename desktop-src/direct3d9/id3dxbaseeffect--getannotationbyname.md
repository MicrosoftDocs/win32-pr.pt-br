---
description: Obtém o identificador de uma anotação pesquisando seu nome.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'Método ID3DXBaseEffect:: GetAnnotationByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763513"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a><span data-ttu-id="fada9-103">Método ID3DXBaseEffect:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="fada9-103">ID3DXBaseEffect::GetAnnotationByName method</span></span>

<span data-ttu-id="fada9-104">Obtém o identificador de uma anotação pesquisando seu nome.</span><span class="sxs-lookup"><span data-stu-id="fada9-104">Gets the handle of an annotation by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="fada9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fada9-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="fada9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fada9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fada9-107">*hObject* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fada9-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fada9-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fada9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fada9-109">Identificador de um parâmetro de técnica, de passagem ou de nível superior.</span><span class="sxs-lookup"><span data-stu-id="fada9-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="fada9-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fada9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fada9-111">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fada9-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fada9-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fada9-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fada9-113">Cadeia de caracteres que contém o nome da anotação.</span><span class="sxs-lookup"><span data-stu-id="fada9-113">String containing the annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fada9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fada9-114">Return value</span></span>

<span data-ttu-id="fada9-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fada9-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fada9-116">Retorna o identificador da anotação especificada ou **NULL** se o nome não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="fada9-116">Returns the handle of the specified annotation, or **NULL** if the name was not found.</span></span> <span data-ttu-id="fada9-117">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fada9-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fada9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fada9-118">Requirements</span></span>



| <span data-ttu-id="fada9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fada9-119">Requirement</span></span> | <span data-ttu-id="fada9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fada9-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fada9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fada9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fada9-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fada9-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="fada9-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fada9-123">Library</span></span><br/> | <dl> <span data-ttu-id="fada9-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fada9-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fada9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fada9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fada9-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fada9-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
