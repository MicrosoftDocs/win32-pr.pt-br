---
description: As seguintes constantes de propriedade de dispositivo devem ser suportadas por todas as interfaces de interface IWiaItem, IWiaItem2 e IWiaDrvItem, a menos que indicado de outra forma em suas descrições.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Constantes de propriedade de item WIA comuns (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789244"
---
# <a name="common-wia-item-property-constants"></a>Constantes de propriedade de item WIA comuns

As seguintes constantes de propriedade de dispositivo devem ser suportadas por todas as interfaces de interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) e [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , a menos que indicado de outra forma em suas descrições.

O prefixo "WIA \_ IPA \_ " indica uma propriedade de item para todos os dispositivos e é a Convenção de nomenclatura usada em C/C++. Para fins de script, essas constantes usam o prefixo "Picture" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.



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
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </dl></td>
<td style="text-align: left;">Esse sinalizador controla o acesso ao item, bem como se o item é excluído.<br/> Necessário para todos os itens do WIA 2,0.<br/> Tipo: <strong>VT_I4</strong>; Leitura/gravação ou somente leitura, dependendo da capacidade do item de ter seus direitos de acesso alterados; Valores válidos: WIA_PROP_FLAG<br/> A tabela a seguir tem os cinco sinalizadores que são válidos com essa propriedade.<br/> 
<table>
<thead>
<tr class="header">
<th>Direitos de acesso</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ITEM_READ</td>
<td>O item tem acesso somente leitura.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_WRITE</td>
<td>O item tem acesso somente gravação.</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_CAN_BE_DELETED</td>
<td>O item tem acesso somente exclusão.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_RD</td>
<td>WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_RWD</td>
<td>WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </dl></td>
<td style="text-align: left;"><p>Esta propriedade é reservada pelo para uso futuro e não é implementada neste momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Contém o número de bits por canal para a imagem. O minidriver cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens de imagem armazenados ou habilitados para aquisição do WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Contém o tamanho do buffer, em bytes, usado durante uma transferência de dados. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo pode ler essa propriedade para determinar o tamanho do buffer especificado pelo driver para transferências de dados. O serviço WIA também lê essa propriedade para alocar memória para o minidriver durante a transferência de dados</p>
<p>Opcional para todos os itens WIA 2,0 habilitados para transferência.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
A propriedade <strong>WIA_IPA_BUFFER_SIZE</strong> contém é a quantidade mínima de dados que um aplicativo pode solicitar em um determinado momento. Quanto maior o tamanho do buffer, maior será as solicitações para o dispositivo. Isso pode fazer com que o dispositivo pareça lento e sem resposta, pode reduzir o desempenho geral do sistema e pode consumir recursos excessivos. Os tamanhos de buffer que são muito pequenos podem reduzir o desempenho da transferência de dados exigindo muitas solicitações menores. Escolha um tamanho de buffer razoável Considerando o tamanho típico de uma solicitação de dados para seu dispositivo e equilibrando o número de solicitações em relação ao tamanho dessas solicitações.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Contém o número de bytes em uma linha de verificação da imagem. O minidriver cria e mantém essa propriedade.</p>
<p>Opcional para todos os itens WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </dl></td>
<td style="text-align: left;"><p>Contém o número de canais por pixel para a imagem. O minidriver cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens de imagem armazenados ou habilitados para aquisição do WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </dl></td>
<td style="text-align: left;"><p>Esta propriedade é reservada pelo para uso futuro e não é implementada neste momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </dl></td>
<td style="text-align: left;"><p>Contém o tipo de compactação atual usado. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar o tipo de compactação da imagem ou define essa propriedade para definir a configuração de compactação.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. O símbolo <strong>V</strong> indica que a constante tem suporte apenas no Windows Vista e posterior. (Só está disponível por meio da interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Tipo de Compactação</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_COMPRESSION_NONE</td>
<td>Sem compactação. Consulte a <strong>Observação</strong> para obter mais informações.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>Modo de compactação automática. Consulte a <strong>Observação</strong> para obter mais informações.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_BI_RLE4</td>
<td>Compactação RLE4</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_BI_RLE8</td>
<td>Compactação RLE8</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_G3</td>
<td>Compactação do grupo 3</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_G4</td>
<td>Compactação do grupo 4</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG</td>
<td>Compactação JPEG.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_JBIG<strong>V</strong></td>
<td>Compactação JBIG.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG2K<strong>V</strong></td>
<td>Compactação JPEG 2000.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_PNG<strong>V</strong></td>
<td>Compactação de PNG.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p>Quando essa propriedade é WIA_COMPRESSION_NONE e WIA_IPA_FORMAT é WiaImgFmt_PDFA ou WiaImgFmt_XPS; em seguida, WIA_COMPRESSION_NONE significa que o modo de compactação é indefinido e o verificador deve decidir em um modo.</p>
<p>WIA_COMPRESSION_AUTO é um novo valor de propriedade definido para a propriedade WIA_IPA_COMPRESSION. Esse valor é válido para todos os itens de fonte de dados de imagem programável, incluindo o feed e o alimentador. Quando esse valor é suportado pelo mini-driver WIA, o cliente do aplicativo WIA pode definir WIA_IPA_COMPRESSION para habilitar a detecção automática do modo de compactação no dispositivo. WIA_COMPRESSION_AUTO pode trabalhar com e sem que a cor automática completa seja suportada ou habilitada (WIA_DATA_AUTO e WIA_DEPTH_AUTO).</p>
<p>WIA_COMPRESSION_AUTO é mais útil com os formatos de arquivo de transferência que dão suporte a vários tipos de dados e profundidades de bits, como WiaImgFmt_RAW. Para obter mais informações sobre os formatos de arquivo de transferência, consulte WIA_IPA_FORMAT nesta tabela.</p>
<p>Ele é Opitonal para o mini-driver WIA para suporte WIA_COMPRESSION_AUTO. Quando há suporte, o mini-driver WIA nunca deve defini-lo como o valor padrão para WIA_IPA_COMPRESSION; somente o aplicativo WIA pode definir esse valor.</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </dl></td>
<td style="text-align: left;"><p>Contém a configuração de tipo de dados atual para o dispositivo. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar o tipo de dados da imagem. Um aplicativo grava essa propriedade para definir o tipo de dados atual da imagem a ser transferida.</p>
<p>Essa propriedade é necessária para todos os itens WIA 2,0. Ele deve ser leitura/gravação para todos os itens habilitados para aquisição do WIA 2,0 e somente leitura para itens de armazenamento WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>; Acesso para sistemas operacionais anteriores ao Windows Vista: essa propriedade é somente leitura para câmeras e leitura/gravação para scanners; Acesso ao Windows Vista e posterior: essa propriedade é somente leitura para itens WIA_CATEGORY_FOLDER e WIA_CATEGORY_FINISHED_FILE e leitura/gravação para todas as outras categorias de item do WIA 2,0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as seis constantes que são válidas com quando <strong>WIA_IPA_FORMAT</strong> não está definida como WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Tipo de Dados</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_AUTO</td>
<td>Válido para todos os itens de fonte de dados de imagem programável, incluindo o feed e o alimentador. Quando esse valor é suportado pelo mini-driver WIA, o cliente do aplicativo WIA pode definir WIA_IPA_DATATYPE para habilitar a detecção automática de cores no dispositivo. Quando WIA_DATA_AUTO é definido, o mini-driver WIA deve atualizar WIA_IPA_DEPTH no mesmo item para WIA_DEPTH_AUTO (que deve ser um valor com suporte se o dispositivo oferecer suporte à cor automática).<br/> Esse é um valor opcional, mas é necessário quando WIA_DEPTH_AUTO tem suporte para WIA_IPA_DEPTH.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>Os dados de verificação são cores vermelha, verde, azul (RGB). O formato de cor completa é descrito usando as seguintes propriedades de WIA: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>O mesmo que WIA_DATA_COLOR, exceto que os dados são dificados usando o padrão de pontilhamento selecionado no momento.</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>O mesmo que WIA_DATA_COLOR, exceto pelo fato de que o valor de limite é usado ao verificar os dados. Valores de cor sobre o valor de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> são convertidos em brilho completo; as cores sob esse valor são convertidas em preto.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>Os dados de verificação são dificados usando o padrão de pontilhamento selecionado no momento.</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>Os dados de verificação representam a intensidade. A paleta é uma escala de cinza fixa e igualmente espaçada com uma profundidade especificada por <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> propriedade.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>O limite é um bit por pixel de dados em preto e branco. Os dados sobre o valor atual de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> são convertidos em branco; os dados sob esse valor são convertidos em preto.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>A propriedade <strong>WIA_IPA_DATATYPE</strong> também é usada para descrever o tipo de transferência de dados brutos a ser usado quando o aplicativo define WiaImgFmt_RAW. O driver deve definir a propriedade <strong>WIA_IPA_DATATYPE</strong> como uma lista de valores permitidos a partir dos quais o aplicativo pode escolher um.</p>
<p>Se o dispositivo puder ser definido como apenas um único valor, crie um tipo de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e coloque o valor válido nele.</p>
<p>Verifique a propriedade <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> para determinar a profundidade de bits. Essa propriedade geralmente contém um único valor para câmeras.</p>
<p>A tabela a seguir lista as constantes que são válidas com <strong>WIA_IPA_DATATYPE</strong> quando <strong>WIA_IPA_FORMAT</strong> é definido como WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Tipo de Dados</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_GRAYSCALE</td>
<td>Os dados de verificação representam a intensidade. A paleta é uma escala de cinza fixa, com espaçamento uniforme, com uma profundidade especificada pela propriedade <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> . <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 1.</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>Os dados de verificação estão no colorspace BGR (Blue-Green-Red). O formato de cor completa é descrito usando o followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>Os dados de verificação estão no colorspace de ciano-magenta-amarelo (CMY). O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>Os dados de verificação estão no colorspace ciano-magenta-amarelo-preto (CMYK). O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 4.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>Os dados de verificação estão no colorspace vermelho-verde-azul (RGB). O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>Os dados de verificação estão na colorspace de luminância-azul-diferença de cor vermelha (YUV). O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>Os dados de verificação estão na diferença de luminância-azul-diferença vermelha-preto (YUVK) colorspace. O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 4.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </dl></td>
<td style="text-align: left;"><p>WIA_IPA_DEPTH contém a configuração de profundidade de bits de uma imagem. O minidriver cria e mantém essa propriedade. Um aplicativo lê essa propriedade para determinar a configuração de profundidade de bits da imagem. O aplicativo também pode ser capaz de definir esse valor para a profundidade de bits desejada.</p>
<p>Se o dispositivo puder ser definido como apenas um único valor, crie um <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo e coloque o valor válido nele.</p>
<p>Essa propriedade é necessária para todos os itens WIA 2,0. Ele deve ser leitura/gravação para todos os itens habilitados para aquisição do WIA 2,0 e somente leitura para itens de armazenamento WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>; Acesso para sistemas operacionais anteriores ao Windows Vista: leitura/gravação; Acesso ao Windows Vista e posterior: essa propriedade é somente leitura para itens WIA_CATEGORY_FOLDER e WIA_CATEGORY_FINISHED_FILE e leitura/gravação para todas as outras categorias de item do WIA 2,0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO é definido como 0 bits por pixel e é um novo valor de propriedade definido para o WIA_IPA_DEPTH. Esse valor é válido para todos os itens de fonte de dados de imagem programável, incluindo o feed e o alimentador. Quando WIA_DEPTH_AUTO é compatível com o mini-driver WIA, o cliente do aplicativo WIA pode definir WIA_IPA_DEPTH para esse valor, para habilitar a detecção automática de cores no dispositivo. Quando WIA_DEPTH_AUTO é definido, o mini-driver WIA deve atualizar WIA_IPA_DATATYPE no mesmo item para WIA_DATA_AUTO (que deve ser um valor com suporte, se o dispositivo oferecer suporte à cor automática).</p>
<p>WIA_DEPTH_AUTO é um valor opcional, mas se torna necessário quando WIA_DATA_AUTO tem suporte para WIA_IPA_DATATYPE.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </dl></td>
<td style="text-align: left;"><p>Contém a extensão de nome de arquivo para um formato de arquivo específico. O minidriver cria e mantém essa propriedade.</p>
<p>Opcional para todos os itens WIA 2,0 habilitados para transferência.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>O driver atualiza essa propriedade para refletir o valor atual da propriedade <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</p>
<p>Por exemplo, se <strong>WIA_IPA_FORMAT</strong> for WiaImgFmt_JPEG, <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> deverá ser <strong>jpg</strong>. Se <strong>WIA_IPA_FORMAT</strong> for WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION deverá ser BMP.</p>
<div class="alert">
<blockquote>
[!Note]<br />
A extensão de nome de arquivo não inclui o ponto.
</blockquote>
</div>
<div>
 
</div>
<p>Essa propriedade é recomendada para drivers que dão suporte a formatos padrão e são necessários para drivers que implementam formatos definidos como personalizados. Ele informa o aplicativo da extensão de nome de arquivo correta a ser usada durante a transferência de arquivos formatados de forma privada. Por exemplo, se a a. Datum Corporation criou um driver WIA que transferiu um arquivo em um novo formato, a empresa poderia especificar uma extensão de &quot; ADC &quot; . Isso permite que os aplicativos transfiram dados nesse formato em um arquivo e criem um nome de arquivo como <em>MyFile. ADC</em>, que é útil para outras pessoas que entendem a nova extensão.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </dl></td>
<td style="text-align: left;"><p>Contém o formato atual da imagem a ser transferida.</p>
<p>Um aplicativo lê essa propriedade para determinar o formato da imagem que ela está prestes a receber. Um aplicativo grava essa propriedade para definir o formato. Essa propriedade depende da propriedade <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> . O minidriver cria e mantém essa propriedade.</p>
<p>Se o dispositivo puder ser definido como apenas um único valor, crie um tipo de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e coloque o valor válido nele.</p>
<p>Tipo: <strong>CLSID</strong>, acesso: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir lista as constantes que são válidas com essa propriedade. O asterisco * indica que a constante não tem suporte no Windows Vista. (Só está disponível por meio da interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .) O asterisco duplo * * indica que a constante não tem suporte no Windows Server 2003 ou no Windows Vista. O símbolo <strong>V</strong> indica que a constante tem suporte apenas no Windows Vista e posterior. (Só está disponível por meio da interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Formatar</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaAudFmt_AIFF</td>
<td>Formato de áudio AIFF</td>
</tr>
<tr class="even">
<td>WiaAudFmt_MP3</td>
<td>Formato de áudio MP3</td>
</tr>
<tr class="odd">
<td>WiaAudFmt_WAV</td>
<td>Formato de áudio WAV</td>
</tr>
<tr class="even">
<td>WiaAudFmt_WMA</td>
<td>Formato de áudio WMA</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_ASF * *</td>
<td>Formato de vídeo ASF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI * *</td>
<td>Formato de vídeo AVI</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Bitmap do Windows com um arquivo de cabeçalho</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF *</td>
<td>Formato de arquivo de imagem da câmera</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>Formato de impressão DPOF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Metarquivo estendido do Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXEC</td>
<td>Arquivo executável</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EXIF</td>
<td>Formato de arquivo intercambiável</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_FLASHPIX</td>
<td>Formato FlashPix</td>
</tr>
<tr class="even">
<td>WiaImgFmt_GIF</td>
<td>Formato de imagem GIF</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_HTML</td>
<td>Formato HTML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Formato do arquivo de ícone do Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>O formato de grupo de especialistas em imagem de nível de BI (JBIG).</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG</td>
<td>Formato compactado JPEG</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG2K</td>
<td>Formato compactado JPEG 2000</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG2KX</td>
<td>Formato compactado JPEG 2000</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Bitmap do Windows sem um arquivo de cabeçalho</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>O formato PDF/A (ISO/CD 19005-1).</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG * *</td>
<td>Formato de vídeo MPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Formato de arquivo da Eastman Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Formato de arquivo da Apple</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>Formato W3C PNG</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>Formato bruto somente para transferências de dados</td>
</tr>
<tr class="even">
<td>WiaImgFmt_RAWRGB</td>
<td>Formato RGB bruto</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RTF</td>
<td>Formato de arquivo de Rich Text</td>
</tr>
<tr class="even">
<td>WiaImgFmt_SCRIPT</td>
<td>Arquivo de script</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Formato TIFF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_TXT</td>
<td>Arquivo de texto</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_UNICODE16</td>
<td>Codificação UNICODE de 16 bits</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Metarquivo do Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_XML</td>
<td>Arquivo XML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_XPS<strong>V</strong></td>
<td>Formato de pacote XPS</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Quando essa propriedade é WiaImgFmt_PDFA ou WiaImgFmt_XPS e WIA_IPA_COMPRESSION é WIA_COMPRESSION_NONE; em seguida, o último valor significa que o modo de compactação é indefinido e o verificador deve decidir em um modo.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </dl></td>
<td style="text-align: left;"><p>Contém o nome completo do item (o nome do item junto com as informações de caminho). O nome completo do item é o mesmo que o parâmetro <em>bstrFullItemName</em> da função utilitário do serviço <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> . Um aplicativo lê essa propriedade para determinar qual item ele está usando no momento e onde esse item está localizado na árvore de itens. Cada item deve ter um nome exclusivo. Normalmente, os aplicativos usam o nome completo do item para pesquisar itens na árvore de itens. O serviço WIA cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens do WIA 2,0.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </dl></td>
<td style="text-align: left;"><p>Esta propriedade é reservada para uso futuro e não é implementada neste momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </dl></td>
<td style="text-align: left;"><p>Contém o nome do perfil ICM que é necessário para decodificar corretamente a imagem. Um aplicativo lê essa propriedade para determinar o perfil ICM a ser usado ao processar a imagem. O serviço WIA cria e mantém essa propriedade com base na entrada ICMProfiles no arquivo de instalação do driver.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </dl></td>
<td style="text-align: left;"><p>Com suporte apenas no Windows Vista e posterior.</p>
<p>Os itens WIA 2,0 são agrupados em categorias que definem como um <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> deve ser tratado ou usado. Por exemplo, se o item representa um alimentador, o aplicativo deve esperar que ele contenha as propriedades necessárias do alimentador de documentos e opere como um alimentador de documentos. Se o item representa um arquivo concluído, um aplicativo WIA 2,0 deve tratá-lo dessa forma, supondo que os dados sejam estáticos e localizados no dispositivo. (As regras para cada item serão definidas em seus documentos de especificação individuais.)</p>
<p>Necessário para todos os itens do WIA 2,0.</p>
<p>Tipo: <strong>VT_CLSID</strong>, Access: somente leitura, valores válidos: <a href="-wia-wia2-itemcategoryguids.md"><strong>GUIDs de categoria de item</strong></a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </dl></td>
<td style="text-align: left;"><p>Contém os sinalizadores descritivos para um item WIA. Os sinalizadores de item são os mesmos do parâmetro <em>lObjectFlags</em> da função utilitário de serviço <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> . O serviço WIA cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar os valores de sinalizador descritivos do item.</p>
<p>Tipo: acesso de <strong>VT_I4</strong> : somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem os sinalizadores que são válidos com essa propriedade. Um asterisco * indica que o sinalizador não tem suporte no Windows Vista ou posterior. (Só está disponível por meio da interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .) Um asterisco duplo * * indica que o sinalizador não tem suporte no Windows Server 2003 ou no Windows Vista ou posterior. O símbolo <strong>V</strong> indica que o sinalizador tem suporte apenas no Windows Vista e posterior. (Só está disponível por meio da interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Sinalizador</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaItemTypeAnalyze*</td>
<td>Este item dá suporte ao método <strong>IWiaItem:: AnalyzeItem</strong> (descrito na documentação do Platform SDK). Esse item também dá suporte à geração automática de itens filho. Esse recurso é útil para a detecção de região ou a decomposição de página.</td>
</tr>
<tr class="even">
<td>WiaItemTypeAudio</td>
<td>Este item dá suporte a áudio. Esse sinalizador é válido somente para itens que também têm o sinalizador <strong>WiaItemTypeFile</strong> definido.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeBurst*</td>
<td>Somente para pastas. Esse sinalizador indica que as imagens nessa pasta foram executadas em uma sequência de tempo contínua.</td>
</tr>
<tr class="even">
<td>WiaItemTypeDeleted</td>
<td>Este item está marcado para exclusão, este item foi excluído, este item não existe ou o conteúdo deste item é inválido.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDocument<strong>V</strong></td>
<td>Este item é um arquivo de documento em um dos formatos de documento que a propriedade <strong>WIA_IPA_FORMAT</strong> contém. (Esses formatos incluem aqueles para arquivos que não são de imagem, como. txt,. htm e arquivos. doc.)</td>
</tr>
<tr class="even">
<td>WiaItemTypeDevice</td>
<td>Este item representa um dispositivo conectado.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDisconnected</td>
<td>Este item representa um dispositivo desconectado.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFile</td>
<td>O item dá suporte a transferências de arquivos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeFolder</td>
<td>O item é uma pasta.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFree</td>
<td>O item não foi inicializado ou foi excluído.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeGenerated</td>
<td>Este item foi gerado por um aplicativo ou pelo driver.</td>
</tr>
<tr class="even">
<td>WiaItemTypeHasAttachments*</td>
<td>Este item dá suporte a anexos e atualmente contém anexos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeHPanorama*</td>
<td>Este item representa uma imagem panorâmica horizontal. Esse sinalizador é válido somente para itens que também têm o sinalizador <strong>WiaItemTypeFolder</strong> definido.</td>
</tr>
<tr class="even">
<td>WiaItemTypeImage</td>
<td>O item é um arquivo de imagem. Esse sinalizador é válido somente para itens que também têm o sinalizador <strong>WiaItemTypeFile</strong> definido.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeProgrammableDataSource<strong>V</strong></td>
<td>O item é uma fonte de dados programável e segue um conjunto de regras de configuração predefinidas, que se baseiam em <strong>WIA_IPA_ITEM_CATEGORY</strong>.</td>
</tr>
<tr class="even">
<td>WiaItemTypeRoot<strong>V</strong></td>
<td>Este item é o item raiz, que é o pai de todos os itens de recurso aos quais o dispositivo dá suporte.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeStorage</td>
<td>Esse sinalizador indica armazenamento adicional para itens de pastas. Os drivers WIA especificam seus itens em termos de imagens e pastas. Não existem propriedades WIA que descrevam as características de um item de armazenamento (como espaço de armazenamento restante, velocidade de gravação ou tipo de mídia. As propriedades específicas do fornecedor que expõem essas informações podem ser adicionadas. Essas propriedades são acessíveis somente para aplicativos ou extensões que são gravadas para reconhecê-las.</td>
</tr>
<tr class="even">
<td>WiaItemTypeTransfer</td>
<td>Este item pode ser usado para transferir dados.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeTwainCapabilityPassThrough</td>
<td>Esse tipo indica que o dispositivo WIA é capaz de receber dados de funcionalidade de TWAIN da camada de compatibilidade TWAIN. Se esse tipo for definido, qualquer recurso de TWAIN que não seja compreendido pela camada de compatibilidade TWAIN será passada para o driver theWIA. Isso é válido somente para o item raiz.</td>
</tr>
<tr class="even">
<td>WiaItemTypeVideo**</td>
<td>Este item dá suporte ao vídeo de streaming.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeVPanorama*</td>
<td>Este item representa uma imagem panorâmica vertical. Esse sinalizador é válido somente para itens que também têm o sinalizador <strong>WiaItemTypeFolder</strong> definido.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Alguns desses sinalizadores são obrigatórios ou opcionais para itens WIA 2,0, de acordo com a categoria do item, conforme mostrado nesta tabela.</p>

<table>
<thead>
<tr class="header">
<th>Categoria do item</th>
<th>Obrigatório</th>
<th>Opcional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_ROOT</td>
<td>WiaItemTypeRoot WiaItemTypeFolder</td>
<td>WiaItemTypeDevice WiaItemTypeDisconnected</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FLATBED</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (se houver suporte para vários itens de regiões de verificação, esse sinalizador será opcional somente para o item de raiz WIA_CATEGORY_FLATBED.)</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (se WIA_CATEGORY_FEEDER_FRONT e WIA_CATEGORY_FEEDER_BACK itens estiverem presentes, esse sinalizador será opcional somente para o item de raiz WIA_CATEGORY_FEEDER.)</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (raiz)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</td>
<td>Nenhum</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (filhos)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>Nenhum</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FOLDER</td>
<td>WiaItemTypeStorage WiaItemTypeFolder</td>
<td>WiaItemTypeDeleted</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td>WiaItemTypeFile WiaItemTypeTransfer</td>
<td>WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </dl></td>
<td style="text-align: left;"><p>Contém o nome do item. Um aplicativo lê essa propriedade para determinar qual item ele está usando no momento. Cada item tem um nome exclusivo. O serviço WIA cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens do WIA 2,0.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Contém o tamanho atual, em bytes, dos dados associados ao item. O minidriver cria e mantém essa propriedade.</p>
<p>Contains é o tamanho total dos dados que estão sendo transferidos. Se esse valor for zero, significa que o minidriver não tem informações sobre o tamanho exato dos dados. (Isso é comum para dados compactados.) Um aplicativo lê esse valor para determinar o tamanho da aquisição antes que ela ocorra. O serviço WIA lê essa propriedade para auxiliar na alocação de memória para transferências de dados. Para obter mais informações, consulte <a href="https://msdn.microsoft.com/library/ms792198.aspx">transferindo dados para um aplicativo WIA</a> se a propriedade for definida como zero e TYMED estiver configurado para uma transferência de arquivo, o serviço WIA não alocará memória para o minidriver WIA.</p>
<p>Necessário para todos os itens WIA 2,0 habilitados para transferência.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </dl></td>
<td style="text-align: left;"><p>Contém a hora em que a imagem foi capturada originalmente. O minidriver cria e mantém essa propriedade. Essa propriedade deve ser relatada como um vetor de oito valores de <strong>palavra</strong> na forma de uma estrutura SYSTEMTIME (descrita na documentação do Platform SDK).</p>
<p>Opcional para todos os itens WIA 2,0.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  acesso a<strong>VT_VECTOR</strong> : leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </dl></td>
<td style="text-align: left;"><p>Com suporte apenas no Windows Vista e posterior.</p>
<p>Especifica quantos itens são armazenados no item de WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Especifica o tamanho mínimo do buffer que é usado em transferências de dados. Se a transferência de dados for executada por meio de um mecanismo de retorno de chamada, o valor da propriedade poderá ser tão pequeno quanto 64 KB. No entanto, se a transferência for para o arquivo, o valor da propriedade será o número de bytes necessários para transferir uma página de dados de cada vez. O minidriver cria e mantém essa propriedade WIA.</p>
<p>Opcional para todos os itens WIA 2,0 habilitados para transferência.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </dl></td>
<td style="text-align: left;"><p>Contém o número de linhas contidas na imagem (a altura vertical da imagem em pixels). O minidriver cria e mantém essa propriedade.</p>
<p>Opcional para todos os itens WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Contém o número de pixels em cada linha da imagem (a largura da imagem em pixels). O minidriver cria e mantém essa propriedade.</p>
<p>Opcional para todos os itens WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </dl></td>
<td style="text-align: left;"><p>Não há suporte para essa propriedade no Windows Vista e posterior.</p>
<p>Contém opções de empacotamento de dados de imagem. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar as opções de empacotamento de imagem ou define as opções de empacotamento da imagem atual.</p>
<p>Tipo: <strong>VT_I4</strong>; Acesso: leitura/gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Se o dispositivo puder ser definido como apenas um único valor, crie um WIA_PROP_LIST tipo e coloque o valor válido nele.</p>
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
<td>WIA_PACKED_PIXEL</td>
<td>Os dados da imagem estão no formato de pixel embalado.</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>Os dados da imagem estão no formato planar.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </dl></td>
<td style="text-align: left;"><p>Contém o formato preferencial para as imagens que esse minidriver transfere. O minidriver cria e mantém essa propriedade.</p>
<p>Necessário para todos os itens WIA 2,0 habilitados para transferência.</p>
<p>Tipo: <strong>CLSID</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </dl></td>
<td style="text-align: left;"><p>Especifica um CLSID que representa um conjunto de valores de propriedade de dispositivo. Se um driver de dispositivo implementar esse recurso, os aplicativos usarão essa propriedade para determinar se o dispositivo dá suporte a um conjunto de valores.</p>
<p>Tipo: <strong>CLSID</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as 12 constantes que são válidas com essa propriedade.</p>

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Definição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Bitmap MicrosoftWindows com um arquivo de cabeçalho</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Metarquivo estendido do Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXIF</td>
<td>Formato de arquivo intercambiável</td>
</tr>
<tr class="even">
<td>WiaImgFmt_FLASHPIX</td>
<td>Formato FlashPix</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_GIF</td>
<td>Formato de imagem GIF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Formato do arquivo de ícone do Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>Formato compactado JPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Formato de arquivo da Eastman Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>Formato W3C PNG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Bitmap do Windows sem um arquivo de cabeçalho</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Formato TIFF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Metarquivo do Windows</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Com suporte apenas no Windows Vista e posterior.</p>
<p>Contém o número de bits em cada canal. Essa propriedade deve ser relatada como um vetor de até muitos valores de BYTE que há canais, em que o primeiro BYTE corresponde ao número de bits no primeiro canal, o segundo byte para o número de bits no segundo canal e assim por diante. Precisa haver tantas entradas quantos forem os canais de acordo com WIA_IPA_CHANNELS_PER_PIXEL. O driver define essa propriedade quando o aplicativo alterna para WiaImgFmt_RAW. Para os subtipos conhecidos, há tantas entradas, conforme listadas na tabela em WIA_IPA_RAW_SUBTYPE.</p>
<p>Tipo: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </dl></td>
<td style="text-align: left;"><p>Esta propriedade é reservada pelo para uso futuro e não é implementada neste momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </dl></td>
<td style="text-align: left;"><p>Especifica se as páginas de propriedades gerais devem ser suprimidas para os itens no dispositivo.</p>
<p>Essa propriedade está disponível no Windows XP e versões posteriores.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. O asterisco * indica que a constante não é válida com o Windows Vista e posterior. (Só está disponível por meio da interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL *</td>
<td>Suprimir a página de propriedades de item geral de uma câmera.</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>Suprimir a página de propriedades de item geral para um scanner.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </dl></td>
<td style="text-align: left;"><p>Essa propriedade contém a configuração do método de transferência. O minidriver cria e mantém essa propriedade.</p>
<p>Um aplicativo lê essa propriedade para determinar o método de transferência de dados de minidriver.</p>
<p>Necessário para todos os itens WIA 2,0 habilitados para transferência.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A tabela a seguir tem as constantes que são válidas com essa propriedade. O asterisco * indica constantes que não são válidas com o Windows Vista e posterior. (Eles só estão disponíveis por meio da interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Tipo de Transferência</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK *</td>
<td>Transferir uma imagem para a memória, em bandas.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK *</td>
<td>Transfira várias imagens para a memória, em bandas.</td>
</tr>
<tr class="odd">
<td>TYMED_FILE</td>
<td>Transferir uma imagem para um arquivo.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_FILE</td>
<td>Transferir uma imagem para um arquivo.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Com suporte apenas no Windows Vista e posterior.</p>
<p>Especifica o número de bytes a serem carregados para um item.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




