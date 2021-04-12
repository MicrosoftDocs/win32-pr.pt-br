---
title: SendMessage, mensagem de mensagens e funções relacionadas
description: Esta seção descreve as considerações sobre o encaminhamento de mensagens usando SendMessage, CreateMessage e funções relacionadas com mensagens de toque.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366335"
---
# <a name="sendmessage-postmessage-and-related-functions"></a><span data-ttu-id="7171e-103">SendMessage, mensagem de mensagens e funções relacionadas</span><span class="sxs-lookup"><span data-stu-id="7171e-103">SendMessage, PostMessage, and Related Functions</span></span>

<span data-ttu-id="7171e-104">Esta seção descreve as considerações sobre o encaminhamento de mensagens usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)e funções relacionadas com mensagens de toque.</span><span class="sxs-lookup"><span data-stu-id="7171e-104">This section describes considerations about forwarding messages using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), and related functions with touch messages.</span></span>

<span data-ttu-id="7171e-105">Se uma mensagem de toque for encaminhada usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)ou alguma outra função relacionada, o identificador de entrada por toque será fechado.</span><span class="sxs-lookup"><span data-stu-id="7171e-105">If a touch message is forwarded using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some other related function, the touch input handle is closed.</span></span> <span data-ttu-id="7171e-106">Se você tiver recuperado as informações contidas referenciadas por um identificador de entrada por toque por meio de uma chamada para [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), esses dados permanecerão válidos até que você libere a memória.</span><span class="sxs-lookup"><span data-stu-id="7171e-106">If you have retrieved the information contained referenced by a touch input handle through a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), that data will remain valid until you free the memory.</span></span>

<span data-ttu-id="7171e-107">Um aplicativo que recebe mensagens de toque encaminhadas por meio de um desses mecanismos possui o identificador de entrada por toque que recebe na mensagem *lParam* e é responsável por fechá-la.</span><span class="sxs-lookup"><span data-stu-id="7171e-107">An application that receives touch messages forwarded through one of these mechanisms owns the touch input handle it receives in the message *LPARAM* and is responsible for closing it.</span></span> <span data-ttu-id="7171e-108">Se você não fechar o identificador com uma chamada para [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), passar a mensagem para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)ou encaminhar a mensagem usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [mensagem](/windows/win32/api/winuser/nf-winuser-postmessagea)posterior ou alguma função relacionada, você terá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="7171e-108">If you don't close the handle with a call to [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pass the message to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), or forward the message using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some related function, you will have a memory leak.</span></span>

> [!Note]  
> <span data-ttu-id="7171e-109">As mensagens de toque estão sujeitas às regras normais de UIPI (isolamento de privilégio de interface do usuário) quando elas são encaminhadas.</span><span class="sxs-lookup"><span data-stu-id="7171e-109">Touch messages are subject to normal User Interface Privilege Isolation (UIPI) rules when they are forwarded.</span></span>

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a><span data-ttu-id="7171e-110">Funções relacionadas a SendMessage e a mensagem</span><span class="sxs-lookup"><span data-stu-id="7171e-110">Functions related to SendMessage and PostMessage</span></span>

<span data-ttu-id="7171e-111">As funções a seguir podem afetar o estado do identificador de entrada por toque.</span><span class="sxs-lookup"><span data-stu-id="7171e-111">The following functions that can affect the state of the touch input handle.</span></span>

-   [<span data-ttu-id="7171e-112">SendMessage</span><span class="sxs-lookup"><span data-stu-id="7171e-112">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="7171e-113">PostMessage</span><span class="sxs-lookup"><span data-stu-id="7171e-113">PostMessage</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   <span data-ttu-id="7171e-114">SendNotifyMessage</span><span class="sxs-lookup"><span data-stu-id="7171e-114">SendNotifyMessage</span></span>
-   <span data-ttu-id="7171e-115">SendMessageCallback</span><span class="sxs-lookup"><span data-stu-id="7171e-115">SendMessageCallback</span></span>
-   <span data-ttu-id="7171e-116">SendMessageTimeout</span><span class="sxs-lookup"><span data-stu-id="7171e-116">SendMessageTimeout</span></span>
-   <span data-ttu-id="7171e-117">PostThreadMessage</span><span class="sxs-lookup"><span data-stu-id="7171e-117">PostThreadMessage</span></span>

## <a name="related-topics"></a><span data-ttu-id="7171e-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7171e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7171e-119">Funções</span><span class="sxs-lookup"><span data-stu-id="7171e-119">Functions</span></span>](mtfunctions.md)
</dt> <dt>

[<span data-ttu-id="7171e-120">DefWindowProc</span><span class="sxs-lookup"><span data-stu-id="7171e-120">DefWindowProc</span></span>](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 