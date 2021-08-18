---
description: explica como habilitar o armazenamento de dados para ser acessado por um serviço web OpenSearch e como evitar possíveis barreiras para isso.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: habilitando seu armazenamento de dados no Windows pesquisa federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26feb231f17dbaacb9656f2ef91e1cdb64bc598831a1e4808327dff7e5787bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456747"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>habilitando seu armazenamento de dados no Windows pesquisa federada

explica como habilitar o armazenamento de dados para ser acessado por um serviço web [OpenSearch](https://github.com/dewitt/opensearch) e como evitar possíveis barreiras para isso.

Este tópico é organizado da seguinte maneira:

-   [Condições para a aceitação da solicitação de pesquisa](#conditions-for-search-request-acceptance)
    -   [Sintaxe de consulta com suporte](#supported-query-syntax)
    -   [Protocolos de autenticação com suporte](#supported-authentication-protocols)
-   [Enviando consultas e retornando resultados da pesquisa em RSS ou Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Exemplo de uma saída de RSS feed](#example-of-an-rss-feed-output)
-   [mapeamento automático para Windows propriedades do Shell](#automatic-mapping-to-windows-shell-properties)
-   [compreendendo como Mapas do Windows itens aos tipos de arquivo](#understanding-how-windows-maps-items-to-file-types)
-   [Evitando possíveis barreiras para habilitar um armazenamento de dados](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Condições para a aceitação da solicitação de pesquisa

o serviço web [OpenSearch](https://github.com/dewitt/opensearch) criado no servidor web **deve** atender aos dois requisitos a seguir:

-   Ser capaz de aceitar uma `GET URL` consulta do cliente.
-   Permitir que os termos de pesquisa sejam inseridos na URL.

    O exemplo a seguir mostra como um termo de pesquisa pode ser inserido em uma URL.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> A pesquisa federada não dá suporte ao envio `POST` de solicitações para um serviço Web.

 

para obter mais informações sobre como construir uma URL, consulte "parâmetros de modelo de URL" em [criando um arquivo de descrição de OpenSearch em Windows pesquisa federada](-search-federated-search-osdx-file.md).

### <a name="supported-query-syntax"></a>Sintaxe de consulta com suporte

não há sintaxe de consulta específica esperada no Windows 7. o provedor de OpenSearch aceita quaisquer termos que o usuário insere na caixa de entrada no Windows Explorer e o codifica na URL. ele faz isso de acordo com o modelo de url descrito em "parâmetros de modelo de url" na [criação de um arquivo de descrição de OpenSearch em Windows pesquisa federada](-search-federated-search-osdx-file.md).

Os usuários esperam que termos separados sejam tratados como ANDed implicitamente juntos. por exemplo, uma consulta para "Microsoft Windows" deve retornar apenas os resultados que contenham "Windows" e "Microsoft".

### <a name="supported-authentication-protocols"></a>Protocolos de autenticação com suporte

Windows a pesquisa federada dá suporte à autenticação baseada em Windows e pode fornecer credenciais para serviços web por meio dos seguintes protocolos:

-   NTLM.
-   Kerberos.
-   Básico (somente via HTTPS).
-   outros SSPs (provedores de suporte de segurança) instalados em Windows que fornecem capacidade de consulta adicional. Consulte a documentação do SDK da [interface do SSP](../secauthn/sspi.md) para manter-se atualizado sobre a possível adição de outros SSPs.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Enviando consultas e retornando resultados da pesquisa em RSS ou Atom

o provedor de [OpenSearch](https://github.com/dewitt/opensearch) é responsável por mapear os valores do elemento XML para Windows propriedades do sistema Shell que podem ser usadas pelos aplicativos Windows. mas você não está limitado aos mapeamentos padrão de elementos RSS ou Atom padrão e pode incluir elementos XML personalizados no namespace Windows para cada uma das propriedades. Por exemplo, você pode adicionar seus próprios elementos XML personalizados dentro do elemento **Item** para fornecer metadados adicionais para Windows. Você também pode mapear elementos de outros namespaces XML, como o iTunes

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



para obter informações mais detalhadas sobre o mapeamento de propriedade, consulte as seções "elementos estendidos na pesquisa federada do WIndows" e "mapeamentos de propriedade personalizada" em [criando um arquivo de descrição de OpenSearch em Windows pesquisa federada](-search-federated-search-osdx-file.md).

## <a name="automatic-mapping-to-windows-shell-properties"></a>mapeamento automático para Windows propriedades do Shell

dentro dos itens em seu RSS feed, você pode optar por incluir outros elementos XML que são mapeados automaticamente para Windows propriedades do sistema Shell. para fazer isso, inclua um elemento chamado após a propriedade Windows shell e prefixado com o namespace do sistema Windows Shell. O exemplo a seguir ilustra a declaração de namespace `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` e a inclusão de um elemento para o mapeamento de propriedade `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



O prefixo de namespace usado aqui ( `"win"` ) é uma sugestão; você pode usar qualquer prefixo. no entanto, você deve usar os nomes de propriedade de Shell exatos Windows e deve incluir o Uniform Resource Identifier (URI) exato, conforme mostrado no exemplo a seguir:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**sobre as propriedades do sistema Windows Shell**

Windows define uma lista completa de [propriedades do sistema](../properties/props.md) e o formato do tipo de valor necessário para cada propriedade. A documentação para a propriedade [System. FileExtension](../properties/props-system-fileextension.md) do Shell de janela, por exemplo, especifica que o valor deve conter o ponto à esquerda (".docx" e não "docx").

**Valores de data e hora**

O formato de data e hora preferencial é ISO-8601, conforme mostrado no exemplo a seguir:


```
2008-01-16T 19:20:30:.45+01:00
```



Os desenvolvedores do .NET devem usar a classe DateTime com `ToString("R") ` para gerar o formato correto.

para obter informações mais detalhadas sobre o mapeamento de propriedade, consulte "elementos estendidos em Windows pesquisa federada" em [criando um arquivo de descrição de OpenSearch no Windows pesquisa federada](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>compreendendo como Mapas do Windows itens aos tipos de arquivo

pesquisar dentro da interface do usuário do Windows Explorer permite que os usuários tratem os resultados como arquivos quando um item RSS aponta para um arquivo armazenado remotamente. o usuário pode arrastar e soltar itens para a área de trabalho, e a interface do usuário do Windows Explorer exibe o ícone correto e fornece o menu de atalho apropriado. Se o item RSS não apontar para um arquivo armazenado remotamente, o arquivo será tratado como um link e os usuários poderão executar ações nele, como criar um atalho ou abri-lo no navegador.

o fluxograma a seguir mostra como Windows determina o tipo de arquivo de um item.

![fluxograma mostrando caminhos de um item para decisões para tratá-lo como um item de tipo de link da Web ou como um tipo de arquivo](images/determineanitemfiletype.png)

o provedor de [OpenSearch](https://github.com/dewitt/opensearch) executa as seguintes etapas para mapear um item para um tipo de arquivo:

-   Identifique se o item deve ser tratado como um arquivo ou um link da Web.
-   Identifique a extensão de nome de arquivo correta a ser usada.

por exemplo, se o item tiver uma URL de link que usa um caminho de sistema de arquivos (como `file:///\\server\share\etc\item.ext` ), o provedor de [OpenSearch](https://github.com/dewitt/opensearch) tratará o link como um arquivo e determinará o tipo pela extensão de nome de arquivo usada no caminho (. ext neste exemplo).

se o item usar o elemento RSS standard ou **MediaRSS media: content** , o provedor de [OpenSearch](https://github.com/dewitt/opensearch) pressupõe que o item é um arquivo e identifica a extensão de nome de arquivo da seguinte maneira:

-   se a propriedade de Shell [System. FileExtension](../properties/props-system-fileextension.md) Windows tiver sido mapeada para o item, o provedor usará essa extensão de nome de arquivo.
-   se a propriedade de Shell [System. FileExtension](../properties/props-system-fileextension.md) Windows não tiver sido mapeada, o provedor usará o atributo **Type** especificado no elemento de compartimento ou de conteúdo. Esse elemento deve conter uma `MIMEType` cadeia de caracteres, como `"image/jpeg"` . Se o `MIMEType` estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o item será considerado como um arquivo desse tipo. Se o `MIMEType` não estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o item será tratado como um tipo de link da Web. o provedor de [OpenSearch](https://github.com/dewitt/opensearch) não tenta analisar o atributo de **Url** para localizar a extensão de nome de arquivo.
-   Se o `MIMEType` estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o provedor determinará se a extensão de nome de arquivo é um tipo de arquivo da Web conhecido (.htm, .html,. asp,. aspx,. php,. swf,. stm). Nesse caso, o tipo de arquivo é considerado um tipo de link da Web; caso contrário, será considerado um tipo de arquivo. Por exemplo, se o `MIMEType "text/html"` estiver associado à extensão de nome de arquivo .htm, esse item será considerado como um link da Web em vez de um tipo de arquivo .htm.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Evitando possíveis barreiras para habilitar um armazenamento de dados

alguns armazenamentos de dados não fornecem um serviço web compatível com [OpenSearch](https://github.com/dewitt/opensearch), mas ainda podem ser conectados a Windows pesquisa federada. Esses armazenamentos de dados incluem:

-   índices remotos com métodos de autenticação que não têm suporte na pesquisa federada do Windows 7.

    Os exemplos incluem autenticação baseada em formulários e outros métodos de autenticação personalizados.

-   se um armazenamento público de alto valor tiver APIs web públicas, qualquer pessoa poderá escrever outro serviço web [OpenSearch](https://github.com/dewitt/opensearch)compatível e chamar essas APIs nos bastidores.

    Os exemplos incluem a biblioteca do Congresso e bancos de dados de pesquisa médica.

-   Armazenamentos de dados corporativos ou índices proprietários e armazenamentos de gerenciamento de conteúdo herdados, para os quais pode ser impossível implementar um front-end.

No entanto, há alternativas que podem evitar barreiras para habilitar um armazenamento de dados. A seguir estão algumas dessas alternativas:

**Para gravar um serviço Web intermediário quando você não pode modificar o serviço Web para a fonte de dados existente ou o serviço Web fornece uma API personalizada:**

1.  escreva um serviço web de man-middle que possa aceitar uma consulta Windows 7.
2.  Conexão à fonte de dados e recuperar os resultados da consulta.
3.  Reformate os resultados no formato RSS ou Atom.
4.  retornar os resultados para o cliente do Windows 7.
5.  Observe que para o Enterprise Data Services e muitos serviços de dados da Internet, talvez seja necessário passar as credenciais do usuário por meio de em nome do serviço Web para executar a corte de resultados com base nas permissões do usuário.

**Para usar um mecanismo de pesquisa existente quando não for possível habilitar um armazenamento de dados público:**

1.  Use um mecanismo de pesquisa pública que já dá suporte a [OpenSearch](https://github.com/dewitt/opensearch) com RSS. Você pode fazer isso fornecendo aos usuários um arquivo. osdx que tem um modelo de URL que restringe os resultados para apenas aqueles para seu domínio específico.
2.  consulte o exemplo a seguir de uma descrição de [OpenSearch](https://github.com/dewitt/opensearch) para pesquisar somente o conteúdo da ajuda para Windows usando uma consulta em relação a live.com.

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

    

**para usar um servidor de indexação existente que dá suporte a OpenSearch quando não é possível habilitar armazenamentos de dados corporativos próprios ou índices:**

1.  selecione um servidor de indexação existente que dê suporte a [OpenSearch](https://github.com/dewitt/opensearch) para indexar o conteúdo, como o SharePoint servidor de pesquisa.
2.  crie um arquivo. osdx que restringe os resultados do índice de SharePoint para apenas aqueles do seu servidor usando a sintaxe de palavra-chave no modelo de URL.

**Para gravar um armazenamento de dados no lado do cliente se uma solução somente no lado do servidor não funcionar:**

1.  escreva uma fonte de dados [OpenSearch](https://github.com/dewitt/opensearch) no lado do cliente que se situa entre o provedor de [OpenSearch](https://github.com/dewitt/opensearch) Windows e a fonte de dados externa.
2.  Use a API de [Interface IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) no SDK do Windows para criar um arquivo. searchconnector-ms configurado adequadamente por meio do qual o Windows Explorer pode chamar sua implementação com os parâmetros de consulta. Em seguida, sua implementação pode retornar os resultados formatados no formato RSS ou Atom. Isso permite que sua implementação forneça a interface do usuário de autenticação personalizada e se conecte à fonte de dados usando sua API proprietária.

> [!Note]  
> Abrir um arquivo. osdx cria um arquivo. searchconnector-MS (conector de pesquisa) no diretório% USERPROFILE%/Searches e coloca um link para ele no diretório% USERPROFILE%/links.

 

## <a name="additional-resources"></a>Recursos adicionais

para obter informações adicionais sobre como implementar a federação de pesquisa em armazenamentos de dados remotos usando OpenSearch tecnologias no Windows 7 e posterior, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introdução com pesquisa federada no Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[conectando seu serviço web no Windows pesquisa federada](-search-federated-search-web-service.md)
</dt> <dt>

[criando um arquivo de descrição de OpenSearch no Windows pesquisa federada](-search-federated-search-osdx-file.md)
</dt> <dt>

[seguindo as práticas recomendadas em Windows pesquisa federada](-search-fedsearch-best.md)
</dt> <dt>

[implantando conectores de pesquisa no Windows pesquisa federada](-search-federated-search-deploying.md)
</dt> </dl>

 

 
