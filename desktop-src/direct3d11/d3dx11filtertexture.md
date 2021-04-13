---
title: Função D3DX11FilterTexture (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, GenerateMipMaps e GenerateMipMaps3D. Gera cadeia de mipmap usando um filtro de textura específico.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- Função D3DX11FilterTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968626"
---
# <a name="d3dx11filtertexture-function"></a><span data-ttu-id="62c34-106">Função D3DX11FilterTexture</span><span class="sxs-lookup"><span data-stu-id="62c34-106">D3DX11FilterTexture function</span></span>

> [!Note]  
> <span data-ttu-id="62c34-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="62c34-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="62c34-108">Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GenerateMipMaps** e **GenerateMipMaps3D**.</span><span class="sxs-lookup"><span data-stu-id="62c34-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GenerateMipMaps** and **GenerateMipMaps3D**.</span></span>

 

<span data-ttu-id="62c34-109">Gera cadeia de mipmap usando um filtro de textura específico.</span><span class="sxs-lookup"><span data-stu-id="62c34-109">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c34-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62c34-110">Syntax</span></span>


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="62c34-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62c34-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c34-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="62c34-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="62c34-113">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="62c34-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="62c34-114">Um ponteiro para um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="62c34-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="62c34-115">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="62c34-115">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="62c34-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="62c34-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="62c34-117">O objeto de textura a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="62c34-117">The texture object to be filtered.</span></span> <span data-ttu-id="62c34-118">Consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="62c34-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="62c34-119">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="62c34-119">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="62c34-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62c34-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62c34-121">O nível de mipmap cujos dados são usados para gerar o restante da cadeia de mipmap.</span><span class="sxs-lookup"><span data-stu-id="62c34-121">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="62c34-122">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="62c34-122">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="62c34-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62c34-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62c34-124">Sinalizadores que controlam como cada MipLevel é filtrado (ou D3DX11 \_ padrão para o \_ filtro D3DX11 \_ linear).</span><span class="sxs-lookup"><span data-stu-id="62c34-124">Flags controlling how each miplevel is filtered (or D3DX11\_DEFAULT for D3DX11\_FILTER\_LINEAR).</span></span> <span data-ttu-id="62c34-125">Consulte [**\_ \_ sinalizador de filtro D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="62c34-125">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c34-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62c34-126">Return value</span></span>

<span data-ttu-id="62c34-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62c34-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62c34-128">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="62c34-128">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62c34-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62c34-129">Requirements</span></span>



| <span data-ttu-id="62c34-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c34-130">Requirement</span></span> | <span data-ttu-id="62c34-131">Valor</span><span class="sxs-lookup"><span data-stu-id="62c34-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c34-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62c34-132">Header</span></span><br/>  | <dl> <span data-ttu-id="62c34-133"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c34-133"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="62c34-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62c34-134">Library</span></span><br/> | <dl> <span data-ttu-id="62c34-135"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62c34-135"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="62c34-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="62c34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c34-137">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="62c34-137">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

