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
# <a name="scanner-device-property-constants"></a>Constantes de propriedade de dispositivo do scanner

Os dispositivos de hardware da aquisição de imagens do Windows (WIA) têm valores de propriedade que são armazenados no registro do Windows. Para obter mais informações, consulte [**constantes de propriedade de dispositivo comum**](-wia-wiaitempropcommondevice.md). As seguintes constantes de propriedade de dispositivo, com suas cadeias de caracteres associadas, são específicas para scanners de imagem digital.

O prefixo " \_ DPS \_ do WIA" indica uma propriedade de dispositivo para dispositivos de scanner e é a Convenção de nomenclatura usada em C/C++. Para fins de script, essas constantes usam o prefixo "ScannerDevice" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.



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
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas no Windows Vista e posterior.
</blockquote>
<br/> Contém um identificador de instância de função exclusivo para um dispositivo de scanner de serviços Web. Esse identificador representa o serviço Web no dispositivo de scanner com o qual o mini-driver WIA está se comunicando. Não é necessário fazer suposições sobre a forma desse identificador. O mini-driver WIA cria e mantém essa propriedade. <br/> Os aplicativos WIA podem usar o valor de WIA_DPS_DEVICE_ID para localizar, usando a API de descoberta de função, o objeto de instância de função que representa o dispositivo de scanner de serviços Web usado na sessão atual do WIA 2,0.<br/> Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td style="text-align: left;">Reservado, não use.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;">Reservado, não use.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td style="text-align: left;">Contém os recursos do verificador. O minidriver cria e mantém essa propriedade. <br/> Um aplicativo lê essa propriedade para determinar se o scanner tem um mesa de alimentação, alimentador de documentos ou duplexador instalado. Essa propriedade também é usada para definir ainda mais os recursos instalados.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> A tabela a seguir descreve as constantes válidas somente com o Windows 7.<br/> 
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AUTO_SOURCE</td>
<td>O verificador tem um manipulador de documento automático instalado.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>A tabela a seguir descreve as constantes que são válidas somente com o Windows 7 e o Windows Vista.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ADVANCED_DUP</td>
<td>O dispositivo dá suporte à configuração de digitalização duplex avançada. Use WIA_IPS_DUPLEX_SETTINGS para alternar entre o uso das configurações de duplex básico e avançado.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>O verificador pode detectar quando o adaptador de transparência/filme está pronto para verificação.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>O verificador pode detectar quando há documentos no armazenamento interno.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>O scanner é equipado com um adaptador de verificação de transparência/filme.</td>
</tr>
<tr class="odd">
<td>ARMA</td>
<td>O scanner está equipado com um dispositivo de armazenamento de imagem interno.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>A tabela a seguir descreve as constantes que são válidas com o Windows XP ou posterior.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_FEED</td>
<td>O verificador pode detectar um documento no alimentador.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>O verificador pode detectar um documento no cilindro de mesa.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>O verificador pode detectar um documento no alimentador somente examinando.</td>
</tr>
<tr class="even">
<td>DUPLICA</td>
<td>O scanner tem um duplexador.</td>
</tr>
<tr class="odd">
<td>FEED</td>
<td>O verificador tem um manipulador de documento automático instalado.</td>
</tr>
<tr class="even">
<td>PLANOS</td>
<td>O scanner tem um cilindro de mesa.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>A tabela a seguir descreve as constantes válidas somente com o Windows XP. Esses valores foram preteridos para o Windows 7 e o Windows Vista e não devem ser usados.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_DUP</td>
<td>O verificador pode detectar uma solicitação de verificação duplex do usuário.</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>O verificador pode saber quando o duplexador está instalado.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>O verificador pode saber quando o alimentador automático de documentos está instalado.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a origem e o modo de aquisição do scanner atual. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar a fonte de aquisição atual do scanner ou para gravar essa propriedade para definir a origem e o modo do verificador. Além disso, os aplicativos usam essa propriedade para habilitar e desabilitar a funcionalidade do duplexador.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>A tabela a seguir tem as dez constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ALIMENTADORA</td>
<td>Digitalizar usando o alimentador de documentos.</td>
</tr>
<tr class="even">
<td>MESA</td>
<td>Digitalizar usando a mesa.</td>
</tr>
<tr class="odd">
<td>DUPLEX</td>
<td>Examinar usando operações do duplex.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Habilita a alimentação automática do próximo documento após uma verificação.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Primeiro examine a frente do documento. Esse valor é válido quando DUPLEX é definido.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Primeiro examine a parte de trás do documento. Esse valor é válido quando DUPLEX é definido.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Verificar somente a frente. Esse valor é válido quando DUPLEX é definido.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Verifique apenas o verso. Esse valor é válido quando DUPLEX é definido.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Digitalizar a próxima página do documento.</td>
</tr>
<tr class="even">
<td>PREFEED</td>
<td>Habilite o modo de pré-feed. Pré-posicionar próximo documento durante a verificação.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td style="text-align: left;"><p>Contém o estado atual do feed instalado do scanner, alimentador de documentos ou duplexador. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar se o dispositivo de scanner está pronto para ser usado. Essa é uma maneira ideal de verificar se o papel está no alimentador antes de adquirir uma imagem.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. Um asterisco * indica que o sinalizador não tem suporte no Windows Vista ou posterior. O símbolo <strong>V</strong> indica que o sinalizador tem suporte apenas no Windows Vista e posterior. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEED_READY</td>
<td>A mesa está pronta para uso.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>O scanner tem um documento no cilindro de mesa.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>O duplexador está habilitado e pronto para ser usado.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>A tampa da cama plana está ativa.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>O caminho do papel é coberto e está impedindo a operação adequada.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Um documento está emperrado no alimentador de documentos.</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>O adaptador de transparência está instalado e pronto para uso.</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>O dispositivo de armazenamento interno está pronto.</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>O armazenamento está cheio, nenhuma operação de carregamento é possível.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Ocorreu uma condição de feed múltiplo (geralmente com um PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Há um erro que requer a intervenção do usuário no dispositivo.</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>O scanner não está pronto devido a um problema de lâmpada.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td style="text-align: left;"><p>Contém todos os caracteres válidos que um aplicativo pode usar para criar cadeias válidas de endossador. Um endossador é uma impressora instalada em um scanner que imprime uma mensagem de texto em todas as páginas verificadas. O minidriver deve validar a configuração da propriedade <strong>WIA_DPS_ENDORSER_STRING</strong> em relação ao conjunto de caracteres válido nesta propriedade. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td style="text-align: left;"><p>Contém uma cadeia de caracteres que deve ser endossada (em outras palavras, impressa) em cada página que o minidriver examina. Um aplicativo define essa propriedade usando o conjunto de caracteres válido que é relatado na propriedade <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> . O minidriver deve endossar documentos somente se uma cadeia de caracteres estiver definida nessa propriedade. Uma cadeia de caracteres vazia significa que a funcionalidade do endossador está desabilitada.</p>
<p>Como é responsabilidade do driver interpretar a cadeia de caracteres do endossador, o driver pode usar caracteres especiais em <strong>WIA_DPS_ENDORSER_STRING</strong>. No entanto, apenas seus aplicativos compreenderiam esses caracteres.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Um driver que dá suporte à propriedade <strong>WIA_DPS_ENDORSER_STRING</strong> deve oferecer suporte à lista de tokens a seguir. </p>
<table>
<thead>
<tr class="header">
<th>Token</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE $</td>
<td>A data no formato AAAA/MM/DD.</td>
</tr>
<tr class="even">
<td>$DAY $</td>
<td>O dia no formato DD.</td>
</tr>
<tr class="odd">
<td>$MONTH $</td>
<td>O mês do ano no formato MM.</td>
</tr>
<tr class="even">
<td>$PAGE _COUNT $</td>
<td>O número de páginas transferidas.</td>
</tr>
<tr class="odd">
<td>$TIME $</td>
<td>A hora do dia no formato HH: MM: SS.</td>
</tr>
<tr class="even">
<td>$YEAR $</td>
<td>O ano no formato aaaa.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas no Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o endereço SOAP de um dispositivo de scanner de serviços Web. O mini-driver WIA 2,0 cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o registro, ou alinhamento horizontal, para documentos colocados na mesa. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as três constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>O papel é justificado à esquerda.</td>
</tr>
<tr class="even">
<td>CENTRA</td>
<td>O papel está centralizado.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>O papel é justificado à direita.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Consulte também</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a largura máxima, em milésimos de polegada, que é verificada no eixo horizontal (X) do cilindro de um scanner de mesa na resolução atual. Essa propriedade também se aplica a alimentadores de documentos automáticos que movem planilhas para o cilindro de um scanner de mesa para verificação. Essa propriedade é obrigatória para scanners que têm um cilindro. Em vez disso, outros tipos de scanner implementarão a propriedade <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a largura máxima, em milésimos de polegada, que é verificada no eixo horizontal (X) de um scanner de alimentação de papel ou portátil na resolução atual. Essa propriedade também se aplica a alimentadores de documentos automáticos que examinam sem mover folhas para o cilindro de um scanner de mesa. Essa propriedade é obrigatória para scanners alimentados por planilhas, com rolagem e por bolso.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td style="text-align: left;"><p>Contém o tempo máximo para verificar uma única página com as configurações de propriedade atuais, em milissegundos. Um aplicativo lê essa propriedade para estimar o tempo que levará para digitalizar uma página. Isso é útil ao determinar as condições de um dispositivo que parou de responder. O minidriver cria e mantém essa propriedade. Essa propriedade é necessária para todos os scanners.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém as dimensões horizontais físicas da menor página que o alimentador de documentos do verificador pode verificar, em milésimos de uma polegada. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Consulte também</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém as dimensões verticais físicas da menor página que o alimentador de documentos do verificador pode verificar, em milésimos de uma polegada. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Consulte também</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Resolução óptica horizontal. Resolução óptica horizontal mais alta com suporte em DPI. Essa propriedade é um único valor. Esta não é uma lista de todas as resoluções que podem ser geradas pelo dispositivo. Em vez disso, essa é a resolução da fibra óptica do dispositivo. O minidriver cria e mantém essa propriedade. Essa propriedade é necessária para todos os scanners.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Resolução óptica vertical. Resolução óptica vertical com suporte mais alta em DPI. Essa propriedade é um único valor. Essa não é uma lista de todas as resoluções que são geradas pelo dispositivo. Em vez disso, essa é a resolução da fibra óptica do dispositivo. O minidriver cria e mantém essa propriedade. Essa propriedade é necessária para todos os scanners.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td style="text-align: left;"><p>Contém a configuração de orientação atual. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo define a propriedade <strong>WIA_DPS_ORIENTATION</strong> para definir a orientação original de uma página ou imagem a ser adquirida. Para obter informações sobre como usar WIA_DPS_ORIENTATION, consulte <strong>WIA_DPS_PAGE_SIZE</strong></p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as quatro constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Defination</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AMBIENTE</td>
<td>rotação no sentido anti-horário de 90 graus, em relação à orientação retrato.</td>
</tr>
<tr class="even">
<td>ORIENTAÇÕES</td>
<td>0 graus.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>rotação no sentido anti-horário de 180 graus, em relação à orientação retrato.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>rotação no sentido anti-horário de 270 graus, em relação à orientação retrato.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Consulte também</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td style="text-align: left;"><p>Cor usada para preencher quando não há dados de imagem suficientes para completar um buffer solicitado. Essa propriedade é implementada para os scanners que esfolham o buffer. Essa propriedade é opcional para todos os scanners. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>O formato das informações de cor é <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a altura, em milésimos de polegada, da página atualmente selecionada. O minidriver cria e mantém a propriedade <strong>WIA_DPS_PAGE_HEIGHT</strong> . Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo examinada. Se as configurações de extensão forem diferentes dos tamanhos de página conhecidos, essa propriedade relatará a altura da página cujo <strong>WIA_DPS_PAGE_SIZE</strong> Propriedade está definida como WIA_PAGE_CUSTOM (que é um valor da propriedade <strong>WIA_DPS_PAGE_SIZE</strong> ). <strong>WIA_DPS_PAGE_HEIGHT</strong> deve estar em sincronia com <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que relata a altura, em pixels, da página a ser verificada.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o tamanho da página selecionada no momento para ser examinada. Para selecionar as dimensões da página a ser verificada, um aplicativo define essa propriedade. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as três constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_A4</td>
<td>8267 X 11692 (orientação retrato)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Definido pelos valores das propriedades <strong>WIA_DPS_PAGE_HEIGHT</strong> e <strong>WIA_DPS_PAGE_WIDTH</strong></td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (orientação retrato)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>O valor da propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> determina a orientação da página atualmente selecionada. As propriedades <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> relatam as dimensões da página, em milésimos de polegada. Observe que essas propriedades devem estar em acordo com <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, que contêm as dimensões da página em pixels. Os valores válidos do tipo WIA_PROP_LIST devem depender das configurações válidas da propriedade <strong>WIA_IPS_ORIENTATION</strong> . Se o dispositivo não puder verificar documentos orientados a paisagem com uma configuração WIA_PAGE_A4, WIA_PAGE_A4 não deverá aparecer na lista de valores válidos para a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> for definido como LANSCAPE.</p>
<p>Se um aplicativo definir <strong>WIA_DPS_PAGE_SIZE</strong> para qualquer valor diferente de WIA_PAGE_CUSTOM, o minidriver deverá ajustar os valores de <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> para as dimensões da página em milésimos de polegada. Ele também deve ajustar os valores de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> e <strong>WIA_IPS_YEXTENT</strong> às dimensões da página em pixels.</p>
<p>Se uma configuração de extensão (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> ou <strong>WIA_IPS_YEXTENT</strong>) for alterada para um valor que não corresponda à configuração de tamanho de página atual, o minidriver deverá alterar o valor da propriedade <strong>WIA_DPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM. O minidriver também deve modificar <strong>WIA_DPS_PAGE_WIDTH</strong> ou <strong>WIA_DPS_PAGE_HEIGHT</strong> de acordo com a nova configuração de extensão.</p>
<p>Se <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> for definido como LANSCAPE, as configurações de extensão serão &quot; invertidas. &quot; Por exemplo, se um aplicativo definir <strong>WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_A4, minidriver deverá definir <strong>WIA_DPS_PAGE_WIDTH</strong> como 11692 e <strong>WIA_DPS_PAGE_HEIGHT</strong> como 8267. (O minidriver também deve definir <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> de acordo.) Observe que, se <strong>WIA_DPS_PAGE_SIZE</strong> for definido como WIA_PAGE_CUSTOM, a configuração de orientação não será usada para determinar as dimensões de extensão da página a ser verificada.</p>
<p>O minidriver é responsável por garantir que a propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> esteja em contrato com a área de seleção atual. Se um aplicativo alterar o valor de <strong>WIA_IPS_ORIENTATION</strong> para um que seja inválido para o tamanho de página selecionado no momento, o minidriver deverá alterar o valor de <strong>WIA_DPS_PAGE_SIZE</strong> para um tamanho de página com suporte no novo valor de orientação.</p>
<p>Se um aplicativo definir a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_CUSTOM, a área de seleção atual não será afetada. O minidriver WIA deve obter o layout da imagem atual, começando com as configurações atuais das propriedades <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> e <strong>WIA_IPS_YPOS</strong> . Se a configuração de tamanho de página resultar em uma área de seleção que está fora do ambiente do scanner, o minidriver deverá ajustar automaticamente os valores das propriedades <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> para as configurações válidas. Se as propriedades <strong>WIA_DPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> forem definidas ao mesmo tempo e forem inválidas quando aplicadas em combinação, o minidriver deverá falhar as configurações do aplicativo retornando um erro no <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>. .</p>
<p>Os quatro exemplos a seguir mostram diferentes cenários de <strong>WIA_DPS_PAGE_SIZE</strong> .</p>
<ol>
<li>O driver relata as configurações.</li>
<li>Um aplicativo define a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_LETTER.</li>
<li>Um aplicativo define a propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> como LANSCAPE.</li>
<li>Um aplicativo altera a propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> para um valor menor.</li>
</ol>
<p><strong>Exemplo 1: o minidriver relata as configurações</strong></p>
<p>No exemplo a seguir, o minidriver define uma área de seleção personalizada antes que um aplicativo defina as propriedades de WIA. Nesse caso, a área de seleção representa a mesa inteira.</p>
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
<p><strong>Exemplo 2: um aplicativo define a</strong> <strong></strong><strong>Propriedade WIA_DPS_PAGE_SIZE como WIA_PAGE_LETTER</strong>  </p>
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
<p><strong>Exemplo 3: um aplicativo define a</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>Propriedade WIA_IPS_ORIENTATION como LANSCAPE</strong>  </p>
<p>A base física deve ser capaz de adquirir uma página que estava originalmente na orientação paisagem.</p>
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
<p><strong>Exemplo 4: um aplicativo altera a</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>Propriedade WIA_IPS_XEXTENT para um valor menor</strong>  </p>
<p>No exemplo a seguir, um aplicativo altera a propriedade <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> para 1000. O minidriver deve assumir que o novo valor contido no <strong>WIA_IPS_XEXTENT</strong> não é mais válido para a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> e, portanto, deve alterar <strong>WIA_DPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM. O minidriver também deve ajustar <strong>WIA_DPS_PAGE_WIDTH</strong>.</p>
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a largura da página atual selecionada, em milésimos de polegada. Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo examinada. Se as configurações de extensão forem diferentes de tamanhos de página conhecidos, essa propriedade relatará a largura da página cuja propriedade <strong>WIA_DPS_PAGE_SIZE</strong> está definida como WIA_PAGE_CUSTOM. <strong>WIA_DPS_PAGE_WIDTH</strong> deve estar em sincronia com o valor de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que relata a largura, em pixels, da página a ser verificada. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o número atual de páginas a serem adquiridas de um alimentador automático de documentos. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>; Acesso: leitura/gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero pelo número máximo de páginas que o alimentador de documentos pode conter)</p>
<p>Um aplicativo lê essa propriedade para determinar a capacidade da página do alimentador de documentos. O aplicativo também define essa propriedade como o número de páginas que ele vai verificar.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Se o modo duplex estiver habilitado (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> é definido como alimentador | DUPLEX), <strong>WIA_DPS_PAGES</strong> ainda é igual ao número de páginas a serem verificadas.
</blockquote>
</div>
<div>
 
</div>
<p>Uma folha de papel conterá automaticamente duas páginas se o DUPLEX estiver habilitado, mesmo se o lado do verso da página estiver em branco.</p>
<p>Definir <strong>WIA_DPS_PAGES</strong> como 1 faz com que um scanner processe um dos lados da página. É recomendável que, se um scanner não possa verificar apenas um lado de uma página enquanto estiver no modo duplex, o <strong>WIA_DPS_PAGES</strong> valor válido para o membro Inc da estrutura de WIA_PROPERTY_INFO deve ser alterado para 2. Esse valor sinaliza ao aplicativo que ele deve solicitar páginas em múltiplos de dois. Um valor de zero significa que <em>todas as</em> páginas atualmente carregadas no alimentador de documentos serão verificadas.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td style="text-align: left;"><p>Especifica a cor do cilindro de fundo da planilha a ser examinado. Essa propriedade é opcional para scanners que têm um cilindro. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>O formato das informações de cor é <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica o modo de visualização de um dispositivo. Um aplicativo define essa propriedade para posicionar o dispositivo em um modo de visualização.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as duas constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FINAL_SCAN</td>
<td>O aplicativo executará uma verificação final.</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>O aplicativo executará uma verificação de visualização.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td style="text-align: left;"><p>Contém um valor que indica se o verificador armazenará em cache as páginas em um buffer de scanner antes de enviá-las ao aplicativo.</p>
<p>Um valor de zero desabilita A verificação antecipada e nenhuma página será verificada antecipadamente. Fazer transferências de dados normais no item varredura em buffer-adiantamento recupera as páginas armazenadas em buffer. As propriedades WIA não podem ser alteradas durante uma operação de varredura antecipada. Essa propriedade é opcional.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de zero para o número máximo de páginas que o alimentador de documentos pode conter.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows 7 e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Indica a fonte de entrada (superfície, alimentador de documentos automático ou adaptador de verificação de FIL) a ser examinada ou o local de armazenamento para o qual transferir dados.</p>
<p>Um evento de verificação notifica o aplicativo que o usuário iniciou uma verificação, mas o evento não fornece o nome do item WIA que representa a fonte de entrada. O manipulador de eventos do aplicativo pode consultar a propriedade WIA_DPS_SCAN_AVAILABLE_ITEM do item raiz para obter o nome do item de origem de entrada.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de zero para o número máximo de páginas que o alimentador de documentos pode conter.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a ID de serviço de um dispositivo de scanner de serviços Web. O mini-driver WIA 2,0 cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o registro, o alinhamento e a detecção de borda para documentos que são colocados na mesa. O minidriver cria e mantém essa propriedade. Essa propriedade indica como a planilha é posicionada horizontalmente no início da verificação de um scanner de mão ou alimentado por folha. A propriedade é usada para prever onde o documento é colocado na cabeça de verificação.</p>
<p>Para os scanners que dão suporte a mais de um cabeçalho de verificação, essa propriedade é relativa ao início da verificação mais alta. Essa propriedade é obrigatória para scanners de mão, alimentados por folhas e alimentados por folha.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as três constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>A planilha está posicionada à esquerda em relação ao cabeçalho de verificação.</td>
</tr>
<tr class="even">
<td>CENTRA</td>
<td>A planilha está centralizada no cabeçalho de verificação.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>A planilha está posicionada à direita em relação ao cabeçalho de verificação.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica se um item precisa de um controle de visualização exibido para o usuário. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as duas constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_SHOW_PREVIEW_CONTROL</td>
<td>Mostrar um controle de visualização para o usuário, pois este dispositivo pode executar uma visualização.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>Não mostrar um controle de visualização para o usuário, pois este dispositivo não pode executar uma visualização.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Usado pelo serviço WIA para informar ao mini-driver sobre o nome da conta de usuário (incluindo o nome de domínio de rede quando aplicável) da sessão em que o aplicativo WIA atual está em execução.</p>
<p>Essa é uma propriedade de item raiz, gerenciada pelo serviço WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o registro, o alinhamento vertical e a detecção de borda para documentos colocados na mesa. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as três constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TOP_JUSTIFIED</td>
<td>O papel é justificado pela parte principal.</td>
</tr>
<tr class="even">
<td>CENTRA</td>
<td>O papel está centralizado.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>O papel é justificado por baixo.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Consulte também</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a altura máxima, em milésimos de polegada, que é verificada no eixo vertical (Y) do cilindro de um scanner de mesa na resolução atual. Essa propriedade também se aplica a alimentadores automáticos de documentos, que movem planilhas para o cilindro de um scanner de mesa para verificação. Essa propriedade é obrigatória para scanners que têm um cilindro. Em vez disso, outros tipos de scanner implementarão a propriedade <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a altura máxima, em milésimos de polegada, que é verificada no eixo vertical (Y) de um scanner de alimentação de papel ou portátil na resolução atual. Essa propriedade também se aplica a alimentadores de documentos automáticos que examinam sem mover folhas para o cilindro de um scanner de mesa. Essa propriedade é obrigatória para scanners alimentados por folha. Os scanners de rolagem e de bolso não devem implementar essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
