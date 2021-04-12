---
title: Quando responder à mensagem de WM_GETOBJECT
description: Se um aplicativo oferecer suporte ao Microsoft Acessibilidade Ativa ou automação de interface do usuário para um elemento de interface do usuário, o aplicativo não deverá responder à mensagem do WM \_ GetObject antes que o objeto que representa o elemento da interface do usuário seja totalmente inicializado ou depois que o aplicativo começar a fechar.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cfa8d6604a13e84ffa89bf1fcf93d5d13e66e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454273"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a><span data-ttu-id="27cb1-103">Quando responder à mensagem do WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="27cb1-103">When to Respond to the WM\_GETOBJECT Message</span></span>

<span data-ttu-id="27cb1-104">Se um aplicativo oferecer suporte ao Microsoft Acessibilidade Ativa ou automação de interface do usuário para um elemento de interface do usuário, o aplicativo não deverá responder à mensagem do [**WM \_ GetObject**](wm-getobject.md) antes que o objeto que representa o elemento da interface do usuário seja totalmente inicializado ou depois que o aplicativo começar a fechar.</span><span class="sxs-lookup"><span data-stu-id="27cb1-104">If an application supports Microsoft Active Accessibility or UI Automation for a UI element, the application must not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message before the object that represents the UI element is fully initialized, or after the application has begun to close.</span></span> <span data-ttu-id="27cb1-105">Quando um aplicativo cria uma nova janela, o sistema gera o [**objeto de evento \_ \_ Create**](event-constants.md) WinEvent para notificar os clientes antes de enviar a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) para o procedimento de janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27cb1-105">When an application creates a new window, the system raises the [**EVENT\_OBJECT\_CREATE**](event-constants.md) WinEvent to notify clients before sending the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to the application's window procedure.</span></span> <span data-ttu-id="27cb1-106">Como muitos aplicativos usam o **WM \_ Create** para iniciar o processo de inicialização, qualquer implementação de acessibilidade de um elemento de interface do usuário não responderá à mensagem do [**WM \_ GetObject**](wm-getobject.md) até que o aplicativo tenha terminado de processar a mensagem de **\_ criação do WM** .</span><span class="sxs-lookup"><span data-stu-id="27cb1-106">Because many applications use **WM\_CREATE** to start the initialization process, any accessibility implementation of a UI element does not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message until after the application has finished processing the **WM\_CREATE** message.</span></span>

 

 