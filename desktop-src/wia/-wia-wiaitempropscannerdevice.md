---
description: Windows os dispositivos de hardware de aquisição de imagem (WIA) têm valores de propriedade que são armazenados no registro de Windows.
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
ms.openlocfilehash: d9e7afee9b5b639c21e52dc797e7ad42a6ee0dd0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627182"
---
# <a name="scanner-device-property-constants"></a>Constantes de propriedade de dispositivo do scanner

Windows os dispositivos de hardware de aquisição de imagem (WIA) têm valores de propriedade que são armazenados no registro de Windows. Para obter mais informações, consulte [**constantes de propriedade de dispositivo comum**](-wia-wiaitempropcommondevice.md). As seguintes constantes de propriedade de dispositivo, com suas cadeias de caracteres associadas, são específicas para scanners de imagem digital.

O prefixo " \_ DPS \_ do WIA" indica uma propriedade de dispositivo para dispositivos de scanner e é a Convenção de nomenclatura usada em C/C++. Para fins de script, essas constantes usam o prefixo "ScannerDevice" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Constante/valor</th>
<th >Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
essa propriedade tem suporte apenas no Windows Vista e versões posteriores.
</blockquote>
<br/> Contém um identificador de instância de função exclusivo para um dispositivo de scanner de serviços Web. Esse identificador representa o serviço Web no dispositivo de scanner com o qual o mini-driver WIA está se comunicando. Não é necessário fazer suposições sobre a forma desse identificador. O mini-driver WIA cria e mantém essa propriedade. <br/> Os aplicativos WIA podem usar o valor de WIA_DPS_DEVICE_ID para localizar, usando a API de descoberta de função, o objeto de instância de função que representa o dispositivo de scanner de serviços Web usado na sessão atual do WIA 2,0.<br/> Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td >Reservado, não use.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td >Reservado, não use.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td >Contém os recursos do verificador. O minidriver cria e mantém essa propriedade. <br/> Um aplicativo lê essa propriedade para determinar se o scanner tem um mesa de alimentação, alimentador de documentos ou duplexador instalado. Essa propriedade também é usada para definir ainda mais os recursos instalados.<br/> Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> a tabela a seguir descreve as constantes que são válidas somente com o Windows 7.<br/> 
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
<p>a tabela a seguir descreve as constantes válidas com Windows 7 e Windows Vista apenas.</p>
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
<p>a tabela a seguir descreve as constantes que são válidas com o Windows XP ou posterior.</p>
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
<p>a tabela a seguir descreve as constantes que são válidas somente com Windows XP. esses valores foram preteridos para o Windows 7 e Windows Vista e não devem ser usados.</p>
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
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
não há suporte para essa propriedade no Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
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
<td>Digitalizar somente a parte frontal. Esse valor é válido quando DUPLEX é definido.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Digitalizar somente a parte traseira. Esse valor é válido quando DUPLEX é definido.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Digitalizar a próxima página do documento.</td>
</tr>
<tr class="even">
<td>PREFEED</td>
<td>Habilitar o modo de pré-feed. Pré-posiciona o próximo documento durante a verificação.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td ><p>Contém o estado atual do flatbed, feeder ou duplexer instalado do scanner. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar se o dispositivo do scanner está pronto para ser usado. Essa é uma maneira ideal de verificar se o papel está no feeder antes de adquirir uma imagem.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. Um asterisco * indica que não há suporte para o sinalizador no Windows Vista ou posterior. O <strong>símbolo V</strong> indica que o sinalizador tem suporte apenas no Windows Vista e posterior. </p>
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
<td>O flatbed está pronto para uso.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>O scanner tem um documento na placa de flatbed.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>O duplexador está habilitado e pronto para ser usado.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>A cobertura de chão simples está em cima.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>O caminho do papel é coberto e está impedindo a operação adequada.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Um documento é ressalvado no feeder de documentos.</td>
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
<td>O armazenamento está cheio, nenhuma operação de upload possível.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Ocorreu uma condição de vários feeds (geralmente com um PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Há um erro que requer intervenção do usuário no dispositivo.</td>
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
<td ><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td ><p>Contém todos os caracteres válidos que um aplicativo pode usar para criar cadeias de caracteres de endossador válidas. Um endossador é uma impressora instalada em um verificador que instala uma mensagem de texto em cada página digitalizada. O minidriver deve validar a configuração <strong>da propriedade WIA_DPS_ENDORSER_STRING</strong> com relação ao conjunto de caracteres válido nesta propriedade. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td ><p>Contém uma cadeia de caracteres que deve ser endossada (em outras palavras, impressa) em cada página que o minidriver examina. Um aplicativo define essa propriedade usando o conjunto de caracteres válido relatado na propriedade <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> dados. O minidriver só deverá endossar documentos se uma cadeia de caracteres estiver definida nessa propriedade. Uma cadeia de caracteres vazia significa que a funcionalidade do endossador está desabilitada.</p>
<p>Como é responsabilidade do driver interpretar a cadeia de caracteres do endosso, o driver pode usar caracteres especiais no <strong>WIA_DPS_ENDORSER_STRING</strong>. No entanto, somente seus aplicativos compreenderiam esses caracteres.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Leitura/Gravação, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Um driver que <strong>WIA_DPS_ENDORSER_STRING</strong> propriedade WIA_DPS_ENDORSER_STRING deve dar suporte à lista de tokens a seguir. </p>
<table>
<thead>
<tr class="header">
<th>Token</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE$</td>
<td>A data no formato AAAA/MM/DD.</td>
</tr>
<tr class="even">
<td>$DAY$</td>
<td>O dia no formato DD.</td>
</tr>
<tr class="odd">
<td>$MONTH$</td>
<td>O mês do ano no formato MM.</td>
</tr>
<tr class="even">
<td>$PAGE_COUNT$</td>
<td>O número de páginas transferidas.</td>
</tr>
<tr class="odd">
<td>$TIME$</td>
<td>A hora do dia no formato HH:MM:SS.</td>
</tr>
<tr class="even">
<td>$YEAR$</td>
<td>O ano no formato AAAA.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td ><p>Reservado, não use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade só tem suporte no Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o endereço SOAP de um dispositivo de scanner de serviços Web. O mini driver WIA 2.0 cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o registro ou alinhamento horizontal para documentos colocados no flatbed. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>O papel é deixado justificado.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>O papel é centralizado.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>O papel tem razão.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Consulte também</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a largura máxima, em milésimos de polegada, que é digitalizada no eixo horizontal (X) da placa de um verificador de flatbed na resolução atual. Essa propriedade também se aplica a feeders de documentos automáticos que movem planilhas para a placa de um scanner de flatbed para verificação. Essa propriedade é obrigatória para scanners que têm uma placa. Em vez disso, outros tipos de scanner <strong>implementarão WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> propriedade .</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a largura máxima, em milésimos de polegada, que é digitalizada no eixo horizontal (X) de um verificador de feed de folha ou portátil na resolução atual. Essa propriedade também se aplica a feeds de documentos automáticos que digitalizar sem mover planilhas para a placa de um scanner de flatbed. Essa propriedade é obrigatória para scanners de rolagem, de rolagem e de mão.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td ><p>Contém o tempo máximo para verificar uma única página com as configurações de propriedade atuais, em milissegundos. Um aplicativo lê essa propriedade para estimar o tempo que levará para examinar uma página. Isso é útil ao determinar as condições de um dispositivo que parou de responder. O minidriver cria e mantém essa propriedade. Essa propriedade é necessária para todos os scanners.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém as dimensões horizontais físicas da menor página que o feed de documentos do scanner pode examinar, em milésimos de polegada. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Consulte também</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém as dimensões verticais físicas da menor página que o feed de documentos do scanner pode examinar, em milésimos de polegada. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Consulte também</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade não é suportada pelo Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Resolução óptica horizontal. Resolução óptica horizontal com suporte mais alta em DPI. Essa propriedade é um único valor. Essa não é uma lista de todas as resoluções que podem ser geradas pelo dispositivo. Em vez disso, essa é a resolução da ótica do dispositivo. O minidriver cria e mantém essa propriedade. Essa propriedade é necessária para todos os scanners.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade não é suportada pelo Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Resolução óptica vertical. Resolução óptica vertical com suporte mais alta em DPI. Essa propriedade é um único valor. Essa não é uma lista de todas as resoluções geradas pelo dispositivo. Em vez disso, essa é a resolução da ótica do dispositivo. O minidriver cria e mantém essa propriedade. Essa propriedade é necessária para todos os scanners.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td ><p>Contém a configuração de orientação atual. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo define a <strong>WIA_DPS_ORIENTATION</strong> para definir a orientação original de uma página ou imagem a ser adquirida. Para obter informações sobre como usar WIA_DPS_ORIENTATION, consulte <strong>WIA_DPS_PAGE_SIZE</strong></p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Leitura/Gravação, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<td>PAISAGEM</td>
<td>Rotação de 90 graus no sentido horário, em relação à orientação PORTRAIT.</td>
</tr>
<tr class="even">
<td>RETRATO</td>
<td>0 graus.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Rotação de 180 graus no sentido horário, em relação à orientação PORTRAIT.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Rotação de 270 graus no sentido horário, em relação à orientação PORTRAIT.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Consulte também</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td ><p>Cor usada para preencher quando não há dados de imagem suficientes para preencher um buffer solicitado. Essa propriedade é implementada para scanners que padram o buffer. Essa propriedade é opcional para todos os scanners. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>O formato das informações de cor é <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD.</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade não é suportada pelo Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a altura, em milésimos de polegada, da página selecionada no momento. O minidriver cria e mantém a <strong>WIA_DPS_PAGE_HEIGHT</strong> propriedade . Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo digitalizada. Se <strong>as configurações</strong> de extensão são diferentes dos tamanhos de página conhecidos, essa propriedade informa a altura da página cuja propriedade WIA_DPS_PAGE_SIZE é definida como WIA_PAGE_CUSTOM (que é um valor da propriedade <strong>WIA_DPS_PAGE_SIZE).</strong> <strong>WIA_DPS_PAGE_HEIGHT</strong> deve estar em sincronia com <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que informa a altura, em pixels, da página a ser digitalizada.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade não é suportada pelo Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o tamanho da página que está selecionada para ser digitalizada no momento. Para selecionar as dimensões da página a ser digitalizada, um aplicativo define essa propriedade. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Leitura/Gravação, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<td>8267 X 11692 (orientação RETRATO)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Definidos pelos valores das propriedades <strong>WIA_DPS_PAGE_HEIGHT</strong> e <strong>WIA_DPS_PAGE_WIDTH</strong> dados</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (orientação RETRATO)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>O valor da <a href="-wia-wiaitempropscanneritem.md"><strong>propriedade WIA_IPS_ORIENTATION</strong></a> determina a orientação da página selecionada no momento. As <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> relatório das dimensões da página, em milésimos de polegada. Observe que essas propriedades devem estar de acordo com <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, que contêm as dimensões da página em pixels. Os valores válidos do tipo WIA_PROP_LIST devem depender de configurações válidas da <strong>propriedade WIA_IPS_ORIENTATION</strong> dados. Se o dispositivo não puder verificar documentos orientados a paisagem com uma configuração de WIA_PAGE_A4, WIA_PAGE_A4 não deverá aparecer na lista de valores válidos para a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> <strong>quando WIA_IPS_ORIENTATION</strong> estiver definido como LANSCAPE.</p>
<p>Se um <strong></strong> aplicativo WIA_DPS_PAGE_SIZE um valor diferente de WIA_PAGE_CUSTOM, o minidriver deverá ajustar os valores de <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> às dimensões da página em milésimos de polegada. Ele também deve ajustar os valores <a href="-wia-wiaitempropscanneritem.md"><strong>de WIA_IPS_XEXTENT</strong></a> e <strong>WIA_IPS_YEXTENT</strong> às dimensões da página em pixels.</p>
<p>Se uma configuração de extensão (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> ou <strong>WIA_IPS_YEXTENT</strong>) for alterada para um valor que não corresponder à configuração de tamanho de página atual, o minidriver deverá alterar o valor da propriedade <strong>WIA_DPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM. O minidriver também deve modificar <strong>WIA_DPS_PAGE_WIDTH</strong> ou <strong>WIA_DPS_PAGE_HEIGHT</strong> de acordo com a nova configuração de extensão.</p>
<p>Se <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> for definido como LANSCAPE, as configurações de extensão serão &quot; invertida. &quot; Por exemplo, se um aplicativo definir <strong>WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_A4, o minidriver deverá definir WIA_DPS_PAGE_WIDTH como 11692 e <strong>WIA_DPS_PAGE_HEIGHT</strong> como 8267. <strong></strong> (O minidriver também deve definir <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> de acordo.) Observe que, <strong>se WIA_DPS_PAGE_SIZE</strong> for definido como WIA_PAGE_CUSTOM, a configuração de orientação não será usada para determinar as dimensões de extensão da página a ser digitalizada.</p>
<p>O minidriver é responsável por garantir que a <a href="-wia-wiaitempropscanneritem.md"><strong>propriedade WIA_IPS_ORIENTATION</strong></a> está em acordo com a área de seleção atual. Se um aplicativo alterar o valor de <strong>WIA_IPS_ORIENTATION</strong> para um inválido para o tamanho da página selecionado no momento, o minidriver deverá alterar o valor de <strong>WIA_DPS_PAGE_SIZE</strong> para um tamanho de página com suporte pelo novo valor de orientação.</p>
<p>Se um aplicativo define a <strong>propriedade WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_CUSTOM, a área de seleção atual não será afetada. O minidriver WIA deve obter o layout da imagem atual, começando com as configurações atuais das propriedades <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> e <strong>WIA_IPS_YPOS</strong> configurações. Se a configuração de tamanho da página resulta em uma área de seleção que está fora da casa do scanner, o minidriver deve ajustar automaticamente os valores das propriedades <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> para configurações válidas. Se as <strong>propriedades WIA_DPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> são definidas ao mesmo tempo e são inválidas quando aplicadas em combinação, o minidriver deve falhar nas configurações do aplicativo retornando um erro em <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvValidateItemProperties</a>. .</p>
<p>Os quatro exemplos a seguir mostram <strong>diferentes WIA_DPS_PAGE_SIZE</strong> cenários.</p>
<ol>
<li>O driver relata as configurações.</li>
<li>Um aplicativo define a <strong>propriedade WIA_DPS_PAGE_SIZE</strong> como WIA_PAGE_LETTER.</li>
<li>Um aplicativo define a <a href="-wia-wiaitempropscanneritem.md"><strong>propriedade WIA_IPS_ORIENTATION</strong></a> como LANSCAPE.</li>
<li>Um aplicativo altera a <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> para um valor menor.</li>
</ol>
<p><strong>Exemplo 1: o minidriver relata as configurações</strong></p>
<p>No exemplo a seguir, o minidriver define uma área de seleção personalizada antes de um aplicativo define as propriedades do WIA. Nesse caso, a área de seleção representa todo o flatbed.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Exemplo 2: um aplicativo define a propriedade</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>como WIA_PAGE_LETTER</strong></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Exemplo 3: um aplicativo define a propriedade</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>como LANSCAPE</strong></p>
<p>A casa física deve ser capaz de adquirir uma página que estava originalmente na orientação paisagem.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Exemplo 4: um aplicativo altera a propriedade</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>para um<strong>valor menor</strong>  </p>
<p>No exemplo a seguir, um aplicativo altera a <a href="-wia-wiaitempropscanneritem.md"><strong>propriedade WIA_IPS_XEXTENT</strong></a> para 1000. O minidriver deve assumir que o novo valor contido no <strong>WIA_IPS_XEXTENT</strong> não é mais <strong></strong> válido para a propriedade <strong>WIA_DPS_PAGE_SIZE</strong> e, portanto, deve alterar WIA_DPS_PAGE_SIZE para WIA_PAGE_CUSTOM. O minidriver também deve ajustar <strong>WIA_DPS_PAGE_WIDTH</strong>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td ><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade não é suportada pelo Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a largura da página atual selecionada, em milésimos de polegada. Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo digitalizada. Se as configurações de extensão são diferentes dos tamanhos de página conhecidos, essa propriedade informa a largura da página cuja propriedade <strong>WIA_DPS_PAGE_SIZE</strong> é definida como WIA_PAGE_CUSTOM. <strong>WIA_DPS_PAGE_WIDTH</strong> deve estar em sincronia com o valor de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que informa a largura, em pixels, da página a ser digitalizada. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade não é suportada pelo Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o número atual de páginas a serem adquiridas de um feed de documentos automático. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>; Acesso: Leitura/Gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero até o número máximo de páginas que o feedr de documentos pode conter)</p>
<p>Um aplicativo lê essa propriedade para determinar a capacidade da página do feeder de documentos. O aplicativo também define essa propriedade como o número de páginas que ele examinará.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Se o modo duplex estiver habilitado<strong>(WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> será definido como FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> ainda é igual ao número de páginas a verificar.
</blockquote>
</div>
<div>
 
</div>
<p>Uma folha de papel conterá automaticamente duas páginas se DUPLEX estiver habilitado, mesmo se o lado de fundo da página estiver em branco.</p>
<p>Definir <strong>WIA_DPS_PAGES</strong> como 1 faz com que um scanner processe um dos lados da página. É recomendável que, se um scanner não puder verificar apenas um lado de uma página enquanto estiver no modo duplex, o valor válido do WIA_DPS_PAGES para <strong>o</strong> membro Inc da estrutura WIA_PROPERTY_INFO deverá ser alterado para 2. Esse valor sinaliza ao aplicativo que ele deve solicitar páginas em múltiplos de dois. Um valor de zero significa que <em>todas</em> as páginas que estão carregadas no feed de documentos devem ser examinadas.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td ><p>Especifica a cor da placa na parte traseira da folha a ser digitalizada. Essa propriedade é opcional para scanners que têm uma placa. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>O formato das informações de cor é <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD.</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade não é suportada pelo Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica o modo de visualização de um dispositivo. Um aplicativo define essa propriedade para colocar o dispositivo em um modo de visualização.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Leitura/Gravação, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<td ><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td ><p>Contém um valor que indica se o scanner armazenará páginas em cache em um buffer do scanner antes de enviá-las ao aplicativo.</p>
<p>Um valor de zero desabilita a verificação antecipada e nenhuma página será digitalizada com antecedência. Fazer transferências de dados normais no item de verificação antecipada em buffer recupera as páginas em buffer. As propriedades do WIA não podem ser alteradas durante uma operação de verificação antecipada. Esta propriedade é opcional.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Leitura/Gravação, Valores válidos: <a href="-wia-property-attributes.md"></a> WIA_PROP_RANGE de zero ao número máximo de páginas que o feed de documentos pode conter.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade é suportada apenas pelo Windows 7 e posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Indica a fonte de entrada (flatbed, o feeder automático de documentos ou o adaptador de verificação de arquivos) a ser verificado ou o local de armazenamento do onde transferir dados.</p>
<p>Um evento de verificação notifica o aplicativo de que o usuário iniciou uma verificação, mas o evento não fornece o nome do item WIA que representa a fonte de entrada. O manipulador de eventos do aplicativo pode consultar a propriedade WIA_DPS_SCAN_AVAILABLE_ITEM do item raiz para obter o nome do item de origem de entrada.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Leitura/Gravação, Valores válidos: <a href="-wia-property-attributes.md"></a> WIA_PROP_RANGE de zero ao número máximo de páginas que o feed de documentos pode conter.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade é suportada apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a ID de serviço de um dispositivo de scanner de Serviços Web. O mini driver WIA 2.0 cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o registro, o alinhamento e a detecção de borda, para documentos que são colocados no flatbed. O minidriver cria e mantém essa propriedade. Essa propriedade indica como a planilha é posicionada horizontalmente na cabeça de verificação de um verificador portátil ou alimentado por planilha. A propriedade é usada para prever o local em que um documento é colocado no meio da cabeça de verificação.</p>
<p>Para scanners que suportam mais de um cabeça de verificação, essa propriedade é relativa ao cabeça de verificação mais alto. Essa propriedade é obrigatória para scanners de folha,alimentados por rolagem e portáteis.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>A planilha é posicionada à esquerda em relação à cabeça de verificação.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>A planilha é centralizada na cabeça de verificação.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>A planilha é posicionada à direita em relação à cabeça de verificação.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade não é suportada pelo Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica se um item precisa de um controle de visualização exibido para o usuário. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>Mostrar um controle de visualização para o usuário, pois esse dispositivo pode executar uma visualização.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>Não mostre um controle de visualização para o usuário, pois esse dispositivo não pode executar uma visualização.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade é suportada apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Usado pelo serviço WIA para informar o mini driver sobre o nome da conta de usuário (incluindo o nome de domínio de rede quando aplicável) da sessão na qual o aplicativo WIA atual está em execução.</p>
<p>Essa é uma propriedade de item raiz, gerenciada pelo serviço WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o registro, o alinhamento vertical e a detecção de borda, para documentos colocados no flatbed. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as três constantes que são válidas com essa propriedade.. </p>
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
<td>O papel é mais justificado.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>O papel é centralizado.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>O papel é justificado na parte inferior.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Consulte também</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a altura máxima, em milésimos de polegada, que é digitalizada no eixo vertical (Y) da placa de um scanner de flatbed na resolução atual. Essa propriedade também se aplica a feeders de documentos automáticos, que movem planilhas para a placa de um scanner de flatbed para verificação. Essa propriedade é obrigatória para scanners que têm uma placa. Outros tipos de scanner implementarão a <strong>propriedade WIA_DPS_VERTICAL_SHEET_FEED_SIZE.</strong></p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Não há suporte para essa propriedade com Windows Vista e posterior. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a altura máxima, em milésimos de polegada, que é digitalizada no eixo vertical (Y) de um verificador de feed de folha ou de mão na resolução atual. Essa propriedade também se aplica a feeds de documentos automáticos que digitalizar sem mover planilhas para a placa de um scanner de flatbed. Essa propriedade é obrigatória para scanners de folha de alimentação. Os scanners de rolagem e de mão não devem implementar essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Acesso: Somente Leitura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da área de \[ trabalho XP\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
