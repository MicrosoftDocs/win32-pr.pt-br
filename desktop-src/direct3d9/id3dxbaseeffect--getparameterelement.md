---
description: Obtenha o identificador de um parâmetro de elemento de matriz.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'Método ID3DXBaseEffect:: ParameterElement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298824"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a><span data-ttu-id="0073b-103">Método ID3DXBaseEffect:: ParameterElement</span><span class="sxs-lookup"><span data-stu-id="0073b-103">ID3DXBaseEffect::GetParameterElement method</span></span>

<span data-ttu-id="0073b-104">Obtenha o identificador de um parâmetro de elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="0073b-104">Get the handle of an array element parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0073b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0073b-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a><span data-ttu-id="0073b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0073b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0073b-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0073b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0073b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0073b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0073b-109">Identificador da matriz.</span><span class="sxs-lookup"><span data-stu-id="0073b-109">Handle of the array.</span></span> <span data-ttu-id="0073b-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0073b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0073b-111">*ElementIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0073b-111">*ElementIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0073b-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0073b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0073b-113">Índice de elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="0073b-113">Array element index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0073b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0073b-114">Return value</span></span>

<span data-ttu-id="0073b-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0073b-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0073b-116">Retorna o identificador do parâmetro especificado ou **NULL** se HParameter ou ElementIndex for inválido.</span><span class="sxs-lookup"><span data-stu-id="0073b-116">Returns the handle of the specified parameter, or **NULL** if either hParameter or ElementIndex is invalid.</span></span> <span data-ttu-id="0073b-117">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0073b-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0073b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0073b-118">Remarks</span></span>

<span data-ttu-id="0073b-119">Esse método é usado para obter um elemento de um parâmetro que é uma matriz.</span><span class="sxs-lookup"><span data-stu-id="0073b-119">This method is used to get an element of a parameter that is an array.</span></span>

## <a name="requirements"></a><span data-ttu-id="0073b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0073b-120">Requirements</span></span>



| <span data-ttu-id="0073b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0073b-121">Requirement</span></span> | <span data-ttu-id="0073b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0073b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0073b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0073b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0073b-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0073b-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0073b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0073b-125">Library</span></span><br/> | <dl> <span data-ttu-id="0073b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0073b-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0073b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0073b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0073b-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0073b-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
