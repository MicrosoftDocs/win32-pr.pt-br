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
# <a name="album-art"></a><span data-ttu-id="1e2fd-108">Arte do álbum</span><span class="sxs-lookup"><span data-stu-id="1e2fd-108">Album Art</span></span>

<span data-ttu-id="1e2fd-109">Ao criar uma capa para o Windows Media Player 10 Mobile ou posterior, talvez você queira exibir a arte do álbum relacionada ao item de mídia em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="1e2fd-109">When you create a skin for Windows Media Player 10 Mobile or later, you may want to display album art that relates to the currently playing media item.</span></span> <span data-ttu-id="1e2fd-110">Ao projetar sua capa, você desejará reservar espaço na imagem de plano de fundo para conter a arte do álbum.</span><span class="sxs-lookup"><span data-stu-id="1e2fd-110">When you design your skin, you will want to reserve space in the Background image to contain the album art.</span></span>

<span data-ttu-id="1e2fd-111">A seção de arte do álbum do arquivo de definição de capa deve começar com a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="1e2fd-111">The Album Art section of the skin definition file must begin with the following line:</span></span>


```C++
[ Album Art ]

```



<span data-ttu-id="1e2fd-112">Em seguida, você deve adicionar informações que especificam o local e o tamanho da arte do álbum em sua capa.</span><span class="sxs-lookup"><span data-stu-id="1e2fd-112">You then must add information that specifies the location and size of the album art in your skin.</span></span> <span data-ttu-id="1e2fd-113">Você deve inserir quatro inteiros positivos, separados por vírgulas que definem a esquerda, a parte superior, a largura e a altura da arte do álbum, em pixels, em relação à imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="1e2fd-113">You must enter four positive integers, separated by commas that define the left, top, width, and height of the album art, in pixels, relative to the background image.</span></span> <span data-ttu-id="1e2fd-114">O exemplo a seguir mostra como especificar dimensões:</span><span class="sxs-lookup"><span data-stu-id="1e2fd-114">The following example shows how to specify dimensions:</span></span>


```C++
//  <Location>
//  ----------
   5,37,230,155

```



<span data-ttu-id="1e2fd-115">Se você planeja incluir uma seção de vídeo em sua capa, poderá usar o mesmo tamanho e local para a arte do seu álbum para conservar espaço.</span><span class="sxs-lookup"><span data-stu-id="1e2fd-115">If you plan on including a video section in your skin, you can use the same size and location for your album art to conserve space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e2fd-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e2fd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e2fd-117">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="1e2fd-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




