---
description: Este tópico lista as práticas recomendadas por meio das quais você pode criar um armazenamento de dados baseado na Web que pode ser pesquisado usando a pesquisa federada do Windows e integra suas fontes de dados remotas ao Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente do Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Seguindo as práticas recomendadas na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090084"
---
# <a name="following-best-practices-in-windows-federated-search"></a>Seguindo as práticas recomendadas na pesquisa federada do Windows

Este tópico lista as práticas recomendadas por meio das quais você pode criar um armazenamento de dados baseado na Web que pode ser pesquisado usando a pesquisa federada do Windows e integra suas fontes de dados remotas ao Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente do Windows.

Este tópico é organizado da seguinte maneira:

-   [Práticas recomendadas para a pesquisa federada do Windows](#best-practices-for-windows-federated-search)
-   [Práticas recomendadas para a criação de saída de RSS](#best-practices-for-creating-rss-output)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Práticas recomendadas para a pesquisa federada do Windows

As práticas recomendadas para trabalhar com o [OpenSearch](https://github.com/dewitt/opensearch) no Windows 7 são as seguintes:

-   Dê suporte aos parâmetros *{startIndex}* e *{Count}* e certifique-se de sempre retornar o número de itens solicitados, a menos que você esteja retornando o último dos resultados.
-   Se você souber a extensão de nome de arquivo, mapeie-a para a propriedade de shell [System. FileExtension](../properties/props-system-fileextension.md) do Windows. O uso de extensões de nome de arquivo é uma maneira melhor de identificar um tipo de arquivo do que o tipo MIME.
-   Verifique se o tipo MIME ou a extensão de nome de arquivo que você especificar no RSS corresponde ao nome do arquivo e ao tipo MIME retornado no cabeçalho HTTP pelo servidor Web que hospeda o item quando o conteúdo do item é solicitado.
-   Se você estiver retornando itens de arquivo, retorne um tamanho de arquivo sempre que possível. Isso garante que a caixa de diálogo progresso do download seja precisa.
-   Verifique se as solicitações de itens além do final do conjunto de resultados não retornam nenhum resultado.
    > [!Note]  
    > Não repita os resultados.

     

-   Não coloque marcas HTML onde elas não pertençam. De acordo com a especificação de RSS, elas são válidas no campo Descrição, mas não no campo título.
-   Não crie compartimentos para itens da página da Web. Por exemplo, se você criar um compartimento e mapear uma extensão de nome de arquivo de. aspx, o arquivo será baixado pelo Windows Explorer para o cache da Internet e executado a partir daí. Os navegadores da Web não manipulam o tipo de arquivo. aspx. O usuário receberia uma caixa de diálogo **abrir com** , ou o arquivo pode ser aberto por um aplicativo como Microsoft Visual Studio. Evite isso retornando um elemento link somente para páginas da Web.
-   Forneça uma URL de rolagem da Web no arquivo. osdx usando um modelo de URL com `format="text\html"` .
-   Forneça uma URL para a pasta pai, o contêiner ou a página da Web mapeando um valor de URL de elemento personalizado para a propriedade de shell do Windows [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) .

## <a name="best-practices-for-creating-rss-output"></a>Práticas recomendadas para a criação de saída de RSS

As práticas recomendadas para a criação de saída RSS são as seguintes:

-   Cada item deve retornar uma URL `link` ou um `enclosure` valor (ou equivalente, como `media:content` )
-   Não inclua marcas de formatação HTML no atributo **title** , ou essas marcas aparecerão no título e serão exibidas no Windows Explorer.
-   Para o elemento **Description** :
    -   Mostrar informações suficientes para que o usuário saiba por que esse resultado pode ser relevante.
    -   Não inclua formatação HTML. O provedor de [OpenSearch](https://github.com/dewitt/opensearch) remove a formatação, o que pode resultar em menos resultados desejáveis para sua descrição.
    -   Não inclua metadados que já são fornecidos em outros elementos, como nome do arquivo de compartimento, tamanho, data de modificação e assim por diante, porque o Windows Explorer já exibe os metadados. Exibi-lo no elemento **Description** seria redundante.
-   Para URLs de conteúdo ou compartimento:
    -   Especifique o atributo de tipo como um tipo MIME válido.
    -   Especifique o tamanho do arquivo em bytes.
-   Se você estiver implementando a saída de RSS no .NET usando `DateTime` , teste o feed no Microsoft Internet Explorer para ver se ele é válido antes de implantá-lo no Windows Explorer.

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

[Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Implantando conectores de pesquisa na pesquisa federada do Windows](-search-federated-search-deploying.md)
</dt> <dt>

[Estendendo o índice](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
