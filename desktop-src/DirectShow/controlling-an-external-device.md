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
# <a name="controlling-an-external-device"></a>Controlando um dispositivo externo

Para controlar um dispositivo VTR (gravador de fita de vídeo), use o método [**IAMExtTransport::p UT \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) . Especifique o novo estado usando uma das constantes listadas no estado de [transporte do dispositivo](device-transport-state.md). Por exemplo, para parar o dispositivo, use o seguinte:


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Como o VTR é um dispositivo físico, normalmente há um atraso entre a emissão do comando e quando o comando é concluído. Seu aplicativo deve criar um segundo thread de trabalho que aguarde a conclusão do comando. Quando o comando é concluído, o thread pode atualizar a interface do usuário. Use uma seção crítica para serializar a alteração de estado.

Alguns VTRs podem notificar o aplicativo quando o estado de transporte do dispositivo for alterado. Se o dispositivo der suporte a esse recurso, o thread de trabalho poderá aguardar a notificação. De acordo com a "especificação de subunidade do gravador/player de fita AV/C" da Associação de comércio 1394, no entanto, o comando de notificação de estado de transporte é opcional, o que significa que os dispositivos não são necessários para dar suporte a ele. Se um dispositivo não oferecer suporte à notificação, você deverá sondar o dispositivo em intervalos periódicos para seu estado atual.

Esta seção descreve primeiro o mecanismo de notificação e descreve a sondagem do dispositivo.

Usando a notificação de estado de transporte

A notificação de estado de transporte funciona fazendo com que o driver sinalize um evento quando o transporte mudar para um novo estado. Em seu aplicativo, declare uma seção crítica, um evento e um identificador de thread. A seção crítica é usada para sincronizar o estado do dispositivo. O evento é usado para interromper o thread de trabalho quando o aplicativo é encerrado:


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



Depois de criar uma instância do filtro de captura, crie o thread de trabalho:


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



No thread de trabalho, comece chamando o método [**IAMExtTransport:: GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) com o valor Ed \_ Notify \_ HEVENT \_ Get. Essa chamada retorna um identificador para um evento que será sinalizado quando uma operação for concluída:


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



Em seguida, chame **GetState** novamente e passe a notificação de alteração do modo Ed do valor \_ \_ \_ :


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Se o dispositivo der suporte à notificação, o método retornará o valor E \_ pendente. (Caso contrário, você deve sondar o dispositivo, conforme descrito na próxima seção.) Supondo que o dispositivo dê suporte à notificação, o evento será sinalizado sempre que o estado do transporte VTR for alterado. Neste ponto, você pode atualizar a interface do usuário para refletir o novo estado. Para obter a próxima notificação, redefina o identificador de eventos e chame **GetStatus** com o \_ modo Ed \_ \_ Notify notificar novamente.

Antes de o thread de trabalho sair, libere o identificador de evento chamando **GetStatus** com a versão Flag Ed \_ notificar \_ HEVENT \_ e o endereço do identificador:


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



O código a seguir mostra o procedimento de thread completo. A função UpdateTransportState é considerada uma função de aplicativo que atualiza a interface do usuário. Observe que o thread aguarda dois eventos: o evento de notificação (*hNotify*) e o evento de encerramento de thread (*hThreadEnd*). Observe também onde a seção crítica é usada para proteger a variável de estado do dispositivo.


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



Use também a seção crítica ao emitir comandos para o dispositivo, da seguinte maneira:


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Antes de o aplicativo ser encerrado, pare o thread secundário definindo o evento thread-end:


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



Sondando o estado de transporte

Se você chamar **IAMExtTransport:: GetStatus** com o \_ sinalizador de notificação de alteração do modo Ed \_ \_ e o valor de retorno não for E \_ pendente, isso significará que o dispositivo não oferece suporte à notificação. Nesse caso, você deve sondar o dispositivo para determinar seu estado. A *sondagem* significa simplesmente chamar o **\_ modo Get** em intervalos regulares para verificar o estado do transporte. Você ainda deve usar um thread secundário e uma seção crítica, conforme descrito anteriormente. O thread consulta o dispositivo em busca de seu estado em intervalos regulares. O exemplo a seguir mostra uma maneira de implementar o thread:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



