---
description: Com o Windows Vista, a árvore de itens de aquisição de imagens do Windows (WIA) mudou significativamente.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Sobre a árvore de itens do IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828458"
---
# <a name="about-the-iwiaitem2-item-tree"></a>Sobre a árvore de itens do IWiaItem2

Com o Windows Vista, a árvore de itens de aquisição de imagens do Windows (WIA) mudou significativamente. Os itens [**IWiaItem2**](-wia-iwiaitem2.md) são usados para representar os atributos do dispositivo e os dados do dispositivo. Os aplicativos de geração de imagens veem um dispositivo de aquisição de imagem do Windows (WIA) 2,0 como uma árvore hierárquica de itens, com o item raiz que representa o próprio dispositivo e os itens filho que representam coisas como fontes de dados programáveis, imagens ou pastas que contêm imagens.

-   [Itens de aplicativo](#application-items)
-   [Sinalizadores de item](#item-flags)
-   [Categorias de item](#item-categories)
-   [Item raiz](#root-item)
-   [Item de dados](#data-item)
-   [Tópicos relacionados](#related-topics)

## <a name="application-items"></a>Itens de aplicativo

A árvore de itens WIA 2,0 que um aplicativo pode ver é separada da árvore criada e mantida por uma minidriver WIA 2,0. Quando um minidriver cria uma árvore, o serviço WIA 2,0 usa essa árvore de itens WIA 2,0 como um guia para criar uma cópia da árvore que pode ser exibida por aplicativos de geração de imagens. Os itens na árvore copiada são chamados de itens de *aplicativo* . Os itens na árvore criados por um minidriver são chamados de itens de *Driver* .

Um item WIA pode representar uma fonte de dados programável para o alimentador de documentos de um scanner ou os dados armazenados nesse dispositivo. Um dispositivo WIA deve ser dividido em itens individuais que descrevem diferentes dados produzidos por esse dispositivo.

Por exemplo, um scanner WIA que dá suporte à verificação de mesa e à verificação do alimentador de documentos pode ser dividido em dois itens filho. Uma representa a funcionalidade de digitalização de mesa e a outra representa a funcionalidade de verificação do alimentador de documentos.

Várias imagens dispostas em um scanner de mesa e verificadas ao mesmo tempo podem ser colocadas em uma única pasta. Usando o filtro de segmentação ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), cada imagem ou subregião pode ser criada como um item filho da pasta.

A árvore WIA para um dispositivo de câmera que armazena fotos ("filme") pode ser dividida em itens que representam pastas, subpastas e fotos.

## <a name="item-flags"></a>Sinalizadores de item

Os sinalizadores de item WIA ajudam a classificar o conteúdo ou o comportamento com suporte de um determinado item WIA. Os sinalizadores de item WIA se enquadram em dois grupos.

1.  Sinalizadores de status do item relatam o estado atual do item WIA, por exemplo, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted** e assim por diante.
2.  Sinalizadores de uso/representação de dados do item relatam os dados que o item WIA representa ou que podem produzir se transferidos. Por exemplo, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) é um sinalizador de representação de dados que informa ao aplicativo que os dados associados ao item WIA atual são dados de imagem e devem ter propriedades de dados de imagem. **WIA \_ \_ \_ Sinalizadores de item de IPA** é um sinalizador de uso de item que informa ao aplicativo que o item WIA é configurável e segue um conjunto de regras de configuração predefinidas com base na [**\_ \_ \_ categoria de item IPA WIA**](-wia-wiaitempropcommonitem.md) e que a configuração pode, possivelmente, alterar o resultado para cada transferência de dados. (Para obter mais informações sobre definições de categoria, consulte categorias de item [categorias de item](#item-categories) .)

O gráfico a seguir mostra um exemplo de uma árvore de itens WIA e os vários sinalizadores que podem ser associados a cada item.

![exemplos de sinalizadores de item para itens em uma árvore](images/scannertree1.jpg)

## <a name="item-categories"></a>Categorias de item

Os itens WIA são agrupados em categorias usando os valores de propriedade de [**\_ \_ \_ categoria do item IPA WIA**](-wia-wiaitempropcommonitem.md) . Essas categorias definem como um item WIA deve ser tratado ou usado. Por exemplo, se o item representa um arquivo concluído ( \_ arquivo de categoria WIA \_ concluído \_ ), um aplicativo WIA deve assumir que os dados são estáticos e localizados no dispositivo. Se o item representa um alimentador ( \_ alimentador de categoria WIA \_ ), o aplicativo deve esperar que ele contenha as propriedades necessárias do alimentador de documentos e opere como um alimentador de documentos.

As categorias definidas por WIA são:

-   \_automático da categoria WIA \_
-   \_alimentador de categoria WIA \_
-   \_filme de categoria WIA \_
-   \_arquivo de categoria WIA \_ concluído \_
-   \_superfície da categoria WIA \_

Por exemplo, o item de mesa de um scanner pode ter os [**\_ \_ \_ sinalizadores de item IPA WIA**](-wia-wiaitempropcommonitem.md) definidos como [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** e **WiaItemTypeProgrammableDataSource**, e a propriedade de **categoria de \_ item de IPA \_ \_ WIA** definida como a \_ superfície de categoria WIA \_ .

A tabela a seguir mostra o agrupamento de categorias WIA com sinalizadores de item e itens WIA. Esta tabela não inclui uma lista completa dos sinalizadores de item WIA definidos pelo WIA.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoria WIA</th>
<th>Sinalizadores de item WIA válidos</th>
<th>Conjunto de propriedades WIA</th>
<th>Itens WIA</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_AUTO</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></li>
</ul></td>
<td>O conjunto de propriedades inclui propriedades de scanner configuradas automaticamente.</td>
<td>O item automático WIA que representa as configurações de verificação automáticas do verificador.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FEEDER</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>O conjunto de propriedades inclui propriedades do controle do scanner do Feeder (geralmente imagem e conjunto de propriedades específicas do documento).</td>
<td>Itens do alimentador WIA, incluindo itens filho que representam as páginas de frente e de trás de um documento.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>O conjunto de propriedades inclui propriedades de controle de scanner de filme (geralmente imagem e conjunto de propriedades específicas de documento).</td>
<td>Itens de filme WIA, incluindo itens filho que representam os quadros de verificação individuais.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
</ul></td>
<td>A propriedade definida neste item depende do tipo de item relatado. Por exemplo, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> deve incluir algumas propriedades de item de imagem, como bits por pixel e assim por diante.</td>
<td>Itens de armazenamento WIA, incluindo itens filho que representam o conteúdo do arquivo concluído (arquivos de dados como JPEG, HTML, TXT e assim por diante).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>— pode estar presente se o verificador oferecer suporte à verificação de vários itens.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>— pode estar presente se o aplicativo gerar um item WIA durante uma sessão de verificação de vários itens.</li>
</ul></td>
<td>O conjunto de propriedades inclui as propriedades do controle do scanner de mesa (geralmente imagem e conjunto de propriedades específicas do documento).</td>
<td>Itens de mesa WIA, incluindo itens filho que representam regiões sendo examinadas no cilindro de mesa do scanner.</td>
</tr>
</tbody>
</table>



 

O gráfico a seguir mostra um exemplo de uma árvore de itens WIA e as várias categorias que podem ser associadas a cada item.

![exemplos de categorias de item para itens em uma árvore](images/scannertree2.jpg)

## <a name="root-item"></a>Item raiz

Um item raiz WIA é um item de pasta marcado com sinalizadores [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) e **WiaItemTypeDevice** que representa o próprio dispositivo. Ele contém atributos de dispositivo, como fabricante, nome do dispositivo e atributos de driver, como versão do driver e identificador de classe de interface do usuário (CLSID). Os aplicativos de geração de imagens obtêm a raiz para a árvore de itens WIA chamando o método [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) . O aplicativo usa o item raiz para obter acesso aos itens WIA filho individuais enumerando a árvore (consulte [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).

## <a name="data-item"></a>Item de Dados

Qualquer item que possa ser usado para transferir dados é considerado um item de dados. Isso inclui itens marcados com o sinalizador [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) .

Itens de pasta e itens não de pasta podem expor a capacidade de transferir dados, sendo marcados com o sinalizador [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) . Qualquer item com esse sinalizador definido deve fornecer as seguintes propriedades de item WIA:

-   [**\_direitos de \_ acesso \_ IPA WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_tamanho do \_ item \_ IPA WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_tamanho do \_ buffer \_ IPA WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_formato IPA \_ WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_ \_ formato preferencial IPA \_ WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_TYMED IPA \_ WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_extensão de \_ nome de arquivo WIA IPA \_**](-wia-wiaitempropcommonitem.md)

Itens de fonte de dados programáveis marcados com o sinalizador [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) também devem fornecer o conjunto de propriedades de item de dados necessário.

Os itens de dados WIA podem ter propriedades adicionais, dependendo das configurações de sinalizador do item. Por exemplo, os itens WIA marcados com o sinalizador [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) devem ter propriedades de informações específicas da imagem, como a [**\_ \_ profundidade IPA do WIA**](-wia-wiaitempropcommonitem.md) e o **\_ \_ número \_ de \_ linhas IPA do WIA**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)
</dt> <dt>

[**IWiaDevMgr2**](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



