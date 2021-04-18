---
description: Seu app pode usar o buffer de estêncil para compor imagens 2D ou 3D em uma cena 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composição (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807157"
---
# <a name="compositing-direct3d-9"></a>Composição (Direct3D 9)

Seu app pode usar o buffer de estêncil para compor imagens 2D ou 3D em uma cena 3D. Uma máscara no buffer de estêncil é usada para ocultar uma área da superfície de destino de renderização. Informações armazenadas 2D, como texto ou bitmaps, podem então ser escritas na área obstruída. Como alternativa, seu app pode renderizar objetos primitivos 3D adicionais para a região mascarada por estêncil da superfície do destino de renderização. Ele pode até mesmo renderizar uma cena inteira.

Jogos geralmente são compostos por diversas cenas 3D juntas. Por exemplo, jogos de direção normalmente exibem um espelho retrovisor. O espelho contém o modo de exibição da cena 3D atrás do condutor. Ele é essencialmente uma segunda cena 3D composta pela visão frontal do condutor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Técnicas de buffer de estêncil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



