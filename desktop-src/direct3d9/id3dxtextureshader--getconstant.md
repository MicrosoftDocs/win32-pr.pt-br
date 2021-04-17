---
description: Obtém uma constante procurando seu índice.
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
ms.openlocfilehash: 24f3f78d5970d5e3beda119ca40a565f45d0d950
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811712"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="c41fe-103">Método ID3DXTextureShader:: getconstant</span><span class="sxs-lookup"><span data-stu-id="c41fe-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="c41fe-104">Obtém uma constante procurando seu índice.</span><span class="sxs-lookup"><span data-stu-id="c41fe-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c41fe-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="c41fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c41fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c41fe-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c41fe-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41fe-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c41fe-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c41fe-109">Um [identificador](handles.md) para a estrutura de dados pai.</span><span class="sxs-lookup"><span data-stu-id="c41fe-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="c41fe-110">Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c41fe-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c41fe-111">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c41fe-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41fe-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c41fe-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c41fe-113">Índice de base zero da constante.</span><span class="sxs-lookup"><span data-stu-id="c41fe-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c41fe-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c41fe-114">Return value</span></span>

<span data-ttu-id="c41fe-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c41fe-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c41fe-116">Retorna um identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="c41fe-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="c41fe-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c41fe-117">Remarks</span></span>

<span data-ttu-id="c41fe-118">Para obter uma constante de uma matriz de constantes, use [**ID3DXTextureShader:: Getconstantelement**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="c41fe-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c41fe-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c41fe-119">Requirements</span></span>



| <span data-ttu-id="c41fe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c41fe-120">Requirement</span></span> | <span data-ttu-id="c41fe-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c41fe-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c41fe-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c41fe-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c41fe-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c41fe-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c41fe-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c41fe-124">Library</span></span><br/> | <dl> <span data-ttu-id="c41fe-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c41fe-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c41fe-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c41fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c41fe-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c41fe-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
