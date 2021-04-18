---
description: O suporte do Windows 7 para a Federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch permite que os usuários acessem e interajam com seus dados remotos no Windows Explorer.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Introdução com pesquisa federada no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c1f887ff2bdba279cdd25e4910162dd9263d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501461"
---
# <a name="getting-started-with-federated-search-in-windows"></a>Introdução com pesquisa federada no Windows

O suporte do Windows 7 para a Federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch permite que os usuários acessem e interajam com seus dados remotos no Windows Explorer. Você pode criar um armazenamento de dados baseado na Web que possa ser pesquisado usando a pesquisa federada do Windows e habilitar a integração rica de suas fontes de dados remotas com o Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente do Windows.

Este tópico é organizado da seguinte maneira:

-   [O que é pesquisa federada?](#what-is-federated-search)
-   [Etapas para criar a pesquisa federada](#steps-for-building-federated-search)
-   [Como funciona a pesquisa federada](#how-federated-search-works)
-   [Enviando consultas e retornando resultados da pesquisa em RSS ou Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [Exemplos de pesquisa federada](#federated-search-examples)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-federated-search"></a>O que é pesquisa federada?

O Windows 7 oferece suporte à conexão de fontes externas para o cliente Windows por meio do protocolo [OpenSearch](https://github.com/dewitt/opensearch) . Isso permite que os usuários pesquisem um armazenamento de dados remoto e exibam os resultados de dentro do Windows Explorer. O padrão [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 define formatos de arquivo simples que podem ser usados para descrever como um cliente deve consultar o serviço Web para o armazenamento de dados e como o serviço deve retornar resultados a serem processados pelo cliente. A pesquisa federada do Windows conecta-se aos serviços Web que recebem consultas [OpenSearch](https://github.com/dewitt/opensearch) e retorna resultados no formato XML RSS ou Atom.

A captura de tela a seguir ilustra os resultados da pesquisa obtidos após a pesquisa remota de um site do SharePoint.

![captura de tela que mostra os resultados da pesquisa de um site do SharePoint, conforme exibido no Windows Explorer](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>Etapas para criar a pesquisa federada

Para criar uma pesquisa federada, execute as seguintes etapas:

1.  Habilite seu armazenamento de dados para ser pesquisado no Windows Explorer, fornecendo um serviço Web compatível com [OpenSearch](https://github.com/dewitt/opensearch)que pode retornar resultados no formato RSS ou Atom.
2.  Crie um arquivo de descrição OpenSearch (. osdx) que descreve como se conectar ao serviço Web e como mapear quaisquer elementos personalizados em seu XML RSS ou Atom.
3.  Implante os conectores de pesquisa em computadores cliente com Windows com um arquivo. osdx.

O diagrama a seguir ilustra as etapas para criar a pesquisa federada.

![diagrama do processo de criação de pesquisa federada](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>Como funciona a pesquisa federada

A comunicação entre o Windows Explorer e o serviço Web do [OpenSearch](https://github.com/dewitt/opensearch) é executada por meio da camada de dados do Windows. A camada de dados do Windows pode se comunicar com diferentes tipos de armazenamentos de dados por meio de provedores da Windows Store. Cada provedor é especialista em comunicação com armazenamentos de dados que dão suporte a um protocolo específico e têm recursos específicos. Por exemplo, a ilustração a seguir mostra como o provedor de [OpenSearch](https://github.com/dewitt/opensearch) se comunica com armazenamentos de dados que fornecem um serviço Web que dá suporte ao padrão [OpenSearch](https://github.com/dewitt/opensearch) .

![diagrama mostrando a comunicação do Windows Explorer no cliente por meio do armazenamento de dados OpenSearch no servidor remoto](images/windowssearchfederationfunctionality.png)

Para habilitar seu armazenamento de dados para dar suporte à pesquisa federada no Windows 7, você deve executar várias tarefas. A tabela a seguir lista as tarefas para habilitar o armazenamento de dados, o que é necessário para realizar cada tarefa e onde encontrar a documentação.



| Tarefa                                                                                                     | Requisito                                                                                                                                                                                            | Documentação                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Habilite o armazenamento de dados a ser pesquisado pelo Windows Explorer.<br/>                                    | Crie um serviço Web compatível com OpenSearch.<br/> Crie um arquivo de descrição de OpenSearch (. osdx).<br/>                                                                                       | [Conectando seu serviço Web na pesquisa federada do Windows](-search-federated-search-web-service.md)<br/> [Habilitando seu armazenamento de dados na pesquisa federada do Windows](-search-federated-search-data-store.md)<br/> |
| Implante ativamente seu serviço Web para usuários em uma empresa.<br/>                               | Forneça um arquivo. osdx para os usuários, copie-o localmente e torne-o acessível ao usuário por meio de um atalho.<br/>                                                                                     | [Implantando conectores de pesquisa na pesquisa federada do Windows](-search-federated-search-deploying.md)<br/>                                                                                                              |
| Enumere os resultados da pesquisa no Windows Explorer em resposta a uma consulta.<br/>                          | Implemente um serviço Web que aceita uma cadeia de caracteres de consulta e retorna resultados em formato RSS ou Atom.<br/>                                                                                              | [Conectando seu serviço Web na pesquisa federada do Windows](-search-federated-search-web-service.md)<br/>                                                                                                            |
| Permita que os usuários adicionem seu armazenamento de dados ao seu Windows Explorer.<br/>                                | Crie um arquivo. osdx e forneça-o aos seus usuários.<br/>                                                                                                                                           | [Habilitando seu armazenamento de dados na pesquisa federada do Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Exiba seus itens como itens do tipo arquivo no Windows Explorer.<br/>                                    | Retornar uma URL para o arquivo ou o fluxo de conteúdo usando o **compartimento** ou **mídia:** elementos de conteúdo<br/> Forneça uma extensão de nome de arquivo ou um tipo MIME que o computador cliente reconhece.<br/> | [Habilitando seu armazenamento de dados na pesquisa federada do Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Exibir propriedades personalizadas no Windows Explorer, além daquelas definidas em padrões RSS ou Atom.<br/> | Forneça metadados adicionais usando outro namespace XML na saída de RSS/Atom.<br/> Adicione um mapa de propriedades ao seu arquivo. osdx.<br/>                                                       | [Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Personalize as propriedades que são exibidas para seus itens no Windows Explorer.<br/>               | Adicione mapeamentos de PropList ao seu arquivo. osdx.<br/>                                                                                                                                                   | [Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Exiba um modo de exibição de página da Web personalizado de seus itens no painel de visualização.<br/>                              | Retornar valores de link e compartimento distintos.<br/> Mapeie um valor de URL para a propriedade de shell do Windows **System. WebPreviewUrl** .<br/>                                                               | [Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Exiba um botão de barra de comandos no Windows Explorer que reverte a consulta para seu site.<br/>   | Forneça um `Url format="text/html"` modelo no arquivo. osdx.<br/>                                                                                                                              | [Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Enviando consultas e retornando resultados da pesquisa em RSS ou Atom

Quando o usuário digita um termo na caixa de pesquisa no canto superior direito do Windows Explorer, a consulta é enviada ao provedor de [OpenSearch](https://github.com/dewitt/opensearch) , que envia a consulta para o armazenamento de dados remoto. O serviço Web remoto responde à consulta, fornecendo resultados em um documento XML, normalmente chamado de feed, em um dos dois formatos com suporte (RSS ou Atom). Cada item de resultado no feed inclui elementos filho XML para representar ou descrever metadados de item, como o título, a URL, a descrição, a imagem em miniatura e assim por diante. O provedor de [OpenSearch](https://github.com/dewitt/opensearch) é responsável por mapear os valores do elemento XML para as propriedades do sistema do shell do Windows que podem ser usadas por aplicativos do Windows.

## <a name="federated-search-examples"></a>Exemplos de pesquisa federada

O arquivo de descrição OpenSearch de exemplo a seguir (. osdx) consiste em `ShortName` `Url` elementos e, que são os elementos filho mínimos necessários para conectar um armazenamento de dados externo ao cliente Windows por meio do protocolo OpenSearch.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



O exemplo a seguir ilustra como tornar um armazenamento de dados habilitado para Web pesquisável em formato RSS e como especificar que um item de pesquisa deve ser retornado:


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



O exemplo a seguir ilustra como mapear Propriedades para propriedades padrão do sistema para que os itens exibidos sejam classificados e agrupados:


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



O exemplo a seguir ilustra como adicionar uma exibição de imagem em miniatura a cada item no Windows Explorer:


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>Recursos adicionais

Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Conectando seu serviço Web na pesquisa federada do Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitando seu armazenamento de dados na pesquisa federada do Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Seguindo as práticas recomendadas na pesquisa federada do Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implantando conectores de pesquisa na pesquisa federada do Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 




