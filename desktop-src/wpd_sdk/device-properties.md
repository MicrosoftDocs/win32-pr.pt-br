---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de dispositivo.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Propriedades do dispositivo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 696d5fefd65d194f9bb451b0095ed87b90f8a22c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754466"
---
# <a name="device-properties-portabledeviceh"></a><span data-ttu-id="91a69-103">Propriedades do dispositivo (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="91a69-103">Device Properties (PortableDevice.h)</span></span>

<span data-ttu-id="91a69-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-104">Windows Portable Devices supports the following device properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="91a69-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="91a69-105">Property</span></span></th>
<th><span data-ttu-id="91a69-106">VarType</span><span class="sxs-lookup"><span data-stu-id="91a69-106">VarType</span></span></th>
<th><span data-ttu-id="91a69-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="91a69-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91a69-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span></span></td>
<td><span data-ttu-id="91a69-109"><strong>VT_DATE</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-109"><strong>VT_DATE</strong></span></span></td>
<td><span data-ttu-id="91a69-110">A data e a hora atuais no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-110">The current date and time on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span></span></td>
<td><span data-ttu-id="91a69-112"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-112"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="91a69-113">A versão do firmware do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-113">The device's firmware version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="91a69-115"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-115"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="91a69-116">Um identificador exclusivo de 16 bytes que é comum em vários transportes com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-116">A unique 16-byte identifier that is common across multiple transports supported by the device.</span></span> <span data-ttu-id="91a69-117">Se um único dispositivo der suporte a vários transportes, essa propriedade poderá ser usada para associar os vários drivers de transporte WPD ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-117">If a single device supports multiple transports, this property may be used to associate the various transport WPD drivers with that device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span></span></td>
<td><span data-ttu-id="91a69-119"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-119"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="91a69-120">Um nome de fabricante de dispositivo legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="91a69-120">A human-readable device manufacturer name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span></span></td>
<td><span data-ttu-id="91a69-122"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-122"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="91a69-123">O modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-123">The device model.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="91a69-125"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-125"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="91a69-126">Um identificador exclusivo de 16 bytes usado para diferenciar entre diferentes modelos de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-126">A unique 16-byte identifier used to differentiate among different models of a device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span></span></td>
<td><span data-ttu-id="91a69-128"><strong>VT_UI8</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-128"><strong>VT_UI8</strong></span></span></td>
<td><span data-ttu-id="91a69-129">Um valor que especifica o identificador de rede EUI-64 do dispositivo; Essa propriedade é usada para operações de rede fora de banda. Se o dispositivo tiver endereços de rede física MAC-48 (típicos de redes IPv4), o endereço MAC-48 será codificado no endereço EUI-64 como as duas metades do endereço MAC-48 separados por FF-FF.</span><span class="sxs-lookup"><span data-stu-id="91a69-129">A value that specifies the EUI-64 network identifier of the device; this property is used for out-of-band network operations.If the device has MAC-48 physical network addresses (typical of IPv4 networks), the MAC-48 address is encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span> <span data-ttu-id="91a69-130">O valor de EUI-64 é armazenado &quot; em &quot; uma rede ou em &quot; uma ordem big-endian &quot; , em que um endereço EUI-64 de 01-02-03-ff-FF-04-05-06 seria colocado no VT_UI8 de modo que o valor decimal seja 72624942021346566.</span><span class="sxs-lookup"><span data-stu-id="91a69-130">The EUI-64 value is stored in &quot;network&quot; or &quot;big-endian&quot; order, where an EUI-64 address of 01-02-03-FF-FF-04-05-06 would be placed in the VT_UI8 such that the decimal value is 72624942021346566.</span></span> <span data-ttu-id="91a69-131">Essa propriedade é necessária em qualquer dispositivo que dê suporte à autenticação nominal ou segura.</span><span class="sxs-lookup"><span data-stu-id="91a69-131">This property is required on any device that supports Nominal or Secure Authentication.</span></span> <span data-ttu-id="91a69-132">Essa propriedade é recomendada em dispositivos que dão suporte apenas à autenticação zero.</span><span class="sxs-lookup"><span data-stu-id="91a69-132">This property is recommended on devices that support only Zero Authentication.</span></span> <span data-ttu-id="91a69-133">O valor pode ser usado pelo host para estabelecer automaticamente o acesso ao dispositivo sem a intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="91a69-133">The value can be used by the host to automatically establish access to the device without user intervention.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span></span></td>
<td><span data-ttu-id="91a69-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="91a69-136">Um valor de 0 a 100 que especifica o nível de energia da bateria do dispositivo, com 0 sendo nenhum e 100 sendo totalmente cobrado.</span><span class="sxs-lookup"><span data-stu-id="91a69-136">A value from 0 to 100 that specifies the power level of the device's battery, with 0 being none, and 100 being fully charged.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span></span></td>
<td><span data-ttu-id="91a69-138">VT_UI4</span><span class="sxs-lookup"><span data-stu-id="91a69-138">VT_UI4</span></span></td>
<td><span data-ttu-id="91a69-139">Uma enumeração <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> que especifica a fonte de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-139">A <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> enumeration that specifies the power source of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span></span></td>
<td><span data-ttu-id="91a69-141"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-141"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="91a69-142">O protocolo de dispositivo que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="91a69-142">The device protocol that is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span></span></td>
<td><span data-ttu-id="91a69-144"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-144"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="91a69-145">Número de série do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-145">The device's serial number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span></span></td>
<td><span data-ttu-id="91a69-147"><strong>VT_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-147"><strong>VT_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="91a69-148">Um valor que especifica se os formatos com suporte retornados do dispositivo estão em uma ordem preferida.</span><span class="sxs-lookup"><span data-stu-id="91a69-148">A value that specifies whether the supported formats returned from the device are in a preferred order.</span></span> <span data-ttu-id="91a69-149">O primeiro formato na lista é mais preferencial pelo dispositivo, enquanto o último é o menos preferencial. Os aplicativos podem usar essa propriedade para determinar se os formatos com suporte do dispositivo estão listados em uma ordem preferida.</span><span class="sxs-lookup"><span data-stu-id="91a69-149">The first format in the list is most preferred by the device, while the last is the least preferred.Applications may use this property to determine whether a device's supported formats are listed in a preferred order.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span></span></td>
<td><span data-ttu-id="91a69-151"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-151"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="91a69-152">Um valor booliano que especifica se os formatos com suporte retornados do dispositivo estão em uma ordem preferida; ou seja, o primeiro formato retornado é mais preferencial, enquanto o último formato retornado é o menos preferencial.</span><span class="sxs-lookup"><span data-stu-id="91a69-152">A Boolean value that specifies whether the supported formats returned from the device are in a preferred order; that is, the first returned format is most preferred while the last returned format is least preferred.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span></span></td>
<td><span data-ttu-id="91a69-154"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-154"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="91a69-155">Um valor booliano que especifica se o dispositivo dá suporte a objetos não consumíveis.</span><span class="sxs-lookup"><span data-stu-id="91a69-155">A Boolean value that specifies whether the device supports non-consumable objects.</span></span> <span data-ttu-id="91a69-156">Esses são objetos que o dispositivo destina-se apenas a armazenar, não reproduzir ou usar de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="91a69-156">These are objects that the device is only meant to store, not play or use in any way.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span></span></td>
<td><span data-ttu-id="91a69-158"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-158"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="91a69-159">Uma descrição legível do <em>parceiro de sincronização</em>de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-159">A human-readable description of a device's <em>synchronization partner</em>.</span></span> <span data-ttu-id="91a69-160">Este é um dispositivo, aplicativo ou servidor com o qual o dispositivo se comunica para manter um Estado comum ou grupo de arquivos entre ambos os parceiros.</span><span class="sxs-lookup"><span data-stu-id="91a69-160">This is a device, application, or server that the device communicates with to maintain a common state or group of files between both partners.</span></span> <span data-ttu-id="91a69-161">Os exemplos incluem programas de email e bibliotecas de música.</span><span class="sxs-lookup"><span data-stu-id="91a69-161">Examples include e-mail programs and music libraries.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span></span></td>
<td><span data-ttu-id="91a69-163"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-163"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="91a69-164">Um valor que representa o nome amigável definido pelo usuário no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-164">A value that represents the friendly name set by the user on the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span></span></td>
<td><span data-ttu-id="91a69-166"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-166"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="91a69-167">o transporte com suporte do dispositivo, como USB, IP ou Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="91a69-167">the transport supported by the device, such as USB, IP, or Bluetooth.</span></span> <span data-ttu-id="91a69-168">Os valores válidos são do tipo de enumeração <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="91a69-168">Valid values are of the <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> enumeration type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a69-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span></span></td>
<td><span data-ttu-id="91a69-170"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-170"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="91a69-171">Um valor que especifica o tipo de dispositivo; os aplicativos usam essa propriedade apenas para fins de representação.</span><span class="sxs-lookup"><span data-stu-id="91a69-171">A value that specifies the device type; applications use this property for representation purposes only.</span></span> <span data-ttu-id="91a69-172">As características funcionais do dispositivo são decididas por meio de objetos funcionais. Os dispositivos que não fornecem um ícone de dispositivo, por exemplo, um <strong>WPD_RESOURCE_ICON</strong> para o objeto de dispositivo, serão representados no namespace WPD com um ícone genérico.</span><span class="sxs-lookup"><span data-stu-id="91a69-172">Functional characteristics of the device are decided through functional objects.Devices that do not supply a device icon, for example, a <strong>WPD_RESOURCE_ICON</strong> for the device object, will be represented in the WPD Namespace with a generic icon.</span></span> <span data-ttu-id="91a69-173">Esse ícone dependerá do tipo de dispositivo especificado, por exemplo, se o tipo de dispositivo for um celular, o ícone de telefone genérico será usado.</span><span class="sxs-lookup"><span data-stu-id="91a69-173">This icon will depend on the specified device type, for example, if the device type is a mobile phone, the generic phone icon is used.</span></span> <span data-ttu-id="91a69-174">Na primeira instalação do dispositivo, o instalador da classe WPD consultará esse valor de propriedade e o armazenará no registro do dispositivo sob o valor de PORTABLE_DEVICE_TYPE como um REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="91a69-174">On first install of the device, the WPD Class Installer will query this property value and store it in the device registry under the PORTABLE_DEVICE_TYPE value as a REG_DWORD.</span></span><br/> <span data-ttu-id="91a69-175">Os valores possíveis desse parâmetro são da enumeração <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> definida em PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="91a69-175">This parameter's possible values are from the <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="91a69-176">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="91a69-176">Values are:</span></span><br/> <dl> <span data-ttu-id="91a69-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span></span><br /><span data-ttu-id="91a69-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span></span><br /><span data-ttu-id="91a69-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span></span><br /><span data-ttu-id="91a69-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span></span><br /><span data-ttu-id="91a69-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span></span><br /><span data-ttu-id="91a69-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span></span><br /><span data-ttu-id="91a69-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a69-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span></span></td>
<td><span data-ttu-id="91a69-185"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="91a69-185"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="91a69-186">Se essa propriedade existir e for definida como <strong>true</strong>, o dispositivo poderá ser usado com o estágio do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91a69-186">If this property exists and is set to <strong>TRUE</strong>, the device can be used with Device Stage .</span></span> <span data-ttu-id="91a69-187">Isso é destinado a dispositivos que não podem armazenar metadados usando o <strong>serviço de metadados do dispositivo</strong>, mas fornecerão metadados nos servidores da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91a69-187">This is meant for devices that cannot store metadata using the <strong>Device Metadata Service</strong>, but will provide metadata on the Microsoft servers.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="91a69-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91a69-188">Requirements</span></span>



| <span data-ttu-id="91a69-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a69-189">Requirement</span></span> | <span data-ttu-id="91a69-190">Valor</span><span class="sxs-lookup"><span data-stu-id="91a69-190">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="91a69-191">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91a69-191">Header</span></span><br/> | <dl> <span data-ttu-id="91a69-192"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a69-192"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91a69-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="91a69-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a69-194">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="91a69-194">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




