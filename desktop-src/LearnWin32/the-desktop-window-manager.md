---
title: O Gerenciador de Janelas da Área de Trabalho
description: O Gerenciador de Janelas da Área de Trabalho
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103894"
---
# <a name="the-desktop-window-manager"></a>O Gerenciador de Janelas da Área de Trabalho

Antes do Windows Vista, um programa do Windows desenharia diretamente na tela. Em outras palavras, o programa gravaria diretamente no buffer de memória mostrado pela placa de vídeo. Essa abordagem pode causar artefatos visuais se uma janela não redesenhar corretamente. Por exemplo, se o usuário arrastar uma janela sobre outra janela e a janela abaixo não for redesenhada com rapidez suficiente, a janela superior poderá sair de uma trilha:

![uma captura de tela que mostra os artefatos redesenhados.](images/graphics04.png)

A trilha é causada porque o Windows Paint para a mesma área de memória. Como a janela superior é arrastada, a janela abaixo dela deve ser redesenhada. Se a repintura for muito lenta, ela causará os artefatos mostrados na imagem anterior.

O Windows Vista mudou fundamentalmente a forma como o Windows é desenhado, introduzindo o Gerenciador de Janelas da Área de Trabalho (DWM). Quando o DWM está habilitado, uma janela não é mais redesenhada diretamente para o buffer de exibição. Em vez disso, cada janela desenha um buffer de memória fora da tela, também chamado de *superfície fora da tela*. Em seguida, o DWM compõe essas superfícies na tela.

![um diagrama que mostra como o DWM compõe a área de trabalho.](images/graphics05.png)

O DWM fornece várias vantagens em relação à arquitetura gráfica antiga.

-   Menos mensagens redesenhadas. Quando uma janela está obstruída por outra janela, a janela obstruída não precisa redesenhar a si mesma.
-   Artefatos reduzidos. Anteriormente, arrastar uma janela poderia criar artefatos visuais, conforme descrito.
-   Efeitos visuais. Como o DWM é responsável por compor a tela, ele pode renderizar áreas translúcidas e borradas da janela.
-   Dimensionamento automático para DPI alto. Embora o dimensionamento não seja a maneira ideal de lidar com o DPI alto, ele é um fallback viável para aplicativos mais antigos que não foram projetados para configurações de DPI alto. (Voltaremos a este tópico mais tarde, na seção [dpi e Device-Independent pixels](dpi-and-device-independent-pixels.md).)
-   Modos de exibição alternativos. O DWM pode usar as superfícies fora da tela de várias maneiras interessantes. Por exemplo, o DWM é a tecnologia por trás do Windows Flip 3D, miniaturas e transições animadas.

No entanto, observe que não há garantia de que o DWM esteja habilitado. A placa gráfica pode não dar suporte aos requisitos de sistema do DWM e os usuários podem desabilitar o DWM por meio do painel de controle **Propriedades do sistema** . Isso significa que seu programa não deve depender do comportamento de repintura do DWM. Teste seu programa com o DWM desabilitado para certificar-se de que ele repinta corretamente.

## <a name="next"></a>Avançar

[Modo retido versus modo imediato](retained-mode-versus-immediate-mode.md)

 

 




