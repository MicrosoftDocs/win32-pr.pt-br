---
title: Portando X aplicativos do sistema de janelas
description: Portando X aplicativos do sistema de janelas
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL no Windows, portando
- portando para o sistema de janelas OpenGL, X
- Portabilidade OpenGL, sistema de janelas X
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159910"
---
# <a name="porting-x-window-system-applications"></a>Portando X aplicativos do sistema de janelas

Como o Windows, o sistema de janelas X é um sistema de manipulação de eventos, baseado em mensagem, que usa controles de janela e menus. O código OpenGL em seu aplicativo de sistema de janela X é provavelmente localizado em áreas que correspondem aproximadamente a onde aparecerão quando você a porta para o Windows. A maior parte do seu código OpenGL não será alterada, mas você deve reescrever qualquer código que seja específico para o sistema de janelas X.

**Use o procedimento geral a seguir para portar seus programas OpenGL do sistema de janelas X para o Windows**

1.  Reescreva o código específico do sistema da janela X usando o código equivalente do Windows. Localize a criação de janela e o código de manipulação de eventos. O sistema de janelas X e o Windows são um manipulador de eventos, sistemas de janelas baseados em mensagens, o que torna mais fácil determinar onde fazer as alterações apropriadas. (No entanto, especialmente para aplicativos grandes, a reescrita de um aplicativo de um sistema operacional para outro pode ser uma tarefa complexa e difícil.)
2.  Localize qualquer código que use as funções GLX. Essas são as funções que você converterá em suas funções equivalentes do Windows.
3.  Traduza funções de formato de pixel GLX e funções visuais/desenháveis para o formato de pixel do Windows/OpenGL apropriado e funções de contexto de dispositivo.
4.  Traduza funções de contexto de renderização GLX para funções de contexto de renderização do Windows/OpenGL.
5.  Traduza as funções GLX pixmap para funções equivalentes do Windows.
6.  Traduza GLX framebuffer e outras funções do GLX para as funções apropriadas do Windows.

 

 




