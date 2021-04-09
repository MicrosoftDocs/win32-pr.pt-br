---
title: Referência do metarquivo do Windows Media
description: Referência do metarquivo do Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Metaarquivos do Windows Media, referência
- metaarquivos, referência
- referência para os metaarquivos do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005482"
---
# <a name="windows-media-metafile-reference"></a>Referência do metarquivo do Windows Media

Esta referência documenta elementos e extensões de nome de arquivo para os metaarquivos de mídia do Windows. A referência é dividida nas seções a seguir.



| Seção                                                                                    | Descrição                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Referência de elementos de metarquivo do Windows Media](windows-media-metafile-elements-reference.md) | Documenta elementos de metarquivo, incluindo definições, atributos e seus valores, e condições especiais relacionadas a cada elemento. |
| [Extensões de nome de arquivo](file-name-extensions.md)                                           | Documenta as extensões de nome de arquivo do metarquivo com regras e diretrizes sobre seu uso.                                                  |



 

Os metaarquivos de mídia do Windows são arquivos de texto que fornecem informações sobre um fluxo de arquivos e sua apresentação. Os metaarquivos são baseados na sintaxe de linguagem XML (XML) e são compostos de vários elementos do tipo XML com suas marcas e atributos. Cada elemento define uma configuração ou ação para mídia de streaming.

Há dois conjuntos de marcas de elemento disponíveis para os metaarquivos. Os metaarquivos do lado do cliente têm um conjunto de elementos e os metaarquivos do lado do servidor têm outro conjunto de elementos.

Se uma marca de elemento não tiver elementos filho (aqueles que modificam ou estiverem contidos em outro elemento), um único caractere de barra (/) poderá ser usado no final da marca de abertura no lugar de uma marca de fechamento. Se os elementos filho não aparecerem entre a marca de abertura e de fechamento de um elemento, eles não serão elementos filho desse elemento e serão ignorados ou causarão um erro na sintaxe do metarquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre os metaarquivos de mídia do Windows**](about-windows-media-metafiles.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Metaarquivos do Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




