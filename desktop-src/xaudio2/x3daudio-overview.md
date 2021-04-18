---
description: X3DAudio é uma API usada com XAudio2 para posicionar o som no espaço 3D para criar a ilusão de som proveniente de um ponto no espaço em relação à posição da câmera.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: Visão geral do X3DAudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff509b16556ee1932d2a2543ad5008ddcbaa5b92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755513"
---
# <a name="x3daudio-overview"></a>Visão geral do X3DAudio

X3DAudio é uma API usada com [XAudio2](programming-guide.md) para posicionar o som no espaço 3D para criar a ilusão de som proveniente de um ponto no espaço em relação à posição da câmera. Em particular, os títulos que apresentam cenas 3D desejarão usar o X3DAudio. Sons que não exigem posicionamento 3D, como trilhas sonoras ou sons de ambiente não posicionados, podem ignorar completamente o X3DAudio.

## <a name="listeners-and-emitters"></a>Ouvintes e emissores

Para gerenciar sons em espaço 3D, o X3DAudio emprega os conceitos de *ouvintes* e *emissores*. Ouvintes e emissores representam a posição de qualquer coisa que esteja ouvindo sons 3D e o ponto do qual os sons se originam.

-   Um ouvinte é definido como um ponto no espaço e uma orientação. É a posição na qual o som é *ouvido*. A posição e a orientação do ouvinte geralmente são as mesmas que a posição e a orientação da câmera. Isso é verdadeiro se um título usa uma exibição de perspectiva da primeira pessoa ou da terceira pessoa. A posição do ouvinte é expressa em coordenadas mundiais. É importante observar que é a posição do ouvinte *relativa* a um emissor que determina como calcular os volumes de alto-falantes finais.
-   Um emissor é definido como um (ou mais) pontos no espaço do qual um som é *originado*. A posição do emissor pode estar em qualquer lugar no espaço 3D. Como um ouvinte, a posição de um emissor é expressa em coordenadas mundiais. É a posição do emissor *relativa* ao ouvinte que determina como os volumes de alto-falante finais são calculados.
-   X3DAudio usa coordenadas da mão esquerda. Para usar com as coordenadas da mão direita, os desenvolvedores precisam negar o elemento. z dos membros OrientTop, OrientFront, position e Velocity de X3DAUDIO \_ Listener e X3DAUDIO \_ emissor.

Além da posição, os ouvintes e os emissores podem incluir a velocidade. Ao contrário de um mecanismo de renderização 3D, o X3DAudio usa apenas a velocidade para calcular efeitos de Doppler (não é usado para calcular a posição).

Para obter mais detalhes sobre ouvintes e emissores, consulte os tópicos de referência de estrutura do [**\_ emissor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) do [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e X3DAUDIO.

## <a name="using-x3daudio-with-xaudio2"></a>Usando X3DAudio com XAudio2

Para toda a interação entre X3DAudio e XAudio2, use as seguintes funções do X3DAudio.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Chame a função [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) para inicializar o X3DAudio. Normalmente, você só precisa chamar **X3DAudioInitialize** uma vez no tempo de vida de um jogo, a menos que a configuração do alto-falante seja alterada.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Depois de inicializar o X3DAudio, você pode determinar o volume e outros valores para um determinado som passando o emissor do som e o ouvinte para a função [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) . Os valores calculados por **X3DAudioCalculate** podem ser aplicados a vozes XAudio2 ou efeitos conforme apropriado para os sinalizadores passados para a função. Você pode aplicar valores de volume e de densidade calculados por X3DAudio a uma voz com os métodos [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) . Outros valores calculados por X3DAudio precisarão ser aplicados a um [**efeito de reverberação**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) usando o método [**IXAudio2Voice:: seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) .

Para obter um exemplo passo a passo de como usar X3DAudio com XAudio2, consulte [como integrar o X3DAudio com XAudio](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
