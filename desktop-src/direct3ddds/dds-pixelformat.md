---
title: Estrutura de DDS_PIXELFORMAT (DDS. h)
description: Formato de pixel de superfície.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT de estrutura DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815505"
---
# <a name="dds_pixelformat-structure"></a><span data-ttu-id="6be07-104">Estrutura de PIXELFORMAT do DDS \_</span><span class="sxs-lookup"><span data-stu-id="6be07-104">DDS\_PIXELFORMAT structure</span></span>

<span data-ttu-id="6be07-105">Formato de pixel de superfície.</span><span class="sxs-lookup"><span data-stu-id="6be07-105">Surface pixel format.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be07-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6be07-106">Syntax</span></span>


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a><span data-ttu-id="6be07-107">Membros</span><span class="sxs-lookup"><span data-stu-id="6be07-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6be07-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="6be07-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="6be07-109">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6be07-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6be07-110">Tamanho da estrutura; Defina como 32 (bytes).</span><span class="sxs-lookup"><span data-stu-id="6be07-110">Structure size; set to 32 (bytes).</span></span>

</dd> <dt>

<span data-ttu-id="6be07-111">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="6be07-111">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6be07-112">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6be07-112">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6be07-113">Valores que indicam que tipo de dados está na superfície.</span><span class="sxs-lookup"><span data-stu-id="6be07-113">Values which indicate what type of data is in the surface.</span></span>



| <span data-ttu-id="6be07-114">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="6be07-114">Flag</span></span>              | <span data-ttu-id="6be07-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6be07-115">Description</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="6be07-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6be07-116">Value</span></span>   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| <span data-ttu-id="6be07-117">DDPF \_ ALPHAPIXELS</span><span class="sxs-lookup"><span data-stu-id="6be07-117">DDPF\_ALPHAPIXELS</span></span> | <span data-ttu-id="6be07-118">A textura contém dados alfa; **dwRGBAlphaBitMask** contém dados válidos.</span><span class="sxs-lookup"><span data-stu-id="6be07-118">Texture contains alpha data; **dwRGBAlphaBitMask** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="6be07-119">0x1</span><span class="sxs-lookup"><span data-stu-id="6be07-119">0x1</span></span>     |
| <span data-ttu-id="6be07-120">DDPF \_ alfa</span><span class="sxs-lookup"><span data-stu-id="6be07-120">DDPF\_ALPHA</span></span>       | <span data-ttu-id="6be07-121">Usado em alguns arquivos DDS mais antigos para dados não compactados somente do canal alfa (dwRGBBitCount contém o canal alfa BitCount; dwABitMask contém dados válidos)</span><span class="sxs-lookup"><span data-stu-id="6be07-121">Used in some older DDS files for alpha channel only uncompressed data (dwRGBBitCount contains the alpha channel bitcount; dwABitMask contains valid data)</span></span>                                                                                  | <span data-ttu-id="6be07-122">0x2</span><span class="sxs-lookup"><span data-stu-id="6be07-122">0x2</span></span>     |
| <span data-ttu-id="6be07-123">DDPF \_ FOURCC</span><span class="sxs-lookup"><span data-stu-id="6be07-123">DDPF\_FOURCC</span></span>      | <span data-ttu-id="6be07-124">A textura contém dados RGB compactados; **dwFourCC** contém dados válidos.</span><span class="sxs-lookup"><span data-stu-id="6be07-124">Texture contains compressed RGB data; **dwFourCC** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="6be07-125">0x4</span><span class="sxs-lookup"><span data-stu-id="6be07-125">0x4</span></span>     |
| <span data-ttu-id="6be07-126">DDPF \_ RGB</span><span class="sxs-lookup"><span data-stu-id="6be07-126">DDPF\_RGB</span></span>         | <span data-ttu-id="6be07-127">A textura contém dados RGB descompactados; **dwRGBBitCount** e as máscaras RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contêm dados válidos.</span><span class="sxs-lookup"><span data-stu-id="6be07-127">Texture contains uncompressed RGB data; **dwRGBBitCount** and the RGB masks (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contain valid data.</span></span>                                                                                           | <span data-ttu-id="6be07-128">0x40</span><span class="sxs-lookup"><span data-stu-id="6be07-128">0x40</span></span>    |
| <span data-ttu-id="6be07-129">\_YUV DDPF</span><span class="sxs-lookup"><span data-stu-id="6be07-129">DDPF\_YUV</span></span>         | <span data-ttu-id="6be07-130">Usado em alguns arquivos DDS mais antigos para dados não compactados YUV (dwRGBBitCount contém a contagem de bits YUV; dwRBitMask contém a máscara Y, dwGBitMask contém a máscara U, dwBBitMask contém a máscara V)</span><span class="sxs-lookup"><span data-stu-id="6be07-130">Used in some older DDS files for YUV uncompressed data (dwRGBBitCount contains the YUV bit count; dwRBitMask contains the Y mask, dwGBitMask contains the U mask, dwBBitMask contains the V mask)</span></span>                                          | <span data-ttu-id="6be07-131">0x200</span><span class="sxs-lookup"><span data-stu-id="6be07-131">0x200</span></span>   |
| <span data-ttu-id="6be07-132">luminância de DDPF \_</span><span class="sxs-lookup"><span data-stu-id="6be07-132">DDPF\_LUMINANCE</span></span>   | <span data-ttu-id="6be07-133">Usado em alguns arquivos DDS mais antigos para dados descompactados de cor de canal único (dwRGBBitCount contém a contagem de bits de canal de luminescência; dwRBitMask contém a máscara de canal).</span><span class="sxs-lookup"><span data-stu-id="6be07-133">Used in some older DDS files for single channel color uncompressed data (dwRGBBitCount contains the luminance channel bit count; dwRBitMask contains the channel mask).</span></span> <span data-ttu-id="6be07-134">Pode ser combinado com DDPF \_ ALPHAPIXELS para um arquivo DDS de dois canais.</span><span class="sxs-lookup"><span data-stu-id="6be07-134">Can be combined with DDPF\_ALPHAPIXELS for a two channel DDS file.</span></span> | <span data-ttu-id="6be07-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="6be07-135">0x20000</span></span> |



 

</dd> <dt>

<span data-ttu-id="6be07-136">**dwFourCC**</span><span class="sxs-lookup"><span data-stu-id="6be07-136">**dwFourCC**</span></span>
</dt> <dd>

<span data-ttu-id="6be07-137">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6be07-137">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6be07-138">Códigos de quatro caracteres para especificar formatos compactados ou personalizados.</span><span class="sxs-lookup"><span data-stu-id="6be07-138">Four-character codes for specifying compressed or custom formats.</span></span> <span data-ttu-id="6be07-139">Os valores possíveis incluem: *DXT1*, *DXT2*, *DXT3*, *DXT4* ou *DXT5*.</span><span class="sxs-lookup"><span data-stu-id="6be07-139">Possible values include: *DXT1*, *DXT2*, *DXT3*, *DXT4*, or *DXT5*.</span></span> <span data-ttu-id="6be07-140">Um FourCC de DX10 indica o prescense do cabeçalho [**DDS \_ \_ DXT10**](dds-header-dxt10.md) Header e o membro dxgiFormat dessa estrutura indica o formato verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="6be07-140">A FourCC of DX10 indicates the prescense of the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extended header, and the dxgiFormat member of that structure indicates the true format.</span></span> <span data-ttu-id="6be07-141">Ao usar um código de quatro caracteres, o dwFlags deve incluir *DDPF \_ FOURCC*.</span><span class="sxs-lookup"><span data-stu-id="6be07-141">When using a four-character code, dwFlags must include *DDPF\_FOURCC*.</span></span>

</dd> <dt>

<span data-ttu-id="6be07-142">**dwRGBBitCount**</span><span class="sxs-lookup"><span data-stu-id="6be07-142">**dwRGBBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="6be07-143">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6be07-143">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6be07-144">Número de bits em um formato RGB (possivelmente incluindo alfa).</span><span class="sxs-lookup"><span data-stu-id="6be07-144">Number of bits in an RGB (possibly including alpha) format.</span></span> <span data-ttu-id="6be07-145">Válido quando **dwFlags** inclui *DDPF \_ RGB*, *DDPF \_ luminescência* ou *DDPF \_ YUV*.</span><span class="sxs-lookup"><span data-stu-id="6be07-145">Valid when **dwFlags** includes *DDPF\_RGB*, *DDPF\_LUMINANCE*, or *DDPF\_YUV*.</span></span>

</dd> <dt>

<span data-ttu-id="6be07-146">**dwRBitMask**</span><span class="sxs-lookup"><span data-stu-id="6be07-146">**dwRBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="6be07-147">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6be07-147">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6be07-148">Máscara vermelha (ou lumiannce ou Y) para a leitura de dados de cores.</span><span class="sxs-lookup"><span data-stu-id="6be07-148">Red (or lumiannce or Y) mask for reading color data.</span></span> <span data-ttu-id="6be07-149">Por exemplo, considerando o formato A8R8G8B8, a máscara vermelha seria 0x00ff0000.</span><span class="sxs-lookup"><span data-stu-id="6be07-149">For instance, given the A8R8G8B8 format, the red mask would be 0x00ff0000.</span></span>

</dd> <dt>

<span data-ttu-id="6be07-150">**dwGBitMask**</span><span class="sxs-lookup"><span data-stu-id="6be07-150">**dwGBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="6be07-151">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6be07-151">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6be07-152">Máscara verde (ou U) para leitura de dados de cor.</span><span class="sxs-lookup"><span data-stu-id="6be07-152">Green (or U) mask for reading color data.</span></span> <span data-ttu-id="6be07-153">Por exemplo, considerando o formato A8R8G8B8, a máscara verde seria 0x0000ff00.</span><span class="sxs-lookup"><span data-stu-id="6be07-153">For instance, given the A8R8G8B8 format, the green mask would be 0x0000ff00.</span></span>

</dd> <dt>

<span data-ttu-id="6be07-154">**dwBBitMask**</span><span class="sxs-lookup"><span data-stu-id="6be07-154">**dwBBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="6be07-155">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6be07-155">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6be07-156">Máscara azul (ou V) para leitura de dados de cor.</span><span class="sxs-lookup"><span data-stu-id="6be07-156">Blue (or V) mask for reading color data.</span></span> <span data-ttu-id="6be07-157">Por exemplo, considerando o formato A8R8G8B8, a máscara azul seria 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="6be07-157">For instance, given the A8R8G8B8 format, the blue mask would be 0x000000ff.</span></span>

</dd> <dt>

<span data-ttu-id="6be07-158">**dwABitMask**</span><span class="sxs-lookup"><span data-stu-id="6be07-158">**dwABitMask**</span></span>
</dt> <dd>

<span data-ttu-id="6be07-159">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6be07-159">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6be07-160">Máscara alfa para leitura de dados alfa.</span><span class="sxs-lookup"><span data-stu-id="6be07-160">Alpha mask for reading alpha data.</span></span> <span data-ttu-id="6be07-161">dwFlags deve incluir *DDPF \_ ALPHAPIXELS* ou *DDPF \_ Alpha*.</span><span class="sxs-lookup"><span data-stu-id="6be07-161">dwFlags must include *DDPF\_ALPHAPIXELS* or *DDPF\_ALPHA*.</span></span> <span data-ttu-id="6be07-162">Por exemplo, dado o formato A8R8G8B8, a máscara alfa seria 0xff000000.</span><span class="sxs-lookup"><span data-stu-id="6be07-162">For instance, given the A8R8G8B8 format, the alpha mask would be 0xff000000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6be07-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="6be07-163">Remarks</span></span>

<span data-ttu-id="6be07-164">Para armazenar formatos DXGI, como dados de ponto flutuante, use um **dwFlags** de DDPF \_ FOURCC e defina **dwFourCC** como ' d', ' X ', ' 1 ', ' 0 '.</span><span class="sxs-lookup"><span data-stu-id="6be07-164">To store DXGI formats such as floating-point data, use a **dwFlags** of DDPF\_FOURCC and set **dwFourCC** to 'D','X','1','0'.</span></span> <span data-ttu-id="6be07-165">Use o cabeçalho de extensão [**\_ \_ DXT10 de cabeçalho DDS**](dds-header-dxt10.md) para armazenar o formato dxgi no membro **dxgiFormat** .</span><span class="sxs-lookup"><span data-stu-id="6be07-165">Use the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extension header to store the DXGI format in the **dxgiFormat** member.</span></span>

<span data-ttu-id="6be07-166">Observe que há variantes não padrão de arquivos DDS em que **dwFlags** tem DDPF \_ FOURCC e o valor **dwFourCC** é definido diretamente para um valor de enumeração de formato D3DFORMAT ou dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="6be07-166">Note that there are non-standard variants of DDS files where **dwFlags** has DDPF\_FOURCC and the **dwFourCC** value is set directly to a D3DFORMAT or DXGI\_FORMAT enumeration value.</span></span> <span data-ttu-id="6be07-167">Não é possível desambiguar os valores de formato D3DFORMAT versus DXGI \_ usando esse esquema não padrão, portanto, o cabeçalho de extensão DX10 é recomendado.</span><span class="sxs-lookup"><span data-stu-id="6be07-167">It is not possible to disambiguate the D3DFORMAT versus DXGI\_FORMAT values using this non-standard scheme, so the DX10 extension header is recommended instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="6be07-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6be07-168">Requirements</span></span>



| <span data-ttu-id="6be07-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="6be07-169">Requirement</span></span> | <span data-ttu-id="6be07-170">Valor</span><span class="sxs-lookup"><span data-stu-id="6be07-170">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6be07-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6be07-171">Header</span></span><br/> | <dl> <span data-ttu-id="6be07-172"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="6be07-172"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6be07-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="6be07-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be07-174">Referência para DDS</span><span class="sxs-lookup"><span data-stu-id="6be07-174">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

