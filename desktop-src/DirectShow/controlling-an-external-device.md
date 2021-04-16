---
description: Controlando um dispositivo externo
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Controlando um dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500218"
---
# <a name="controlling-an-external-device"></a><span data-ttu-id="d4238-103">Controlando um dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="d4238-103">Controlling an External Device</span></span>

<span data-ttu-id="d4238-104">Para controlar um dispositivo VTR (gravador de fita de vídeo), use o método [**IAMExtTransport::p UT \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="d4238-104">To control a video tape recorder (VTR) device, use the [**IAMExtTransport::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) method.</span></span> <span data-ttu-id="d4238-105">Especifique o novo estado usando uma das constantes listadas no estado de [transporte do dispositivo](device-transport-state.md).</span><span class="sxs-lookup"><span data-stu-id="d4238-105">Specify the new state by using one of the constants listed in the [Device Transport State](device-transport-state.md).</span></span> <span data-ttu-id="d4238-106">Por exemplo, para parar o dispositivo, use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d4238-106">For example, to stop the device, use the following:</span></span>


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



<span data-ttu-id="d4238-107">Como o VTR é um dispositivo físico, normalmente há um atraso entre a emissão do comando e quando o comando é concluído.</span><span class="sxs-lookup"><span data-stu-id="d4238-107">Because the VTR is a physical device, there is typically a lag between issuing the command and when the command completes.</span></span> <span data-ttu-id="d4238-108">Seu aplicativo deve criar um segundo thread de trabalho que aguarde a conclusão do comando.</span><span class="sxs-lookup"><span data-stu-id="d4238-108">Your application should create a second worker thread that waits for the command to finish.</span></span> <span data-ttu-id="d4238-109">Quando o comando é concluído, o thread pode atualizar a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4238-109">When the command finishes, the thread can update the user interface.</span></span> <span data-ttu-id="d4238-110">Use uma seção crítica para serializar a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="d4238-110">Use a critical section to serialize the state change.</span></span>

<span data-ttu-id="d4238-111">Alguns VTRs podem notificar o aplicativo quando o estado de transporte do dispositivo for alterado.</span><span class="sxs-lookup"><span data-stu-id="d4238-111">Some VTRs can notify the application when the device's transport state has changed.</span></span> <span data-ttu-id="d4238-112">Se o dispositivo der suporte a esse recurso, o thread de trabalho poderá aguardar a notificação.</span><span class="sxs-lookup"><span data-stu-id="d4238-112">If the device supports this feature, the worker thread can wait for the notification.</span></span> <span data-ttu-id="d4238-113">De acordo com a "especificação de subunidade do gravador/player de fita AV/C" da Associação de comércio 1394, no entanto, o comando de notificação de estado de transporte é opcional, o que significa que os dispositivos não são necessários para dar suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="d4238-113">According to the 1394 Trade Association's "AV/C Tape Recorder/Player Subunit Specification", however, the transport-state notification command is optional, meaning devices are not required to support it.</span></span> <span data-ttu-id="d4238-114">Se um dispositivo não oferecer suporte à notificação, você deverá sondar o dispositivo em intervalos periódicos para seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="d4238-114">If a device does not support notification, you should poll the device at periodic intervals for its current state.</span></span>

<span data-ttu-id="d4238-115">Esta seção descreve primeiro o mecanismo de notificação e descreve a sondagem do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4238-115">This section first describes the notification mechanism, and then describes device polling.</span></span>

<span data-ttu-id="d4238-116">Usando a notificação de estado de transporte</span><span class="sxs-lookup"><span data-stu-id="d4238-116">Using Transport State Notification</span></span>

<span data-ttu-id="d4238-117">A notificação de estado de transporte funciona fazendo com que o driver sinalize um evento quando o transporte mudar para um novo estado.</span><span class="sxs-lookup"><span data-stu-id="d4238-117">Transport state notification works by having the driver signal an event when the transport switches to a new state.</span></span> <span data-ttu-id="d4238-118">Em seu aplicativo, declare uma seção crítica, um evento e um identificador de thread.</span><span class="sxs-lookup"><span data-stu-id="d4238-118">In your application, declare a critical section, an event, and a thread handle.</span></span> <span data-ttu-id="d4238-119">A seção crítica é usada para sincronizar o estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4238-119">The critical section is used to synchronize the device state.</span></span> <span data-ttu-id="d4238-120">O evento é usado para interromper o thread de trabalho quando o aplicativo é encerrado:</span><span class="sxs-lookup"><span data-stu-id="d4238-120">The event is used to halt the worker thread when the application exits:</span></span>


```C++
HANDLE hThread = 0;
HANDLE hThreadEnd = CreateEvent(NULL, TRUE, FALSE, NULL); 
if (hThreadEnd == NULL)
{
    // Handle error.
}
CRITICAL_SECTION csIssueCmd;
InitializeCriticalSection(&cdIssueCmd);
```



<span data-ttu-id="d4238-121">Depois de criar uma instância do filtro de captura, crie o thread de trabalho:</span><span class="sxs-lookup"><span data-stu-id="d4238-121">After you create an instance of the capture filter, create the worker thread:</span></span>


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



<span data-ttu-id="d4238-122">No thread de trabalho, comece chamando o método [**IAMExtTransport:: GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) com o valor Ed \_ Notify \_ HEVENT \_ Get.</span><span class="sxs-lookup"><span data-stu-id="d4238-122">In the worker thread, start by calling the [**IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) method with the value ED\_NOTIFY\_HEVENT\_GET.</span></span> <span data-ttu-id="d4238-123">Essa chamada retorna um identificador para um evento que será sinalizado quando uma operação for concluída:</span><span class="sxs-lookup"><span data-stu-id="d4238-123">This call returns a handle to an event that will be signaled when an operation completes:</span></span>


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



<span data-ttu-id="d4238-124">Em seguida, chame **GetState** novamente e passe a notificação de alteração do modo Ed do valor \_ \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="d4238-124">Next, call **GetState** again and pass the value ED\_MODE\_CHANGE\_NOTIFY:</span></span>


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



<span data-ttu-id="d4238-125">Se o dispositivo der suporte à notificação, o método retornará o valor E \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="d4238-125">If the device supports notification, the method returns the value E\_PENDING.</span></span> <span data-ttu-id="d4238-126">(Caso contrário, você deve sondar o dispositivo, conforme descrito na próxima seção.) Supondo que o dispositivo dê suporte à notificação, o evento será sinalizado sempre que o estado do transporte VTR for alterado.</span><span class="sxs-lookup"><span data-stu-id="d4238-126">(Otherwise, you must poll device, as described in the next section.) Assuming the device supports notification, the event will be signaled whenever the state of the VTR transport changes.</span></span> <span data-ttu-id="d4238-127">Neste ponto, você pode atualizar a interface do usuário para refletir o novo estado.</span><span class="sxs-lookup"><span data-stu-id="d4238-127">At this point, you can update the user interface to reflect the new state.</span></span> <span data-ttu-id="d4238-128">Para obter a próxima notificação, redefina o identificador de eventos e chame **GetStatus** com o \_ modo Ed \_ \_ Notify notificar novamente.</span><span class="sxs-lookup"><span data-stu-id="d4238-128">To get the next notification, reset the event handle and call **GetStatus** with ED\_MODE\_CHANGE\_NOTIFY again.</span></span>

<span data-ttu-id="d4238-129">Antes de o thread de trabalho sair, libere o identificador de evento chamando **GetStatus** com a versão Flag Ed \_ notificar \_ HEVENT \_ e o endereço do identificador:</span><span class="sxs-lookup"><span data-stu-id="d4238-129">Before the worker thread exits, release the event handle by calling **GetStatus** with the flag ED\_NOTIFY\_HEVENT\_RELEASE and the address of the handle:</span></span>


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



<span data-ttu-id="d4238-130">O código a seguir mostra o procedimento de thread completo.</span><span class="sxs-lookup"><span data-stu-id="d4238-130">The following code shows the complete thread procedure.</span></span> <span data-ttu-id="d4238-131">A função UpdateTransportState é considerada uma função de aplicativo que atualiza a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4238-131">The function UpdateTransportState is assumed to be an application function that updates the user interface.</span></span> <span data-ttu-id="d4238-132">Observe que o thread aguarda dois eventos: o evento de notificação (*hNotify*) e o evento de encerramento de thread (*hThreadEnd*).</span><span class="sxs-lookup"><span data-stu-id="d4238-132">Note that the thread waits for two events: the notification event (*hNotify*) and the thread-termination event (*hThreadEnd*).</span></span> <span data-ttu-id="d4238-133">Observe também onde a seção crítica é usada para proteger a variável de estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4238-133">Also note where the critical section is used to protect the device state variable.</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    HANDLE  EventHandles[2];
    HANDLE  hNotify = NULL;
    DWORD   WaitStatus;
    LONG    State;

    // Get the notification event handle. This event will be signaled when
    // the next state-change operation completes.   
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);

    while (hThread && hNotify && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);
        // Ask the device to notify us when the state changes.
        hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
        LeaveCriticalSection(&csIssueCmd); 

        if(hr == E_PENDING)  // The device supports notification.
        {
            // Wait for the notification.
            EventHandles[0] = hNotify;
            EventHandles[1] = hThreadEnd;
            WaitStatus = WaitForMultipleObjects(2, EventHandles, FALSE, INFINITE);
            if(WAIT_OBJECT_0 == WaitStatus) 
            {
                // We got notified. Query for the new state.
                EnterCriticalSection(&csIssueCmd);  
                hr = m_pTransport->get_Mode(State);
                UpdateTransportState(State);  // Update the UI.
                LeaveCriticalSection(&m_csIssueCmd);
                ResetEvent(hNotify);
            } 
            else {
                break;  // End this thread.
            }
        } 
        else {          
            // The device does not support notification.
            PollDevice();        
        } 
    } // while

    // Cancel notification. 
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify);
    return 1; 
}
```



<span data-ttu-id="d4238-134">Use também a seção crítica ao emitir comandos para o dispositivo, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d4238-134">Also use the critical section when you issue commands to the device, as follows:</span></span>


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



<span data-ttu-id="d4238-135">Antes de o aplicativo ser encerrado, pare o thread secundário definindo o evento thread-end:</span><span class="sxs-lookup"><span data-stu-id="d4238-135">Before the application exits, halt the secondary thread by setting the thread-end event:</span></span>


```C++
if (hThread) 
{
    // Signaling this event will cause the thread to end.    
    if (SetEvent(hThreadEnd))
    {
        // Wait for it to end.
        WaitForSingleObjectEx(hThread, INFINITE, FALSE);
    }
}
CloseHandle(hThreadEnd);
CloseHandle(hThread);
```



<span data-ttu-id="d4238-136">Sondando o estado de transporte</span><span class="sxs-lookup"><span data-stu-id="d4238-136">Polling the Transport State</span></span>

<span data-ttu-id="d4238-137">Se você chamar **IAMExtTransport:: GetStatus** com o \_ sinalizador de notificação de alteração do modo Ed \_ \_ e o valor de retorno não for E \_ pendente, isso significará que o dispositivo não oferece suporte à notificação.</span><span class="sxs-lookup"><span data-stu-id="d4238-137">If you call **IAMExtTransport::GetStatus** with the ED\_MODE\_CHANGE\_NOTIFY flag and the return value is not E\_PENDING, it means the device does not support notification.</span></span> <span data-ttu-id="d4238-138">Nesse caso, você deve sondar o dispositivo para determinar seu estado.</span><span class="sxs-lookup"><span data-stu-id="d4238-138">In that case, you must poll the device to determine its state.</span></span> <span data-ttu-id="d4238-139">A *sondagem* significa simplesmente chamar o **\_ modo Get** em intervalos regulares para verificar o estado do transporte.</span><span class="sxs-lookup"><span data-stu-id="d4238-139">*Polling* simply means calling **get\_Mode** at regular intervals to check the transport state.</span></span> <span data-ttu-id="d4238-140">Você ainda deve usar um thread secundário e uma seção crítica, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d4238-140">You should still use a secondary thread and a critical section, as described earlier.</span></span> <span data-ttu-id="d4238-141">O thread consulta o dispositivo em busca de seu estado em intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="d4238-141">The thread queries the device for its state at a regular interval.</span></span> <span data-ttu-id="d4238-142">O exemplo a seguir mostra uma maneira de implementar o thread:</span><span class="sxs-lookup"><span data-stu-id="d4238-142">The following example shows one way to implement the thread:</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    LONG State;
    DWORD WaitStatus;

    while (hThread && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);  
        State = 0;
        hr = pTransport->get_Mode(&State);
        LeaveCriticalSection(&csIssueCmd); 
        UpdateTransportState(State);

        // Wait for a while, or until the thread ends. 
        WaitStatus = WaitForSingleObjectEx(hThreadEnd, 200, FALSE); 
        if (WaitStatus == WAIT_OBJECT_0)
        {
            break; // Exit thread now. 
        }
        // Otherwise, the wait timed out. Time to poll again.
    }
    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="d4238-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4238-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4238-144">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="d4238-144">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



