---
description: 'Método ID3DXTextureShader:: getconstant – Obtém uma constante pesquisando seu índice.'
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: 'Método ID3DXTextureShader:: getconstant (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117664"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="2b665-103">Método ID3DXTextureShader:: getconstant</span><span class="sxs-lookup"><span data-stu-id="2b665-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="2b665-104">Obtém uma constante procurando seu índice.</span><span class="sxs-lookup"><span data-stu-id="2b665-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b665-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b665-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="2b665-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b665-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b665-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b665-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b665-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2b665-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2b665-109">Um [identificador](handles.md) para a estrutura de dados pai.</span><span class="sxs-lookup"><span data-stu-id="2b665-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="2b665-110">Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b665-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2b665-111">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2b665-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b665-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b665-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b665-113">Índice de base zero da constante.</span><span class="sxs-lookup"><span data-stu-id="2b665-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b665-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2b665-114">Return value</span></span>

<span data-ttu-id="2b665-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2b665-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2b665-116">Retorna um identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="2b665-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b665-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b665-117">Remarks</span></span>

<span data-ttu-id="2b665-118">Para obter uma constante de uma matriz de constantes, use [**ID3DXTextureShader:: Getconstantelement**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b665-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b665-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b665-119">Requirements</span></span>



| <span data-ttu-id="2b665-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b665-120">Requirement</span></span> | <span data-ttu-id="2b665-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2b665-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b665-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b665-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2b665-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b665-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2b665-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b665-124">Library</span></span><br/> | <dl> <span data-ttu-id="2b665-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b665-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2b665-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2b665-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b665-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2b665-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
