---
title: Função D3DX11LoadTextureFromTexture (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, é recomendável usar a biblioteca DirectXTex, redimensionar, converter, compactar, descompactar e/ou CopyRectangle. Carregar uma textura de uma textura.
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- Função D3DX11LoadTextureFromTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968622"
---
# <a name="d3dx11loadtexturefromtexture-function"></a><span data-ttu-id="b43d2-106">Função D3DX11LoadTextureFromTexture</span><span class="sxs-lookup"><span data-stu-id="b43d2-106">D3DX11LoadTextureFromTexture function</span></span>

> [!Note]  
> <span data-ttu-id="b43d2-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b43d2-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="b43d2-108">Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **redimensione**, **converta**, **compacte**, **Descompacte** e/ou **CopyRectangle**.</span><span class="sxs-lookup"><span data-stu-id="b43d2-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **Resize**, **Convert**, **Compress**, **Decompress**, and/or **CopyRectangle**.</span></span>

 

<span data-ttu-id="b43d2-109">Carregar uma textura de uma textura.</span><span class="sxs-lookup"><span data-stu-id="b43d2-109">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b43d2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b43d2-110">Syntax</span></span>


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="b43d2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b43d2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b43d2-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="b43d2-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="b43d2-113">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="b43d2-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="b43d2-114">Um ponteiro para um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="b43d2-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="b43d2-115">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="b43d2-115">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="b43d2-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="b43d2-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="b43d2-117">Ponteiro para a textura de origem.</span><span class="sxs-lookup"><span data-stu-id="b43d2-117">Pointer to the source texture.</span></span> <span data-ttu-id="b43d2-118">Consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="b43d2-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="b43d2-119">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="b43d2-119">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b43d2-120">Tipo: **[ **\_ informações de \_ carregamento \_ de textura D3DX11**](d3dx11-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b43d2-120">Type: **[**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md)\***</span></span>

<span data-ttu-id="b43d2-121">Ponteiro para parâmetros de carregamento de textura.</span><span class="sxs-lookup"><span data-stu-id="b43d2-121">Pointer to texture loading parameters.</span></span> <span data-ttu-id="b43d2-122">Consulte [**\_ informações de \_ carregamento \_ de textura do D3DX11**](d3dx11-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="b43d2-122">See [**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="b43d2-123">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="b43d2-123">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="b43d2-124">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="b43d2-124">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="b43d2-125">Ponteiro para a textura de destino.</span><span class="sxs-lookup"><span data-stu-id="b43d2-125">Pointer to the destination texture.</span></span> <span data-ttu-id="b43d2-126">Consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="b43d2-126">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b43d2-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b43d2-127">Return value</span></span>

<span data-ttu-id="b43d2-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b43d2-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b43d2-129">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b43d2-129">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b43d2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b43d2-130">Requirements</span></span>



| <span data-ttu-id="b43d2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b43d2-131">Requirement</span></span> | <span data-ttu-id="b43d2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b43d2-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b43d2-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b43d2-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b43d2-134"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b43d2-134"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b43d2-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b43d2-135">Library</span></span><br/> | <dl> <span data-ttu-id="b43d2-136"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b43d2-136"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b43d2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b43d2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b43d2-138">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="b43d2-138">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





