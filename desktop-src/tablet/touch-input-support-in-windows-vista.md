---
description: A partir do Windows Vista, a tecnologia do Tablet PC tem suporte para entrada por toque no Tablet PC com Digitalizadores com capacidade de toque. Esse suporte inclui uma interface do usuário aprimorada para auxiliar no direcionamento e nas janelas de comando ao usar um dedo para entrada.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Suporte à entrada por toque no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762999"
---
# <a name="touch-input-support-in-windows-vista"></a><span data-ttu-id="e9e97-104">Suporte à entrada por toque no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9e97-104">Touch Input Support in Windows Vista</span></span>

<span data-ttu-id="e9e97-105">A partir do Windows Vista, a tecnologia do Tablet PC tem suporte para entrada por toque no Tablet PC com Digitalizadores com capacidade de toque.</span><span class="sxs-lookup"><span data-stu-id="e9e97-105">Starting with Windows Vista, Tablet PC Technology has support for touch input on Tablet PC's with touch capable digitizers.</span></span> <span data-ttu-id="e9e97-106">Esse suporte inclui uma interface do usuário aprimorada para auxiliar no direcionamento e nas janelas de comando ao usar um dedo para entrada.</span><span class="sxs-lookup"><span data-stu-id="e9e97-106">This support includes an enhanced user interface to aid in targeting and commanding Windows when using a finger for input.</span></span>

## <a name="touch-digitizer-support"></a><span data-ttu-id="e9e97-107">Suporte ao Touch digitalizador</span><span class="sxs-lookup"><span data-stu-id="e9e97-107">Touch Digitizer Support</span></span>

### <a name="pen-and-touch-input-not-exclusive"></a><span data-ttu-id="e9e97-108">Entrada de caneta e toque não exclusiva</span><span class="sxs-lookup"><span data-stu-id="e9e97-108">Pen and Touch Input Not Exclusive</span></span>

<span data-ttu-id="e9e97-109">Não presuma que a entrada de caneta e toque sejam mutuamente exclusivas em aplicativos [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)e [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e9e97-109">Do not assume pen and touch input are mutually exclusive in [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), and [**RealTimeStylus**](realtimestylus-class.md) applications.</span></span>

<span data-ttu-id="e9e97-110">No Windows Vista, quando o sistema reconhece uma caneta, ele ignora a entrada por toque.</span><span class="sxs-lookup"><span data-stu-id="e9e97-110">In Windows Vista, when the system recognizes a pen it ignores touch input.</span></span> <span data-ttu-id="e9e97-111">Ou seja, o pressionamento de toque termina e o traço da caneta começa.</span><span class="sxs-lookup"><span data-stu-id="e9e97-111">That is, the touch stroke ends and the pen stroke begins.</span></span> <span data-ttu-id="e9e97-112">Como isso poderia ser alterado no futuro, seu código não deve assumir que a entrada de caneta e toque seja mutuamente exclusiva.</span><span class="sxs-lookup"><span data-stu-id="e9e97-112">Because this could possibly change in the future, your code should not assume pen and touch input are mutually exclusive.</span></span>

### <a name="other-mouse-message-sources"></a><span data-ttu-id="e9e97-113">Outras fontes de mensagens do mouse</span><span class="sxs-lookup"><span data-stu-id="e9e97-113">Other Mouse Message Sources</span></span>

<span data-ttu-id="e9e97-114">Há outras fontes de mensagens do mouse, mesmo quando o usuário está interagindo apenas usando o dedo ou a caneta.</span><span class="sxs-lookup"><span data-stu-id="e9e97-114">There are other sources of mouse messages even when the user is only interacting using finger or pen.</span></span> <span data-ttu-id="e9e97-115">As fontes incluem touchpads, bem como o movimento destinado a permitir que um aplicativo por trás de uma janela em camadas esteja ciente de que o mouse está se movendo para cima do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9e97-115">Sources include touchpads, as well as movement intended to let an application behind a layered window be aware that the mouse is moving above the application.</span></span>

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a><span data-ttu-id="e9e97-116">Habilitando e desabilitando a interface do usuário de entrada por toque</span><span class="sxs-lookup"><span data-stu-id="e9e97-116">Enabling and Disabling the Touch Input User Interface</span></span>

<span data-ttu-id="e9e97-117">Talvez você queira habilitar ou desabilitar a interface do usuário de entrada por toque, dependendo dos requisitos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9e97-117">You may wish to enable or disable the touch input user interface depending on the requirements of your application.</span></span> <span data-ttu-id="e9e97-118">Para fazer isso, intercepte as mensagens da janela do sistema operacional em um procedimento de janela e modifique a mensagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="e9e97-118">To accomplish this, intercept operating system window messages in a window procedure and modify the Windows message.</span></span> <span data-ttu-id="e9e97-119">Substitua [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) em seu aplicativo para interceptar essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="e9e97-119">Override [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in your application to intercept these messages.</span></span> <span data-ttu-id="e9e97-120">O pseudocódigo C a seguir \# mostra como habilitar e desabilitar a interface do usuário de entrada por toque.</span><span class="sxs-lookup"><span data-stu-id="e9e97-120">The following C\# pseudo-code shows how to enable and disable the touch input user interface.</span></span> <span data-ttu-id="e9e97-121">O código também mostra o uso da mesma técnica para desabilitar o gesto de pressionar e manter pressionado.</span><span class="sxs-lookup"><span data-stu-id="e9e97-121">The code also shows using the same technique to disable the press-and-hold gesture.</span></span> <span data-ttu-id="e9e97-122">Esse método também funciona para desabilitar a caneta.</span><span class="sxs-lookup"><span data-stu-id="e9e97-122">This method also works for disabling the stylus.</span></span>


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="e9e97-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9e97-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9e97-124">Toque do Windows</span><span class="sxs-lookup"><span data-stu-id="e9e97-124">Windows Touch</span></span>](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
