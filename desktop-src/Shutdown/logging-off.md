---
description: A função ExitWindows faz logoff do usuário atual. Você também pode chamar a função ExitWindowsEx com o \_ sinalizador de logoff EXW.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Fazendo logoff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837496"
---
# <a name="logging-off"></a><span data-ttu-id="e86c4-104">Fazendo logoff</span><span class="sxs-lookup"><span data-stu-id="e86c4-104">Logging Off</span></span>

<span data-ttu-id="e86c4-105">A função [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) faz logoff do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="e86c4-105">The [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function logs off the current user.</span></span> <span data-ttu-id="e86c4-106">Você também pode chamar a função [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) com o \_ sinalizador de logoff EXW.</span><span class="sxs-lookup"><span data-stu-id="e86c4-106">You can also call the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function with the EXW\_LOGOFF flag.</span></span>

<span data-ttu-id="e86c4-107">Por padrão, quando um aplicativo usa [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) ou [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para fazer logoff, o sistema envia a mensagem do [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) para cada janela.</span><span class="sxs-lookup"><span data-stu-id="e86c4-107">By default, when an application uses [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) to log off, the system sends the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message to each window.</span></span> <span data-ttu-id="e86c4-108">Os aplicativos concordam em terminar retornando **true** quando recebem esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="e86c4-108">Applications agree to terminate by returning **TRUE** when they receive this message.</span></span> <span data-ttu-id="e86c4-109">Se qualquer aplicativo retornar **false** ao processar essa mensagem, a operação de logoff será cancelada.</span><span class="sxs-lookup"><span data-stu-id="e86c4-109">If any application returns **FALSE** when processing this message, the log-off operation is canceled.</span></span> <span data-ttu-id="e86c4-110">Se seu aplicativo manipula a mensagem do **WM \_ QUERYENDSESSION** , você pode permitir que o usuário cancele a operação de logoff, mesmo que outro aplicativo ou o sistema tenha originado a solicitação de sessão de término.</span><span class="sxs-lookup"><span data-stu-id="e86c4-110">If your application handles the **WM\_QUERYENDSESSION** message, you can allow the user to cancel the log-off operation, even if another application or the system originated the end-session request.</span></span> <span data-ttu-id="e86c4-111">Para obter um exemplo, consulte [como fazer logoff do usuário atual](how-to-log-off-the-current-user.md).</span><span class="sxs-lookup"><span data-stu-id="e86c4-111">For an example, see [How to Log Off the Current User](how-to-log-off-the-current-user.md).</span></span>

<span data-ttu-id="e86c4-112">Quando um aplicativo retorna **true** para o [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), ele recebe a mensagem de [**\_ EndSession do WM**](wm-endsession.md) e é encerrado, independentemente de como os outros aplicativos respondem à mensagem do **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="e86c4-112">When an application returns **TRUE** for [**WM\_QUERYENDSESSION**](wm-queryendsession.md), it receives the [**WM\_ENDSESSION**](wm-endsession.md) message and it is terminated, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="e86c4-113">Para forçar a finalização de todos os aplicativos, use o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)e especifique o \_ sinalizador de força EXW.</span><span class="sxs-lookup"><span data-stu-id="e86c4-113">To force all applications to terminate, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), and specify the EXW\_FORCE flag.</span></span> <span data-ttu-id="e86c4-114">Isso impede que o sistema envie mensagens do [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="e86c4-114">This prevents the system from sending [**WM\_QUERYENDSESSION**](wm-queryendsession.md) messages.</span></span>

<span data-ttu-id="e86c4-115">O sistema também envia o \_ sinal de controle de evento CTRL logoff \_ para cada processo durante uma operação de logoff.</span><span class="sxs-lookup"><span data-stu-id="e86c4-115">The system also sends the CTRL\_LOGOFF\_EVENT control signal to every process during a log-off operation.</span></span> <span data-ttu-id="e86c4-116">Um aplicativo de console pode registrar um [**HandlerRoutine**](/windows/console/handlerroutine) para processar essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="e86c4-116">A console application can register a [**HandlerRoutine**](/windows/console/handlerroutine) to process these messages.</span></span>

<span data-ttu-id="e86c4-117">Se o processo que chamou o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) estiver em execução na sessão de logon do usuário interativo, todos os processos na sessão de logon serão encerrados.</span><span class="sxs-lookup"><span data-stu-id="e86c4-117">If the process that called [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) is running in the logon session of the interactive user, all processes in the logon session are terminated.</span></span> <span data-ttu-id="e86c4-118">Se o processo que chama o **ExitWindowsEx** estiver em alguma outra sessão de logon, somente as notificações serão feitas; nenhum processo foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="e86c4-118">If the process calling **ExitWindowsEx** is in some other logon session, only the notifications are made; no processes are terminated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e86c4-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e86c4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e86c4-120">Como fazer logoff do usuário atual</span><span class="sxs-lookup"><span data-stu-id="e86c4-120">How to Log Off the Current User</span></span>](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
