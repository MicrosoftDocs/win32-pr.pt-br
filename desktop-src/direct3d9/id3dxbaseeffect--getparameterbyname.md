---
description: Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura procurando seu nome.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'Método ID3DXBaseEffect:: GetParameterByName (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f9f7457ffa3bba867d03cceb3521664fecc9d67d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930746"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a><span data-ttu-id="fcc4d-103">Método ID3DXBaseEffect:: GetParameterByName</span><span class="sxs-lookup"><span data-stu-id="fcc4d-103">ID3DXBaseEffect::GetParameterByName method</span></span>

<span data-ttu-id="fcc4d-104">Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura procurando seu nome.</span><span class="sxs-lookup"><span data-stu-id="fcc4d-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc4d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcc4d-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="fcc4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcc4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc4d-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc4d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc4d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fcc4d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fcc4d-109">Identificador do parâmetro ou **nulo** para parâmetros de nível superior.</span><span class="sxs-lookup"><span data-stu-id="fcc4d-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="fcc4d-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fcc4d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fcc4d-111">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc4d-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc4d-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcc4d-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcc4d-113">Cadeia de caracteres que contém o nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fcc4d-113">String containing the parameter name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc4d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcc4d-114">Return value</span></span>

<span data-ttu-id="fcc4d-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fcc4d-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fcc4d-116">Retorna o identificador do parâmetro especificado ou **NULL** se o índice era inválido.</span><span class="sxs-lookup"><span data-stu-id="fcc4d-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="fcc4d-117">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fcc4d-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc4d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcc4d-118">Requirements</span></span>



| <span data-ttu-id="fcc4d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc4d-119">Requirement</span></span> | <span data-ttu-id="fcc4d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fcc4d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc4d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcc4d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fcc4d-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc4d-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fcc4d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcc4d-123">Library</span></span><br/> | <dl> <span data-ttu-id="fcc4d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcc4d-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fcc4d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcc4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc4d-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fcc4d-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
