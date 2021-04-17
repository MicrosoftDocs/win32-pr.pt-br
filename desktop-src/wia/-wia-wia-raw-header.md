---
description: A \_ estrutura de cabeçalho bruto do WIA \_ define uma imagem no formato de dados brutos de um dispositivo e permite que os aplicativos usem o formato bruto em transferências do WIA (aquisição de imagem do Windows).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: Estrutura de WIA_RAW_HEADER (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798270"
---
# <a name="wia_raw_header-structure"></a><span data-ttu-id="84f91-103">\_Estrutura de \_ cabeçalho bruto WIA</span><span class="sxs-lookup"><span data-stu-id="84f91-103">WIA\_RAW\_HEADER structure</span></span>

<span data-ttu-id="84f91-104">A estrutura de **\_ \_ cabeçalho bruto do WIA** define uma imagem no formato de dados brutos de um dispositivo e permite que os aplicativos usem o formato bruto em transferências do WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="84f91-104">The **WIA\_RAW\_HEADER** structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f91-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84f91-105">Syntax</span></span>


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a><span data-ttu-id="84f91-106">Membros</span><span class="sxs-lookup"><span data-stu-id="84f91-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="84f91-107">**Tag**</span><span class="sxs-lookup"><span data-stu-id="84f91-107">**Tag**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-109">O nome do formato.</span><span class="sxs-lookup"><span data-stu-id="84f91-109">The name of the format.</span></span> <span data-ttu-id="84f91-110">Deve ser o ' WRAW ' literal (quatro caracteres ASCII de byte único).</span><span class="sxs-lookup"><span data-stu-id="84f91-110">This must be the literal 'WRAW' (four single byte ASCII characters).</span></span>

</dd> <dt>

<span data-ttu-id="84f91-111">**Versão**</span><span class="sxs-lookup"><span data-stu-id="84f91-111">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-112">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-112">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-113">A versão do formato bruto.</span><span class="sxs-lookup"><span data-stu-id="84f91-113">The version of the RAW format.</span></span> <span data-ttu-id="84f91-114">Sempre use 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="84f91-114">Always use 0x00010000.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-115">**Cabeçalhosize**</span><span class="sxs-lookup"><span data-stu-id="84f91-115">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-117">O total de bytes válidos no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="84f91-117">The total valid bytes in the header.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-118">**XRes**</span><span class="sxs-lookup"><span data-stu-id="84f91-118">**XRes**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-119">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-120">A resolução horizontal em pontos por polegada.</span><span class="sxs-lookup"><span data-stu-id="84f91-120">The horizontal resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-121">**YRes**</span><span class="sxs-lookup"><span data-stu-id="84f91-121">**YRes**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-123">A resolução vertical em pontos por polegada.</span><span class="sxs-lookup"><span data-stu-id="84f91-123">The vertical resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-124">**XExtent**</span><span class="sxs-lookup"><span data-stu-id="84f91-124">**XExtent**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-125">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-125">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-126">A largura da imagem em pixels.</span><span class="sxs-lookup"><span data-stu-id="84f91-126">The width of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-127">**YExtent**</span><span class="sxs-lookup"><span data-stu-id="84f91-127">**YExtent**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-128">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-128">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-129">A altura da imagem em pixels.</span><span class="sxs-lookup"><span data-stu-id="84f91-129">The height of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-130">**BytesPerLine**</span><span class="sxs-lookup"><span data-stu-id="84f91-130">**BytesPerLine**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-131">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-132">O número de bytes em uma linha de uma imagem descompactada.</span><span class="sxs-lookup"><span data-stu-id="84f91-132">The number of bytes in a line of an uncompressed image.</span></span> <span data-ttu-id="84f91-133">Use 0 quando os dados forem compactados para sinalizar que o número de bytes por linha é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="84f91-133">Use 0 when the data is compressed to signal that the number of bytes per line is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-134">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="84f91-134">**BitsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-135">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-135">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-136">O número total de bits por pixel para todos os canais do pixel.</span><span class="sxs-lookup"><span data-stu-id="84f91-136">The total number of bits per pixel for all the pixel's channels.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-137">**ChannelsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="84f91-137">**ChannelsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-138">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-139">O número de canais de cores em um pixel.</span><span class="sxs-lookup"><span data-stu-id="84f91-139">The number of color channels in a pixel.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-140">**DataType**</span><span class="sxs-lookup"><span data-stu-id="84f91-140">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-141">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-141">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-142">O \_ \_ tipo de dados IPA WIA da imagem.</span><span class="sxs-lookup"><span data-stu-id="84f91-142">The WIA\_IPA\_DATATYPE of the image.</span></span> <span data-ttu-id="84f91-143">Como \_ o formato IPA do WIA \_ é definido como WiaImgFmt \_ RAW, essa é uma lista de valores permitidos dos quais o aplicativo é escolhido.</span><span class="sxs-lookup"><span data-stu-id="84f91-143">Since WIA\_IPA\_FORMAT is set to WiaImgFmt\_RAW, this is a list of allowed values from which the application picks.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-144">**BitsPerChannel \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="84f91-144">**BitsPerChannel\[8\]**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-145">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="84f91-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-146">O número de bits em um canal, até um máximo de 8.</span><span class="sxs-lookup"><span data-stu-id="84f91-146">The number of bits in a channel, up to a maximum of 8.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-147">**Compactação**</span><span class="sxs-lookup"><span data-stu-id="84f91-147">**Compression**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-148">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-148">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-149">Um \_ \_ valor de compactação IPA WIA que especifica o tipo de compactação usado, se houver.</span><span class="sxs-lookup"><span data-stu-id="84f91-149">A WIA\_IPA\_COMPRESSION value specifying the type of compression used, if any.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-150">**PhotometricInterp**</span><span class="sxs-lookup"><span data-stu-id="84f91-150">**PhotometricInterp**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-151">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-151">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-152">Um \_ \_ valor INTERP IPA da multimetric do WIA \_ que especifica a interpretação fotométrica da imagem.</span><span class="sxs-lookup"><span data-stu-id="84f91-152">A WIA\_IPA\_PHOTOMETRIC\_INTERP value specifying the photometric interpretation of the image.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-153">**LineOrder**</span><span class="sxs-lookup"><span data-stu-id="84f91-153">**LineOrder**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-154">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-154">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-155">Um valor que representa a ordem da linha da imagem.</span><span class="sxs-lookup"><span data-stu-id="84f91-155">A value representing the image line order.</span></span> <span data-ttu-id="84f91-156">Essa é sempre a \_ ordem de linha WIA da \_ \_ parte superior \_ ou da \_ \_ \_ ordem de linha WIA \_ inferior \_ para a parte \_ superior.</span><span class="sxs-lookup"><span data-stu-id="84f91-156">This is always either WIA\_LINE\_ORDER\_TOP\_TO\_BOTTOM or WIA\_LINE\_ORDER\_BOTTOM\_TO\_TOP.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-157">**RawDataOffset**</span><span class="sxs-lookup"><span data-stu-id="84f91-157">**RawDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-158">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-158">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-159">A posição dos dados brutos da imagem em bytes, começando da posição onde o cabeçalho termina ou da posição onde a paleta termina.</span><span class="sxs-lookup"><span data-stu-id="84f91-159">The position of the raw image data in bytes, starting from position where the header ends or the position where the palette ends.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-160">**RawDataSize**</span><span class="sxs-lookup"><span data-stu-id="84f91-160">**RawDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-161">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-161">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-162">O tamanho, em bytes, dos dados brutos da imagem.</span><span class="sxs-lookup"><span data-stu-id="84f91-162">The size, in bytes, of the raw image data.</span></span>

</dd> <dt>

<span data-ttu-id="84f91-163">**PaletteOffset**</span><span class="sxs-lookup"><span data-stu-id="84f91-163">**PaletteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-164">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-165">A posição da paleta em bytes, a partir da posição onde o cabeçalho termina ou da posição onde os dados são encerrados.</span><span class="sxs-lookup"><span data-stu-id="84f91-165">The position of the palette in bytes, starting from the position where the header ends or the position where the data ends.</span></span> <span data-ttu-id="84f91-166">(Esse valor será 0, se não houver nenhuma paleta.)</span><span class="sxs-lookup"><span data-stu-id="84f91-166">(This value is 0, if there is no palette.)</span></span>

</dd> <dt>

<span data-ttu-id="84f91-167">**PaletteSize**</span><span class="sxs-lookup"><span data-stu-id="84f91-167">**PaletteSize**</span></span>
</dt> <dd>

<span data-ttu-id="84f91-168">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="84f91-168">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="84f91-169">O tamanho, em bytes, da tabela de paleta.</span><span class="sxs-lookup"><span data-stu-id="84f91-169">The size, in bytes, of the palette table.</span></span> <span data-ttu-id="84f91-170">(Isso será 0, se não houver nenhuma paleta.)</span><span class="sxs-lookup"><span data-stu-id="84f91-170">(This is 0, if there is no palette.)</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84f91-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="84f91-171">Remarks</span></span>

<span data-ttu-id="84f91-172">Como esse não é um formato de arquivo, use uma cadeia de caracteres vazia para a \_ propriedade de extensão de arquivo WIA IPA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="84f91-172">Because this is not a file format, use an empty string for the WIA\_IPA\_FILE\_EXTENSION property.</span></span>

<span data-ttu-id="84f91-173">A paleta e os dados podem ser obtidos em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="84f91-173">The palette and the data can come in either order.</span></span>

<span data-ttu-id="84f91-174">**RawDataSize** não inclui o cabeçalho ou a paleta.</span><span class="sxs-lookup"><span data-stu-id="84f91-174">**RawDataSize** does not include either the header or the palette.</span></span> <span data-ttu-id="84f91-175">Use esse campo para verificar se a transferência da imagem foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="84f91-175">Use this field to verify that the transfer of the image has been successful.</span></span>

<span data-ttu-id="84f91-176">**PaletteSize** é bytes, não o número de entradas na paleta.</span><span class="sxs-lookup"><span data-stu-id="84f91-176">**PaletteSize** is bytes, not the number of entries in the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f91-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84f91-177">Requirements</span></span>



| <span data-ttu-id="84f91-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f91-178">Requirement</span></span> | <span data-ttu-id="84f91-179">Valor</span><span class="sxs-lookup"><span data-stu-id="84f91-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="84f91-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84f91-180">Minimum supported client</span></span><br/> | <span data-ttu-id="84f91-181">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84f91-181">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="84f91-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84f91-182">Minimum supported server</span></span><br/> | <span data-ttu-id="84f91-183">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84f91-183">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="84f91-184">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84f91-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f91-185"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f91-185"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




