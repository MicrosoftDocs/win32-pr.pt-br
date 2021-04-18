---
description: Salvar uma textura em um arquivo.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Função D3DX10SaveTextureToFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764004"
---
# <a name="d3dx10savetexturetofile-function"></a><span data-ttu-id="db3b4-103">Função D3DX10SaveTextureToFile</span><span class="sxs-lookup"><span data-stu-id="db3b4-103">D3DX10SaveTextureToFile function</span></span>

<span data-ttu-id="db3b4-104">Salvar uma textura em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="db3b4-104">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="db3b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db3b4-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="db3b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db3b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db3b4-107">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db3b4-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db3b4-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="db3b4-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="db3b4-109">Ponteiro para a textura a ser salva.</span><span class="sxs-lookup"><span data-stu-id="db3b4-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="db3b4-110">Consulte a [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="db3b4-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="db3b4-111">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db3b4-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db3b4-112">Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="db3b4-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="db3b4-113">O formato em que a textura será salva (consulte [**o \_ \_ \_ formato de arquivo de imagem D3DX10**](d3dx10-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="db3b4-113">The format the texture will be saved as (see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)).</span></span> <span data-ttu-id="db3b4-114">D3DX10 \_ IFF \_ DDS é o formato preferencial, pois é a única opção que dá suporte a todos os formatos no [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="db3b4-114">D3DX10\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="db3b4-115">*pDestFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db3b4-115">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db3b4-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db3b4-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db3b4-117">Nome do arquivo de saída de destino em que a textura será salva.</span><span class="sxs-lookup"><span data-stu-id="db3b4-117">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="db3b4-118">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="db3b4-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="db3b4-119">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="db3b4-119">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db3b4-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db3b4-120">Return value</span></span>

<span data-ttu-id="db3b4-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db3b4-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db3b4-122">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md); Use o valor de retorno para ver se o *DestFormat* tem suporte.</span><span class="sxs-lookup"><span data-stu-id="db3b4-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="db3b4-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="db3b4-123">Remarks</span></span>

<span data-ttu-id="db3b4-124">O **D3DX10SaveTextureToFile** grava a estrutura [**\_ \_ DXT10 de cabeçalho DDS**](../direct3ddds/dds-header-dxt10.md) extra para a textura de entrada somente se necessário (por exemplo, porque a textura de entrada está no formato RGB padrão (sRGB)).</span><span class="sxs-lookup"><span data-stu-id="db3b4-124">**D3DX10SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](../direct3ddds/dds-header-dxt10.md) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="db3b4-125">Se **D3DX10SaveTextureToFile** gravar a estrutura **de \_ \_ DXT10 do cabeçalho do DDS** , ele definirá o membro **dwFourCC** da estrutura de [**\_ PIXELFORMAT do DDS**](../direct3ddds/dds-pixelformat.md) para a textura a ser **DX10** para indicar o prescense do cabeçalho estendido **\_ \_ DXT10 do cabeçalho DDS** .</span><span class="sxs-lookup"><span data-stu-id="db3b4-125">If **D3DX10SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="db3b4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db3b4-126">Requirements</span></span>



| <span data-ttu-id="db3b4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="db3b4-127">Requirement</span></span> | <span data-ttu-id="db3b4-128">Valor</span><span class="sxs-lookup"><span data-stu-id="db3b4-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db3b4-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db3b4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="db3b4-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="db3b4-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="db3b4-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db3b4-131">Library</span></span><br/> | <dl> <span data-ttu-id="db3b4-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db3b4-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="db3b4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="db3b4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3b4-134">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="db3b4-134">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="db3b4-135">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="db3b4-135">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
