---
description: Constantes de propriedade de informações do dispositivo – As propriedades de informações do dispositivo são propriedades que descrevem a instalação e a instalação do dispositivo.
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Constantes de propriedade de informações do dispositivo (Wiadef.h)
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
ms.openlocfilehash: eff970a3eb1d9285ca469963c3961d90e78874fc5aa7344c3a493093451dcd5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449916"
---
# <a name="device-information-property-constants"></a>Constantes de propriedade de informações do dispositivo

Propriedades de Informações do Dispositivo são propriedades que descrevem a instalação e a instalação do dispositivo. Essas propriedades estão disponíveis por meio das interfaces [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) e também por meio do item raiz. As propriedades de informações do dispositivo são prefixadas com "WIA DIP" (Propriedade de Informações do Dispositivo) e são fornecidas pelo \_ \_ WIA (Aquisição Windows Imagem). Para fins de script, essas constantes usam o prefixo "DeviceInfo" e fazem parte do tipo enumerado [WiaDeviceInfoPropertyId.](-wia-wiadeviceinfopropertyid.md) O nome do membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome constante C/C++ na lista a seguir.



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
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </dl></td>
<td style="text-align: left;">A cadeia de caracteres de ID do dispositivo para o minidriver WIA. O serviço WIA cria e mantém essa propriedade.<br/> Tipo: VT_BSTR, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </dl></td>
<td style="text-align: left;">A cadeia de caracteres de descrição do fornecedor para o minidriver WIA. A descrição do fornecedor é obtida do arquivo INF. Um aplicativo lê essa propriedade para obter uma descrição do fornecedor do dispositivo. O serviço WIA cria e mantém essa propriedade.<br/> Tipo: VT_BSTR, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </dl></td>
<td style="text-align: left;">A cadeia de caracteres de descrição do dispositivo para o minidriver WIA. O serviço WIA cria e mantém essa propriedade. A cadeia de caracteres de descrição do dispositivo que essa propriedade contém é obtida do arquivo INF. Um aplicativo lê essa propriedade para obter uma descrição do dispositivo.<br/> Tipo: VT_BSTR, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </dl></td>
<td style="text-align: left;">O tipo de dispositivo e o subtipo de dispositivo. O serviço WIA cria e mantém essa propriedade. Use a GET_STIDEVICE_TYPE para obter o tipo de dispositivo. O tipo de dispositivo e o subtipo são obtidos do arquivo INF. Um aplicativo lê essa propriedade para determinar se está usando um scanner, uma câmera ou um dispositivo de vídeo.<br/> Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Atualmente, os tipos de dispositivo são definidos da seguinte maneira. O asterisco * indica que o tipo de dispositivo não é suportado pelo Windows Vista e posterior. O asterisco duplo ** indica que o tipo de dispositivo não é suportado pelo Windows Server 2003, Windows Vista ou posterior. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AultDeviceTypeDefault</td>
<td>0x0000</td>
<td>Dispositivo padrão</td>
</tr>
<tr class="even">
<td>Operação DeviceTypeScanner</td>
<td>0x0001</td>
<td>Dispositivo de scanner (consulte <a href="-wia-wiaitempropscannerdevice.md"><strong>a WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> para determinar se o scanner é de flatbed ou sheet-fed.)</td>
</tr>
<tr class="odd">
<td>WallDeviceTypeDigitalCamera*</td>
<td>0x0002</td>
<td>Dispositivo de câmera</td>
</tr>
<tr class="even">
<td>WallDeviceTypeStreamingVideo**</td>
<td>0x0003</td>
<td>Dispositivo de vídeo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </dl></td>
<td style="text-align: left;"><p>O nome da porta do dispositivo instalado, que é atribuído pelo driver de modo kernel que opera o dispositivo. O serviço WIA cria e mantém essa propriedade. Um aplicativo lê essa propriedade para determinar o nome da porta.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </dl></td>
<td style="text-align: left;"><p>O nome do dispositivo. O serviço WIA cria e mantém essa propriedade. O nome do dispositivo contido nessa propriedade é obtido do arquivo INF. Um aplicativo lê essa propriedade para obter o nome do dispositivo.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </dl></td>
<td style="text-align: left;"><p>O nome do servidor em que o minidriver WIA está sendo executado. Essa propriedade é opcional para Windows XP e posterior.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </dl></td>
<td style="text-align: left;"><p>A ID do dispositivo WIA instalada em um computador remoto. O serviço WIA cria e mantém essa propriedade. Ele só é usado internamente pelo serviço WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </dl></td>
<td style="text-align: left;"><p>O CLSID fornecido pelo fornecedor para qualquer objeto COM de extensão de interface do usuário instalado com o minidriver WIA. O serviço WIA cria e mantém essa propriedade. O valor CLSID da interface do usuário contido nessa propriedade é obtido do arquivo INF. Se nenhuma CLSID da interface do usuário for especificada, o serviço WIA fornece um valor padrão. Essa propriedade só é usada internamente pelo serviço WIA quando a interface do usuário está sendo exibida.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </dl></td>
<td style="text-align: left;"><p>O tipo de conexão que o dispositivo está usando. O serviço WIA cria e mantém essa propriedade e somente o serviço WIA pode alterá-la.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A propriedade pode ter os seguintes valores possíveis.</p>

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Dispositivo WDM genérico</td>
</tr>
<tr class="even">
<td>2</td>
<td>Dispositivo SCSI</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Dispositivo USB</td>
</tr>
<tr class="even">
<td>8</td>
<td>Dispositivo serial</td>
</tr>
<tr class="odd">
<td>16</td>
<td>Dispositivo paralelo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </dl></td>
<td style="text-align: left;"><p>A configuração de taxa de bug atual para o dispositivo. O serviço WIA cria e mantém essa propriedade. O valor deverá ser &quot; Vazio se o dispositivo não estiver conectado por um cabo &quot; serial.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </dl></td>
<td style="text-align: left;"><p>As funcionalidades genericAMENTE para o dispositivo, conforme obtido do arquivo INF. O serviço WIA cria e mantém essa propriedade. Um aplicativo lê essa propriedade para determinar as funcionalidades genericAMENTE do dispositivo.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </dl></td>
<td style="text-align: left;"><p>O número (como uma cadeia de caracteres) da versão atual do WIA instalada no sistema. Um aplicativo lê essa propriedade para determinar a versão do WIA instalada no sistema. O serviço WIA cria e mantém essa propriedade. Essa propriedade está disponível no Windows XP e posterior.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </dl></td>
<td style="text-align: left;"><p>A versão DLL atual do minidriver WIA. O serviço WIA cria e mantém essa propriedade. Essa propriedade está disponível no Windows XP e posterior.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </dl></td>
<td style="text-align: left;"><p>A ID do PnP atual para o dispositivo. O serviço WIA cria e mantém essa propriedade. Essa propriedade está disponível no Windows Vista e posterior.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </dl></td>
<td style="text-align: left;"><p>A versão genérica do driver GENERIC. O serviço WIA cria e mantém essa propriedade. Um aplicativo lê essa propriedade para determinar a versão genérica do driver GENERIC. Essa propriedade está disponível no Windows Vista e posterior.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




