---
description: As constantes a seguir especificam o conjunto válido de propriedades do item de scanner WIA (aquisição de imagem do Windows).
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Constantes da propriedade item do scanner WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aa3b1cc4ae14a9460a24f652a9599035cacca2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811657"
---
# <a name="scanner-wia-item-property-constants"></a><span data-ttu-id="6f739-103">Constantes da propriedade item do scanner WIA</span><span class="sxs-lookup"><span data-stu-id="6f739-103">Scanner WIA Item Property Constants</span></span>

<span data-ttu-id="6f739-104">As constantes a seguir especificam o conjunto válido de propriedades do item de scanner WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="6f739-104">The following constants specify the valid set of Windows Image Acquisition (WIA) scanner item properties.</span></span>

<span data-ttu-id="6f739-105">O prefixo " \_ IPS WIA \_ " indica uma propriedade de item para dispositivos de scanner e é a Convenção de nomenclatura usada em C/C++.</span><span class="sxs-lookup"><span data-stu-id="6f739-105">The prefix "WIA\_IPS\_" indicates an Item Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="6f739-106">Para fins de script, essas constantes usam o prefixo "ScannerPicture" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="6f739-106">For scripting purposes these constants use the prefix "ScannerPicture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="6f739-107">O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f739-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="6f739-108">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="6f739-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="6f739-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <span data-ttu-id="6f739-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="6f739-111">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-111">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="6f739-112">Ativa ou desativa a distorção automática.</span><span class="sxs-lookup"><span data-stu-id="6f739-112">Turns automatic deskew on or off.</span></span><br/> <span data-ttu-id="6f739-113">Opcional somente para WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-113">Optional for WIA_CATEGORY_FEEDER only.</span></span><br/> <span data-ttu-id="6f739-114">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6f739-114">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="6f739-115">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-115">The following table has the constants that are valid with this property.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-116">Constante</span><span class="sxs-lookup"><span data-stu-id="6f739-116">Constant</span></span></th>
<th><span data-ttu-id="6f739-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-118">WIA_AUTO_DESKEW_ON</span><span class="sxs-lookup"><span data-stu-id="6f739-118">WIA_AUTO_DESKEW_ON</span></span></td>
<td><span data-ttu-id="6f739-119">Ativar a distorção automática.</span><span class="sxs-lookup"><span data-stu-id="6f739-119">Turn on automatic deskew.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-120">WIA_AUTO_DESKEW_OFF</span><span class="sxs-lookup"><span data-stu-id="6f739-120">WIA_AUTO_DESKEW_OFF</span></span></td>
<td><span data-ttu-id="6f739-121">Desative a distorção automática.</span><span class="sxs-lookup"><span data-stu-id="6f739-121">Turn off automatic deskew.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <span data-ttu-id="6f739-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-123">Os valores de brilho da imagem disponíveis no scanner.</span><span class="sxs-lookup"><span data-stu-id="6f739-123">The image brightness values available within the scanner.</span></span></p>
<p><span data-ttu-id="6f739-124">Contém a configuração de brilho do hardware atual para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-124">Contains the current hardware brightness setting for the device.</span></span> <span data-ttu-id="6f739-125">Um aplicativo define essa propriedade como o valor de brilho do hardware.</span><span class="sxs-lookup"><span data-stu-id="6f739-125">An application sets this property to the hardware's brightness value.</span></span> <span data-ttu-id="6f739-126">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-126">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-127">Os valores devem ser mapeados em um intervalo de-1000 até 1000, em que 1000 corresponde ao brilho máximo, 0 corresponde ao brilho normal e-1000 corresponde ao brilho mínimo.</span><span class="sxs-lookup"><span data-stu-id="6f739-127">Values should be mapped in a range from -1000 through 1000, where 1000 corresponds to the maximum brightness, 0 corresponds to normal brightness, and -1000 corresponds to the minimum brightness.</span></span></p>
<p><span data-ttu-id="6f739-128">Necessário para todos os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-128">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="6f739-129">Opcional, mas recomendado, para itens de WIA_CATEGORY_FINISHED_FILE que dão suporte a visualizações.</span><span class="sxs-lookup"><span data-stu-id="6f739-129">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="6f739-130">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-130">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <span data-ttu-id="6f739-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-132">Contém a configuração de contraste de hardware atual para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-132">Contains the current hardware contrast setting for a device.</span></span> <span data-ttu-id="6f739-133">Um aplicativo define essa propriedade como o valor de contraste do hardware.</span><span class="sxs-lookup"><span data-stu-id="6f739-133">An application sets this property to the hardware's contrast value.</span></span> <span data-ttu-id="6f739-134">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-134">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-135">Os valores devem ser mapeados em um intervalo de-1000 até 1000, em que-1000 corresponde ao contraste mínimo, 0 corresponde ao contraste normal e 1000 corresponde ao contraste máximo.</span><span class="sxs-lookup"><span data-stu-id="6f739-135">Values should be mapped in a range from -1000 through 1000, where -1000 corresponds to the minimum contrast, 0 corresponds to normal contrast, and 1000 corresponds to the maximum contrast.</span></span></p>
<p><span data-ttu-id="6f739-136">Necessário para todos os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-136">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="6f739-137">Opcional, mas recomendado, para itens de WIA_CATEGORY_FINISHED_FILE que dão suporte a visualizações.</span><span class="sxs-lookup"><span data-stu-id="6f739-137">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="6f739-138">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-138">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <span data-ttu-id="6f739-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-140">Contém as configurações de tentativa atuais.</span><span class="sxs-lookup"><span data-stu-id="6f739-140">Contains the current intent settings.</span></span> <span data-ttu-id="6f739-141">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-141">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-142">Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-142">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="6f739-143">Não há suporte para itens de WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-143">It is not supported for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="6f739-144">Tipo: <strong>VT_I4</strong> acesso: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span><span class="sxs-lookup"><span data-stu-id="6f739-144">Type: <strong>VT_I4</strong> Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span></span></p>
<p><span data-ttu-id="6f739-145">O driver os usa para predefinir Propriedades de item com base no uso pretendido da imagem por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f739-145">The driver uses these to preset item properties based on an application's intended use of the image.</span></span> <span data-ttu-id="6f739-146">Isso pode incluir, por exemplo, a qualidade máxima, o tamanho mínimo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6f739-146">This might include, for example, maximum quality, minimum size, and so on.</span></span></p>
<p><span data-ttu-id="6f739-147">O driver escolhe a profundidade de bits, em pontos por polegada, e outras configurações que ele determina são apropriadas para a intenção selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f739-147">The driver chooses the bit depth, in dots per inch, and other settings that it determines are appropriate for the selected intent.</span></span> <span data-ttu-id="6f739-148">Cabe ao aplicativo ler as configurações atuais para determinar quais propriedades foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="6f739-148">It is up to the application to read the current settings to determine which properties were changed.</span></span> <span data-ttu-id="6f739-149">Um aplicativo define essa propriedade para definir automaticamente as propriedades do WIA para uma tentativa de aquisição específica.</span><span class="sxs-lookup"><span data-stu-id="6f739-149">An application sets this property to auto-set the WIA properties for specific acquisition intent.</span></span> <span data-ttu-id="6f739-150">Essa propriedade é necessária para todos os scanners.</span><span class="sxs-lookup"><span data-stu-id="6f739-150">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="6f739-151">Um aplicativo define essa propriedade para definir automaticamente as propriedades de WIA para uma intenção de aquisição específica</span><span class="sxs-lookup"><span data-stu-id="6f739-151">An application sets this property to auto-set the WIA properties for specific acquisition intent</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-152">Os sinalizadores podem ser combinados com um operador <strong>OR bit a</strong> bit, mas uma imagem não pode ser escala de cinza e cor.</span><span class="sxs-lookup"><span data-stu-id="6f739-152">The flags can be combined with a bitwise <strong>OR</strong> operator, but an image cannot be both grayscale and color.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-153">Essa propriedade é necessária para todos os scanners.</span><span class="sxs-lookup"><span data-stu-id="6f739-153">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="6f739-154">A tabela a seguir contém os sinalizadores de tipo de imagem e suas definições.</span><span class="sxs-lookup"><span data-stu-id="6f739-154">The following table contains the image-type flags and their definitions.</span></span> <span data-ttu-id="6f739-155">Esses sinalizadores são usados para definir qual tipo de imagem é pretendido: cor, escala de cinza e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6f739-155">These flags are used to set which type of image is intended: color, grayscale, and so on.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-156">Sinalizadores de tipo de imagem pretendidos</span><span class="sxs-lookup"><span data-stu-id="6f739-156">Intended image type flags</span></span></th>
<th><span data-ttu-id="6f739-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-158">WIA_INTENT_NONE</span><span class="sxs-lookup"><span data-stu-id="6f739-158">WIA_INTENT_NONE</span></span></td>
<td><span data-ttu-id="6f739-159">Valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6f739-159">Default value.</span></span> <span data-ttu-id="6f739-160">Nenhuma tentativa foi especificada.</span><span class="sxs-lookup"><span data-stu-id="6f739-160">No intent is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-161">WIA_INTENT_IMAGE_TYPE_COLOR</span><span class="sxs-lookup"><span data-stu-id="6f739-161">WIA_INTENT_IMAGE_TYPE_COLOR</span></span></td>
<td><span data-ttu-id="6f739-162">O aplicativo pretende preparar o dispositivo para uma verificação de cor.</span><span class="sxs-lookup"><span data-stu-id="6f739-162">The application intends to prepare the device for a color scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="6f739-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span></span></td>
<td><span data-ttu-id="6f739-164">O aplicativo pretende preparar o dispositivo para uma verificação em tons de cinza.</span><span class="sxs-lookup"><span data-stu-id="6f739-164">The application intends to prepare the device for a grayscale scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-165">WIA_INTENT_IMAGE_TYPE_TEXT</span><span class="sxs-lookup"><span data-stu-id="6f739-165">WIA_INTENT_IMAGE_TYPE_TEXT</span></span></td>
<td><span data-ttu-id="6f739-166">O aplicativo pretende preparar o dispositivo para verificar o texto.</span><span class="sxs-lookup"><span data-stu-id="6f739-166">The application intends to prepare the device for scanning text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-167">WIA_INTENT_IMAGE_TYPE_MASK</span><span class="sxs-lookup"><span data-stu-id="6f739-167">WIA_INTENT_IMAGE_TYPE_MASK</span></span></td>
<td><span data-ttu-id="6f739-168">Máscara para todos os sinalizadores de tipo de imagem.</span><span class="sxs-lookup"><span data-stu-id="6f739-168">Mask for all of the image-type flags.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="6f739-169">A tabela a seguir contém os sinalizadores de qualidade e tamanho e suas definições.</span><span class="sxs-lookup"><span data-stu-id="6f739-169">The following table contains the quality and size flags and their definitions.</span></span> <span data-ttu-id="6f739-170">Esses sinalizadores são usados para definir o nível de qualidade pretendido.</span><span class="sxs-lookup"><span data-stu-id="6f739-170">These flags are used to set which level of quality is intended.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-171">Tamanho de imagem pretendido/sinalizadores de qualidade</span><span class="sxs-lookup"><span data-stu-id="6f739-171">Intended image size/quality flags</span></span></th>
<th><span data-ttu-id="6f739-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-172">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-173">WIA_INTENT_MINIMIZE_SIZE</span><span class="sxs-lookup"><span data-stu-id="6f739-173">WIA_INTENT_MINIMIZE_SIZE</span></span></td>
<td><span data-ttu-id="6f739-174">O aplicativo pretende preparar o dispositivo para verificar uma imagem que resulte em uma pequena verificação.</span><span class="sxs-lookup"><span data-stu-id="6f739-174">The application intends to prepare the device for scanning an image that result's in a small scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-175">WIA_INTENT_MAXIMIZE_QUALITY</span><span class="sxs-lookup"><span data-stu-id="6f739-175">WIA_INTENT_MAXIMIZE_QUALITY</span></span></td>
<td><span data-ttu-id="6f739-176">O aplicativo pretende preparar o dispositivo para verificar uma imagem de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="6f739-176">The application intends to prepare the device for scanning a high-quality image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-177">WIA_INTENT_SIZE_MASK</span><span class="sxs-lookup"><span data-stu-id="6f739-177">WIA_INTENT_SIZE_MASK</span></span></td>
<td><span data-ttu-id="6f739-178">Esse sinalizador é uma máscara para todos os sinalizadores de tamanho/qualidade.</span><span class="sxs-lookup"><span data-stu-id="6f739-178">This flag is a mask for all of the size/quality flags.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-179">WIA_INTENT_BEST_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="6f739-179">WIA_INTENT_BEST_PREVIEW</span></span></td>
<td><span data-ttu-id="6f739-180">O aplicativo pretende preparar o dispositivo para verificar uma versão prévia.</span><span class="sxs-lookup"><span data-stu-id="6f739-180">The application intends to prepare the device for scanning a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <span data-ttu-id="6f739-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-182">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-182">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-183">Contém o número de pixels na direção x de WIA_IPS_XPOS para a coordenada x do canto superior da imagem a ser deinclinada.</span><span class="sxs-lookup"><span data-stu-id="6f739-183">Contains the number of pixels in the x-direction from WIA_IPS_XPOS to the x-coordinate of the uppermost corner of the image to be deskewed.</span></span> <span data-ttu-id="6f739-184">Portanto, ele descreve, em conjunto com WIA_IPS_DESKEW_Y, onde os dois cantos superiores da imagem distorcida estão localizados dentro do retângulo delimitador definido por WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT e WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="6f739-184">Hence, it describes, in conjunction with WIA_IPS_DESKEW_Y, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="6f739-185">sua propriedade será implementada pelo driver do scanner se ele der suporte à desalinhamento.</span><span class="sxs-lookup"><span data-stu-id="6f739-185">his property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="6f739-186">Os valores válidos para WIA_IPS_DESKEW_X devem estar entre 0 e (WIA_IPS_XEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="6f739-186">The valid values for WIA_IPS_DESKEW_X must be between 0 and (WIA_IPS_XEXTENT - 1).</span></span> <span data-ttu-id="6f739-187">Um valor de 0 significa que nenhuma distorção deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6f739-187">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="6f739-188">Essa propriedade é opcional para itens das categorias WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM; e não está disponível para WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER itens.</span><span class="sxs-lookup"><span data-stu-id="6f739-188">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="6f739-189">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="6f739-189">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <span data-ttu-id="6f739-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-191">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-191">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-192">Contém o número de pixels na direção y de WIA_IPS_YPOS para a coordenada y do canto mais à esquerda da imagem a ser deinclinada.</span><span class="sxs-lookup"><span data-stu-id="6f739-192">Contains the number of pixels in the y-direction from WIA_IPS_YPOS to the y-coordinate of the leftmost corner of the image to be deskewed.</span></span> <span data-ttu-id="6f739-193">Portanto, ele descreve, em conjunto com WIA_IPS_DESKEW_X, onde os dois cantos superiores da imagem distorcida estão localizados dentro do retângulo delimitador definido por WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT e WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="6f739-193">Hence, it describes, in conjunction with WIA_IPS_DESKEW_X, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="6f739-194">Essa propriedade é implementada pelo driver do verificador se ele der suporte à distorção.</span><span class="sxs-lookup"><span data-stu-id="6f739-194">This property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="6f739-195">Os valores válidos para WIA_IPS_DESKEW_Y devem estar entre 0 e (WIA_IPS_YEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="6f739-195">The valid values for WIA_IPS_DESKEW_Y must be between 0 and (WIA_IPS_YEXTENT - 1).</span></span> <span data-ttu-id="6f739-196">Um valor de 0 significa que nenhuma distorção deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="6f739-196">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="6f739-197">Essa propriedade é opcional para itens das categorias WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM; e não está disponível para WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER itens.</span><span class="sxs-lookup"><span data-stu-id="6f739-197">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="6f739-198">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="6f739-198">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <span data-ttu-id="6f739-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-200">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-200">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-201">Contém a origem e o modo de aquisição do scanner atual.</span><span class="sxs-lookup"><span data-stu-id="6f739-201">Contains the current scanner acquisition source and mode.</span></span> <span data-ttu-id="6f739-202">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-202">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-203">Um aplicativo lê essa propriedade para determinar a fonte de aquisição atual do scanner ou para gravar essa propriedade para definir a origem e o modo do verificador.</span><span class="sxs-lookup"><span data-stu-id="6f739-203">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="6f739-204">Além disso, os aplicativos usam essa propriedade para habilitar e desabilitar a funcionalidade do duplexador.</span><span class="sxs-lookup"><span data-stu-id="6f739-204">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="6f739-205">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="6f739-205">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="6f739-206">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-206">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-207">Flags</span><span class="sxs-lookup"><span data-stu-id="6f739-207">Flags</span></span></th>
<th><span data-ttu-id="6f739-208">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-209">DUPLEX</span><span class="sxs-lookup"><span data-stu-id="6f739-209">DUPLEX</span></span></td>
<td><span data-ttu-id="6f739-210">Examinar usando operações do duplex.</span><span class="sxs-lookup"><span data-stu-id="6f739-210">Scan using duplexer operations.</span></span> <span data-ttu-id="6f739-211">Verifique ambos os lados do documento usando configurações comuns configuradas para o item do alimentador (WIA_CATEGORY_FEEDER).</span><span class="sxs-lookup"><span data-stu-id="6f739-211">Scan both document sides using common settings configured for the feeder item (WIA_CATEGORY_FEEDER).</span></span> <span data-ttu-id="6f739-212">DUPLEX e ADVANCE_DUPLEX não podem ser ambos definidos.</span><span class="sxs-lookup"><span data-stu-id="6f739-212">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-213">ADVANCED_DUPLEX</span><span class="sxs-lookup"><span data-stu-id="6f739-213">ADVANCED_DUPLEX</span></span></td>
<td><span data-ttu-id="6f739-214">Digitalizar usando configurações individuais configuradas para cada item de alimentador filho (WIA_CATEGORY_FEEDER_FRONT e WIA_CATEGORY_FEEDER_BACK).</span><span class="sxs-lookup"><span data-stu-id="6f739-214">Scan using individual settings configured for each child feeder item (WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK).</span></span> <span data-ttu-id="6f739-215">DUPLEX e ADVANCE_DUPLEX não podem ser ambos definidos.</span><span class="sxs-lookup"><span data-stu-id="6f739-215">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-216">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="6f739-216">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="6f739-217">Primeiro examine a frente do documento.</span><span class="sxs-lookup"><span data-stu-id="6f739-217">Scan the front of the document first.</span></span> <span data-ttu-id="6f739-218">Esse valor é válido quando DUPLEX ou ADVANCED_DUPLEX é definido.</span><span class="sxs-lookup"><span data-stu-id="6f739-218">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-219">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="6f739-219">BACK_FIRST</span></span></td>
<td><span data-ttu-id="6f739-220">Primeiro examine a parte de trás do documento.</span><span class="sxs-lookup"><span data-stu-id="6f739-220">Scan the back of the document first.</span></span> <span data-ttu-id="6f739-221">Esse valor é válido quando DUPLEX ou ADVANCED_DUPLEX é definido.</span><span class="sxs-lookup"><span data-stu-id="6f739-221">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-222">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="6f739-222">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="6f739-223">Verificar somente a frente.</span><span class="sxs-lookup"><span data-stu-id="6f739-223">Scan the front only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-224">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="6f739-224">BACK_ONLY</span></span></td>
<td><span data-ttu-id="6f739-225">Verifique apenas o verso.</span><span class="sxs-lookup"><span data-stu-id="6f739-225">Scan the back only.</span></span> <span data-ttu-id="6f739-226">Esse valor é válido quando DUPLEX ou ADVANCED_DUPLEX é definido.</span><span class="sxs-lookup"><span data-stu-id="6f739-226">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <span data-ttu-id="6f739-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-228">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-228">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-229">Habilita a especificação de um anexo de verificação de filme específico quando há mais de um.</span><span class="sxs-lookup"><span data-stu-id="6f739-229">Enables specification of a particular film scanning attachment when there is more than one.</span></span></p>
<p><span data-ttu-id="6f739-230">Essa propriedade é necessária para os itens de WIA_CATEGORY_FILM quando há vários itens de verificação de filme.</span><span class="sxs-lookup"><span data-stu-id="6f739-230">This property is required for the WIA_CATEGORY_FILM items when there are multiple film scan items.</span></span> <span data-ttu-id="6f739-231">Se o dispositivo der suporte a apenas um item de filme do scanner raiz, essa propriedade será opcional.</span><span class="sxs-lookup"><span data-stu-id="6f739-231">If the device supports only one root scanner film item then this property is optional.</span></span></p>
<p><span data-ttu-id="6f739-232">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-232">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6f739-233">Valores permitidos: o BSTR deve estar na forma de @ResourceBinary ,- <ResourceID> para permitir que a localização como essa cadeia de caracteres seja exposta ao usuário por meio da interface do usuário de verificação de filme.</span><span class="sxs-lookup"><span data-stu-id="6f739-233">Allowed values: The BSTR should be in the form of @ResourceBinary,-<ResourceID> to allow localization as this string would be exposed to the user through the film scanning UI.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <span data-ttu-id="6f739-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-235">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-235">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-236">Habilita a configuração da verificação de filme atual.</span><span class="sxs-lookup"><span data-stu-id="6f739-236">Enables configuration of the current film scan.</span></span></p>
<p><span data-ttu-id="6f739-237">Essa propriedade é necessária para o item de WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-237">This property is required for the WIA_CATEGORY_FILM item.</span></span></p>
<p><span data-ttu-id="6f739-238">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6f739-238">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6f739-239">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-239">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-240">Constante</span><span class="sxs-lookup"><span data-stu-id="6f739-240">Constant</span></span></th>
<th><span data-ttu-id="6f739-241">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-241">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-242">WIA_FILM_COLOR_SLIDE</span><span class="sxs-lookup"><span data-stu-id="6f739-242">WIA_FILM_COLOR_SLIDE</span></span></td>
<td><span data-ttu-id="6f739-243">Digitalizar um slide de cor.</span><span class="sxs-lookup"><span data-stu-id="6f739-243">Scan for a color slide.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-244">WIA_FILM_COLOR_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="6f739-244">WIA_FILM_COLOR_NEGATIVE</span></span></td>
<td><span data-ttu-id="6f739-245">Verificar se há uma cor negativa.</span><span class="sxs-lookup"><span data-stu-id="6f739-245">Scan for a color negative.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-246">WIA_FILM_BW_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="6f739-246">WIA_FILM_BW_NEGATIVE</span></span></td>
<td><span data-ttu-id="6f739-247">Verificar se há um negativo preto e branco.</span><span class="sxs-lookup"><span data-stu-id="6f739-247">Scan for a black and white negative.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <span data-ttu-id="6f739-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-249">Reservado para uso futuro e não é implementado neste momento.</span><span class="sxs-lookup"><span data-stu-id="6f739-249">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="6f739-250">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-250">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="6f739-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-252">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-252">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-253">Especifica quantos itens são armazenados no item de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-253">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="6f739-254">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-254">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <span data-ttu-id="6f739-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-256">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-256">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-257">Ativa ou desativa a lâmpada do scanner.</span><span class="sxs-lookup"><span data-stu-id="6f739-257">Turns the scanner lamp on or off.</span></span></p>
<p><span data-ttu-id="6f739-258">Opcional para os itens WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM e recomendado para WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-258">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-259">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6f739-259">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6f739-260">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-260">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-261">Constante</span><span class="sxs-lookup"><span data-stu-id="6f739-261">Constant</span></span></th>
<th><span data-ttu-id="6f739-262">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-263">WIA_LAMP_ON</span><span class="sxs-lookup"><span data-stu-id="6f739-263">WIA_LAMP_ON</span></span></td>
<td><span data-ttu-id="6f739-264">Ligue a lâmpada.</span><span class="sxs-lookup"><span data-stu-id="6f739-264">Turn on the lamp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-265">WIA_LAMP_OFF</span><span class="sxs-lookup"><span data-stu-id="6f739-265">WIA_LAMP_OFF</span></span></td>
<td><span data-ttu-id="6f739-266">Desative a lâmpada.</span><span class="sxs-lookup"><span data-stu-id="6f739-266">Turn off the lamp.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <span data-ttu-id="6f739-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-268">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-268">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-269">Define o tempo máximo para manter a lâmpada quando o scanner não está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="6f739-269">Sets the maximum time to keep the lamp on when the scanner is not being used.</span></span></p>
<p><span data-ttu-id="6f739-270">Opcional para os itens WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM e recomendado para WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-270">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-271">Tipo: <strong>VT_UI4</strong>, Access: leitura/gravação, valores válidos: 0-0xFFF segundos</span><span class="sxs-lookup"><span data-stu-id="6f739-271">Type: <strong>VT_UI4</strong>, Access: Read/Write, Valid Values: 0 - 0xFFF seconds</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <span data-ttu-id="6f739-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-273">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-273">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-274">Especifica a largura máxima, em milésimos de polegada, que é verificada no eixo horizontal (X) na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="6f739-274">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span> <span data-ttu-id="6f739-275">Essa pode ser a largura do alimentador de planilhas ou da base de digitalização, de acordo com o tipo de item.</span><span class="sxs-lookup"><span data-stu-id="6f739-275">This may be the width of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="6f739-276">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <span data-ttu-id="6f739-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-278">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-278">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-279">Especifica a altura máxima, em milésimos de polegada, que é verificada no eixo vertical (Y) na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="6f739-279">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span> <span data-ttu-id="6f739-280">Essa pode ser a altura do alimentador de planilhas ou da base de digitalização, de acordo com o tipo de item.</span><span class="sxs-lookup"><span data-stu-id="6f739-280">This may be the height of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="6f739-281">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-281">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <span data-ttu-id="6f739-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-283">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-283">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-284">Especifica a largura mínima, em milésimos de polegada, que é verificada no eixo horizontal (X) na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="6f739-284">Specifies the minimum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="6f739-285">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-285">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <span data-ttu-id="6f739-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-287">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-287">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-288">Especifica a altura mínima, em milésimos de polegada, que é verificada no eixo vertical (Y) na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="6f739-288">Specifies the minimum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="6f739-289">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-289">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <span data-ttu-id="6f739-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-291">Reservado para uso futuro e não é implementado neste momento.</span><span class="sxs-lookup"><span data-stu-id="6f739-291">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="6f739-292">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-292">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <span data-ttu-id="6f739-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-294">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-294">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-295">Resolução óptica horizontal.</span><span class="sxs-lookup"><span data-stu-id="6f739-295">Horizontal Optical Resolution.</span></span> <span data-ttu-id="6f739-296">Resolução óptica horizontal mais alta com suporte em DPI.</span><span class="sxs-lookup"><span data-stu-id="6f739-296">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="6f739-297">Essa propriedade é um único valor.</span><span class="sxs-lookup"><span data-stu-id="6f739-297">This property is a single value.</span></span> <span data-ttu-id="6f739-298">Esta não é uma lista de todas as resoluções que podem ser geradas pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-298">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="6f739-299">Em vez disso, essa é a resolução da fibra óptica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-299">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="6f739-300">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-300">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="6f739-301">Essa propriedade é necessária para todos os itens.</span><span class="sxs-lookup"><span data-stu-id="6f739-301">This property is required for all items.</span></span></p>
<p><span data-ttu-id="6f739-302">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-302">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <span data-ttu-id="6f739-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-304">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-304">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-305">Resolução óptica vertical.</span><span class="sxs-lookup"><span data-stu-id="6f739-305">Vertical Optical Resolution.</span></span> <span data-ttu-id="6f739-306">Resolução óptica vertical com suporte mais alta em DPI.</span><span class="sxs-lookup"><span data-stu-id="6f739-306">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="6f739-307">Essa propriedade é um único valor.</span><span class="sxs-lookup"><span data-stu-id="6f739-307">This property is a single value.</span></span> <span data-ttu-id="6f739-308">Essa não é uma lista de todas as resoluções que são geradas pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-308">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="6f739-309">Em vez disso, essa é a resolução da fibra óptica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-309">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="6f739-310">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-310">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="6f739-311">Essa propriedade é necessária para todos os itens.</span><span class="sxs-lookup"><span data-stu-id="6f739-311">This property is required for all items.</span></span></p>
<p><span data-ttu-id="6f739-312">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <span data-ttu-id="6f739-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-314">Especifica a orientação atual dos documentos a serem examinados.</span><span class="sxs-lookup"><span data-stu-id="6f739-314">Specifies the current orientation of the documents to be scanned.</span></span> <span data-ttu-id="6f739-315">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-315">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-316">Um aplicativo define essa propriedade para definir a orientação original de uma página ou imagem a ser adquirida.</span><span class="sxs-lookup"><span data-stu-id="6f739-316">An application sets this property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="6f739-317">Para obter informações sobre como usar WIA_IPS_ORIENTATION, consulte <strong>WIA_IPS_PAGE_SIZE</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f739-317">For information on how to use WIA_IPS_ORIENTATION, see <strong>WIA_IPS_PAGE_SIZE</strong>.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-318">WIA_IPS_ORIENTATION se refere à posição do documento a ser examinado na base do scanner ou no alimentador.</span><span class="sxs-lookup"><span data-stu-id="6f739-318">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="6f739-319">É a orientação do documento em relação à direção da verificação.</span><span class="sxs-lookup"><span data-stu-id="6f739-319">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="6f739-320">WIA_IPS_ROTATION se refere à rotação aplicada à imagem depois que ela é verificada, logo antes de a imagem ser transferida para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f739-320">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-321">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6f739-321">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6f739-322">A tabela a seguir tem as quatro constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-322">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-323">Valor</span><span class="sxs-lookup"><span data-stu-id="6f739-323">Value</span></span></th>
<th><span data-ttu-id="6f739-324">Definição</span><span class="sxs-lookup"><span data-stu-id="6f739-324">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-325">ORIENTAÇÕES</span><span class="sxs-lookup"><span data-stu-id="6f739-325">PORTRAIT</span></span></td>
<td><span data-ttu-id="6f739-326">0 graus.</span><span class="sxs-lookup"><span data-stu-id="6f739-326">0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-327">AMBIENTE</span><span class="sxs-lookup"><span data-stu-id="6f739-327">LANDSCAPE</span></span></td>
<td><span data-ttu-id="6f739-328">rotação no sentido anti-horário de 90 graus, em relação à orientação retrato.</span><span class="sxs-lookup"><span data-stu-id="6f739-328">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-329">ROT180</span><span class="sxs-lookup"><span data-stu-id="6f739-329">ROT180</span></span></td>
<td><span data-ttu-id="6f739-330">rotação no sentido anti-horário de 180 graus, em relação à orientação retrato.</span><span class="sxs-lookup"><span data-stu-id="6f739-330">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-331">ROT270</span><span class="sxs-lookup"><span data-stu-id="6f739-331">ROT270</span></span></td>
<td><span data-ttu-id="6f739-332">rotação no sentido anti-horário de 270 graus, em relação à orientação retrato.</span><span class="sxs-lookup"><span data-stu-id="6f739-332">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <span data-ttu-id="6f739-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-334">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-334">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-335">Contém o tamanho da página que está atualmente definida para ser verificada.</span><span class="sxs-lookup"><span data-stu-id="6f739-335">Contains the size of the page that is currently set to be scanned.</span></span> <span data-ttu-id="6f739-336">Um aplicativo define essa propriedade para selecionar as dimensões da página a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="6f739-336">An application sets this property to select the dimensions of the page to scan.</span></span> <span data-ttu-id="6f739-337">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-337">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-338">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6f739-338">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6f739-339">Para obter as constantes que podem ser usadas com essa propriedade, consulte <a href="-wia-wia2-pagesizeconstants.md"><strong>constantes de tamanho de página WIA 2,0</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6f739-339">For the constants that can be used with this property, see <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2.0 Page Size Constants</strong></a>.</span></span> <span data-ttu-id="6f739-340">Observe esses tamanhos não fixos, em particular:</span><span class="sxs-lookup"><span data-stu-id="6f739-340">Note these non-fixed sizes, in particular:</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-341">Valor</span><span class="sxs-lookup"><span data-stu-id="6f739-341">Value</span></span></th>
<th><span data-ttu-id="6f739-342">Definição</span><span class="sxs-lookup"><span data-stu-id="6f739-342">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-343">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="6f739-343">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="6f739-344">Definido pelos valores das propriedades <strong>WIA_IPS_PAGE_HEIGHT</strong> e <strong>WIA_IPS_PAGE_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f739-344">Defined by the values of the <strong>WIA_IPS_PAGE_HEIGHT</strong> and <strong>WIA_IPS_PAGE_WIDTH</strong> properties.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-345">WIA_PAGE_AUTO</span><span class="sxs-lookup"><span data-stu-id="6f739-345">WIA_PAGE_AUTO</span></span></td>
<td><span data-ttu-id="6f739-346">O tamanho da página é determinado automaticamente pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-346">Page size is automatically determined by the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-347">WIA_PAGE_CUSTOM_BASE</span><span class="sxs-lookup"><span data-stu-id="6f739-347">WIA_PAGE_CUSTOM_BASE</span></span></td>
<td><span data-ttu-id="6f739-348">Um tamanho de página personalizado cujas dimensões já são conhecidas pelo aplicativo e o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-348">A custom page size whose dimensions are already known to the application and the device driver.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="6f739-349">O valor da propriedade <strong>WIA_IPS_ORIENTATION</strong> determina a orientação da página atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f739-349">The value of the <strong>WIA_IPS_ORIENTATION</strong> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="6f739-350">As propriedades <strong>WIA_IPS_PAGE_WIDTH</strong> e <strong>WIA_IPS_PAGE_HEIGHT</strong> relatam as dimensões da página, em milésimos de polegada.</span><span class="sxs-lookup"><span data-stu-id="6f739-350">The <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="6f739-351">Essas propriedades devem estar em acordo com <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, que contêm as dimensões da página em pixels.</span><span class="sxs-lookup"><span data-stu-id="6f739-351">These properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-352">Os valores válidos do tipo WIA_PROP_LIST dependem das configurações válidas da propriedade <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f739-352">Valid values of type WIA_PROP_LIST depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="6f739-353">Se, por exemplo, o dispositivo não puder verificar documentos orientados a paisagem com uma configuração de WIA_PAGE_A4, WIA_PAGE_A4 não será um valor válido para a propriedade <strong>WIA_IPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> estiver definido como paisagem.</span><span class="sxs-lookup"><span data-stu-id="6f739-353">If, for example, the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 is not a valid value for the <strong>WIA_IPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-354">Se um aplicativo definir <strong>WIA_IPS_PAGE_SIZE</strong> para qualquer valor diferente dos três na tabela acima, o minidriver deverá ajustar os valores de <strong>WIA_IPS_PAGE_WIDTH</strong> e <strong>WIA_IPS_PAGE_HEIGHT</strong> às dimensões da página em milésimos de uma polegada.</span><span class="sxs-lookup"><span data-stu-id="6f739-354">If an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to any value other than the three in the table above, the minidriver should adjust the values of <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="6f739-355">Ele também deve ajustar os valores de <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> às dimensões da página em pixels.</span><span class="sxs-lookup"><span data-stu-id="6f739-355">It should also adjust the values of <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="6f739-356">Se uma configuração de extensão (<strong>WIA_IPS_XEXTENT</strong> ou <strong>WIA_IPS_YEXTENT</strong>) for alterada para um valor que não corresponda à configuração de tamanho de página atual, minidriver deverá alterar o valor da propriedade <strong>WIA_IPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="6f739-356">If an extent setting (<strong>WIA_IPS_XEXTENT</strong> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page size setting, the minidriver should change the value of the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="6f739-357">O minidriver também deve modificar <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> ou <strong>WIA_IPS_PAGE_HEIGHT</strong> de acordo com a nova configuração de extensão.</span><span class="sxs-lookup"><span data-stu-id="6f739-357">The minidriver should also modify <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> or <strong>WIA_IPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="6f739-358">Se <strong>WIA_IPS_ORIENTATION</strong> for definido como paisagem, as configurações de extensão serão trocadas em relação aos seus valores usuais.</span><span class="sxs-lookup"><span data-stu-id="6f739-358">If <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE, the extent settings will be exchanged relative to their usual values.</span></span> <span data-ttu-id="6f739-359">Por exemplo, se um aplicativo definir <strong>WIA_IPS_PAGE_SIZE</strong> como WIA_PAGE_A4, o minidriver definirá <strong>WIA_IPS_PAGE_WIDTH</strong> como 11692 e <strong>WIA_IPS_PAGE_HEIGHT</strong> como 8267.</span><span class="sxs-lookup"><span data-stu-id="6f739-359">For example, if an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver sets <strong>WIA_IPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_IPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="6f739-360">(O minidriver também deve ajustar <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> de acordo.)</span><span class="sxs-lookup"><span data-stu-id="6f739-360">(The minidriver should also adjust <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.)</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-361">Se <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> for definido como WIA_PAGE_CUSTOM, a configuração de orientação não será usada para determinar as dimensões de extensão da página a ser examinada.</span><span class="sxs-lookup"><span data-stu-id="6f739-361">If <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-362">O minidriver é responsável por garantir que a propriedade <strong>WIA_IPS_ORIENTATION</strong> esteja em contrato com a área de seleção atual.</span><span class="sxs-lookup"><span data-stu-id="6f739-362">The minidriver is responsible for ensuring that the <strong>WIA_IPS_ORIENTATION</strong> property is in agreement with the current selection area.</span></span> <span data-ttu-id="6f739-363">Se um aplicativo alterar o valor de <strong>WIA_IPS_ORIENTATION</strong> para um que seja inválido para o tamanho de página selecionado no momento, o minidriver deverá alterar o valor de <strong>WIA_IPS_PAGE_SIZE</strong> para um tamanho de página com suporte no novo valor de orientação.</span><span class="sxs-lookup"><span data-stu-id="6f739-363">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_IPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="6f739-364">Se um aplicativo definir a propriedade <strong>WIA_IPS_PAGE_SIZE</strong> como WIA_PAGE_CUSTOM, a área de seleção atual não será afetada.</span><span class="sxs-lookup"><span data-stu-id="6f739-364">If an application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="6f739-365">O minidriver WIA deve obter o layout da imagem atual, começando com as configurações atuais das propriedades <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f739-365">The WIA minidriver should obtain the current image layout, starting from the current settings of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="6f739-366">Se a configuração tamanho da página resultar em uma área de seleção que está fora do ambiente do scanner, o minidriver deverá ajustar automaticamente os valores das propriedades <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> para as configurações válidas.</span><span class="sxs-lookup"><span data-stu-id="6f739-366">If the page size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="6f739-367">Se as propriedades <strong>WIA_IPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> forem definidas ao mesmo tempo e forem inválidas quando aplicadas em combinação, o minidriver deverá falhar as configurações do aplicativo retornando um erro no <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>.</span><span class="sxs-lookup"><span data-stu-id="6f739-367">If the <strong>WIA_IPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span></p>
<p><span data-ttu-id="6f739-368">Os quatro exemplos a seguir mostram diferentes cenários de <strong>WIA_IPS_PAGE_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f739-368">The following four examples show different <strong>WIA_IPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="6f739-369">O driver relata as configurações.</span><span class="sxs-lookup"><span data-stu-id="6f739-369">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="6f739-370">Um aplicativo define a propriedade <strong>WIA_IPS_PAGE_SIZE</strong> como WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="6f739-370">An application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="6f739-371">Um aplicativo define a propriedade <strong>WIA_IPS_ORIENTATION</strong> como paisagem.</span><span class="sxs-lookup"><span data-stu-id="6f739-371">An application sets the <strong>WIA_IPS_ORIENTATION</strong> property to LANDSCAPE.</span></span></li>
<li><span data-ttu-id="6f739-372">Um aplicativo altera a propriedade <strong>WIA_IPS_XEXTENT</strong> para um valor menor.</span><span class="sxs-lookup"><span data-stu-id="6f739-372">An application changes the <strong>WIA_IPS_XEXTENT</strong> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="6f739-373"><strong>Exemplo 1: o minidriver relata as configurações</strong></span><span class="sxs-lookup"><span data-stu-id="6f739-373"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="6f739-374">No exemplo a seguir, o minidriver define uma área de seleção personalizada antes que um aplicativo defina as propriedades de WIA.</span><span class="sxs-lookup"><span data-stu-id="6f739-374">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="6f739-375">Nesse caso, a área de seleção representa a mesa inteira.</span><span class="sxs-lookup"><span data-stu-id="6f739-375">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="6f739-376"><strong>Exemplo 2: um aplicativo define a</strong> <strong></strong><strong>Propriedade WIA_IPS_PAGE_SIZE como WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="6f739-376"><strong>Example 2: An application sets the</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="6f739-377"><strong>Exemplo 3: um aplicativo define a</strong> <strong></strong><strong>Propriedade WIA_IPS_ORIENTATION como paisagem</strong>  </span><span class="sxs-lookup"><span data-stu-id="6f739-377"><strong>Example 3: An application sets the</strong> <strong>WIA_IPS_ORIENTATION</strong>  <strong>property to LANDSCAPE</strong></span></span></p>
<p><span data-ttu-id="6f739-378">A base física deve ser capaz de adquirir uma página que estava originalmente na orientação paisagem.</span><span class="sxs-lookup"><span data-stu-id="6f739-378">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="6f739-379"><strong>Exemplo 4: um aplicativo altera a</strong> <strong></strong> <strong>Propriedade WIA_IPS_XEXTENT para um valor menor</strong></span><span class="sxs-lookup"><span data-stu-id="6f739-379"><strong>Example 4: An application changes the</strong> <strong>WIA_IPS_XEXTENT</strong> <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="6f739-380">No exemplo a seguir, um aplicativo altera a propriedade <strong>WIA_IPS_XEXTENT</strong> para 1000.</span><span class="sxs-lookup"><span data-stu-id="6f739-380">In the following example, an application changes the <strong>WIA_IPS_XEXTENT</strong> property to 1000.</span></span> <span data-ttu-id="6f739-381">O minidriver deve assumir que o novo valor contido no <strong>WIA_IPS_XEXTENT</strong> não é mais válido para a propriedade <strong>WIA_IPS_PAGE_SIZE</strong> e, portanto, deve alterar <strong>WIA_IPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="6f739-381">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_IPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="6f739-382">O minidriver também deve ajustar <strong>WIA_IPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f739-382">The minidriver must also adjust <strong>WIA_IPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <span data-ttu-id="6f739-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-384">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-384">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-385">Contém a altura, em milésimos de polegada, da página atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f739-385">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="6f739-386">O minidriver cria e mantém a propriedade <strong>WIA_IPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f739-386">The minidriver creates and maintains the <strong>WIA_IPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="6f739-387">Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo examinada.</span><span class="sxs-lookup"><span data-stu-id="6f739-387">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="6f739-388">Se as configurações de extensão forem diferentes dos tamanhos de página conhecidos, essa propriedade relatará a altura da página cujo <strong>WIA_IPS_PAGE_SIZE</strong> Propriedade está definida como WIA_PAGE_CUSTOM (que é um valor da propriedade <strong>WIA_IPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="6f739-388">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_IPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="6f739-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> deve estar em sincronia com <strong>WIA_IPS_XEXTENT</strong>, que relata a altura, em pixels, da página a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="6f739-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> must be in sync with <strong>WIA_IPS_XEXTENT</strong>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="6f739-390">Essa propriedade é necessária para itens de WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-390">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="6f739-391">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <span data-ttu-id="6f739-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-393">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-393">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-394">Contém a largura da página atual selecionada, em milésimos de polegada.</span><span class="sxs-lookup"><span data-stu-id="6f739-394">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="6f739-395">Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo examinada.</span><span class="sxs-lookup"><span data-stu-id="6f739-395">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="6f739-396">Se as configurações de extensão forem diferentes de tamanhos de página conhecidos, essa propriedade relatará a largura da página cuja propriedade <strong>WIA_IPS_PAGE_SIZE</strong> está definida como WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="6f739-396">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="6f739-397"><strong>WIA_IPS_PAGE_WIDTH</strong> deve estar em sincronia com o valor de <strong>WIA_IPS_XEXTENT</strong>, que relata a largura, em pixels, da página a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="6f739-397"><strong>WIA_IPS_PAGE_WIDTH</strong> must be in sync with the value of <strong>WIA_IPS_XEXTENT</strong>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="6f739-398">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-398">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-399">Essa propriedade é necessária para itens de WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-399">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="6f739-400">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-400">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <span data-ttu-id="6f739-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-402">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-402">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-403">Contém o número atual de páginas a serem adquiridas de um alimentador automático de documentos.</span><span class="sxs-lookup"><span data-stu-id="6f739-403">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="6f739-404">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-404">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-405">Tipo: <strong>VT_I4</strong>; Acesso: leitura/gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> isso é zero por meio do número máximo de páginas que o verificador pode verificar.</span><span class="sxs-lookup"><span data-stu-id="6f739-405">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> This is zero through the maximum number of pages that the scanner can scan.</span></span> <span data-ttu-id="6f739-406">O valor é ALL_PAGES (= 0) se o verificador pode verificar continuamente.</span><span class="sxs-lookup"><span data-stu-id="6f739-406">The value is ALL_PAGES (= 0) if the scanner can scan continuously.</span></span></p>
<p><span data-ttu-id="6f739-407">Um aplicativo lê essa propriedade para determinar a capacidade da página do alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="6f739-407">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="6f739-408">O aplicativo também define essa propriedade como o número de páginas que ele vai verificar.</span><span class="sxs-lookup"><span data-stu-id="6f739-408">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-409">Se o modo duplex estiver habilitado (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> é definido como alimentador | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> ainda é igual ao número de páginas a serem verificadas.</span><span class="sxs-lookup"><span data-stu-id="6f739-409">If duplex mode is enabled (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-410">Uma folha de papel conterá automaticamente duas páginas se o DUPLEX estiver habilitado, mesmo se o lado do verso da página estiver em branco.</span><span class="sxs-lookup"><span data-stu-id="6f739-410">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="6f739-411">Definir <strong>WIA_IPS_PAGES</strong> como 1 faz com que um scanner processe um lado da página.</span><span class="sxs-lookup"><span data-stu-id="6f739-411">Setting <strong>WIA_IPS_PAGES</strong> to 1 causes a scanner to process one side of the page.</span></span> <span data-ttu-id="6f739-412">Recomendamos que, se um scanner não conseguir verificar apenas um lado de uma página enquanto estiver no modo duplex, você alterará o valor <strong>WIA_IPS_PAGES</strong> para o membro Inc do membro de intervalo da estrutura de WIA_PROPERTY_INFO para 2.</span><span class="sxs-lookup"><span data-stu-id="6f739-412">We recommend that, if a scanner is unable to scan only one side of a page while in duplex mode, you change the <strong>WIA_IPS_PAGES</strong> value for the Inc member of the Range member of the WIA_PROPERTY_INFO structure to 2.</span></span> <span data-ttu-id="6f739-413">Esse valor sinaliza ao aplicativo que ele deve solicitar páginas em múltiplos de dois.</span><span class="sxs-lookup"><span data-stu-id="6f739-413">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="6f739-414">Um valor de ALL_PAGES (= 0) significa que <em>todas as</em> páginas atualmente carregadas no alimentador de documentos serão verificadas.</span><span class="sxs-lookup"><span data-stu-id="6f739-414">A value of ALL_PAGES (= 0) means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <span data-ttu-id="6f739-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-416">Contém a configuração atual para pixels brancos e pretos.</span><span class="sxs-lookup"><span data-stu-id="6f739-416">Contains the current setting for white and black pixels.</span></span> <span data-ttu-id="6f739-417">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-417">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-418">Um aplicativo lê esse valor para determinar o valor de branco ou preto (dependendo do que o aplicativo está fazendo).</span><span class="sxs-lookup"><span data-stu-id="6f739-418">An application reads this value to determine the value of WHITE or BLACK (depending on what the application is doing).</span></span></p>
<p><span data-ttu-id="6f739-419">Necessário para todos os itens habilitados para aquisição ou armazenados; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-419">Required for all acquisition enabled or stored items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="6f739-420">Não há suporte para itens de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-420">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="6f739-421">Tipo: <strong>VT_I4</strong>; Acesso: leitura/gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="6f739-421">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="6f739-422">Se o dispositivo puder ser definido como apenas um único valor, crie um tipo de WIA_PROP_LIST e coloque o valor válido nele.</span><span class="sxs-lookup"><span data-stu-id="6f739-422">If the device can be set to only a single value, create a WIA_PROP_LIST type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="6f739-423">A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-423">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-424">Valor</span><span class="sxs-lookup"><span data-stu-id="6f739-424">Value</span></span></th>
<th><span data-ttu-id="6f739-425">Definição</span><span class="sxs-lookup"><span data-stu-id="6f739-425">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-426">WIA_PHOTO_WHITE_0</span><span class="sxs-lookup"><span data-stu-id="6f739-426">WIA_PHOTO_WHITE_0</span></span></td>
<td><span data-ttu-id="6f739-427">O branco é 0 e o preto é 1.</span><span class="sxs-lookup"><span data-stu-id="6f739-427">WHITE is 0, and BLACK is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-428">WIA_PHOTO_WHITE_1</span><span class="sxs-lookup"><span data-stu-id="6f739-428">WIA_PHOTO_WHITE_1</span></span></td>
<td><span data-ttu-id="6f739-429">O branco é 1 e o preto é 0.</span><span class="sxs-lookup"><span data-stu-id="6f739-429">WHITE is 1, and BLACK is 0.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <span data-ttu-id="6f739-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-431">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-431">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-432">Indica o modo de visualização de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-432">Indicates the preview mode for a device.</span></span> <span data-ttu-id="6f739-433">Um aplicativo define essa propriedade para posicionar o dispositivo em um modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="6f739-433">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="6f739-434">Essa propriedade é necessária para os itens WIA_CATEGORY_FLATBED e WIA_CATEGORY_FILM, opcional para o item WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-434">This property is required for the WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items, optional for the WIA_CATEGORY_FEEDER item.</span></span></p>
<p><span data-ttu-id="6f739-435">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6f739-435">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6f739-436">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-436">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-437">Valor</span><span class="sxs-lookup"><span data-stu-id="6f739-437">Value</span></span></th>
<th><span data-ttu-id="6f739-438">Definição</span><span class="sxs-lookup"><span data-stu-id="6f739-438">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-439">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="6f739-439">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="6f739-440">O aplicativo executará uma verificação final.</span><span class="sxs-lookup"><span data-stu-id="6f739-440">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-441">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="6f739-441">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="6f739-442">O aplicativo executará uma verificação de visualização.</span><span class="sxs-lookup"><span data-stu-id="6f739-442">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <span data-ttu-id="6f739-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-444">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-444">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-445">Especifica se a imagem de visualização existente pode ser atualizada durante uma visualização de imagem (em resposta a uma alteração nas propriedades WIA_IPA_DATATYPE ou WIA_IPA_DEPTH).</span><span class="sxs-lookup"><span data-stu-id="6f739-445">Specifies whether the existing preview image can be updated during an image preview (in response to a change in the WIA_IPA_DATATYPE or WIA_IPA_DEPTH properties).</span></span></p>
<p><span data-ttu-id="6f739-446">Essa propriedade é opcional para todos os itens habilitados para aquisição que dão suporte a verificações de visualização; ou seja, há suporte para WIA_IPS_PREVIEW com WIA_PREVIEW_SCAN.</span><span class="sxs-lookup"><span data-stu-id="6f739-446">This property is optional for all acquisition enabled items that support preview scans; that is, WIA_IPS_PREVIEW is supported with WIA_PREVIEW_SCAN.</span></span> <span data-ttu-id="6f739-447">Isso inclui itens de tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-447">This includes items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-448">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-448">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6f739-449">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-449">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-450">Constante</span><span class="sxs-lookup"><span data-stu-id="6f739-450">Constant</span></span></th>
<th><span data-ttu-id="6f739-451">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-451">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-452">WIA_ADVANCED_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="6f739-452">WIA_ADVANCED_PREVIEW</span></span></td>
<td><span data-ttu-id="6f739-453">A atualização da imagem existente é possível.</span><span class="sxs-lookup"><span data-stu-id="6f739-453">Updating the existing image is possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-454">WIA_BASIC_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="6f739-454">WIA_BASIC_PREVIEW</span></span></td>
<td><span data-ttu-id="6f739-455">Outra verificação de visualização deve ser executada porque não é possível atualizar a imagem existente.</span><span class="sxs-lookup"><span data-stu-id="6f739-455">Another preview scan must be executed because updating the existing image is not possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <span data-ttu-id="6f739-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-457">Contém a configuração de rotação atual, se for implementada.</span><span class="sxs-lookup"><span data-stu-id="6f739-457">Contains the current rotation setting, if it is implemented.</span></span> <span data-ttu-id="6f739-458">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-458">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-459">Um aplicativo define essa propriedade para informar ao driver quanto (se houver) para girar a imagem antes que o driver a retorne ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f739-459">An application sets this property to inform the driver how much (if at all) to rotate the image before the driver returns it to the application.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-460">WIA_IPS_ORIENTATION se refere à posição do documento a ser examinado na base do scanner ou no alimentador.</span><span class="sxs-lookup"><span data-stu-id="6f739-460">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="6f739-461">É a orientação do documento em relação à direção da verificação.</span><span class="sxs-lookup"><span data-stu-id="6f739-461">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="6f739-462">WIA_IPS_ROTATION se refere à rotação aplicada à imagem depois que ela é verificada, logo antes de a imagem ser transferida para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f739-462">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-463">O minidriver WIA é responsável por girar os dados da imagem antes de enviá-los de volta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f739-463">The WIA minidriver is responsible for rotating the image data before sending it back to the application.</span></span> <span data-ttu-id="6f739-464">O aplicativo é responsável por verificar os cabeçalhos de imagem para ver os valores recentemente girados.</span><span class="sxs-lookup"><span data-stu-id="6f739-464">The application is responsible for checking the image headers to see the newly rotated values.</span></span></p>
<p><span data-ttu-id="6f739-465">Existe uma confusão considerável sobre como resolver o efeito de rotação na área de seleção da imagem atual (que é definida pelas propriedades <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> ).</span><span class="sxs-lookup"><span data-stu-id="6f739-465">Considerable confusion exists about resolving the effect of rotation on the current image's selection area (which is defined by the <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> properties).</span></span></p>
<p><span data-ttu-id="6f739-466">A <em>área de seleção</em> refere-se à área selecionada na base do scanner físico da qual uma imagem é adquirida.</span><span class="sxs-lookup"><span data-stu-id="6f739-466"><em>Selection area</em> refers to the selected area on the physical scanner bed that an image is be acquired from.</span></span> <span data-ttu-id="6f739-467"><strong>WIA_IPS_ROTATION</strong> não modifica a área de seleção.</span><span class="sxs-lookup"><span data-stu-id="6f739-467"><strong>WIA_IPS_ROTATION</strong> does not modify the selection area.</span></span> <span data-ttu-id="6f739-468">O driver aplica uma rotação no sentido anti-horário de acordo com <strong>WIA_IPS_ROTATION</strong> somente depois que o driver tiver adquirido a área de seleção apropriada.</span><span class="sxs-lookup"><span data-stu-id="6f739-468">The driver applies a counterclockwise rotation according to <strong>WIA_IPS_ROTATION</strong> only after the driver has acquired the appropriate selection area.</span></span> <span data-ttu-id="6f739-469"><strong>WIA_IPS_ROTATION</strong> afeta as dimensões da imagem de saída, portanto, essas dimensões devem ser refletidas no cabeçalho de dados da imagem resultante.</span><span class="sxs-lookup"><span data-stu-id="6f739-469"><strong>WIA_IPS_ROTATION</strong> does affect the dimensions of the output image, so these dimensions must be reflected in the resulting image's data header.</span></span></p>
<p><span data-ttu-id="6f739-470">Opcional para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-470">Optional for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-471">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="6f739-471">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="6f739-472">As constantes de rotação a seguir são definidas.</span><span class="sxs-lookup"><span data-stu-id="6f739-472">The following rotation constants are defined.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-473">Constante</span><span class="sxs-lookup"><span data-stu-id="6f739-473">Constant</span></span></th>
<th><span data-ttu-id="6f739-474">Definição</span><span class="sxs-lookup"><span data-stu-id="6f739-474">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-475">ORIENTAÇÕES</span><span class="sxs-lookup"><span data-stu-id="6f739-475">PORTRAIT</span></span></td>
<td><span data-ttu-id="6f739-476">O driver não irá girar a imagem.</span><span class="sxs-lookup"><span data-stu-id="6f739-476">The driver will not rotate the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-477">AMBIENTE</span><span class="sxs-lookup"><span data-stu-id="6f739-477">LANDSCAPE</span></span></td>
<td><span data-ttu-id="6f739-478">O driver Tnão gira a imagem 90 graus no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="6f739-478">TThe driver rotates the image 90 degrees counterclockwise.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-479">ROT180</span><span class="sxs-lookup"><span data-stu-id="6f739-479">ROT180</span></span></td>
<td><span data-ttu-id="6f739-480">O driver gira a imagem 180 graus no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="6f739-480">The driver rotates the image 180 degrees counterclockwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-481">ROT270</span><span class="sxs-lookup"><span data-stu-id="6f739-481">ROT270</span></span></td>
<td><span data-ttu-id="6f739-482">O driver gira a imagem 270 graus no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="6f739-482">The driver rotates the image 270 degrees counterclockwise.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <span data-ttu-id="6f739-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-484">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-484">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-485">Especifica se o aplicativo deve usar o filtro de segmentação do driver para verificação de várias regiões.</span><span class="sxs-lookup"><span data-stu-id="6f739-485">Specifies whether the application should use the driver's segmentation filter for multi-region scanning.</span></span> <span data-ttu-id="6f739-486">WIA_IPS_SEGMENTATION deve ser implementado para itens de WIA_CATEGORY_FLATBED e WIA_CATEGORY_FILM se eles suportarem a criação de itens filho com um filtro de segmentação ou se o próprio driver criar itens filho para os quadros fixos.</span><span class="sxs-lookup"><span data-stu-id="6f739-486">WIA_IPS_SEGMENTATION must be implemented for WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items if they support either the creation of child items with a segmentation filter or if the driver itself creates child items for fixed frames.</span></span></p>
<p><span data-ttu-id="6f739-487">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-487">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6f739-488">A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-488">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-489">Valor</span><span class="sxs-lookup"><span data-stu-id="6f739-489">Value</span></span></th>
<th><span data-ttu-id="6f739-490">Definição</span><span class="sxs-lookup"><span data-stu-id="6f739-490">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-491">WIA_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="6f739-491">WIA_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="6f739-492">O aplicativo deve usar o filtro de segmentação para verificação de várias regiões.</span><span class="sxs-lookup"><span data-stu-id="6f739-492">The application should use the segmentation filter for multi-region scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-493">WIA_DONT_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="6f739-493">WIA_DONT_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="6f739-494">O driver cria os próprios itens filho para verificação de várias regiões.</span><span class="sxs-lookup"><span data-stu-id="6f739-494">The driver creates the child items itself for multi-region scanning.</span></span> <span data-ttu-id="6f739-495">Esse é geralmente o caso se o verificador usar quadros fixos para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="6f739-495">This is usually the case if the scanner uses fixed frames for this purpose.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-496">É possível que um driver venha a vir com um filtro de segmentação, mas ainda tem WIA_IPS_SEGMENTATION definido como WIA_DONT_USE_SEGMENTATION_FILTER para um de seus itens (como, o item de WIA_CATEGORY_FILM).</span><span class="sxs-lookup"><span data-stu-id="6f739-496">It is possible for a driver to come with a segmentation filter, but still have WIA_IPS_SEGMENTATION set to WIA_DONT_USE_SEGMENTATION_FILTER for one of its items (such as, the WIA_CATEGORY_FILM item).</span></span> <span data-ttu-id="6f739-497">Esse pode ser o caso se o verificador usar quadros fixos para verificação de filmes, mas não para verificação regular de itens de WIA_CATEGORY_FLATBED.</span><span class="sxs-lookup"><span data-stu-id="6f739-497">This could be the case if the scanner uses fixed frames for film scanning, but not for regular scanning from WIA_CATEGORY_FLATBED items.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <span data-ttu-id="6f739-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-499">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-499">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-500">Contém o registro, o alinhamento e a detecção de borda para documentos que são colocados na mesa.</span><span class="sxs-lookup"><span data-stu-id="6f739-500">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="6f739-501">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-501">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="6f739-502">Essa propriedade indica como a planilha é posicionada horizontalmente no início da verificação de um scanner de mão ou alimentado por folha.</span><span class="sxs-lookup"><span data-stu-id="6f739-502">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="6f739-503">A propriedade é usada para prever onde o documento é colocado na cabeça de verificação.</span><span class="sxs-lookup"><span data-stu-id="6f739-503">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="6f739-504">Para os scanners que dão suporte a mais de um cabeçalho de verificação, essa propriedade é relativa ao início da verificação mais alta.</span><span class="sxs-lookup"><span data-stu-id="6f739-504">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="6f739-505">Essa propriedade é obrigatória para scanners de mão, alimentados por folhas e alimentados por folha.</span><span class="sxs-lookup"><span data-stu-id="6f739-505">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="6f739-506">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-506">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6f739-507">A tabela a seguir tem as três constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-507">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-508">Constante</span><span class="sxs-lookup"><span data-stu-id="6f739-508">Constant</span></span></th>
<th><span data-ttu-id="6f739-509">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-509">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-510">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="6f739-510">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="6f739-511">A planilha está posicionada à esquerda em relação ao cabeçalho de verificação.</span><span class="sxs-lookup"><span data-stu-id="6f739-511">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-512">CENTRA</span><span class="sxs-lookup"><span data-stu-id="6f739-512">CENTERED</span></span></td>
<td><span data-ttu-id="6f739-513">A planilha está centralizada no cabeçalho de verificação.</span><span class="sxs-lookup"><span data-stu-id="6f739-513">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f739-514">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="6f739-514">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="6f739-515">A planilha está posicionada à direita em relação ao cabeçalho de verificação.</span><span class="sxs-lookup"><span data-stu-id="6f739-515">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <span data-ttu-id="6f739-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-517">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-517">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-518">Indica se um item precisa de um controle de visualização exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6f739-518">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="6f739-519">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-519">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-520">Opcional para todos os itens habilitados para transferência.</span><span class="sxs-lookup"><span data-stu-id="6f739-520">Optional for all transfer enabled items.</span></span> <span data-ttu-id="6f739-521">Normalmente, isso é apenas itens das categorias WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e WIA_CATEGORY_FINISHED_FILE.</span><span class="sxs-lookup"><span data-stu-id="6f739-521">This is usually just items of the categories WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM, and WIA_CATEGORY_FINISHED_FILE.</span></span></p>
<p><span data-ttu-id="6f739-522">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-522">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6f739-523">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-523">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f739-524">Constante</span><span class="sxs-lookup"><span data-stu-id="6f739-524">Constant</span></span></th>
<th><span data-ttu-id="6f739-525">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f739-525">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f739-526">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="6f739-526">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="6f739-527">Mostrar um controle de visualização para o usuário, pois este dispositivo pode executar uma visualização.</span><span class="sxs-lookup"><span data-stu-id="6f739-527">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f739-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="6f739-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="6f739-529">Não mostrar um controle de visualização para o usuário, pois este dispositivo não pode executar uma visualização.</span><span class="sxs-lookup"><span data-stu-id="6f739-529">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <span data-ttu-id="6f739-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-531">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-531">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-532">Especifica se o aplicativo (ou os filtros) pode criar itens filho sob o item atual.</span><span class="sxs-lookup"><span data-stu-id="6f739-532">Specifies whether the application (or the filters) can create child items under the current item.</span></span></p>
<p><span data-ttu-id="6f739-533">Opcional para todas as categorias de item habilitado para transferência: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e até mesmo WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-533">Optional for all transfer enabled item categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM and even WIA_CATEGORY_FOLDER.</span></span> <span data-ttu-id="6f739-534">(Se o armazenamento não oferecer suporte ao carregamento de novos itens, essa propriedade não deverá ser suportada ou ter suporte com o valor <strong>falso</strong> .)</span><span class="sxs-lookup"><span data-stu-id="6f739-534">(If the storage won't support upload of new items then this property should be either unsupported or supported with the <strong>FALSE</strong> value.)</span></span></p>
<p><span data-ttu-id="6f739-535">Os itens que dão suporte a WIA_IPS_SEGMENTATION e WIA_USE_SEGMENTATION_FILTER também devem oferecer suporte a WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION e ter definido como <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f739-535">Items supporting WIA_IPS_SEGMENTATION and WIA_USE_SEGMENTATION_FILTER must also support WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION and have it set to <strong>TRUE</strong>.</span></span></p>
<p><span data-ttu-id="6f739-536">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <strong>true</strong> e <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="6f739-536">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <strong>TRUE</strong> and <strong>FALSE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <span data-ttu-id="6f739-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-538">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-538">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-539">Especifica o valor de escala de cinza que determina se um pixel será convertido em branco ou preto quando uma imagem for convertida em monodesvio.</span><span class="sxs-lookup"><span data-stu-id="6f739-539">Specifies the grayscale value that determines whether a pixel will be converted to white or black when an image is converted to monochromatic.</span></span> <span data-ttu-id="6f739-540">Os pixels acima do limite se tornam brancos.</span><span class="sxs-lookup"><span data-stu-id="6f739-540">Pixels above the threshold become white.</span></span> <span data-ttu-id="6f739-541">Os pixels abaixo do limite se tornam brancos.</span><span class="sxs-lookup"><span data-stu-id="6f739-541">Pixels below the threshold become white.</span></span></p>
<p><span data-ttu-id="6f739-542">Essa propriedade é necessária para itens de aquisição que dão suporte a verificações de 1-bpp e que têm a propriedade WIA_IPA_DATATYPE definida como WIA_DATA_THRESHOLD.</span><span class="sxs-lookup"><span data-stu-id="6f739-542">This property is required for acquisition items that support 1-bpp scans and that have the WIA_IPA_DATATYPE property set to WIA_DATA_THRESHOLD.</span></span></p>
<p><span data-ttu-id="6f739-543">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-543">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <span data-ttu-id="6f739-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-545">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-545">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-546">Especifica se o driver é capaz de transferir vários itens filho em uma única chamada de transferência.</span><span class="sxs-lookup"><span data-stu-id="6f739-546">Specifies whether the driver is capable of transferring multiple child items in single transfer call.</span></span></p>
<p><span data-ttu-id="6f739-547">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="6f739-547">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="6f739-548">O único valor possível para essa propriedade é WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span><span class="sxs-lookup"><span data-stu-id="6f739-548">The only possible value for this property is WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span></span> <span data-ttu-id="6f739-549">Se esse sinalizador for definido, o driver será capaz de transferir vários itens filho em uma única chamada de transferência.</span><span class="sxs-lookup"><span data-stu-id="6f739-549">If this flag is set, then the driver is capable of transfering multiple child items in single transfer call.</span></span> <span data-ttu-id="6f739-550">Se o sinalizador não estiver definido, o serviço WIA examinará os itens filho recursivamente e, em seguida, transferirá cada um desses itens.</span><span class="sxs-lookup"><span data-stu-id="6f739-550">If the flag is not set, the WIA Service will walk through the child items recursively and then transfer each of those items.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="6f739-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-552">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-552">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-553">Especifica o número de bytes a serem carregados para o item.</span><span class="sxs-lookup"><span data-stu-id="6f739-553">Specifies the number of bytes to upload for the item.</span></span></p>
<p><span data-ttu-id="6f739-554">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-554">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <span data-ttu-id="6f739-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-556">Especifica o tempo máximo de aquecimento, em milissegundos, que o dispositivo precisa antes de iniciar a operação de verificação.</span><span class="sxs-lookup"><span data-stu-id="6f739-556">Specifies the maximum warm-up time, in milliseconds, that the device needs before starting the scanning operation.</span></span> <span data-ttu-id="6f739-557">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-557">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-558">Um aplicativo pode ler essa propriedade para determinar o tempo máximo de aquecimento para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-558">An application can read this property to determine the maximum warm-up time for this device.</span></span> <span data-ttu-id="6f739-559">Em seguida, ele pode apresentar uma &quot; caixa de diálogo aguardando &quot; que o dispositivo fique quente, para permitir que o usuário saiba que uma espera ou pausa pode ocorrer antes de qualquer coisa acontecer.</span><span class="sxs-lookup"><span data-stu-id="6f739-559">It can then present a &quot;waiting for the device to warm up&quot; dialog box, to let the user know that a wait or pause might occur before anything happens.</span></span></p>
<p><span data-ttu-id="6f739-560">Esta propriedade é necessária para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-560">This property is required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-561">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <span data-ttu-id="6f739-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-563">Contém a largura atual, em pixels, da imagem selecionada a ser adquirida.</span><span class="sxs-lookup"><span data-stu-id="6f739-563">Contains the current width, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="6f739-564">Um aplicativo define essa propriedade para marcar a largura de uma área de seleção a ser adquirida.</span><span class="sxs-lookup"><span data-stu-id="6f739-564">An application sets this property to mark the width of a selection area to acquire.</span></span> <span data-ttu-id="6f739-565">Essa propriedade deve concordar com a propriedade <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6f739-565">This property must agree with the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="6f739-566">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-566">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-567">Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-567">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-568">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-568">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <span data-ttu-id="6f739-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-570">Contém a coordenada x, em pixels, do canto superior esquerdo da imagem selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f739-570">Contains the x coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="6f739-571">Um aplicativo define essa propriedade para marcar o canto superior esquerdo da área de seleção.</span><span class="sxs-lookup"><span data-stu-id="6f739-571">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="6f739-572">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-572">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-573">Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-573">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="6f739-574">Não há suporte para itens de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-574">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="6f739-575">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-575">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <span data-ttu-id="6f739-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-577">Contém a resolução horizontal atual, em pixels por polegada, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-577">Contains the current horizontal resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="6f739-578">Um aplicativo define essa propriedade para definir a resolução horizontal.</span><span class="sxs-lookup"><span data-stu-id="6f739-578">An application sets this property to set the horizontal resolution.</span></span> <span data-ttu-id="6f739-579">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-579">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-580">Se o dispositivo puder ser definido como apenas um único valor, crie um <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo e coloque o valor válido nele.</span><span class="sxs-lookup"><span data-stu-id="6f739-580">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="6f739-581">Esse também é um caso em que uma configuração de resolução depende de outra resolução.</span><span class="sxs-lookup"><span data-stu-id="6f739-581">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="6f739-582">(A resolução vertical pode depender da resolução horizontal.)</span><span class="sxs-lookup"><span data-stu-id="6f739-582">(The vertical resolution can depend on the horizontal resolution.)</span></span></p>
<p><span data-ttu-id="6f739-583">Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-583">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="6f739-584">Não há suporte para itens de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-584">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="6f739-585">Tipo: <strong>VT_I4</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="6f739-585">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <span data-ttu-id="6f739-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-587">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-587">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-588">Define o dimensionamento horizontal, como uma porcentagem, que pode ser aplicada a imagens digitalizadas dentro do dispositivo de scanner ou de seu driver.</span><span class="sxs-lookup"><span data-stu-id="6f739-588">Sets the horizontal scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="6f739-589">Essa propriedade é opcional para todos os itens habilitados para aquisição; ou seja, os itens dos tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-589">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-590">Tipo: <strong>VT_I4</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="6f739-590">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="6f739-591">Os valores podem ser de 1 a máximo VT_I4 (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="6f739-591">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="6f739-592">Por exemplo, 100 significa que não há dimensionamento, 050 significa escalar verticalmente para 50% do tamanho do original e 200 significa escalar verticalmente até 200% do tamanho original.</span><span class="sxs-lookup"><span data-stu-id="6f739-592">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <span data-ttu-id="6f739-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-594">Contém a altura atual, em pixels, da imagem selecionada a ser adquirida.</span><span class="sxs-lookup"><span data-stu-id="6f739-594">Contains the current height, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="6f739-595">Um aplicativo define essa propriedade para marcar a altura de uma área de seleção.</span><span class="sxs-lookup"><span data-stu-id="6f739-595">An application sets this property to mark the height of a selection area.</span></span> <span data-ttu-id="6f739-596">Essa propriedade deve ser aceita com o valor da propriedade <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6f739-596">This property must be agree with the value of the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="6f739-597">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-597">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-598">Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-598">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-599">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-599">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <span data-ttu-id="6f739-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-601">Coordenada y atual, em pixels, do canto superior esquerdo da imagem selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f739-601">Current y coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="6f739-602">Um aplicativo define essa propriedade para marcar o canto superior esquerdo da área de seleção.</span><span class="sxs-lookup"><span data-stu-id="6f739-602">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="6f739-603">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-603">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-604">Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-604">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="6f739-605">Não há suporte para itens de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-605">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="6f739-606">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="6f739-606">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <span data-ttu-id="6f739-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6f739-608">Contém a resolução vertical atual, em pixels por polegada, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f739-608">Contains the current vertical resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="6f739-609">Um aplicativo define essa propriedade para definir a resolução vertical.</span><span class="sxs-lookup"><span data-stu-id="6f739-609">An application sets this property to set the vertical resolution.</span></span> <span data-ttu-id="6f739-610">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f739-610">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6f739-611">Se o dispositivo puder ser definido como apenas um único valor, crie um <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo e coloque o valor válido nele.</span><span class="sxs-lookup"><span data-stu-id="6f739-611">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="6f739-612">Esse também é um caso em que uma configuração de resolução depende de outra resolução.</span><span class="sxs-lookup"><span data-stu-id="6f739-612">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="6f739-613">(A resolução horizontal pode depender da resolução vertical.)</span><span class="sxs-lookup"><span data-stu-id="6f739-613">(The horizontal resolution can depend on the vertical resolution.)</span></span></p>
<p><span data-ttu-id="6f739-614">Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-614">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="6f739-615">Não há suporte para itens de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="6f739-615">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="6f739-616">Tipo: <strong>VT_I4</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="6f739-616">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <span data-ttu-id="6f739-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="6f739-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6f739-618">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6f739-618">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="6f739-619">Define o dimensionamento vertical, como um percentual, que pode ser aplicado a imagens digitalizadas dentro do dispositivo de scanner ou de seu driver.</span><span class="sxs-lookup"><span data-stu-id="6f739-619">Sets the vertical scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="6f739-620">Essa propriedade é opcional para todos os itens habilitados para aquisição; ou seja, os itens dos tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="6f739-620">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="6f739-621">Tipo: <strong>VT_I4</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="6f739-621">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="6f739-622">Os valores podem ser de 1 a máximo VT_I4 (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="6f739-622">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="6f739-623">Por exemplo, 100 significa que não há dimensionamento, 050 significa escalar verticalmente para 50% do tamanho do original e 200 significa escalar verticalmente até 200% do tamanho original.</span><span class="sxs-lookup"><span data-stu-id="6f739-623">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="6f739-624">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f739-624">Requirements</span></span>



| <span data-ttu-id="6f739-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f739-625">Requirement</span></span> | <span data-ttu-id="6f739-626">Valor</span><span class="sxs-lookup"><span data-stu-id="6f739-626">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6f739-627">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f739-627">Minimum supported client</span></span><br/> | <span data-ttu-id="6f739-628">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6f739-628">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6f739-629">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f739-629">Minimum supported server</span></span><br/> | <span data-ttu-id="6f739-630">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6f739-630">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6f739-631">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f739-631">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f739-632"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f739-632"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




