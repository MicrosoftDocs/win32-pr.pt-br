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
# <a name="device-properties-portabledeviceh"></a>Propriedades do dispositivo (PortableDevice. h)

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de dispositivo.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>VarType</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></td>
<td><strong>VT_DATE</strong></td>
<td>A data e a hora atuais no dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>A versão do firmware do dispositivo.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Um identificador exclusivo de 16 bytes que é comum em vários transportes com suporte do dispositivo. Se um único dispositivo der suporte a vários transportes, essa propriedade poderá ser usada para associar os vários drivers de transporte WPD ao dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Um nome de fabricante de dispositivo legível por humanos.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>O modelo do dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Um identificador exclusivo de 16 bytes usado para diferenciar entre diferentes modelos de um dispositivo.</td>
</tr>
<tr class="odd">
<td><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></td>
<td><strong>VT_UI8</strong></td>
<td>Um valor que especifica o identificador de rede EUI-64 do dispositivo; Essa propriedade é usada para operações de rede fora de banda. Se o dispositivo tiver endereços de rede física MAC-48 (típicos de redes IPv4), o endereço MAC-48 será codificado no endereço EUI-64 como as duas metades do endereço MAC-48 separados por FF-FF. O valor de EUI-64 é armazenado &quot; em &quot; uma rede ou em &quot; uma ordem big-endian &quot; , em que um endereço EUI-64 de 01-02-03-ff-FF-04-05-06 seria colocado no VT_UI8 de modo que o valor decimal seja 72624942021346566. Essa propriedade é necessária em qualquer dispositivo que dê suporte à autenticação nominal ou segura. Essa propriedade é recomendada em dispositivos que dão suporte apenas à autenticação zero. O valor pode ser usado pelo host para estabelecer automaticamente o acesso ao dispositivo sem a intervenção do usuário.<br/></td>
</tr>
<tr class="even">
<td><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Um valor de 0 a 100 que especifica o nível de energia da bateria do dispositivo, com 0 sendo nenhum e 100 sendo totalmente cobrado.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></td>
<td>VT_UI4</td>
<td>Uma enumeração <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> que especifica a fonte de energia do dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>O protocolo de dispositivo que está sendo usado.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Número de série do dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></td>
<td><strong>VT_UNKNOWN</strong></td>
<td>Um valor que especifica se os formatos com suporte retornados do dispositivo estão em uma ordem preferida. O primeiro formato na lista é mais preferencial pelo dispositivo, enquanto o último é o menos preferencial. Os aplicativos podem usar essa propriedade para determinar se os formatos com suporte do dispositivo estão listados em uma ordem preferida.<br/></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Um valor booliano que especifica se os formatos com suporte retornados do dispositivo estão em uma ordem preferida; ou seja, o primeiro formato retornado é mais preferencial, enquanto o último formato retornado é o menos preferencial.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Um valor booliano que especifica se o dispositivo dá suporte a objetos não consumíveis. Esses são objetos que o dispositivo destina-se apenas a armazenar, não reproduzir ou usar de qualquer forma.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Uma descrição legível do <em>parceiro de sincronização</em>de um dispositivo. Este é um dispositivo, aplicativo ou servidor com o qual o dispositivo se comunica para manter um Estado comum ou grupo de arquivos entre ambos os parceiros. Os exemplos incluem programas de email e bibliotecas de música.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Um valor que representa o nome amigável definido pelo usuário no dispositivo.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></td>
<td><strong>VT_UI4</strong></td>
<td>o transporte com suporte do dispositivo, como USB, IP ou Bluetooth. Os valores válidos são do tipo de enumeração <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</td>
</tr>
<tr class="even">
<td><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Um valor que especifica o tipo de dispositivo; os aplicativos usam essa propriedade apenas para fins de representação. As características funcionais do dispositivo são decididas por meio de objetos funcionais. Os dispositivos que não fornecem um ícone de dispositivo, por exemplo, um <strong>WPD_RESOURCE_ICON</strong> para o objeto de dispositivo, serão representados no namespace WPD com um ícone genérico. Esse ícone dependerá do tipo de dispositivo especificado, por exemplo, se o tipo de dispositivo for um celular, o ícone de telefone genérico será usado. Na primeira instalação do dispositivo, o instalador da classe WPD consultará esse valor de propriedade e o armazenará no registro do dispositivo sob o valor de PORTABLE_DEVICE_TYPE como um REG_DWORD.<br/> Os valores possíveis desse parâmetro são da enumeração <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> definida em PortableDevice. h. Os valores são:<br/> <dl> <strong>WPD_DEVICE_TYPE_GENERIC</strong><br />
<strong>WPD_DEVICE_TYPE_CAMERA</strong><br />
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong><br />
<strong>WPD_DEVICE_TYPE_PHONE</strong><br />
<strong>WPD_DEVICE_TYPE_VIDEO</strong><br />
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong><br />
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Se essa propriedade existir e for definida como <strong>true</strong>, o dispositivo poderá ser usado com o estágio do dispositivo. Isso é destinado a dispositivos que não podem armazenar metadados usando o <strong>serviço de metadados do dispositivo</strong>, mas fornecerão metadados nos servidores da Microsoft.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




