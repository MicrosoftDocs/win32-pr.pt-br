---
title: Estrutura de _BITMAPINFOHEADER
description: A \_ estrutura BITMAPINFOHEADER define o formato de um quadro de vídeo.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- Estrutura de _BITMAPINFOHEADER Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763395"
---
# <a name="_bitmapinfoheader-structure"></a><span data-ttu-id="909c9-104">\_Estrutura BITMAPINFOHEADER</span><span class="sxs-lookup"><span data-stu-id="909c9-104">\_BITMAPINFOHEADER structure</span></span>

<span data-ttu-id="909c9-105">A estrutura **\_ BITMAPINFOHEADER** define o formato de um quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="909c9-105">The **\_BITMAPINFOHEADER** structure defines the format of a video frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="909c9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="909c9-106">Syntax</span></span>


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="909c9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="909c9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="909c9-108">**bidimensional**</span><span class="sxs-lookup"><span data-stu-id="909c9-108">**biSize**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-109">Especifica o número de bytes exigidos pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="909c9-109">Specifies the number of bytes required by the structure.</span></span>

</dd> <dt>

<span data-ttu-id="909c9-110">**bilargura**</span><span class="sxs-lookup"><span data-stu-id="909c9-110">**biWidth**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-111">Especifica a largura do bitmap, em pixels.</span><span class="sxs-lookup"><span data-stu-id="909c9-111">Specifies the width of the bitmap, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="909c9-112">**biHeight**</span><span class="sxs-lookup"><span data-stu-id="909c9-112">**biHeight**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-113">Especifica a altura do bitmap, em pixels.</span><span class="sxs-lookup"><span data-stu-id="909c9-113">Specifies the height of the bitmap, in pixels.</span></span> <span data-ttu-id="909c9-114">Se a **interheight** for positiva, o bitmap será um DIB de baixo para cima e sua origem será o canto inferior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="909c9-114">If **biHeight** is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner.</span></span> <span data-ttu-id="909c9-115">Se a **interheight** for negativa, o bitmap será um DIB de cima para baixo e sua origem será o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="909c9-115">If **biHeight** is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.</span></span> <span data-ttu-id="909c9-116">Se a **interheight** for negativa, indicando um DIB de cima para baixo, a **biCompression** deverá ser bi \_ RGB ou bi \_ BITFIELDS.</span><span class="sxs-lookup"><span data-stu-id="909c9-116">If **biHeight** is negative, indicating a top-down DIB, **biCompression** must be either BI\_RGB or BI\_BITFIELDS.</span></span> <span data-ttu-id="909c9-117">Os DIBs de cima para baixo não podem ser compactados.</span><span class="sxs-lookup"><span data-stu-id="909c9-117">Top-down DIBs cannot be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="909c9-118">**monoplans**</span><span class="sxs-lookup"><span data-stu-id="909c9-118">**biPlanes**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-119">Especifica o número de planos para o dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="909c9-119">Specifies the number of planes for the target device.</span></span> <span data-ttu-id="909c9-120">Esse valor deve ser definido como 1.</span><span class="sxs-lookup"><span data-stu-id="909c9-120">This value must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="909c9-121">**biBitCount**</span><span class="sxs-lookup"><span data-stu-id="909c9-121">**biBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-122">Especifica o número de bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="909c9-122">Specifies the number of bits per pixel.</span></span> <span data-ttu-id="909c9-123">O membro **biBitCount** da estrutura **BITMAPINFOHEADER** determina o número de bits que definem cada pixel e o número máximo de cores no bitmap.</span><span class="sxs-lookup"><span data-stu-id="909c9-123">The **biBitCount** member of the **BITMAPINFOHEADER** structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap.</span></span> <span data-ttu-id="909c9-124">Esse membro deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="909c9-124">This member must be one of the following values.</span></span>



| <span data-ttu-id="909c9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="909c9-125">Value</span></span> | <span data-ttu-id="909c9-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="909c9-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="909c9-127">1</span><span class="sxs-lookup"><span data-stu-id="909c9-127">1</span></span>     | <span data-ttu-id="909c9-128">O bitmap é monocromático e o membro bmiColors contém duas entradas.</span><span class="sxs-lookup"><span data-stu-id="909c9-128">The bitmap is monochrome, and the bmiColors member contains two entries.</span></span> <span data-ttu-id="909c9-129">Cada bit na matriz de bitmap representa um pixel.</span><span class="sxs-lookup"><span data-stu-id="909c9-129">Each bit in the bitmap array represents a pixel.</span></span> <span data-ttu-id="909c9-130">Se o bit estiver claro, o pixel será exibido com a cor da primeira entrada na tabela bmiColors; Se o bit for definido, o pixel terá a cor da segunda entrada na tabela.</span><span class="sxs-lookup"><span data-stu-id="909c9-130">If the bit is clear, the pixel is displayed with the color of the first entry in the bmiColors table; if the bit is set, the pixel has the color of the second entry in the table.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="909c9-131">2</span><span class="sxs-lookup"><span data-stu-id="909c9-131">2</span></span>     | <span data-ttu-id="909c9-132">O bitmap tem quatro valores de cor possíveis.</span><span class="sxs-lookup"><span data-stu-id="909c9-132">The bitmap has four possible color values.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="909c9-133">4</span><span class="sxs-lookup"><span data-stu-id="909c9-133">4</span></span>     | <span data-ttu-id="909c9-134">O bitmap tem um máximo de 16 cores e o membro bmiColors contém até 16 entradas.</span><span class="sxs-lookup"><span data-stu-id="909c9-134">The bitmap has a maximum of 16 colors, and the bmiColors member contains up to 16 entries.</span></span> <span data-ttu-id="909c9-135">Cada pixel no bitmap é representado por um índice de 4 bits na tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="909c9-135">Each pixel in the bitmap is represented by a 4-bit index into the color table.</span></span> <span data-ttu-id="909c9-136">Por exemplo, se o primeiro byte no bitmap for 0x1F, o byte representará dois pixels.</span><span class="sxs-lookup"><span data-stu-id="909c9-136">For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels.</span></span> <span data-ttu-id="909c9-137">O primeiro pixel contém a cor na segunda entrada de tabela e o segundo pixel contém a cor na décima primeira entrada da tabela.</span><span class="sxs-lookup"><span data-stu-id="909c9-137">The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="909c9-138">8</span><span class="sxs-lookup"><span data-stu-id="909c9-138">8</span></span>     | <span data-ttu-id="909c9-139">O bitmap tem um máximo de 256 cores e o membro bmiColors contém até 256 entradas.</span><span class="sxs-lookup"><span data-stu-id="909c9-139">The bitmap has a maximum of 256 colors, and the bmiColors member contains up to 256 entries.</span></span> <span data-ttu-id="909c9-140">Nesse caso, cada byte na matriz representa um único pixel.</span><span class="sxs-lookup"><span data-stu-id="909c9-140">In this case, each byte in the array represents a single pixel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="909c9-141">16</span><span class="sxs-lookup"><span data-stu-id="909c9-141">16</span></span>    | <span data-ttu-id="909c9-142">O bitmap tem um máximo de 2 ^ 16 cores.</span><span class="sxs-lookup"><span data-stu-id="909c9-142">The bitmap has a maximum of 2^16 colors.</span></span> <span data-ttu-id="909c9-143">Se o membro de bicompressão do BITMAPINFOHEADER for BI \_ RGB, o membro bmiColors será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="909c9-143">If the biCompression member of the BITMAPINFOHEADER is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="909c9-144">Cada palavra na matriz de bitmap representa um único pixel.</span><span class="sxs-lookup"><span data-stu-id="909c9-144">Each WORD in the bitmap array represents a single pixel.</span></span> <span data-ttu-id="909c9-145">As intensidades relativas de vermelho, verde e azul são representadas com 5 bits para cada componente de cor.</span><span class="sxs-lookup"><span data-stu-id="909c9-145">The relative intensities of red, green, and blue are represented with 5 bits for each color component.</span></span> <span data-ttu-id="909c9-146">O valor de Blue é, no mínimo, 5 bits, seguido de 5 bits cada para verde e vermelho.</span><span class="sxs-lookup"><span data-stu-id="909c9-146">The value for blue is in the least significant 5 bits, followed by 5 bits each for green and red.</span></span> <span data-ttu-id="909c9-147">O bit mais significativo não é usado.</span><span class="sxs-lookup"><span data-stu-id="909c9-147">The most significant bit is not used.</span></span> <span data-ttu-id="909c9-148">A tabela de cores bmiColors é usada para otimizar as cores usadas em dispositivos baseados em paleta e deve conter o número de entradas especificado pelo membro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="909c9-148">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span> |
| <span data-ttu-id="909c9-149">24</span><span class="sxs-lookup"><span data-stu-id="909c9-149">24</span></span>    | <span data-ttu-id="909c9-150">O bitmap tem um máximo de 2 ^ 24 cores e o membro bmiColors é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="909c9-150">The bitmap has a maximum of 2^24 colors, and the bmiColors member is **NULL**.</span></span> <span data-ttu-id="909c9-151">Cada terceto de 3 bytes na matriz de bitmap representa as intensidades relativas de azul, verde e vermelho, respectivamente, para um pixel.</span><span class="sxs-lookup"><span data-stu-id="909c9-151">Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="909c9-152">A tabela de cores bmiColors é usada para otimizar as cores usadas em dispositivos baseados em paleta e deve conter o número de entradas especificado pelo membro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="909c9-152">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="909c9-153">32</span><span class="sxs-lookup"><span data-stu-id="909c9-153">32</span></span>    | <span data-ttu-id="909c9-154">O bitmap tem um máximo de 2 ^ 32 cores.</span><span class="sxs-lookup"><span data-stu-id="909c9-154">The bitmap has a maximum of 2^32 colors.</span></span> <span data-ttu-id="909c9-155">Se o membro de bicompressão for BI \_ RGB, o membro bmiColors será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="909c9-155">If the biCompression member is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="909c9-156">Cada DWORD na matriz de bitmap representa as intensidades relativas de azul, verde e vermelho, respectivamente, para um pixel.</span><span class="sxs-lookup"><span data-stu-id="909c9-156">Each DWORD in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="909c9-157">O byte alto em cada DWORD não é usado.</span><span class="sxs-lookup"><span data-stu-id="909c9-157">The high byte in each DWORD is not used.</span></span> <span data-ttu-id="909c9-158">A tabela de cores bmiColors é usada para otimizar as cores usadas em dispositivos baseados em paleta e deve conter o número de entradas especificado pelo membro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="909c9-158">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="909c9-159">**bicompressão**</span><span class="sxs-lookup"><span data-stu-id="909c9-159">**biCompression**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-160">Especifica o tipo de compactação para um bitmap de parte inferior compactado (o DIBs superior não pode ser compactado).</span><span class="sxs-lookup"><span data-stu-id="909c9-160">Specifies the type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed).</span></span> <span data-ttu-id="909c9-161">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="909c9-161">This member can be the one of the following values.</span></span>



| <span data-ttu-id="909c9-162">Valor</span><span class="sxs-lookup"><span data-stu-id="909c9-162">Value</span></span>         | <span data-ttu-id="909c9-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="909c9-163">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="909c9-164">RGB de BI \_</span><span class="sxs-lookup"><span data-stu-id="909c9-164">BI\_RGB</span></span>       | <span data-ttu-id="909c9-165">Um formato descompactado.</span><span class="sxs-lookup"><span data-stu-id="909c9-165">An uncompressed format.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="909c9-166">\_BITFIELDS bi</span><span class="sxs-lookup"><span data-stu-id="909c9-166">BI\_BITFIELDS</span></span> | <span data-ttu-id="909c9-167">Especifica que o bitmap não é compactado e que a tabela de cores consiste em três máscaras de cor DWORD que especificam os componentes vermelho, verde e azul, respectivamente, de cada pixel.</span><span class="sxs-lookup"><span data-stu-id="909c9-167">Specifies that the bitmap is not compressed and that the color table consists of three DWORD color masks that specify the red, green, and blue components, respectively, of each pixel.</span></span> <span data-ttu-id="909c9-168">Isso é válido quando usado com bitmaps de 16-BPP e 32-bpp.</span><span class="sxs-lookup"><span data-stu-id="909c9-168">This is valid when used with 16-bpp and 32-bpp bitmaps.</span></span> <span data-ttu-id="909c9-169">Esse valor é válido no Microsoft Windows CE versão 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="909c9-169">This value is valid in Microsoft Windows CE version 2.0 and later.</span></span> |



 

</dd> <dt>

<span data-ttu-id="909c9-170">**biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="909c9-170">**biSizeImage**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-171">Especifica o tamanho da imagem, em bytes.</span><span class="sxs-lookup"><span data-stu-id="909c9-171">Specifies the size of the image, in bytes.</span></span> <span data-ttu-id="909c9-172">Isso pode ser definido como zero para \_ bitmaps RGB de BI.</span><span class="sxs-lookup"><span data-stu-id="909c9-172">This may be set to zero for BI\_RGB bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="909c9-173">**biXPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="909c9-173">**biXPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-174">Especifica a resolução horizontal, em pixels por medidor, do dispositivo de destino para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="909c9-174">Specifies the horizontal resolution, in pixels per meter, of the target device for the bitmap.</span></span> <span data-ttu-id="909c9-175">Um aplicativo pode usar esse valor para selecionar um bitmap de um grupo de recursos que melhor corresponda às características do dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="909c9-175">An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.</span></span>

</dd> <dt>

<span data-ttu-id="909c9-176">**biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="909c9-176">**biYPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-177">Especifica a resolução vertical, em pixels por medidor, do dispositivo de destino para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="909c9-177">Specifies the vertical resolution, in pixels per meter, of the target device for the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="909c9-178">**biClrUsed**</span><span class="sxs-lookup"><span data-stu-id="909c9-178">**biClrUsed**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-179">Especifica o número de índices de cores na tabela de cores que são realmente usados pelo bitmap.</span><span class="sxs-lookup"><span data-stu-id="909c9-179">Specifies the number of color indexes in the color table that are actually used by the bitmap.</span></span> <span data-ttu-id="909c9-180">Se esse valor for zero, o bitmap usará o número máximo de cores correspondentes ao valor do membro **biBitCount** para o modo de compactação especificado pela **biCompression**.</span><span class="sxs-lookup"><span data-stu-id="909c9-180">If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the **biBitCount** member for the compression mode specified by **biCompression**.</span></span>

</dd> <dt>

<span data-ttu-id="909c9-181">**biClrImportant**</span><span class="sxs-lookup"><span data-stu-id="909c9-181">**biClrImportant**</span></span>
</dt> <dd>

<span data-ttu-id="909c9-182">Especifica o número de índices de cores necessários para exibir o bitmap.</span><span class="sxs-lookup"><span data-stu-id="909c9-182">Specifies the number of color indexes required for displaying the bitmap.</span></span> <span data-ttu-id="909c9-183">Se esse valor for zero, todas as cores serão necessárias.</span><span class="sxs-lookup"><span data-stu-id="909c9-183">If this value is zero, all colors are required.</span></span>

<span data-ttu-id="909c9-184">Se biClrUsed for diferente de zero e o membro biBitCount for menor que 16, o membro biClrUsed especificará o número real de cores que o mecanismo de gráficos ou o driver de dispositivo acessa.</span><span class="sxs-lookup"><span data-stu-id="909c9-184">If biClrUsed is nonzero and the biBitCount member is less than 16, the biClrUsed member specifies the actual number of colors the graphics engine or device driver accesses.</span></span> <span data-ttu-id="909c9-185">Se biBitCount for 16 ou superior, o membro biClrUsed especificará o tamanho da tabela de cores usada para otimizar o desempenho das paletas de cores do sistema.</span><span class="sxs-lookup"><span data-stu-id="909c9-185">If biBitCount is 16 or greater, the biClrUsed member specifies the size of the color table used to optimize performance of the system color palettes.</span></span> <span data-ttu-id="909c9-186">Se biBitCount for igual a 16 ou 32, a paleta de cores ideal começará imediatamente após as três máscaras DWORD.</span><span class="sxs-lookup"><span data-stu-id="909c9-186">If biBitCount equals 16 or 32, the optimal color palette starts immediately following the three DWORD masks.</span></span>

<span data-ttu-id="909c9-187">Se o bitmap é um bitmap empacotado (um bitmap no qual a matriz de bitmap segue imediatamente a \_ estrutura BITMAPINFOHEADER e é referenciada por um único ponteiro), o membro biClrUsed deve ser zero ou o tamanho real da tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="909c9-187">If the bitmap is a packed bitmap (a bitmap in which the bitmap array immediately follows the \_BITMAPINFOHEADER structure and is referenced by a single pointer), the biClrUsed member must be either zero or the actual size of the color table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="909c9-188">Comentários</span><span class="sxs-lookup"><span data-stu-id="909c9-188">Remarks</span></span>

<span data-ttu-id="909c9-189">Essa estrutura está contida em uma estrutura **\_ VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="909c9-189">This structure is contained within a **\_VIDEOINFOHEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="909c9-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="909c9-190">Requirements</span></span>



| <span data-ttu-id="909c9-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="909c9-191">Requirement</span></span> | <span data-ttu-id="909c9-192">Valor</span><span class="sxs-lookup"><span data-stu-id="909c9-192">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="909c9-193">parâmetro</span><span class="sxs-lookup"><span data-stu-id="909c9-193">Header</span></span><br/> | <dl> <span data-ttu-id="909c9-194"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="909c9-194"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="909c9-195">Confira também</span><span class="sxs-lookup"><span data-stu-id="909c9-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="909c9-196">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="909c9-196">**Structures**</span></span>](structures.md)
</dt> <dt>

[<span data-ttu-id="909c9-197">**\_VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="909c9-197">**\_VIDEOINFOHEADER**</span></span>](-videoinfoheader.md)
</dt> </dl>

 

 





