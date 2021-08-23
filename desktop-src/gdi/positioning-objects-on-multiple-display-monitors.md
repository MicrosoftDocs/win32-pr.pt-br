---
description: Uma janela ou menu que está em mais de um monitor causa interrupção visual para um visualizador. Para minimizar esse problema, o sistema exibe menus e janelas novas e maximizada em um monitor. A tabela a seguir mostra como o monitor é escolhido.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Posicionando objetos em vários monitores de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6581fbed64b6a8ac83e29410e9758c6dea7b2d145958c57fa187abf34985c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602726"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Posicionando objetos em vários monitores de exibição

Uma janela ou menu que está em mais de um monitor causa interrupção visual para um visualizador. Para minimizar esse problema, o sistema exibe menus e janelas novas e maximizada em um monitor. A tabela a seguir mostra como o monitor é escolhido.



| Objeto         | Localização                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| janela         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(Ex) exibe uma janela no monitor que contém a maior parte da janela. Maximiza o monitor que contém a maior parte da janela antes de ser minimizado.<br/> A combinação de teclas ALT-TAB exibe uma janela no monitor que tem a janela ativa no momento.<br/>                                                                                                                                          |
| janela de propriedade   | no mesmo monitor que seu proprietário.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Submenu        | Aparece no monitor que contém a maior parte do item de menu correspondente.                                                                                                                                                                                                                                                                                                                                                                                                          |
| menu de contexto   | Aparece no monitor em que ocorreu o clique com o botão direito do mouse.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| lista suspensa | Aparece no monitor que contém o retângulo da caixa de combinação.                                                                                                                                                                                                                                                                                                                                                                                                                           |
|  (caixa de diálogo)     | Aparece no monitor da janela que a possui. Se estiver definido com o estilo DS \_ CENTERMOUSE, ele aparecerá no monitor com o mouse.<br/> Se ele não tiver proprietário, a janela ativa e a caixa de diálogo estão no mesmo aplicativo, a caixa de diálogo será exibida no monitor da janela ativa no momento.<br/> Se a caixa de diálogo não tiver proprietário e a janela ativa não estiver no mesmo aplicativo que a caixa de diálogo, a caixa de diálogo será exibida no monitor primário.<br/> |
| caixa de mensagem    | Aparece no monitor da janela que a possui.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Se uma janela entre dois monitores e um dos monitores for reposicionado, o sistema posicionará a janela no monitor que contém a maior parte da janela original.

Um aplicativo também normalmente precisará posicionar objetos. Por exemplo, uma janela pode precisar ser criada no mesmo monitor que outra janela.

**Para posicionar um objeto em um sistema de vários monitores**

1.  Determine o monitor apropriado.
2.  Obter as coordenadas para o monitor.
3.  Posiciona o objeto usando as coordenadas.

Normalmente, você posicionará um objeto no monitor primário ou em um monitor que já tenha um objeto nele. Para identificar o monitor para um determinado ponto, retângulo ou janela, use [**MonitorFromPoint,**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)e [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow).

Para obter as coordenadas do monitor, use [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), que fornece a área de trabalho e todo o retângulo do monitor. Observe que SM CXSCREEN e SM CYSCREEN sempre se referem ao monitor primário, não necessariamente ao monitor que \_ \_ exibe seu aplicativo. Além disso, evite SM \_ xxVIRTUALSCREEN porque isso centraliza sua janela na tela virtual, não em um monitor.

Para centralr caixas de diálogo na área de trabalho de uma janela, use o estilo DS \_ CENTER. Para centralr a caixa de diálogo em uma janela do aplicativo, use [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect). Windows restringe automaticamente menus e caixas de diálogo a um monitor. No entanto, pode haver um problema para menus personalizados, caixas suspensos personalizadas, paletas de ferramentas personalizadas e a posição do aplicativo salva.

Para ver um exemplo de como posicionar objetos corretamente, consulte [Posicionando objetos em uma instalação de várias exibições.](positioning-objects-on-a-multiple-display-setup.md)

Usar SM CXSCREEN e SM CYSCREEN para determinar o local de uma barra de ferramentas da área de trabalho do aplicativo (também chamada de barra de aplicativos ) restringe a barra de \_ \_ aplicativos ao monitor primário.  Para permitir que uma barra de aplicativos seja em qualquer borda de qualquer monitor, use as métricas do sistema apropriadas para calcular as bordas dos monitores. Além disso, use as **macros GET \_ X \_ LPARAM** e **GET Y \_ \_ LPARAM** para extrair as coordenadas, caso contrário, o sinal das coordenadas pode estar errado. Essas macros estão incluídas no Windowsx.h.

O tamanho de uma janela de tela inteira precisa mudar conforme ela se move entre monitores com resoluções diferentes. Para fazer isso, o aplicativo deve verificar em qual janela ele está, usando [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) ou [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) e, em seguida, usar [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para obter o tamanho do monitor. Como alternativa, você pode usar o **HMONITOR** da função **DirectDrawEnumerateEx** do DirectX. Em seguida, [**use SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) para posicionar e tamanho da janela para cobrir o monitor.

Uma janela maximizada não abrange uma barra de tarefas que tem a propriedade "Always on top". No entanto, uma janela de tela inteira abrange a barra de tarefas , por exemplo, em microsoft PowerPoint slides e jogos.

Para salvar e restaurar posteriormente a posição de uma janela quando um aplicativo é final, use as funções [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) e [**SetWindowPlacement.**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) No entanto, verifique se a posição ainda é válida antes de usá-la porque o monitor pode ter sido movido ou removido do sistema. O aplicativo exibirá a janela no monitor primário se **o HMONITOR** de uma janela for inválido.

O sistema tenta iniciar um aplicativo no monitor que contém seu atalho. Portanto, uma maneira de posicionar um aplicativo é ter seu atalho em um monitor desejado.

Se você usar [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) , fornecerá um *hWnd* para que o sistema abra novas janelas no mesmo monitor que o aplicativo de chamada.

Observe que os valores da estrutura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) são ligeiramente alterados para um sistema com vários monitores.

 

 
