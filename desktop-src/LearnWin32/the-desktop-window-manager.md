---
title: O Gerenciador de Janelas da Área de Trabalho
description: O Gerenciador de Janelas da Área de Trabalho
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99585a75bf2b25b086f09a17a0d8d93391b1f94f5018c5d4f83f90937fde620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896868"
---
# <a name="the-desktop-window-manager"></a>O Gerenciador de Janelas da Área de Trabalho

Antes Windows Vista, Windows programa de programação desenharia diretamente para a tela. Em outras palavras, o programa gravaria diretamente no buffer de memória mostrado pela placa de vídeo. Essa abordagem poderá causar artefatos visuais se uma janela não se reintint corretamente. Por exemplo, se o usuário arrastar uma janela sobre outra janela e a janela abaixo não for reintint rapidamente o suficiente, a janela superior poderá deixar uma trilha:

![uma captura de tela que mostra os artefatos de repintar.](images/graphics04.png)

A trilha é causada porque ambas as janelas pintam para a mesma área de memória. À medida que a janela superior é arrastada, a janela abaixo dela deve ser repintada. Se a reainting for muito lenta, ela causará os artefatos mostrados na imagem anterior.

Windows O Vista mudou fundamentalmente a maneira como as janelas são desenhadas, introduzindo o DWM (Gerenciador de Janelas da Área de Trabalho). Quando a DWM está habilitada, uma janela não é mais desenhada diretamente para o buffer de exibição. Em vez disso, cada janela desenha para um buffer de memória fora da tela, também chamado de *superfície de tela externa.* Em seguida, o DWM composição dessas superfícies na tela.

![um diagrama que mostra como o dwm composição da área de trabalho.](images/graphics05.png)

O DWM oferece várias vantagens em relação à arquitetura gráfica antiga.

-   Menos mensagens de repintar. Quando uma janela é impedida por outra janela, a janela obstruída não precisa repintar a si mesma.
-   Artefatos reduzidos. Anteriormente, arrastar uma janela podia criar artefatos visuais, conforme descrito.
-   Efeitos visuais. Como o DWM é responsável pela composição da tela, ele pode renderizar áreas translúcidas e desfocados da janela.
-   Dimensionamento automático para alto DPI. Embora o dimensionamento não seja a maneira ideal de lidar com alto DPI, é um fallback viável para aplicativos mais antigos que não foram projetados para configurações de DPI altas. (Retornaremos a este tópico posteriormente, na seção [DPI e Device-Independent Pixels](dpi-and-device-independent-pixels.md).)
-   Exibições alternativas. O DWM pode usar as superfícies fora da tela de várias maneiras interessantes. Por exemplo, a DWM é a tecnologia por trás Windows Flip 3D, miniaturas e transições animadas.

Observe, no entanto, que não há garantia de que a DWM está habilitada. A placa gráfica pode não dar suporte aos requisitos do sistema DWM e os usuários podem desabilitar o DWM por meio do painel de controle **Propriedades** do Sistema. Isso significa que seu programa não deve depender do comportamento de reainting do DWM. Teste seu programa com o DWM desabilitado para garantir que ele seja reintint corretamente.

## <a name="next"></a>Avançar

[Modo retido versus modo imediato](retained-mode-versus-immediate-mode.md)

 

 




