---
description: Carregar uma textura de uma textura.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Função D3DX10LoadTextureFromTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298536"
---
# <a name="d3dx10loadtexturefromtexture-function"></a><span data-ttu-id="577f5-103">Função D3DX10LoadTextureFromTexture</span><span class="sxs-lookup"><span data-stu-id="577f5-103">D3DX10LoadTextureFromTexture function</span></span>

<span data-ttu-id="577f5-104">Carregar uma textura de uma textura.</span><span class="sxs-lookup"><span data-stu-id="577f5-104">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="577f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="577f5-105">Syntax</span></span>


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="577f5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="577f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577f5-107">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="577f5-107">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="577f5-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="577f5-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="577f5-109">Ponteiro para a textura de origem.</span><span class="sxs-lookup"><span data-stu-id="577f5-109">Pointer to the source texture.</span></span> <span data-ttu-id="577f5-110">Consulte [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="577f5-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="577f5-111">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="577f5-111">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="577f5-112">Tipo: **[ **\_ informações de \_ carregamento \_ de textura D3DX10**](d3dx10-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="577f5-112">Type: **[**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md)\***</span></span>

<span data-ttu-id="577f5-113">Ponteiro para parâmetros de carregamento de textura.</span><span class="sxs-lookup"><span data-stu-id="577f5-113">Pointer to texture loading parameters.</span></span> <span data-ttu-id="577f5-114">Consulte [**\_ informações de \_ carregamento \_ de textura do D3DX10**](d3dx10-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="577f5-114">See [**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="577f5-115">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="577f5-115">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="577f5-116">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="577f5-116">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="577f5-117">Ponteiro para a textura de destino.</span><span class="sxs-lookup"><span data-stu-id="577f5-117">Pointer to the destination texture.</span></span> <span data-ttu-id="577f5-118">Consulte a [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="577f5-118">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="577f5-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="577f5-119">Return value</span></span>

<span data-ttu-id="577f5-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="577f5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="577f5-121">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="577f5-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="577f5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="577f5-122">Requirements</span></span>



| <span data-ttu-id="577f5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="577f5-123">Requirement</span></span> | <span data-ttu-id="577f5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="577f5-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="577f5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="577f5-125">Header</span></span><br/> | <dl> <span data-ttu-id="577f5-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="577f5-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577f5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="577f5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577f5-128">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="577f5-128">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




