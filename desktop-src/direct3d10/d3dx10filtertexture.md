---
description: Gera cadeia de mipmap usando um filtro de textura específico.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Função D3DX10FilterTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771628"
---
# <a name="d3dx10filtertexture-function"></a><span data-ttu-id="d4045-103">Função D3DX10FilterTexture</span><span class="sxs-lookup"><span data-stu-id="d4045-103">D3DX10FilterTexture function</span></span>

<span data-ttu-id="d4045-104">Gera cadeia de mipmap usando um filtro de textura específico.</span><span class="sxs-lookup"><span data-stu-id="d4045-104">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4045-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4045-105">Syntax</span></span>


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="d4045-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4045-107">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="d4045-107">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="d4045-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="d4045-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="d4045-109">O objeto de textura a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="d4045-109">The texture object to be filtered.</span></span> <span data-ttu-id="d4045-110">Consulte [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="d4045-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="d4045-111">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="d4045-111">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="d4045-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4045-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4045-113">O nível de mipmap cujos dados são usados para gerar o restante da cadeia de mipmap.</span><span class="sxs-lookup"><span data-stu-id="d4045-113">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="d4045-114">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="d4045-114">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="d4045-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4045-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4045-116">Sinalizadores que controlam como cada MipLevel é filtrado (ou D3DX10 \_ padrão para a \_ caixa de filtro D3DX10 \_ ).</span><span class="sxs-lookup"><span data-stu-id="d4045-116">Flags controlling how each miplevel is filtered (or D3DX10\_DEFAULT for D3DX10\_FILTER\_BOX).</span></span> <span data-ttu-id="d4045-117">Consulte [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="d4045-117">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4045-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4045-118">Return value</span></span>

<span data-ttu-id="d4045-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4045-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4045-120">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d4045-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4045-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4045-121">Requirements</span></span>



| <span data-ttu-id="d4045-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4045-122">Requirement</span></span> | <span data-ttu-id="d4045-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d4045-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4045-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4045-124">Header</span></span><br/> | <dl> <span data-ttu-id="d4045-125"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4045-125"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4045-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4045-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4045-127">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="d4045-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
