---
title: Enumeração de WMDM_FORMATCODE
description: O \_ tipo de enumeração WMDM FORMATCODE define uma lista de códigos de formato que descrevem os tipos de conteúdo transferidos de e para um dispositivo.
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- WMDM_FORMATCODE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04db31578f36455fdf77bb4044ad45e5ca9f9a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794533"
---
# <a name="wmdm_formatcode-enumeration"></a><span data-ttu-id="90d40-104">\_Enumeração WMDM FORMATCODE</span><span class="sxs-lookup"><span data-stu-id="90d40-104">WMDM\_FORMATCODE enumeration</span></span>

<span data-ttu-id="90d40-105">O tipo de enumeração **WMDM \_ FORMATCODE** define uma lista de códigos de formato que descrevem os tipos de conteúdo transferidos de e para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90d40-105">The **WMDM\_FORMATCODE** enumeration type defines a list of format codes that describe types of content transferred to and from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d40-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="90d40-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a><span data-ttu-id="90d40-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="90d40-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="90d40-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM \_ FORMATCODE \_ não usado**</span><span class="sxs-lookup"><span data-stu-id="90d40-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM\_FORMATCODE\_NOTUSED**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-109">Nenhum código de formato é usado.</span><span class="sxs-lookup"><span data-stu-id="90d40-109">No format code is used.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**FORMATCODE de todas as imagens do WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM\_FORMATCODE\_ALLIMAGES**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-111">Código de formato que pode ser usado para consultar todas as imagens.</span><span class="sxs-lookup"><span data-stu-id="90d40-111">Format code that can be used to query for all images.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM \_ FORMATCODE \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="90d40-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM\_FORMATCODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-113">Código de formato usado para consultar todos os objetos indefinidos.</span><span class="sxs-lookup"><span data-stu-id="90d40-113">Format code used to query for all undefined objects.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**Associação do WMDM \_ FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM\_FORMATCODE\_ASSOCIATION**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-115">Código de formato usado para definir um link entre dois objetos.</span><span class="sxs-lookup"><span data-stu-id="90d40-115">Format code used to define a link between two objects.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**\_script WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM\_FORMATCODE\_SCRIPT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-117">Formate o código de um arquivo de script.</span><span class="sxs-lookup"><span data-stu-id="90d40-117">Format code for a script file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_executável WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM\_FORMATCODE\_EXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-119">Formatar código para um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="90d40-119">Format code for an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**\_texto de FORMATCODE do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM\_FORMATCODE\_TEXT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-121">Formate o código de um arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="90d40-121">Format code for a text file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**HTML do WMDM \_ FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM\_FORMATCODE\_HTML**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-123">Formate o código de um arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="90d40-123">Format code for an HTML file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**\_FORMATCODE WMDM \_ DPOF**</span><span class="sxs-lookup"><span data-stu-id="90d40-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM\_FORMATCODE\_DPOF**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-125">Código de formato usado para representar o formato de ordem de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="90d40-125">Format code used to represent the digital print order format.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ AIFF**</span><span class="sxs-lookup"><span data-stu-id="90d40-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM\_FORMATCODE\_AIFF**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-127">Código de formato usado para representar o formato de arquivo de intercâmbio de áudio.</span><span class="sxs-lookup"><span data-stu-id="90d40-127">Format code used to represent the audio interchange file format.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**onda do WMDM \_ FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM\_FORMATCODE\_WAVE**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-129">Código de formato usado para um arquivo WAV.</span><span class="sxs-lookup"><span data-stu-id="90d40-129">Format code used for a WAV file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**\_FORMATCODE de \_ mp3 do WMDM**</span><span class="sxs-lookup"><span data-stu-id="90d40-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM\_FORMATCODE\_MP3**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-131">Código de formato usado para um arquivo MP3.</span><span class="sxs-lookup"><span data-stu-id="90d40-131">Format code used for an MP3 file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**FORMATCODE do WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM\_FORMATCODE\_AVI**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-133">Código de formato usado para um arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="90d40-133">Format code used for an AVI file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM \_ FORMATCODE \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="90d40-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM\_FORMATCODE\_MPEG**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-135">Código de formato usado para um arquivo MPEG.</span><span class="sxs-lookup"><span data-stu-id="90d40-135">Format code used for an MPEG file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**\_ASF FORMATCODE do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM\_FORMATCODE\_ASF**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-137">Código de formato usado para representar um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="90d40-137">Format code used to represent an Advanced Systems Format (ASF) file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM \_ FORMATCODE \_ reservado \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="90d40-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM\_FORMATCODE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-139">Formate o código que é o primeiro em um intervalo reservado para o PTP (protocolo de transferência de imagem).</span><span class="sxs-lookup"><span data-stu-id="90d40-139">Format code that is the first in a range reserved for Picture Transfer Protocol (PTP).</span></span>

</dd> <dt>

<span data-ttu-id="90d40-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM \_ FORMATCODE \_ reservado \_ pela última vez**</span><span class="sxs-lookup"><span data-stu-id="90d40-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM\_FORMATCODE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-141">Formato de código que é o último em um intervalo reservado para PTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-141">Format code that is last in a range reserved for PTP.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**imagem do WMDM \_ FORMATCODE \_ \_ indefinida**</span><span class="sxs-lookup"><span data-stu-id="90d40-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM\_FORMATCODE\_IMAGE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-143">Código de formato usado para representar e imagem de um tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-143">Format code used to represent and image of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**\_EXIF FORMATCODE de \_ imagem \_ do WMDM**</span><span class="sxs-lookup"><span data-stu-id="90d40-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM\_FORMATCODE\_IMAGE\_EXIF**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-145">Formate o código de um arquivo EXIF.</span><span class="sxs-lookup"><span data-stu-id="90d40-145">Format code for an EXIF file.</span></span> <span data-ttu-id="90d40-146">Também usado para imagens JPEG não cobertas pela imagem do WMDM \_ FORMATCODE \_ \_ JP2 ou da imagem do WMDM \_ FORMATCODE \_ \_ JPX.</span><span class="sxs-lookup"><span data-stu-id="90d40-146">Also used for JPEG images not covered by WMDM\_FORMATCODE\_IMAGE\_JP2 or WMDM\_FORMATCODE\_IMAGE\_JPX.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**\_FORMATCODE de \_ imagem WMDM \_ TIFFEP**</span><span class="sxs-lookup"><span data-stu-id="90d40-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFEP**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-148">Código de formato usado para imagens que são do tipo formato de arquivo de imagem marcada para fotografia eletrônica (TIFF/EP)</span><span class="sxs-lookup"><span data-stu-id="90d40-148">Format code used for images that are of type Tagged Image File Format for Electronic Photography (TIFF/EP)</span></span>

</dd> <dt>

<span data-ttu-id="90d40-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**imagem do WMDM \_ FORMATCODE \_ \_ FLASHPIX**</span><span class="sxs-lookup"><span data-stu-id="90d40-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM\_FORMATCODE\_IMAGE\_FLASHPIX**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-150">Formate o código de um arquivo do tipo FPX.</span><span class="sxs-lookup"><span data-stu-id="90d40-150">Format code for a file of type FPX.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**imagem do WMDM \_ FORMATCODE \_ \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="90d40-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM\_FORMATCODE\_IMAGE\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-152">Código de formato para um arquivo do tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="90d40-152">Format code for a file of type BMP.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**\_FORMATCODE de \_ imagem WMDM \_ CIFF**</span><span class="sxs-lookup"><span data-stu-id="90d40-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM\_FORMATCODE\_IMAGE\_CIFF**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-154">Formate o código de uma imagem no formato de arquivo de imagem da câmera.</span><span class="sxs-lookup"><span data-stu-id="90d40-154">Format code for an image in the camera image file format.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**\_GIF de \_ imagem WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM\_FORMATCODE\_IMAGE\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-156">Formate o código de um arquivo GIF.</span><span class="sxs-lookup"><span data-stu-id="90d40-156">Format code for a GIF file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**imagem do WMDM \_ FORMATCODE \_ \_ JFIF**</span><span class="sxs-lookup"><span data-stu-id="90d40-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM\_FORMATCODE\_IMAGE\_JFIF**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-158">Formate o código para um arquivo do tipo JFIF.</span><span class="sxs-lookup"><span data-stu-id="90d40-158">Format code for a file of type JFIF.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**PCD da imagem do WMDM \_ FORMATCODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM\_FORMATCODE\_IMAGE\_PCD**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-160">Formatar código para uma imagem do tipo Photo CD.</span><span class="sxs-lookup"><span data-stu-id="90d40-160">Format code for an image of type photo cd.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**imagem do WMDM \_ FORMATCODE \_ \_ PICT**</span><span class="sxs-lookup"><span data-stu-id="90d40-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM\_FORMATCODE\_IMAGE\_PICT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-162">Formatar código para uma imagem do tipo PICT.</span><span class="sxs-lookup"><span data-stu-id="90d40-162">Format code for an image of type PICT.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**PNG de imagem do WMDM \_ FORMATCODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM\_FORMATCODE\_IMAGE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-164">Formate o código para uma imagem do tipo PNG.</span><span class="sxs-lookup"><span data-stu-id="90d40-164">Format code for an image of type PNG.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**\_ \_ imagem \_ TIFF do WMDM FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="90d40-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-166">Código de formato para um arquivo do tipo TIFF.</span><span class="sxs-lookup"><span data-stu-id="90d40-166">Format code for a file of type TIFF.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**\_FORMATCODE de \_ imagem WMDM \_ TIFFIT**</span><span class="sxs-lookup"><span data-stu-id="90d40-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFIT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-168">Formate o código para uma imagem do tipo formato de arquivo de imagem marcada com tecnologia de imagem.</span><span class="sxs-lookup"><span data-stu-id="90d40-168">Format code for an image of type Tagged Image File Format with image technology.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**\_FORMATCODE de \_ imagem WMDM \_ JP2**</span><span class="sxs-lookup"><span data-stu-id="90d40-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM\_FORMATCODE\_IMAGE\_JP2**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-170">Formate o código de uma imagem Jpeg200.</span><span class="sxs-lookup"><span data-stu-id="90d40-170">Format code for a jpeg200 image.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**\_FORMATCODE de \_ imagem WMDM \_ JPX**</span><span class="sxs-lookup"><span data-stu-id="90d40-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM\_FORMATCODE\_IMAGE\_JPX**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-172">Formate o código de uma imagem criada em JPEG200, usando o registro de imagem ainda estendido.</span><span class="sxs-lookup"><span data-stu-id="90d40-172">Format code for an image built on JPEG200, using extended still image registration.</span></span> <span data-ttu-id="90d40-173">A extensão de nome de arquivo geralmente é. jpf ou. jpx.</span><span class="sxs-lookup"><span data-stu-id="90d40-173">The file name extension is usually .jpf or .jpx.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**imagem do WMDM \_ FORMATCODE \_ \_ reservada \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="90d40-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-175">Formate o código que é o primeiro em um intervalo reservado para uma referência de imagem no PTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-175">Format code that is the first in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**imagem do WMDM \_ FORMATCODE \_ \_ reservada \_ por último**</span><span class="sxs-lookup"><span data-stu-id="90d40-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-177">O código de formato que é o último em um intervalo reservado para uma referência de imagem no PTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-177">Format code that is the last in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**\_FORMATCODE WMDM \_ UNDEFINEDFIRMWARE**</span><span class="sxs-lookup"><span data-stu-id="90d40-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM\_FORMATCODE\_UNDEFINEDFIRMWARE**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-179">Formate o código quando o firmware estiver indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-179">Format code when firmware is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ FORMATCODE \_ WBMP**</span><span class="sxs-lookup"><span data-stu-id="90d40-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span> **WMDM\_FORMATCODE\_WBMP**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-181">Formate o código de uma imagem de bitmap do protocolo de aplicativo sem fio (. WBMP).</span><span class="sxs-lookup"><span data-stu-id="90d40-181">Format code for a Wireless Application Protocol Bitmap (.wbmp) image.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ FORMATCODE \_ JPEGXR**</span><span class="sxs-lookup"><span data-stu-id="90d40-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span> **WMDM\_FORMATCODE\_JPEGXR**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-183">Formatar código para uma imagem de HD Photo</span><span class="sxs-lookup"><span data-stu-id="90d40-183">Format code for an HD Photo image</span></span>

</dd> <dt>

<span data-ttu-id="90d40-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**\_FORMATCODE WMDM \_ WINDOWSIMAGEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="90d40-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-185">Formatar código para formato de imagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="90d40-185">Format code for Windows image format.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**\_FORMATCODE WMDM \_ UNDEFINEDAUDIO**</span><span class="sxs-lookup"><span data-stu-id="90d40-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM\_FORMATCODE\_UNDEFINEDAUDIO**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-187">Formatar código para um arquivo de áudio de tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-187">Format code for an audio file of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**\_sqlFORMATCODE \_ WMA**</span><span class="sxs-lookup"><span data-stu-id="90d40-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM\_FORMATCODE\_WMA**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-189">Formate o código de um arquivo de áudio do Windows Media (WMA).</span><span class="sxs-lookup"><span data-stu-id="90d40-189">Format code for a Windows Media Audio (WMA) file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**\_FORMATCODE WMDM \_ OGG**</span><span class="sxs-lookup"><span data-stu-id="90d40-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM\_FORMATCODE\_OGG**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-191">Formate o código de um arquivo de áudio codificado em Vorbis em um contêiner OGG.</span><span class="sxs-lookup"><span data-stu-id="90d40-191">Format code for a Vorbis-encoded audio file in an Ogg container.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="90d40-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM\_FORMATCODE\_AAC**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-193">Formatar código para um arquivo de codificação de áudio avançado (AAC).</span><span class="sxs-lookup"><span data-stu-id="90d40-193">Format code for an Advanced Audio Coding (AAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM \_ FORMATCODE \_ audível**</span><span class="sxs-lookup"><span data-stu-id="90d40-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM\_FORMATCODE\_AUDIBLE**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-195">Formatar código para um arquivo audível.</span><span class="sxs-lookup"><span data-stu-id="90d40-195">Format code for an Audible file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**\_FORMATCODE WMDM \_ FLAC**</span><span class="sxs-lookup"><span data-stu-id="90d40-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM\_FORMATCODE\_FLAC**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-197">Formate o código de um arquivo FLAC (codec de áudio sem perdas).</span><span class="sxs-lookup"><span data-stu-id="90d40-197">Format code for a Free Lossless Audio Codec (FLAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ FORMATCODE \_ QCELP**</span><span class="sxs-lookup"><span data-stu-id="90d40-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span> **WMDM\_FORMATCODE\_QCELP**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-199">Formato de código para um arquivo de codec de QCELP (previsão linear empolgante) de código do Qualcomm.</span><span class="sxs-lookup"><span data-stu-id="90d40-199">Format code for a Qualcomm Code Excited Linear Prediction (QCELP) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ FORMATCODE \_ Amr**</span><span class="sxs-lookup"><span data-stu-id="90d40-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span> **WMDM\_FORMATCODE\_AMR**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-201">Formate o código para um arquivo de codec de áudio de várias taxas (AMR) adaptável.</span><span class="sxs-lookup"><span data-stu-id="90d40-201">Format code for an Adaptive Multi-Rate audio (AMR) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**\_FORMATCODE WMDM \_ UNDEFINEDVIDEO**</span><span class="sxs-lookup"><span data-stu-id="90d40-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM\_FORMATCODE\_UNDEFINEDVIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-203">Formate o código de um arquivo de vídeo com um tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-203">Format code for a video file with an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ FORMATCODE \_ WMV**</span><span class="sxs-lookup"><span data-stu-id="90d40-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM\_FORMATCODE\_WMV**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-205">Formate o código de um arquivo de vídeo do Windows Media (WMV).</span><span class="sxs-lookup"><span data-stu-id="90d40-205">Format code for a Windows Media Video (WMV) file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**FORMATCODE do WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM\_FORMATCODE\_MP4**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-207">Formatar código para um arquivo MP4.</span><span class="sxs-lookup"><span data-stu-id="90d40-207">Format code for an MP4 file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**\_FORMATCODE WMDM \_ MP2**</span><span class="sxs-lookup"><span data-stu-id="90d40-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM\_FORMATCODE\_MP2**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-209">Formate o código de um arquivo MP2.</span><span class="sxs-lookup"><span data-stu-id="90d40-209">Format code for an MP2 file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3G2**</span><span class="sxs-lookup"><span data-stu-id="90d40-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span> **WMDM\_FORMATCODE\_3G2**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-211">Código de formato para um formato de contêiner multimídia 3G2 (3GPP2).</span><span class="sxs-lookup"><span data-stu-id="90d40-211">Format code for a 3G2 (3GPP2) multimedia container format.</span></span> <span data-ttu-id="90d40-212">Um arquivo desse tipo pode conter áudio, vídeo ou texto.</span><span class="sxs-lookup"><span data-stu-id="90d40-212">A file of this type may contain audio, video, or text.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD**</span><span class="sxs-lookup"><span data-stu-id="90d40-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span> **WMDM\_FORMATCODE\_AVCHD**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-214">Formate o código de um arquivo de vídeo AVCHD (codificação de vídeo avançada alta definição).</span><span class="sxs-lookup"><span data-stu-id="90d40-214">Format code for an AVCHD (Advanced Video Coding High Definition) video file.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_ ATSCTS**</span><span class="sxs-lookup"><span data-stu-id="90d40-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span> **WMDM\_FORMATCODE\_ATSCTS**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-216">Código de formato do padrão de formato ATSCTS (Comitê de sistemas de televisão avançado).</span><span class="sxs-lookup"><span data-stu-id="90d40-216">Format code for the Advanced Television Systems Committee (ATSCTS) format standard.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ FORMATCODE \_ DVBTS**</span><span class="sxs-lookup"><span data-stu-id="90d40-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span> **WMDM\_FORMATCODE\_DVBTS**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-218">Formate o código para um vídeo MPEG-2 e MPEG-1 Layer II ou AC-3, áudio em um fluxo de transporte MPEG-2 em conformidade com DVB.</span><span class="sxs-lookup"><span data-stu-id="90d40-218">Format code for an MPEG-2 video and MPEG-1 Layer II, or AC-3, audio within a DVB-compliant MPEG-2 Transport Stream.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ undefinecollection**</span><span class="sxs-lookup"><span data-stu-id="90d40-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM\_FORMATCODE\_UNDEFINEDCOLLECTION**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-220">Código de formato para uma coleção de um tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-220">Format code for a collection of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**\_FORMATCODE WMDM \_ ABSTRACTMULTIMEDIAALBUM**</span><span class="sxs-lookup"><span data-stu-id="90d40-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTMULTIMEDIAALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-222">Formate o código de um álbum de multimídia em que o objeto contém as propriedades de um álbum de multimídia e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-222">Format code for a multimedia album where the object contains the properties of a multimedia album and, optionally, data.</span></span> <span data-ttu-id="90d40-223">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-223">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**\_FORMATCODE WMDM \_ ABSTRACTIMAGEALBUM**</span><span class="sxs-lookup"><span data-stu-id="90d40-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM\_FORMATCODE\_ABSTRACTIMAGEALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-225">Formate o código de um álbum de imagem em que o objeto contém as propriedades de um álbum de imagem e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-225">Format code for an image album where the object contains the properties of an image album and, optionally, data.</span></span> <span data-ttu-id="90d40-226">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-226">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**\_FORMATCODE WMDM \_ ABSTRACTAUDIOALBUM**</span><span class="sxs-lookup"><span data-stu-id="90d40-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-228">Formate o código de um álbum de áudio em que o objeto contém as propriedades de um álbum de áudio e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-228">Format code for an audio album where the object contains the properties of an audio album and, optionally, data.</span></span> <span data-ttu-id="90d40-229">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-229">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**\_FORMATCODE WMDM \_ ABSTRACTVIDEOALBUM**</span><span class="sxs-lookup"><span data-stu-id="90d40-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTVIDEOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-231">Formate o código de um álbum de vídeo em que o objeto contém as propriedades de um álbum de vídeo e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-231">Format code for a video album where the object contains the properties of a video album and, optionally, data.</span></span> <span data-ttu-id="90d40-232">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-232">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**\_FORMATCODE WMDM \_ ABSTRACTAUDIOVIDEOPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="90d40-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-234">Formate o código de uma playlist de áudio/vídeo em que o objeto contém as propriedades de uma lista de reprodução de áudio/vídeo e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-234">Format code for an audio/video playlist where the object contains the properties of an audio/video playlist and, optionally, data.</span></span> <span data-ttu-id="90d40-235">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-235">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**\_FORMATCODE WMDM \_ ABSTRACTCONTACTGROUP**</span><span class="sxs-lookup"><span data-stu-id="90d40-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACTGROUP**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-237">Formate o código de um grupo de contatos em que o objeto contém as propriedades de um grupo de contatos e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-237">Format code for a contact group where the object contains the properties of a contact group and, optionally, data.</span></span> <span data-ttu-id="90d40-238">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-238">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**\_FORMATCODE WMDM \_ ABSTRACTMESSAGEFOLDER**</span><span class="sxs-lookup"><span data-stu-id="90d40-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGEFOLDER**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-240">Formate o código de uma pasta de mensagens em que o objeto contém as propriedades de uma pasta de mensagens e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-240">Format code for a message folder where the object contains the properties of a message folder and, optionally, data.</span></span> <span data-ttu-id="90d40-241">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-241">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**\_FORMATCODE WMDM \_ ABSTRACTCHAPTEREDPRODUCTION**</span><span class="sxs-lookup"><span data-stu-id="90d40-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM\_FORMATCODE\_ABSTRACTCHAPTEREDPRODUCTION**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-243">Formate o código para uma produção com capítulo em que o objeto contém as propriedades de uma produção com capítulo e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-243">Format code for a chaptered production where the object contains the properties of a chaptered production and, optionally, data.</span></span> <span data-ttu-id="90d40-244">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-244">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**\_FORMATCODE WMDM \_ WPLPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="90d40-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM\_FORMATCODE\_WPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-246">Formate o código de uma lista de reprodução formatada com a formatação de playlist do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="90d40-246">Format code for a playlist formatted with Windows Media playlist formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**\_FORMATCODE WMDM \_ M3UPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="90d40-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM\_FORMATCODE\_M3UPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-248">Formate o código de uma playlist com formatação M3U.</span><span class="sxs-lookup"><span data-stu-id="90d40-248">Format code for a playlist with M3U formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**\_FORMATCODE WMDM \_ MPLPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="90d40-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM\_FORMATCODE\_MPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-250">Formate o código de uma playlist com formatação MPL.</span><span class="sxs-lookup"><span data-stu-id="90d40-250">Format code for a playlist with MPL formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**\_FORMATCODE WMDM \_ ASXPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="90d40-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM\_FORMATCODE\_ASXPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-252">Formate o código de uma playlist com formatação ASX.</span><span class="sxs-lookup"><span data-stu-id="90d40-252">Format code for a playlist with ASX formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**\_FORMATCODE WMDM \_ PLSPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="90d40-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM\_FORMATCODE\_PLSPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-254">Formate o código de uma playlist com formatação PLS.</span><span class="sxs-lookup"><span data-stu-id="90d40-254">Format code for a playlist with PLS formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**\_FORMATCODE WMDM \_ UNDEFINEDDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="90d40-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM\_FORMATCODE\_UNDEFINEDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-256">Formatar código para um documento de tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-256">Format code for a document of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**\_FORMATCODE WMDM \_ ABSTRACTDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="90d40-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM\_FORMATCODE\_ABSTRACTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-258">Formate o código de um documento em que o objeto contém as propriedades de um documento e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-258">Format code for a document where the object contains the properties of a document and, optionally, data.</span></span> <span data-ttu-id="90d40-259">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-259">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**\_XMLDOCUMENT de FORMATCODE do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM\_FORMATCODE\_XMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-261">Formatar código para um documento XML.</span><span class="sxs-lookup"><span data-stu-id="90d40-261">Format code for an XML document.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**\_FORMATCODE WMDM \_ MICROSOFTWORDDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="90d40-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM\_FORMATCODE\_MICROSOFTWORDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-263">Formate o código de um documento do Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="90d40-263">Format code for a Microsoft Word document.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**\_FORMATCODE WMDM \_ MHTCOMPILEDHTMLDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="90d40-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM\_FORMATCODE\_MHTCOMPILEDHTMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-265">Formate o código de um documento HTML compilado.</span><span class="sxs-lookup"><span data-stu-id="90d40-265">Format code for a compiled HTML document.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**\_FORMATCODE WMDM \_ MICROSOFTEXCELSPREADSHEET**</span><span class="sxs-lookup"><span data-stu-id="90d40-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM\_FORMATCODE\_MICROSOFTEXCELSPREADSHEET**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-267">Formate o código de uma planilha do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="90d40-267">Format code for a Microsoft Excel spreadsheet.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**\_FORMATCODE WMDM \_ MICROSOFTPOWERPOINTDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="90d40-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM\_FORMATCODE\_MICROSOFTPOWERPOINTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-269">Formate o código de um documento do Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="90d40-269">Format code for a Microsoft PowerPoint document.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**\_FORMATCODE WMDM \_ UNDEFINEDMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="90d40-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM\_FORMATCODE\_UNDEFINEDMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-271">Código de formato para uma mensagem de tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-271">Format code for a message of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**\_FORMATCODE WMDM \_ ABSTRACTMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="90d40-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-273">Formate o código de uma mensagem em que o objeto contém as propriedades de uma mensagem e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-273">Format code for a message where the object contains the properties of a message and, optionally, data.</span></span> <span data-ttu-id="90d40-274">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-274">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**\_FORMATCODE WMDM \_ UNDEFINEDCONTACT**</span><span class="sxs-lookup"><span data-stu-id="90d40-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM\_FORMATCODE\_UNDEFINEDCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-276">Formatar código para um contato de tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-276">Format code for a contact of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**\_FORMATCODE WMDM \_ ABSTRACTCONTACT**</span><span class="sxs-lookup"><span data-stu-id="90d40-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-278">Formate o código de um contato em que o objeto contém as propriedades de um contato e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-278">Format code for a contact where the object contains the properties of a contact and, optionally, data.</span></span> <span data-ttu-id="90d40-279">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-279">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**\_FORMATCODE WMDM \_ VCARD2**</span><span class="sxs-lookup"><span data-stu-id="90d40-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM\_FORMATCODE\_VCARD2**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-281">Formate o código de um cartão eletrônico com a formatação de vCard versão 2.</span><span class="sxs-lookup"><span data-stu-id="90d40-281">Format code for an electronic card with vcard version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**\_FORMATCODE WMDM \_ VCARD3**</span><span class="sxs-lookup"><span data-stu-id="90d40-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM\_FORMATCODE\_VCARD3**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-283">Formate o código de um cartão eletrônico com a formatação de vCard versão 3.</span><span class="sxs-lookup"><span data-stu-id="90d40-283">Format code for an electronic card with vcard version 3 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**\_FORMATCODE WMDM \_ UNDEFINEDCALENDARITEM**</span><span class="sxs-lookup"><span data-stu-id="90d40-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM\_FORMATCODE\_UNDEFINEDCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-285">Formatar código para um item de calendário eletrônico de tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-285">Format code for an electronic calendar item of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**\_FORMATCODE WMDM \_ ABSTRACTCALENDARITEM**</span><span class="sxs-lookup"><span data-stu-id="90d40-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM\_FORMATCODE\_ABSTRACTCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-287">Formate o código de um item de calendário em que o objeto contém as propriedades de um item de calendário e, opcionalmente, dados.</span><span class="sxs-lookup"><span data-stu-id="90d40-287">Format code for a calendar item where the object contains the properties of a calendar item and, optionally, data.</span></span> <span data-ttu-id="90d40-288">Quaisquer dados contidos são de um formato indefinido em relação à especificação do MTP.</span><span class="sxs-lookup"><span data-stu-id="90d40-288">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**\_FORMATCODE WMDM \_ VCALENDAR1**</span><span class="sxs-lookup"><span data-stu-id="90d40-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM\_FORMATCODE\_VCALENDAR1**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-290">Formate o código de um item de calendário eletrônico com a formatação do vCalendar versão 1.</span><span class="sxs-lookup"><span data-stu-id="90d40-290">Format code for an electronic calendar item with vcalendar version 1 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**\_FORMATCODE WMDM \_ VCALENDAR2**</span><span class="sxs-lookup"><span data-stu-id="90d40-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM\_FORMATCODE\_VCALENDAR2**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-292">Formate o código de um item de calendário eletrônico com a formatação do vCalendar versão 2.</span><span class="sxs-lookup"><span data-stu-id="90d40-292">Format code for an electronic calendar item with vcalendar version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**\_FORMATCODE WMDM \_ UNDEFINEDWINDOWSEXECUTABLE**</span><span class="sxs-lookup"><span data-stu-id="90d40-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM\_FORMATCODE\_UNDEFINEDWINDOWSEXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-294">Código de formato para um executável baseado no Windows de tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="90d40-294">Format code for a Windows-based executable of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**conversão de mídia do WMDM \_ FORMATCODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM\_FORMATCODE\_MEDIA\_CAST**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-296">Formate o código de um objeto de conversão de mídia.</span><span class="sxs-lookup"><span data-stu-id="90d40-296">Format code for a media cast object.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_seção WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="90d40-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM\_FORMATCODE\_SECTION**</span></span>
</dt> <dd>

<span data-ttu-id="90d40-298">Formate o código para uma seção de dados contida em outro objeto.</span><span class="sxs-lookup"><span data-stu-id="90d40-298">Format code for a section of data that is contained in another object.</span></span>

</dd> <dt>

<span data-ttu-id="90d40-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ FORMATCODE \_ 3G2A**</span><span class="sxs-lookup"><span data-stu-id="90d40-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span> **WMDM\_FORMATCODE\_3G2A**</span></span> 
</dt> <dd>

<span data-ttu-id="90d40-300">Código de formato para um formato de contêiner multimídia 3G2A (3GPP2A).</span><span class="sxs-lookup"><span data-stu-id="90d40-300">Format code for a 3G2A (3GPP2A) multimedia container format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90d40-301">Comentários</span><span class="sxs-lookup"><span data-stu-id="90d40-301">Remarks</span></span>

<span data-ttu-id="90d40-302">Para descobrir os formatos com suporte de um dispositivo, um aplicativo pode usar [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para consultar a propriedade de dispositivo **g \_ wszWMDMFormatsSupported** .</span><span class="sxs-lookup"><span data-stu-id="90d40-302">To discover the formats supported by a device, an application can use [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to query the **g\_wszWMDMFormatsSupported** device property.</span></span>

<span data-ttu-id="90d40-303">Para descobrir recursos de dispositivo para um formato específico, um aplicativo pode chamar [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="90d40-303">To discover device capabilities for a particular format, an application can call [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span>

<span data-ttu-id="90d40-304">Um aplicativo pode definir o código de formato ao criar um armazenamento no dispositivo, incluindo a propriedade **g \_ wszWMDMFormatCode** nos metadados passados no parâmetro *pMetaData* de uma chamada para [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span><span class="sxs-lookup"><span data-stu-id="90d40-304">An application can set the format code while creating a storage on device by including the **g\_wszWMDMFormatCode** property in metadata passed in the *pMetaData* parameter of a call to [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span>

<span data-ttu-id="90d40-305">Um aplicativo pode consultar o código de formato de um armazenamento chamando [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) e recuperando a propriedade **g \_ wszWMDMFormatCode** .</span><span class="sxs-lookup"><span data-stu-id="90d40-305">An application can query the format code of a storage by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) and retrieving the **g\_wszWMDMFormatCode** property.</span></span>

<span data-ttu-id="90d40-306">Se o dispositivo der suporte à definição do código de formato após a criação do armazenamento, um aplicativo poderá usar [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) para definir a propriedade **g \_ wszWMDMFormatCode** .</span><span class="sxs-lookup"><span data-stu-id="90d40-306">If the device supports setting the format code after the creation of storage, an application can use [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) to set the **g\_wszWMDMFormatCode** property.</span></span> <span data-ttu-id="90d40-307">Alguns dispositivos podem não permitir a alteração do código de formato depois que o armazenamento é criado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90d40-307">Some devices may not allow changing the format code after the storage is created on the device.</span></span> <span data-ttu-id="90d40-308">Portanto, a definição dessa propriedade junto com os metadados passados em [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) é altamente recomendável.</span><span class="sxs-lookup"><span data-stu-id="90d40-308">Therefore, setting this property along with the metadata passed in [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) is strongly recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="90d40-309">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90d40-309">Requirements</span></span>



| <span data-ttu-id="90d40-310">Requisito</span><span class="sxs-lookup"><span data-stu-id="90d40-310">Requirement</span></span> | <span data-ttu-id="90d40-311">Valor</span><span class="sxs-lookup"><span data-stu-id="90d40-311">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90d40-312">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90d40-312">Header</span></span><br/> | <dl> <span data-ttu-id="90d40-313"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90d40-313"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90d40-314">Confira também</span><span class="sxs-lookup"><span data-stu-id="90d40-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d40-315">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="90d40-315">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="90d40-316">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="90d40-316">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="90d40-317">**IWMDMDevice3:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="90d40-317">**IWMDMDevice3::GetProperty**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[<span data-ttu-id="90d40-318">**IWMDMStorage3:: GetMetadata**</span><span class="sxs-lookup"><span data-stu-id="90d40-318">**IWMDMStorage3::GetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[<span data-ttu-id="90d40-319">**IWMDMStorage3:: SetMetadata**</span><span class="sxs-lookup"><span data-stu-id="90d40-319">**IWMDMStorage3::SetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[<span data-ttu-id="90d40-320">**IWMDMStorage4::GetSpecifiedMetadata**</span><span class="sxs-lookup"><span data-stu-id="90d40-320">**IWMDMStorage4::GetSpecifiedMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[<span data-ttu-id="90d40-321">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="90d40-321">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[<span data-ttu-id="90d40-322">**Constantes de metadados**</span><span class="sxs-lookup"><span data-stu-id="90d40-322">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 





