---
title: Portando aplicativos do sistema de janela X
description: Portando aplicativos do sistema de janela X
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL no Windows, portando
- portando para OpenGL,Sistema de JanelaS X
- Portação openGL, sistema de janelas X
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07a20de68df3806da40629252246f176beece0a4c3951180d484d9fadc6b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034756"
---
# <a name="porting-x-window-system-applications"></a>Portando aplicativos do sistema de janela X

Como Windows, o Sistema de JanelaS X é um sistema baseado em mensagens e manipulação de eventos que usa controles de janela e menus. O código OpenGL em seu aplicativo sistema de janela X provavelmente está localizado em áreas que correspondem aproximadamente ao local em que ele será exibido quando você porá-lo para Windows. A maioria do código OpenGL não será mudada, mas você deve reescrever qualquer código específico para o Sistema de Janela X.

**Use o procedimento geral a seguir para por portabilidade de seus programas OpenGL do Sistema de Janela X para Windows**

1.  Reescreva o código específico do Sistema de JanelaS X usando código Windows código equivalente. Localize o código de criação de janela e manipulação de eventos. O Sistema de Janelas X e Windows são sistemas de janelas baseados em mensagem e manipulação de eventos, o que facilita a determinação de onde fazer as alterações apropriadas. (No entanto, especialmente para aplicativos grandes, reescrever um aplicativo de um sistema operacional para outro pode ser uma tarefa complexa e difícil.)
2.  Localize qualquer código que use funções GLX. Essas são as funções que você converterá em suas funções Windows equivalentes.
3.  Traduza funções de formato de pixel GLX e funções visual/desenhável para funções apropriadas Windows/formato de pixel OpenGL e funções de contexto do dispositivo.
4.  Traduza funções de contexto de renderização GLX para Windows de contexto de renderização/OpenGL.
5.  Traduza funções deMap GLX em funções Windows equivalentes.
6.  Traduza o framebuffer GLX e outras funções GLX para as funções Windows apropriadas.

 

 




