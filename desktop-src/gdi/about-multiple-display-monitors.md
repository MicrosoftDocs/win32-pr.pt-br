---
description: Quando vários monitores fazem parte da área de trabalho, os objetos podem viajar diretamente entre monitores.
ms.assetid: eb7576c6-322c-48d0-abbb-bdc3b34976c3
title: Sobre vários monitores de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5997e39768d01522ae1fdd2e976c611e67826350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967560"
---
# <a name="about-multiple-display-monitors"></a>Sobre vários monitores de exibição

Quando vários monitores fazem parte da área de trabalho, os objetos podem viajar diretamente entre monitores. Ou seja, você pode arrastar janelas ou atalhos de um monitor para outro, e pode dimensionar o Windows para cobrir mais de um monitor. Além disso, se um monitor for instalado acima de outro, um cursor que sai da parte inferior do monitor superior aparecerá na parte superior do monitor inferior.

Normalmente, um usuário organiza os monitores no sistema para refletir a disposição das unidades de exibição físicas; por exemplo, lado a lado ou um-on-top-do-outro. O usuário faz isso com a guia monitores, que substitui a guia **configurações** na caixa de diálogo **Propriedades de exibição** por meio do painel de controle. Os monitores devem formar uma região contígua, ou seja, cada monitor toca em outro monitor em pelo menos parte de uma borda.

Quando uma janela é movida ou redimensionada, parte da legenda fica sempre visível para que o usuário possa mover e redimensionar a janela usando o mouse. O movimento do cursor é restrito à área dos monitores, portanto, está sempre visível. Os ícones do shell são posicionados no mesmo monitor da barra de tarefas e a barra de tarefas pode estar em qualquer monitor, consulte [várias considerações de monitor para programas mais antigos](multiple-monitor-considerations-for-older-programs.md).

Um sistema de vários monitores afeta certas combinações de teclas. A combinação de teclas ALT + PRINTSCRN tira um instantâneo da janela em primeiro plano, como sempre. No entanto, a chave PRINTSCRN tira um instantâneo do monitor que tem o mouse. A combinação de teclas CTRL + PRINTSCRN tira um instantâneo da tela virtual inteira, confira [a tela virtual](the-virtual-screen.md).

O suporte para vários monitores não afeta o desempenho dos aplicativos durante a execução em um único ambiente de exibição. Ou seja, quando executado em um único sistema de vídeo, nenhuma sobrecarga adicional estará presente no código de operações de gráficos de alto desempenho. No entanto, em um sistema de vários monitores, o desempenho é ligeiramente afetado se um aplicativo é executado apenas em um dos dispositivos gráficos. Além disso, o desempenho pode ser bastante afetado se um aplicativo abranger vários monitores, especialmente para operações com uso intensivo de gráficos.

*Tela inteira* é um recurso fornecido pelo sistema operacional que permite que um usuário alterne um aplicativo para um estado especial em que o aplicativo possa acessar o hardware de gráficos VGA diretamente. Esse é um recurso importante para jogos e outros aplicativos voltados para gráficos que exigem alto desempenho. Além disso, ele costuma ser usado por desenvolvedores para edição de texto, pois permite a rolagem de texto muito rápida.

Em um ambiente de vários monitores, apenas um dispositivo de gráficos pode ser compatível com VGA. Essa é uma limitação do hardware do computador que exige que apenas um dispositivo responda a qualquer endereço de hardware. Como o padrão de compatibilidade de hardware VGA requer endereços de hardware específicos, apenas um dispositivo de gráficos VGA pode estar presente em um computador e somente esse dispositivo pode responder fisicamente aos endereços VGA. Assim, os aplicativos que exigem a tela inteira serão executados apenas no dispositivo específico que dá suporte à compatibilidade de hardware VGA.

Esta visão geral fornece informações sobre os tópicos a seguir.

-   [A tela virtual](the-virtual-screen.md)
-   [HMONITOR e o contexto do dispositivo](hmonitor-and-the-device-context.md)
-   [Enumeração e controle de exibição](enumeration-and-display-control.md)
-   [Várias métricas do sistema de monitor](multiple-monitor-system-metrics.md)
-   [Usando monitores múltiplos como exibições independentes](using-multiple-monitors-as-independent-displays.md)
-   [Cores em vários monitores de vídeo](colors-on-multiple-display-monitors.md)
-   [Posicionando objetos em vários monitores de vídeo](positioning-objects-on-multiple-display-monitors.md)
-   [Vários aplicativos de monitor em sistemas diferentes](multiple-monitor-applications-on-different-systems.md)
-   [Várias considerações de monitor para programas mais antigos](multiple-monitor-considerations-for-older-programs.md)

 

 



