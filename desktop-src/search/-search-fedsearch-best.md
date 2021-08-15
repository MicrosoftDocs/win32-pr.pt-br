---
description: este tópico lista as práticas recomendadas por meio das quais você pode criar um armazenamento de dados baseado na web que pode ser pesquisado usando Windows pesquisa federada e integra suas fontes de dados remotas com o Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: seguindo as práticas recomendadas em Windows pesquisa federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e52d2b74f245e4ec76550cbf0a1c56b63db0a8ca6afcf9e8b736f3c7b39a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463084"
---
# <a name="following-best-practices-in-windows-federated-search"></a>seguindo as práticas recomendadas em Windows pesquisa federada

este tópico lista as práticas recomendadas por meio das quais você pode criar um armazenamento de dados baseado na web que pode ser pesquisado usando Windows pesquisa federada e integra suas fontes de dados remotas com o Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente Windows.

Este tópico é organizado da seguinte maneira:

-   [práticas recomendadas para Windows pesquisa federada](#best-practices-for-windows-federated-search)
-   [Práticas recomendadas para a criação de saída de RSS](#best-practices-for-creating-rss-output)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>práticas recomendadas para Windows pesquisa federada

as práticas recomendadas para trabalhar com [OpenSearch](https://github.com/dewitt/opensearch) no Windows 7 são as seguintes:

-   Dê suporte aos parâmetros *{startIndex}* e *{Count}* e certifique-se de sempre retornar o número de itens solicitados, a menos que você esteja retornando o último dos resultados.
-   se você souber a extensão de nome de arquivo, mapeie-a para a propriedade [System. FileExtension](../properties/props-system-fileextension.md) Windows Shell. O uso de extensões de nome de arquivo é uma maneira melhor de identificar um tipo de arquivo do que o tipo MIME.
-   Verifique se o tipo MIME ou a extensão de nome de arquivo que você especificar no RSS corresponde ao nome do arquivo e ao tipo MIME retornado no cabeçalho HTTP pelo servidor Web que hospeda o item quando o conteúdo do item é solicitado.
-   Se você estiver retornando itens de arquivo, retorne um tamanho de arquivo sempre que possível. Isso garante que a caixa de diálogo progresso do download seja precisa.
-   Verifique se as solicitações de itens além do final do conjunto de resultados não retornam nenhum resultado.
    > [!Note]  
    > Não repita os resultados.

     

-   Não coloque marcas HTML onde elas não pertençam. De acordo com a especificação de RSS, elas são válidas no campo Descrição, mas não no campo título.
-   Não crie compartimentos para itens da página da Web. por exemplo, se você criar um compartimento e mapear uma extensão de nome de arquivo de. aspx, o arquivo será baixado pelo Windows Explorer para o cache da Internet e executado a partir daí. Os navegadores da Web não manipulam o tipo de arquivo. aspx. O usuário receberia uma caixa de diálogo **abrir com** , ou o arquivo pode ser aberto por um aplicativo como Microsoft Visual Studio. Evite isso retornando um elemento link somente para páginas da Web.
-   Forneça uma URL de rolagem da Web no arquivo. osdx usando um modelo de URL com `format="text\html"` .
-   forneça uma url para a pasta pai, o contêiner ou a página da web mapeando um valor de URL de elemento personalizado para a propriedade de Shell [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows.

## <a name="best-practices-for-creating-rss-output"></a>Práticas recomendadas para a criação de saída de RSS

As práticas recomendadas para a criação de saída RSS são as seguintes:

-   Cada item deve retornar uma URL `link` ou um `enclosure` valor (ou equivalente, como `media:content` )
-   não inclua marcas de formatação HTML no atributo **title** ou essas marcas aparecerão no título e serão exibidas no Windows Explorer.
-   Para o elemento **Description** :
    -   Mostrar informações suficientes para que o usuário saiba por que esse resultado pode ser relevante.
    -   Não inclua formatação HTML. o provedor de [OpenSearch](https://github.com/dewitt/opensearch) remove a formatação, o que pode resultar em menos que os resultados desejáveis para sua descrição.
    -   não inclua metadados que já são fornecidos em outros elementos, como nome do arquivo de compartimento, tamanho, data de modificação e assim por diante, porque Windows Explorer já exibe os metadados. Exibi-lo no elemento **Description** seria redundante.
-   Para URLs de conteúdo ou compartimento:
    -   Especifique o atributo de tipo como um tipo MIME válido.
    -   Especifique o tamanho do arquivo em bytes.
-   se você estiver implementando a saída de RSS no .net usando `DateTime` , teste o feed no Microsoft Internet Explorer para ver se ele é válido antes de implantá-lo no Windows Explorer.

## <a name="additional-resources"></a>Recursos adicionais

para obter informações adicionais sobre como implementar a federação de pesquisa em armazenamentos de dados remotos usando OpenSearch tecnologias no Windows 7 e posterior, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introdução com pesquisa federada no Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[conectando seu serviço Web no Windows pesquisa federada](-search-federated-search-web-service.md)
</dt> <dt>

[habilitando seu armazenamento de dados no Windows pesquisa federada](-search-federated-search-data-store.md)
</dt> <dt>

[criando um arquivo de descrição de OpenSearch no Windows pesquisa federada](-search-federated-search-osdx-file.md)
</dt> <dt>

[implantando conectores de pesquisa no Windows pesquisa federada](-search-federated-search-deploying.md)
</dt> <dt>

[Estendendo o índice](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
