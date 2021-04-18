---
description: Propriedades de informações do dispositivo são propriedades que descrevem a instalação e a instalação do dispositivo.
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Constantes da propriedade de informações do dispositivo (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 18c44bb310c2dcee5bb227e0885a71b58f5b362e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793854"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="d694d-103">Constantes da propriedade de informações do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d694d-103">Device Information Property Constants</span></span>

<span data-ttu-id="d694d-104">Propriedades de informações do dispositivo são propriedades que descrevem a instalação e a instalação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="d694d-105">Essas propriedades estão disponíveis por meio das interfaces [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) e também por meio do item raiz.</span><span class="sxs-lookup"><span data-stu-id="d694d-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="d694d-106">As propriedades de informações do dispositivo são prefixadas com "WIA \_ DIP \_ " (Propriedade de informações do dispositivo) e são fornecidas pela aquisição de imagem do Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="d694d-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="d694d-107">Para fins de script, essas constantes usam o prefixo "DeviceInfo" e fazem parte do tipo enumerado [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="d694d-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="d694d-108">O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="d694d-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d694d-109">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="d694d-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d694d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d694d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="d694d-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d694d-112">A cadeia de caracteres de ID do dispositivo para o minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="d694d-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="d694d-113">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="d694d-114">Tipo: VT_BSTR, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="d694d-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d694d-116">A cadeia de caracteres de descrição do fornecedor para o minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="d694d-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="d694d-117">A descrição do fornecedor é obtida do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="d694d-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="d694d-118">Um aplicativo lê essa propriedade para obter uma descrição do fornecedor do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="d694d-119">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="d694d-120">Tipo: VT_BSTR, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="d694d-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d694d-122">A cadeia de caracteres de descrição do dispositivo para o minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="d694d-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="d694d-123">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-124">A cadeia de caracteres de descrição do dispositivo que esta propriedade contém é obtida do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="d694d-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="d694d-125">Um aplicativo lê essa propriedade para obter uma descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="d694d-126">Tipo: VT_BSTR, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="d694d-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d694d-128">O tipo de dispositivo e o subtipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-128">The device type and device subtype.</span></span> <span data-ttu-id="d694d-129">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-130">Use a macro GET_STIDEVICE_TYPE para obter o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="d694d-131">O tipo e subtipo de dispositivo são obtidos do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="d694d-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="d694d-132">Um aplicativo lê essa propriedade para determinar se está usando um scanner, câmera ou dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d694d-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="d694d-133">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="d694d-134">Atualmente, os tipos de dispositivo são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="d694d-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="d694d-135">O asterisco \* indica que o tipo de dispositivo não tem suporte no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="d694d-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="d694d-136">O asterisco duplo \* \* indica que o tipo de dispositivo não é suportado pelo Windows Server 2003, Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d694d-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d694d-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="d694d-137">Type</span></span></th>
<th><span data-ttu-id="d694d-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d694d-138">Value</span></span></th>
<th><span data-ttu-id="d694d-139">Definição</span><span class="sxs-lookup"><span data-stu-id="d694d-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d694d-140">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="d694d-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="d694d-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="d694d-141">0x0000</span></span></td>
<td><span data-ttu-id="d694d-142">Dispositivo padrão</span><span class="sxs-lookup"><span data-stu-id="d694d-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d694d-143">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="d694d-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="d694d-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="d694d-144">0x0001</span></span></td>
<td><span data-ttu-id="d694d-145">Dispositivo de scanner (consulte a <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> para determinar se o scanner é alimentado por folhas ou de mesa.)</span><span class="sxs-lookup"><span data-stu-id="d694d-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d694d-146">StiDeviceTypeDigitalCamera\*</span><span class="sxs-lookup"><span data-stu-id="d694d-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="d694d-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="d694d-147">0x0002</span></span></td>
<td><span data-ttu-id="d694d-148">Dispositivo de câmera</span><span class="sxs-lookup"><span data-stu-id="d694d-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d694d-149">StiDeviceTypeStreamingVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="d694d-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="d694d-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="d694d-150">0x0003</span></span></td>
<td><span data-ttu-id="d694d-151">Dispositivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="d694d-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="d694d-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-153">O nome da porta do dispositivo instalado, que é atribuído pelo driver de modo kernel que opera o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="d694d-154">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-155">Um aplicativo lê essa propriedade para determinar o nome da porta.</span><span class="sxs-lookup"><span data-stu-id="d694d-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="d694d-156">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="d694d-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-158">O nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-158">The name of the device.</span></span> <span data-ttu-id="d694d-159">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-160">O nome do dispositivo contido nessa propriedade é obtido do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="d694d-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="d694d-161">Um aplicativo lê essa propriedade para obter o nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="d694d-162">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="d694d-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-164">O nome do servidor no qual o minidriver WIA está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="d694d-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="d694d-165">Essa propriedade é opcional para o Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="d694d-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="d694d-166">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="d694d-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-168">A ID do dispositivo WIA que está instalado em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d694d-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="d694d-169">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-170">Ele é usado apenas internamente pelo serviço WIA.</span><span class="sxs-lookup"><span data-stu-id="d694d-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="d694d-171">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="d694d-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-173">O CLSID fornecido pelo fornecedor para qualquer objeto COM de extensão de interface do usuário que é instalado com o minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="d694d-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="d694d-174">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-175">O valor CLSID da interface do usuário contido nesta propriedade é obtido do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="d694d-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="d694d-176">Se nenhum CLSID de interface do usuário for especificado, o serviço WIA fornecerá um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="d694d-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="d694d-177">Essa propriedade só é usada internamente pelo serviço WIA quando a interface do usuário está sendo exibida.</span><span class="sxs-lookup"><span data-stu-id="d694d-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="d694d-178">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="d694d-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-180">O tipo de conexão que o dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="d694d-180">The type of connection that the device is using.</span></span> <span data-ttu-id="d694d-181">O serviço WIA cria e mantém essa propriedade, e somente o serviço WIA pode alterá-la.</span><span class="sxs-lookup"><span data-stu-id="d694d-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="d694d-182">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="d694d-183">A propriedade pode ter os seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="d694d-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d694d-184">Valor</span><span class="sxs-lookup"><span data-stu-id="d694d-184">Value</span></span></th>
<th><span data-ttu-id="d694d-185">Definição</span><span class="sxs-lookup"><span data-stu-id="d694d-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d694d-186">1</span><span class="sxs-lookup"><span data-stu-id="d694d-186">1</span></span></td>
<td><span data-ttu-id="d694d-187">Dispositivo WDM genérico</span><span class="sxs-lookup"><span data-stu-id="d694d-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d694d-188">2</span><span class="sxs-lookup"><span data-stu-id="d694d-188">2</span></span></td>
<td><span data-ttu-id="d694d-189">Dispositivo SCSI</span><span class="sxs-lookup"><span data-stu-id="d694d-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d694d-190">4</span><span class="sxs-lookup"><span data-stu-id="d694d-190">4</span></span></td>
<td><span data-ttu-id="d694d-191">Dispositivo USB</span><span class="sxs-lookup"><span data-stu-id="d694d-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d694d-192">8</span><span class="sxs-lookup"><span data-stu-id="d694d-192">8</span></span></td>
<td><span data-ttu-id="d694d-193">Dispositivo serial</span><span class="sxs-lookup"><span data-stu-id="d694d-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d694d-194">16</span><span class="sxs-lookup"><span data-stu-id="d694d-194">16</span></span></td>
<td><span data-ttu-id="d694d-195">Dispositivo paralelo</span><span class="sxs-lookup"><span data-stu-id="d694d-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="d694d-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-197">A configuração da taxa de transmissão atual para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="d694d-198">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-199">O valor deve estar &quot; vazio &quot; se o dispositivo não estiver conectado por um cabo serial.</span><span class="sxs-lookup"><span data-stu-id="d694d-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="d694d-200">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="d694d-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-202">Os recursos de STI genéricos para o dispositivo, conforme obtido do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="d694d-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="d694d-203">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-204">Um aplicativo lê essa propriedade para determinar os recursos de STI genéricos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="d694d-205">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="d694d-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-207">O número (como uma cadeia de caracteres) da versão atual do WIA que está instalada no sistema.</span><span class="sxs-lookup"><span data-stu-id="d694d-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="d694d-208">Um aplicativo lê essa propriedade para determinar a versão do WIA que está instalada no sistema.</span><span class="sxs-lookup"><span data-stu-id="d694d-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="d694d-209">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-210">Essa propriedade está disponível no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d694d-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="d694d-211">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="d694d-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-213">A versão atual da DLL do minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="d694d-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="d694d-214">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-215">Essa propriedade está disponível no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d694d-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="d694d-216">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="d694d-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-218">A ID de PnP atual para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d694d-218">The current PnP id for the device.</span></span> <span data-ttu-id="d694d-219">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-220">Essa propriedade está disponível no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d694d-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="d694d-221">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="d694d-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="d694d-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="d694d-223">A versão do Driver STI genérico.</span><span class="sxs-lookup"><span data-stu-id="d694d-223">The generic STI driver version.</span></span> <span data-ttu-id="d694d-224">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d694d-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="d694d-225">Um aplicativo lê essa propriedade para determinar a versão do Driver STI genérico.</span><span class="sxs-lookup"><span data-stu-id="d694d-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="d694d-226">Essa propriedade está disponível no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d694d-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="d694d-227">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="d694d-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="d694d-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d694d-228">Requirements</span></span>



| <span data-ttu-id="d694d-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="d694d-229">Requirement</span></span> | <span data-ttu-id="d694d-230">Valor</span><span class="sxs-lookup"><span data-stu-id="d694d-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d694d-231">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d694d-231">Minimum supported client</span></span><br/> | <span data-ttu-id="d694d-232">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d694d-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d694d-233">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d694d-233">Minimum supported server</span></span><br/> | <span data-ttu-id="d694d-234">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d694d-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d694d-235">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d694d-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="d694d-236"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="d694d-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




