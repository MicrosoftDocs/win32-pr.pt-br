---
description: Uma janela ou menu que está em mais de um monitor causa uma interrupção Visual para um visualizador. Para minimizar esse problema, o sistema exibe menus e as janelas novas e maximizadas em um monitor. A tabela a seguir mostra como o monitor é escolhido.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Posicionando objetos em vários monitores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77149291737482fa0f3e7fe19ee4f350ee6521d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967610"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Posicionando objetos em vários monitores de vídeo

Uma janela ou menu que está em mais de um monitor causa uma interrupção Visual para um visualizador. Para minimizar esse problema, o sistema exibe menus e as janelas novas e maximizadas em um monitor. A tabela a seguir mostra como o monitor é escolhido.



| Objeto         | Localização                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| janela         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(ex) exibe uma janela no monitor que contém a maior parte da janela. Maximiza o monitor que contém a maior parte da janela antes que ela seja minimizada.<br/> A combinação de teclas ALT-TAB exibe uma janela no monitor que tem a janela ativa no momento.<br/>                                                                                                                                          |
| janela de propriedade   | no mesmo monitor que seu proprietário.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| submenu        | Aparece no monitor que contém a maior parte do item de menu correspondente.                                                                                                                                                                                                                                                                                                                                                                                                          |
| menu de contexto   | Aparece no monitor onde ocorreu o clique com o botão direito do mouse.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| lista suspensa | Aparece no monitor que contém o retângulo da caixa de combinação.                                                                                                                                                                                                                                                                                                                                                                                                                           |
|  (caixa de diálogo)     | Aparece no monitor da janela que o possui. Se ele for definido com \_ o estilo DS CENTERMOUSE, ele aparecerá no monitor com o mouse.<br/> Se não tiver proprietário e a janela ativa e a caixa de diálogo estiverem no mesmo aplicativo, a caixa de diálogo aparecerá no monitor da janela ativa no momento.<br/> Se a caixa de diálogo não tiver proprietário e a janela ativa não estiver no mesmo aplicativo que a caixa de diálogo, a caixa de diálogo aparecerá no monitor primário.<br/> |
| caixa de mensagem    | Aparece no monitor da janela que o possui.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Se uma janela espalhada por dois monitores e um dos monitores for reposicionado, o sistema posicionará a janela no monitor que contém a maior parte da janela original.

Normalmente, um aplicativo também precisa posicionar objetos. Por exemplo, uma janela pode precisar ser criada no mesmo monitor que outra janela.

**Para posicionar um objeto em um sistema de vários monitores**

1.  Determine o monitor apropriado.
2.  Obtenha as coordenadas para o monitor.
3.  Posicione o objeto usando as coordenadas.

Normalmente, você posicionará um objeto no monitor primário ou em um monitor que já tenha um objeto nele. Para identificar o monitor de um determinado ponto, retângulo ou janela, use [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint), [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)e [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow).

Para obter as coordenadas do monitor, use [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), que fornece a área de trabalho e todo o retângulo do monitor. Observe que SM \_ CXSCREEN e SM \_ CYSCREEN sempre fazem referência ao monitor primário, não necessariamente ao monitor que exibe seu aplicativo. Além disso, evite \_ o SM xxVIRTUALSCREEN porque isso centraliza sua janela na tela virtual, não em um monitor.

Para centralizar as caixas de diálogo na área de trabalho de uma janela, use o \_ estilo DS Center. Para centralizar a caixa de diálogo em uma janela de aplicativo, use [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect). O Windows restringe automaticamente os menus e as caixas de diálogo a um monitor. No entanto, pode haver um problema para menus personalizados, caixas suspensas personalizadas, paletas de ferramentas personalizadas e a posição do aplicativo salvo.

Para obter um exemplo de como posicionar objetos corretamente, consulte [posicionando objetos em uma configuração de vários monitores](positioning-objects-on-a-multiple-display-setup.md).

Usar SM \_ CXSCREEN e SM \_ CYSCREEN para determinar o local de uma barra de ferramentas de área de trabalho do aplicativo (também chamado de *AppBar*) restringe o AppBar ao monitor primário. Para permitir que um AppBar esteja em qualquer borda de qualquer monitor, use as métricas de sistema apropriadas para calcular as bordas dos monitores. Além disso, use as macros **Get \_ X \_ lParam** e **Get \_ Y \_ lParam** para extrair as coordenadas, caso contrário, o sinal das coordenadas pode estar errado. Essas macros estão incluídas no Windowsx. h.

O tamanho de uma janela de tela inteira precisa ser alterado à medida que ela se move entre monitores com resoluções diferentes. Para fazer isso, o aplicativo deve verificar em qual janela ele está, usando [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) ou [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) e, em seguida, usar [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para obter o tamanho do monitor. Como alternativa, você pode usar o **HMONITOR** da função DirectX **DirectDrawEnumerateEx** . Em seguida, use [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) para posicionar e dimensionar a janela para cobrir o monitor.

Uma janela maximizada não cobre uma barra de tarefas que tem a propriedade "Always on Top". No entanto, uma janela de tela inteira cobre a barra de tarefas, por exemplo, em apresentações e jogos de slides do Microsoft PowerPoint.

Para salvar e posteriormente restaurar, a posição de uma janela quando um aplicativo é encerrado, use as funções [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) e [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) . No entanto, verifique se a posição ainda é válida antes de usá-la porque o monitor pode ter sido movido ou removido do sistema. O aplicativo exibirá a janela no monitor primário se o **HMONITOR** de uma janela for inválido.

O sistema tenta iniciar um aplicativo no monitor que contém seu atalho. Portanto, uma maneira de posicionar um aplicativo é ter seu atalho em um monitor desejado.

Se você usar [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) , forneça um *hWnd* para que o sistema abra todas as janelas novas no mesmo monitor que o aplicativo de chamada.

Observe que os valores da estrutura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) são ligeiramente alterados para um sistema com vários monitores.

 

 
