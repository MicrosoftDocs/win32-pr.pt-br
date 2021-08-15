---
title: Implementando renderização
description: Implementando renderização
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- visualizações, eventos temporados
- visualizações personalizadas, eventos com tempo
- visualizações, função Renderizar
- visualizações personalizadas, função Renderizar
- visualizações, função RenderWindow
- visualizações personalizadas, função RenderWindow
- Função de renderização, parâmetros
- Função RenderWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af44299c8a8e34c8f63844dc7d2c143f1d85e0b622c50dd246ea12571d94af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390686"
---
# <a name="implementing-render"></a>Implementando renderização

A maneira mais fácil de pensar na programação de visualização é que você está criando um manipulador para um evento com tempo. Em intervalos específicos, Windows Media Player um instantâneo dos dados de áudio que ele está tocando e fornece os dados de instantâneo para a visualização carregada no momento. Isso é semelhante à programação controlada por eventos e faz parte do modelo de programação do Microsoft Windows. Escreva o código e aguarde até que ele seja chamado por um evento específico.

Se seu código for uma implementação da função [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) para renderização no modo sem janela, ele receberá os seguintes parâmetros:

*TimedLevel*

Essa é uma estrutura que define os dados de áudio que seu código analisará. A estrutura é composta por duas matrizes. A primeira matriz é baseada em informações de frequência e contém um instantâneo do espectro de áudio dividido em 1024 partes. Cada célula da matriz contém um valor de 0 a 255. A primeira célula começa em 20 Hz e a última em 22050 Hz. A matriz é bidimensional para representar áudio estéreo. A segunda matriz é baseada em informações de forma de onda e corresponde à potência de áudio, em que quanto mais forte a onda for, maior será o valor. A matriz waveform é um instantâneo granular das últimas 1024 fatias de energia de áudio tomadas em intervalos de tempo muito pequenos. Essa matriz também é bidimensional para representar áudio estéreo.

*Hdc*

Esse é um microsoft Windows para um contexto de dispositivo. Isso fornece uma maneira de identificar a superfície de desenho para Windows. Você não precisa criar, você só precisa usá-lo para chamadas de função de desenho específicas.

*Rect*

Este é um retângulo Windows Microsoft que define o tamanho de uma superfície de desenho. Esse é um retângulo simples com quatro propriedades: **esquerda,** **direita,** **superior** e **inferior.** Os valores reais são fornecidos pelo Windows Media Player para que você possa determinar como o usuário ou desenvolvedor de capa dimensionou a janela na qual você desenhará. Ele também determina a posição no HDC na qual o efeito deve ser renderizar.

Se seu código for uma implementação da função **IWMPEffects2::RenderWindowed** para renderização em uma janela, ele receberá os seguintes parâmetros:

*TimedLevel*

Essas são as mesmas informações que a **função Renderização** recebe.

*fRequiredRender*

O *parâmetro fRequiredRender* informa que sua visualização deve reint si mesmo, por exemplo, quando outra janela é arrastada sobre ela. Quando esse valor for false, você poderá ignorar com segurança o código de renderização se o item de mídia atual for interrompido ou pausado. Isso permite evitar o consumo de ciclos de CPU desnecessariamente.

O plug-in de exemplo gerado pelo Assistente de Plug-in não fornece uma implementação personalizada **para RenderWindowed.** Em vez disso, o código de plug-in de exemplo recupera o contexto do dispositivo da janela pai fornecida pelo Windows Media Player em [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)e, em seguida, recupera as dimensões da janela pai como uma estrutura RECT e, em seguida, chama para **Renderizar** usando o contexto do dispositivo, o RECT e o ponteiro de nível temporizada **de RenderWindowed**.

As seções a seguir fornecem mais informações sobre como implementar **Renderização**:

-   [Usando níveis temporáveis](using-timed-levels.md)
-   [Usando contextos de dispositivo](using-device-contexts.md)
-   [Usando retângulos](using-rectangles.md)
-   [Código de renderização de exemplo](sample-render-code.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando seu código**](implementing-your-code.md)
</dt> </dl>

 

 




