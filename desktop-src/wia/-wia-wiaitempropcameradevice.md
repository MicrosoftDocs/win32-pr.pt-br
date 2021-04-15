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
# <a name="camera-device-property-constants"></a>Constantes de Propriedade do dispositivo Camera

Os dispositivos de hardware da aquisição de imagens do Windows (WIA) têm valores de propriedade que são armazenados no registro do Windows. Para obter mais informações, consulte [**constantes de propriedade de dispositivo comum**](-wia-wiaitempropcommondevice.md).

As seguintes constantes de propriedade de dispositivo, com suas cadeias de caracteres associadas, são específicas para câmeras digitais. O prefix "WIA \_ DPC \_ " indica uma propriedade de dispositivo para câmeras e é a Convenção de nomenclatura usada em C/C++. Para fins de script, essas constantes usam o prefixo "CameraDevice" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.

> [!Note]  
> O WIA não oferece suporte a câmeras no Windows Vista ou posterior. Para essas versões do Windows, use a API do dispositivo portátil do Windows (WPD) descrita no kit de desenvolvimento de driver do Windows (DDK) para adquirir imagens de câmeras.

 



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
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </dl></td>
<td style="text-align: left;">O número de imagens que a câmera levou. O minidriver cria e mantém essa propriedade.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </dl></td>
<td style="text-align: left;">O número de imagens que podem ser executadas, dadas as configurações de propriedade atuais. Se essas configurações forem alteradas e as alterações afetarem o tamanho das imagens que o dispositivo de câmera produz, o minidriver WIA deverá atualizar o número de imagens restantes. O minidriver cria e mantém essa propriedade.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </dl></td>
<td style="text-align: left;">Indica o modo de exposição atual da câmera. Um aplicativo altera essa propriedade para controlar o modo de exposição do dispositivo de câmera.<br/> Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> A tabela a seguir tem as sete constantes que são válidas com essa propriedade.<br/> 
<table>
<thead>
<tr class="header">
<th>Modo de exposição</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMODE_MANUAL</td>
<td>A velocidade do obturador e a abertura são definidas pelo usuário.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>A velocidade e a abertura do obturador são definidas automaticamente pela câmera.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>A abertura é definida pelo usuário e a câmera define automaticamente a velocidade do obturador.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>A velocidade do obturador é definida pelo usuário e a câmera define automaticamente a abertura.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>A velocidade e a abertura do obturador são automaticamente definidas pela câmera, otimizadas para o assunto ainda.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>A velocidade e a abertura do obturador são automaticamente definidas pela câmera, otimizadas para cenas que contêm movimentos rápidos.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>A velocidade e a abertura do obturador são automaticamente definidas pela câmera, otimizadas para fotografias em retrato.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </dl></td>
<td style="text-align: left;"><p>Permite o ajuste do ponto definido do controle de exposição automática da câmera digital. Por exemplo, uma configuração de zero não altera o nível de exposição automática de conjunto de fábrica. As unidades estão em &quot; interrupções &quot; que são dimensionadas por um fator de 1000, para permitir valores de parada fracionais. Uma configuração de 2000 corresponde a duas para mais exposição (quatro vezes mais energia no sensor), produzindo imagens mais brilhantes. Uma configuração de-1000 corresponde a uma parada menos exposição (uma metade da energia no sensor) que gera imagens mais escuras. Os valores de configuração estão no sistema aditivo de unidades de exposição fotográfica (APEX). Essa propriedade pode ser expressa como uma lista ou um intervalo de valores. Essa propriedade normalmente é usada somente quando o dispositivo tem a propriedade <strong>WIA_DPC_EXPOSURE_MODE</strong> definida como EXPOSUREMODE_MANUAL.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </dl></td>
<td style="text-align: left;"><p>Corresponde à velocidade do obturador, em segundos, dimensionada por 10.000. Normalmente, o dispositivo usa essa propriedade somente quando a propriedade <strong>WIA_DPC_EXPOSURE_MODE</strong> é definida como EXPOSUREMODE_MANUAL ou EXPOSUREMODE_SHUTTER_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </dl></td>
<td style="text-align: left;"><p>Corresponde à abertura da lente, em unidades do número f-stop dimensionado por 100. A configuração dessa propriedade normalmente é válida somente quando a propriedade <strong>WIA_DPC_EXPOSURE_MODE</strong> é definida como EXPOSUREMODE_MANUAL ou EXPOSUREMODE_APERTURE_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </dl></td>
<td style="text-align: left;"><p>Define a configuração do modo flash atual para o dispositivo de câmera. O driver de dispositivo enumera os valores com suporte dessa propriedade. Um aplicativo grava essa propriedade para definir o modo flash para o dispositivo de câmera.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as seis constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Modo flash</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLASHMODE_AUTO</td>
<td>O dispositivo de câmera determina as configurações corretas do flash.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>O dispositivo de câmera está configurado para ser atualizado independentemente das condições de iluminação atuais.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>O dispositivo de câmera está configurado para <em>não</em> piscar para qualquer imagem tirada.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>O dispositivo de câmera determina as configurações do flash apropriadas usando a redução de olhos vermelhos, independentemente das condições de iluminação atuais.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>O dispositivo de câmera está configurado para usar a redução de olhos vermelhos e o flash, independentemente das condições de iluminação atuais.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>O dispositivo de câmera está configurado para sincronizar com unidades flash externas.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </dl></td>
<td style="text-align: left;"><p>Define a configuração do modo de foco atual para o dispositivo de câmera. O driver de dispositivo enumera os valores com suporte dessa propriedade. Um aplicativo grava essa propriedade para definir o modo de foco para o dispositivo de câmera.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as três constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Modo de foco</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMODE_MANUAL</td>
<td>O dispositivo de câmera está configurado para permitir que o usuário se concentre manualmente.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>O dispositivo de câmera está configurado para se concentrar automaticamente.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>O dispositivo de câmera está configurado para se concentrar automaticamente usando configurações de macro de curto alcance.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </dl></td>
<td style="text-align: left;"><p>Define a fonte de energia atual para o dispositivo de câmera. Um aplicativo lê essa propriedade para determinar qual fonte de energia a câmera está usando.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Modo de energia</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>POWERMODE_LINE</td>
<td>O dispositivo de câmera está operando em um adaptador de energia.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>O dispositivo de câmera está operando com energia da bateria.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </dl></td>
<td style="text-align: left;"><p>A porcentagem de energia da bateria que é deixada para operar o dispositivo de câmera. Esse valor deve ser um inteiro de 0 a 100. Um aplicativo lê essa propriedade para determinar a duração da bateria restante do dispositivo de câmera.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </dl></td>
<td style="text-align: left;"><p>A largura, em pixels, de uma imagem em miniatura a ser usada para imagens recentemente capturadas. Um aplicativo lê esse valor para obter um tamanho estimado para exibir miniaturas em sua interface do usuário.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) ou somente leitura (WIA_PROP_NONE), valores válidos: WIA_PROP_LIST ou WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </dl></td>
<td style="text-align: left;"><p>A largura, em pixels, de uma imagem em miniatura a ser usada para imagens recentemente capturadas. Um aplicativo lê esse valor para obter um tamanho estimado para exibir miniaturas em sua interface do usuário.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) ou somente leitura (WIA_PROP_NONE), valores válidos: WIA_PROP_LIST ou WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </dl></td>
<td style="text-align: left;"><p>A largura em pixels a ser usada para imagens recentemente capturadas. A lista de valores válidos para essa propriedade tem uma correspondência um-para-um com a lista de valores válidos para a propriedade <strong>WIA_DPC_PICT_HEIGHT</strong> . Se a largura e a altura individuais forem linearmente configuradas e ortogonal umas às outras, elas poderão ser expressas como um intervalo.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </dl></td>
<td style="text-align: left;"><p>A altura em pixels a ser usada para imagens recentemente capturadas. A lista de valores válidos para essa propriedade tem uma correspondência um-para-um com a lista de valores válidos para a propriedade <strong>WIA_DPC_PICT_WIDTH</strong> . Se a largura e a altura individuais forem linearmente configuradas e ortogonal umas às outras, elas poderão ser expressas como um intervalo.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </dl></td>
<td style="text-align: left;"><p>Deve ser aproximadamente linear em relação à qualidade de imagem percebida em uma ampla gama de conteúdo de cena e contém um intervalo ou uma lista de inteiros. Inteiros menores são usados para representar a menor qualidade (ou seja, compactação máxima), enquanto inteiros maiores são usados para representar uma qualidade maior (ou seja, compactação mínima). Todas as configurações disponíveis em um dispositivo são relativas somente a esse dispositivo e, portanto, são específicas do dispositivo.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </dl></td>
<td style="text-align: left;"><p>O tempo, em milissegundos, entre capturas de imagem em uma operação de captura de lapso de tempo.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </dl></td>
<td style="text-align: left;"><p>O número de imagens que o dispositivo tenta capturar durante uma captura de lapso de tempo.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </dl></td>
<td style="text-align: left;"><p>O tempo, em milissegundos, entre capturas de imagem durante uma operação de intermitência.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </dl></td>
<td style="text-align: left;"><p>O número de imagens que o dispositivo tenta capturar durante uma operação de intermitência.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica o modo de aquisição de imagem especial da câmera.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as três constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Modo de efeito</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EFFECTMODE_STANDARD</td>
<td>Capture uma imagem no modo padrão da câmera.</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>Capturar uma imagem em escala de cinza.</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>Capturar uma imagem de sépia.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </dl></td>
<td style="text-align: left;"><p>A taxa de zoom efetiva da imagem adquirida da câmera digital, dimensionada por um fator de 10. Um valor de 10 corresponde à ausência de zoom digital (1X), que é o tamanho de cena padrão capturado pela câmera. Um valor de 20 corresponde a um zoom 2X, em que um quarto do tamanho da cena padrão é capturado pela câmera.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </dl></td>
<td style="text-align: left;"><p>A nitidez percebida de uma imagem capturada. Essa propriedade pode usar uma lista de valores ou um intervalo de valores. O valor mínimo representa a menor quantidade de nitidez, enquanto o valor máximo representa a nitidez máxima. Normalmente, um valor no meio do intervalo representa a nitidez normal, ou padrão.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </dl></td>
<td style="text-align: left;"><p>O contraste percebido de uma imagem capturada. Essa propriedade pode conter uma lista de valores ou um intervalo de valores. O valor mínimo com suporte representa a menor quantidade de contraste, enquanto o valor máximo representa o maior contraste. Normalmente, um valor no meio do intervalo representa normal, ou padrão, o contraste.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </dl></td>
<td style="text-align: left;"><p>Define o modo de captura de imagem.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as três constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Modo de captura</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAPTUREMODE_NORMAL</td>
<td>Modo normal para a câmera.</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>Capture mais de uma imagem em sucessão rápida, conforme definido pelos valores das propriedades <strong>WIA_DPC_BURST_NUMBER</strong> e <strong>WIA_DPC_BURST_INTERVAL</strong> .</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Capture mais de uma imagem sucessivamente, conforme definido pelas propriedades <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </dl></td>
<td style="text-align: left;"><p>O valor que representa a quantidade de tempo de atraso, em milissegundos, que deve ser inserido entre o gatilho de captura e a inicialização real da captura de dados. Essa propriedade não deve ser usada para descrever o tempo entre os quadros para inicialização única, várias capturas como intermitência ou tempo decorrido, que têm propriedades de intervalo separadas <strong>WIA_DPC_BURST_INTERVAL</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>. Nesses casos, ele ainda funciona como um atraso inicial antes que a primeira imagem na série seja capturada, independentemente do tempo entre os quadros. Para nenhum atraso de precaptura, essa propriedade deve ser definida como zero.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </dl></td>
<td style="text-align: left;"><p>Permite a emulação de configurações de velocidade de filme em uma câmera digital. As configurações correspondem às designações ISO (ASA/DIN). Normalmente, um dispositivo dá suporte a valores enumerados discretos, mas o controle contínuo sobre um intervalo de valores é possível. Um valor de 0xFFFF corresponde à configuração automática de ISO.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica o modo que a câmera usa para ajustar automaticamente a configuração de exposição.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

<table>
<thead>
<tr class="header">
<th>Modo de medição de exposição</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMETERING_AVERAGE</td>
<td>Defina a exposição com base em uma média da cena inteira.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>Defina a exposição com base em uma média ponderada no centro.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>Defina a exposição com base em um padrão multiespecial.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Defina a exposição com base em um ponto central.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica o modo que a câmera usa para ajustar o foco automaticamente.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Modo de medição de foco</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMETERING_CENTERSPOT</td>
<td>Ajuste o foco com base em um ponto central.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Ajuste o foco com base em um padrão multiespecial.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </dl></td>
<td style="text-align: left;"><p>A distância, em milímetros, entre o plano de captura de imagem da câmera digital e o ponto de foco. Um valor de 0xFFFF corresponde a uma configuração maior que 655 metros.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </dl></td>
<td style="text-align: left;"><p>O comprimento focal 35mm-equivalente. Os valores dessa propriedade correspondem ao comprimento focal em milímetros multiplicado por 100. O comprimento focal determina o zoom óptico.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </dl></td>
<td style="text-align: left;"><p>Uma cadeia de caracteres Unicode terminada em nulo que representa o lucro vermelho, verde e azul aplicado aos dados da imagem, respectivamente. Por exemplo, &quot; 4:25:50 &quot; representa um lucro vermelho de 4, um lucro verde de 25 e um lucro azul de 50.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </dl></td>
<td style="text-align: left;"><p>Especifica como a câmera digital pondera os canais de cor.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A seguir está uma lista de possíveis valores para essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Balanço de branco</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>O equilíbrio de branco é definido diretamente usando a propriedade <strong>WIA_DPC_RGB_GAIN</strong> .</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>A câmera usa um mecanismo automático para definir o equilíbrio de branco.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>A câmera determina a configuração de balanço de branco quando um usuário pressiona o botão capturar enquanto aponta a câmera uma área branca.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>A câmera define o equilíbrio de branco com um valor apropriado para uso em condições de horário de verão.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>A câmera define o equilíbrio de branco com um valor apropriado para uso com uma fonte de luz fluorescente.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>A câmera define o equilíbrio de branco com um valor apropriado para uso com uma fonte de luz Tungsten.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>A câmera define o equilíbrio de branco com um valor apropriado para uso com um flash eletrônico.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </dl></td>
<td style="text-align: left;"><p>Descreve uma URL. A URL descrita por esse proroperty é aquela que as imagens ou os objetos, depois de serem adquiridos do dispositivo, podem ser carregados para – de acordo com um dos cenários a seguir.</p>
<ul>
<li>Um aplicativo WIA lê essa propriedade e permite que o usuário carregue imagens automaticamente na URL.</li>
<li>Um aplicativo define a URL e outros dispositivos (quiosques e assim por diante) usam essa propriedade.</li>
</ul>
<p>O Microsoft Windows não carrega imagens por si só.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </dl></td>
<td style="text-align: left;"><p>O nome do proprietário (que é o usuário atual) do dispositivo. O dispositivo usa essa propriedade para popular o campo artista em todas as imagens EXIF capturadas.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </dl></td>
<td style="text-align: left;"><p>A notificação de direitos autorais. O dispositivo usa essa propriedade para popular o campo de direitos autorais em cada imagem de EXIF capturada.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




