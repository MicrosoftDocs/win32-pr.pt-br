---
description: Descreve como criar um arquivo OpenSearch Description (.osdx) para conectar armazenamentos de dados externos ao cliente Windows por meio do protocolo OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Criando um arquivo OpenSearch descrição no Windows Federado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f58b29a860c7d53583b7fd17ddd942bb21b08d649ea7e54d5b2278be2f8d4c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456829"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Criando um arquivo OpenSearch descrição no Windows Federado

Descreve como criar um arquivo OpenSearch Description (.osdx) para conectar armazenamentos de dados externos ao cliente Windows por meio do [protocolo OpenSearch.](https://github.com/dewitt/opensearch) A pesquisa federada permite que os usuários pesquisem um armazenamento de dados remoto e vejam os resultados de dentro Windows Explorer.

Este tópico contém as seguintes seções:

-   [OpenSearch Arquivo de descrição](#opensearch-description-file)
    -   [Elementos filho mínimos necessários](#mininum-required-child-elements)
-   [Elementos padrão na Windows Federadas](#standard-elements-in-windows-federated-search)
    -   [Shortname](#shortname)
    -   [Descrição](#description)
    -   [Modelo de URL para resultados RSS/Atom](#url-template-for-rssatom-results)
    -   [Modelo de URL para resultados da Web](#url-template-for-web-results)
    -   [Parâmetros de modelo de URL](#url-template-parameters)
    -   [Resultados de página](#paged-results)
    -   [Paging usando o índice de item](#paging-using-the-item-index)
    -   [Paging Usando o índice de página](#paging-using-the-page-index)
    -   [Tamanho da página](#page-size)
-   [Elementos estendidos Windows pesquisa federada](#extended-elements-in-windows-federated-search)
    -   [Contagem máxima de resultados](#maximum-result-count)
    -   [Mapeamento de propriedade](#property-mapping)
-   [Versões prévias](#previews)
-   [Item de menu Abrir Local do Arquivo](#open-file-location-menu-item)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="opensearch-description-file"></a>OpenSearch Arquivo de descrição

Um OpenSearch descrição (.osdx) para Windows Federated Search deve obedecer às seguintes regras:

-   Seja um documento OpenSearch descrição válido, conforme definido pela [especificação OpenSearch](https://github.com/dewitt/opensearch) 1.1.
-   Forneça um modelo de URL com um RSS ou um tipo de formato Atom.
-   Use a extensão de nome de arquivo .osdx ou seja associado à extensão de nome de arquivo .osdx ao baixar da Web. Por exemplo, um servidor não é necessário para usar .osdx. Um servidor pode retornar o arquivo com qualquer extensão de nome de arquivo, como .xml por exemplo, e tratado como se fosse um arquivo .osdx se ele usa o Tipo MIME correto para documentos de Descrição do OpenSearch (arquivos .osdx).
-   Forneça um **valor de elemento ShortName** (recomendado).

### <a name="mininum-required-child-elements"></a>Elementos filho mínimos necessários

O arquivo .osdx de exemplo a seguir consiste em **ShortName** e elementos, que são os `Url` elementos filho mínimos necessários.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Elementos padrão na Windows Federadas

Além dos elementos filho mínimos, a pesquisa federada dá suporte aos seguintes elementos padrão.

### <a name="shortname"></a>Shortname

Windows usa o valor do elemento **ShortName** para nomear o arquivo .searchconnector-ms (conector de pesquisa) criado quando o usuário abre o arquivo .osdx. Windows garante que o nome de arquivo gerado use apenas caracteres que são permitidos em Windows de arquivo. Se nenhum **valor ShortName** for fornecido, o arquivo .searchconnector-ms tentará usar o nome do arquivo .osdx.

O código a seguir ilustra como usar o **elemento ShortName** em um arquivo .osdx.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>Descrição

Windows usa o valor do elemento **Description** para preencher a descrição do arquivo mostrada no painel de detalhes do Windows Explorer quando um usuário seleciona um arquivo .searchconnector-ms.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>Modelo de URL para resultados RSS/Atom

O arquivo .osdx deve incluir  um elemento de formato **de URL** e um atributo de modelo (um modelo de URL) que retorna resultados no formato RSS ou Atom. O atributo de formato deve ser definido como para resultados formatados em RSS ou para resultados formatados atom, conforme `application/rss+xml` mostrado no código a `application/atom+xml` seguir.

> [!Note]  
> O **elemento de formato** de URL e o atributo **de** modelo normalmente são conhecidos como um modelo de URL.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>Modelo de URL para resultados da Web

Se houver uma versão dos resultados da pesquisa que possa ser exibida em um navegador da Web, você deverá fornecer um elemento **Url format=** e um atributo de modelo, conforme mostrado no código a `text/html`  seguir.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Se você fornecer um elemento **url format="text/html"** e um atributo de modelo, um botão aparecerá na barra de comandos do Windows Explorer, conforme mostrado na captura de tela a seguir, que permite que o usuário abra um navegador da Web para exibir os resultados da pesquisa quando o usuário executa uma consulta. 

![captura de tela mostrando o botão de rolagem de pesquisa na Web.](images/websearchroll-overcommandbarbutton.png)

A replicação da consulta de volta para a interface do usuário da Web do armazenamento de dados é importante em alguns cenários. Por exemplo, um usuário pode querer exibir mais de 100 resultados (o número padrão de itens que o provedor OpenSearch solicita). Nesse caso, o usuário também pode querer usar recursos de pesquisa que estão disponíveis apenas no site do armazenamento de dados, como a consulta com uma ordem de classificação diferente ou a dinâmica e filtragem da consulta com metadados relacionados.

### <a name="url-template-parameters&quot;></a>Parâmetros de modelo de URL

O OpenSearch provedor executa sempre as seguintes ações:

1.  Usa o modelo de URL para enviar a solicitação para o serviço Web.
2.  Tenta substituir os tokens encontrados no modelo de URL antes de enviar a solicitação para o serviço Web, da seguinte forma:
    -   Substitui os tokens OpenSearch padrão listados na tabela a seguir.
    -   Remove todos os tokens que não estão listados na tabela a seguir.



| Token com suporte  | Como usado pelo OpenSearch provedor                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| {searchTerms}    | Substituídos por termos de pesquisa que o usuário digita na caixa de Windows de entrada de pesquisa do Explorer.<br/>                                         |
| {startIndex}     | Usado ao obter resultados em &quot;páginas&quot;.<br/> Substituído pelo índice para o primeiro item de resultado a ser retornada.<br/>                        |
| {startPage}      | Usado ao obter resultados em &quot;páginas&quot;.<br/> Substituído pelo número de página do conjunto de resultados da pesquisa a ser retornada.<br/>               |
| {count}          | Usado ao obter resultados em &quot;páginas&quot;.<br/> Substituído pelo número de resultados da pesquisa por página que Windows Explorer.<br/> |
| {language}       | Substituído por uma cadeia de caracteres que indica o idioma da consulta que está sendo enviada.<br/>                                                          |
| {inputEncoding}  | Substituído por uma cadeia de caracteres (como &quot;UTF-16") que indica a codificação de caracteres da consulta que está sendo enviada.<br/>                                |
| {outputEncoding} | Substituído por uma cadeia de caracteres (como "UTF-16") que indica a codificação de caracteres desejada para a resposta do serviço Web.<br/>       |



 

### <a name="paged-results"></a>Resultados de página

Talvez você queira limitar o número de resultados retornados por solicitação. Você pode optar por retornar uma "página" de resultados por vez ou fazer com que o provedor OpenSearch receba páginas adicionais de resultados por número de item ou número de página. Por exemplo, se você enviar vinte resultados por página, a primeira página que você enviar começará no índice de item 1 e na página 1; a segunda página que você envia começa no índice de item 21 e na página 2. Você pode definir como deseja que o provedor OpenSearch solicite itens usando o ou o `{startItem}` token no modelo de `{startPage}` URL.

### <a name="paging-using-the-item-index"></a>Paging usando o índice de item

Um índice de item identifica o primeiro item de resultado em uma página de resultados. Se você quiser que os clientes enviem solicitações usando um índice de item, poderá usar o token no atributo de modelo de elemento `{startIndex}` **url,** conforme mostrado no código a seguir. 


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



O [OpenSearch](https://github.com/dewitt/opensearch) de dados substitui o token na URL por um valor de índice inicial. A primeira solicitação começa com o primeiro item, conforme ilustrado no exemplo a seguir:


```
https://example.com/rss.php?query=frogs&start=1
```



O OpenSearch provedor pode obter itens adicionais alterando o valor do parâmetro e `{startIndex}` emindo uma nova solicitação. O provedor repete esse processo até que ele obtém resultados suficientes para atender ao limite ou atingir o final dos resultados. O OpenSearch provedor analisa o número de itens retornados pelo serviço Web na primeira página de resultados e define o tamanho esperado da página para esse número. Ele usa esse número para incrementar o `{startIndex}` valor para solicitações subsequentes. Por exemplo, se o serviço Web retornar 20 resultados na primeira solicitação, o provedor define o tamanho esperado da página como 20. Para a próxima solicitação, o provedor `{startIndex}` substitui pelo valor de 21 para obter os próximos 20 itens.

> [!Note]  
> Se uma página de resultados retornados pelo serviço Web tiver menos itens do que o tamanho esperado da página, o provedor OpenSearch assumirá que recebeu a última página de resultados e para de fazer solicitações.

 

### <a name="paging-using-the-page-index"></a>Paging Usando o índice de página

Um índice de página identifica a página de resultados especificada. Se você quiser que os clientes enviem solicitações usando um número de página, poderá usar o token no atributo de modelo de elemento de formato url para indicar isso, conforme ilustrado no exemplo a `{startPage}` seguir:  


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



O OpenSearch de dados substitui o token na URL por um parâmetro de número de página. A primeira solicitação começa com a primeira página, conforme mostrado no exemplo a seguir:


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Se uma página de resultados retornados pelo serviço Web tiver menos itens do que o tamanho esperado da página, o provedor OpenSearch assumirá que recebeu a última página de resultados e para de fazer solicitações.

 

### <a name="page-size"></a>Tamanho da Página

Talvez você queira configurar seu serviço Web para permitir que uma solicitação especifique o tamanho das páginas usando algum parâmetro na URL. Uma solicitação deve ser especificada no arquivo .osdx usando o `{count}` token , da seguinte forma:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



O [OpenSearch](https://github.com/dewitt/opensearch) provedor pode definir o tamanho desejado da página, em número de resultados por página, conforme mostrado no exemplo a seguir:


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



Por padrão, o OpenSearch faz solicitações usando um tamanho de página de 50. Se você quiser um tamanho de página diferente, não forneça um token e, em vez disso, coloque o número desejado diretamente no elemento de modelo `{count}` **de** URL.

O OpenSearch provedor determina o tamanho da página com base no número de resultados retornados na primeira solicitação. Se a primeira página de resultados recebida tiver menos itens do que a contagem solicitada, o provedor redefini o tamanho da página para quaisquer solicitações de página subsequentes. Se as solicitações de página subsequentes retornarem menos itens do que o solicitado, o provedor de OpenSearch assumirá que ele atingiu o final dos resultados.

## <a name="extended-elements-in-windows-federated-search"></a>Elementos estendidos Windows pesquisa federada

Além dos elementos padrão, a pesquisa federada dá suporte aos seguintes elementos estendidos: **MaximumResultCount** e **ResultsProcessing.**

Como esses elementos filho estendidos não têm suporte na especificação [OpenSearch](https://github.com/dewitt/opensearch) v1.1, eles devem ser adicionados usando o seguinte namespace:


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Contagem máxima de resultados

Por padrão, os conectores de pesquisa são limitados a 100 resultados por consulta de usuário. Esse limite pode ser personalizado incluindo o **elemento MaximumResultCount** dentro do arquivo OSD, conforme mostrado no exemplo a seguir:


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



O exemplo anterior declara o prefixo de namespace no elemento `ms-ose` **OpenSearchDescription** de nível superior e, em seguida, o usa como um prefixo no nome do elemento. Essa declaração é necessária porque Não há suporte para **MaximumResultCount** na [especificação OpenSearch](https://github.com/dewitt/opensearch) v1.1.

### <a name="property-mapping"></a>Mapeamento de propriedade

Quando os resultados são retornados pelo serviço Web como um RSS ou feed Atom, o provedor OpenSearch deve mapear os metadados do item nos feeds para propriedades que o shell Windows pode usar. A captura de tela a seguir ilustra como o provedor OpenSearch mapeia alguns dos elementos RSS padrão.

![captura de tela mostrando mapeamentos de propriedade rss-to-windows-shell integrados](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Mapeamentos padrão

Os mapeamentos padrão de elementos XML do RSS Windows propriedades do sistema shell são listados na tabela a seguir. Os caminhos XML são relativos ao elemento de item. O `"media:"` prefixo é definido pelo [namespace do Namespace](https://www.rssboard.org/media-rss) do Yahoo Search.



| Caminho XML do RSS                  | Windows Propriedade shell (nome canônico) |
|-------------------------------|-----------------------------------------|
| Link                          | System.ItemUrl                          |
| Título                         | System.ItemName                         |
| Autor                        | System.Author                           |
| pubDate                       | System.DateModified                     |
| Descrição                   | System.AutoSummary                      |
| Categoria                      | System.Keywords                         |
| enclosure/@type               | System.MIMEType                         |
| enclosure/@length             | System.Size                             |
| enclosure/@url                | System.ContentUrl                       |
| media:category                | System.Keywords                         |
| media:content/@fileSize       | System.Size                             |
| media:content/@type           | System.MIMEType                         |
| media:content/@url            | System.ContentUrl                       |
| media:group/content/@fileSize | System.Size                             |
| media:group/content/@type     | System.MIMEType                         |
| media:group/content/@url      | System.ContentUrl                       |
| media:thumbnail/@url          | System.ItemThumbnailUrl                 |



 

> [!Note]  
> Além dos mapeamentos padrão de elementos RSS ou Atom padrão, você pode mapear outras propriedades do sistema shell do Windows incluindo elementos XML adicionais no namespace Windows para cada uma das propriedades. Você também pode mapear elementos de outros namespaces XML existentes, como MediaRSS, iTunes e assim por diante, adicionando o mapeamento de propriedade personalizado no arquivo .osdx.

 

### <a name="custom-property-mappings"></a>Mapeamentos de propriedade personalizados

Você pode personalizar o mapeamento de elementos da saída do RSS para Windows do sistema shell especificando o mapeamento no arquivo .osdx.

A saída do RSS especifica:

-   Um namespace XML e
-   Para qualquer elemento filho de um item, um nome de elemento para mapear.

O arquivo .osdx identifica uma propriedade Windows Shell para cada nome de elemento em um namespace. Os mapeamentos de propriedade que você define no arquivo .osdx substituem os mapeamentos padrão, se existirem, para essas propriedades especificadas.

O diagrama a seguir ilustra como uma extensão RSS é mapeado para Windows propriedades (nome canônico).

![diagrama mostrando que a combinação de namespace xml e caminho xml produz o nome canônico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Exemplo de resultados do RSS e mapeamento de propriedade osd

O exemplo de saída RSS a seguir identifica `https://example.com/schema/2009` como o namespace XML com o prefixo "example". Esse prefixo deve aparecer novamente antes do **elemento de email.**


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



No arquivo .osdx de exemplo a seguir, o elemento **de email** XML é mapeado para a propriedade Windows Shell [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).


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



Há algumas propriedades que não podem ser mapeadas porque os valores para elas são substituídos posteriormente ou não são editáveis. Por exemplo, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) ou [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) não podem ser mapeados porque são calculados com base no valor de URL fornecido nos elementos de link ou compartimento.

### <a name="thumbnails"></a>Miniaturas

UrLs de imagem em miniatura podem ser fornecidas para qualquer item usando o **elemento media:thumbnail url="".** A resolução ideal é de 150 x 150 pixels. As maiores miniaturas com suporte são 256 x 256 pixels. Fornecer imagens maiores leva mais largura de banda para nenhum benefício adicional para o usuário.

### <a name="open-file-location-context-menu"></a>Menu de contexto Abrir Local do Arquivo

Windows fornece um menu de atalho chamado **Abrir local do arquivo para** itens de resultado. Se o usuário selecionar um item nesse menu, a URL "pai" do item selecionado será aberta. Se a URL for uma URL da Web, como , o navegador da `https://...` Web será aberto e navegará até essa URL. Seu feed deve fornecer uma URL personalizada para cada item para garantir que Windows abra uma URL válida. Isso pode ser feito incluindo a URL dentro de um elemento dentro do XML do item, conforme ilustrado no exemplo a seguir:


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



Se essa propriedade não for definida explicitamente no XML do item, o provedor OpenSearch o definirá como a pasta pai da URL do item. No exemplo acima, o provedor OpenSearch usaria o valor do link e definiria o valor da propriedade [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell como `"https://example.com/"` .

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Personalizar exibições Windows Explorer com listas de descrição da propriedade

Alguns Windows layouts de exibição do Explorer são definidos por listas de descrições de propriedade ou proplists. Uma lista de propriedades é uma lista delimitada por ponto e vírgula de propriedades, como , que é usada para controlar como os resultados aparecem no `"prop:System.ItemName; System.Author"` Windows Explorer.

As áreas de interface do Windows Explorer que podem ser personalizadas usando proplists são ilustradas na captura de tela a seguir:

![captura de tela mostrando as áreas de interface do usuário do Windows Explorer que podem ser personalizadas usando proplists](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

Cada área do Windows Explorer tem um conjunto associado de proplists, que são especificados como propriedades. Você pode especificar listas de propriedades personalizadas para itens individuais em seus conjuntos de resultados ou para todos os itens em um conjunto de resultados.



| Área de interface do usuário para personalizar               | Windows Propriedade shell que implementa a personalização |
|------------------------------------|----------------------------------------------------------|
| Modo de exibição de conteúdo (ao pesquisar) | System.PropList.ContentViewModeForSearch                 |
| Modo de exibição de conteúdo (ao navegar)  | System.PropList.ContentViewModeForBrowse                 |
| Modo de exibição de tile                     | System.PropList.TileInfo                                 |
| Painel de detalhes                       | System.PropList.PreviewDetails                           |
| Infotip (dica de ferramenta de foco do item)     | System.PropList.Infotip                                  |



 

 

**Para especificar uma lista de propriedades exclusiva para um item individual:**

1.  Na saída do RSS, adicione um elemento personalizado que representa a lista de propriedades que você deseja personalizar. Por exemplo, o exemplo a seguir define a lista para o painel de detalhes:
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Para aplicar uma propriedade a cada item nos resultados da pesquisa sem modificar a saída do RSS, especifique uma lista de propriedades dentro de um elemento **ms-ose:PropertyDefaultValues** no arquivo .osdx, conforme mostrado no exemplo a seguir:

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Layout de propriedades do modo de exibição de conteúdo

A lista de propriedades especificada nas listas de propriedades **System.PropList.ContentViewModeForSearch** e **System.PropList.ContentViewModeForBrowse** determina o que é mostrado no modo de exibição conteúdo. Para obter mais informações sobre listas de propriedades, consulte [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).

As propriedades são colocadas de acordo com os números mostrados no seguinte padrão de layout:

![captura de tela mostrando o padrão de layout na exibição de conteúdo](images/propertiesnumberslayoutpattern.png)

Se usarmos a lista de propriedades a seguir,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



Em seguida, vemos a seguinte exibição:

![captura de tela mostrando o layout da propriedade de exemplo.](images/samplepropertylayout.png)

> [!Note]  
> Para melhor leitura, as propriedades mostradas na coluna mais à direita devem ser rotuladas.

 

### <a name="property-list-flags"></a>Sinalizadores de lista de propriedades

Somente um dos sinalizadores definidos na documentação proplists se aplica à exibição de itens em layouts de modo de Exibição de Conteúdo: ` "~"` . Nos exemplos anteriores, a exibição Windows Explorer rotula algumas das propriedades, como `Tags: animals; zoo; lion` . Esse é o comportamento padrão quando você especifica uma propriedade na lista. Por exemplo, a lista de propriedades `"System.Author"` tem que é exibida como `"Authors: value"` . Quando você quiser ocultar o rótulo da propriedade, coloque `"~"` um na frente do nome da propriedade. Por exemplo, se a lista de propriedades tiver `"~System.Size"` , a propriedade será exibida como apenas um valor, sem o rótulo.

## <a name="previews"></a>Visualizações

Quando o usuário seleciona um item de resultado no Windows Explorer e o painel de visualização está aberto, o conteúdo do item é visualizado.

O conteúdo a ser mostrar na versão prévia é especificado por uma URL, que é determinada da seguinte forma:

1.  Se a **propriedade System.WebPreviewUrl** Windows Shell estiver definida para o item, use essa URL.
    > [!Note]  
    > A propriedade precisa ser fornecida no RSS usando o namespace Windows Shell ou explicitamente mapeado no arquivo .osdx.

     

2.  Caso contrário, use a URL do link.

O fluxograma a seguir mostra essa lógica.

![fluxograma mostrando como o Windows Explorer seleciona a URL a ser usada para versões prévias](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

É possível usar uma URL diferente para a versão prévia do item em si. Isso significa que, se você fornecer URLs diferentes para a URL do link e o compartimento ou , o Windows Explorer usará a URL de link para visualizações do item, mas usará a outra URL para detecção, abertura, download e assim por `media:content URL` diante.

Como Windows Explorer determina qual URL usar:

1.  Se você fornecer um mapeamento para [System.ItemFolderPathDisplay,](../properties/props-system-itemfolderpathdisplay.md)o Windows Explorer usará essa URL
2.  Se você não fornecer um mapeamento, Windows Explorer identificará se as URLs do link e do compartimento são diferentes. Nesse caso, o Windows Explorer usa a URL do link.
3.  Se as URLs são as mesmas ou se houver apenas uma URL de link, o Windows Explorer analisará o link para encontrar o contêiner pai removendo o nome do arquivo da URL completa.
    > [!Note]  
    > Se você reconhecer que a análise de URL resultaria em links inoos para o serviço, forneça um mapeamento explícito para a propriedade .

     

## <a name="open-file-location-menu-item"></a>Item de menu Abrir Local do Arquivo

Quando um clica com o botão direito do mouse em um item, o comando de menu **Abrir local do** arquivo é exibido. Esse comando leva o usuário para o contêiner ou para o local desse item. Por exemplo, em uma SharePoint, selecionar essa opção para um arquivo em uma biblioteca de documentos abriria a raiz da biblioteca de documentos no navegador da Web.

Quando um usuário clica em **Abrir** local do arquivo, Windows Explorer tenta localizar um contêiner pai, usando a lógica mostrada no fluxograma a seguir:

![fluxograma mostrando como o Windows Explorer identifica um contêiner pai](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a>Recursos adicionais

Para obter informações adicionais sobre como implementar a federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch no Windows 7 e posterior, consulte "Recursos adicionais" em [Pesquisa Federada](/previous-versions//dd742958(v=vs.85))no Windows .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Ponto de Partida com a Pesquisa Federada Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conectando seu serviço Web Windows Pesquisa Federada](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitando seu armazenamento de dados Windows pesquisa federada](-search-federated-search-data-store.md)
</dt> <dt>

[Seguindo as práticas recomendadas Windows pesquisa federada](-search-fedsearch-best.md)
</dt> <dt>

[Implantando conectores de pesquisa Windows Pesquisa Federada](-search-federated-search-deploying.md)
</dt> </dl>

 

 
