---
description: Há vários formatos de persistência que a plataforma do Tablet PC gera, que são úteis como blocos de construção para os formatos listados anteriormente. Os formatos a seguir são todos gerados e consumidos usando os métodos Load e Save do objeto Ink.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Blocos de construção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32e6121ddfaabfc860239019ce62df65bdc36c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762968"
---
# <a name="building-blocks"></a>Blocos de construção

Há vários formatos de persistência que a plataforma do Tablet PC gera, que são úteis como blocos de construção para os formatos listados anteriormente. Os formatos a seguir são todos gerados e consumidos usando os métodos [**Load**](/previous-versions/ms569609(v=vs.100)) e [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto [**Ink**](/previous-versions/ms583670(v=vs.100)) .

-   Formato serializado da tinta (ISF): o formato serializado da tinta (ISF) é a representação persistente mais compacta da tinta. Você pode inserir ISF em um formato de documento binário ou movê-lo diretamente para a área de transferência. A tinta armazenada em ISF deve usar o sistema de coordenadas padrão, que é HIMETRIC, com o eixo vertical invertido.
-   ISF codificado em base-64: você pode usar ISF codificado em base 64 para codificar a tinta diretamente em um arquivo de linguagem XML (XML) ou HTML.
-   Reforçada Graphics Interchange Format (GIF): reforçada GIF é um arquivo GIF que contém ISF como metadados inseridos no arquivo. A tinta gerada como um GIF reforçada pode ser exibida em aplicativos que não reconhecem a tinta, e todos os dados de tinta serão mantidos se a tinta retornar a um aplicativo que reconheça a tinta. Esse formato é ideal para transportar conteúdo de tinta em um arquivo HTML. A tinta está disponível para qualquer aplicativo, independentemente se o aplicativo reconhece a tinta.
-   Reforçada GIF codificado em base 64: esse formato é fornecido para os desenvolvedores que desejam codificar a tinta diretamente em um arquivo XML ou HTML e, em seguida, converter o arquivo em uma imagem posteriormente. Você pode usar isso quando desejar que um arquivo XML gerado contenha todas as informações de tinta e seja usado como uma maneira de gerar HTML usando transformações de linguagem de folha de estilos extensível (XSLT).
    > [!Note]  
    > A tecnologia de compactação e descompactação LZW é abcobertamente pela patente dos EUA. 4.558.302 e suas patentes de contraparte relacionadas e estrangeiras (coletivamente, as patentes LZW) pertencentes à Unisys Corporation. A Microsoft Corporation obteve uma licença da Unisys sob as patentes LZW para usar a tecnologia GIF e LZW em determinados produtos da Microsoft. No entanto, essa licença não se estende a desenvolvedores de terceiros que usam produtos de desenvolvimento da Microsoft, como o Microsoft Toolkit e os produtos de desenvolvimento de linguagem, para fornecer leitura/gravação de GIF ou quaisquer outros recursos de LZW em seus próprios produtos. Os desenvolvedores de terceiros precisam fazer sua própria determinação sobre se precisam de uma licença da Unisys para seus produtos.

     

Um aplicativo pode gerar um desses formatos persistentes usando o método [Microsoft. Ink. Stroke. HitTest](/previous-versions/ms828460(v=msdn.10)) ou [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para gerar uma coleção Strokes e:

-   Adicionar esses traços a um novo objeto de [**tinta**](/previous-versions/ms583670(v=vs.100)) usando o método [AddStrokesAtRectangle](/previous-versions/ms569548(v=vs.100)) .
-   Gerando um novo objeto de [**tinta**](/previous-versions/ms583670(v=vs.100)) usando o método [ExtractStrokes](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90)) .

O primeiro traduz o retângulo de seleção para a origem, enquanto o segundo não. Em seguida, o aplicativo usa o método [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto [**Ink**](/previous-versions/ms583670(v=vs.100)) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos sInk e tInk](sink-and-tink-objects.md)
</dt> </dl>

 

 
