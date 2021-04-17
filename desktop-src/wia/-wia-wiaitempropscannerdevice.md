---
description: Os dispositivos de hardware da aquisição de imagens do Windows (WIA) têm valores de propriedade que são armazenados no registro do Windows.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Constantes de propriedade de dispositivo do scanner (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763054"
---
# <a name="scanner-device-property-constants"></a><span data-ttu-id="cf985-103">Constantes de propriedade de dispositivo do scanner</span><span class="sxs-lookup"><span data-stu-id="cf985-103">Scanner Device Property Constants</span></span>

<span data-ttu-id="cf985-104">Os dispositivos de hardware da aquisição de imagens do Windows (WIA) têm valores de propriedade que são armazenados no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="cf985-104">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="cf985-105">Para obter mais informações, consulte [**constantes de propriedade de dispositivo comum**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="cf985-105">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span> <span data-ttu-id="cf985-106">As seguintes constantes de propriedade de dispositivo, com suas cadeias de caracteres associadas, são específicas para scanners de imagem digital.</span><span class="sxs-lookup"><span data-stu-id="cf985-106">The following device property constants, with their associated strings, are specific to digital image scanners.</span></span>

<span data-ttu-id="cf985-107">O prefixo " \_ DPS \_ do WIA" indica uma propriedade de dispositivo para dispositivos de scanner e é a Convenção de nomenclatura usada em C/C++.</span><span class="sxs-lookup"><span data-stu-id="cf985-107">The prefix "WIA\_DPS\_" indicates a Device Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="cf985-108">Para fins de script, essas constantes usam o prefixo "ScannerDevice" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="cf985-108">For scripting purposes these constants use the prefix "ScannerDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="cf985-109">O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf985-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="cf985-110">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="cf985-110">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="cf985-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <span data-ttu-id="cf985-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="cf985-113">Essa propriedade tem suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-113">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="cf985-114">Contém um identificador de instância de função exclusivo para um dispositivo de scanner de serviços Web.</span><span class="sxs-lookup"><span data-stu-id="cf985-114">Contains a unique function instance identifier for a web services scanner device.</span></span> <span data-ttu-id="cf985-115">Esse identificador representa o serviço Web no dispositivo de scanner com o qual o mini-driver WIA está se comunicando.</span><span class="sxs-lookup"><span data-stu-id="cf985-115">This identifier represents the web service on the scanner device with which the WIA mini-driver is communicating.</span></span> <span data-ttu-id="cf985-116">Não é necessário fazer suposições sobre a forma desse identificador.</span><span class="sxs-lookup"><span data-stu-id="cf985-116">No assumptions about the form of this identifier should be made.</span></span> <span data-ttu-id="cf985-117">O mini-driver WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-117">The WIA mini-driver creates and maintains this property.</span></span> <br/> <span data-ttu-id="cf985-118">Os aplicativos WIA podem usar o valor de WIA_DPS_DEVICE_ID para localizar, usando a API de descoberta de função, o objeto de instância de função que representa o dispositivo de scanner de serviços Web usado na sessão atual do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="cf985-118">WIA applications can use the value of WIA_DPS_DEVICE_ID to find, using the Function Discovery API, the function instance object representing the web services scanner device used in the current WIA 2.0 session.</span></span><br/> <span data-ttu-id="cf985-119">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-119">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <span data-ttu-id="cf985-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cf985-121">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="cf985-121">Reserved, do not use.</span></span><br/> <span data-ttu-id="cf985-122">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-122">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <span data-ttu-id="cf985-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cf985-124">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="cf985-124">Reserved, do not use.</span></span><br/> <span data-ttu-id="cf985-125">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-125">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <span data-ttu-id="cf985-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cf985-127">Contém os recursos do verificador.</span><span class="sxs-lookup"><span data-stu-id="cf985-127">Contains the capabilities of the scanner.</span></span> <span data-ttu-id="cf985-128">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-128">The minidriver creates and maintains this property.</span></span> <br/> <span data-ttu-id="cf985-129">Um aplicativo lê essa propriedade para determinar se o scanner tem um mesa de alimentação, alimentador de documentos ou duplexador instalado.</span><span class="sxs-lookup"><span data-stu-id="cf985-129">An application reads this property to determine whether the scanner has a flatbed, document feeder, or duplexer installed.</span></span> <span data-ttu-id="cf985-130">Essa propriedade também é usada para definir ainda mais os recursos instalados.</span><span class="sxs-lookup"><span data-stu-id="cf985-130">This property is also used to further define the installed features.</span></span><br/> <span data-ttu-id="cf985-131">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-131">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="cf985-132">A tabela a seguir descreve as constantes válidas somente com o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cf985-132">The following table describes the constants that are valid with Windows 7 only.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-133">Flags</span><span class="sxs-lookup"><span data-stu-id="cf985-133">Flags</span></span></th>
<th><span data-ttu-id="cf985-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-135">AUTO_SOURCE</span><span class="sxs-lookup"><span data-stu-id="cf985-135">AUTO_SOURCE</span></span></td>
<td><span data-ttu-id="cf985-136">O verificador tem um manipulador de documento automático instalado.</span><span class="sxs-lookup"><span data-stu-id="cf985-136">The scanner has an automatic document handler installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cf985-137">A tabela a seguir descreve as constantes que são válidas somente com o Windows 7 e o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-137">The following table describes the constants that are valid with Windows 7 and Windows Vista only.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-138">Flags</span><span class="sxs-lookup"><span data-stu-id="cf985-138">Flags</span></span></th>
<th><span data-ttu-id="cf985-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-140">ADVANCED_DUP</span><span class="sxs-lookup"><span data-stu-id="cf985-140">ADVANCED_DUP</span></span></td>
<td><span data-ttu-id="cf985-141">O dispositivo dá suporte à configuração de digitalização duplex avançada.</span><span class="sxs-lookup"><span data-stu-id="cf985-141">The device supports advanced duplex scan configuration.</span></span> <span data-ttu-id="cf985-142">Use WIA_IPS_DUPLEX_SETTINGS para alternar entre o uso das configurações de duplex básico e avançado.</span><span class="sxs-lookup"><span data-stu-id="cf985-142">Use WIA_IPS_DUPLEX_SETTINGS to switch between using basic and advanced duplex configurations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-143">DETECT_FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="cf985-143">DETECT_FILM_TPA</span></span></td>
<td><span data-ttu-id="cf985-144">O verificador pode detectar quando o adaptador de transparência/filme está pronto para verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-144">The scanner can detect when the transparency/film adapter is ready to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-145">DETECT_STOR</span><span class="sxs-lookup"><span data-stu-id="cf985-145">DETECT_STOR</span></span></td>
<td><span data-ttu-id="cf985-146">O verificador pode detectar quando há documentos no armazenamento interno.</span><span class="sxs-lookup"><span data-stu-id="cf985-146">The scanner can detect when there are documents in the internal storage.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-147">FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="cf985-147">FILM_TPA</span></span></td>
<td><span data-ttu-id="cf985-148">O scanner é equipado com um adaptador de verificação de transparência/filme.</span><span class="sxs-lookup"><span data-stu-id="cf985-148">The scanner is equipped with a transparency/film scanning adapter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-149">ARMA</span><span class="sxs-lookup"><span data-stu-id="cf985-149">STOR</span></span></td>
<td><span data-ttu-id="cf985-150">O scanner está equipado com um dispositivo de armazenamento de imagem interno.</span><span class="sxs-lookup"><span data-stu-id="cf985-150">The scanner is equipped with an internal image storage device.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cf985-151">A tabela a seguir descreve as constantes que são válidas com o Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-151">The following table describes the constants that are valid with Windows XP or later.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-152">Flags</span><span class="sxs-lookup"><span data-stu-id="cf985-152">Flags</span></span></th>
<th><span data-ttu-id="cf985-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-154">DETECT_FEED</span><span class="sxs-lookup"><span data-stu-id="cf985-154">DETECT_FEED</span></span></td>
<td><span data-ttu-id="cf985-155">O verificador pode detectar um documento no alimentador.</span><span class="sxs-lookup"><span data-stu-id="cf985-155">The scanner can detect a document in the feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-156">DETECT_FLAT</span><span class="sxs-lookup"><span data-stu-id="cf985-156">DETECT_FLAT</span></span></td>
<td><span data-ttu-id="cf985-157">O verificador pode detectar um documento no cilindro de mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-157">The scanner can detect a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-158">DETECT_SCAN</span><span class="sxs-lookup"><span data-stu-id="cf985-158">DETECT_SCAN</span></span></td>
<td><span data-ttu-id="cf985-159">O verificador pode detectar um documento no alimentador somente examinando.</span><span class="sxs-lookup"><span data-stu-id="cf985-159">The scanner can detect a document in the feeder only by scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-160">DUPLICA</span><span class="sxs-lookup"><span data-stu-id="cf985-160">DUP</span></span></td>
<td><span data-ttu-id="cf985-161">O scanner tem um duplexador.</span><span class="sxs-lookup"><span data-stu-id="cf985-161">The scanner has a duplexer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-162">FEED</span><span class="sxs-lookup"><span data-stu-id="cf985-162">FEED</span></span></td>
<td><span data-ttu-id="cf985-163">O verificador tem um manipulador de documento automático instalado.</span><span class="sxs-lookup"><span data-stu-id="cf985-163">The scanner has an automatic document handler installed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-164">PLANOS</span><span class="sxs-lookup"><span data-stu-id="cf985-164">FLAT</span></span></td>
<td><span data-ttu-id="cf985-165">O scanner tem um cilindro de mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-165">The scanner has a flatbed platen.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cf985-166">A tabela a seguir descreve as constantes válidas somente com o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cf985-166">The following table describes the constants that are valid with Windows XP only.</span></span> <span data-ttu-id="cf985-167">Esses valores foram preteridos para o Windows 7 e o Windows Vista e não devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="cf985-167">These values have been deprecated for Windows 7 and Windows Vista and should not be used.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-168">Flags</span><span class="sxs-lookup"><span data-stu-id="cf985-168">Flags</span></span></th>
<th><span data-ttu-id="cf985-169">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-170">DETECT_DUP</span><span class="sxs-lookup"><span data-stu-id="cf985-170">DETECT_DUP</span></span></td>
<td><span data-ttu-id="cf985-171">O verificador pode detectar uma solicitação de verificação duplex do usuário.</span><span class="sxs-lookup"><span data-stu-id="cf985-171">The scanner can detect a duplex scan request from the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-172">DETECT_DUP_AVAIL</span><span class="sxs-lookup"><span data-stu-id="cf985-172">DETECT_DUP_AVAIL</span></span></td>
<td><span data-ttu-id="cf985-173">O verificador pode saber quando o duplexador está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf985-173">The scanner can tell when the duplexer is installed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-174">DETECT_FEED_AVAIL</span><span class="sxs-lookup"><span data-stu-id="cf985-174">DETECT_FEED_AVAIL</span></span></td>
<td><span data-ttu-id="cf985-175">O verificador pode saber quando o alimentador automático de documentos está instalado.</span><span class="sxs-lookup"><span data-stu-id="cf985-175">The scanner can tell when the automatic document feeder is installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <span data-ttu-id="cf985-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-177">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-177">This property is not supported in Windows Vista and later.</span></span> <span data-ttu-id="cf985-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-179">Contém a origem e o modo de aquisição do scanner atual. O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-179">Contains the current scanner acquisition source and mode.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-180">Um aplicativo lê essa propriedade para determinar a fonte de aquisição atual do scanner ou para gravar essa propriedade para definir a origem e o modo do verificador.</span><span class="sxs-lookup"><span data-stu-id="cf985-180">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="cf985-181">Além disso, os aplicativos usam essa propriedade para habilitar e desabilitar a funcionalidade do duplexador.</span><span class="sxs-lookup"><span data-stu-id="cf985-181">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="cf985-182">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="cf985-182">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="cf985-183">A tabela a seguir tem as dez constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-183">The following table has the ten constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-184">Flags</span><span class="sxs-lookup"><span data-stu-id="cf985-184">Flags</span></span></th>
<th><span data-ttu-id="cf985-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-186">ALIMENTADORA</span><span class="sxs-lookup"><span data-stu-id="cf985-186">FEEDER</span></span></td>
<td><span data-ttu-id="cf985-187">Digitalizar usando o alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="cf985-187">Scan using the document feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-188">MESA</span><span class="sxs-lookup"><span data-stu-id="cf985-188">FLATBED</span></span></td>
<td><span data-ttu-id="cf985-189">Digitalizar usando a mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-189">Scan using the flatbed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-190">DUPLEX</span><span class="sxs-lookup"><span data-stu-id="cf985-190">DUPLEX</span></span></td>
<td><span data-ttu-id="cf985-191">Examinar usando operações do duplex.</span><span class="sxs-lookup"><span data-stu-id="cf985-191">Scan using duplexer operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-192">AUTO_ADVANCE</span><span class="sxs-lookup"><span data-stu-id="cf985-192">AUTO_ADVANCE</span></span></td>
<td><span data-ttu-id="cf985-193">Habilita a alimentação automática do próximo documento após uma verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-193">Enables automatic feeding of the next document after a scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-194">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="cf985-194">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="cf985-195">Primeiro examine a frente do documento.</span><span class="sxs-lookup"><span data-stu-id="cf985-195">Scan the front of the document first.</span></span> <span data-ttu-id="cf985-196">Esse valor é válido quando DUPLEX é definido.</span><span class="sxs-lookup"><span data-stu-id="cf985-196">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-197">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="cf985-197">BACK_FIRST</span></span></td>
<td><span data-ttu-id="cf985-198">Primeiro examine a parte de trás do documento.</span><span class="sxs-lookup"><span data-stu-id="cf985-198">Scan the back of the document first.</span></span> <span data-ttu-id="cf985-199">Esse valor é válido quando DUPLEX é definido.</span><span class="sxs-lookup"><span data-stu-id="cf985-199">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-200">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="cf985-200">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="cf985-201">Verificar somente a frente.</span><span class="sxs-lookup"><span data-stu-id="cf985-201">Scan the front only.</span></span> <span data-ttu-id="cf985-202">Esse valor é válido quando DUPLEX é definido.</span><span class="sxs-lookup"><span data-stu-id="cf985-202">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-203">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="cf985-203">BACK_ONLY</span></span></td>
<td><span data-ttu-id="cf985-204">Verifique apenas o verso.</span><span class="sxs-lookup"><span data-stu-id="cf985-204">Scan the back only.</span></span> <span data-ttu-id="cf985-205">Esse valor é válido quando DUPLEX é definido.</span><span class="sxs-lookup"><span data-stu-id="cf985-205">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-206">NEXT_PAGE</span><span class="sxs-lookup"><span data-stu-id="cf985-206">NEXT_PAGE</span></span></td>
<td><span data-ttu-id="cf985-207">Digitalizar a próxima página do documento.</span><span class="sxs-lookup"><span data-stu-id="cf985-207">Scan the next page of the document.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-208">PREFEED</span><span class="sxs-lookup"><span data-stu-id="cf985-208">PREFEED</span></span></td>
<td><span data-ttu-id="cf985-209">Habilite o modo de pré-feed.</span><span class="sxs-lookup"><span data-stu-id="cf985-209">Enable pre-feed mode.</span></span> <span data-ttu-id="cf985-210">Pré-posicionar próximo documento durante a verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-210">Pre-position next document while scanning.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <span data-ttu-id="cf985-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-212">Contém o estado atual do feed instalado do scanner, alimentador de documentos ou duplexador.</span><span class="sxs-lookup"><span data-stu-id="cf985-212">Contains current state of the scanner's installed flatbed, document feeder, or duplexer.</span></span> <span data-ttu-id="cf985-213">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-213">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-214">Um aplicativo lê essa propriedade para determinar se o dispositivo de scanner está pronto para ser usado.</span><span class="sxs-lookup"><span data-stu-id="cf985-214">An application reads this property to determine whether the scanner device is ready to be used.</span></span> <span data-ttu-id="cf985-215">Essa é uma maneira ideal de verificar se o papel está no alimentador antes de adquirir uma imagem.</span><span class="sxs-lookup"><span data-stu-id="cf985-215">This is an ideal way to check whether paper is in the feeder prior to acquiring an image.</span></span></p>
<p><span data-ttu-id="cf985-216">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-216">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-217">A tabela a seguir tem as constantes que são válidas com essa propriedade. Um asterisco \* indica que o sinalizador não tem suporte no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-217">The following table has the constants that are valid with this property.An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="cf985-218">O símbolo <strong>V</strong> indica que o sinalizador tem suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-218">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-219">Flags</span><span class="sxs-lookup"><span data-stu-id="cf985-219">Flags</span></span></th>
<th><span data-ttu-id="cf985-220">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-220">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-221">FEED_READY</span><span class="sxs-lookup"><span data-stu-id="cf985-221">FEED_READY</span></span></td>
<td><span data-ttu-id="cf985-222">A mesa está pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="cf985-222">The flatbed is ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-223">FLAT_READY</span><span class="sxs-lookup"><span data-stu-id="cf985-223">FLAT_READY</span></span></td>
<td><span data-ttu-id="cf985-224">O scanner tem um documento no cilindro de mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-224">The scanner has a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-225">DUP_READY</span><span class="sxs-lookup"><span data-stu-id="cf985-225">DUP_READY</span></span></td>
<td><span data-ttu-id="cf985-226">O duplexador está habilitado e pronto para ser usado.</span><span class="sxs-lookup"><span data-stu-id="cf985-226">The duplexer is enabled and ready to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-227">FLAT_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="cf985-227">FLAT_COVER_UP</span></span></td>
<td><span data-ttu-id="cf985-228">A tampa da cama plana está ativa.</span><span class="sxs-lookup"><span data-stu-id="cf985-228">The flat bed cover is up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-229">PATH_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="cf985-229">PATH_COVER_UP</span></span></td>
<td><span data-ttu-id="cf985-230">O caminho do papel é coberto e está impedindo a operação adequada.</span><span class="sxs-lookup"><span data-stu-id="cf985-230">The paper path is covered up and is preventing proper operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-231">PAPER_JAM</span><span class="sxs-lookup"><span data-stu-id="cf985-231">PAPER_JAM</span></span></td>
<td><span data-ttu-id="cf985-232">Um documento está emperrado no alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="cf985-232">A document is jammed in the document feeder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-233">FILM_TPA_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-233">FILM_TPA_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="cf985-234">O adaptador de transparência está instalado e pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="cf985-234">The transparency adapter is installed and ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-235">STORAGE_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-235">STORAGE_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="cf985-236">O dispositivo de armazenamento interno está pronto.</span><span class="sxs-lookup"><span data-stu-id="cf985-236">The internal storage device is ready.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-237">STORAGE_FULL<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-237">STORAGE_FULL<strong>V</strong></span></span></td>
<td><span data-ttu-id="cf985-238">O armazenamento está cheio, nenhuma operação de carregamento é possível.</span><span class="sxs-lookup"><span data-stu-id="cf985-238">The storage is full, no upload operations possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-239">MULTIPLE_FEED<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-239">MULTIPLE_FEED<strong>V</strong></span></span></td>
<td><span data-ttu-id="cf985-240">Ocorreu uma condição de feed múltiplo (geralmente com um PAPER_JAM).</span><span class="sxs-lookup"><span data-stu-id="cf985-240">A multiple feed condition occurred (usually with a PAPER_JAM).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-241">DEVICE_ATTENTION<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-241">DEVICE_ATTENTION<strong>V</strong></span></span></td>
<td><span data-ttu-id="cf985-242">Há um erro que requer a intervenção do usuário no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf985-242">There is an error that requires user intervention on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-243">LAMP_ERR<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-243">LAMP_ERR<strong>V</strong></span></span></td>
<td><span data-ttu-id="cf985-244">O scanner não está pronto devido a um problema de lâmpada.</span><span class="sxs-lookup"><span data-stu-id="cf985-244">The scanner is not ready due to a lamp problem.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <span data-ttu-id="cf985-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-246">Contém todos os caracteres válidos que um aplicativo pode usar para criar cadeias válidas de endossador.</span><span class="sxs-lookup"><span data-stu-id="cf985-246">Contains all the valid characters that an application can use to create valid endorser strings.</span></span> <span data-ttu-id="cf985-247">Um endossador é uma impressora instalada em um scanner que imprime uma mensagem de texto em todas as páginas verificadas.</span><span class="sxs-lookup"><span data-stu-id="cf985-247">An endorser is a printer installed on a scanner that imprints a text message on every page scanned.</span></span> <span data-ttu-id="cf985-248">O minidriver deve validar a configuração da propriedade <strong>WIA_DPS_ENDORSER_STRING</strong> em relação ao conjunto de caracteres válido nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-248">The minidriver should validate the setting of the <strong>WIA_DPS_ENDORSER_STRING</strong> property against the valid character set in this property.</span></span> <span data-ttu-id="cf985-249">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-249">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-250">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-250">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <span data-ttu-id="cf985-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-252">Contém uma cadeia de caracteres que deve ser endossada (em outras palavras, impressa) em cada página que o minidriver examina.</span><span class="sxs-lookup"><span data-stu-id="cf985-252">Contains a string that is to be endorsed (in other words, printed) on each page that the minidriver scans.</span></span> <span data-ttu-id="cf985-253">Um aplicativo define essa propriedade usando o conjunto de caracteres válido que é relatado na propriedade <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> .</span><span class="sxs-lookup"><span data-stu-id="cf985-253">An application sets this property using the valid character set that is reported in the <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> property.</span></span> <span data-ttu-id="cf985-254">O minidriver deve endossar documentos somente se uma cadeia de caracteres estiver definida nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-254">The minidriver should endorse documents only if a string is set in this property.</span></span> <span data-ttu-id="cf985-255">Uma cadeia de caracteres vazia significa que a funcionalidade do endossador está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="cf985-255">An empty string means that the endorser functionality is disabled.</span></span></p>
<p><span data-ttu-id="cf985-256">Como é responsabilidade do driver interpretar a cadeia de caracteres do endossador, o driver pode usar caracteres especiais em <strong>WIA_DPS_ENDORSER_STRING</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf985-256">Because it is the driver's responsibility to interpret the endorser string, your driver can use special characters in <strong>WIA_DPS_ENDORSER_STRING</strong>.</span></span> <span data-ttu-id="cf985-257">No entanto, apenas seus aplicativos compreenderiam esses caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf985-257">However, only your applications would understand these characters.</span></span></p>
<p><span data-ttu-id="cf985-258">Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-258">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-259">Um driver que dá suporte à propriedade <strong>WIA_DPS_ENDORSER_STRING</strong> deve oferecer suporte à lista de tokens a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf985-259">A driver supporting the <strong>WIA_DPS_ENDORSER_STRING</strong> property must support the following list of tokens.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-260">Token</span><span class="sxs-lookup"><span data-stu-id="cf985-260">Token</span></span></th>
<th><span data-ttu-id="cf985-261">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-262">$DATE $</span><span class="sxs-lookup"><span data-stu-id="cf985-262">$DATE$</span></span></td>
<td><span data-ttu-id="cf985-263">A data no formato AAAA/MM/DD.</span><span class="sxs-lookup"><span data-stu-id="cf985-263">The date in the form YYYY/MM/DD.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-264">$DAY $</span><span class="sxs-lookup"><span data-stu-id="cf985-264">$DAY$</span></span></td>
<td><span data-ttu-id="cf985-265">O dia no formato DD.</span><span class="sxs-lookup"><span data-stu-id="cf985-265">The day in the form DD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-266">$MONTH $</span><span class="sxs-lookup"><span data-stu-id="cf985-266">$MONTH$</span></span></td>
<td><span data-ttu-id="cf985-267">O mês do ano no formato MM.</span><span class="sxs-lookup"><span data-stu-id="cf985-267">The month of the year in the form MM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-268">$PAGE _COUNT $</span><span class="sxs-lookup"><span data-stu-id="cf985-268">$PAGE_COUNT$</span></span></td>
<td><span data-ttu-id="cf985-269">O número de páginas transferidas.</span><span class="sxs-lookup"><span data-stu-id="cf985-269">The number of pages transferred.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-270">$TIME $</span><span class="sxs-lookup"><span data-stu-id="cf985-270">$TIME$</span></span></td>
<td><span data-ttu-id="cf985-271">A hora do dia no formato HH: MM: SS.</span><span class="sxs-lookup"><span data-stu-id="cf985-271">The time of day in the form HH:MM:SS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-272">$YEAR $</span><span class="sxs-lookup"><span data-stu-id="cf985-272">$YEAR$</span></span></td>
<td><span data-ttu-id="cf985-273">O ano no formato aaaa.</span><span class="sxs-lookup"><span data-stu-id="cf985-273">The year in the form YYYY.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <span data-ttu-id="cf985-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-275">Reservado, não use.</span><span class="sxs-lookup"><span data-stu-id="cf985-275">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="cf985-276">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <span data-ttu-id="cf985-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-278">Essa propriedade tem suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-278">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-279">Contém o endereço SOAP de um dispositivo de scanner de serviços Web.</span><span class="sxs-lookup"><span data-stu-id="cf985-279">Contains the SOAP address of a web services scanner device.</span></span> <span data-ttu-id="cf985-280">O mini-driver WIA 2,0 cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-280">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-281">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-281">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <span data-ttu-id="cf985-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-283">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-283">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-284">Contém o registro, ou alinhamento horizontal, para documentos colocados na mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-284">Contains the registration, or horizontal alignment, for documents placed on the flatbed.</span></span> <span data-ttu-id="cf985-285">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-285">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-286">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-286">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-287">A tabela a seguir tem as três constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-287">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-288">Constante</span><span class="sxs-lookup"><span data-stu-id="cf985-288">Constant</span></span></th>
<th><span data-ttu-id="cf985-289">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-290">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="cf985-290">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="cf985-291">O papel é justificado à esquerda.</span><span class="sxs-lookup"><span data-stu-id="cf985-291">The paper is left justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-292">CENTRA</span><span class="sxs-lookup"><span data-stu-id="cf985-292">CENTERED</span></span></td>
<td><span data-ttu-id="cf985-293">O papel está centralizado.</span><span class="sxs-lookup"><span data-stu-id="cf985-293">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-294">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="cf985-294">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="cf985-295">O papel é justificado à direita.</span><span class="sxs-lookup"><span data-stu-id="cf985-295">The paper is right justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cf985-296"><strong>Consulte também</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-296"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="cf985-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <span data-ttu-id="cf985-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-299">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-299">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="cf985-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-301">Especifica a largura máxima, em milésimos de polegada, que é verificada no eixo horizontal (X) do cilindro de um scanner de mesa na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="cf985-301">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="cf985-302">Essa propriedade também se aplica a alimentadores de documentos automáticos que movem planilhas para o cilindro de um scanner de mesa para verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-302">This property also applies to automatic document feeders that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="cf985-303">Essa propriedade é obrigatória para scanners que têm um cilindro.</span><span class="sxs-lookup"><span data-stu-id="cf985-303">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="cf985-304">Em vez disso, outros tipos de scanner implementarão a propriedade <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="cf985-304">Other scanner types will instead implement the <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="cf985-305">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-305">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="cf985-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-307">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-307">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="cf985-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-309">Especifica a largura máxima, em milésimos de polegada, que é verificada no eixo horizontal (X) de um scanner de alimentação de papel ou portátil na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="cf985-309">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="cf985-310">Essa propriedade também se aplica a alimentadores de documentos automáticos que examinam sem mover folhas para o cilindro de um scanner de mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-310">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="cf985-311">Essa propriedade é obrigatória para scanners alimentados por planilhas, com rolagem e por bolso.</span><span class="sxs-lookup"><span data-stu-id="cf985-311">This property is mandatory for sheet-fed, scroll-fed, and hand-held scanners.</span></span></p>
<p><span data-ttu-id="cf985-312">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <span data-ttu-id="cf985-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-314">Contém o tempo máximo para verificar uma única página com as configurações de propriedade atuais, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="cf985-314">Contains the maximum time to scan a single page with the current property settings, in milliseconds.</span></span> <span data-ttu-id="cf985-315">Um aplicativo lê essa propriedade para estimar o tempo que levará para digitalizar uma página.</span><span class="sxs-lookup"><span data-stu-id="cf985-315">An application reads this property to estimate the time it will take to scan a page.</span></span> <span data-ttu-id="cf985-316">Isso é útil ao determinar as condições de um dispositivo que parou de responder.</span><span class="sxs-lookup"><span data-stu-id="cf985-316">This is helpful when determining the conditions of a device that has stopped responding.</span></span> <span data-ttu-id="cf985-317">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-317">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="cf985-318">Essa propriedade é necessária para todos os scanners.</span><span class="sxs-lookup"><span data-stu-id="cf985-318">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="cf985-319">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-319">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="cf985-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-321">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-321">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="cf985-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-323">Contém as dimensões horizontais físicas da menor página que o alimentador de documentos do verificador pode verificar, em milésimos de uma polegada.</span><span class="sxs-lookup"><span data-stu-id="cf985-323">Contains the physical horizontal dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="cf985-324">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-324">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-325">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-325">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-326"><strong>Consulte também</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-326"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="cf985-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="cf985-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-329">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-329">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="cf985-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-331">Contém as dimensões verticais físicas da menor página que o alimentador de documentos do verificador pode verificar, em milésimos de uma polegada.</span><span class="sxs-lookup"><span data-stu-id="cf985-331">Contains the physical vertical dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="cf985-332">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-332">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-333">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-333">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-334"><strong>Consulte também</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-334"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="cf985-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <span data-ttu-id="cf985-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-337">Não há suporte para essa propriedade no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-337">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="cf985-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-339">Resolução óptica horizontal.</span><span class="sxs-lookup"><span data-stu-id="cf985-339">Horizontal Optical Resolution.</span></span> <span data-ttu-id="cf985-340">Resolução óptica horizontal mais alta com suporte em DPI.</span><span class="sxs-lookup"><span data-stu-id="cf985-340">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="cf985-341">Essa propriedade é um único valor.</span><span class="sxs-lookup"><span data-stu-id="cf985-341">This property is a single value.</span></span> <span data-ttu-id="cf985-342">Esta não é uma lista de todas as resoluções que podem ser geradas pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf985-342">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="cf985-343">Em vez disso, essa é a resolução da fibra óptica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf985-343">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="cf985-344">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-344">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="cf985-345">Essa propriedade é necessária para todos os scanners.</span><span class="sxs-lookup"><span data-stu-id="cf985-345">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="cf985-346">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-346">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <span data-ttu-id="cf985-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-348">Não há suporte para essa propriedade no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-348">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="cf985-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-350">Resolução óptica vertical.</span><span class="sxs-lookup"><span data-stu-id="cf985-350">Vertical Optical Resolution.</span></span> <span data-ttu-id="cf985-351">Resolução óptica vertical com suporte mais alta em DPI.</span><span class="sxs-lookup"><span data-stu-id="cf985-351">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="cf985-352">Essa propriedade é um único valor.</span><span class="sxs-lookup"><span data-stu-id="cf985-352">This property is a single value.</span></span> <span data-ttu-id="cf985-353">Essa não é uma lista de todas as resoluções que são geradas pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf985-353">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="cf985-354">Em vez disso, essa é a resolução da fibra óptica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf985-354">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="cf985-355">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-355">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="cf985-356">Essa propriedade é necessária para todos os scanners.</span><span class="sxs-lookup"><span data-stu-id="cf985-356">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="cf985-357">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-357">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <span data-ttu-id="cf985-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-359">Contém a configuração de orientação atual. O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-359">Contains the current orientation setting.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-360">Um aplicativo define a propriedade <strong>WIA_DPS_ORIENTATION</strong> para definir a orientação original de uma página ou imagem a ser adquirida.</span><span class="sxs-lookup"><span data-stu-id="cf985-360">An application sets the <strong>WIA_DPS_ORIENTATION</strong> property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="cf985-361">Para obter informações sobre como usar WIA_DPS_ORIENTATION, consulte <strong>WIA_DPS_PAGE_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-361">For information on how to use WIA_DPS_ORIENTATION, see <strong>WIA_DPS_PAGE_SIZE</strong></span></span></p>
<p><span data-ttu-id="cf985-362">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cf985-362">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cf985-363">A tabela a seguir tem as quatro constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-363">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-364">Valor</span><span class="sxs-lookup"><span data-stu-id="cf985-364">Value</span></span></th>
<th><span data-ttu-id="cf985-365">Defination</span><span class="sxs-lookup"><span data-stu-id="cf985-365">Defination</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-366">AMBIENTE</span><span class="sxs-lookup"><span data-stu-id="cf985-366">LANDSCAPE</span></span></td>
<td><span data-ttu-id="cf985-367">rotação no sentido anti-horário de 90 graus, em relação à orientação retrato.</span><span class="sxs-lookup"><span data-stu-id="cf985-367">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-368">ORIENTAÇÕES</span><span class="sxs-lookup"><span data-stu-id="cf985-368">PORTRAIT</span></span></td>
<td><span data-ttu-id="cf985-369">0 graus.</span><span class="sxs-lookup"><span data-stu-id="cf985-369">0 degrees.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-370">ROT180</span><span class="sxs-lookup"><span data-stu-id="cf985-370">ROT180</span></span></td>
<td><span data-ttu-id="cf985-371">rotação no sentido anti-horário de 180 graus, em relação à orientação retrato.</span><span class="sxs-lookup"><span data-stu-id="cf985-371">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-372">ROT270</span><span class="sxs-lookup"><span data-stu-id="cf985-372">ROT270</span></span></td>
<td><span data-ttu-id="cf985-373">rotação no sentido anti-horário de 270 graus, em relação à orientação retrato.</span><span class="sxs-lookup"><span data-stu-id="cf985-373">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cf985-374"><strong>Consulte também</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-374"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="cf985-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf985-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <span data-ttu-id="cf985-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-377">Cor usada para preencher quando não há dados de imagem suficientes para completar um buffer solicitado.</span><span class="sxs-lookup"><span data-stu-id="cf985-377">Color used to pad when there is not enough image data to fill a requested buffer.</span></span> <span data-ttu-id="cf985-378">Essa propriedade é implementada para os scanners que esfolham o buffer.</span><span class="sxs-lookup"><span data-stu-id="cf985-378">This property is implemented for scanners that pad the buffer.</span></span> <span data-ttu-id="cf985-379">Essa propriedade é opcional para todos os scanners.</span><span class="sxs-lookup"><span data-stu-id="cf985-379">This property is optional for all scanners.</span></span> <span data-ttu-id="cf985-380">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-380">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-381">Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-381">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-382">O formato das informações de cor é <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-382">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <span data-ttu-id="cf985-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-384">Não há suporte para essa propriedade no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-384">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="cf985-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-386">Contém a altura, em milésimos de polegada, da página atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="cf985-386">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="cf985-387">O minidriver cria e mantém a propriedade <strong>WIA_DPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="cf985-387">The minidriver creates and maintains the <strong>WIA_DPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="cf985-388">Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo examinada.</span><span class="sxs-lookup"><span data-stu-id="cf985-388">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="cf985-389">Se as configurações de extensão forem diferentes dos tamanhos de página conhecidos, essa propriedade relatará a altura da página cujo <strong>WIA_DPS_PAGE_SIZE</strong> Propriedade está definida como WIA_PAGE_CUSTOM (que é um valor da propriedade <strong>WIA_DPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="cf985-389">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_DPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="cf985-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> deve estar em sincronia com <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que relata a altura, em pixels, da página a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="cf985-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> must be in sync with <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="cf985-391">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <span data-ttu-id="cf985-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-393">Não há suporte para essa propriedade no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-393">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="cf985-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-395">Contém o tamanho da página selecionada no momento para ser examinada.</span><span class="sxs-lookup"><span data-stu-id="cf985-395">Contains the size of the page that is currently selected to be scanned.</span></span> <span data-ttu-id="cf985-396">Para selecionar as dimensões da página a ser verificada, um aplicativo define essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-396">To select the dimensions of the page to scan, an application sets this property.</span></span> <span data-ttu-id="cf985-397">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-397">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-398">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cf985-398">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cf985-399">A tabela a seguir tem as três constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-399">The following table has the three constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-400">Valor</span><span class="sxs-lookup"><span data-stu-id="cf985-400">Value</span></span></th>
<th><span data-ttu-id="cf985-401">Definição</span><span class="sxs-lookup"><span data-stu-id="cf985-401">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-402">WIA_PAGE_A4</span><span class="sxs-lookup"><span data-stu-id="cf985-402">WIA_PAGE_A4</span></span></td>
<td><span data-ttu-id="cf985-403">8267 X 11692 (orientação retrato)</span><span class="sxs-lookup"><span data-stu-id="cf985-403">8267 X 11692 (PORTRAIT orientation)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-404">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="cf985-404">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="cf985-405">Definido pelos valores das propriedades <strong>WIA_DPS_PAGE_HEIGHT</strong> e <strong>WIA_DPS_PAGE_WIDTH</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-405">Defined by the values of the <strong>WIA_DPS_PAGE_HEIGHT</strong> and <strong>WIA_DPS_PAGE_WIDTH</strong> properties</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-406">WIA_PAGE_LETTER</span><span class="sxs-lookup"><span data-stu-id="cf985-406">WIA_PAGE_LETTER</span></span></td>
<td><span data-ttu-id="cf985-407">8500 X 11000 (orientação retrato)</span><span class="sxs-lookup"><span data-stu-id="cf985-407">8500 X 11000 (PORTRAIT orientation)</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cf985-408">O valor da propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> determina a orientação da página atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="cf985-408">The value of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="cf985-409">As propriedades <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> relatam as dimensões da página, em milésimos de polegada.</span><span class="sxs-lookup"><span data-stu-id="cf985-409">The <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="cf985-410">Observe que essas propriedades devem estar em acordo com <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, que contêm as dimensões da página em pixels.</span><span class="sxs-lookup"><span data-stu-id="cf985-410">Note that these properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span> <span data-ttu-id="cf985-411">Os valores válidos do tipo WIA_PROP_LIST devem depender das configurações válidas da propriedade <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="cf985-411">Valid values of type WIA_PROP_LIST should depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="cf985-412">Se o dispositivo não puder verificar documentos orientados a paisagem com uma configuração WIA_PAGE_A4, WIA_PAGE_A4 não deverá aparecer na lista de valores válidos para a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> for definido como LANSCAPE.</span><span class="sxs-lookup"><span data-stu-id="cf985-412">If the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 should not appear in the list of valid values for the <strong>WIA_DPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANSCAPE.</span></span></p>
<p><span data-ttu-id="cf985-413">Se um aplicativo definir <strong>WIA_DPS_PAGE_SIZE</strong> para qualquer valor diferente de WIA_PAGE_CUSTOM, o minidriver deverá ajustar os valores de <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> para as dimensões da página em milésimos de polegada.</span><span class="sxs-lookup"><span data-stu-id="cf985-413">If an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to any value other than WIA_PAGE_CUSTOM, the minidriver should adjust the values of <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="cf985-414">Ele também deve ajustar os valores de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> e <strong>WIA_IPS_YEXTENT</strong> às dimensões da página em pixels.</span><span class="sxs-lookup"><span data-stu-id="cf985-414">It should also adjust the values of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="cf985-415">Se uma configuração de extensão (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> ou <strong>WIA_IPS_YEXTENT</strong>) for alterada para um valor que não corresponda à configuração de tamanho de página atual, o minidriver deverá alterar o valor da propriedade <strong>WIA_DPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="cf985-415">If an extent setting (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page-size setting, the minidriver should change the value of the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="cf985-416">O minidriver também deve modificar <strong>WIA_DPS_PAGE_WIDTH</strong> ou <strong>WIA_DPS_PAGE_HEIGHT</strong> de acordo com a nova configuração de extensão.</span><span class="sxs-lookup"><span data-stu-id="cf985-416">The minidriver should also modify <strong>WIA_DPS_PAGE_WIDTH</strong> or <strong>WIA_DPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="cf985-417">Se <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> for definido como LANSCAPE, as configurações de extensão serão &quot; invertidas. &quot; Por exemplo, se um aplicativo definir <strong>WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_A4, minidriver deverá definir <strong>WIA_DPS_PAGE_WIDTH</strong> como 11692 e <strong>WIA_DPS_PAGE_HEIGHT</strong> como 8267.</span><span class="sxs-lookup"><span data-stu-id="cf985-417">If <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> is set to LANSCAPE, the extent settings will be &quot;flipped.&quot; For example, if an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver should set <strong>WIA_DPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_DPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="cf985-418">(O minidriver também deve definir <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> de acordo.) Observe que, se <strong>WIA_DPS_PAGE_SIZE</strong> for definido como WIA_PAGE_CUSTOM, a configuração de orientação não será usada para determinar as dimensões de extensão da página a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="cf985-418">(The minidriver should also set <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.) Note that if <strong>WIA_DPS_PAGE_SIZE</strong> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span></p>
<p><span data-ttu-id="cf985-419">O minidriver é responsável por garantir que a propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> esteja em contrato com a área de seleção atual.</span><span class="sxs-lookup"><span data-stu-id="cf985-419">The minidriver is responsible for ensuring that the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property is in agreement with the current selection area.</span></span> <span data-ttu-id="cf985-420">Se um aplicativo alterar o valor de <strong>WIA_IPS_ORIENTATION</strong> para um que seja inválido para o tamanho de página selecionado no momento, o minidriver deverá alterar o valor de <strong>WIA_DPS_PAGE_SIZE</strong> para um tamanho de página com suporte no novo valor de orientação.</span><span class="sxs-lookup"><span data-stu-id="cf985-420">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_DPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="cf985-421">Se um aplicativo definir a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_CUSTOM, a área de seleção atual não será afetada.</span><span class="sxs-lookup"><span data-stu-id="cf985-421">If an application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="cf985-422">O minidriver WIA deve obter o layout da imagem atual, começando com as configurações atuais das propriedades <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> e <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="cf985-422">The WIA minidriver should obtain the current image layout, starting from the current settings of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="cf985-423">Se a configuração de tamanho de página resultar em uma área de seleção que está fora do ambiente do scanner, o minidriver deverá ajustar automaticamente os valores das propriedades <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> para as configurações válidas.</span><span class="sxs-lookup"><span data-stu-id="cf985-423">If the page-size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="cf985-424">Se as propriedades <strong>WIA_DPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> forem definidas ao mesmo tempo e forem inválidas quando aplicadas em combinação, o minidriver deverá falhar as configurações do aplicativo retornando um erro no <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-424">If the <strong>WIA_DPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span> <span data-ttu-id="cf985-425">.</span><span class="sxs-lookup"><span data-stu-id="cf985-425">.</span></span></p>
<p><span data-ttu-id="cf985-426">Os quatro exemplos a seguir mostram diferentes cenários de <strong>WIA_DPS_PAGE_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="cf985-426">The following four examples show different <strong>WIA_DPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="cf985-427">O driver relata as configurações.</span><span class="sxs-lookup"><span data-stu-id="cf985-427">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="cf985-428">Um aplicativo define a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="cf985-428">An application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="cf985-429">Um aplicativo define a propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> como LANSCAPE.</span><span class="sxs-lookup"><span data-stu-id="cf985-429">An application sets the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property to LANSCAPE.</span></span></li>
<li><span data-ttu-id="cf985-430">Um aplicativo altera a propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> para um valor menor.</span><span class="sxs-lookup"><span data-stu-id="cf985-430">An application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="cf985-431"><strong>Exemplo 1: o minidriver relata as configurações</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-431"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="cf985-432">No exemplo a seguir, o minidriver define uma área de seleção personalizada antes que um aplicativo defina as propriedades de WIA.</span><span class="sxs-lookup"><span data-stu-id="cf985-432">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="cf985-433">Nesse caso, a área de seleção representa a mesa inteira.</span><span class="sxs-lookup"><span data-stu-id="cf985-433">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
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
<p><span data-ttu-id="cf985-434"><strong>Exemplo 2: um aplicativo define a</strong> <strong></strong><strong>Propriedade WIA_DPS_PAGE_SIZE como WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="cf985-434"><strong>Example 2: An application sets the</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
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
<p><span data-ttu-id="cf985-435"><strong>Exemplo 3: um aplicativo define a</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>Propriedade WIA_IPS_ORIENTATION como LANSCAPE</strong>  </span><span class="sxs-lookup"><span data-stu-id="cf985-435"><strong>Example 3: An application sets the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>property to LANSCAPE</strong></span></span></p>
<p><span data-ttu-id="cf985-436">A base física deve ser capaz de adquirir uma página que estava originalmente na orientação paisagem.</span><span class="sxs-lookup"><span data-stu-id="cf985-436">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<p><span data-ttu-id="cf985-437"><strong>Exemplo 4: um aplicativo altera a</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>Propriedade WIA_IPS_XEXTENT para um valor menor</strong>  </span><span class="sxs-lookup"><span data-stu-id="cf985-437"><strong>Example 4: An application changes the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="cf985-438">No exemplo a seguir, um aplicativo altera a propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> para 1000.</span><span class="sxs-lookup"><span data-stu-id="cf985-438">In the following example, an application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to 1000.</span></span> <span data-ttu-id="cf985-439">O minidriver deve assumir que o novo valor contido no <strong>WIA_IPS_XEXTENT</strong> não é mais válido para a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> e, portanto, deve alterar <strong>WIA_DPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="cf985-439">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_DPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="cf985-440">O minidriver também deve ajustar <strong>WIA_DPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf985-440">The minidriver must also adjust <strong>WIA_DPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <span data-ttu-id="cf985-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-442">Não há suporte para essa propriedade no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-442">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="cf985-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-444">Contém a largura da página atual selecionada, em milésimos de polegada.</span><span class="sxs-lookup"><span data-stu-id="cf985-444">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="cf985-445">Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo examinada.</span><span class="sxs-lookup"><span data-stu-id="cf985-445">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="cf985-446">Se as configurações de extensão forem diferentes de tamanhos de página conhecidos, essa propriedade relatará a largura da página cuja propriedade <strong>WIA_DPS_PAGE_SIZE</strong> está definida como WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="cf985-446">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="cf985-447"><strong>WIA_DPS_PAGE_WIDTH</strong> deve estar em sincronia com o valor de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que relata a largura, em pixels, da página a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="cf985-447"><strong>WIA_DPS_PAGE_WIDTH</strong> must be in sync with the value of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="cf985-448">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-448">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-449">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-449">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <span data-ttu-id="cf985-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-451">Não há suporte para essa propriedade no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-451">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="cf985-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-453">Contém o número atual de páginas a serem adquiridas de um alimentador automático de documentos.</span><span class="sxs-lookup"><span data-stu-id="cf985-453">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="cf985-454">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-454">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-455">Tipo: <strong>VT_I4</strong>; Acesso: leitura/gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero pelo número máximo de páginas que o alimentador de documentos pode conter)</span><span class="sxs-lookup"><span data-stu-id="cf985-455">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero through the maximum number of pages that the document feeder can hold)</span></span></p>
<p><span data-ttu-id="cf985-456">Um aplicativo lê essa propriedade para determinar a capacidade da página do alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="cf985-456">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="cf985-457">O aplicativo também define essa propriedade como o número de páginas que ele vai verificar.</span><span class="sxs-lookup"><span data-stu-id="cf985-457">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-458">Se o modo duplex estiver habilitado (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> é definido como alimentador | DUPLEX), <strong>WIA_DPS_PAGES</strong> ainda é igual ao número de páginas a serem verificadas.</span><span class="sxs-lookup"><span data-stu-id="cf985-458">If duplex mode is enabled (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-459">Uma folha de papel conterá automaticamente duas páginas se o DUPLEX estiver habilitado, mesmo se o lado do verso da página estiver em branco.</span><span class="sxs-lookup"><span data-stu-id="cf985-459">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="cf985-460">Definir <strong>WIA_DPS_PAGES</strong> como 1 faz com que um scanner processe um dos lados da página.</span><span class="sxs-lookup"><span data-stu-id="cf985-460">Setting <strong>WIA_DPS_PAGES</strong> to 1 causes a scanner to process one of the sides of the page.</span></span> <span data-ttu-id="cf985-461">É recomendável que, se um scanner não possa verificar apenas um lado de uma página enquanto estiver no modo duplex, o <strong>WIA_DPS_PAGES</strong> valor válido para o membro Inc da estrutura de WIA_PROPERTY_INFO deve ser alterado para 2.</span><span class="sxs-lookup"><span data-stu-id="cf985-461">It is recommended that if a scanner is unable to scan only one side of a page while in duplex mode, the <strong>WIA_DPS_PAGES</strong> valid value for the Inc member of the WIA_PROPERTY_INFO structure should be changed to 2.</span></span> <span data-ttu-id="cf985-462">Esse valor sinaliza ao aplicativo que ele deve solicitar páginas em múltiplos de dois.</span><span class="sxs-lookup"><span data-stu-id="cf985-462">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="cf985-463">Um valor de zero significa que <em>todas as</em> páginas atualmente carregadas no alimentador de documentos serão verificadas.</span><span class="sxs-lookup"><span data-stu-id="cf985-463">A value of zero means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <span data-ttu-id="cf985-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-465">Especifica a cor do cilindro de fundo da planilha a ser examinado.</span><span class="sxs-lookup"><span data-stu-id="cf985-465">Specifies the color of the platen in back of the sheet to be scanned.</span></span> <span data-ttu-id="cf985-466">Essa propriedade é opcional para scanners que têm um cilindro.</span><span class="sxs-lookup"><span data-stu-id="cf985-466">This property is optional for scanners that have a platen.</span></span> <span data-ttu-id="cf985-467">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-467">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-468">Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-468">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-469">O formato das informações de cor é <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-469">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <span data-ttu-id="cf985-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-471">Não há suporte para essa propriedade no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-471">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="cf985-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-473">Indica o modo de visualização de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf985-473">Indicates the preview mode for a device.</span></span> <span data-ttu-id="cf985-474">Um aplicativo define essa propriedade para posicionar o dispositivo em um modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="cf985-474">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="cf985-475">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cf985-475">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cf985-476">A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-476">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-477">Valor</span><span class="sxs-lookup"><span data-stu-id="cf985-477">Value</span></span></th>
<th><span data-ttu-id="cf985-478">Definição</span><span class="sxs-lookup"><span data-stu-id="cf985-478">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-479">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="cf985-479">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="cf985-480">O aplicativo executará uma verificação final.</span><span class="sxs-lookup"><span data-stu-id="cf985-480">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-481">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="cf985-481">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="cf985-482">O aplicativo executará uma verificação de visualização.</span><span class="sxs-lookup"><span data-stu-id="cf985-482">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <span data-ttu-id="cf985-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cf985-484">Contém um valor que indica se o verificador armazenará em cache as páginas em um buffer de scanner antes de enviá-las ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cf985-484">Contains a value that indicates whether the scanner will cache pages in a scanner buffer before sending them to the application.</span></span></p>
<p><span data-ttu-id="cf985-485">Um valor de zero desabilita A verificação antecipada e nenhuma página será verificada antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="cf985-485">A value of zero disables scan ahead and no pages will be scanned ahead.</span></span> <span data-ttu-id="cf985-486">Fazer transferências de dados normais no item varredura em buffer-adiantamento recupera as páginas armazenadas em buffer.</span><span class="sxs-lookup"><span data-stu-id="cf985-486">Doing normal data transfers on the buffered scan-ahead item retrieves the buffered pages.</span></span> <span data-ttu-id="cf985-487">As propriedades WIA não podem ser alteradas durante uma operação de varredura antecipada.</span><span class="sxs-lookup"><span data-stu-id="cf985-487">WIA properties cannot be changed during a scan-ahead operation.</span></span> <span data-ttu-id="cf985-488">Essa propriedade é opcional.</span><span class="sxs-lookup"><span data-stu-id="cf985-488">This property is optional.</span></span></p>
<p><span data-ttu-id="cf985-489">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de zero para o número máximo de páginas que o alimentador de documentos pode conter.</span><span class="sxs-lookup"><span data-stu-id="cf985-489">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <span data-ttu-id="cf985-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-491">Essa propriedade tem suporte apenas pelo Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-491">This property is supported only by Windows 7 and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-492">Indica a fonte de entrada (superfície, alimentador de documentos automático ou adaptador de verificação de FIL) a ser examinada ou o local de armazenamento para o qual transferir dados.</span><span class="sxs-lookup"><span data-stu-id="cf985-492">Indicates the input source (flatbed, automatic document feeder, or fil-scanning adapter) to scan from, or the storage location to transfer data from.</span></span></p>
<p><span data-ttu-id="cf985-493">Um evento de verificação notifica o aplicativo que o usuário iniciou uma verificação, mas o evento não fornece o nome do item WIA que representa a fonte de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf985-493">A scan event notifies the application that the user has initiated a scan, but the event does not supply the name of the WIA item that represents the input source.</span></span> <span data-ttu-id="cf985-494">O manipulador de eventos do aplicativo pode consultar a propriedade WIA_DPS_SCAN_AVAILABLE_ITEM do item raiz para obter o nome do item de origem de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf985-494">The application's event handler can query the root item's WIA_DPS_SCAN_AVAILABLE_ITEM property to get the name of the input source item.</span></span></p>
<p><span data-ttu-id="cf985-495">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de zero para o número máximo de páginas que o alimentador de documentos pode conter.</span><span class="sxs-lookup"><span data-stu-id="cf985-495">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <span data-ttu-id="cf985-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-497">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-497">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-498">Contém a ID de serviço de um dispositivo de scanner de serviços Web.</span><span class="sxs-lookup"><span data-stu-id="cf985-498">Contains the Service ID of a Web Services scanner device.</span></span> <span data-ttu-id="cf985-499">O mini-driver WIA 2,0 cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-499">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-500">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-500">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <span data-ttu-id="cf985-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-502">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-502">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="cf985-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-504">Contém o registro, o alinhamento e a detecção de borda para documentos que são colocados na mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-504">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="cf985-505">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-505">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="cf985-506">Essa propriedade indica como a planilha é posicionada horizontalmente no início da verificação de um scanner de mão ou alimentado por folha.</span><span class="sxs-lookup"><span data-stu-id="cf985-506">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="cf985-507">A propriedade é usada para prever onde o documento é colocado na cabeça de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-507">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="cf985-508">Para os scanners que dão suporte a mais de um cabeçalho de verificação, essa propriedade é relativa ao início da verificação mais alta.</span><span class="sxs-lookup"><span data-stu-id="cf985-508">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="cf985-509">Essa propriedade é obrigatória para scanners de mão, alimentados por folhas e alimentados por folha.</span><span class="sxs-lookup"><span data-stu-id="cf985-509">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="cf985-510">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-510">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-511">A tabela a seguir tem as três constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-511">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-512">Constante</span><span class="sxs-lookup"><span data-stu-id="cf985-512">Constant</span></span></th>
<th><span data-ttu-id="cf985-513">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-513">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-514">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="cf985-514">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="cf985-515">A planilha está posicionada à esquerda em relação ao cabeçalho de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-515">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-516">CENTRA</span><span class="sxs-lookup"><span data-stu-id="cf985-516">CENTERED</span></span></td>
<td><span data-ttu-id="cf985-517">A planilha está centralizada no cabeçalho de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-517">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-518">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="cf985-518">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="cf985-519">A planilha está posicionada à direita em relação ao cabeçalho de verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-519">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <span data-ttu-id="cf985-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-521">Não há suporte para essa propriedade no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf985-521">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="cf985-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-523">Indica se um item precisa de um controle de visualização exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="cf985-523">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="cf985-524">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-524">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-525">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-525">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-526">A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-526">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-527">Constante</span><span class="sxs-lookup"><span data-stu-id="cf985-527">Constant</span></span></th>
<th><span data-ttu-id="cf985-528">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-528">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-529">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="cf985-529">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="cf985-530">Mostrar um controle de visualização para o usuário, pois este dispositivo pode executar uma visualização.</span><span class="sxs-lookup"><span data-stu-id="cf985-530">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="cf985-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="cf985-532">Não mostrar um controle de visualização para o usuário, pois este dispositivo não pode executar uma visualização.</span><span class="sxs-lookup"><span data-stu-id="cf985-532">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <span data-ttu-id="cf985-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-534">Essa propriedade tem suporte apenas pelo Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-534">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-535">Usado pelo serviço WIA para informar ao mini-driver sobre o nome da conta de usuário (incluindo o nome de domínio de rede quando aplicável) da sessão em que o aplicativo WIA atual está em execução.</span><span class="sxs-lookup"><span data-stu-id="cf985-535">Used by the WIA service to inform the mini-driver about the user account name (including the network domain name when applicable) of the session in which the current WIA application is running.</span></span></p>
<p><span data-ttu-id="cf985-536">Essa é uma propriedade de item raiz, gerenciada pelo serviço WIA.</span><span class="sxs-lookup"><span data-stu-id="cf985-536">This is a root item property, managed by the WIA service.</span></span></p>
<p><span data-ttu-id="cf985-537">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-537">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <span data-ttu-id="cf985-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-539">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-539">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-540">Contém o registro, o alinhamento vertical e a detecção de borda para documentos colocados na mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-540">Contains the registration, or vertical alignment and edge detection, for documents placed on the flatbed.</span></span> <span data-ttu-id="cf985-541">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-541">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cf985-542">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-542">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cf985-543">A tabela a seguir tem as três constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-543">The following table has the three constants that are valid with this property..</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf985-544">Constante</span><span class="sxs-lookup"><span data-stu-id="cf985-544">Constant</span></span></th>
<th><span data-ttu-id="cf985-545">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf985-545">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf985-546">TOP_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="cf985-546">TOP_JUSTIFIED</span></span></td>
<td><span data-ttu-id="cf985-547">O papel é justificado pela parte principal.</span><span class="sxs-lookup"><span data-stu-id="cf985-547">The paper is top justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf985-548">CENTRA</span><span class="sxs-lookup"><span data-stu-id="cf985-548">CENTERED</span></span></td>
<td><span data-ttu-id="cf985-549">O papel está centralizado.</span><span class="sxs-lookup"><span data-stu-id="cf985-549">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf985-550">BOTTOM_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="cf985-550">BOTTOM_JUSTIFIED</span></span></td>
<td><span data-ttu-id="cf985-551">O papel é justificado por baixo.</span><span class="sxs-lookup"><span data-stu-id="cf985-551">The paper is bottom justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cf985-552"><strong>Consulte também</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf985-552"><strong>See Also</strong>.</span></span></p>
<p><span data-ttu-id="cf985-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="cf985-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <span data-ttu-id="cf985-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-555">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-555">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="cf985-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-557">Especifica a altura máxima, em milésimos de polegada, que é verificada no eixo vertical (Y) do cilindro de um scanner de mesa na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="cf985-557">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="cf985-558">Essa propriedade também se aplica a alimentadores automáticos de documentos, que movem planilhas para o cilindro de um scanner de mesa para verificação.</span><span class="sxs-lookup"><span data-stu-id="cf985-558">This property also applies to automatic document feeders, that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="cf985-559">Essa propriedade é obrigatória para scanners que têm um cilindro.</span><span class="sxs-lookup"><span data-stu-id="cf985-559">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="cf985-560">Em vez disso, outros tipos de scanner implementarão a propriedade <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="cf985-560">Other scanner types will instead implement the <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="cf985-561">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="cf985-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cf985-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cf985-563">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf985-563">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="cf985-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf985-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cf985-565">Especifica a altura máxima, em milésimos de polegada, que é verificada no eixo vertical (Y) de um scanner de alimentação de papel ou portátil na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="cf985-565">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="cf985-566">Essa propriedade também se aplica a alimentadores de documentos automáticos que examinam sem mover folhas para o cilindro de um scanner de mesa.</span><span class="sxs-lookup"><span data-stu-id="cf985-566">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="cf985-567">Essa propriedade é obrigatória para scanners alimentados por folha.</span><span class="sxs-lookup"><span data-stu-id="cf985-567">This property is mandatory for sheet-fed scanners.</span></span> <span data-ttu-id="cf985-568">Os scanners de rolagem e de bolso não devem implementar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf985-568">Scroll-fed and hand-held scanners should not implement this property.</span></span></p>
<p><span data-ttu-id="cf985-569">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cf985-569">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="cf985-570">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf985-570">Requirements</span></span>



| <span data-ttu-id="cf985-571">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf985-571">Requirement</span></span> | <span data-ttu-id="cf985-572">Valor</span><span class="sxs-lookup"><span data-stu-id="cf985-572">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cf985-573">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf985-573">Minimum supported client</span></span><br/> | <span data-ttu-id="cf985-574">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cf985-574">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="cf985-575">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf985-575">Minimum supported server</span></span><br/> | <span data-ttu-id="cf985-576">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf985-576">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cf985-577">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf985-577">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf985-578"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf985-578"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
