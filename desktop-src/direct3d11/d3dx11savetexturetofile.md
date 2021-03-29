---
title: Função D3DX11SaveTextureToFile (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, CaptureTexture, SaveToXXXFile (em que XXX é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Para o cenário simplificado de criação de uma captura de tela de uma textura de destino de renderização, recomendamos que você use a biblioteca DirectXTK, SaveDDSTextureToFile ou SaveWICTextureToFile. Salvar uma textura em um arquivo.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- Função D3DX11SaveTextureToFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968620"
---
# <a name="d3dx11savetexturetofile-function"></a><span data-ttu-id="3efd5-107">Função D3DX11SaveTextureToFile</span><span class="sxs-lookup"><span data-stu-id="3efd5-107">D3DX11SaveTextureToFile function</span></span>

> [!Note]  
> <span data-ttu-id="3efd5-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3efd5-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="3efd5-109">Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** , **SaveToXXXFile** (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="3efd5-109">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="3efd5-110">Para o cenário simplificado de criação de uma captura de tela de uma textura de destino de renderização, recomendamos que você use a biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SaveDDSTextureToFile** ou **SaveWICTextureToFile**.</span><span class="sxs-lookup"><span data-stu-id="3efd5-110">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SaveDDSTextureToFile** or **SaveWICTextureToFile**.</span></span>

 

<span data-ttu-id="3efd5-111">Salvar uma textura em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3efd5-111">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3efd5-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3efd5-112">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="3efd5-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3efd5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3efd5-114">*pContext*</span><span class="sxs-lookup"><span data-stu-id="3efd5-114">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="3efd5-115">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="3efd5-115">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="3efd5-116">Um ponteiro para um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="3efd5-116">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="3efd5-117">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3efd5-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3efd5-118">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="3efd5-118">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="3efd5-119">Ponteiro para a textura a ser salva.</span><span class="sxs-lookup"><span data-stu-id="3efd5-119">Pointer to the texture to be saved.</span></span> <span data-ttu-id="3efd5-120">Consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="3efd5-120">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="3efd5-121">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3efd5-121">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3efd5-122">Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="3efd5-122">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="3efd5-123">O formato em que a textura será salva (consulte [**o \_ \_ \_ formato de arquivo de imagem D3DX11**](d3dx11-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="3efd5-123">The format the texture will be saved as (see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)).</span></span> <span data-ttu-id="3efd5-124">D3DX11 \_ IFF \_ DDS é o formato preferencial, pois é a única opção que dá suporte a todos os formatos no [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3efd5-124">D3DX11\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="3efd5-125">*pDestFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3efd5-125">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3efd5-126">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3efd5-126">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3efd5-127">Nome do arquivo de saída de destino em que a textura será salva.</span><span class="sxs-lookup"><span data-stu-id="3efd5-127">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="3efd5-128">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3efd5-128">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3efd5-129">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3efd5-129">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3efd5-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3efd5-130">Return value</span></span>

<span data-ttu-id="3efd5-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3efd5-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3efd5-132">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md); Use o valor de retorno para ver se o *DestFormat* tem suporte.</span><span class="sxs-lookup"><span data-stu-id="3efd5-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="3efd5-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="3efd5-133">Remarks</span></span>

<span data-ttu-id="3efd5-134">O **D3DX11SaveTextureToFile** grava a estrutura [**\_ \_ DXT10 de cabeçalho DDS**](/windows/desktop/direct3ddds/dds-header-dxt10) extra para a textura de entrada somente se necessário (por exemplo, porque a textura de entrada está no formato RGB padrão (sRGB)).</span><span class="sxs-lookup"><span data-stu-id="3efd5-134">**D3DX11SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="3efd5-135">Se **D3DX11SaveTextureToFile** gravar a estrutura **de \_ \_ DXT10 do cabeçalho do DDS** , ele definirá o membro **dwFourCC** da estrutura de [**\_ PIXELFORMAT do DDS**](/windows/desktop/direct3ddds/dds-pixelformat) para a textura a ser **DX10** para indicar o prescense do cabeçalho estendido **\_ \_ DXT10 do cabeçalho DDS** .</span><span class="sxs-lookup"><span data-stu-id="3efd5-135">If **D3DX11SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="3efd5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3efd5-136">Requirements</span></span>



| <span data-ttu-id="3efd5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3efd5-137">Requirement</span></span> | <span data-ttu-id="3efd5-138">Valor</span><span class="sxs-lookup"><span data-stu-id="3efd5-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3efd5-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3efd5-139">Header</span></span><br/>  | <dl> <span data-ttu-id="3efd5-140"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3efd5-140"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3efd5-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3efd5-141">Library</span></span><br/> | <dl> <span data-ttu-id="3efd5-142"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3efd5-142"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3efd5-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="3efd5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3efd5-144">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="3efd5-144">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

