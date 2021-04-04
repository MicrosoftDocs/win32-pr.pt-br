---
title: Implementando renderização
description: Implementando renderização
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- visualizações, eventos cronometrados
- visualizações personalizadas, eventos cronometrados
- visualizações, função render
- visualizações personalizadas, função render
- visualizações, função RenderWindow
- visualizações personalizadas, função RenderWindow
- Processar função, parâmetros
- Função RenderWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007117"
---
# <a name="implementing-render"></a>Implementando renderização

A maneira mais fácil de considerar a programação de visualização é que você está criando um manipulador para um evento cronometrado. Em intervalos específicos, o Windows Media Player tira um instantâneo dos dados de áudio que está jogando e fornece os dados de instantâneo para a visualização atualmente carregada. Isso é semelhante à programação orientada a eventos e faz parte do modelo de programação do Microsoft Windows. Você escreve o código e aguarda que ele seja chamado por um evento específico.

Se o seu código for uma implementação da função [IWMPEffects:: render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) para renderização no modo sem janela, ele receberá os seguintes parâmetros:

*TimedLevel*

Essa é uma estrutura que define os dados de áudio que seu código analisará. A estrutura é composta de duas matrizes. A primeira matriz é baseada em informações de frequência e contém um instantâneo do espectro de áudio dividido em 1024 partes. Cada célula da matriz contém um valor de 0 a 255. A primeira célula começa em 20 Hz e a última em 22050 Hz. A matriz é bidimensional para representar áudio estéreo. A segunda matriz baseia-se nas informações de forma de onda e corresponde à energia de áudio, em que quanto mais forte for a onda, maior será o valor. A matriz de forma de onda é um instantâneo granular das últimas 1024 fatias de energia de áudio executadas em intervalos de tempo muito pequenos. Essa matriz também é bidimensional para representar áudio estéreo.

*HDC*

Trata-se de um identificador do Microsoft Windows para um contexto de dispositivo. Isso oferece uma maneira de identificar a superfície de desenho para o Windows. Você não precisa criá-lo, só precisa usá-lo para chamadas de função de desenho específicas.

*RECT*

Este é um retângulo do Microsoft Windows que define o tamanho de uma superfície de desenho. Este é um retângulo simples com quatro propriedades: **esquerda**, **direita**, **superior** e **inferior**. Os valores reais são fornecidos pelo Windows Media Player para que você possa determinar como o usuário ou o desenvolvedor de capa dimensionará a janela que você desenhará. Ele também determina a posição no HDC em que o efeito deve renderizar.

Se o seu código for uma implementação da função **IWMPEffects2:: RenderWindowed** para renderização em uma janela, ele receberá os seguintes parâmetros:

*TimedLevel*

Essas são as mesmas informações que a função **render** recebe.

*fRequiredRender*

O parâmetro *fRequiredRender* informa que sua visualização deve redesenhar a si mesma, por exemplo, quando outra janela é arrastada sobre ela. Quando esse valor for false, você poderá ignorar com segurança o código de renderização se o item de mídia atual for interrompido ou pausado. Isso permite evitar o consumo de ciclos de CPU desnecessariamente.

O plug-in de exemplo gerado pelo assistente de plug-in não fornece uma implementação personalizada para **RenderWindowed**. Em vez disso, o código de plug-in de exemplo recupera o contexto do dispositivo da janela pai fornecida pelo Windows Media Player em [IWMPEffects2:: Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), recupera as dimensões da janela pai como uma estrutura RECT e, em seguida, chama para **render** usando o contexto do dispositivo, o Rect e o ponteiro de nível cronometrado de **RenderWindowed**.

As seções a seguir fornecem mais informações sobre como implementar o **render**:

-   [Usando níveis de tempo](using-timed-levels.md)
-   [Usando contextos de dispositivo](using-device-contexts.md)
-   [Usando retângulos](using-rectangles.md)
-   [Exemplo de código de renderização](sample-render-code.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando seu código**](implementing-your-code.md)
</dt> </dl>

 

 




