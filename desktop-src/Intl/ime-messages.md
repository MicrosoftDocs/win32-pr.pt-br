---
description: O sistema operacional envia mensagens de janela do IME para o procedimento de janela de um aplicativo quando ocorrem determinados eventos que afetam as janelas do IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Mensagens do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010562"
---
# <a name="ime-messages"></a><span data-ttu-id="069e8-103">Mensagens do IME</span><span class="sxs-lookup"><span data-stu-id="069e8-103">IME Messages</span></span>

<span data-ttu-id="069e8-104">O sistema operacional envia mensagens de janela do IME para o procedimento de janela de um aplicativo quando ocorrem determinados eventos que afetam as janelas do IME.</span><span class="sxs-lookup"><span data-stu-id="069e8-104">The operating system sends IME window messages to the window procedure of an application when certain events occur that affect the IME windows.</span></span> <span data-ttu-id="069e8-105">Por exemplo, o sistema operacional envia a [**mensagem \_ \_ SetContext do WM IME**](wm-ime-setcontext.md) para o aplicativo quando uma janela é ativada.</span><span class="sxs-lookup"><span data-stu-id="069e8-105">For example, the operating system sends the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message to the application when a window is activated.</span></span> <span data-ttu-id="069e8-106">Os aplicativos sem reconhecimento de IME passam essas mensagens para a função [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que as envia para a janela do IME padrão correspondente.</span><span class="sxs-lookup"><span data-stu-id="069e8-106">IME-unaware applications pass these messages to the [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which sends them to the corresponding default IME window.</span></span> <span data-ttu-id="069e8-107">Os aplicativos que reconhecem o IME processam essas mensagens ou as encaminham para suas janelas do IME.</span><span class="sxs-lookup"><span data-stu-id="069e8-107">IME-aware applications either process these messages or forward them to their own IME windows.</span></span>

<span data-ttu-id="069e8-108">Seu aplicativo pode direcionar uma janela IME para executar um comando, por exemplo, alterar a posição de uma janela de composição usando a mensagem [**de \_ \_ controle IME do WM**](wm-ime-control.md) .</span><span class="sxs-lookup"><span data-stu-id="069e8-108">Your application can direct an IME window to carry out a command, for example, change the position of a composition window, by using the [**WM\_IME\_CONTROL**](wm-ime-control.md) message.</span></span> <span data-ttu-id="069e8-109">O IME notifica o aplicativo sobre as alterações na cadeia de caracteres de composição usando a mensagem de [**\_ \_ composição IME do WM**](wm-ime-composition.md) e sobre as alterações gerais no status das janelas do IME enviando a mensagem de [**notificação do WM \_ \_ IME**](wm-ime-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="069e8-109">The IME notifies the application about changes to the composition string by using the [**WM\_IME\_COMPOSITION**](wm-ime-composition.md) message, and about general changes to the status of the IME windows by sending the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="069e8-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="069e8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="069e8-111">Sobre o Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="069e8-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
