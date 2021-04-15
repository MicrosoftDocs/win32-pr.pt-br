---
description: Os dispositivos de hardware da aquisição de imagens do Windows (WIA) têm valores de propriedade que são armazenados no registro do Windows. Para obter mais informações, consulte constantes de propriedade de dispositivo comum.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Constantes da Propriedade do dispositivo Camera (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461140"
---
# <a name="camera-device-property-constants"></a><span data-ttu-id="10779-104">Constantes de Propriedade do dispositivo Camera</span><span class="sxs-lookup"><span data-stu-id="10779-104">Camera Device Property Constants</span></span>

<span data-ttu-id="10779-105">Os dispositivos de hardware da aquisição de imagens do Windows (WIA) têm valores de propriedade que são armazenados no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="10779-105">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="10779-106">Para obter mais informações, consulte [**constantes de propriedade de dispositivo comum**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="10779-106">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span>

<span data-ttu-id="10779-107">As seguintes constantes de propriedade de dispositivo, com suas cadeias de caracteres associadas, são específicas para câmeras digitais.</span><span class="sxs-lookup"><span data-stu-id="10779-107">The following device property constants, with their associated strings, are specific to digital cameras.</span></span> <span data-ttu-id="10779-108">O prefix "WIA \_ DPC \_ " indica uma propriedade de dispositivo para câmeras e é a Convenção de nomenclatura usada em C/C++.</span><span class="sxs-lookup"><span data-stu-id="10779-108">The prefix "WIA\_DPC\_" indicates a Device Property for Cameras and is the naming convention used in C/C++.</span></span> <span data-ttu-id="10779-109">Para fins de script, essas constantes usam o prefixo "CameraDevice" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="10779-109">For scripting purposes these constants use the prefix "CameraDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="10779-110">O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="10779-110">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="10779-111">O WIA não oferece suporte a câmeras no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="10779-111">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="10779-112">Para essas versões do Windows, use a API do dispositivo portátil do Windows (WPD) descrita no kit de desenvolvimento de driver do Windows (DDK) para adquirir imagens de câmeras.</span><span class="sxs-lookup"><span data-stu-id="10779-112">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="10779-113">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="10779-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="10779-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <span data-ttu-id="10779-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="10779-116">O número de imagens que a câmera levou.</span><span class="sxs-lookup"><span data-stu-id="10779-116">The number of pictures that the camera has taken.</span></span> <span data-ttu-id="10779-117">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-117">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="10779-118">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-118">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <span data-ttu-id="10779-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="10779-120">O número de imagens que podem ser executadas, dadas as configurações de propriedade atuais.</span><span class="sxs-lookup"><span data-stu-id="10779-120">The number of pictures that can be taken, given the current property settings.</span></span> <span data-ttu-id="10779-121">Se essas configurações forem alteradas e as alterações afetarem o tamanho das imagens que o dispositivo de câmera produz, o minidriver WIA deverá atualizar o número de imagens restantes.</span><span class="sxs-lookup"><span data-stu-id="10779-121">If these settings change, and the changes affect the size of the images that the camera device produces, the WIA minidriver should update the number of remaining pictures.</span></span> <span data-ttu-id="10779-122">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-122">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="10779-123">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-123">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <span data-ttu-id="10779-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="10779-125">Indica o modo de exposição atual da câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-125">Indicates the camera's current exposure mode.</span></span> <span data-ttu-id="10779-126">Um aplicativo altera essa propriedade para controlar o modo de exposição do dispositivo de câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-126">An application changes this property to control the exposure mode of the camera device.</span></span><br/> <span data-ttu-id="10779-127">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-127">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="10779-128">A tabela a seguir tem as sete constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-128">The following table has the seven constants that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-129">Modo de exposição</span><span class="sxs-lookup"><span data-stu-id="10779-129">Exposure Mode</span></span></th>
<th><span data-ttu-id="10779-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-131">EXPOSUREMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="10779-131">EXPOSUREMODE_MANUAL</span></span></td>
<td><span data-ttu-id="10779-132">A velocidade do obturador e a abertura são definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="10779-132">The shutter speed and aperture are set by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-133">EXPOSUREMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="10779-133">EXPOSUREMODE_AUTO</span></span></td>
<td><span data-ttu-id="10779-134">A velocidade e a abertura do obturador são definidas automaticamente pela câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-134">The shutter speed and aperture are automatically set by the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-135">EXPOSUREMODE_APERTURE_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="10779-135">EXPOSUREMODE_APERTURE_PRIORITY</span></span></td>
<td><span data-ttu-id="10779-136">A abertura é definida pelo usuário e a câmera define automaticamente a velocidade do obturador.</span><span class="sxs-lookup"><span data-stu-id="10779-136">The aperture is set by the user, and the camera automatically sets the shutter speed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-137">EXPOSUREMODE_SHUTTER_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="10779-137">EXPOSUREMODE_SHUTTER_PRIORITY</span></span></td>
<td><span data-ttu-id="10779-138">A velocidade do obturador é definida pelo usuário e a câmera define automaticamente a abertura.</span><span class="sxs-lookup"><span data-stu-id="10779-138">The shutter speed is set by the user, and the camera automatically sets the aperture.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-139">EXPOSUREMODE_PROGRAM_CREATIVE</span><span class="sxs-lookup"><span data-stu-id="10779-139">EXPOSUREMODE_PROGRAM_CREATIVE</span></span></td>
<td><span data-ttu-id="10779-140">A velocidade e a abertura do obturador são automaticamente definidas pela câmera, otimizadas para o assunto ainda.</span><span class="sxs-lookup"><span data-stu-id="10779-140">The shutter speed and aperture are automatically set by the camera, optimized for still subject matter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-141">EXPOSUREMODE_PROGRAM_ACTION</span><span class="sxs-lookup"><span data-stu-id="10779-141">EXPOSUREMODE_PROGRAM_ACTION</span></span></td>
<td><span data-ttu-id="10779-142">A velocidade e a abertura do obturador são automaticamente definidas pela câmera, otimizadas para cenas que contêm movimentos rápidos.</span><span class="sxs-lookup"><span data-stu-id="10779-142">The shutter speed and aperture are automatically set by the camera, optimized for scenes containing fast motion.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-143">EXPOSUREMODE_PORTRAIT</span><span class="sxs-lookup"><span data-stu-id="10779-143">EXPOSUREMODE_PORTRAIT</span></span></td>
<td><span data-ttu-id="10779-144">A velocidade e a abertura do obturador são automaticamente definidas pela câmera, otimizadas para fotografias em retrato.</span><span class="sxs-lookup"><span data-stu-id="10779-144">The shutter speed and aperture are automatically set by the camera, optimized for portrait photography.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <span data-ttu-id="10779-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-146">Permite o ajuste do ponto definido do controle de exposição automática da câmera digital.</span><span class="sxs-lookup"><span data-stu-id="10779-146">Allows for the adjustment of the set point of the digital camera's auto-exposure control.</span></span> <span data-ttu-id="10779-147">Por exemplo, uma configuração de zero não altera o nível de exposição automática de conjunto de fábrica.</span><span class="sxs-lookup"><span data-stu-id="10779-147">For example, a setting of zero does not change the factory-set auto-exposure level.</span></span> <span data-ttu-id="10779-148">As unidades estão em &quot; interrupções &quot; que são dimensionadas por um fator de 1000, para permitir valores de parada fracionais.</span><span class="sxs-lookup"><span data-stu-id="10779-148">The units are in &quot;stops&quot; that are scaled by a factor of 1000, to allow for fractional stop values.</span></span> <span data-ttu-id="10779-149">Uma configuração de 2000 corresponde a duas para mais exposição (quatro vezes mais energia no sensor), produzindo imagens mais brilhantes.</span><span class="sxs-lookup"><span data-stu-id="10779-149">A setting of 2000 corresponds to two stops more exposure (four times more energy on the sensor), yielding brighter images.</span></span> <span data-ttu-id="10779-150">Uma configuração de-1000 corresponde a uma parada menos exposição (uma metade da energia no sensor) que gera imagens mais escuras.</span><span class="sxs-lookup"><span data-stu-id="10779-150">A setting of -1000 corresponds to one stop less exposure (one-half the energy on the sensor) yielding darker images.</span></span> <span data-ttu-id="10779-151">Os valores de configuração estão no sistema aditivo de unidades de exposição fotográfica (APEX).</span><span class="sxs-lookup"><span data-stu-id="10779-151">The setting values are in Additive System of Photographic Exposure (APEX) units.</span></span> <span data-ttu-id="10779-152">Essa propriedade pode ser expressa como uma lista ou um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="10779-152">This property may be expressed as either a list or a range of values.</span></span> <span data-ttu-id="10779-153">Essa propriedade normalmente é usada somente quando o dispositivo tem a propriedade <strong>WIA_DPC_EXPOSURE_MODE</strong> definida como EXPOSUREMODE_MANUAL.</span><span class="sxs-lookup"><span data-stu-id="10779-153">This property is typically used only when the device has the <strong>WIA_DPC_EXPOSURE_MODE</strong> property set to EXPOSUREMODE_MANUAL.</span></span></p>
<p><span data-ttu-id="10779-154">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="10779-154">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <span data-ttu-id="10779-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-156">Corresponde à velocidade do obturador, em segundos, dimensionada por 10.000.</span><span class="sxs-lookup"><span data-stu-id="10779-156">Corresponds to the shutter speed, in seconds that are scaled by 10,000.</span></span> <span data-ttu-id="10779-157">Normalmente, o dispositivo usa essa propriedade somente quando a propriedade <strong>WIA_DPC_EXPOSURE_MODE</strong> é definida como EXPOSUREMODE_MANUAL ou EXPOSUREMODE_SHUTTER_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="10779-157">Typically, the device uses this property only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_SHUTTER_PRIORITY.</span></span></p>
<p><span data-ttu-id="10779-158">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="10779-158">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <span data-ttu-id="10779-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-160">Corresponde à abertura da lente, em unidades do número f-stop dimensionado por 100.</span><span class="sxs-lookup"><span data-stu-id="10779-160">Corresponds to the aperture of the lens, in units of the f-stop number scaled by 100.</span></span> <span data-ttu-id="10779-161">A configuração dessa propriedade normalmente é válida somente quando a propriedade <strong>WIA_DPC_EXPOSURE_MODE</strong> é definida como EXPOSUREMODE_MANUAL ou EXPOSUREMODE_APERTURE_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="10779-161">The setting of this property is typically valid only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_APERTURE_PRIORITY.</span></span></p>
<p><span data-ttu-id="10779-162">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-162">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <span data-ttu-id="10779-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-164">Define a configuração do modo flash atual para o dispositivo de câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-164">Defines the current flash mode setting for the camera device.</span></span> <span data-ttu-id="10779-165">O driver de dispositivo enumera os valores com suporte dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-165">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="10779-166">Um aplicativo grava essa propriedade para definir o modo flash para o dispositivo de câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-166">An application writes this property to set the flash mode for the camera device.</span></span></p>
<p><span data-ttu-id="10779-167">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-167">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="10779-168">A tabela a seguir tem as seis constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-168">The following table has the six constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-169">Modo flash</span><span class="sxs-lookup"><span data-stu-id="10779-169">Flash Mode</span></span></th>
<th><span data-ttu-id="10779-170">Definição</span><span class="sxs-lookup"><span data-stu-id="10779-170">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-171">FLASHMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="10779-171">FLASHMODE_AUTO</span></span></td>
<td><span data-ttu-id="10779-172">O dispositivo de câmera determina as configurações corretas do flash.</span><span class="sxs-lookup"><span data-stu-id="10779-172">The camera device determines the proper flash settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-173">FLASHMODE_FILL</span><span class="sxs-lookup"><span data-stu-id="10779-173">FLASHMODE_FILL</span></span></td>
<td><span data-ttu-id="10779-174">O dispositivo de câmera está configurado para ser atualizado independentemente das condições de iluminação atuais.</span><span class="sxs-lookup"><span data-stu-id="10779-174">The camera device is configured to flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-175">FLASHMODE_OFF</span><span class="sxs-lookup"><span data-stu-id="10779-175">FLASHMODE_OFF</span></span></td>
<td><span data-ttu-id="10779-176">O dispositivo de câmera está configurado para <em>não</em> piscar para qualquer imagem tirada.</span><span class="sxs-lookup"><span data-stu-id="10779-176">The camera device is configured <em>not</em> to flash for any picture taken.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-177">FLASHMODE_REDEYE_AUTO</span><span class="sxs-lookup"><span data-stu-id="10779-177">FLASHMODE_REDEYE_AUTO</span></span></td>
<td><span data-ttu-id="10779-178">O dispositivo de câmera determina as configurações do flash apropriadas usando a redução de olhos vermelhos, independentemente das condições de iluminação atuais.</span><span class="sxs-lookup"><span data-stu-id="10779-178">The camera device determines the proper flash settings using red-eye reduction, regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-179">FLASHMODE_REDEYE_FILL</span><span class="sxs-lookup"><span data-stu-id="10779-179">FLASHMODE_REDEYE_FILL</span></span></td>
<td><span data-ttu-id="10779-180">O dispositivo de câmera está configurado para usar a redução de olhos vermelhos e o flash, independentemente das condições de iluminação atuais.</span><span class="sxs-lookup"><span data-stu-id="10779-180">The camera device is configured to use red-eye reduction and flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-181">FLASHMODE_EXTERNALSYNC</span><span class="sxs-lookup"><span data-stu-id="10779-181">FLASHMODE_EXTERNALSYNC</span></span></td>
<td><span data-ttu-id="10779-182">O dispositivo de câmera está configurado para sincronizar com unidades flash externas.</span><span class="sxs-lookup"><span data-stu-id="10779-182">The camera device is configured to synchronize with external flash units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <span data-ttu-id="10779-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-184">Define a configuração do modo de foco atual para o dispositivo de câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-184">Defines the current focus mode setting for the camera device.</span></span> <span data-ttu-id="10779-185">O driver de dispositivo enumera os valores com suporte dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-185">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="10779-186">Um aplicativo grava essa propriedade para definir o modo de foco para o dispositivo de câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-186">An application writes this property to set the focus mode for the camera device.</span></span></p>
<p><span data-ttu-id="10779-187">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-187">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="10779-188">A tabela a seguir tem as três constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-188">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-189">Modo de foco</span><span class="sxs-lookup"><span data-stu-id="10779-189">Focus Mode</span></span></th>
<th><span data-ttu-id="10779-190">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-191">FOCUSMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="10779-191">FOCUSMODE_MANUAL</span></span></td>
<td><span data-ttu-id="10779-192">O dispositivo de câmera está configurado para permitir que o usuário se concentre manualmente.</span><span class="sxs-lookup"><span data-stu-id="10779-192">The camera device is configured to allow the user to focus manually.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-193">FOCUSMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="10779-193">FOCUSMODE_AUTO</span></span></td>
<td><span data-ttu-id="10779-194">O dispositivo de câmera está configurado para se concentrar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="10779-194">The camera device is configured to focus automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-195">FOCUSMODE_MACROAUTO</span><span class="sxs-lookup"><span data-stu-id="10779-195">FOCUSMODE_MACROAUTO</span></span></td>
<td><span data-ttu-id="10779-196">O dispositivo de câmera está configurado para se concentrar automaticamente usando configurações de macro de curto alcance.</span><span class="sxs-lookup"><span data-stu-id="10779-196">The camera device is configured to focus automatically using short-range macro settings.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <span data-ttu-id="10779-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="10779-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-198">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="10779-198">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="10779-199">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-199">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <span data-ttu-id="10779-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="10779-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-201">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="10779-201">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="10779-202">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-202">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <span data-ttu-id="10779-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-204">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="10779-204">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="10779-205">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <span data-ttu-id="10779-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-207">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="10779-207">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="10779-208">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-208">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <span data-ttu-id="10779-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-210">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="10779-210">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="10779-211">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-211">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <span data-ttu-id="10779-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-213">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="10779-213">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="10779-214">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-214">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <span data-ttu-id="10779-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-216">Define a fonte de energia atual para o dispositivo de câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-216">Defines the current power source for the camera device.</span></span> <span data-ttu-id="10779-217">Um aplicativo lê essa propriedade para determinar qual fonte de energia a câmera está usando.</span><span class="sxs-lookup"><span data-stu-id="10779-217">An application reads this property to determine what power source the camera is using.</span></span></p>
<p><span data-ttu-id="10779-218">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-218">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="10779-219">A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-219">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-220">Modo de energia</span><span class="sxs-lookup"><span data-stu-id="10779-220">Power Mode</span></span></th>
<th><span data-ttu-id="10779-221">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-222">POWERMODE_LINE</span><span class="sxs-lookup"><span data-stu-id="10779-222">POWERMODE_LINE</span></span></td>
<td><span data-ttu-id="10779-223">O dispositivo de câmera está operando em um adaptador de energia.</span><span class="sxs-lookup"><span data-stu-id="10779-223">The camera device is operating on a power adapter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-224">POWERMODE_BATTERY</span><span class="sxs-lookup"><span data-stu-id="10779-224">POWERMODE_BATTERY</span></span></td>
<td><span data-ttu-id="10779-225">O dispositivo de câmera está operando com energia da bateria.</span><span class="sxs-lookup"><span data-stu-id="10779-225">The camera device is operating on battery power.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <span data-ttu-id="10779-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-227">A porcentagem de energia da bateria que é deixada para operar o dispositivo de câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-227">The percentage of battery power that is left to operate the camera device.</span></span> <span data-ttu-id="10779-228">Esse valor deve ser um inteiro de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="10779-228">This value should be an integer from 0 through 100.</span></span> <span data-ttu-id="10779-229">Um aplicativo lê essa propriedade para determinar a duração da bateria restante do dispositivo de câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-229">An application reads this property to determine the remaining battery life of the camera device.</span></span></p>
<p><span data-ttu-id="10779-230">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-230">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <span data-ttu-id="10779-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-232">A largura, em pixels, de uma imagem em miniatura a ser usada para imagens recentemente capturadas.</span><span class="sxs-lookup"><span data-stu-id="10779-232">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="10779-233">Um aplicativo lê esse valor para obter um tamanho estimado para exibir miniaturas em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="10779-233">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="10779-234">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) ou somente leitura (WIA_PROP_NONE), valores válidos: WIA_PROP_LIST ou WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="10779-234">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <span data-ttu-id="10779-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-236">A largura, em pixels, de uma imagem em miniatura a ser usada para imagens recentemente capturadas.</span><span class="sxs-lookup"><span data-stu-id="10779-236">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="10779-237">Um aplicativo lê esse valor para obter um tamanho estimado para exibir miniaturas em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="10779-237">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="10779-238">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) ou somente leitura (WIA_PROP_NONE), valores válidos: WIA_PROP_LIST ou WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="10779-238">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <span data-ttu-id="10779-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-240">A largura em pixels a ser usada para imagens recentemente capturadas.</span><span class="sxs-lookup"><span data-stu-id="10779-240">The width in pixels to use for newly captured images.</span></span> <span data-ttu-id="10779-241">A lista de valores válidos para essa propriedade tem uma correspondência um-para-um com a lista de valores válidos para a propriedade <strong>WIA_DPC_PICT_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="10779-241">The list of valid values for this property has a one-to-one correspondence to the list of valid values for the <strong>WIA_DPC_PICT_HEIGHT</strong> property.</span></span> <span data-ttu-id="10779-242">Se a largura e a altura individuais forem linearmente configuradas e ortogonal umas às outras, elas poderão ser expressas como um intervalo.</span><span class="sxs-lookup"><span data-stu-id="10779-242">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="10779-243">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-243">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <span data-ttu-id="10779-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-245">A altura em pixels a ser usada para imagens recentemente capturadas.</span><span class="sxs-lookup"><span data-stu-id="10779-245">The height in pixels to use for newly captured images.</span></span> <span data-ttu-id="10779-246">A lista de valores válidos para essa propriedade tem uma correspondência um-para-um com a lista de valores válidos para a propriedade <strong>WIA_DPC_PICT_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="10779-246">The list of valid values for this property has a one-to-one correspondence with the list of valid values for the <strong>WIA_DPC_PICT_WIDTH</strong> property.</span></span> <span data-ttu-id="10779-247">Se a largura e a altura individuais forem linearmente configuradas e ortogonal umas às outras, elas poderão ser expressas como um intervalo.</span><span class="sxs-lookup"><span data-stu-id="10779-247">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="10779-248">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-248">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <span data-ttu-id="10779-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="10779-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-250">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="10779-250">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="10779-251">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-251">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <span data-ttu-id="10779-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-253">Deve ser aproximadamente linear em relação à qualidade de imagem percebida em uma ampla gama de conteúdo de cena e contém um intervalo ou uma lista de inteiros.</span><span class="sxs-lookup"><span data-stu-id="10779-253">Intended to be approximately linear with respect to perceived image quality over a broad range of scene content, and it contains either a range or a list of integers.</span></span> <span data-ttu-id="10779-254">Inteiros menores são usados para representar a menor qualidade (ou seja, compactação máxima), enquanto inteiros maiores são usados para representar uma qualidade maior (ou seja, compactação mínima).</span><span class="sxs-lookup"><span data-stu-id="10779-254">Smaller integers are used to represent lower quality (that is, maximum compression), whereas larger integers are used to represent higher quality (that is, minimum compression).</span></span> <span data-ttu-id="10779-255">Todas as configurações disponíveis em um dispositivo são relativas somente a esse dispositivo e, portanto, são específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10779-255">Any available settings on a device are relative only to that device and are therefore device specific.</span></span></p>
<p><span data-ttu-id="10779-256">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-256">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <span data-ttu-id="10779-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="10779-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-258">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="10779-258">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="10779-259">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-259">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <span data-ttu-id="10779-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-261">O tempo, em milissegundos, entre capturas de imagem em uma operação de captura de lapso de tempo.</span><span class="sxs-lookup"><span data-stu-id="10779-261">The time, in milliseconds, between image captures in a time-lapse capture operation.</span></span></p>
<p><span data-ttu-id="10779-262">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-262">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <span data-ttu-id="10779-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-264">O número de imagens que o dispositivo tenta capturar durante uma captura de lapso de tempo.</span><span class="sxs-lookup"><span data-stu-id="10779-264">The number of images the device attempts to capture during a time-lapse capture.</span></span></p>
<p><span data-ttu-id="10779-265">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-265">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <span data-ttu-id="10779-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-267">O tempo, em milissegundos, entre capturas de imagem durante uma operação de intermitência.</span><span class="sxs-lookup"><span data-stu-id="10779-267">The time, in milliseconds, between image captures during a burst operation.</span></span></p>
<p><span data-ttu-id="10779-268">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-268">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <span data-ttu-id="10779-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-270">O número de imagens que o dispositivo tenta capturar durante uma operação de intermitência.</span><span class="sxs-lookup"><span data-stu-id="10779-270">The number of images the device attempts to capture during a burst operation.</span></span></p>
<p><span data-ttu-id="10779-271">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-271">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <span data-ttu-id="10779-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-273">Especifica o modo de aquisição de imagem especial da câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-273">Specifies the special image acquisition mode of the camera.</span></span></p>
<p><span data-ttu-id="10779-274">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-274">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="10779-275">A tabela a seguir tem as três constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-275">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-276">Modo de efeito</span><span class="sxs-lookup"><span data-stu-id="10779-276">Effect Mode</span></span></th>
<th><span data-ttu-id="10779-277">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-277">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-278">EFFECTMODE_STANDARD</span><span class="sxs-lookup"><span data-stu-id="10779-278">EFFECTMODE_STANDARD</span></span></td>
<td><span data-ttu-id="10779-279">Capture uma imagem no modo padrão da câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-279">Capture an image in the standard mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-280">EFFECTMODE_BW</span><span class="sxs-lookup"><span data-stu-id="10779-280">EFFECTMODE_BW</span></span></td>
<td><span data-ttu-id="10779-281">Capturar uma imagem em escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="10779-281">Capture a grayscale image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-282">EFFECTMODE_SEPIA</span><span class="sxs-lookup"><span data-stu-id="10779-282">EFFECTMODE_SEPIA</span></span></td>
<td><span data-ttu-id="10779-283">Capturar uma imagem de sépia.</span><span class="sxs-lookup"><span data-stu-id="10779-283">Capture a sepia image.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <span data-ttu-id="10779-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-285">A taxa de zoom efetiva da imagem adquirida da câmera digital, dimensionada por um fator de 10.</span><span class="sxs-lookup"><span data-stu-id="10779-285">The effective zoom ratio of the digital camera's acquired image, scaled by a factor of 10.</span></span> <span data-ttu-id="10779-286">Um valor de 10 corresponde à ausência de zoom digital (1X), que é o tamanho de cena padrão capturado pela câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-286">A value of 10 corresponds to the absence of digital zoom (1X), which is the standard scene size captured by the camera.</span></span> <span data-ttu-id="10779-287">Um valor de 20 corresponde a um zoom 2X, em que um quarto do tamanho da cena padrão é capturado pela câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-287">A value of 20 corresponds to a 2X zoom, where one-quarter of the standard scene size is captured by the camera.</span></span></p>
<p><span data-ttu-id="10779-288">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-288">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <span data-ttu-id="10779-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-290">A nitidez percebida de uma imagem capturada.</span><span class="sxs-lookup"><span data-stu-id="10779-290">The perceived sharpness of a captured image.</span></span> <span data-ttu-id="10779-291">Essa propriedade pode usar uma lista de valores ou um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="10779-291">This property can use either a list of values or a range of values.</span></span> <span data-ttu-id="10779-292">O valor mínimo representa a menor quantidade de nitidez, enquanto o valor máximo representa a nitidez máxima.</span><span class="sxs-lookup"><span data-stu-id="10779-292">The minimum value represents the least amount of sharpness, whereas the maximum value represents the maximum sharpness.</span></span> <span data-ttu-id="10779-293">Normalmente, um valor no meio do intervalo representa a nitidez normal, ou padrão.</span><span class="sxs-lookup"><span data-stu-id="10779-293">Typically a value in the middle of the range represents normal, or default, sharpness.</span></span></p>
<p><span data-ttu-id="10779-294">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-294">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <span data-ttu-id="10779-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-296">O contraste percebido de uma imagem capturada.</span><span class="sxs-lookup"><span data-stu-id="10779-296">The perceived contrast of a captured image.</span></span> <span data-ttu-id="10779-297">Essa propriedade pode conter uma lista de valores ou um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="10779-297">This property can contain either a list of values or a range of values.</span></span> <span data-ttu-id="10779-298">O valor mínimo com suporte representa a menor quantidade de contraste, enquanto o valor máximo representa o maior contraste.</span><span class="sxs-lookup"><span data-stu-id="10779-298">The minimum supported value represents the least amount of contrast, whereas the maximum value represents the most contrast.</span></span> <span data-ttu-id="10779-299">Normalmente, um valor no meio do intervalo representa normal, ou padrão, o contraste.</span><span class="sxs-lookup"><span data-stu-id="10779-299">Typically, a value in the middle of the range represents normal, or default, contrast.</span></span></p>
<p><span data-ttu-id="10779-300">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-300">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <span data-ttu-id="10779-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-302">Define o modo de captura de imagem.</span><span class="sxs-lookup"><span data-stu-id="10779-302">Sets the image capture mode.</span></span></p>
<p><span data-ttu-id="10779-303">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-303">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="10779-304">A tabela a seguir tem as três constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-304">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-305">Modo de captura</span><span class="sxs-lookup"><span data-stu-id="10779-305">Capture Mode</span></span></th>
<th><span data-ttu-id="10779-306">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-306">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-307">CAPTUREMODE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="10779-307">CAPTUREMODE_NORMAL</span></span></td>
<td><span data-ttu-id="10779-308">Modo normal para a câmera.</span><span class="sxs-lookup"><span data-stu-id="10779-308">Normal mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-309">CAPTUREMODE_BURST</span><span class="sxs-lookup"><span data-stu-id="10779-309">CAPTUREMODE_BURST</span></span></td>
<td><span data-ttu-id="10779-310">Capture mais de uma imagem em sucessão rápida, conforme definido pelos valores das propriedades <strong>WIA_DPC_BURST_NUMBER</strong> e <strong>WIA_DPC_BURST_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="10779-310">Capture more than one image in quick succession as defined by the values of the <strong>WIA_DPC_BURST_NUMBER</strong> and <strong>WIA_DPC_BURST_INTERVAL</strong> properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-311">CAPTUREMODE_TIMELAPSE</span><span class="sxs-lookup"><span data-stu-id="10779-311">CAPTUREMODE_TIMELAPSE</span></span></td>
<td><span data-ttu-id="10779-312">Capture mais de uma imagem sucessivamente, conforme definido pelas propriedades <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="10779-312">Capture more than one image in succession as defined by the <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> properties.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <span data-ttu-id="10779-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-314">O valor que representa a quantidade de tempo de atraso, em milissegundos, que deve ser inserido entre o gatilho de captura e a inicialização real da captura de dados.</span><span class="sxs-lookup"><span data-stu-id="10779-314">The value representing the amount of time delay, in milliseconds, that should be inserted between the capture trigger and the actual initiation of the data capture.</span></span> <span data-ttu-id="10779-315">Essa propriedade não deve ser usada para descrever o tempo entre os quadros para inicialização única, várias capturas como intermitência ou tempo decorrido, que têm propriedades de intervalo separadas <strong>WIA_DPC_BURST_INTERVAL</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="10779-315">This property is not intended to be used to describe the time between frames for single-initiation, multiple captures such as burst or time lapse, which have separate interval properties <strong>WIA_DPC_BURST_INTERVAL</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span></span> <span data-ttu-id="10779-316">Nesses casos, ele ainda funciona como um atraso inicial antes que a primeira imagem na série seja capturada, independentemente do tempo entre os quadros.</span><span class="sxs-lookup"><span data-stu-id="10779-316">In those cases, it still serves as an initial delay before the first image in the series is captured, independent of the time between frames.</span></span> <span data-ttu-id="10779-317">Para nenhum atraso de precaptura, essa propriedade deve ser definida como zero.</span><span class="sxs-lookup"><span data-stu-id="10779-317">For no precapture delay, this property should be set to zero.</span></span></p>
<p><span data-ttu-id="10779-318">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-318">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <span data-ttu-id="10779-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-320">Permite a emulação de configurações de velocidade de filme em uma câmera digital.</span><span class="sxs-lookup"><span data-stu-id="10779-320">Allows for the emulation of film speed settings on a digital camera.</span></span> <span data-ttu-id="10779-321">As configurações correspondem às designações ISO (ASA/DIN).</span><span class="sxs-lookup"><span data-stu-id="10779-321">The settings correspond to the ISO designations (ASA/DIN).</span></span> <span data-ttu-id="10779-322">Normalmente, um dispositivo dá suporte a valores enumerados discretos, mas o controle contínuo sobre um intervalo de valores é possível.</span><span class="sxs-lookup"><span data-stu-id="10779-322">Typically, a device supports discrete enumerated values, but continuous control over a range of values is possible.</span></span> <span data-ttu-id="10779-323">Um valor de 0xFFFF corresponde à configuração automática de ISO.</span><span class="sxs-lookup"><span data-stu-id="10779-323">A value of 0xFFFF corresponds to the Automatic ISO setting.</span></span></p>
<p><span data-ttu-id="10779-324">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-324">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <span data-ttu-id="10779-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-326">Especifica o modo que a câmera usa para ajustar automaticamente a configuração de exposição.</span><span class="sxs-lookup"><span data-stu-id="10779-326">Specifies the mode the camera uses to automatically adjust the exposure setting.</span></span></p>
<p><span data-ttu-id="10779-327">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-327">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-328">Modo de medição de exposição</span><span class="sxs-lookup"><span data-stu-id="10779-328">Exposure Metering Mode</span></span></th>
<th><span data-ttu-id="10779-329">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-330">EXPOSUREMETERING_AVERAGE</span><span class="sxs-lookup"><span data-stu-id="10779-330">EXPOSUREMETERING_AVERAGE</span></span></td>
<td><span data-ttu-id="10779-331">Defina a exposição com base em uma média da cena inteira.</span><span class="sxs-lookup"><span data-stu-id="10779-331">Set the exposure based on an average of the entire scene.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-332">EXPOSUREMETERING_CENTERWEIGHT</span><span class="sxs-lookup"><span data-stu-id="10779-332">EXPOSUREMETERING_CENTERWEIGHT</span></span></td>
<td><span data-ttu-id="10779-333">Defina a exposição com base em uma média ponderada no centro.</span><span class="sxs-lookup"><span data-stu-id="10779-333">Set the exposure based on a center-weighted average.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-334">EXPOSUREMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="10779-334">EXPOSUREMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="10779-335">Defina a exposição com base em um padrão multiespecial.</span><span class="sxs-lookup"><span data-stu-id="10779-335">Set the exposure based on a multispot pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-336">EXPOSUREMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="10779-336">EXPOSUREMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="10779-337">Defina a exposição com base em um ponto central.</span><span class="sxs-lookup"><span data-stu-id="10779-337">Set the exposure based on a center spot.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <span data-ttu-id="10779-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-339">Especifica o modo que a câmera usa para ajustar o foco automaticamente.</span><span class="sxs-lookup"><span data-stu-id="10779-339">Specifies the mode the camera uses to automatically adjust the focus.</span></span></p>
<p><span data-ttu-id="10779-340">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-340">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="10779-341">A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-341">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-342">Modo de medição de foco</span><span class="sxs-lookup"><span data-stu-id="10779-342">Focus Metering Mode</span></span></th>
<th><span data-ttu-id="10779-343">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-343">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-344">FOCUSMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="10779-344">FOCUSMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="10779-345">Ajuste o foco com base em um ponto central.</span><span class="sxs-lookup"><span data-stu-id="10779-345">Adjust the focus based on a center spot.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-346">FOCUSMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="10779-346">FOCUSMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="10779-347">Ajuste o foco com base em um padrão multiespecial.</span><span class="sxs-lookup"><span data-stu-id="10779-347">Adjust the focus based on a multispot pattern.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <span data-ttu-id="10779-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-349">A distância, em milímetros, entre o plano de captura de imagem da câmera digital e o ponto de foco.</span><span class="sxs-lookup"><span data-stu-id="10779-349">The distance, in millimeters, between the image-capturing plane of the digital camera and the point of focus.</span></span> <span data-ttu-id="10779-350">Um valor de 0xFFFF corresponde a uma configuração maior que 655 metros.</span><span class="sxs-lookup"><span data-stu-id="10779-350">A value of 0xFFFF corresponds to a setting greater than 655 meters.</span></span></p>
<p><span data-ttu-id="10779-351">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="10779-351">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <span data-ttu-id="10779-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-353">O comprimento focal 35mm-equivalente.</span><span class="sxs-lookup"><span data-stu-id="10779-353">The 35mm-equivalent focal length.</span></span> <span data-ttu-id="10779-354">Os valores dessa propriedade correspondem ao comprimento focal em milímetros multiplicado por 100.</span><span class="sxs-lookup"><span data-stu-id="10779-354">The values of this property correspond to the focal length in millimeters multiplied by 100.</span></span> <span data-ttu-id="10779-355">O comprimento focal determina o zoom óptico.</span><span class="sxs-lookup"><span data-stu-id="10779-355">The focal length determines the optical zoom.</span></span></p>
<p><span data-ttu-id="10779-356">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-356">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <span data-ttu-id="10779-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-358">Uma cadeia de caracteres Unicode terminada em nulo que representa o lucro vermelho, verde e azul aplicado aos dados da imagem, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="10779-358">A null-terminated Unicode string that represents the red, green, and blue gain applied to image data, respectively.</span></span> <span data-ttu-id="10779-359">Por exemplo, &quot; 4:25:50 &quot; representa um lucro vermelho de 4, um lucro verde de 25 e um lucro azul de 50.</span><span class="sxs-lookup"><span data-stu-id="10779-359">For example, &quot;4:25:50&quot; represents a red gain of 4, a green gain of 25, and a blue gain of 50.</span></span></p>
<p><span data-ttu-id="10779-360">Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-360">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <span data-ttu-id="10779-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-362">Especifica como a câmera digital pondera os canais de cor.</span><span class="sxs-lookup"><span data-stu-id="10779-362">Specifies how the digital camera weights color channels.</span></span></p>
<p><span data-ttu-id="10779-363">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="10779-363">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="10779-364">A seguir está uma lista de possíveis valores para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-364">The following is a list of possible values for this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10779-365">Balanço de branco</span><span class="sxs-lookup"><span data-stu-id="10779-365">White Balance</span></span></th>
<th><span data-ttu-id="10779-366">Descrição</span><span class="sxs-lookup"><span data-stu-id="10779-366">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10779-367">WHITEBALANCE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="10779-367">WHITEBALANCE_MANUAL</span></span></td>
<td><span data-ttu-id="10779-368">O equilíbrio de branco é definido diretamente usando a propriedade <strong>WIA_DPC_RGB_GAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="10779-368">The white balance is set directly using the <strong>WIA_DPC_RGB_GAIN</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-369">WHITEBALANCE_AUTO</span><span class="sxs-lookup"><span data-stu-id="10779-369">WHITEBALANCE_AUTO</span></span></td>
<td><span data-ttu-id="10779-370">A câmera usa um mecanismo automático para definir o equilíbrio de branco.</span><span class="sxs-lookup"><span data-stu-id="10779-370">The camera uses an automatic mechanism to set the white balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-371">WHITEBALANCE_ONEPUSH_AUTO</span><span class="sxs-lookup"><span data-stu-id="10779-371">WHITEBALANCE_ONEPUSH_AUTO</span></span></td>
<td><span data-ttu-id="10779-372">A câmera determina a configuração de balanço de branco quando um usuário pressiona o botão capturar enquanto aponta a câmera uma área branca.</span><span class="sxs-lookup"><span data-stu-id="10779-372">The camera determines the white balance setting when a user presses the capture button while pointing the camera at a white surface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-373">WHITEBALANCE_DAYLIGHT</span><span class="sxs-lookup"><span data-stu-id="10779-373">WHITEBALANCE_DAYLIGHT</span></span></td>
<td><span data-ttu-id="10779-374">A câmera define o equilíbrio de branco com um valor apropriado para uso em condições de horário de verão.</span><span class="sxs-lookup"><span data-stu-id="10779-374">The camera sets the white balance to a value appropriate for use in daylight conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-375">WHITEBALANCE_FLORESCENT</span><span class="sxs-lookup"><span data-stu-id="10779-375">WHITEBALANCE_FLORESCENT</span></span></td>
<td><span data-ttu-id="10779-376">A câmera define o equilíbrio de branco com um valor apropriado para uso com uma fonte de luz fluorescente.</span><span class="sxs-lookup"><span data-stu-id="10779-376">The camera sets the white balance to a value appropriate for use with a fluorescent light source.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10779-377">WHITEBALANCE_TUNGSTEN</span><span class="sxs-lookup"><span data-stu-id="10779-377">WHITEBALANCE_TUNGSTEN</span></span></td>
<td><span data-ttu-id="10779-378">A câmera define o equilíbrio de branco com um valor apropriado para uso com uma fonte de luz Tungsten.</span><span class="sxs-lookup"><span data-stu-id="10779-378">The camera sets the white balance to a value appropriate for use with a tungsten light source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10779-379">WHITEBALANCE_FLASH</span><span class="sxs-lookup"><span data-stu-id="10779-379">WHITEBALANCE_FLASH</span></span></td>
<td><span data-ttu-id="10779-380">A câmera define o equilíbrio de branco com um valor apropriado para uso com um flash eletrônico.</span><span class="sxs-lookup"><span data-stu-id="10779-380">The camera sets the white balance to a value appropriate for use with an electronic flash.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <span data-ttu-id="10779-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-382">Descreve uma URL.</span><span class="sxs-lookup"><span data-stu-id="10779-382">Describes a URL.</span></span> <span data-ttu-id="10779-383">A URL descrita por esse proroperty é aquela que as imagens ou os objetos, depois de serem adquiridos do dispositivo, podem ser carregados para – de acordo com um dos cenários a seguir.</span><span class="sxs-lookup"><span data-stu-id="10779-383">The URL described by this proroperty is one that images or objects, after they are acquired from the device, can be uploaded to—according to one of the following scenarios.</span></span></p>
<ul>
<li><span data-ttu-id="10779-384">Um aplicativo WIA lê essa propriedade e permite que o usuário carregue imagens automaticamente na URL.</span><span class="sxs-lookup"><span data-stu-id="10779-384">A WIA application reads this property and allows the user to automatically upload images to the URL.</span></span></li>
<li><span data-ttu-id="10779-385">Um aplicativo define a URL e outros dispositivos (quiosques e assim por diante) usam essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10779-385">An application sets the URL, and other devices (kiosks and so forth) use this property.</span></span></li>
</ul>
<p><span data-ttu-id="10779-386">O Microsoft Windows não carrega imagens por si só.</span><span class="sxs-lookup"><span data-stu-id="10779-386">Microsoft Windows does not upload images by itself.</span></span></p>
<p><span data-ttu-id="10779-387">Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-387">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <span data-ttu-id="10779-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-389">O nome do proprietário (que é o usuário atual) do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10779-389">The name of the owner ( which is the current user) of the device.</span></span> <span data-ttu-id="10779-390">O dispositivo usa essa propriedade para popular o campo artista em todas as imagens EXIF capturadas.</span><span class="sxs-lookup"><span data-stu-id="10779-390">The device uses this property to populate the Artist field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="10779-391">Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-391">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <span data-ttu-id="10779-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span><span class="sxs-lookup"><span data-stu-id="10779-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="10779-393">A notificação de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="10779-393">The copyright notification.</span></span> <span data-ttu-id="10779-394">O dispositivo usa essa propriedade para popular o campo de direitos autorais em cada imagem de EXIF capturada.</span><span class="sxs-lookup"><span data-stu-id="10779-394">The device uses this property to populate the Copyright field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="10779-395">Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="10779-395">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="10779-396">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10779-396">Requirements</span></span>



| <span data-ttu-id="10779-397">Requisito</span><span class="sxs-lookup"><span data-stu-id="10779-397">Requirement</span></span> | <span data-ttu-id="10779-398">Valor</span><span class="sxs-lookup"><span data-stu-id="10779-398">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="10779-399">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10779-399">Minimum supported client</span></span><br/> | <span data-ttu-id="10779-400">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="10779-400">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="10779-401">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10779-401">Minimum supported server</span></span><br/> | <span data-ttu-id="10779-402">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10779-402">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="10779-403">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10779-403">Header</span></span><br/>                   | <dl> <span data-ttu-id="10779-404"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="10779-404"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




