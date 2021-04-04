---
title: Parent-Child interação da janela
description: Parent-Child interação da janela
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640740"
---
# <a name="parent-child-window-interaction"></a><span data-ttu-id="72d19-103">Parent-Child interação da janela</span><span class="sxs-lookup"><span data-stu-id="72d19-103">Parent-Child Window Interaction</span></span>

<span data-ttu-id="72d19-104">Algumas mensagens no nível do sistema, como o [**WM \_ PaletteChanged**](/windows/desktop/gdi/wm-palettechanged) e o [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), são enviadas somente para janelas de nível superior e sobrepostas.</span><span class="sxs-lookup"><span data-stu-id="72d19-104">Some system-level messages, such as [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), are sent only to top-level and overlapped windows.</span></span> <span data-ttu-id="72d19-105">Se uma janela de captura for uma janela filho, seu pai deverá encaminhar essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="72d19-105">If a capture window is a child window, its parent must forward these messages.</span></span>

<span data-ttu-id="72d19-106">Da mesma forma, se a janela pai alterar o tamanho, talvez seja necessário enviar mensagens de notificação para a janela de captura.</span><span class="sxs-lookup"><span data-stu-id="72d19-106">Similarly, if the parent window changes size, it might need to send notification messages to the capture window.</span></span> <span data-ttu-id="72d19-107">Por outro lado, se as dimensões do vídeo capturado forem alteradas, a janela de captura poderá precisar enviar mensagens de notificação para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="72d19-107">Conversely, if the dimensions of the captured video change, the capture window might need to send notification messages to the parent window.</span></span> <span data-ttu-id="72d19-108">A maneira mais simples de gerenciar isso é sempre manter as dimensões da janela de captura iguais ao tamanho do fluxo de vídeo capturado, notificando o pai sempre que essas dimensões forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="72d19-108">The simplest way to manage this is to always keep the capture window dimensions equal to the size of the captured video stream, notifying the parent whenever these dimensions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72d19-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72d19-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72d19-110">Capturar janelas</span><span class="sxs-lookup"><span data-stu-id="72d19-110">Capture Windows</span></span>](capture-windows.md)
</dt> </dl>

 

 