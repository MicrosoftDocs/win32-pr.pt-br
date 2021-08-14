---
description: X3DAudio é uma API usada com XAudio2 para posicionar o som no espaço 3D para criar a ilusão de som proveniente de um ponto no espaço em relação à posição da câmera.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: Visão geral do X3DAudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb39239027bf8c7387fbe4cb25b80cef88bb241b74facf0b7bd7ee35c77965b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962545"
---
# <a name="x3daudio-overview"></a>Visão geral do X3DAudio

X3DAudio é uma API usada com [XAudio2](programming-guide.md) para posicionar o som no espaço 3D para criar a ilusão de som proveniente de um ponto no espaço em relação à posição da câmera. Em particular, os títulos que apresentam cenas 3D vão querer usar X3DAudio. Sons que não exigem posicionamento 3D, como trilhas ou sons de ambiente não posicionados, podem ignorar completamente o X3DAudio.

## <a name="listeners-and-emitters"></a>Ouvintes e emissores

Para gerenciar sons no espaço 3D, o X3DAudio emprega os *conceitos* de ouvintes *e emissores*. Ouvintes e emissores representam a posição do que está escutando sons 3D e o ponto do qual esses sons se originam.

-   Um ouvinte é definido como um ponto no espaço e uma orientação. É a posição na qual o som é *ouvido.* A posição e a orientação do ouvinte geralmente são as mesmas que a posição e a orientação da câmera. Isso é verdadeiro se um título usa uma exibição de perspectiva de primeira pessoa ou de terceira pessoa. A posição do ouvinte é expressa em coordenadas de mundo. É importante observar que é a posição  do ouvinte em relação a um emissor que determina como calcular os volumes finais do locutor.
-   Um emissor é definido como um (ou mais) pontos no espaço do qual um som *se origina.* A posição do emissor pode estar em qualquer lugar no espaço 3D. Como um ouvinte, a posição de um emissor é expressa em coordenadas de mundo. É a posição do emissor em relação *ao* ouvinte que determina como os volumes finais do locutor são calculados.
-   O X3DAudio usa coordenadas à esquerda. Para usar com coordenadas de direita, os desenvolvedores precisam negar o elemento .z dos membros OrientTop, OrientFront, Position e Velocity de X3DAUDIO LISTENER e \_ X3DAUDIO \_ EMITTER.

Além da posição, ouvintes e emissores podem incluir velocidade. Ao contrário de um mecanismo de renderização 3D, o X3DAudio usa apenas a velocidade para calcular efeitos do Doppler (ele não é usado para calcular a posição).

Para obter mais detalhes sobre ouvintes e emissores, consulte os tópicos de referência da estrutura [**EMITTER X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO. \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

## <a name="using-x3daudio-with-xaudio2"></a>Usando X3DAudio com XAudio2

Para toda a interação entre X3DAudio e XAudio2, use as funções X3DAudio a seguir.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Chame a [**função X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) para inicializar X3DAudio. Normalmente, você só precisa chamar **X3DAudioInitialize** uma vez no tempo de vida de um jogo, a menos que a configuração do locutor seja alterada.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Depois de inicializar x3DAudio, você pode determinar o volume e outros valores para um determinado som passando o emitter do som e o ouvinte para a [**função X3DAudioCalculate.**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) Os valores calculados por **X3DAudioCalculate** podem ser aplicados a vozes ou efeitos XAudio2 conforme apropriado para os sinalizadores passados para a função. Você pode aplicar valores de volume e tom calculados por X3DAudio a uma voz com os métodos [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice::SetFrequencyRatio.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) Outros valores calculados por X3DAudio precisarão ser aplicados a um efeito [**reverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) usando o método [**IXAudio2Voice::SetEffectParameters.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)

Para ver um exemplo passo a passo de como usar X3DAudio com XAudio2, consulte Como [integrar o X3DAudio ao XAudio](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
