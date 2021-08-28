---
title: Posicionar e mover retângulos de vídeo no espaço de composição
description: Posicionando e movendo retângulos de vídeo no espaço de composição
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563509e062335f496f001d8d61dae8eecfe2cff998da6e63320a7c95c347438c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583597"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Posicionar e mover retângulos de vídeo no espaço de composição

Quando a VMR combina vários fluxos de entrada, ela posiciona cada fluxo dentro de um retângulo normalizado, chamado de "espaço de composição". No espaço de composição, as coordenadas (0,0, 0,0) a (1.0, 1.0) formam o retângulo de vídeo visível. Todas as coordenadas que ficam fora desse retângulo são recortados.

Um aplicativo pode executar efeitos especiais ao mover, alongar e reduzir o vídeo de um fluxo de entrada, alterando o retângulo de destino no espaço de composição para esse fluxo. Se o retângulo especificado for um tamanho diferente do retângulo de vídeo nativo, o vídeo nativo será reduzido ou estendido para se ajustar. O retângulo de destino é especificado chamando o [**método IVMRMixerControl::SetOutputRect.**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs)

Por exemplo, suponha que o fluxo 0 (que corresponde ao pino 0) contenha o fluxo de vídeo principal e o fluxo 1 (que corresponde à pino 1) contenha um vídeo secundário. O fluxo 1 pode ser posicionado completamente fora da tela especificando um retângulo normalizado de { -1.0f, 0.0f, 0.0f, 1.0f }. O fluxo 1 pode então ser movido para a área visível modificando os lados esquerdo e direito do retângulo em chamadas sucessivas para **SetOutputRect**:



| Rótulo | Valor |
|--------|-----------------------------|
| Tempo   | Retângulo                   |
| t + 0  | { -1.0f, 0.0f, 0.0f, 1.0f } |
| t + 1  | { -0.9f, 0.0f, 0.1f, 1.0f } |
| t + 2  | { -0.8f, 0.0f, 0.2f, 1.0f } |
| ...    | ...                         |
| t + 10 | { 0.0f, 0.0f, 1.0f, 1.0f }  |



 

![movendo um fluxo de vídeo no espaço de composição](images/composition-space.png)

No momento t+10, o vídeo do fluxo 1 fica completamente visível. Neste exemplo, o tamanho nativo do fluxo 1 foi mantido durante a movimentação. Você também pode alongar ou reduzir o retângulo para produzir efeitos interessantes. Você também pode inverter o vídeo verticalmente, especificando um valor maior para a parte superior que a parte inferior ou espelhar o vídeo horizontalmente, especificando um valor maior para a esquerda do que a direita.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de combinação de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



