---
description: Descreve como criar um arquivo de descrição OpenSearch (. osdx) para conectar armazenamentos de dados externos ao cliente Windows por meio do protocolo OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920765"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows

Descreve como criar um arquivo de descrição OpenSearch (. osdx) para conectar armazenamentos de dados externos ao cliente Windows por meio do protocolo [OpenSearch](https://github.com/dewitt/opensearch) . A pesquisa federada permite que os usuários pesquisem um armazenamento de dados remoto e exibam os resultados de dentro do Windows Explorer.

Este tópico contém as seguintes seções:

-   [Arquivo de descrição de OpenSearch](#opensearch-description-file)
    -   [Largura elementos filho necessários](#mininum-required-child-elements)
-   [Elementos padrão na pesquisa federada do Windows](#standard-elements-in-windows-federated-search)
    -   [Nome curto](#shortname)
    -   [Descrição](#description)
    -   [Modelo de URL para resultados de RSS/Atom](#url-template-for-rssatom-results)
    -   [Modelo de URL para resultados da Web](#url-template-for-web-results)
    -   [Parâmetros de modelo de URL](#url-template-parameters)
    -   [Resultados paginados](#paged-results)
    -   [Paginação usando o índice do item](#paging-using-the-item-index)
    -   [Paginação usando o índice de página](#paging-using-the-page-index)
    -   [Tamanho da página](#page-size)
-   [Elementos estendidos na pesquisa federada do Windows](#extended-elements-in-windows-federated-search)
    -   [Contagem máxima de resultados](#maximum-result-count)
    -   [Mapeamento de propriedade](#property-mapping)
-   [Versões prévias](#previews)
-   [Abrir item de menu do local do arquivo](#open-file-location-menu-item)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="opensearch-description-file"></a>Arquivo de descrição de OpenSearch

Um arquivo de descrição de OpenSearch (. osdx) para a pesquisa federada do Windows deve obedecer às seguintes regras:

-   Ser um documento de descrição de OpenSearch válido, conforme definido pela especificação [OpenSearch](https://github.com/dewitt/opensearch) 1,1.
-   Forneça um modelo de URL com um tipo de formato RSS ou Atom.
-   Use a extensão de nome de arquivo. osdx ou esteja associada à extensão de nome de arquivo. osdx ao baixar da Web. Por exemplo, um servidor não precisa usar. osdx. Um servidor pode retornar o arquivo com qualquer extensão de nome de arquivo, como. xml, por exemplo, e tratado como se fosse um arquivo. osdx se ele usar o tipo MIME correto para documentos de descrição de OpenSearch (arquivos. osdx).
-   Forneça um valor de elemento **curtoname** (recomendado).

### <a name="mininum-required-child-elements"></a>Largura elementos filho necessários

O arquivo. osdx de exemplo a seguir consiste em **curtoname** e `Url` elementos, que são os elementos filho mínimos necessários.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Elementos padrão na pesquisa federada do Windows

Além dos elementos filho mínimos, a pesquisa federada dá suporte aos seguintes elementos padrão.

### <a name="shortname"></a>Nome curto

O Windows usa o valor de elemento **curtoname** para nomear o arquivo. searchconnector-MS (conector de pesquisa) que é criado quando o usuário abre o arquivo. osdx. O Windows garante que o nome de arquivo gerado Use apenas caracteres permitidos em nomes de arquivo do Windows. Se nenhum valor **curtoname** for fornecido, o arquivo. searchconnector-MS tentará usar o nome de arquivo do arquivo. osdx em vez disso.

O código a seguir ilustra como usar o elemento **curtoname** em um arquivo. osdx.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>Descrição

O Windows usa o valor do elemento **Description** para preencher a descrição do arquivo mostrado no painel de detalhes do Windows Explorer quando um usuário seleciona um arquivo. searchconnector-MS.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>Modelo de URL para resultados de RSS/Atom

O arquivo. osdx deve incluir um elemento de **formato de URL** e um atributo de **modelo** (um modelo de URL) que retorna resultados em formato RSS ou Atom. O atributo de formato deve ser definido como `application/rss+xml` para os resultados formatados em RSS ou `application/atom+xml` para resultados em formato Atom, conforme mostrado no código a seguir.

> [!Note]  
> O elemento **formato de URL** e o atributo de **modelo** são normalmente conhecidos como um modelo de URL.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>Modelo de URL para resultados da Web

Se houver uma versão dos resultados da pesquisa que possa ser exibida em um navegador da Web, você deverá fornecer um atributo **URL Format =** `text/html` Element e **Template** , conforme mostrado no código a seguir.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Se você fornecer um elemento **formato de URL = "texto/HTML"** e um atributo de **modelo** , um botão aparecerá na barra de comandos do Windows Explorer, conforme mostrado na captura de tela a seguir, que permite ao usuário abrir um navegador da Web para exibir os resultados da pesquisa quando o usuário executa uma consulta.

![captura de tela mostrando o botão de rolagem da pesquisa na Web.](images/websearchroll-overcommandbarbutton.png)

O lançamento da consulta de volta à interface do usuário da Web do repositório de dados é importante em alguns cenários. Por exemplo, um usuário pode querer exibir mais de 100 resultados (o número padrão de itens que o provedor de OpenSearch solicita). Nesse caso, o usuário também pode querer usar os recursos de pesquisa que estão disponíveis somente no site do repositório de dados, como consultar novamente com uma ordem de classificação diferente ou dinamizar e filtrar a consulta com metadados relacionados.

### <a name="url-template-parameters&quot;></a>Parâmetros de modelo de URL

O provedor de OpenSearch executa sempre as seguintes ações:

1.  Usa o modelo de URL para enviar a solicitação ao serviço Web.
2.  Tenta substituir os tokens encontrados no modelo de URL antes de enviar a solicitação para o serviço Web, da seguinte maneira:
    -   Substitui os tokens de OpenSearch padrão listados na tabela a seguir.
    -   Remove todos os tokens que não estão listados na tabela a seguir.



| Token com suporte  | Como é usado pelo provedor de OpenSearch                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| {searchTerms}    | Substituído pelos termos de pesquisa que o usuário digita na caixa de entrada de pesquisa do Windows Explorer.<br/>                                         |
| startIndex     | Usado ao obter resultados em &quot;páginas&quot;.<br/> Substituído pelo índice do primeiro item de resultado a ser retornado.<br/>                        |
| Inicial      | Usado ao obter resultados em &quot;páginas&quot;.<br/> Substituído pelo número de página do conjunto de resultados da pesquisa a ser retornado.<br/>               |
| contar          | Usado ao obter resultados em &quot;páginas&quot;.<br/> Substituído pelo número de resultados da pesquisa por página que o Windows Explorer solicita.<br/> |
| idioma       | Substituído por uma cadeia de caracteres que indica o idioma da consulta que está sendo enviada.<br/>                                                          |
| {inputEncoding}  | Substituído por uma cadeia de caracteres (como &quot;UTF-16") que indica a codificação de caracteres da consulta que está sendo enviada.<br/>                                |
| OutputEncoding | Substituído por uma cadeia de caracteres (como "UTF-16") que indica a codificação de caractere desejada para a resposta do serviço Web.<br/>       |



 

### <a name="paged-results"></a>Resultados paginados

Talvez você queira limitar o número de resultados retornados por solicitação. Você pode optar por retornar uma "página" de resultados por vez ou fazer com que o provedor de OpenSearch obtenha páginas adicionais de resultados por número de item ou número de página. Por exemplo, se você enviar vinte resultados por página, a primeira página que você enviar começará no índice de item 1 e na página 1; a segunda página que você envia começa no índice de item 21 e na página 2. Você pode definir como deseja que o provedor de OpenSearch solicite itens usando o `{startItem}` ou o `{startPage}` token no modelo de URL.

### <a name="paging-using-the-item-index"></a>Paginação usando o índice do item

Um índice de item identifica o primeiro item de resultado em uma página de resultados. Se desejar que os clientes enviem solicitações usando um índice de item, você poderá usar o `{startIndex}` token no atributo de **modelo** de elemento de **URL** , conforme mostrado no código a seguir.


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



Em seguida, o provedor de [OpenSearch](https://github.com/dewitt/opensearch) substitui o token na URL por um valor de índice inicial. A primeira solicitação começa com o primeiro item, conforme ilustrado no exemplo a seguir:


```
https://example.com/rss.php?query=frogs&start=1
```



O provedor de OpenSearch pode obter itens adicionais alterando o `{startIndex}` valor do parâmetro e emitindo uma nova solicitação. O provedor repete esse processo até obter resultados suficientes para atender ao seu limite ou atingir o final dos resultados. O provedor de OpenSearch examina o número de itens retornados pelo serviço Web na primeira página de resultados e define o tamanho de página esperado para esse número. Ele usa esse número para incrementar o `{startIndex}` valor das solicitações subsequentes. Por exemplo, se o serviço Web retornar 20 resultados na primeira solicitação, o provedor definirá o tamanho de página esperado como 20. Para a próxima solicitação, o provedor substituirá `{startIndex}` pelo valor 21 para obter os próximos 20 itens.

> [!Note]  
> Se uma página de resultados retornada pelo serviço Web tiver menos itens que o tamanho de página esperado, o provedor de OpenSearch assumirá que recebeu a última página de resultados e interromperá a realização de solicitações.

 

### <a name="paging-using-the-page-index"></a>Paginação usando o índice de página

Um índice de página identifica a página de resultados especificada. Se desejar que os clientes enviem solicitações usando um número de página, você poderá usar o `{startPage}` token em seu atributo de **modelo** de elemento de **formato de URL** para indicar que, conforme ilustrado no exemplo a seguir:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



O provedor de OpenSearch substitui o token na URL por um parâmetro de número de página. A primeira solicitação começa com a primeira página, conforme mostrado no exemplo a seguir:


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Se uma página de resultados retornada pelo serviço Web tiver menos itens que o tamanho de página esperado, o provedor de OpenSearch assumirá que recebeu a última página de resultados e interromperá a realização de solicitações.

 

### <a name="page-size"></a>Tamanho da Página

Talvez você queira configurar seu serviço Web para permitir que uma solicitação especifique o tamanho das páginas usando algum parâmetro na URL. Uma solicitação deve ser especificada no arquivo. osdx usando o `{count}` token, da seguinte maneira:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



O provedor de [OpenSearch](https://github.com/dewitt/opensearch) pode definir o tamanho de página desejado, em número de resultados por página, conforme mostrado no exemplo a seguir:


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



Por padrão, o provedor de OpenSearch faz solicitações usando um tamanho de página de 50. Se você quiser um tamanho de página diferente, não forneça um `{count}` token e, em vez disso, coloque o número desejado diretamente no elemento de **modelo de URL** .

O provedor de OpenSearch determina o tamanho da página com base no número de resultados retornados na primeira solicitação. Se a primeira página de resultados recebidos tiver menos itens do que a contagem solicitada, o provedor redefinirá o tamanho da página para todas as solicitações de página subsequentes. Se as solicitações de página subsequentes retornarem menos itens do que o solicitado, o provedor de OpenSearch pressupõe que atingiu o final dos resultados.

## <a name="extended-elements-in-windows-federated-search"></a>Elementos estendidos na pesquisa federada do Windows

Além dos elementos padrão, a pesquisa federada dá suporte aos seguintes elementos estendidos: **MaximumResultCount** e **ResultsProcessing**.

Como esses elementos filho estendidos não têm suporte na especificação [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, eles devem ser adicionados usando o seguinte namespace:


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Contagem máxima de resultados

Por padrão, os conectores de pesquisa são limitados a resultados de 100 por consulta de usuário. Esse limite pode ser personalizado incluindo o elemento **MaximumResultCount** dentro do arquivo OSD, conforme mostrado no exemplo a seguir:


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



O exemplo anterior declara o prefixo do namespace `ms-ose` no elemento **OpenSearchDescription** de nível superior e, em seguida, o usa como um prefixo no nome do elemento. Essa declaração é necessária porque o **MaximumResultCount** não tem suporte na especificação [OpenSearch](https://github.com/dewitt/opensearch) v 1.1.

### <a name="property-mapping"></a>Mapeamento de propriedade

Quando os resultados são retornados pelo serviço Web como um feed RSS ou Atom, o provedor de OpenSearch deve mapear os metadados do item nos feeds para propriedades que o Shell do Windows pode usar. A captura de tela a seguir ilustra como o provedor de OpenSearch mapeia alguns dos elementos RSS padrão.

![captura de tela mostrando mapeamentos de propriedades internos de RSS para Windows-Shell](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Mapeamentos padrão

Os mapeamentos padrão de elementos XML RSS para as propriedades do sistema shell do Windows são listados na tabela a seguir. Os caminhos XML são relativos ao elemento item. O `"media:"` prefixo é definido pelo namespace do [namespace de pesquisa do Yahoo](https://www.rssboard.org/media-rss) .



| Caminho XML do RSS                  | Propriedade shell do Windows (nome canônico) |
|-------------------------------|-----------------------------------------|
| Link                          | System. ItemUrl                          |
| Título                         | System. ItemName                         |
| Autor                        | System.Author                           |
| pubDate                       | System. DateModified                     |
| Descrição                   | System. autosummary                      |
| Category                      | System.Keywords                         |
| enclosure/@type               | System. MIMEType                         |
| enclosure/@length             | Sistema. tamanho                             |
| enclosure/@url                | System. ContentUrl                       |
| mídia: categoria                | System.Keywords                         |
| media:content/@fileSize       | Sistema. tamanho                             |
| media:content/@type           | System. MIMEType                         |
| media:content/@url            | System. ContentUrl                       |
| media:group/content/@fileSize | Sistema. tamanho                             |
| media:group/content/@type     | System. MIMEType                         |
| media:group/content/@url      | System. ContentUrl                       |
| media:thumbnail/@url          | System. ItemThumbnailUrl                 |



 

> [!Note]  
> Além dos mapeamentos padrão dos elementos RSS ou Atom padrão, você pode mapear outras propriedades do sistema shell do Windows incluindo elementos XML adicionais no namespace do Windows para cada uma das propriedades. Você também pode mapear elementos de outros namespaces XML existentes, como MediaRSS, iTunes e assim por diante, adicionando o mapeamento de propriedade personalizada no arquivo. osdx.

 

### <a name="custom-property-mappings"></a>Mapeamentos de propriedade personalizada

Você pode personalizar o mapeamento de elementos de sua saída RSS para as propriedades do sistema shell do Windows especificando o mapeamento no arquivo. osdx.

A saída RSS especifica:

-   Um namespace XML e
-   Para qualquer elemento filho de um item, um nome de elemento para o qual mapear.

O arquivo. osdx identifica uma propriedade de shell do Windows para cada nome de elemento em um namespace. Os mapeamentos de propriedade que você define em seu arquivo. osdx substituem os mapeamentos padrão, se existirem, para essas propriedades especificadas.

O diagrama a seguir ilustra como uma extensão RSS é mapeada para as propriedades do Windows (nome canônico).

![diagrama mostrando que a combinação de namespace XML e caminho XML produz o nome canônico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Resultados RSS de exemplo e mapeamento de propriedade OSD

O exemplo de saída RSS a seguir identifica `https://example.com/schema/2009` como o namespace XML com o prefixo "example". Esse prefixo deve aparecer novamente antes do elemento de **email** .


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



No arquivo de exemplo. osdx a seguir, o elemento **email** XML é mapeado para a propriedade shell do Windows [System. Contact. EmailAddress](../properties/props-system-contact-emailaddress.md).


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



Há algumas propriedades que não podem ser mapeadas porque os valores para elas são substituídos posteriormente ou não são editáveis. Por exemplo, [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) ou [System. ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) não podem ser mapeados porque eles são calculados a partir do valor da URL fornecido nos elementos do link ou do compartimento.

### <a name="thumbnails"></a>Miniaturas

As URLs de imagem em miniatura podem ser fornecidas para qualquer item usando o elemento **Media: thumbnail URL = ""** . A resolução ideal é 150 x 150 pixels. As maiores miniaturas com suporte são 256 x 256 pixels. Fornecer imagens maiores consome mais largura de banda para nenhum benefício adicional ao usuário.

### <a name="open-file-location-context-menu"></a>Abrir menu de contexto do local do arquivo

O Windows fornece um menu de atalho chamado **abrir local do arquivo** para itens de resultado. Se o usuário selecionar um item desse menu, a URL "pai" para o item selecionado será aberta. Se a URL for uma URL da Web, como `https://...` , o navegador da Web será aberto e navegado para essa URL. O feed deve fornecer uma URL personalizada para cada item para garantir que o Windows abra uma URL válida. Isso pode ser feito com a inclusão da URL dentro de um elemento dentro do XML do item, conforme ilustrado no exemplo a seguir:


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



Se essa propriedade não estiver definida explicitamente no XML do item, o provedor de OpenSearch a definirá como a pasta pai da URL do item. No exemplo acima, o provedor de OpenSearch usaria o valor do link e definiu o valor da Propriedade do shell do Windows [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) como `"https://example.com/"` .

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Personalizar exibições do Windows Explorer com listas de descrição de propriedade

Alguns layouts de exibição do Windows Explorer são definidos pelas listas de descrição de propriedade ou pelo propliss. Uma PropList é uma lista delimitada por ponto-e-vírgula de propriedades, como `"prop:System.ItemName; System.Author"` , que é usada para controlar como os resultados são exibidos no Windows Explorer.

As áreas de interface do usuário do Windows Explorer que podem ser personalizadas usando o propliss são ilustradas na captura de tela a seguir:

![captura de tela mostrando as áreas de interface do usuário do Windows Explorer que podem ser personalizadas usando o propliss](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

Cada área do Windows Explorer tem um conjunto associado de propliss, que são especificados como propriedades. Você pode especificar proplistes personalizados para itens individuais em seus conjuntos de resultados ou para todos os itens em um conjunto de resultados.



| Área da interface do usuário a ser personalizada               | Propriedade do shell do Windows que implementa a personalização |
|------------------------------------|----------------------------------------------------------|
| Modo de exibição de conteúdo (ao Pesquisar) | System. PropList. ContentViewModeForSearch                 |
| Modo de exibição de conteúdo (ao navegar)  | System. PropList. ContentViewModeForBrowse                 |
| Modo de exibição de bloco                     | System. PropList. TileInfo                                 |
| Painel de detalhes                       | System. PropList. PreviewDetails                           |
| Infotip (dica de ferramenta de foco do item)     | System. PropList. InfoTip                                  |



 

 

**Para especificar uma PropList exclusiva para um item individual:**

1.  Em sua saída de RSS, adicione um elemento personalizado que represente a PropList que você deseja personalizar. Por exemplo, o exemplo a seguir define a lista para o painel de detalhes:
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Para aplicar uma propriedade a cada item nos resultados da pesquisa sem modificar a saída RSS, especifique uma PropList em um elemento **MS-OSE: PropertyDefaultValues** no arquivo. osdx, conforme mostrado no exemplo a seguir:

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Layout das propriedades do modo de exibição de conteúdo

A lista de propriedades especificada nos proplistions **System. PropList. ContentViewModeForSearch** e **System. PropList. ContentViewModeForBrowse** determina o que é mostrado no modo de exibição de conteúdo. Para obter mais informações sobre listas de propriedades, consulte [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).

As propriedades são dispostas de acordo com os números mostrados no seguinte padrão de layout:

![captura de tela mostrando o padrão de layout padrão na exibição de conteúdo](images/propertiesnumberslayoutpattern.png)

Se usarmos a seguinte lista de propriedades,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



Em seguida, vemos a seguinte exibição:

![captura de tela mostrando layout de propriedade de exemplo.](images/samplepropertylayout.png)

> [!Note]  
> Para obter a melhor legibilidade, as propriedades mostradas na coluna mais à direita devem ser rotuladas.

 

### <a name="property-list-flags"></a>Sinalizadores da lista de propriedades

Somente um dos sinalizadores definidos na documentação do proplistor se aplica à exibição de itens nos layouts do modo de exibição de conteúdo: ` "~"` . Nos exemplos anteriores, o modo de exibição do Windows Explorer rotula algumas das propriedades, como `Tags: animals; zoo; lion` . Esse é o comportamento padrão quando você especifica uma propriedade na lista. Por exemplo, a PropList tem o `"System.Author"` que é exibido como `"Authors: value"` . Quando desejar ocultar o rótulo de propriedade, coloque um `"~"` na frente do nome da propriedade. Por exemplo, se PropList tiver `"~System.Size"` , a propriedade será exibida como apenas um valor, sem o rótulo.

## <a name="previews"></a>Visualizações

Quando o usuário seleciona um item de resultado no Windows Explorer e o painel de visualização está aberto, o conteúdo do item é visualizado.

O conteúdo a ser mostrado na visualização é especificado por uma URL, que é determinada da seguinte maneira:

1.  Se a propriedade shell do Windows **System. WebPreviewUrl** for definida para o item, use essa URL.
    > [!Note]  
    > A propriedade precisa ser fornecida no RSS usando o namespace do shell do Windows ou explicitamente mapeada no arquivo. osdx.

     

2.  Caso contrário, use a URL do link em vez disso.

O fluxograma a seguir mostra essa lógica.

![fluxograma mostrando como o Windows Explorer seleciona a URL a ser usada para visualizações](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

É possível usar uma URL diferente para a visualização do que para o próprio item. Isso significa que, se você fornecer URLs diferentes para a URL de link e o compartimento ou `media:content URL` , o Windows Explorer usará a URL de link para visualizações do item, mas usará a outra URL para detecção de tipo de arquivo, abertura, download e assim por diante.

Como o Windows Explorer determina qual URL usar:

1.  Se você fornecer um mapeamento para [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), o Windows Explorer usará essa URL
2.  Se você não fornecer um mapeamento, o Windows Explorer identificará se as URLs do link e do compartimento são diferentes. Nesse caso, o Windows Explorer usa a URL do link.
3.  Se as URLs forem iguais ou se houver apenas uma URL de link, o Windows Explorer analisará o link para localizar o contêiner pai removendo o nome do arquivo da URL completa.
    > [!Note]  
    > Se você reconhecer que a análise de URL resultaria em Links inativos para seu serviço, você deverá fornecer um mapeamento explícito para a propriedade.

     

## <a name="open-file-location-menu-item"></a>Abrir item de menu do local do arquivo

Quando um item é clicado com o botão direito do mouse, o comando **abrir local do arquivo** é exibido. Esse comando leva o usuário para o contêiner ou local desse item. Por exemplo, em uma pesquisa do SharePoint, selecionar essa opção para um arquivo em uma biblioteca de documentos abriria a raiz da biblioteca de documentos no navegador da Web.

Quando um usuário clica em **abrir local do arquivo**, o Windows Explorer tenta localizar um contêiner pai, usando a lógica mostrada no seguinte fluxograma:

![fluxograma mostrando como o Windows Explorer identifica um contêiner pai](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a>Recursos adicionais

Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introdução com pesquisa federada no Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conectando seu serviço Web na pesquisa federada do Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitando seu armazenamento de dados na pesquisa federada do Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Seguindo as práticas recomendadas na pesquisa federada do Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implantando conectores de pesquisa na pesquisa federada do Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
