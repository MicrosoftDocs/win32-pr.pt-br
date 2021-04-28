---
description: 'Método ID3DXTextureShader:: GetConstantByName – Obtém uma constante procurando seu nome.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'Método ID3DXTextureShader:: GetConstantByName (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 825aca3f3227a340952092985f4730018fe316e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117654"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="7d71f-103">Método ID3DXTextureShader:: GetConstantByName</span><span class="sxs-lookup"><span data-stu-id="7d71f-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="7d71f-104">Obtém uma constante procurando seu nome.</span><span class="sxs-lookup"><span data-stu-id="7d71f-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d71f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d71f-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="7d71f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d71f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d71f-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7d71f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d71f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7d71f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7d71f-109">Um [identificador](handles.md) para a estrutura de dados pai.</span><span class="sxs-lookup"><span data-stu-id="7d71f-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="7d71f-110">Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7d71f-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7d71f-111">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7d71f-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d71f-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d71f-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7d71f-113">Uma cadeia de caracteres que contém o nome da constante.</span><span class="sxs-lookup"><span data-stu-id="7d71f-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d71f-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7d71f-114">Return value</span></span>

<span data-ttu-id="7d71f-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7d71f-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7d71f-116">Retorna um identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="7d71f-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d71f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d71f-117">Requirements</span></span>



| <span data-ttu-id="7d71f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d71f-118">Requirement</span></span> | <span data-ttu-id="7d71f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7d71f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d71f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d71f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7d71f-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d71f-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7d71f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d71f-122">Library</span></span><br/> | <dl> <span data-ttu-id="7d71f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d71f-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7d71f-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7d71f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d71f-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="7d71f-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
