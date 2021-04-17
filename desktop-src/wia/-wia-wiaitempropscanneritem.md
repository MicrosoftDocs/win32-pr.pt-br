---
description: As constantes a seguir especificam o conjunto válido de propriedades do item de scanner WIA (aquisição de imagem do Windows).
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Constantes da propriedade item do scanner WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aa3b1cc4ae14a9460a24f652a9599035cacca2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811657"
---
# <a name="scanner-wia-item-property-constants"></a>Constantes da propriedade item do scanner WIA

As constantes a seguir especificam o conjunto válido de propriedades do item de scanner WIA (aquisição de imagem do Windows).

O prefixo " \_ IPS WIA \_ " indica uma propriedade de item para dispositivos de scanner e é a Convenção de nomenclatura usada em C/C++. Para fins de script, essas constantes usam o prefixo "ScannerPicture" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.



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
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
<br/> Ativa ou desativa a distorção automática.<br/> Opcional somente para WIA_CATEGORY_FEEDER.<br/> Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> A tabela a seguir tem as constantes que são válidas com essa propriedade. 
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_AUTO_DESKEW_ON</td>
<td>Ativar a distorção automática.</td>
</tr>
<tr class="even">
<td>WIA_AUTO_DESKEW_OFF</td>
<td>Desative a distorção automática.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </dl></td>
<td style="text-align: left;"><p>Os valores de brilho da imagem disponíveis no scanner.</p>
<p>Contém a configuração de brilho do hardware atual para o dispositivo. Um aplicativo define essa propriedade como o valor de brilho do hardware. O minidriver cria e mantém essa propriedade.</p>
<p>Os valores devem ser mapeados em um intervalo de-1000 até 1000, em que 1000 corresponde ao brilho máximo, 0 corresponde ao brilho normal e-1000 corresponde ao brilho mínimo.</p>
<p>Necessário para todos os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM. Opcional, mas recomendado, para itens de WIA_CATEGORY_FINISHED_FILE que dão suporte a visualizações.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </dl></td>
<td style="text-align: left;"><p>Contém a configuração de contraste de hardware atual para um dispositivo. Um aplicativo define essa propriedade como o valor de contraste do hardware. O minidriver cria e mantém essa propriedade.</p>
<p>Os valores devem ser mapeados em um intervalo de-1000 até 1000, em que-1000 corresponde ao contraste mínimo, 0 corresponde ao contraste normal e 1000 corresponde ao contraste máximo.</p>
<p>Necessário para todos os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM. Opcional, mas recomendado, para itens de WIA_CATEGORY_FINISHED_FILE que dão suporte a visualizações.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </dl></td>
<td style="text-align: left;"><p>Contém as configurações de tentativa atuais. O minidriver cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM. Não há suporte para itens de WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong> acesso: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></p>
<p>O driver os usa para predefinir Propriedades de item com base no uso pretendido da imagem por um aplicativo. Isso pode incluir, por exemplo, a qualidade máxima, o tamanho mínimo e assim por diante.</p>
<p>O driver escolhe a profundidade de bits, em pontos por polegada, e outras configurações que ele determina são apropriadas para a intenção selecionada. Cabe ao aplicativo ler as configurações atuais para determinar quais propriedades foram alteradas. Um aplicativo define essa propriedade para definir automaticamente as propriedades do WIA para uma tentativa de aquisição específica. Essa propriedade é necessária para todos os scanners.</p>
<p>Um aplicativo define essa propriedade para definir automaticamente as propriedades de WIA para uma intenção de aquisição específica</p>
<div class="alert">
<blockquote>
[!Note]<br />
Os sinalizadores podem ser combinados com um operador <strong>OR bit a</strong> bit, mas uma imagem não pode ser escala de cinza e cor.
</blockquote>
</div>
<div>
 
</div>
<p>Essa propriedade é necessária para todos os scanners.</p>
<p>A tabela a seguir contém os sinalizadores de tipo de imagem e suas definições. Esses sinalizadores são usados para definir qual tipo de imagem é pretendido: cor, escala de cinza e assim por diante.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Sinalizadores de tipo de imagem pretendidos</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_NONE</td>
<td>Valor padrão. Nenhuma tentativa foi especificada.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_COLOR</td>
<td>O aplicativo pretende preparar o dispositivo para uma verificação de cor.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_GRAYSCALE</td>
<td>O aplicativo pretende preparar o dispositivo para uma verificação em tons de cinza.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_TEXT</td>
<td>O aplicativo pretende preparar o dispositivo para verificar o texto.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_MASK</td>
<td>Máscara para todos os sinalizadores de tipo de imagem.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>A tabela a seguir contém os sinalizadores de qualidade e tamanho e suas definições. Esses sinalizadores são usados para definir o nível de qualidade pretendido.</p>

<table>
<thead>
<tr class="header">
<th>Tamanho de imagem pretendido/sinalizadores de qualidade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_MINIMIZE_SIZE</td>
<td>O aplicativo pretende preparar o dispositivo para verificar uma imagem que resulte em uma pequena verificação.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_MAXIMIZE_QUALITY</td>
<td>O aplicativo pretende preparar o dispositivo para verificar uma imagem de alta qualidade.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_SIZE_MASK</td>
<td>Esse sinalizador é uma máscara para todos os sinalizadores de tamanho/qualidade.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_BEST_PREVIEW</td>
<td>O aplicativo pretende preparar o dispositivo para verificar uma versão prévia.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o número de pixels na direção x de WIA_IPS_XPOS para a coordenada x do canto superior da imagem a ser deinclinada. Portanto, ele descreve, em conjunto com WIA_IPS_DESKEW_Y, onde os dois cantos superiores da imagem distorcida estão localizados dentro do retângulo delimitador definido por WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT e WIA_IPS_YEXTENT. sua propriedade será implementada pelo driver do scanner se ele der suporte à desalinhamento.</p>
<p>Os valores válidos para WIA_IPS_DESKEW_X devem estar entre 0 e (WIA_IPS_XEXTENT-1). Um valor de 0 significa que nenhuma distorção deve ser executada.</p>
<p>Essa propriedade é opcional para itens das categorias WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM; e não está disponível para WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER itens.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o número de pixels na direção y de WIA_IPS_YPOS para a coordenada y do canto mais à esquerda da imagem a ser deinclinada. Portanto, ele descreve, em conjunto com WIA_IPS_DESKEW_X, onde os dois cantos superiores da imagem distorcida estão localizados dentro do retângulo delimitador definido por WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT e WIA_IPS_YEXTENT. Essa propriedade é implementada pelo driver do verificador se ele der suporte à distorção.</p>
<p>Os valores válidos para WIA_IPS_DESKEW_Y devem estar entre 0 e (WIA_IPS_YEXTENT-1). Um valor de 0 significa que nenhuma distorção deve ser executada.</p>
<p>Essa propriedade é opcional para itens das categorias WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM; e não está disponível para WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER itens.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a origem e o modo de aquisição do scanner atual. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar a fonte de aquisição atual do scanner ou para gravar essa propriedade para definir a origem e o modo do verificador. Além disso, os aplicativos usam essa propriedade para habilitar e desabilitar a funcionalidade do duplexador.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DUPLEX</td>
<td>Examinar usando operações do duplex. Verifique ambos os lados do documento usando configurações comuns configuradas para o item do alimentador (WIA_CATEGORY_FEEDER). DUPLEX e ADVANCE_DUPLEX não podem ser ambos definidos.</td>
</tr>
<tr class="even">
<td>ADVANCED_DUPLEX</td>
<td>Digitalizar usando configurações individuais configuradas para cada item de alimentador filho (WIA_CATEGORY_FEEDER_FRONT e WIA_CATEGORY_FEEDER_BACK). DUPLEX e ADVANCE_DUPLEX não podem ser ambos definidos.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Primeiro examine a frente do documento. Esse valor é válido quando DUPLEX ou ADVANCED_DUPLEX é definido.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Primeiro examine a parte de trás do documento. Esse valor é válido quando DUPLEX ou ADVANCED_DUPLEX é definido.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Verificar somente a frente.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Verifique apenas o verso. Esse valor é válido quando DUPLEX ou ADVANCED_DUPLEX é definido.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Habilita a especificação de um anexo de verificação de filme específico quando há mais de um.</p>
<p>Essa propriedade é necessária para os itens de WIA_CATEGORY_FILM quando há vários itens de verificação de filme. Se o dispositivo der suporte a apenas um item de filme do scanner raiz, essa propriedade será opcional.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Valores permitidos: o BSTR deve estar na forma de @ResourceBinary ,- <ResourceID> para permitir que a localização como essa cadeia de caracteres seja exposta ao usuário por meio da interface do usuário de verificação de filme.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Habilita a configuração da verificação de filme atual.</p>
<p>Essa propriedade é necessária para o item de WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FILM_COLOR_SLIDE</td>
<td>Digitalizar um slide de cor.</td>
</tr>
<tr class="even">
<td>WIA_FILM_COLOR_NEGATIVE</td>
<td>Verificar se há uma cor negativa.</td>
</tr>
<tr class="odd">
<td>WIA_FILM_BW_NEGATIVE</td>
<td>Verificar se há um negativo preto e branco.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td style="text-align: left;"><p>Reservado para uso futuro e não é implementado neste momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica quantos itens são armazenados no item de WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Ativa ou desativa a lâmpada do scanner.</p>
<p>Opcional para os itens WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM e recomendado para WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_LAMP_ON</td>
<td>Ligue a lâmpada.</td>
</tr>
<tr class="even">
<td>WIA_LAMP_OFF</td>
<td>Desative a lâmpada.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Define o tempo máximo para manter a lâmpada quando o scanner não está sendo usado.</p>
<p>Opcional para os itens WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM e recomendado para WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_UI4</strong>, Access: leitura/gravação, valores válidos: 0-0xFFF segundos</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a largura máxima, em milésimos de polegada, que é verificada no eixo horizontal (X) na resolução atual. Essa pode ser a largura do alimentador de planilhas ou da base de digitalização, de acordo com o tipo de item.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a altura máxima, em milésimos de polegada, que é verificada no eixo vertical (Y) na resolução atual. Essa pode ser a altura do alimentador de planilhas ou da base de digitalização, de acordo com o tipo de item.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a largura mínima, em milésimos de polegada, que é verificada no eixo horizontal (X) na resolução atual.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica a altura mínima, em milésimos de polegada, que é verificada no eixo vertical (Y) na resolução atual.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </dl></td>
<td style="text-align: left;"><p>Reservado para uso futuro e não é implementado neste momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Resolução óptica horizontal. Resolução óptica horizontal mais alta com suporte em DPI. Essa propriedade é um único valor. Esta não é uma lista de todas as resoluções que podem ser geradas pelo dispositivo. Em vez disso, essa é a resolução da fibra óptica do dispositivo. O minidriver cria e mantém essa propriedade. Essa propriedade é necessária para todos os itens.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Resolução óptica vertical. Resolução óptica vertical com suporte mais alta em DPI. Essa propriedade é um único valor. Essa não é uma lista de todas as resoluções que são geradas pelo dispositivo. Em vez disso, essa é a resolução da fibra óptica do dispositivo. O minidriver cria e mantém essa propriedade. Essa propriedade é necessária para todos os itens.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </dl></td>
<td style="text-align: left;"><p>Especifica a orientação atual dos documentos a serem examinados. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo define essa propriedade para definir a orientação original de uma página ou imagem a ser adquirida. Para obter informações sobre como usar WIA_IPS_ORIENTATION, consulte <strong>WIA_IPS_PAGE_SIZE</strong>.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION se refere à posição do documento a ser examinado na base do scanner ou no alimentador. É a orientação do documento em relação à direção da verificação. WIA_IPS_ROTATION se refere à rotação aplicada à imagem depois que ela é verificada, logo antes de a imagem ser transferida para o aplicativo.
</blockquote>
</div>
<div>
 
</div>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as quatro constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ORIENTAÇÕES</td>
<td>0 graus.</td>
</tr>
<tr class="even">
<td>AMBIENTE</td>
<td>rotação no sentido anti-horário de 90 graus, em relação à orientação retrato.</td>
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

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o tamanho da página que está atualmente definida para ser verificada. Um aplicativo define essa propriedade para selecionar as dimensões da página a ser verificada. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Para obter as constantes que podem ser usadas com essa propriedade, consulte <a href="-wia-wia2-pagesizeconstants.md"><strong>constantes de tamanho de página WIA 2,0</strong></a>. Observe esses tamanhos não fixos, em particular: </p>
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_CUSTOM</td>
<td>Definido pelos valores das propriedades <strong>WIA_IPS_PAGE_HEIGHT</strong> e <strong>WIA_IPS_PAGE_WIDTH</strong> .</td>
</tr>
<tr class="even">
<td>WIA_PAGE_AUTO</td>
<td>O tamanho da página é determinado automaticamente pelo dispositivo.</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_CUSTOM_BASE</td>
<td>Um tamanho de página personalizado cujas dimensões já são conhecidas pelo aplicativo e o driver de dispositivo.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>O valor da propriedade <strong>WIA_IPS_ORIENTATION</strong> determina a orientação da página atualmente selecionada. As propriedades <strong>WIA_IPS_PAGE_WIDTH</strong> e <strong>WIA_IPS_PAGE_HEIGHT</strong> relatam as dimensões da página, em milésimos de polegada. Essas propriedades devem estar em acordo com <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, que contêm as dimensões da página em pixels.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Os valores válidos do tipo WIA_PROP_LIST dependem das configurações válidas da propriedade <strong>WIA_IPS_ORIENTATION</strong> . Se, por exemplo, o dispositivo não puder verificar documentos orientados a paisagem com uma configuração de WIA_PAGE_A4, WIA_PAGE_A4 não será um valor válido para a propriedade <strong>WIA_IPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> estiver definido como paisagem.
</blockquote>
</div>
<div>
 
</div>
<p>Se um aplicativo definir <strong>WIA_IPS_PAGE_SIZE</strong> para qualquer valor diferente dos três na tabela acima, o minidriver deverá ajustar os valores de <strong>WIA_IPS_PAGE_WIDTH</strong> e <strong>WIA_IPS_PAGE_HEIGHT</strong> às dimensões da página em milésimos de uma polegada. Ele também deve ajustar os valores de <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> às dimensões da página em pixels.</p>
<p>Se uma configuração de extensão (<strong>WIA_IPS_XEXTENT</strong> ou <strong>WIA_IPS_YEXTENT</strong>) for alterada para um valor que não corresponda à configuração de tamanho de página atual, minidriver deverá alterar o valor da propriedade <strong>WIA_IPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM. O minidriver também deve modificar <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> ou <strong>WIA_IPS_PAGE_HEIGHT</strong> de acordo com a nova configuração de extensão.</p>
<p>Se <strong>WIA_IPS_ORIENTATION</strong> for definido como paisagem, as configurações de extensão serão trocadas em relação aos seus valores usuais. Por exemplo, se um aplicativo definir <strong>WIA_IPS_PAGE_SIZE</strong> como WIA_PAGE_A4, o minidriver definirá <strong>WIA_IPS_PAGE_WIDTH</strong> como 11692 e <strong>WIA_IPS_PAGE_HEIGHT</strong> como 8267. (O minidriver também deve ajustar <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> de acordo.)</p>
<div class="alert">
<blockquote>
[!Note]<br />
Se <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> for definido como WIA_PAGE_CUSTOM, a configuração de orientação não será usada para determinar as dimensões de extensão da página a ser examinada.
</blockquote>
</div>
<div>
 
</div>
<p>O minidriver é responsável por garantir que a propriedade <strong>WIA_IPS_ORIENTATION</strong> esteja em contrato com a área de seleção atual. Se um aplicativo alterar o valor de <strong>WIA_IPS_ORIENTATION</strong> para um que seja inválido para o tamanho de página selecionado no momento, o minidriver deverá alterar o valor de <strong>WIA_IPS_PAGE_SIZE</strong> para um tamanho de página com suporte no novo valor de orientação.</p>
<p>Se um aplicativo definir a propriedade <strong>WIA_IPS_PAGE_SIZE</strong> como WIA_PAGE_CUSTOM, a área de seleção atual não será afetada. O minidriver WIA deve obter o layout da imagem atual, começando com as configurações atuais das propriedades <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> . Se a configuração tamanho da página resultar em uma área de seleção que está fora do ambiente do scanner, o minidriver deverá ajustar automaticamente os valores das propriedades <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> para as configurações válidas. Se as propriedades <strong>WIA_IPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> forem definidas ao mesmo tempo e forem inválidas quando aplicadas em combinação, o minidriver deverá falhar as configurações do aplicativo retornando um erro no <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>.</p>
<p>Os quatro exemplos a seguir mostram diferentes cenários de <strong>WIA_IPS_PAGE_SIZE</strong> .</p>
<ol>
<li>O driver relata as configurações.</li>
<li>Um aplicativo define a propriedade <strong>WIA_IPS_PAGE_SIZE</strong> como WIA_PAGE_LETTER.</li>
<li>Um aplicativo define a propriedade <strong>WIA_IPS_ORIENTATION</strong> como paisagem.</li>
<li>Um aplicativo altera a propriedade <strong>WIA_IPS_XEXTENT</strong> para um valor menor.</li>
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
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
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
<p><strong>Exemplo 2: um aplicativo define a</strong> <strong></strong><strong>Propriedade WIA_IPS_PAGE_SIZE como WIA_PAGE_LETTER</strong>  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
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
<p><strong>Exemplo 3: um aplicativo define a</strong> <strong></strong><strong>Propriedade WIA_IPS_ORIENTATION como paisagem</strong>  </p>
<p>A base física deve ser capaz de adquirir uma página que estava originalmente na orientação paisagem.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
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
<p><strong>Exemplo 4: um aplicativo altera a</strong> <strong></strong> <strong>Propriedade WIA_IPS_XEXTENT para um valor menor</strong></p>
<p>No exemplo a seguir, um aplicativo altera a propriedade <strong>WIA_IPS_XEXTENT</strong> para 1000. O minidriver deve assumir que o novo valor contido no <strong>WIA_IPS_XEXTENT</strong> não é mais válido para a propriedade <strong>WIA_IPS_PAGE_SIZE</strong> e, portanto, deve alterar <strong>WIA_IPS_PAGE_SIZE</strong> para WIA_PAGE_CUSTOM. O minidriver também deve ajustar <strong>WIA_IPS_PAGE_WIDTH</strong>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
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
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a altura, em milésimos de polegada, da página atualmente selecionada. O minidriver cria e mantém a propriedade <strong>WIA_IPS_PAGE_HEIGHT</strong> . Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo examinada. Se as configurações de extensão forem diferentes dos tamanhos de página conhecidos, essa propriedade relatará a altura da página cujo <strong>WIA_IPS_PAGE_SIZE</strong> Propriedade está definida como WIA_PAGE_CUSTOM (que é um valor da propriedade <strong>WIA_IPS_PAGE_SIZE</strong> ). <strong>WIA_IPS_PAGE_HEIGHT</strong> deve estar em sincronia com <strong>WIA_IPS_XEXTENT</strong>, que relata a altura, em pixels, da página a ser verificada.</p>
<p>Essa propriedade é necessária para itens de WIA_CATEGORY_FEEDER.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém a largura da página atual selecionada, em milésimos de polegada. Um aplicativo lê essa propriedade para determinar as dimensões físicas da página que está sendo examinada. Se as configurações de extensão forem diferentes de tamanhos de página conhecidos, essa propriedade relatará a largura da página cuja propriedade <strong>WIA_IPS_PAGE_SIZE</strong> está definida como WIA_PAGE_CUSTOM. <strong>WIA_IPS_PAGE_WIDTH</strong> deve estar em sincronia com o valor de <strong>WIA_IPS_XEXTENT</strong>, que relata a largura, em pixels, da página a ser verificada. O minidriver cria e mantém essa propriedade.</p>
<p>Essa propriedade é necessária para itens de WIA_CATEGORY_FEEDER.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Contém o número atual de páginas a serem adquiridas de um alimentador automático de documentos. O minidriver cria e mantém essa propriedade.</p>
<p>Tipo: <strong>VT_I4</strong>; Acesso: leitura/gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> isso é zero por meio do número máximo de páginas que o verificador pode verificar. O valor é ALL_PAGES (= 0) se o verificador pode verificar continuamente.</p>
<p>Um aplicativo lê essa propriedade para determinar a capacidade da página do alimentador de documentos. O aplicativo também define essa propriedade como o número de páginas que ele vai verificar.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Se o modo duplex estiver habilitado (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> é definido como alimentador | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> ainda é igual ao número de páginas a serem verificadas.
</blockquote>
</div>
<div>
 
</div>
<p>Uma folha de papel conterá automaticamente duas páginas se o DUPLEX estiver habilitado, mesmo se o lado do verso da página estiver em branco.</p>
<p>Definir <strong>WIA_IPS_PAGES</strong> como 1 faz com que um scanner processe um lado da página. Recomendamos que, se um scanner não conseguir verificar apenas um lado de uma página enquanto estiver no modo duplex, você alterará o valor <strong>WIA_IPS_PAGES</strong> para o membro Inc do membro de intervalo da estrutura de WIA_PROPERTY_INFO para 2. Esse valor sinaliza ao aplicativo que ele deve solicitar páginas em múltiplos de dois. Um valor de ALL_PAGES (= 0) significa que <em>todas as</em> páginas atualmente carregadas no alimentador de documentos serão verificadas.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </dl></td>
<td style="text-align: left;"><p>Contém a configuração atual para pixels brancos e pretos. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê esse valor para determinar o valor de branco ou preto (dependendo do que o aplicativo está fazendo).</p>
<p>Necessário para todos os itens habilitados para aquisição ou armazenados; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Não há suporte para itens de WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>; Acesso: leitura/gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Se o dispositivo puder ser definido como apenas um único valor, crie um tipo de WIA_PROP_LIST e coloque o valor válido nele.</p>
<p>A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PHOTO_WHITE_0</td>
<td>O branco é 0 e o preto é 1.</td>
</tr>
<tr class="even">
<td>WIA_PHOTO_WHITE_1</td>
<td>O branco é 1 e o preto é 0.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Indica o modo de visualização de um dispositivo. Um aplicativo define essa propriedade para posicionar o dispositivo em um modo de visualização.</p>
<p>Essa propriedade é necessária para os itens WIA_CATEGORY_FLATBED e WIA_CATEGORY_FILM, opcional para o item WIA_CATEGORY_FEEDER.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. </p>
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
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica se a imagem de visualização existente pode ser atualizada durante uma visualização de imagem (em resposta a uma alteração nas propriedades WIA_IPA_DATATYPE ou WIA_IPA_DEPTH).</p>
<p>Essa propriedade é opcional para todos os itens habilitados para aquisição que dão suporte a verificações de visualização; ou seja, há suporte para WIA_IPS_PREVIEW com WIA_PREVIEW_SCAN. Isso inclui itens de tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ADVANCED_PREVIEW</td>
<td>A atualização da imagem existente é possível.</td>
</tr>
<tr class="even">
<td>WIA_BASIC_PREVIEW</td>
<td>Outra verificação de visualização deve ser executada porque não é possível atualizar a imagem existente.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </dl></td>
<td style="text-align: left;"><p>Contém a configuração de rotação atual, se for implementada. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo define essa propriedade para informar ao driver quanto (se houver) para girar a imagem antes que o driver a retorne ao aplicativo.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION se refere à posição do documento a ser examinado na base do scanner ou no alimentador. É a orientação do documento em relação à direção da verificação. WIA_IPS_ROTATION se refere à rotação aplicada à imagem depois que ela é verificada, logo antes de a imagem ser transferida para o aplicativo.
</blockquote>
</div>
<div>
 
</div>
<p>O minidriver WIA é responsável por girar os dados da imagem antes de enviá-los de volta para o aplicativo. O aplicativo é responsável por verificar os cabeçalhos de imagem para ver os valores recentemente girados.</p>
<p>Existe uma confusão considerável sobre como resolver o efeito de rotação na área de seleção da imagem atual (que é definida pelas propriedades <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> ).</p>
<p>A <em>área de seleção</em> refere-se à área selecionada na base do scanner físico da qual uma imagem é adquirida. <strong>WIA_IPS_ROTATION</strong> não modifica a área de seleção. O driver aplica uma rotação no sentido anti-horário de acordo com <strong>WIA_IPS_ROTATION</strong> somente depois que o driver tiver adquirido a área de seleção apropriada. <strong>WIA_IPS_ROTATION</strong> afeta as dimensões da imagem de saída, portanto, essas dimensões devem ser refletidas no cabeçalho de dados da imagem resultante.</p>
<p>Opcional para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>As constantes de rotação a seguir são definidas.</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ORIENTAÇÕES</td>
<td>O driver não irá girar a imagem.</td>
</tr>
<tr class="even">
<td>AMBIENTE</td>
<td>O driver Tnão gira a imagem 90 graus no sentido anti-horário.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>O driver gira a imagem 180 graus no sentido anti-horário.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>O driver gira a imagem 270 graus no sentido anti-horário.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica se o aplicativo deve usar o filtro de segmentação do driver para verificação de várias regiões. WIA_IPS_SEGMENTATION deve ser implementado para itens de WIA_CATEGORY_FLATBED e WIA_CATEGORY_FILM se eles suportarem a criação de itens filho com um filtro de segmentação ou se o próprio driver criar itens filho para os quadros fixos.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_USE_SEGMENTATION_FILTER</td>
<td>O aplicativo deve usar o filtro de segmentação para verificação de várias regiões.</td>
</tr>
<tr class="even">
<td>WIA_DONT_USE_SEGMENTATION_FILTER</td>
<td>O driver cria os próprios itens filho para verificação de várias regiões. Esse é geralmente o caso se o verificador usar quadros fixos para essa finalidade.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
É possível que um driver venha a vir com um filtro de segmentação, mas ainda tem WIA_IPS_SEGMENTATION definido como WIA_DONT_USE_SEGMENTATION_FILTER para um de seus itens (como, o item de WIA_CATEGORY_FILM). Esse pode ser o caso se o verificador usar quadros fixos para verificação de filmes, mas não para verificação regular de itens de WIA_CATEGORY_FLATBED.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
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
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Indica se um item precisa de um controle de visualização exibido para o usuário. O minidriver cria e mantém essa propriedade.</p>
<p>Opcional para todos os itens habilitados para transferência. Normalmente, isso é apenas itens das categorias WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e WIA_CATEGORY_FINISHED_FILE.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. </p>
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
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica se o aplicativo (ou os filtros) pode criar itens filho sob o item atual.</p>
<p>Opcional para todas as categorias de item habilitado para transferência: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e até mesmo WIA_CATEGORY_FOLDER. (Se o armazenamento não oferecer suporte ao carregamento de novos itens, essa propriedade não deverá ser suportada ou ter suporte com o valor <strong>falso</strong> .)</p>
<p>Os itens que dão suporte a WIA_IPS_SEGMENTATION e WIA_USE_SEGMENTATION_FILTER também devem oferecer suporte a WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION e ter definido como <strong>true</strong>.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <strong>true</strong> e <strong>false</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica o valor de escala de cinza que determina se um pixel será convertido em branco ou preto quando uma imagem for convertida em monodesvio. Os pixels acima do limite se tornam brancos. Os pixels abaixo do limite se tornam brancos.</p>
<p>Essa propriedade é necessária para itens de aquisição que dão suporte a verificações de 1-bpp e que têm a propriedade WIA_IPA_DATATYPE definida como WIA_DATA_THRESHOLD.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica se o driver é capaz de transferir vários itens filho em uma única chamada de transferência.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>O único valor possível para essa propriedade é WIA_TRANSFER_CHILDREN_SINGLE_SCAN. Se esse sinalizador for definido, o driver será capaz de transferir vários itens filho em uma única chamada de transferência. Se o sinalizador não estiver definido, o serviço WIA examinará os itens filho recursivamente e, em seguida, transferirá cada um desses itens.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica o número de bytes a serem carregados para o item.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </dl></td>
<td style="text-align: left;"><p>Especifica o tempo máximo de aquecimento, em milissegundos, que o dispositivo precisa antes de iniciar a operação de verificação. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo pode ler essa propriedade para determinar o tempo máximo de aquecimento para este dispositivo. Em seguida, ele pode apresentar uma &quot; caixa de diálogo aguardando &quot; que o dispositivo fique quente, para permitir que o usuário saiba que uma espera ou pausa pode ocorrer antes de qualquer coisa acontecer.</p>
<p>Esta propriedade é necessária para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </dl></td>
<td style="text-align: left;"><p>Contém a largura atual, em pixels, da imagem selecionada a ser adquirida. Um aplicativo define essa propriedade para marcar a largura de uma área de seleção a ser adquirida. Essa propriedade deve concordar com a propriedade <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> . O minidriver cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </dl></td>
<td style="text-align: left;"><p>Contém a coordenada x, em pixels, do canto superior esquerdo da imagem selecionada. Um aplicativo define essa propriedade para marcar o canto superior esquerdo da área de seleção. O minidriver cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Não há suporte para itens de WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </dl></td>
<td style="text-align: left;"><p>Contém a resolução horizontal atual, em pixels por polegada, para o dispositivo. Um aplicativo define essa propriedade para definir a resolução horizontal. O minidriver cria e mantém essa propriedade.</p>
<p>Se o dispositivo puder ser definido como apenas um único valor, crie um <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo e coloque o valor válido nele. Esse também é um caso em que uma configuração de resolução depende de outra resolução. (A resolução vertical pode depender da resolução horizontal.)</p>
<p>Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Não há suporte para itens de WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Define o dimensionamento horizontal, como uma porcentagem, que pode ser aplicada a imagens digitalizadas dentro do dispositivo de scanner ou de seu driver.</p>
<p>Essa propriedade é opcional para todos os itens habilitados para aquisição; ou seja, os itens dos tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE.</p>
<p>Os valores podem ser de 1 a máximo VT_I4 (0xFFFF). Por exemplo, 100 significa que não há dimensionamento, 050 significa escalar verticalmente para 50% do tamanho do original e 200 significa escalar verticalmente até 200% do tamanho original.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </dl></td>
<td style="text-align: left;"><p>Contém a altura atual, em pixels, da imagem selecionada a ser adquirida. Um aplicativo define essa propriedade para marcar a altura de uma área de seleção. Essa propriedade deve ser aceita com o valor da propriedade <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> . O minidriver cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </dl></td>
<td style="text-align: left;"><p>Coordenada y atual, em pixels, do canto superior esquerdo da imagem selecionada. Um aplicativo define essa propriedade para marcar o canto superior esquerdo da área de seleção. O minidriver cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Não há suporte para itens de WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </dl></td>
<td style="text-align: left;"><p>Contém a resolução vertical atual, em pixels por polegada, para o dispositivo. Um aplicativo define essa propriedade para definir a resolução vertical. O minidriver cria e mantém essa propriedade.</p>
<p>Se o dispositivo puder ser definido como apenas um único valor, crie um <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo e coloque o valor válido nele. Esse também é um caso em que uma configuração de resolução depende de outra resolução. (A resolução horizontal pode depender da resolução vertical.)</p>
<p>Necessário para todos os itens habilitados para aquisição; ou seja, os itens nas categorias: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Não há suporte para itens de WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Essa propriedade tem suporte apenas pelo Windows Vista e posterior.
</blockquote>
</div>
<div>
 
</div>
<p>Define o dimensionamento vertical, como um percentual, que pode ser aplicado a imagens digitalizadas dentro do dispositivo de scanner ou de seu driver.</p>
<p>Essa propriedade é opcional para todos os itens habilitados para aquisição; ou seja, os itens dos tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, acesso: leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE.</p>
<p>Os valores podem ser de 1 a máximo VT_I4 (0xFFFF). Por exemplo, 100 significa que não há dimensionamento, 050 significa escalar verticalmente para 50% do tamanho do original e 200 significa escalar verticalmente até 200% do tamanho original.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




