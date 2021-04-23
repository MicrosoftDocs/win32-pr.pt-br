---
title: Posicionar e mover os retângulos de vídeo no espaço de composição
description: Posicionando e movendo os retângulos de vídeo no espaço de composição
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909624"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Posicionar e mover os retângulos de vídeo no espaço de composição

Quando o VMR combina vários fluxos de entrada, ele posiciona cada fluxo dentro de um retângulo normalizado, chamado "espaço de composição". No espaço de composição, as coordenadas (0,0, 0,0) a (1,0, 1,0) formam o retângulo de vídeo visível. Todas as coordenadas que estão fora deste retângulo são recortadas.

Um aplicativo pode executar efeitos especiais com a movimentação, o alongamento e a redução do vídeo de um fluxo de entrada, alterando o retângulo de destino no espaço de composição para esse fluxo. Se o retângulo especificado for um tamanho diferente do retângulo de vídeo nativo, o vídeo nativo será reduzido ou ampliado para caber. O retângulo de destino é especificado chamando o método [**IVMRMixerControl:: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .

Por exemplo, suponha que o fluxo 0 (que corresponde ao pino 0) contenha o fluxo de vídeo principal, e o fluxo 1 (que corresponde ao pino 1) contenha um vídeo secundário. O fluxo 1 pode ser posicionado completamente fora da tela, especificando um retângulo normalizado de {-1,0 f, 0,0 f, 0,0 f, 1,0 f}. O fluxo 1 pode então ser movido para a área visível modificando os lados esquerdo e direito do retângulo sobre as chamadas sucessivas para **SetOutputRect**:



| Label | Valor |
|--------|-----------------------------|
| Hora   | Retângulo                   |
| t + 0  | {-1,0 f, 0,0 f, 0,0 f, 1,0 f} |
| t + 1  | {-0,9 f, 0,0 f, 0,1 f, 1,0 f} |
| t + 2  | {-0,8 f, 0,0 f, 0,2 f, 1,0 f} |
| ...    | ...                         |
| t + 10 | {0,0 f, 0,0 f, 1,0 f, 1,0 f}  |



 

![movendo um fluxo de vídeo no espaço de composição](images/composition-space.png)

No tempo t + 10, o vídeo do fluxo 1 fica completamente visível. Neste exemplo, o tamanho nativo do fluxo 1 foi mantido enquanto estava sendo movido. Você também pode alongar ou reduzir o retângulo para produzir efeitos interessantes. Você também pode virar o vídeo verticalmente, especificando um valor maior para o topo da parte inferior ou espelhar o vídeo horizontalmente, especificando um valor maior para o lado esquerdo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de mixagem do VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



