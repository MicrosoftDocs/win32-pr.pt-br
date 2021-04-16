---
title: Estrutura de DDS_HEADER (DDS. h)
description: Descreve um cabeçalho de arquivo DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER de estrutura DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765045"
---
# <a name="dds_header-structure"></a><span data-ttu-id="695d5-104">Estrutura do cabeçalho do DDS \_</span><span class="sxs-lookup"><span data-stu-id="695d5-104">DDS\_HEADER structure</span></span>

<span data-ttu-id="695d5-105">Descreve um cabeçalho de arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="695d5-105">Describes a DDS file header.</span></span>

## <a name="syntax"></a><span data-ttu-id="695d5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="695d5-106">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a><span data-ttu-id="695d5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="695d5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="695d5-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="695d5-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-109">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-110">Tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="695d5-110">Size of structure.</span></span> <span data-ttu-id="695d5-111">Esse membro deve ser definido como 124.</span><span class="sxs-lookup"><span data-stu-id="695d5-111">This member must be set to 124.</span></span>

</dd> <dt>

<span data-ttu-id="695d5-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="695d5-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-113">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-113">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-114">Sinalizadores para indicar quais membros contêm dados válidos.</span><span class="sxs-lookup"><span data-stu-id="695d5-114">Flags to indicate which members contain valid data.</span></span>



| <span data-ttu-id="695d5-115">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="695d5-115">Flag</span></span>              | <span data-ttu-id="695d5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="695d5-116">Description</span></span>                                                  | <span data-ttu-id="695d5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="695d5-117">Value</span></span>    |
|-------------------|--------------------------------------------------------------|----------|
| <span data-ttu-id="695d5-118">DDSD \_ Caps</span><span class="sxs-lookup"><span data-stu-id="695d5-118">DDSD\_CAPS</span></span>        | <span data-ttu-id="695d5-119">Necessário em cada arquivo. DDS.</span><span class="sxs-lookup"><span data-stu-id="695d5-119">Required in every .dds file.</span></span>                                 | <span data-ttu-id="695d5-120">0x1</span><span class="sxs-lookup"><span data-stu-id="695d5-120">0x1</span></span>      |
| <span data-ttu-id="695d5-121">altura de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="695d5-121">DDSD\_HEIGHT</span></span>      | <span data-ttu-id="695d5-122">Necessário em cada arquivo. DDS.</span><span class="sxs-lookup"><span data-stu-id="695d5-122">Required in every .dds file.</span></span>                                 | <span data-ttu-id="695d5-123">0x2</span><span class="sxs-lookup"><span data-stu-id="695d5-123">0x2</span></span>      |
| <span data-ttu-id="695d5-124">largura de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="695d5-124">DDSD\_WIDTH</span></span>       | <span data-ttu-id="695d5-125">Necessário em cada arquivo. DDS.</span><span class="sxs-lookup"><span data-stu-id="695d5-125">Required in every .dds file.</span></span>                                 | <span data-ttu-id="695d5-126">0x4</span><span class="sxs-lookup"><span data-stu-id="695d5-126">0x4</span></span>      |
| <span data-ttu-id="695d5-127">DDSD \_</span><span class="sxs-lookup"><span data-stu-id="695d5-127">DDSD\_PITCH</span></span>       | <span data-ttu-id="695d5-128">Necessário quando pitch é fornecido para uma textura não compactada.</span><span class="sxs-lookup"><span data-stu-id="695d5-128">Required when pitch is provided for an uncompressed texture.</span></span> | <span data-ttu-id="695d5-129">0x8</span><span class="sxs-lookup"><span data-stu-id="695d5-129">0x8</span></span>      |
| <span data-ttu-id="695d5-130">\_PIXELFORMAT DDSD</span><span class="sxs-lookup"><span data-stu-id="695d5-130">DDSD\_PIXELFORMAT</span></span> | <span data-ttu-id="695d5-131">Necessário em cada arquivo. DDS.</span><span class="sxs-lookup"><span data-stu-id="695d5-131">Required in every .dds file.</span></span>                                 | <span data-ttu-id="695d5-132">0x1000</span><span class="sxs-lookup"><span data-stu-id="695d5-132">0x1000</span></span>   |
| <span data-ttu-id="695d5-133">DDSD \_ MIPMAPCOUNT</span><span class="sxs-lookup"><span data-stu-id="695d5-133">DDSD\_MIPMAPCOUNT</span></span> | <span data-ttu-id="695d5-134">Necessário em uma textura mipmapped.</span><span class="sxs-lookup"><span data-stu-id="695d5-134">Required in a mipmapped texture.</span></span>                             | <span data-ttu-id="695d5-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="695d5-135">0x20000</span></span>  |
| <span data-ttu-id="695d5-136">DDSD \_ LINEARSIZE</span><span class="sxs-lookup"><span data-stu-id="695d5-136">DDSD\_LINEARSIZE</span></span>  | <span data-ttu-id="695d5-137">Necessário quando pitch é fornecido para uma textura compactada.</span><span class="sxs-lookup"><span data-stu-id="695d5-137">Required when pitch is provided for a compressed texture.</span></span>    | <span data-ttu-id="695d5-138">0x80000</span><span class="sxs-lookup"><span data-stu-id="695d5-138">0x80000</span></span>  |
| <span data-ttu-id="695d5-139">profundidade de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="695d5-139">DDSD\_DEPTH</span></span>       | <span data-ttu-id="695d5-140">Necessário em uma textura de profundidade.</span><span class="sxs-lookup"><span data-stu-id="695d5-140">Required in a depth texture.</span></span>                                 | <span data-ttu-id="695d5-141">0x800000</span><span class="sxs-lookup"><span data-stu-id="695d5-141">0x800000</span></span> |



 

> [!Note]  
> <span data-ttu-id="695d5-142">Ao gravar arquivos. DDS, você deve definir os sinalizadores DDSD \_ Caps e DDSD \_ PixelFormats e, para texturas Mipmapped, você também deve definir o \_ sinalizador DDSD MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="695d5-142">When you write .dds files, you should set the DDSD\_CAPS and DDSD\_PIXELFORMAT flags, and for mipmapped textures you should also set the DDSD\_MIPMAPCOUNT flag.</span></span> <span data-ttu-id="695d5-143">No entanto, ao ler um arquivo. DDS, você não deve contar com os \_ sinalizadores DDSD Caps, DDSD \_ PIXELFORMAT e DDSD \_ MIPMAPCOUNT sendo definidos porque alguns gravadores desse arquivo podem não definir esses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="695d5-143">However, when you read a .dds file, you should not rely on the DDSD\_CAPS, DDSD\_PIXELFORMAT, and DDSD\_MIPMAPCOUNT flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="695d5-144">O sinalizador de textura de sinalizadores de cabeçalho do DDS \_ \_ \_ , que é definido em DDS. h, é uma combinação de bit-a-or ou de DDSD \_ Caps, DDSD \_ Height, largura de DDSD \_ e sinalizadores de \_ PIXELFORMAT DDSD.</span><span class="sxs-lookup"><span data-stu-id="695d5-144">The DDS\_HEADER\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSD\_CAPS, DDSD\_HEIGHT, DDSD\_WIDTH, and DDSD\_PIXELFORMAT flags.</span></span>

<span data-ttu-id="695d5-145">O sinalizador MIPMAP do cabeçalho do DDS sinaliza \_ \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador DDSD MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="695d5-145">The DDS\_HEADER\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is equal to the DDSD\_MIPMAPCOUNT flag.</span></span>

<span data-ttu-id="695d5-146">O \_ sinalizador de volume flags de cabeçalho do DDS \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador de profundidade DDSD.</span><span class="sxs-lookup"><span data-stu-id="695d5-146">The DDS\_HEADER\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSD\_DEPTH flag.</span></span>

<span data-ttu-id="695d5-147">O sinalizador de densidade dos sinalizadores de cabeçalho do DDS \_ \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador de densidade DDSD.</span><span class="sxs-lookup"><span data-stu-id="695d5-147">The DDS\_HEADER\_FLAGS\_PITCH flag, which is defined in Dds.h, is equal to the DDSD\_PITCH flag.</span></span>

<span data-ttu-id="695d5-148">O sinalizador LINEARSIZE do cabeçalho do DDS sinaliza \_ \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador DDSD LINEARSIZE.</span><span class="sxs-lookup"><span data-stu-id="695d5-148">The DDS\_HEADER\_FLAGS\_LINEARSIZE flag, which is defined in Dds.h, is equal to the DDSD\_LINEARSIZE flag.</span></span>

</dd> <dt>

<span data-ttu-id="695d5-149">**dwHeight**</span><span class="sxs-lookup"><span data-stu-id="695d5-149">**dwHeight**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-150">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-150">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-151">Altura da superfície (em pixels).</span><span class="sxs-lookup"><span data-stu-id="695d5-151">Surface height (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="695d5-152">**dwWidth**</span><span class="sxs-lookup"><span data-stu-id="695d5-152">**dwWidth**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-153">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-153">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-154">Largura da superfície (em pixels).</span><span class="sxs-lookup"><span data-stu-id="695d5-154">Surface width (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="695d5-155">**dwPitchOrLinearSize**</span><span class="sxs-lookup"><span data-stu-id="695d5-155">**dwPitchOrLinearSize**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-156">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-156">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-157">A densidade ou o número de bytes por linha de varredura em uma textura não compactada; o número total de bytes na textura de nível superior para uma textura compactada.</span><span class="sxs-lookup"><span data-stu-id="695d5-157">The pitch or number of bytes per scan line in an uncompressed texture; the total number of bytes in the top level texture for a compressed texture.</span></span> <span data-ttu-id="695d5-158">Para obter informações sobre como calcular o timbre, consulte a seção de layout de arquivo DDS do [Guia de programação do DDS](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="695d5-158">For information about how to compute the pitch, see the DDS File Layout section of the [Programming Guide for DDS](dx-graphics-dds-pguide.md).</span></span>

</dd> <dt>

<span data-ttu-id="695d5-159">**dwDepth**</span><span class="sxs-lookup"><span data-stu-id="695d5-159">**dwDepth**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-160">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-160">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-161">Profundidade de uma textura de volume (em pixels), caso contrário, não utilizada.</span><span class="sxs-lookup"><span data-stu-id="695d5-161">Depth of a volume texture (in pixels), otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="695d5-162">**dwMipMapCount**</span><span class="sxs-lookup"><span data-stu-id="695d5-162">**dwMipMapCount**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-163">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-163">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-164">Número de níveis de mipmap, caso contrário, não utilizado.</span><span class="sxs-lookup"><span data-stu-id="695d5-164">Number of mipmap levels, otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="695d5-165">**dwReserved1 \[ 11\]**</span><span class="sxs-lookup"><span data-stu-id="695d5-165">**dwReserved1\[11\]**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-166">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-166">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-167">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="695d5-167">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="695d5-168">**ddspf**</span><span class="sxs-lookup"><span data-stu-id="695d5-168">**ddspf**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-169">Tipo: o **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**</span><span class="sxs-lookup"><span data-stu-id="695d5-169">Type: **[**DDS\_PIXELFORMAT**](dds-pixelformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-170">O formato de pixel (consulte [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).</span><span class="sxs-lookup"><span data-stu-id="695d5-170">The pixel format (see [**DDS\_PIXELFORMAT**](dds-pixelformat.md)).</span></span>

</dd> <dt>

<span data-ttu-id="695d5-171">**dwCaps**</span><span class="sxs-lookup"><span data-stu-id="695d5-171">**dwCaps**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-172">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-172">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-173">Especifica a complexidade das superfícies armazenadas.</span><span class="sxs-lookup"><span data-stu-id="695d5-173">Specifies the complexity of the surfaces stored.</span></span>



| <span data-ttu-id="695d5-174">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="695d5-174">Flag</span></span>             | <span data-ttu-id="695d5-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="695d5-175">Description</span></span>                                                                                                                              | <span data-ttu-id="695d5-176">Valor</span><span class="sxs-lookup"><span data-stu-id="695d5-176">Value</span></span>    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="695d5-177">DDSCAPS \_ complexo</span><span class="sxs-lookup"><span data-stu-id="695d5-177">DDSCAPS\_COMPLEX</span></span> | <span data-ttu-id="695d5-178">Adicional deve ser usado em qualquer arquivo que contenha mais de uma superfície (um mipmap, um mapa de ambiente cúbico ou uma textura de volume mipmapped).</span><span class="sxs-lookup"><span data-stu-id="695d5-178">Optional; must be used on any file that contains more than one surface (a mipmap, a cubic environment map, or mipmapped volume texture).</span></span> | <span data-ttu-id="695d5-179">0x8</span><span class="sxs-lookup"><span data-stu-id="695d5-179">0x8</span></span>      |
| <span data-ttu-id="695d5-180">DDSCAPS \_ MIPMAP</span><span class="sxs-lookup"><span data-stu-id="695d5-180">DDSCAPS\_MIPMAP</span></span>  | <span data-ttu-id="695d5-181">Adicional deve ser usado para um mipmap.</span><span class="sxs-lookup"><span data-stu-id="695d5-181">Optional; should be used for a mipmap.</span></span>                                                                                                   | <span data-ttu-id="695d5-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="695d5-182">0x400000</span></span> |
| <span data-ttu-id="695d5-183">\_textura DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="695d5-183">DDSCAPS\_TEXTURE</span></span> | <span data-ttu-id="695d5-184">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="695d5-184">Required</span></span>                                                                                                                                 | <span data-ttu-id="695d5-185">0x1000</span><span class="sxs-lookup"><span data-stu-id="695d5-185">0x1000</span></span>   |



 

> [!Note]  
> <span data-ttu-id="695d5-186">Ao gravar arquivos. DDS, você deve definir o sinalizador de \_ textura DDSCAPS e, para várias superfícies, você também deve definir o \_ sinalizador complexo DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="695d5-186">When you write .dds files, you should set the DDSCAPS\_TEXTURE flag, and for multiple surfaces you should also set the DDSCAPS\_COMPLEX flag.</span></span> <span data-ttu-id="695d5-187">No entanto, ao ler um arquivo. DDS, você não deve contar com a \_ textura DDSCAPS e os \_ sinalizadores complexos DDSCAPS estão sendo definidos porque alguns gravadores desse arquivo podem não definir esses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="695d5-187">However, when you read a .dds file, you should not rely on the DDSCAPS\_TEXTURE and DDSCAPS\_COMPLEX flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="695d5-188">O \_ \_ sinalizador MIPMAP dos sinalizadores de superfície do DDS \_ , que é definido em DDS. h, é uma combinação bit-a-or dos \_ sinalizadores DDSCAPS complexos e DDSCAPS \_ MIPMAP.</span><span class="sxs-lookup"><span data-stu-id="695d5-188">The DDS\_SURFACE\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS\_COMPLEX and DDSCAPS\_MIPMAP flags.</span></span>

<span data-ttu-id="695d5-189">O sinalizador de textura de sinalizadores de superfície de DDS \_ \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador de textura DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="695d5-189">The DDS\_SURFACE\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is equal to the DDSCAPS\_TEXTURE flag.</span></span>

<span data-ttu-id="695d5-190">O \_ sinalizador CUBEMAP dos sinalizadores de superfície do DDS \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador complexo DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="695d5-190">The DDS\_SURFACE\_FLAGS\_CUBEMAP flag, which is defined in Dds.h, is equal to the DDSCAPS\_COMPLEX flag.</span></span>

</dd> <dt>

<span data-ttu-id="695d5-191">**dwCaps2**</span><span class="sxs-lookup"><span data-stu-id="695d5-191">**dwCaps2**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-192">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-192">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-193">Detalhes adicionais sobre as superfícies armazenadas.</span><span class="sxs-lookup"><span data-stu-id="695d5-193">Additional detail about the surfaces stored.</span></span>



| <span data-ttu-id="695d5-194">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="695d5-194">Flag</span></span>                         | <span data-ttu-id="695d5-195">Descrição</span><span class="sxs-lookup"><span data-stu-id="695d5-195">Description</span></span>                                            | <span data-ttu-id="695d5-196">Valor</span><span class="sxs-lookup"><span data-stu-id="695d5-196">Value</span></span>    |
|------------------------------|--------------------------------------------------------|----------|
| <span data-ttu-id="695d5-197">DDSCAPS2 \_ CUBEMAP</span><span class="sxs-lookup"><span data-stu-id="695d5-197">DDSCAPS2\_CUBEMAP</span></span>            | <span data-ttu-id="695d5-198">Necessário para um mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="695d5-198">Required for a cube map.</span></span>                               | <span data-ttu-id="695d5-199">0x200</span><span class="sxs-lookup"><span data-stu-id="695d5-199">0x200</span></span>    |
| <span data-ttu-id="695d5-200">DDSCAPS2 \_ CUBEMAP \_ POSITIVEX</span><span class="sxs-lookup"><span data-stu-id="695d5-200">DDSCAPS2\_CUBEMAP\_POSITIVEX</span></span> | <span data-ttu-id="695d5-201">Necessário quando essas superfícies são armazenadas em um mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="695d5-201">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="695d5-202">0x400</span><span class="sxs-lookup"><span data-stu-id="695d5-202">0x400</span></span>    |
| <span data-ttu-id="695d5-203">DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX</span><span class="sxs-lookup"><span data-stu-id="695d5-203">DDSCAPS2\_CUBEMAP\_NEGATIVEX</span></span> | <span data-ttu-id="695d5-204">Necessário quando essas superfícies são armazenadas em um mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="695d5-204">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="695d5-205">0x800</span><span class="sxs-lookup"><span data-stu-id="695d5-205">0x800</span></span>    |
| <span data-ttu-id="695d5-206">DDSCAPS2 \_ CUBEMAP \_ positiva</span><span class="sxs-lookup"><span data-stu-id="695d5-206">DDSCAPS2\_CUBEMAP\_POSITIVEY</span></span> | <span data-ttu-id="695d5-207">Necessário quando essas superfícies são armazenadas em um mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="695d5-207">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="695d5-208">0x1000</span><span class="sxs-lookup"><span data-stu-id="695d5-208">0x1000</span></span>   |
| <span data-ttu-id="695d5-209">DDSCAPS2 \_ CUBEMAP \_ negativa</span><span class="sxs-lookup"><span data-stu-id="695d5-209">DDSCAPS2\_CUBEMAP\_NEGATIVEY</span></span> | <span data-ttu-id="695d5-210">Necessário quando essas superfícies são armazenadas em um mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="695d5-210">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="695d5-211">0x2000</span><span class="sxs-lookup"><span data-stu-id="695d5-211">0x2000</span></span>   |
| <span data-ttu-id="695d5-212">DDSCAPS2 \_ CUBEMAP \_ POSITIVEZ</span><span class="sxs-lookup"><span data-stu-id="695d5-212">DDSCAPS2\_CUBEMAP\_POSITIVEZ</span></span> | <span data-ttu-id="695d5-213">Necessário quando essas superfícies são armazenadas em um mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="695d5-213">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="695d5-214">0x4000</span><span class="sxs-lookup"><span data-stu-id="695d5-214">0x4000</span></span>   |
| <span data-ttu-id="695d5-215">DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ</span><span class="sxs-lookup"><span data-stu-id="695d5-215">DDSCAPS2\_CUBEMAP\_NEGATIVEZ</span></span> | <span data-ttu-id="695d5-216">Necessário quando essas superfícies são armazenadas em um mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="695d5-216">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="695d5-217">0x8000</span><span class="sxs-lookup"><span data-stu-id="695d5-217">0x8000</span></span>   |
| <span data-ttu-id="695d5-218">\_Volume DDSCAPS2</span><span class="sxs-lookup"><span data-stu-id="695d5-218">DDSCAPS2\_VOLUME</span></span>             | <span data-ttu-id="695d5-219">Necessário para uma textura de volume.</span><span class="sxs-lookup"><span data-stu-id="695d5-219">Required for a volume texture.</span></span>                         | <span data-ttu-id="695d5-220">0x200000</span><span class="sxs-lookup"><span data-stu-id="695d5-220">0x200000</span></span> |



 

<span data-ttu-id="695d5-221">O \_ sinalizador de POSITIVEX DDS CUBEMAP \_ , que é definido em DDS. h, é uma combinação bit-a-or de DDSCAPS2 \_ CUBEMAP e DDSCAPS2 CUBEMAP POSITIVEX \_ \_ flags.</span><span class="sxs-lookup"><span data-stu-id="695d5-221">The DDS\_CUBEMAP\_POSITIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEX flags.</span></span>

<span data-ttu-id="695d5-222">O \_ sinalizador de NEGATIVEX DDS CUBEMAP \_ , que é definido em DDS. h, é uma combinação bit-a-or de DDSCAPS2 \_ CUBEMAP e DDSCAPS2 CUBEMAP NEGATIVEX \_ \_ flags.</span><span class="sxs-lookup"><span data-stu-id="695d5-222">The DDS\_CUBEMAP\_NEGATIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEX flags.</span></span>

<span data-ttu-id="695d5-223">O \_ sinalizador de positiva CUBEMAP de DDS \_ , que é definido em DDS. h, é uma combinação de bit-a-or ou DDSCAPS2 \_ CUBEMAP e DDSCAPS2 \_ CUBEMAP de \_ sinalizadores positivos.</span><span class="sxs-lookup"><span data-stu-id="695d5-223">The DDS\_CUBEMAP\_POSITIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEY flags.</span></span>

<span data-ttu-id="695d5-224">O \_ sinalizador de \_ negativo CUBEMAP de DDS, que é definido em DDS. h, é uma combinação de bit-a-or ou DDSCAPS2 \_ CUBEMAP e DDSCAPS2 \_ CUBEMAP de \_ sinalizadores negativos.</span><span class="sxs-lookup"><span data-stu-id="695d5-224">The DDS\_CUBEMAP\_NEGATIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEY flags.</span></span>

<span data-ttu-id="695d5-225">O \_ sinalizador de POSITIVEZ DDS CUBEMAP \_ , que é definido em DDS. h, é uma combinação bit-a-or de DDSCAPS2 \_ CUBEMAP e DDSCAPS2 CUBEMAP POSITIVEZ \_ \_ flags.</span><span class="sxs-lookup"><span data-stu-id="695d5-225">The DDS\_CUBEMAP\_POSITIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEZ flags.</span></span>

<span data-ttu-id="695d5-226">O \_ sinalizador de NEGATIVEZ DDS CUBEMAP \_ , que é definido em DDS. h, é uma combinação bit-a-or de DDSCAPS2 \_ CUBEMAP e DDSCAPS2 CUBEMAP NEGATIVEZ \_ \_ flags.</span><span class="sxs-lookup"><span data-stu-id="695d5-226">The DDS\_CUBEMAP\_NEGATIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="695d5-227">O sinalizador de CUBEMAP de DDS \_ \_ , que é definido em DDS. h, é uma combinação de bit-a-or ou de DDS \_ CUBEMAP \_ POSITIVEX, DDS \_ CUBEMAP \_ NEGATIVEX, DDS \_ CUBEMAP \_ positivo, DDS \_ CUBEMAP \_ negativo, DDS \_ CUBEMAP \_ POSITIVEZ e DDSCAPS2 CUBEMAP \_ NEGATIVEZ \_ flags.</span><span class="sxs-lookup"><span data-stu-id="695d5-227">The DDS\_CUBEMAP\_ALLFACES flag, which is defined in Dds.h, is a bitwise-OR combination of the DDS\_CUBEMAP\_POSITIVEX, DDS\_CUBEMAP\_NEGATIVEX, DDS\_CUBEMAP\_POSITIVEY, DDS\_CUBEMAP\_NEGATIVEY, DDS\_CUBEMAP\_POSITIVEZ, and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="695d5-228">O \_ sinalizador de volume de sinalizadores DDS \_ , que é definido em DDS. h, é igual ao \_ sinalizador de volume DDSCAPS2.</span><span class="sxs-lookup"><span data-stu-id="695d5-228">The DDS\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSCAPS2\_VOLUME flag.</span></span>

> [!Note]  
> <span data-ttu-id="695d5-229">Embora o Direct3D 9 ofereça suporte a mapas de cubos parciais, o Direct3D 10, o 10,1 e o 11 exigem que você defina todas as seis faces do mapa de cubos (ou seja, você deve definir o DDS \_ CUBEMAP \_ ).</span><span class="sxs-lookup"><span data-stu-id="695d5-229">Although Direct3D 9 supports partial cube-maps, Direct3D 10, 10.1, and 11 require that you define all six cube-map faces (that is, you must set DDS\_CUBEMAP\_ALLFACES).</span></span>

 

</dd> <dt>

<span data-ttu-id="695d5-230">**dwCaps3**</span><span class="sxs-lookup"><span data-stu-id="695d5-230">**dwCaps3**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-231">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-231">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-232">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="695d5-232">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="695d5-233">**dwCaps4**</span><span class="sxs-lookup"><span data-stu-id="695d5-233">**dwCaps4**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-234">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-234">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-235">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="695d5-235">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="695d5-236">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="695d5-236">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="695d5-237">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="695d5-237">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="695d5-238">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="695d5-238">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="695d5-239">Comentários</span><span class="sxs-lookup"><span data-stu-id="695d5-239">Remarks</span></span>

<span data-ttu-id="695d5-240">Inclua sinalizadores no **dwFlags** para os membros da estrutura que contêm dados válidos.</span><span class="sxs-lookup"><span data-stu-id="695d5-240">Include flags in **dwFlags** for the members of the structure that contain valid data.</span></span>

<span data-ttu-id="695d5-241">Use essa estrutura em combinação com um [**\_ cabeçalho DDS \_ DXT10**](dds-header-dxt10.md) para armazenar uma matriz de recursos em um arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="695d5-241">Use this structure in combination with a [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="695d5-242">Para obter mais informações, consulte [matrizes de textura](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="695d5-242">For more information, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="695d5-243">**DDS \_ O cabeçalho** é idêntico à estrutura DDSURFACEDESC2 do DirectDraw sem dependências do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="695d5-243">**DDS\_HEADER** is identical to the DirectDraw DDSURFACEDESC2 structure without DirectDraw dependencies.</span></span>

## <a name="requirements"></a><span data-ttu-id="695d5-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="695d5-244">Requirements</span></span>



| <span data-ttu-id="695d5-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="695d5-245">Requirement</span></span> | <span data-ttu-id="695d5-246">Valor</span><span class="sxs-lookup"><span data-stu-id="695d5-246">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="695d5-247">parâmetro</span><span class="sxs-lookup"><span data-stu-id="695d5-247">Header</span></span><br/> | <dl> <span data-ttu-id="695d5-248"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="695d5-248"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="695d5-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="695d5-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="695d5-250">Referência para DDS</span><span class="sxs-lookup"><span data-stu-id="695d5-250">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

