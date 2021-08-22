---
description: Cada vez mais, aplicativos empregam efeitos especiais que são comumente usados em filmes e vídeo, como desintegração, passagem de dedo e desvanecimento.
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: Dessolucionar, esmaecer e passar o dedo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d6df834ad19fa4b00b6e4706d0884227bc4af33c6a25ec09cba14757e1248
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607456"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a>Dessolucionar, esmaecer e passar o dedo (Direct3D 9)

Cada vez mais, aplicativos empregam efeitos especiais que são comumente usados em filmes e vídeo, como desintegração, passagem de dedo e desvanecimento.

Em uma desintegração, uma imagem é gradualmente substituída por outra em uma sequência de quadros suavizada. Embora o Direct3D forneça métodos de utilizar várias mesclagens de textura para conseguir o mesmo efeito, os aplicativos que utilizam o buffer de estêncil para desintegrações podem usar recursos de mesclagem de textura para outros efeitos enquanto eles fazem uma desintegração.

Quando seu aplicativo executa uma desintegração, ele deve renderizar duas imagens diferentes. Ele usa o buffer de estêncil para controlar quais pixels de cada imagem são desenhadas na superfície de destino de renderização. Você pode definir uma série de máscaras de estêncil e copiá-las para o buffer de estêncil em quadros sucessivos. Como alternativa, você pode definir uma máscara de estêncil de base para o primeiro quadro e alterá-la de forma incremental.

No início da desintegração, seu aplicativo define a função de estêncil e máscara de estêncil para que a maioria dos pixels da imagem inicial passem no teste de estêncil. A maioria dos pixels da imagem final deve falhar no teste de estêncil. Em quadros sucessivos, a máscara de estêncil é atualizada para que cada vez menos pixels da imagem inicial passem no teste. À medida que os quadros progridem, cada vez menos pixels da imagem final falham no teste. Dessa forma, seu aplicativo pode executar uma desintegração usando qualquer padrão arbitrário de desintegração.

O desvanecimento para dentro ou para fora é um caso especial de desintegração. Ao desvanecer para dentro, o buffer de estêncil é usado para desintegrar a partir de uma imagem preta ou branca para uma renderização de uma cena 3D. O desvanecimento para fora é o oposto, seu aplicativo é iniciado com uma renderização de uma cena 3D e se desintegra em preto e branco. O desvanecimento pode ser feito usando qualquer padrão arbitrário que você deseja empregar.

Os aplicativos Direct3D usam uma técnica semelhante para as passagens de dedo. Por exemplo, quando um aplicativo realiza uma passagem de dedo da esquerda para a direita, a imagem final parece deslizar gradualmente na parte superior da imagem inicial da esquerda para a direita. Assim como em uma desintegração, você deve definir uma série de máscaras de estêncil que são carregadas no buffer de estêncil em quadros sucessivos, ou modificar sucessivamente a máscara de estêncil inicial. As máscaras de estêncil são usadas para desativar a gravação de pixels da imagem inicial e para habilitar a gravação de pixels da imagem final.

Uma passagem de dedo é um pouco mais complexa do que uma desintegração em que seu aplicativo deve ler os pixels da imagem final na ordem inversa da passagem do dedo. Ou seja, se a passagem do dedo acontecer da esquerda para a direita, seu aplicativo deverá ler pixels da imagem final da direita para a esquerda.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Técnicas de buffer de estêncil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



