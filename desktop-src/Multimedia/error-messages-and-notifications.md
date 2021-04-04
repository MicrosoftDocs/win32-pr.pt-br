---
title: Mensagens de erro e notificações
description: Mensagens de erro e notificações
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- Macro MCIWndGetError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007444"
---
# <a name="error-messages-and-notifications"></a><span data-ttu-id="6f8a6-104">Mensagens de erro e notificações</span><span class="sxs-lookup"><span data-stu-id="6f8a6-104">Error Messages and Notifications</span></span>

<span data-ttu-id="6f8a6-105">O MCIWnd usa o MCI para controlar os dispositivos que desempenham e registram dados de multimídia.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-105">MCIWnd uses MCI to control the devices that play and record multimedia data.</span></span> <span data-ttu-id="6f8a6-106">Em geral, o MCIWnd exibe erros de MCI em uma caixa de diálogo de erro.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-106">In general, MCIWnd displays MCI errors in an error dialog box.</span></span> <span data-ttu-id="6f8a6-107">Um erro MCI é gerado sempre que um comando MCI falha.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-107">An MCI error is generated whenever an MCI command fails.</span></span> <span data-ttu-id="6f8a6-108">Por exemplo, se seu aplicativo tentar retomar a reprodução pausada usando a macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) e o dispositivo atual não oferecer suporte a resume, um erro será relatado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-108">For example, if your application tries to resume paused playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro and the current device does not support resume, an error is reported to the user.</span></span>

<span data-ttu-id="6f8a6-109">O MCIWnd permite que você tenha duas opções para lidar com mensagens de erro:</span><span class="sxs-lookup"><span data-stu-id="6f8a6-109">MCIWnd allows you two choices for handling error messages:</span></span>

-   <span data-ttu-id="6f8a6-110">Você pode impedir que mensagens de erro cheguem ao usuário.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-110">You can prevent error messages from reaching the user.</span></span> <span data-ttu-id="6f8a6-111">Para evitar a exibição de mensagens de erro MCI, especifique o \_ estilo de janela MCIWNDF NOERRORDLG ao criar uma instância de uma janela MCIWnd usando a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ou [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="6f8a6-111">To prevent the display of MCI error messages, specify the MCIWNDF\_NOERRORDLG window style when you create an instance of an MCIWnd window by using the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) or [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>
-   <span data-ttu-id="6f8a6-112">Você pode redirecioná-los para o aplicativo para exibição.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-112">You can redirect them to your application for display.</span></span> <span data-ttu-id="6f8a6-113">Para redirecionar mensagens de erro MCI para seu aplicativo, especifique o \_ estilo de janela MCIWNDF NOTIFYERROR ao criar uma instância de uma janela MCIWnd usando **MCIWndCreate** ou **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-113">To redirect MCI error messages to your application, specify the MCIWNDF\_NOTIFYERROR window style when you create an instance of an MCIWnd window by using **MCIWndCreate** or **CreateWindowEx**.</span></span>

<span data-ttu-id="6f8a6-114">Quando a notificação de erro é habilitada, o MCIWnd envia cada mensagem de notificação ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) para o manipulador de mensagens principal do pai da janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-114">When error notification is enabled, MCIWnd sends each notification message ([**MCIWNDM\_NOTIFYERROR**](mciwndm-notifyerror.md)) to the main message handler of the parent of the MCIWnd window.</span></span> <span data-ttu-id="6f8a6-115">Seu aplicativo deve ter um manipulador de mensagens para processar as mensagens de notificação recebidas.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-115">Your application must have a message handler to process the notification messages it receives.</span></span>

<span data-ttu-id="6f8a6-116">Você pode obter uma descrição textual da mensagem de erro MCI mais recente usando a macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="6f8a6-116">You can obtain a textual description of the most recent MCI error message by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span> <span data-ttu-id="6f8a6-117">Essa macro retorna o texto em um buffer definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-117">This macro returns the text in an application-defined buffer.</span></span> <span data-ttu-id="6f8a6-118">Se a cadeia de caracteres de erro for maior que o buffer, MCIWnd truncará a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6f8a6-118">If the error string is longer than the buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="6f8a6-119">Você pode rotear todas as notificações para outra janela usando a macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="6f8a6-119">You can route all notifications to another window by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>

 

 