---
description: Obtenha uma constante da tabela de constantes.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'Método ID3DXTextureShader:: getconstantelement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173029"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a><span data-ttu-id="c1547-103">Método ID3DXTextureShader:: getconstantelement</span><span class="sxs-lookup"><span data-stu-id="c1547-103">ID3DXTextureShader::GetConstantElement method</span></span>

<span data-ttu-id="c1547-104">Obtenha uma constante da tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="c1547-104">Get a constant from the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1547-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1547-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="c1547-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1547-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1547-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1547-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c1547-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c1547-109">Um [identificador](handles.md) para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="c1547-109">A [handle](handles.md) to the array of constants.</span></span> <span data-ttu-id="c1547-110">Esse valor não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c1547-110">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c1547-111">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c1547-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1547-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1547-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1547-113">Índice de base zero do elemento na tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="c1547-113">Zero-based index of the element in the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1547-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1547-114">Return value</span></span>

<span data-ttu-id="c1547-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c1547-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c1547-116">Retorna um identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="c1547-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1547-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1547-117">Remarks</span></span>

<span data-ttu-id="c1547-118">Para obter uma constante que não faz parte de uma matriz, use [**ID3DXTextureShader:: getconstant**](id3dxtextureshader--getconstant.md) ou [**ID3DXTextureShader:: GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="c1547-118">To get a constant that is not part of an array, use [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) or [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1547-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1547-119">Requirements</span></span>



| <span data-ttu-id="c1547-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1547-120">Requirement</span></span> | <span data-ttu-id="c1547-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c1547-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1547-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1547-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c1547-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1547-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c1547-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1547-124">Library</span></span><br/> | <dl> <span data-ttu-id="c1547-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1547-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c1547-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1547-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1547-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c1547-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
