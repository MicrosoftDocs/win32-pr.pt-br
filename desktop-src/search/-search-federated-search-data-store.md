---
description: Explica como habilitar o armazenamento de dados para ser acessado por um serviço Web do OpenSearch e como evitar possíveis barreiras para isso.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Habilitando seu armazenamento de dados na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791062"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Habilitando seu armazenamento de dados na pesquisa federada do Windows

Explica como habilitar o armazenamento de dados para ser acessado por um serviço Web do [OpenSearch](https://github.com/dewitt/opensearch) e como evitar possíveis barreiras para isso.

Este tópico é organizado da seguinte maneira:

-   [Condições para a aceitação da solicitação de pesquisa](#conditions-for-search-request-acceptance)
    -   [Sintaxe de consulta com suporte](#supported-query-syntax)
    -   [Protocolos de autenticação com suporte](#supported-authentication-protocols)
-   [Enviando consultas e retornando resultados da pesquisa em RSS ou Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Exemplo de uma saída de RSS feed](#example-of-an-rss-feed-output)
-   [Mapeamento automático para propriedades do shell do Windows](#automatic-mapping-to-windows-shell-properties)
-   [Noções básicas sobre como o Windows mapeia itens para tipos de arquivo](#understanding-how-windows-maps-items-to-file-types)
-   [Evitando possíveis barreiras para habilitar um armazenamento de dados](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Condições para a aceitação da solicitação de pesquisa

O serviço Web do [OpenSearch](https://github.com/dewitt/opensearch) que você cria em seu servidor Web **deve** atender aos dois requisitos a seguir:

-   Ser capaz de aceitar uma `GET URL` consulta do cliente.
-   Permitir que os termos de pesquisa sejam inseridos na URL.

    O exemplo a seguir mostra como um termo de pesquisa pode ser inserido em uma URL.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> A pesquisa federada não dá suporte ao envio `POST` de solicitações para um serviço Web.

 

Para obter mais informações sobre como construir uma URL, consulte "parâmetros de modelo de URL" em [criando um arquivo de descrição de OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md).

### <a name="supported-query-syntax"></a>Sintaxe de consulta com suporte

Não há sintaxe de consulta específica esperada no Windows 7. O provedor de OpenSearch aceita quaisquer termos que o usuário insere na caixa de entrada no Windows Explorer e o codifica na URL. Ele faz isso de acordo com o modelo de URL descrito em "parâmetros de modelo de URL" na [criação de um arquivo de descrição de OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md).

Os usuários esperam que termos separados sejam tratados como ANDed implicitamente juntos. Por exemplo, uma consulta para "Microsoft Windows" deve retornar apenas os resultados que contenham "Windows" e "Microsoft".

### <a name="supported-authentication-protocols"></a>Protocolos de autenticação com suporte

A pesquisa federada do Windows dá suporte à autenticação baseada no Windows e pode fornecer credenciais aos serviços Web por meio dos seguintes protocolos:

-   NTLM.
-   Kerberos.
-   Básico (somente via HTTPS).
-   Outros SSPs (provedores de suporte de segurança) instalados no Windows que fornecem capacidade de consulta adicional. Consulte a documentação do SDK da [interface do SSP](../secauthn/sspi.md) para manter-se atualizado sobre a possível adição de outros SSPs.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Enviando consultas e retornando resultados da pesquisa em RSS ou Atom

O provedor de [OpenSearch](https://github.com/dewitt/opensearch) é responsável por mapear os valores do elemento XML para as propriedades do sistema do shell do Windows que podem ser usadas por aplicativos do Windows. Mas você não está limitado aos mapeamentos padrão de elementos RSS ou Atom padrão e pode incluir elementos XML personalizados no namespace do Windows para cada uma das propriedades. Por exemplo, você pode adicionar seus próprios elementos XML personalizados dentro do elemento **Item** para fornecer metadados adicionais ao Windows. Você também pode mapear elementos de outros namespaces XML, como o iTunes

### <a name="example-of-an-rss-feed-output"></a>Exemplo de uma saída de RSS feed

O exemplo de saída de RSS feed a seguir retorna um item.


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



Para obter informações mais detalhadas sobre o mapeamento de propriedade, consulte as seções "elementos estendidos na pesquisa federada do WIndows" e "mapeamentos de propriedade personalizada" em [criando um arquivo de descrição de OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md).

## <a name="automatic-mapping-to-windows-shell-properties"></a>Mapeamento automático para propriedades do shell do Windows

Dentro dos itens em seu RSS feed, você pode optar por incluir outros elementos XML que são mapeados automaticamente para as propriedades do sistema shell do Windows. Para fazer isso, inclua um elemento chamado após a propriedade shell do Windows e prefixado com o namespace do sistema shell do Windows. O exemplo a seguir ilustra a declaração de namespace `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` e a inclusão de um elemento para o mapeamento de propriedade `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



O prefixo de namespace usado aqui ( `"win"` ) é uma sugestão; você pode usar qualquer prefixo. No entanto, você deve usar os nomes de Propriedade do shell do Windows exatos e deve incluir o Uniform Resource Identifier exato (URI), conforme mostrado no exemplo a seguir:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**Sobre as propriedades do sistema shell do Windows**

O Windows define uma lista completa de [Propriedades do sistema](../properties/props.md) e o formato do tipo de valor necessário para cada propriedade. A documentação para a propriedade [System. FileExtension](../properties/props-system-fileextension.md) do Shell de janela, por exemplo, especifica que o valor deve conter o ponto à esquerda (". docx" e não "docx").

**Valores de data e hora**

O formato de data e hora preferencial é ISO-8601, conforme mostrado no exemplo a seguir:


```
2008-01-16T 19:20:30:.45+01:00
```



Os desenvolvedores do .NET devem usar a classe DateTime com `ToString("R") ` para gerar o formato correto.

Para obter informações mais detalhadas sobre o mapeamento de propriedade, consulte "elementos estendidos na pesquisa federada do Windows" em [criando um arquivo de descrição de OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Noções básicas sobre como o Windows mapeia itens para tipos de arquivo

Pesquisar dentro da interface do usuário do Windows Explorer permite que os usuários tratem os resultados como arquivos quando um item RSS aponta para um arquivo armazenado remotamente. O usuário pode arrastar e soltar itens para a área de trabalho, e a interface do usuário do Windows Explorer exibe o ícone correto e fornece o menu de atalho apropriado. Se o item RSS não apontar para um arquivo armazenado remotamente, o arquivo será tratado como um link e os usuários poderão executar ações nele, como criar um atalho ou abri-lo no navegador.

O fluxograma a seguir mostra como o Windows determina o tipo de arquivo de um item.

![fluxograma mostrando caminhos de um item para decisões para tratá-lo como um item de tipo de link da Web ou como um tipo de arquivo](images/determineanitemfiletype.png)

O provedor de [OpenSearch](https://github.com/dewitt/opensearch) executa as seguintes etapas para mapear um item para um tipo de arquivo:

-   Identifique se o item deve ser tratado como um arquivo ou um link da Web.
-   Identifique a extensão de nome de arquivo correta a ser usada.

Por exemplo, se o item tiver uma URL de link que usa um caminho de sistema de arquivos (como `file:///\\server\share\etc\item.ext` ), o provedor de [OpenSearch](https://github.com/dewitt/opensearch) tratará o link como um arquivo e determinará o tipo pela extensão de nome de arquivo usada no caminho (. ext neste exemplo).

Se o item usar o elemento RSS Standard ou **MediaRSS Media: content** , o provedor de [OpenSearch](https://github.com/dewitt/opensearch) pressupõe que o item é um arquivo e identifica a extensão de nome de arquivo da seguinte maneira:

-   Se a propriedade shell do Windows [System. FileExtension](../properties/props-system-fileextension.md) tiver sido mapeada para o item, o provedor usará essa extensão de nome de arquivo.
-   Se a propriedade shell do Windows [System. FileExtension](../properties/props-system-fileextension.md) não tiver sido mapeada, o provedor usará o atributo **Type** especificado no elemento de compartimento ou de conteúdo. Esse elemento deve conter uma `MIMEType` cadeia de caracteres, como `"image/jpeg"` . Se o `MIMEType` estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o item será considerado como um arquivo desse tipo. Se o `MIMEType` não estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o item será tratado como um tipo de link da Web. O provedor de [OpenSearch](https://github.com/dewitt/opensearch) não tenta analisar o atributo de **URL** para localizar a extensão de nome de arquivo.
-   Se o `MIMEType` estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o provedor determinará se a extensão de nome de arquivo é um tipo de arquivo da Web conhecido (. htm,. html,. asp,. aspx,. php,. swf,. stm). Nesse caso, o tipo de arquivo é considerado um tipo de link da Web; caso contrário, será considerado um tipo de arquivo. Por exemplo, se o `MIMEType "text/html"` estiver associado à extensão de nome de arquivo. htm, esse item será considerado como um link da Web em vez de um tipo de arquivo. htm.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Evitando possíveis barreiras para habilitar um armazenamento de dados

Alguns armazenamentos de dados não fornecem um serviço Web compatível com [OpenSearch](https://github.com/dewitt/opensearch), mas ainda podem ser conectados à pesquisa federada do Windows. Esses armazenamentos de dados incluem:

-   Índices remotos com métodos de autenticação que não têm suporte na pesquisa federada do Windows 7.

    Os exemplos incluem autenticação baseada em formulários e outros métodos de autenticação personalizados.

-   Se um armazenamento público de alto valor tiver APIs Web públicas, qualquer pessoa poderá escrever outro serviço Web que seja compatível com [OpenSearch](https://github.com/dewitt/opensearch)e chame essas APIs nos bastidores.

    Os exemplos incluem a biblioteca do Congresso e bancos de dados de pesquisa médica.

-   Armazenamentos de dados corporativos ou índices proprietários e armazenamentos de gerenciamento de conteúdo herdados, para os quais pode ser impossível implementar um front-end.

No entanto, há alternativas que podem evitar barreiras para habilitar um armazenamento de dados. A seguir estão algumas dessas alternativas:

**Para gravar um serviço Web intermediário quando você não pode modificar o serviço Web para a fonte de dados existente ou o serviço Web fornece uma API personalizada:**

1.  Escreva um serviço Web intermediário que possa aceitar uma consulta do Windows 7.
2.  Conecte-se à fonte de dados e recupere os resultados da consulta.
3.  Reformate os resultados no formato RSS ou Atom.
4.  Retorne os resultados para o cliente do Windows 7.
5.  Observe que para o Enterprise Data Services e muitos serviços de dados da Internet, talvez seja necessário passar as credenciais do usuário por meio de em nome do serviço Web para executar a corte de resultados com base nas permissões do usuário.

**Para usar um mecanismo de pesquisa existente quando não for possível habilitar um armazenamento de dados público:**

1.  Use um mecanismo de pesquisa pública que já dá suporte a [OpenSearch](https://github.com/dewitt/opensearch) com RSS. Você pode fazer isso fornecendo aos usuários um arquivo. osdx que tem um modelo de URL que restringe os resultados para apenas aqueles para seu domínio específico.
2.  Consulte o exemplo a seguir de uma descrição de [OpenSearch](https://github.com/dewitt/opensearch) para pesquisar somente o conteúdo da ajuda do Windows usando uma consulta em relação a Live.com.

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

**Para usar um servidor de indexação existente que ofereça suporte a OpenSearch quando você não puder habilitar armazenamentos de dados corporativos próprios ou índices:**

1.  Selecione um servidor de indexação existente que dê suporte a [OpenSearch](https://github.com/dewitt/opensearch) para indexar seu conteúdo, como o servidor de pesquisa do SharePoint.
2.  Crie um arquivo. osdx que restringe os resultados do índice do SharePoint somente para aqueles do seu servidor usando sua sintaxe de palavra-chave no modelo de URL.

**Para gravar um armazenamento de dados no lado do cliente se uma solução somente no lado do servidor não funcionar:**

1.  Escreva uma fonte de dados [OpenSearch](https://github.com/dewitt/opensearch) do lado do cliente que se situa entre o provedor de [OpenSearch](https://github.com/dewitt/opensearch) do Windows e a fonte de dados externa.
2.  Use a API de [interface IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) no SDK do Windows para criar um arquivo. searchconnector-MS configurado adequadamente por meio do qual o Windows Explorer pode chamar sua implementação com os parâmetros de consulta. Em seguida, sua implementação pode retornar os resultados formatados no formato RSS ou Atom. Isso permite que sua implementação forneça a interface do usuário de autenticação personalizada e se conecte à fonte de dados usando sua API proprietária.

> [!Note]  
> Abrir um arquivo. osdx cria um arquivo. searchconnector-MS (conector de pesquisa) no diretório% USERPROFILE%/Searches e coloca um link para ele no diretório% USERPROFILE%/links.

 

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

[Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Seguindo as práticas recomendadas na pesquisa federada do Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implantando conectores de pesquisa na pesquisa federada do Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
