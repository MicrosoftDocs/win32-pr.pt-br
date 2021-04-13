---
title: Criando uma janela de captura do AVICap
description: Criando uma janela de captura do AVICap
ms.assetid: a1418e98-f16d-401a-94a7-64fb272a39e2
keywords:
- função capCreateCaptureWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d035d44b8d0b46df31afa5c3235e59286121c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292010"
---
# <a name="creating-an-avicap-capture-window"></a><span data-ttu-id="e2fd8-104">Criando uma janela de captura do AVICap</span><span class="sxs-lookup"><span data-stu-id="e2fd8-104">Creating an AVICap Capture Window</span></span>

<span data-ttu-id="e2fd8-105">Você pode criar uma janela de captura da classe de janela AVICap usando a função [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) .</span><span class="sxs-lookup"><span data-stu-id="e2fd8-105">You can create a capture window of the AVICap window class by using the [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) function.</span></span> <span data-ttu-id="e2fd8-106">Essa função retorna um identificador de janela que identifica a janela de captura e é usada por um aplicativo para enviar mensagens subsequentes para a janela.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-106">This function returns a window handle that identifies the capture window and is used by an application to send subsequent messages to the window.</span></span>

<span data-ttu-id="e2fd8-107">Você pode criar uma ou mais janelas de captura em um aplicativo e conectar cada janela de captura a um dispositivo de captura diferente.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-107">You can create one or more capture windows in an application and connect each capture window to a different capture device.</span></span>

 

 




