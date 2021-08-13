---
description: Explica como permitir que seu armazenamento de dados seja acessado por um OpenSearch Web e como evitar possíveis barreiras para fazer isso.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Habilitando seu armazenamento de dados Windows Pesquisa Federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26feb231f17dbaacb9656f2ef91e1cdb64bc598831a1e4808327dff7e5787bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456747"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Habilitando seu armazenamento de dados Windows Pesquisa Federada

Explica como permitir que o armazenamento de dados seja acessado por um OpenSearch [Web](https://github.com/dewitt/opensearch) e como evitar possíveis barreiras para fazer isso.

Este tópico é organizado da seguinte forma:

-   [Condições para aceitação da solicitação de pesquisa](#conditions-for-search-request-acceptance)
    -   [Sintaxe de consulta com suporte](#supported-query-syntax)
    -   [Protocolos de autenticação com suporte](#supported-authentication-protocols)
-   [Enviando consultas e retornando resultados da pesquisa no RSS ou atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Exemplo de uma saída do RSS Feed](#example-of-an-rss-feed-output)
-   [Mapeamento automático para propriedades Windows Shell](#automatic-mapping-to-windows-shell-properties)
-   [Noções básicas sobre Mapas do Windows itens para tipos de arquivo](#understanding-how-windows-maps-items-to-file-types)
-   [Evitando possíveis barreiras à habilitação de um armazenamento de dados](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Condições para aceitação da solicitação de pesquisa

O [OpenSearch](https://github.com/dewitt/opensearch) Web criado no servidor Web deve **atender** aos dois requisitos a seguir:

-   Ser capaz de aceitar `GET URL` uma consulta do cliente.
-   Permitir que os termos de pesquisa sejam inseridos na URL.

    O exemplo a seguir mostra como um termo de pesquisa pode ser inserido em uma URL.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> A pesquisa federada não dá suporte ao envio `POST` de solicitações para um serviço Web.

 

Para obter mais informações sobre como construir uma URL, consulte "Parâmetros de modelo de URL" em Criando um arquivo OpenSearch descrição no [Windows Federated Search](-search-federated-search-osdx-file.md).

### <a name="supported-query-syntax"></a>Sintaxe de consulta com suporte

Não há nenhuma sintaxe de consulta específica esperada Windows 7. O OpenSearch provedor aceita quaisquer termos que o usuário insira na caixa de entrada no Windows Explorer e codifica-o na URL. Ele faz isso de acordo com o modelo de URL descrito em "Parâmetros de modelo de URL" em Criando um arquivo OpenSearch descrição no [Windows Federated Search](-search-federated-search-osdx-file.md).

Os usuários esperam que termos separados sejam tratados como ANDed implicitamente juntos. Por exemplo, uma consulta para "Microsoft Windows" deve retornar apenas os resultados que contêm "Windows" e "Microsoft".

### <a name="supported-authentication-protocols"></a>Protocolos de autenticação com suporte

Windows A Pesquisa Federada dá suporte Windows autenticação baseada em dados e pode fornecer credenciais para serviços Web por meio dos seguintes protocolos:

-   NTLM.
-   Kerberos.
-   Básico (somente por https).
-   Outros SSPs (Provedores de Suporte de Segurança) instalados no Windows que fornecem capacidade de consulta adicional. Confira a documentação do SDK da [Interface SSP](../secauthn/sspi.md) para se manter atualizado sobre a possível adição de outros SSPs.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Enviando consultas e retornando resultados da pesquisa no RSS ou atom

O [OpenSearch](https://github.com/dewitt/opensearch) provedor é responsável por mapear os valores do elemento XML para Windows do sistema shell que podem ser usadas por Windows aplicativos. Mas você não está limitado aos mapeamentos padrão de elementos RSS ou Atom padrão e pode incluir elementos XML personalizados no namespace Windows para cada uma das propriedades. Por exemplo, você pode adicionar seus próprios elementos XML personalizados dentro do **elemento de item** para fornecer metadados adicionais para Windows. Você também pode mapear elementos de outros namespaces XML, como o iTunes

### <a name="example-of-an-rss-feed-output"></a>Exemplo de uma saída do RSS Feed

O exemplo a seguir RSS feed saída retorna um item.


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



Para obter informações mais detalhadas sobre o mapeamento de propriedades, consulte as seções "Elementos Estendidos na Pesquisa Federada do WIndows" e "Mapeamentos de Propriedades Personalizadas" em Criando um arquivo de descrição do OpenSearch no [Windows Federated Search](-search-federated-search-osdx-file.md).

## <a name="automatic-mapping-to-windows-shell-properties"></a>Mapeamento automático para propriedades Windows Shell

Dentro dos itens em sua RSS feed, você pode optar por incluir outros elementos XML que são mapeados automaticamente para Windows do sistema shell. Para fazer isso, inclua um elemento chamado após a propriedade Windows Shell e prefixado com o namespace do sistema Windows Shell. O exemplo a seguir ilustra a declaração de namespace `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` e a inclusão de um elemento para o mapeamento de propriedade `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



O prefixo de namespace usado aqui ( `"win"` ) é uma sugestão; você pode usar qualquer prefixo. No entanto, você deve usar os nomes de propriedade Windows Shell exatos e deve incluir o URI (Uniform Resource Identifier) exato, conforme mostrado no exemplo a seguir:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**Sobre Windows do sistema shell**

Windows define uma lista completa de [Propriedades](../properties/props.md) do Sistema e o formato de tipo de valor necessário para cada propriedade. A documentação da propriedade [System.FileExtension](../properties/props-system-fileextension.md) Window Shell, por exemplo, especifica que o valor deve conter o ponto à frente (".docx" e não "docx").

**Valores de data e hora**

O formato de data e hora preferencial é ISO-8601, conforme mostrado no exemplo a seguir:


```
2008-01-16T 19:20:30:.45+01:00
```



Os desenvolvedores do .NET devem usar a classe DateTime com `ToString("R") ` para a saída do formato correto.

Para obter informações mais detalhadas sobre o mapeamento de propriedades, consulte "Extended Elements in Windows Federated Search" em Criando um arquivo de descrição OpenSearch no [Windows Federated Search](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Noções básicas sobre Mapas do Windows itens para tipos de arquivo

Pesquisar na interface do usuário Windows Explorer permite que os usuários tratem os resultados como arquivos quando um item RSS aponta para um arquivo armazenado remotamente. O usuário pode arrastar e soltar itens para a área de trabalho e a interface do usuário Windows Explorer exibe o ícone correto e fornece o menu de atalho apropriado. Se o item RSS não apontar para um arquivo armazenado remotamente, o arquivo será tratado como um link e os usuários poderão executar ações nele, como criar um atalho ou abri-lo no navegador.

O fluxograma a seguir mostra como Windows determina o tipo de arquivo de um item.

![fluxograma mostrando caminhos de um item para decisões para tratá-lo como um item de tipo de link da Web ou como um tipo de arquivo](images/determineanitemfiletype.png)

O [OpenSearch](https://github.com/dewitt/opensearch) provedor executa as seguintes etapas para mapear um item para um tipo de arquivo:

-   Identifique se o item deve ser tratado como um arquivo ou um link da Web.
-   Identifique a extensão de nome de arquivo correta a ser usada.

Por exemplo, se o item tiver uma URL de link que usa um caminho do sistema de arquivos (como ), o provedor OpenSearch tratará o link como um arquivo e determinará o tipo pela extensão de nome de arquivo `file:///\\server\share\etc\item.ext` usado no caminho (.ext [neste](https://github.com/dewitt/opensearch) exemplo).

Se o item usar o compartimento RSS padrão ou o elemento **media:content mediaRSS,** o provedor [OpenSearch](https://github.com/dewitt/opensearch) assumirá que o item é um arquivo e identificará a extensão de nome de arquivo da seguinte forma:

-   Se a [propriedade System.FileExtension](../properties/props-system-fileextension.md) Windows Shell tiver sido mapeada para o item, o provedor usará essa extensão de nome de arquivo.
-   Se a [propriedade System.FileExtension](../properties/props-system-fileextension.md) Windows Shell não tiver sido mapeada, o provedor usará o atributo **Type** especificado no compartimento ou no elemento de conteúdo. Esse elemento deve conter uma cadeia `MIMEType` de caracteres, como `"image/jpeg"` . Se o estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o item será considerado como `MIMEType` um arquivo desse tipo. Se o não estiver associado a uma extensão de nome de arquivo registrada no computador `MIMEType` cliente, o item será tratado como um tipo de link da Web. O [OpenSearch](https://github.com/dewitt/opensearch) provedor não tenta analisar o atributo **url** para localizar a extensão de nome de arquivo.
-   Se o estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o provedor determinará se a extensão de nome de arquivo é um tipo de arquivo Web conhecido `MIMEType` (.htm, .html, .asp, .aspx, .php, .swf, .stm). Nesse caso, o tipo de arquivo é considerado um tipo de link da Web; caso contrário, ele será considerado como um tipo de arquivo. Por exemplo, se o estiver associado à extensão .htm nome de arquivo, esse item será considerado como um link da Web em vez de como um tipo `MIMEType "text/html"` .htm arquivo.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Evitando possíveis barreiras à habilitação de um armazenamento de dados

Alguns armazenamentos de dados não fornecem um serviço Web compatível [com](https://github.com/dewitt/opensearch)OpenSearch, mas ainda podem ser conectados Windows Federated Search. Esses armazenamentos de dados incluem:

-   Índices remotos com métodos de autenticação sem suporte no Windows 7 Federated Search.

    Exemplos incluem autenticação baseada em formulários e outros métodos de autenticação personalizados.

-   Se um armazenamento público de alto valor tiver APIs Web [](https://github.com/dewitt/opensearch)públicas, qualquer pessoa poderá escrever outro serviço Web que seja compatível com OpenSearch e chamar essas APIs nos bastidores.

    Os exemplos incluem a Biblioteca de Médicos e os bancos de dados de pesquisa médica.

-   Armazenamentos de dados corporativos proprietários ou índices e armazenamentos de gerenciamento de conteúdo herdado, para os quais pode ser impossível implementar um front-end.

No entanto, há alternativas que podem evitar barreiras na habilitação de um armazenamento de dados. A seguir estão algumas dessas alternativas:

**Para escrever um serviço Web intermediário quando você não pode modificar o serviço Web para a fonte de dados existente ou o serviço Web fornece uma API personalizada:**

1.  Escreva um serviço Web intermediário que possa aceitar uma Windows 7.
2.  Conexão à fonte de dados e recuperar os resultados da consulta.
3.  Reformate os resultados no formato RSS ou Atom.
4.  Retorne os resultados para o cliente Windows 7.
5.  Observe que, para serviços de dados corporativos e muitos serviços de dados da Internet, talvez seja necessário passar as credenciais do usuário em nome do serviço Web para executar o corte de resultados com base nas permissões do usuário.

**Para usar um mecanismo de pesquisa existente quando não é possível habilitar um armazenamento de dados público:**

1.  Use um mecanismo de pesquisa público que já dá [suporte OpenSearch](https://github.com/dewitt/opensearch) com RSS. Você pode fazer isso fornecendo aos usuários um arquivo .osdx que tem um modelo de URL que restringe os resultados apenas àqueles para seu domínio específico.
2.  Consulte o exemplo a seguir de [uma OpenSearch](https://github.com/dewitt/opensearch) para pesquisar apenas o conteúdo da Ajuda para Windows usando uma consulta em live.com.

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

    

**Para usar um servidor de indexação existente que dá suporte OpenSearch quando você não pode habilitar índices ou armazenamentos de dados corporativos proprietários:**

1.  Selecione um servidor de indexação existente que OpenSearch [para](https://github.com/dewitt/opensearch) indexar seu conteúdo, como o SharePoint Search Server.
2.  Crie um arquivo .osdx que restrinja os resultados do índice SharePoint somente aqueles do servidor usando sua sintaxe KeyWord no modelo de URL.

**Para gravar um armazenamento de dados do lado do cliente se uma solução somente do lado do servidor não funcionar:**

1.  Escreva uma fonte de dados [OpenSearch](https://github.com/dewitt/opensearch) do lado do cliente que fica entre o provedor Windows [OpenSearch](https://github.com/dewitt/opensearch) e a fonte de dados externa.
2.  Use a API de [Interface IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) no SDK do Windows para criar um arquivo .searchconnector-ms configurado adequadamente por meio do qual o Windows Explorer pode chamar sua implementação com os parâmetros de consulta. Sua implementação pode retornar resultados formatados no formato RSS ou Atom. Isso permite que sua implementação forneça a interface do usuário de autenticação personalizada e conecte-se à fonte de dados usando sua API proprietária.

> [!Note]  
> Abrir um arquivo .osdx cria um arquivo .searchconnector-ms (conector de pesquisa) no diretório %userprofile%/searches e coloca um link para ele no diretório %userprofile%/links.

 

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

[Criando um arquivo OpenSearch descrição no Windows Federado](-search-federated-search-osdx-file.md)
</dt> <dt>

[Seguindo as práticas recomendadas Windows pesquisa federada](-search-fedsearch-best.md)
</dt> <dt>

[Implantando conectores de pesquisa Windows Pesquisa Federada](-search-federated-search-deploying.md)
</dt> </dl>

 

 
