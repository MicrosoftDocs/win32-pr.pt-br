---
description: Com Windows Vista, a árvore de itens wia (aquisição Windows imagem) do Windows foi alterada significativamente.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Sobre a árvore de itens IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae342f5a85e61b6384604dae703881c6888e3e1cf8e61cc8a39a32ac77ad436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264416"
---
# <a name="about-the-iwiaitem2-item-tree"></a>Sobre a árvore de itens IWiaItem2

Com Windows Vista, a árvore de itens wia (aquisição Windows imagem) do Windows foi alterada significativamente. [**Os itens IWiaItem2**](-wia-iwiaitem2.md) são usados para representar atributos de dispositivo e dados do dispositivo. Os aplicativos de imagens veem um dispositivo WIA (Aquisição de Imagem) 2.0 do Windows como uma árvore hierárquica de itens, com o item raiz representando o próprio dispositivo e os itens filho que representam itens como fontes de dados programáveis, imagens ou pastas que contêm imagens.

-   [Itens de aplicativo](#application-items)
-   [Sinalizadores de item](#item-flags)
-   [Categorias de item](#item-categories)
-   [Item raiz](#root-item)
-   [Item de dados](#data-item)
-   [Tópicos relacionados](#related-topics)

## <a name="application-items"></a>Itens de aplicativo

A árvore de itens do WIA 2.0 que um aplicativo pode ver é separada da árvore criada e mantida por um minidriver WIA 2.0. Quando um minidriver cria uma árvore, o serviço WIA 2.0 usa essa árvore de itens wia 2.0 como um guia para criar uma cópia da árvore que pode ser exibida por aplicativos de imagens. Os itens na árvore copiada são chamados de *itens de* aplicativo. Os itens na árvore criada por um minidriver são chamados de *itens de* driver.

Um item WIA pode representar uma fonte de dados programável para o feed de documentos de um scanner ou os dados armazenados nesse dispositivo. Um dispositivo WIA deve ser dividido em itens individuais que descrevem dados diferentes produzidos por esse dispositivo.

Por exemplo, um scanner WIA que dá suporte à verificação de flatbed e à verificação do feeder de documentos pode ser dividido em dois itens filho. Um representa a funcionalidade de verificação de flatbed e o outro representa a funcionalidade de verificação do feeder de documentos.

Várias imagens colocadas em um scanner de flatbed e examinadas ao mesmo tempo podem ser colocadas em uma pasta. Usando o filtro de segmentação ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), cada imagem ou sub-região pode ser criada como um item filho da pasta.

A árvore WIA para um dispositivo de câmera que armazena fotos ("Filme") pode ser dividida em itens que representam pastas, subpastas e fotos.

## <a name="item-flags"></a>Sinalizadores de item

Os sinalizadores de item WIA ajudam a classificar o conteúdo ou o comportamento com suporte de um item WIA específico. Os sinalizadores de item WIA se enquadram em dois grupos.

1.  Os sinalizadores de status do item relatam o estado atual do item WIA, por exemplo, [**WiaItemTypeDisconnected,**](-wia-wia-item-type-flags.md) **WiaItemTypeDeleted** e assim por diante.
2.  Sinalizadores de representação/uso de dados de item relatam os dados que o item WIA representa ou pode produzir se transferido. Por exemplo, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) é um sinalizador de representação de dados que informa ao aplicativo que os dados associados ao item WIA atual são dados de imagem e devem ter propriedades de dados de imagem. **WIA \_ SINALIZADORES \_ \_ DE ITEM IPA** é um sinalizador de uso de item que informa ao aplicativo que o item WIA é configurável e segue um conjunto de regras de configuração predefinidos com base na CATEGORIA DE [**ITEM \_ IPA \_ \_**](-wia-wiaitempropcommonitem.md) do WIA e que a configuração pode possivelmente alterar o resultado de cada transferência de dados. (Para obter mais informações sobre definições de categoria, consulte [Categorias de item categorias](#item-categories) de item.)

O gráfico a seguir mostra um exemplo de uma árvore de itens wia e os vários sinalizadores que podem ser associados a cada item.

![exemplos de sinalizadores de item para itens em uma árvore](images/scannertree1.jpg)

## <a name="item-categories"></a>Categorias de item

Os itens do WIA são agrupados em categorias usando os valores de propriedade [**CATEGORIA \_ DE ITEM IPA \_ \_ DO WIA.**](-wia-wiaitempropcommonitem.md) Essas categorias definem como um item WIA deve ser tratado ou usado. Por exemplo, se o item representar um arquivo concluído (WIA CATEGORY FINISHED FILE), um aplicativo WIA deverá supor que os dados são estáticos e \_ \_ \_ localizados no dispositivo. Se o item representa um feeder (WIA CATEGORY FEEDER), o aplicativo deve esperar que ele contenha as propriedades necessárias do feeder de documentos e opere como um \_ \_ feeder de documentos.

As categorias definidas pelo WIA são:

-   CATEGORIA WIA \_ \_ AUTO
-   FEEDER \_ DE CATEGORIA \_ WIA
-   FILME DE \_ CATEGORIA \_ WIA
-   ARQUIVO CONCLUÍDO \_ DA \_ CATEGORIA WIA \_
-   CATEGORIA WIA \_ \_ FLATBED

Por exemplo, o item de flatbed de um scanner pode ter os SINALIZADORES DE [**ITEM IPA WIA \_ \_ \_ definidos**](-wia-wiaitempropcommonitem.md) como [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** e **WiaItemTypeProgrammableDataSource** e a propriedade CATEGORIA DE **\_ \_ ITEM \_ IPA WIA** definida como WIA \_ CATEGORY \_ FLATBED.

A tabela a seguir mostra o grupo de categorias wia com sinalizadores de item e itens WIA. Esta tabela não inclui uma lista completa dos sinalizadores de item WIA definidos pelo WIA.



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
<th>Itens wia</th>
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
<td>O conjunto de propriedades inclui propriedades do scanner configuradas automaticamente.</td>
<td>Item automático do WIA que representa as configurações de verificação configuradas automaticamente do verificador.</td>
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
<td>O conjunto de propriedades inclui propriedades de controle do scanner do feeder (geralmente conjunto de propriedades específicas da imagem e do documento).</td>
<td>Itens do WiA Feeder, incluindo itens filho que representam as páginas frontal e traseira de um documento.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>O conjunto de propriedades inclui propriedades de controle do scanner de filmes (geralmente conjunto de propriedades específicas de imagem e documento).</td>
<td>Itens de filmes do WIA, incluindo itens filho que representam os quadros de verificação individuais.</td>
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
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>— pode estar presente se o verificador dá suporte à verificação de vários itens.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>— pode estar presente se o aplicativo gerar um item WIA durante uma sessão de verificação de vários itens.</li>
</ul></td>
<td>O conjunto de propriedades inclui propriedades de controle do scanner de flatbed (geralmente conjunto de propriedades específicas da imagem e do documento).</td>
<td>Itens de flatbed do WIA, incluindo itens filho que representam as regiões que estão sendo examinadas na placa de fundo simples do verificador.</td>
</tr>
</tbody>
</table>



 

O gráfico a seguir mostra um exemplo de uma árvore de itens WIA e as várias categorias que podem ser associadas a cada item.

![exemplos de categorias de item para itens em uma árvore](images/scannertree2.jpg)

## <a name="root-item"></a>Item raiz

Um item raiz do WIA é um item de pasta marcado com sinalizadores [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) e **WiaItemTypeDevice** que representa o próprio dispositivo. Ele contém atributos de dispositivo, como fabricante, nome do dispositivo e atributos de driver, como a versão do driver e o CLSID (identificador de classe de interface do usuário). Os aplicativos de imagens geram a raiz para a árvore de itens wia chamando [**o método IWiaDevMgr2::CreateDevice.**](-wia-iwiadevmgr2-createdevice.md) O aplicativo usa o item raiz para obter acesso aos itens de WIA filho individuais enumerando a árvore (consulte [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).

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

 

 



