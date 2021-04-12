---
description: Descreve os formatos de arquivo de imagem com suporte. Consulte comentários para obter descrições desses formatos.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: Enumeração de D3DXIMAGE_FILEFORMAT (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298615"
---
# <a name="d3dximage_fileformat-enumeration"></a><span data-ttu-id="dc655-104">\_Enumeração de FILEformat D3DXIMAGE</span><span class="sxs-lookup"><span data-stu-id="dc655-104">D3DXIMAGE\_FILEFORMAT enumeration</span></span>

<span data-ttu-id="dc655-105">Descreve os formatos de arquivo de imagem com suporte.</span><span class="sxs-lookup"><span data-stu-id="dc655-105">Describes the supported image file formats.</span></span> <span data-ttu-id="dc655-106">Consulte comentários para obter descrições desses formatos.</span><span class="sxs-lookup"><span data-stu-id="dc655-106">See Remarks for descriptions of these formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc655-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc655-107">Syntax</span></span>


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a><span data-ttu-id="dc655-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="dc655-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dc655-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="dc655-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-110">Formato de arquivo de bitmap do Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="dc655-110">Windows bitmap (BMP) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ jpg**</span><span class="sxs-lookup"><span data-stu-id="dc655-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-112">Formato de arquivo compactado do JPEG (Joint Experts Group).</span><span class="sxs-lookup"><span data-stu-id="dc655-112">Joint Photographics Experts Group (JPEG) compressed file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**</span><span class="sxs-lookup"><span data-stu-id="dc655-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF\_TGA**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-114">Formato de arquivo de imagem Truevision (Targa ou TGA).</span><span class="sxs-lookup"><span data-stu-id="dc655-114">Truevision (Targa, or TGA) image file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ png**</span><span class="sxs-lookup"><span data-stu-id="dc655-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-116">Formato de arquivo PNG (Portable Network Graphics).</span><span class="sxs-lookup"><span data-stu-id="dc655-116">Portable Network Graphics (PNG) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="dc655-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-118">Formato de arquivo da superfície do DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="dc655-118">DirectDraw surface (DDS) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**</span><span class="sxs-lookup"><span data-stu-id="dc655-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF\_PPM**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-120">Formato de arquivo pixmap portátil (PPM).</span><span class="sxs-lookup"><span data-stu-id="dc655-120">Portable pixmap (PPM) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**\_DIB D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="dc655-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF\_DIB**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-122">Formato de arquivo DIB (bitmap independente de dispositivo) do Windows.</span><span class="sxs-lookup"><span data-stu-id="dc655-122">Windows device-independent bitmap (DIB) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**\_HDR D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="dc655-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF\_HDR**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-124">Formato de arquivo de intervalo dinâmico alto (HDR).</span><span class="sxs-lookup"><span data-stu-id="dc655-124">High dynamic range (HDR) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**</span><span class="sxs-lookup"><span data-stu-id="dc655-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF\_PFM**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-126">Formato de arquivo do mapa float portátil.</span><span class="sxs-lookup"><span data-stu-id="dc655-126">Portable float map file format.</span></span>

</dd> <dt>

<span data-ttu-id="dc655-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="dc655-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="dc655-128">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="dc655-128">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="dc655-129">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dc655-129">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="dc655-130">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="dc655-130">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc655-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc655-131">Remarks</span></span>

<span data-ttu-id="dc655-132">Funções que começam com D3DXLoadxxx dão suporte a todos os formatos listados.</span><span class="sxs-lookup"><span data-stu-id="dc655-132">Functions that begin with D3DXLoadxxx support all of the formats listed.</span></span> <span data-ttu-id="dc655-133">Funções que começam com D3DXSavexxx dão suporte a todos os formatos listados, exceto os formatos Truevision (. tga) e pixmap portátil (. ppm).</span><span class="sxs-lookup"><span data-stu-id="dc655-133">Functions that begin with D3DXSavexxx support all of the formats listed except the Truevision (.tga) and portable pixmap (.ppm) formats.</span></span>

<span data-ttu-id="dc655-134">A tabela a seguir lista os formatos de entrada e saída disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dc655-134">The following table lists the available input and output formats.</span></span>



| <span data-ttu-id="dc655-135">Extensão do arquivo</span><span class="sxs-lookup"><span data-stu-id="dc655-135">File Extension</span></span> | <span data-ttu-id="dc655-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc655-136">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc655-137">.bmp</span><span class="sxs-lookup"><span data-stu-id="dc655-137">.bmp</span></span>           | <span data-ttu-id="dc655-138">Formato de bitmap do Windows.</span><span class="sxs-lookup"><span data-stu-id="dc655-138">Windows bitmap format.</span></span> <span data-ttu-id="dc655-139">Contém um cabeçalho que descreve a resolução do dispositivo no qual o retângulo de pixels foi criado, as dimensões do retângulo, o tamanho da matriz de bits, uma paleta lógica e uma matriz de bits que define a relação entre os pixels na imagem de bitmap e as entradas na paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="dc655-139">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> |
| <span data-ttu-id="dc655-140">.dds</span><span class="sxs-lookup"><span data-stu-id="dc655-140">.dds</span></span>           | <span data-ttu-id="dc655-141">Formato do arquivo de superfície do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="dc655-141">DirectDraw Surface file format.</span></span> <span data-ttu-id="dc655-142">Armazena texturas, texturas de volume e mapas de ambiente cúbico, com ou sem os níveis de mipmap, e com ou sem a compactação de pixel.</span><span class="sxs-lookup"><span data-stu-id="dc655-142">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="dc655-143">Consulte [DDS](../direct3ddds/dx-graphics-dds.md).</span><span class="sxs-lookup"><span data-stu-id="dc655-143">See [DDS](../direct3ddds/dx-graphics-dds.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="dc655-144">.dib</span><span class="sxs-lookup"><span data-stu-id="dc655-144">.dib</span></span>           | <span data-ttu-id="dc655-145">DIB do Windows.</span><span class="sxs-lookup"><span data-stu-id="dc655-145">Windows DIB.</span></span> <span data-ttu-id="dc655-146">Contém uma matriz de bits combinada com estruturas que especificam a largura e a altura da imagem de bitmap, o formato de cor do dispositivo no qual a imagem foi criada e a resolução do dispositivo usado para criar essa imagem.</span><span class="sxs-lookup"><span data-stu-id="dc655-146">Contains an array of bits combined with structures that specify width and height of the bitmapped image, color format of the device where the image was created, and resolution of the device used to create that image.</span></span>                                                                                                              |
| <span data-ttu-id="dc655-147">. HDR</span><span class="sxs-lookup"><span data-stu-id="dc655-147">.hdr</span></span>           | <span data-ttu-id="dc655-148">Formato HDR.</span><span class="sxs-lookup"><span data-stu-id="dc655-148">HDR format.</span></span> <span data-ttu-id="dc655-149">Codifica cada pixel como uma cor de RGBE de 32 bits, com 8 bits de mantissa para vermelho, verde e azul, e um expoente de 8 bits compartilhado.</span><span class="sxs-lookup"><span data-stu-id="dc655-149">Encodes each pixel as an RGBE 32-bit color, with 8 bits of mantissa for red, green, and blue, and a shared 8-bit exponent.</span></span> <span data-ttu-id="dc655-150">Cada canal é compactado separadamente com RLE (codificação de comprimento de execução).</span><span class="sxs-lookup"><span data-stu-id="dc655-150">Each channel is separately compressed with run-length encoding (RLE).</span></span>                                                                                                                                       |
| <span data-ttu-id="dc655-151">.jpg</span><span class="sxs-lookup"><span data-stu-id="dc655-151">.jpg</span></span>           | <span data-ttu-id="dc655-152">Padrão JPEG.</span><span class="sxs-lookup"><span data-stu-id="dc655-152">JPEG standard.</span></span> <span data-ttu-id="dc655-153">Especifica a compactação de variável de cores RGB de 24 bits e arquivos de documento de imagem TIFF de escala cinza de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="dc655-153">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="dc655-154">. PFM</span><span class="sxs-lookup"><span data-stu-id="dc655-154">.pfm</span></span>           | <span data-ttu-id="dc655-155">Formato de mapa float portátil.</span><span class="sxs-lookup"><span data-stu-id="dc655-155">Portable float map format.</span></span> <span data-ttu-id="dc655-156">Um formato de imagem de ponto flutuante não processado, sem nenhuma compactação.</span><span class="sxs-lookup"><span data-stu-id="dc655-156">A raw floating point image format, without any compression.</span></span> <span data-ttu-id="dc655-157">O cabeçalho do arquivo especifica a largura da imagem, a altura, o monocromático ou a cor e a ordem das palavras do computador.</span><span class="sxs-lookup"><span data-stu-id="dc655-157">The file header specifies image width, height, monochrome or color, and machine word order.</span></span> <span data-ttu-id="dc655-158">Os dados de pixel são armazenados como valores de ponto flutuante de 32 bits, com 3 valores por pixel para cor e um valor por pixel para monocromático.</span><span class="sxs-lookup"><span data-stu-id="dc655-158">Pixel data is stored as 32-bit floating point values, with 3 values per pixel for color, and one value per pixel for monochrome.</span></span>                                |
| <span data-ttu-id="dc655-159">.png</span><span class="sxs-lookup"><span data-stu-id="dc655-159">.png</span></span>           | <span data-ttu-id="dc655-160">Formato PNG.</span><span class="sxs-lookup"><span data-stu-id="dc655-160">PNG format.</span></span> <span data-ttu-id="dc655-161">Um formato de bitmap não proprietário usando compactação sem perdas.</span><span class="sxs-lookup"><span data-stu-id="dc655-161">A non-proprietary bitmap format using lossless compression.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="dc655-162">. ppm</span><span class="sxs-lookup"><span data-stu-id="dc655-162">.ppm</span></span>           | <span data-ttu-id="dc655-163">Formato pixmap portátil.</span><span class="sxs-lookup"><span data-stu-id="dc655-163">Portable Pixmap format.</span></span> <span data-ttu-id="dc655-164">Um formato de arquivo binário ou ASCII para imagens coloridas que inclui a altura e a largura da imagem e o valor do componente de cor máximo.</span><span class="sxs-lookup"><span data-stu-id="dc655-164">A binary or ASCII file format for color images that includes image height and width and the maximum color component value.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="dc655-165">.tga</span><span class="sxs-lookup"><span data-stu-id="dc655-165">.tga</span></span>           | <span data-ttu-id="dc655-166">Formato de adaptador gráfico Targa ou Truevision.</span><span class="sxs-lookup"><span data-stu-id="dc655-166">Targa or Truevision Graphics Adapter format.</span></span> <span data-ttu-id="dc655-167">Dá suporte a profundidades de 8, 15, 16, 24 e 32 bits, incluindo a escala de cinza de 8 bits e contém dados de paleta de cores opcionais, dados de origem (x, y) e de tamanho e dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="dc655-167">Supports depths of 8, 15, 16, 24, and 32 bits, including 8-bit gray scale, and contains optional color palette data, image (x, y) origin and size data, and pixel data.</span></span>                                                                                                                               |



 

<span data-ttu-id="dc655-168">Consulte [tipos de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obter mais informações sobre alguns desses formatos.</span><span class="sxs-lookup"><span data-stu-id="dc655-168">See [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc655-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc655-169">Requirements</span></span>



| <span data-ttu-id="dc655-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc655-170">Requirement</span></span> | <span data-ttu-id="dc655-171">Valor</span><span class="sxs-lookup"><span data-stu-id="dc655-171">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc655-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc655-172">Header</span></span><br/> | <dl> <span data-ttu-id="dc655-173"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc655-173"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc655-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc655-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc655-175">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="dc655-175">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
