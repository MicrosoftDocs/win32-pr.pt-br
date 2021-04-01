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
# <a name="porting-x-window-system-applications"></a><span data-ttu-id="ac689-106">Portando X aplicativos do sistema de janelas</span><span class="sxs-lookup"><span data-stu-id="ac689-106">Porting X Window System Applications</span></span>

<span data-ttu-id="ac689-107">Como o Windows, o sistema de janelas X é um sistema de manipulação de eventos, baseado em mensagem, que usa controles de janela e menus.</span><span class="sxs-lookup"><span data-stu-id="ac689-107">Like Windows, the X Window System is an event-handling, message-based system that uses window controls and menus.</span></span> <span data-ttu-id="ac689-108">O código OpenGL em seu aplicativo de sistema de janela X é provavelmente localizado em áreas que correspondem aproximadamente a onde aparecerão quando você a porta para o Windows.</span><span class="sxs-lookup"><span data-stu-id="ac689-108">The OpenGL code in your X Window System application is probably located in areas that roughly correspond to where it will appear when you port it to Windows.</span></span> <span data-ttu-id="ac689-109">A maior parte do seu código OpenGL não será alterada, mas você deve reescrever qualquer código que seja específico para o sistema de janelas X.</span><span class="sxs-lookup"><span data-stu-id="ac689-109">Most of your OpenGL code will not change, but you must rewrite any code that is specific to the X Window System.</span></span>

<span data-ttu-id="ac689-110">**Use o procedimento geral a seguir para portar seus programas OpenGL do sistema de janelas X para o Windows**</span><span class="sxs-lookup"><span data-stu-id="ac689-110">**Use the following general procedure to port your X Window System OpenGL programs to Windows**</span></span>

1.  <span data-ttu-id="ac689-111">Reescreva o código específico do sistema da janela X usando o código equivalente do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac689-111">Rewrite the X Window System specific code using equivalent Windows code.</span></span> <span data-ttu-id="ac689-112">Localize a criação de janela e o código de manipulação de eventos.</span><span class="sxs-lookup"><span data-stu-id="ac689-112">Locate window-creation and event-handling code.</span></span> <span data-ttu-id="ac689-113">O sistema de janelas X e o Windows são um manipulador de eventos, sistemas de janelas baseados em mensagens, o que torna mais fácil determinar onde fazer as alterações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ac689-113">The X Window System and Windows are event-handling, message-based windowing systems, which makes it easier to determine where to make the appropriate changes.</span></span> <span data-ttu-id="ac689-114">(No entanto, especialmente para aplicativos grandes, a reescrita de um aplicativo de um sistema operacional para outro pode ser uma tarefa complexa e difícil.)</span><span class="sxs-lookup"><span data-stu-id="ac689-114">(However, especially for large applications, rewriting an application from one operating system to another can be a complex and difficult undertaking.)</span></span>
2.  <span data-ttu-id="ac689-115">Localize qualquer código que use as funções GLX.</span><span class="sxs-lookup"><span data-stu-id="ac689-115">Locate any code that uses GLX functions.</span></span> <span data-ttu-id="ac689-116">Essas são as funções que você converterá em suas funções equivalentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac689-116">These are the functions you'll translate to their equivalent Windows functions.</span></span>
3.  <span data-ttu-id="ac689-117">Traduza funções de formato de pixel GLX e funções visuais/desenháveis para o formato de pixel do Windows/OpenGL apropriado e funções de contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac689-117">Translate GLX pixel format functions and Visual/Drawable functions to appropriate Windows/OpenGL pixel format and device context functions.</span></span>
4.  <span data-ttu-id="ac689-118">Traduza funções de contexto de renderização GLX para funções de contexto de renderização do Windows/OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ac689-118">Translate GLX rendering context functions to Windows/OpenGL rendering context functions.</span></span>
5.  <span data-ttu-id="ac689-119">Traduza as funções GLX pixmap para funções equivalentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac689-119">Translate GLX Pixmap functions to equivalent Windows functions.</span></span>
6.  <span data-ttu-id="ac689-120">Traduza GLX framebuffer e outras funções do GLX para as funções apropriadas do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac689-120">Translate GLX framebuffer and other GLX functions to the appropriate Windows functions.</span></span>

 

 




