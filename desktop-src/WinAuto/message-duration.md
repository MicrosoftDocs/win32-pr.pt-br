---
title: Parâmetro de duração da mensagem
description: Normalmente, os aplicativos usam janelas pop-up para exibir brevemente mensagens de notificação importantes para o usuário. Um aplicativo cria a janela, exibe-a para uma duração definida pelo aplicativo e, em seguida, destrói a janela.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366140"
---
# <a name="message-duration-parameter"></a><span data-ttu-id="bc493-104">Parâmetro de duração da mensagem</span><span class="sxs-lookup"><span data-stu-id="bc493-104">Message duration parameter</span></span>

<span data-ttu-id="bc493-105">Normalmente, os aplicativos usam janelas pop-up para exibir brevemente mensagens de notificação importantes para o usuário.</span><span class="sxs-lookup"><span data-stu-id="bc493-105">Applications typically use pop-up windows to briefly display important notification messages to the user.</span></span> <span data-ttu-id="bc493-106">Um aplicativo cria a janela, exibe-a para uma duração definida pelo aplicativo e, em seguida, destrói a janela.</span><span class="sxs-lookup"><span data-stu-id="bc493-106">An application creates the window, displays it for an application-defined duration, and then destroys the window.</span></span>

<span data-ttu-id="bc493-107">Como os usuários com deficiências visuais ou condições cognitivas podem precisar de mais tempo para ler pop-ups de notificação, os aplicativos não devem embutir em código a duração.</span><span class="sxs-lookup"><span data-stu-id="bc493-107">Because users with visual impairments or cognitive conditions might need more time to read notification pop-ups, applications should not hard code the duration.</span></span> <span data-ttu-id="bc493-108">Em vez disso, um aplicativo deve definir a duração com base no valor do parâmetro de sistema **SPI \_ GETMESSAGEDURATION** .</span><span class="sxs-lookup"><span data-stu-id="bc493-108">Instead, an application should set the duration based on the value of the **SPI\_GETMESSAGEDURATION** system parameter.</span></span> <span data-ttu-id="bc493-109">Para recuperar esse parâmetro, use a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="bc493-109">To retrieve this parameter, use the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="bc493-110">Os aplicativos de tecnologia assistencial podem definir a duração da mensagem, com base na entrada do usuário, definindo o parâmetro do sistema **SPI \_ SETMESSAGEDURATION** .</span><span class="sxs-lookup"><span data-stu-id="bc493-110">Assistive technology applications can set the message duration, based on user input, by setting the **SPI\_SETMESSAGEDURATION** system parameter.</span></span>

 

 