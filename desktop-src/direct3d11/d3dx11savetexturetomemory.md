---
title: Função D3DX11SaveTextureToMemory (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, CaptureTexture, SaveToXXXMemory (em que XXX é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Salve uma textura na memória.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- Função D3DX11SaveTextureToMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173114"
---
# <a name="d3dx11savetexturetomemory-function"></a><span data-ttu-id="e5ad4-106">Função D3DX11SaveTextureToMemory</span><span class="sxs-lookup"><span data-stu-id="e5ad4-106">D3DX11SaveTextureToMemory function</span></span>

> [!Note]  
> <span data-ttu-id="e5ad4-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="e5ad4-108">Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** , **SaveToXXXMemory** (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="e5ad4-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="e5ad4-109">Salve uma textura na memória.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-109">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ad4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5ad4-110">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e5ad4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5ad4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ad4-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="e5ad4-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ad4-113">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="e5ad4-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="e5ad4-114">Um ponteiro para um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="e5ad4-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-115">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="e5ad4-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="e5ad4-117">Ponteiro para a textura a ser salva.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-117">Pointer to the texture to be saved.</span></span> <span data-ttu-id="e5ad4-118">Consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="e5ad4-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-119">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-119">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-120">Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="e5ad4-120">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="e5ad4-121">O formato em que a textura será salva.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-121">The format the texture will be saved as.</span></span> <span data-ttu-id="e5ad4-122">Consulte [**\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="e5ad4-122">See [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-123">*ppDestBuf* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-123">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-124">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="e5ad4-124">Type: **[**LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="e5ad4-125">Endereço de um ponteiro para a memória que contém a textura salva.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-125">Address of a pointer to the memory containing the saved texture.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-127">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e5ad4-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e5ad4-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-128">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ad4-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5ad4-129">Return value</span></span>

<span data-ttu-id="e5ad4-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5ad4-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5ad4-131">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e5ad4-131">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ad4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5ad4-132">Requirements</span></span>



| <span data-ttu-id="e5ad4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5ad4-133">Requirement</span></span> | <span data-ttu-id="e5ad4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e5ad4-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ad4-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5ad4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e5ad4-136"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad4-136"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e5ad4-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5ad4-137">Library</span></span><br/> | <dl> <span data-ttu-id="e5ad4-138"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad4-138"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e5ad4-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5ad4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ad4-140">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="e5ad4-140">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

