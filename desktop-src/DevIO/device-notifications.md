---
description: O sistema transmite um conjunto de eventos de alteração de dispositivo padrão para todos os aplicativos e serviços.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notificações do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089443"
---
# <a name="device-notifications"></a><span data-ttu-id="8705b-103">Notificações do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8705b-103">Device Notifications</span></span>

<span data-ttu-id="8705b-104">O sistema transmite um conjunto de eventos de alteração de dispositivo padrão para todos os aplicativos e serviços.</span><span class="sxs-lookup"><span data-stu-id="8705b-104">The system broadcasts a set of default device change events to all applications and services.</span></span> <span data-ttu-id="8705b-105">Você não precisa se registrar para receber esses eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="8705b-105">You do not need to register to receive these default events.</span></span> <span data-ttu-id="8705b-106">Consulte a seção comentários em [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="8705b-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details.</span></span> <span data-ttu-id="8705b-107">Para especificar outros eventos que seu aplicativo ou serviço deve receber, use a função **RegisterDeviceNotification** .</span><span class="sxs-lookup"><span data-stu-id="8705b-107">To specify other events your application or service should receive, use the **RegisterDeviceNotification** function.</span></span>

<span data-ttu-id="8705b-108">Quando um aplicativo ou serviço chama [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), ele também especifica a janela que receberá os eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="8705b-108">When an application or service calls [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), it also specifies the window that will receive the notification events.</span></span> <span data-ttu-id="8705b-109">Os serviços podem especificar um identificador de status de serviço em vez de um identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="8705b-109">Services can specify a service status handle instead of a window handle.</span></span> <span data-ttu-id="8705b-110">Se um serviço especificar seu identificador de status de serviço, seu manipulador de controle de serviço receberá os eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="8705b-110">If a service specifies its service status handle, its service control handler will receive the notification events.</span></span> <span data-ttu-id="8705b-111">Para obter mais informações, consulte [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="8705b-111">For more information, see [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="8705b-112">Certifique-se de manipular Plug and Play eventos de dispositivo o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="8705b-112">Be sure to handle Plug and Play device events as quickly as possible.</span></span> <span data-ttu-id="8705b-113">Caso contrário, o sistema pode deixar de responder.</span><span class="sxs-lookup"><span data-stu-id="8705b-113">Otherwise, the system may become unresponsive.</span></span> <span data-ttu-id="8705b-114">Se o manipulador de eventos for executar uma operação que possa bloquear a execução (como e/s), é melhor iniciar outro thread para executar a operação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8705b-114">If your event handler is to perform an operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.</span></span>

<span data-ttu-id="8705b-115">Os identificadores de notificação de dispositivo retornados por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) devem ser fechados chamando a função [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) quando não forem mais necessários.</span><span class="sxs-lookup"><span data-stu-id="8705b-115">Device notification handles returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) must be closed by calling the [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) function when they are no longer needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8705b-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8705b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8705b-117">Registro para notificação de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8705b-117">Registering for device notification</span></span>](registering-for-device-notification.md)
</dt> </dl>

 

 
