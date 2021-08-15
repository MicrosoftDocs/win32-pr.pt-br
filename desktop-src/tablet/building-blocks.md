---
description: Há vários formatos de persistência gerados pela plataforma tablet pc que são úteis como blocos de construção para os formatos listados anteriormente. Os formatos a seguir são todos gerados e consumidos usando os métodos Carregar e Salvar do objeto Ink.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Blocos de construção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dbf34cc0159bdf2efe9b68255292a8b644ab10e684f44c11fa60d484bd45516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714286"
---
# <a name="building-blocks"></a>Blocos de construção

Há vários formatos de persistência gerados pela plataforma tablet pc que são úteis como blocos de construção para os formatos listados anteriormente. Os formatos a seguir são todos gerados [](/previous-versions/ms569609(v=vs.100)) e consumidos usando os métodos [**Carregar**](/previous-versions/ms583670(v=vs.100)) e Salvar [**do objeto**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) Ink.

-   FORMATO serializado de tinta (ISF): formato ISF (ISF) é a representação persistente mais compacta de tinta. Você pode inserir ISF em um formato de documento binário ou movê-lo diretamente para a Área de Transferência. A tinta armazenada no ISF deve usar o sistema de coordenadas padrão, que é HIMETRIC, com o eixo vertical invertido.
-   ISF codificado em Base 64: você pode usar o ISF codificado em base 64 para codificar tinta diretamente em um arquivo XML ou HTML do linguagem XML.
-   GIF (Graphics Interchange Format): GIF forteizado é um arquivo GIF que contém ISF como metadados inseridos no arquivo. A tinta gerada como um GIF forte pode ser exibida em aplicativos que não reconhecem tinta e todos os dados de tinta são mantidos se a tinta retorna para um aplicativo que reconhece tinta. Esse formato é ideal para transportar conteúdo de tinta dentro de um arquivo HTML. A tinta está disponível para qualquer aplicativo, independentemente de o aplicativo reconhecer tinta.
-   GIF Codificado em Base 64: esse formato é fornecido para desenvolvedores que querem codificar tinta diretamente em um arquivo XML ou HTML e, em seguida, converter o arquivo em uma imagem em um momento posterior. Você pode usar isso quando quiser que um arquivo XML gerado contenha todas as informações de tinta e seja usado como uma maneira de gerar HTML usando XSLT (Extensible Stylesheet Language Transformations).
    > [!Note]  
    > A tecnologia de compactação e descompactação LZW é coberta de forma insauamente pelo Us Patent No. 4.558.302 e suas patentes relacionadas e estrangeiras (coletivamente, as LZW Patents) pertencentes à Unisys Corporation. Microsoft Corporation obteve uma licença da Unisys nas Patentes LZW para usar o GIF e a tecnologia LZW em determinados produtos da Microsoft. Essa licença, no entanto, não se estende a desenvolvedores de terceiros que usam produtos de desenvolvimento da Microsoft, como produtos de desenvolvimento de linguagem e kit de ferramentas da Microsoft, para fornecer leitura/gravação GIF ou qualquer outra funcionalidade LZW em seus próprios produtos. Os desenvolvedores de terceiros precisam fazer sua própria determinação sobre se precisam de uma licença da Unisys para seus produtos.

     

Um aplicativo pode gerar um desses formatos persistentes usando o [método Microsoft.Ink.Stroke.HitTest](/previous-versions/ms828460(v=msdn.10)) ou [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para gerar uma coleção de traços e:

-   Adicionar esses traços a um novo [**objeto Ink**](/previous-versions/ms583670(v=vs.100)) usando o [método AddStrkesAtRectangle.](/previous-versions/ms569548(v=vs.100))
-   Gerando um novo [**objeto Ink**](/previous-versions/ms583670(v=vs.100)) usando o [método ExtractStrkes.](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90))

O primeiro converte o retângulo de seleção para a origem, enquanto o segundo não. Em seguida, o aplicativo usa [**o método Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) do objeto [**Ink.**](/previous-versions/ms583670(v=vs.100))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos sInk e tInk](sink-and-tink-objects.md)
</dt> </dl>

 

 
