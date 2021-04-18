---
title: Arte do álbum
description: Arte do álbum
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Capas móveis do Windows Media Player, arte do álbum
- capas, arte do álbum
- referência para capas, arte do álbum
- arquivos de arte para capas, arte do álbum
- arte do álbum em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788196"
---
# <a name="album-art"></a>Arte do álbum

Ao criar uma capa para o Windows Media Player 10 Mobile ou posterior, talvez você queira exibir a arte do álbum relacionada ao item de mídia em execução no momento. Ao projetar sua capa, você desejará reservar espaço na imagem de plano de fundo para conter a arte do álbum.

A seção de arte do álbum do arquivo de definição de capa deve começar com a seguinte linha:


```C++
[ Album Art ]

```



Em seguida, você deve adicionar informações que especificam o local e o tamanho da arte do álbum em sua capa. Você deve inserir quatro inteiros positivos, separados por vírgulas que definem a esquerda, a parte superior, a largura e a altura da arte do álbum, em pixels, em relação à imagem de plano de fundo. O exemplo a seguir mostra como especificar dimensões:


```C++
//  <Location>
//  ----------
   5,37,230,155

```



Se você planeja incluir uma seção de vídeo em sua capa, poderá usar o mesmo tamanho e local para a arte do seu álbum para conservar espaço.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




