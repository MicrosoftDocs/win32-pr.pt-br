---
description: Além das propriedades de informações do dispositivo, os dispositivos de aquisição de imagem do Windows (WIA) têm valores de propriedade armazenados no registro que os aplicativos lêem e gravam.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Constantes de propriedade de dispositivo comum (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501771"
---
# <a name="common-device-property-constants"></a><span data-ttu-id="671e6-103">Constantes de propriedade de dispositivo comum</span><span class="sxs-lookup"><span data-stu-id="671e6-103">Common Device Property Constants</span></span>

<span data-ttu-id="671e6-104">Além das propriedades de informações do dispositivo, os dispositivos de aquisição de imagem do Windows (WIA) têm valores de propriedade armazenados no registro que os aplicativos lêem e gravam.</span><span class="sxs-lookup"><span data-stu-id="671e6-104">In addition to device information properties, Windows Image Acquisition (WIA) devices have property values stored in the registry that applications read and write.</span></span> <span data-ttu-id="671e6-105">Eles estão associados ao objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou ao objeto [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="671e6-105">They are associated with the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object or [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <span data-ttu-id="671e6-106">As propriedades do dispositivo representam informações do dispositivo, como o status da conexão e a hora do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="671e6-106">Device properties represent device information such as connection status and device time.</span></span> <span data-ttu-id="671e6-107">Cada propriedade de dispositivo tem uma cadeia de caracteres de propriedade de dispositivo associada.</span><span class="sxs-lookup"><span data-stu-id="671e6-107">Each device property has an associated device property string.</span></span>

<span data-ttu-id="671e6-108">As constantes de propriedade de dispositivo listadas aqui são comuns à maioria ou a todos os dispositivos de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="671e6-108">The Device Property Constants listed here are common to most or all WIA hardware devices.</span></span>

<span data-ttu-id="671e6-109">O prefixo "WIA \_ DPA \_ " indica uma propriedade de dispositivo para todos os dispositivos e é a Convenção de nomenclatura usada em C/C++.</span><span class="sxs-lookup"><span data-stu-id="671e6-109">The prefix "WIA\_DPA\_" indicates a Device Property for All devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="671e6-110">Para fins de script, essas constantes usam o prefixo "Device" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="671e6-110">For scripting purposes these constants use the prefix "Device" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="671e6-111">O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="671e6-111">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="671e6-112">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="671e6-112">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="671e6-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="671e6-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <span data-ttu-id="671e6-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="671e6-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="671e6-115">O status de conexão atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="671e6-115">The current connection status for the device.</span></span> <span data-ttu-id="671e6-116">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="671e6-116">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="671e6-117">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="671e6-117">Type: <strong>VT_I4</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="671e6-118">A propriedade pode ter os seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="671e6-118">The property can have the following possible values.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="671e6-119">Status de conexão</span><span class="sxs-lookup"><span data-stu-id="671e6-119">Connect Status</span></span></th>
<th><span data-ttu-id="671e6-120">Definição</span><span class="sxs-lookup"><span data-stu-id="671e6-120">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="671e6-121">WIA_DEVICE_NOT_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="671e6-121">WIA_DEVICE_NOT_CONNECTED</span></span></td>
<td><span data-ttu-id="671e6-122">O dispositivo não está conectado.</span><span class="sxs-lookup"><span data-stu-id="671e6-122">Device is not connected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="671e6-123">WIA_DEVICE_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="671e6-123">WIA_DEVICE_CONNECTED</span></span></td>
<td><span data-ttu-id="671e6-124">O dispositivo está conectado e operacional.</span><span class="sxs-lookup"><span data-stu-id="671e6-124">Device is connected and operational.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <span data-ttu-id="671e6-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span><span class="sxs-lookup"><span data-stu-id="671e6-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="671e6-126">A hora do relógio atual que está armazenada no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="671e6-126">The current clock time that is stored on the device.</span></span> <span data-ttu-id="671e6-127">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="671e6-127">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="671e6-128">Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="671e6-128">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong>, Access: Read/Write or Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="671e6-129">Essa propriedade tem suporte apenas em dispositivos que têm um relógio interno.</span><span class="sxs-lookup"><span data-stu-id="671e6-129">This property is supported only by devices that have an internal clock.</span></span> <span data-ttu-id="671e6-130">Se o relógio do dispositivo puder ser definido, essa propriedade será leitura/gravação; caso contrário, ele será somente leitura.</span><span class="sxs-lookup"><span data-stu-id="671e6-130">If the device clock can be set, this property is Read/Write; otherwise, it is Read-only.</span></span></p>
<p><span data-ttu-id="671e6-131">Os dispositivos WIA relatam o tempo em uma estrutura <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> .</span><span class="sxs-lookup"><span data-stu-id="671e6-131">WIA devices report time in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <span data-ttu-id="671e6-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="671e6-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="671e6-133">A versão do firmware do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="671e6-133">The device firmware version.</span></span> <span data-ttu-id="671e6-134">Esse valor deve ser um valor de cadeia de caracteres, como &quot; 1.0.4 &quot; ou &quot; 1.0 ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="671e6-134">This value must be a string value, such as &quot;1.0.4&quot; or &quot;1.0abc&quot;.</span></span> <span data-ttu-id="671e6-135">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="671e6-135">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="671e6-136">Se o minidriver WIA não fornecer um recurso de versão, o serviço WIA fornecerá o valor &quot; 0.0.0.0 &quot; como padrão.</span><span class="sxs-lookup"><span data-stu-id="671e6-136">If the WIA minidriver does not supply a version resource, the WIA service supplies the value &quot;0.0.0.0&quot; as a default.</span></span> <span data-ttu-id="671e6-137">Um aplicativo lê essa propriedade para determinar a versão da DLL minidriver do WIA.</span><span class="sxs-lookup"><span data-stu-id="671e6-137">An application reads this property to determine the version of the WIA minidriver DLL.</span></span></p>
<p><span data-ttu-id="671e6-138">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="671e6-138">Type: <strong>VT_BSTR</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="671e6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671e6-139">Requirements</span></span>



| <span data-ttu-id="671e6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="671e6-140">Requirement</span></span> | <span data-ttu-id="671e6-141">Valor</span><span class="sxs-lookup"><span data-stu-id="671e6-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="671e6-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="671e6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="671e6-143">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="671e6-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="671e6-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="671e6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="671e6-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="671e6-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="671e6-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="671e6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="671e6-147"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="671e6-147"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
