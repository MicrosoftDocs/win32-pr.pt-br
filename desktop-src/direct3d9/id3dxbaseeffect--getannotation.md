---
description: Obtém o identificador de uma anotação.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'Método ID3DXBaseEffect:: GetAnnotation (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765120"
---
# <a name="id3dxbaseeffectgetannotation-method"></a><span data-ttu-id="beb54-103">Método ID3DXBaseEffect:: GetAnnotation</span><span class="sxs-lookup"><span data-stu-id="beb54-103">ID3DXBaseEffect::GetAnnotation method</span></span>

<span data-ttu-id="beb54-104">Obtém o identificador de uma anotação.</span><span class="sxs-lookup"><span data-stu-id="beb54-104">Gets the handle of an annotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="beb54-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="beb54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="beb54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb54-107">*hObject* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="beb54-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb54-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="beb54-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="beb54-109">Identificador de um parâmetro de técnica, de passagem ou de nível superior.</span><span class="sxs-lookup"><span data-stu-id="beb54-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="beb54-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="beb54-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="beb54-111">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="beb54-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb54-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="beb54-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="beb54-113">Índice de anotação.</span><span class="sxs-lookup"><span data-stu-id="beb54-113">Annotation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb54-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="beb54-114">Return value</span></span>

<span data-ttu-id="beb54-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="beb54-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="beb54-116">Retorna o identificador da anotação especificada ou **NULL** se o índice era inválido.</span><span class="sxs-lookup"><span data-stu-id="beb54-116">Returns the handle of the specified annotation, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="beb54-117">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="beb54-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="beb54-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="beb54-118">Remarks</span></span>

<span data-ttu-id="beb54-119">As anotações são dados específicos do usuário que podem ser anexados a qualquer técnica, passagem ou parâmetro.</span><span class="sxs-lookup"><span data-stu-id="beb54-119">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="beb54-120">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="beb54-120">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="beb54-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beb54-121">Requirements</span></span>



| <span data-ttu-id="beb54-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb54-122">Requirement</span></span> | <span data-ttu-id="beb54-123">Valor</span><span class="sxs-lookup"><span data-stu-id="beb54-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb54-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="beb54-124">Header</span></span><br/>  | <dl> <span data-ttu-id="beb54-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb54-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="beb54-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="beb54-126">Library</span></span><br/> | <dl> <span data-ttu-id="beb54-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beb54-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="beb54-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="beb54-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb54-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="beb54-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
