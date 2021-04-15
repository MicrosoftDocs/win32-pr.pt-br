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
# <a name="common-device-property-constants"></a>Constantes de propriedade de dispositivo comum

Além das propriedades de informações do dispositivo, os dispositivos de aquisição de imagem do Windows (WIA) têm valores de propriedade armazenados no registro que os aplicativos lêem e gravam. Eles estão associados ao objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou ao objeto [**IWiaItem2**](-wia-iwiaitem2.md) . As propriedades do dispositivo representam informações do dispositivo, como o status da conexão e a hora do dispositivo. Cada propriedade de dispositivo tem uma cadeia de caracteres de propriedade de dispositivo associada.

As constantes de propriedade de dispositivo listadas aqui são comuns à maioria ou a todos os dispositivos de hardware WIA.

O prefixo "WIA \_ DPA \_ " indica uma propriedade de dispositivo para todos os dispositivos e é a Convenção de nomenclatura usada em C/C++. Para fins de script, essas constantes usam o prefixo "Device" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valor</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </dl></td>
<td style="text-align: left;">O status de conexão atual do dispositivo. O minidriver cria e mantém essa propriedade.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> A propriedade pode ter os seguintes valores possíveis.<br/> 
<table>
<thead>
<tr class="header">
<th>Status de conexão</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DEVICE_NOT_CONNECTED</td>
<td>O dispositivo não está conectado.</td>
</tr>
<tr class="even">
<td>WIA_DEVICE_CONNECTED</td>
<td>O dispositivo está conectado e operacional.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </dl></td>
<td style="text-align: left;"><p>A hora do relógio atual que está armazenada no dispositivo. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Essa propriedade tem suporte apenas em dispositivos que têm um relógio interno. Se o relógio do dispositivo puder ser definido, essa propriedade será leitura/gravação; caso contrário, ele será somente leitura.</p>
<p>Os dispositivos WIA relatam o tempo em uma estrutura <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> .</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </dl></td>
<td style="text-align: left;"><p>A versão do firmware do dispositivo. Esse valor deve ser um valor de cadeia de caracteres, como &quot; 1.0.4 &quot; ou &quot; 1.0 ABC &quot; . O minidriver cria e mantém essa propriedade. Se o minidriver WIA não fornecer um recurso de versão, o serviço WIA fornecerá o valor &quot; 0.0.0.0 &quot; como padrão. Um aplicativo lê essa propriedade para determinar a versão da DLL minidriver do WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
