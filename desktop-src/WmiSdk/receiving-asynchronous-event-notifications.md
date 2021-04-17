---
description: A notificação de eventos assíncronos é uma técnica que permite que um aplicativo monitore constantemente os eventos sem monopolizar os recursos do sistema.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Recebendo notificações de eventos assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748889"
---
# <a name="receiving-asynchronous-event-notifications"></a><span data-ttu-id="86a19-103">Recebendo notificações de eventos assíncronos</span><span class="sxs-lookup"><span data-stu-id="86a19-103">Receiving Asynchronous Event Notifications</span></span>

<span data-ttu-id="86a19-104">A notificação de eventos assíncronos é uma técnica que permite que um aplicativo monitore constantemente os eventos sem monopolizar os recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="86a19-104">Asynchronous event notification is a technique that allows an application to constantly monitor events without monopolizing system resources.</span></span> <span data-ttu-id="86a19-105">As notificações de eventos assíncronos têm as mesmas limitações de segurança que outras chamadas assíncronas têm.</span><span class="sxs-lookup"><span data-stu-id="86a19-105">Asynchronous event notifications have the same security limitations that other asynchronous calls have.</span></span> <span data-ttu-id="86a19-106">Em vez disso, você pode fazer chamadas semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="86a19-106">You can make semisynchronous calls instead.</span></span> <span data-ttu-id="86a19-107">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="86a19-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="86a19-108">A fila de eventos assíncronos roteados para um cliente tem o potencial de crescer excepcionalmente grande.</span><span class="sxs-lookup"><span data-stu-id="86a19-108">The queue of asynchronous events routed to a client has the potential to grow exceptionally large.</span></span> <span data-ttu-id="86a19-109">Portanto, o WMI implementa uma política de todo o sistema para evitar ficar sem memória.</span><span class="sxs-lookup"><span data-stu-id="86a19-109">Therefore, WMI implements a system-wide policy to avoid running out of memory.</span></span> <span data-ttu-id="86a19-110">O WMI torna os eventos lentos ou começa a descartar eventos da fila quando a fila cresce além de um determinado tamanho.</span><span class="sxs-lookup"><span data-stu-id="86a19-110">WMI either slows down events, or starts dropping events from the queue when the queue grows past a certain size.</span></span>

<span data-ttu-id="86a19-111">O WMI usa as propriedades [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) e [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) da classe [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para definir limites para evitar memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="86a19-111">WMI uses the [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) and [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) properties of the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) class to set limits on out-of-memory avoidance.</span></span> <span data-ttu-id="86a19-112">O valor mínimo indica quando o WMI deve iniciar a lentidão na notificação de eventos e o valor máximo indica quando iniciar a descartar eventos.</span><span class="sxs-lookup"><span data-stu-id="86a19-112">The minimum value indicates when WMI should start slowing event notification, and the maximum value indicates when to start dropping events.</span></span> <span data-ttu-id="86a19-113">Os valores padrão para os limites baixo e alto são 1 milhão (10 MB) e 2 milhões (20 MB).</span><span class="sxs-lookup"><span data-stu-id="86a19-113">The default values for the low and high thresholds are 1000000 (10 MB) and 2000000 (20 MB).</span></span> <span data-ttu-id="86a19-114">Além disso, você pode definir a propriedade [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para descrever a quantidade de tempo que o WMI deve aguardar antes de remover eventos.</span><span class="sxs-lookup"><span data-stu-id="86a19-114">In addition, you can set the [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property to describe the amount of time WMI should wait before dropping events.</span></span> <span data-ttu-id="86a19-115">O valor padrão para **MaxWaitOnEvents** é 2000 ou 2 segundos.</span><span class="sxs-lookup"><span data-stu-id="86a19-115">The default value for **MaxWaitOnEvents** is 2000, or 2 seconds.</span></span>

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a><span data-ttu-id="86a19-116">Recebendo notificações de eventos assíncronos no VBScript</span><span class="sxs-lookup"><span data-stu-id="86a19-116">Receiving Asynchronous Event Notifications in VBScript</span></span>

<span data-ttu-id="86a19-117">As chamadas de script para receber notificações de eventos são essencialmente as mesmas que todas as chamadas assíncronas com os mesmos problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="86a19-117">The scripting calls to receive event notifications are essentially the same as all asynchronous calls with the same security issues.</span></span> <span data-ttu-id="86a19-118">Para obter mais informações, consulte [fazendo uma chamada assíncrona com o VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="86a19-118">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="86a19-119">**Para receber notificações de eventos assíncronas no VBScript**</span><span class="sxs-lookup"><span data-stu-id="86a19-119">**To receive asynchronous event notifications in VBScript**</span></span>

1.  <span data-ttu-id="86a19-120">Crie um objeto de coletor chamando [WScript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e especificando o ProgID de "WbemScripting" e o tipo de objeto de [**SWbemSink**](swbemsink.md).</span><span class="sxs-lookup"><span data-stu-id="86a19-120">Create a sink object by calling [WScript.CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and specifying the progid of "WbemScripting" and the object type of [**SWbemSink**](swbemsink.md).</span></span> <span data-ttu-id="86a19-121">O objeto Sink recebe as notificações.</span><span class="sxs-lookup"><span data-stu-id="86a19-121">The sink object receives the notifications.</span></span>
2.  <span data-ttu-id="86a19-122">Escreva uma sub-rotina para cada evento que você deseja manipular.</span><span class="sxs-lookup"><span data-stu-id="86a19-122">Write a subroutine for each event you want to handle.</span></span> <span data-ttu-id="86a19-123">A tabela a seguir lista os eventos [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="86a19-123">The following table lists the [**SWbemSink**](swbemsink.md) events.</span></span>

    

    | <span data-ttu-id="86a19-124">Evento</span><span class="sxs-lookup"><span data-stu-id="86a19-124">Event</span></span>                                            | <span data-ttu-id="86a19-125">Significado</span><span class="sxs-lookup"><span data-stu-id="86a19-125">Meaning</span></span>                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="86a19-126">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="86a19-126">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="86a19-127">Relata os retornos de um objeto para o coletor.</span><span class="sxs-lookup"><span data-stu-id="86a19-127">Reports the returns of an object to the sink.</span></span> <span data-ttu-id="86a19-128">O uso dessa chamada retorna um objeto cada vez até que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="86a19-128">Using this call returns one object each time until the operation is complete.</span></span>     |
    | [<span data-ttu-id="86a19-129">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="86a19-129">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="86a19-130">Relata quando uma chamada assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="86a19-130">Reports when an asynchronous call is complete.</span></span> <span data-ttu-id="86a19-131">Esse evento nunca ocorrerá se a operação estiver indefinida.</span><span class="sxs-lookup"><span data-stu-id="86a19-131">This event never occurs if the operation is indefinite.</span></span>                          |
    | [<span data-ttu-id="86a19-132">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="86a19-132">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="86a19-133">Relata a conclusão de uma operação Put assíncrona.</span><span class="sxs-lookup"><span data-stu-id="86a19-133">Reports the completion of an asynchronous put operation.</span></span> <span data-ttu-id="86a19-134">Esse evento retorna o caminho do objeto da instância ou da classe salva.</span><span class="sxs-lookup"><span data-stu-id="86a19-134">This event returns the object path of the instance or the saved class.</span></span> |
    | [<span data-ttu-id="86a19-135">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="86a19-135">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="86a19-136">Relata o status de uma chamada assíncrona que está em andamento.</span><span class="sxs-lookup"><span data-stu-id="86a19-136">Reports the status of an asynchronous call that is in progress.</span></span> <span data-ttu-id="86a19-137">Nem todos os provedores dão suporte a relatórios de progresso provisório.</span><span class="sxs-lookup"><span data-stu-id="86a19-137">Not all providers support interim progress reports.</span></span>             |
    | [<span data-ttu-id="86a19-138">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="86a19-138">**Cancel**</span></span>](swbemsink-cancel.md)               | <span data-ttu-id="86a19-139">Cancela todas as operações assíncronas pendentes associadas a este coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="86a19-139">Cancels all of the outstanding asynchronous operations associated with this object sink.</span></span>                                        |

    

     

<span data-ttu-id="86a19-140">O exemplo de código VBScript a seguir notifica a exclusão de processos com um intervalo de sondagem de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="86a19-140">The following VBScript code example notifies the deletion of processes with a 10 second polling interval.</span></span> <span data-ttu-id="86a19-141">Nesse script, o coletor de sub-rotina \_ OnObjectReady manipula a ocorrência do evento.</span><span class="sxs-lookup"><span data-stu-id="86a19-141">In this script, the subroutine SINK\_OnObjectReady handles the event occurrence.</span></span> <span data-ttu-id="86a19-142">No exemplo, o objeto Sink é denominado "Sink", no entanto, você pode nomear esse objeto conforme escolher.</span><span class="sxs-lookup"><span data-stu-id="86a19-142">In the example, the sink object is named "Sink", however you can name this object as you choose.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a><span data-ttu-id="86a19-143">Recebendo notificações de eventos assíncronos em C++</span><span class="sxs-lookup"><span data-stu-id="86a19-143">Receiving Asynchronous Event Notifications in C++</span></span>

<span data-ttu-id="86a19-144">Para executar uma notificação assíncrona, você cria um thread separado exclusivamente para monitorar e receber eventos de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="86a19-144">To perform asynchronous notification, you create a separate thread solely to monitor and receive events from Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="86a19-145">Quando esse thread recebe uma mensagem, o thread notifica seu aplicativo principal.</span><span class="sxs-lookup"><span data-stu-id="86a19-145">When that thread receives a message, the thread notifies your main application.</span></span>

<span data-ttu-id="86a19-146">Ao dedicar um thread separado, você permite que seu processo principal execute outras atividades enquanto aguarda a chegada de um evento.</span><span class="sxs-lookup"><span data-stu-id="86a19-146">By dedicating a separate thread, you permit your main process to perform other activities while waiting for an event to arrive.</span></span> <span data-ttu-id="86a19-147">A entrega assíncrona de notificações melhora o desempenho, mas pode fornecer menos segurança do que o desejado.</span><span class="sxs-lookup"><span data-stu-id="86a19-147">Asynchronous delivery of notifications improves performance but may provide less security than you want.</span></span> <span data-ttu-id="86a19-148">Em C++, você tem a opção de usar a interface [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) ou executar verificações de acesso em descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="86a19-148">In C++, you have the option of using the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface or performing access checks on security descriptors.</span></span> <span data-ttu-id="86a19-149">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="86a19-149">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="86a19-150">**Para configurar notificações de eventos assíncronos**</span><span class="sxs-lookup"><span data-stu-id="86a19-150">**To set up asynchronous event notifications**</span></span>

1.  <span data-ttu-id="86a19-151">Antes de inicializar qualquer notificação assíncrona, verifique se os parâmetros de prevenção de memória insuficiente estão definidos corretamente no [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span><span class="sxs-lookup"><span data-stu-id="86a19-151">Before initializing any asynchronous notifications, ensure your out-of-memory avoidance parameters are set correctly in [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span></span>

2.  <span data-ttu-id="86a19-152">Determine que tipo de eventos você deseja receber.</span><span class="sxs-lookup"><span data-stu-id="86a19-152">Determine what kind of events you want to receive.</span></span>

    <span data-ttu-id="86a19-153">O WMI dá suporte a eventos intrínsecos e extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="86a19-153">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="86a19-154">Um evento intrínseco é um evento predefinido pelo WMI, enquanto um evento extrínsecos é um evento definido por um provedor de terceiros.</span><span class="sxs-lookup"><span data-stu-id="86a19-154">An intrinsic event is an event predefined by WMI, whereas an extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="86a19-155">Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="86a19-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="86a19-156">O procedimento a seguir descreve como receber notificações de eventos assíncronos em C++.</span><span class="sxs-lookup"><span data-stu-id="86a19-156">The following procedure describes how to receive asynchronous event notifications in C++.</span></span>

<span data-ttu-id="86a19-157">**Para receber notificações de eventos assíncronos em C++**</span><span class="sxs-lookup"><span data-stu-id="86a19-157">**To receive asynchronous event notifications in C++**</span></span>

1.  <span data-ttu-id="86a19-158">Configure seu aplicativo com chamadas para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="86a19-158">Set up your application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="86a19-159">Chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) inicializa com, enquanto [**COINITIALIZESECURITY**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) concede ao WMI a permissão para chamar o processo do consumidor.</span><span class="sxs-lookup"><span data-stu-id="86a19-159">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) initializes COM, while [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) grants WMI the permission to call into the process of the consumer.</span></span> <span data-ttu-id="86a19-160">A função **CoInitializeEx** também concede a capacidade de programar um aplicativo multithread, que é necessário para a notificação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="86a19-160">The **CoInitializeEx** function also grants you the ability to program a multithreaded application, which is necessary for asynchronous notification.</span></span> <span data-ttu-id="86a19-161">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="86a19-161">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="86a19-162">O código neste tópico requer as seguintes referências e \# inclui instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="86a19-162">The code in this topic requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    <span data-ttu-id="86a19-163">O exemplo de código a seguir descreve como configurar o consumidor de evento temporário com chamadas para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="86a19-163">The following code example describes how to set up the temporary event consumer with calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  <span data-ttu-id="86a19-164">Crie um objeto de coletor por meio da interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="86a19-164">Create a sink object through the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="86a19-165">O WMI usa [**IWbemObjectSink**](iwbemobjectsink.md) para enviar notificações de eventos e relatar o status em uma operação assíncrona ou notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="86a19-165">WMI uses [**IWbemObjectSink**](iwbemobjectsink.md) to send event notifications and to report status on an asynchronous operation or event notification.</span></span>

3.  <span data-ttu-id="86a19-166">Registre seu consumidor de evento com uma chamada para o método [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="86a19-166">Register your event consumer with a call to the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span>

    <span data-ttu-id="86a19-167">Certifique-se de que o parâmetro *pResponseHandler* aponta para o objeto de coletor criado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="86a19-167">Make sure that the *pResponseHandler* parameter points to the sink object created in the preceding step.</span></span>

    <span data-ttu-id="86a19-168">A finalidade do registro é receber apenas as notificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="86a19-168">The purpose of registration is to receive only the required notifications.</span></span> <span data-ttu-id="86a19-169">O recebimento de notificações supérfluas desperdiça o tempo de processamento e de entrega; e não usa a capacidade de filtragem do WMI para o potencial máximo.</span><span class="sxs-lookup"><span data-stu-id="86a19-169">Receiving superfluous notifications wastes processing and delivery time; and does not use the filtering ability of WMI to the fullest potential.</span></span>

    <span data-ttu-id="86a19-170">No entanto, um consumidor temporário pode receber mais de um tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="86a19-170">However, a temporary consumer can receive more than one type of event.</span></span> <span data-ttu-id="86a19-171">Nesse caso, um consumidor temporário deve fazer chamadas separadas para [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) para cada tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="86a19-171">In this case, a temporary consumer must make separate calls to [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) for each event type.</span></span> <span data-ttu-id="86a19-172">Por exemplo, um consumidor pode exigir notificação quando novos processos são criados (um evento de criação de instância ou [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) e para alterações em determinadas chaves do registro (um evento de registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span><span class="sxs-lookup"><span data-stu-id="86a19-172">For example, a consumer might require notification when new processes are created (an instance creation event or [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) and for changes to certain registry keys (a registry event such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span></span> <span data-ttu-id="86a19-173">Portanto, o consumidor faz uma chamada para [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) para registrar eventos de criação de instância e outra chamada para **ExecNotificationQueryAsync** para registrar eventos de registro.</span><span class="sxs-lookup"><span data-stu-id="86a19-173">Therefore, the consumer makes one call to [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) to register for instance creation events and another call to **ExecNotificationQueryAsync** to register for registry events.</span></span>

    <span data-ttu-id="86a19-174">Se você optar por criar um consumidor de eventos que se registra para vários eventos, evite registrar várias classes com o mesmo coletor.</span><span class="sxs-lookup"><span data-stu-id="86a19-174">If you choose to create an event consumer that registers for multiple events, you should avoid registering multiple classes with the same sink.</span></span> <span data-ttu-id="86a19-175">Em vez disso, use um coletor separado para cada classe de evento registrado.</span><span class="sxs-lookup"><span data-stu-id="86a19-175">Instead, use a separate sink for each class of registered event.</span></span> <span data-ttu-id="86a19-176">Ter um coletor dedicado simplifica o processamento e ajuda na manutenção, permitindo que você cancele um registro sem afetar os outros.</span><span class="sxs-lookup"><span data-stu-id="86a19-176">Having a dedicated sink simplifies processing and aids in maintenance, allowing you to cancel one registration without affecting the others.</span></span>

4.  <span data-ttu-id="86a19-177">Execute as atividades necessárias em seu consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="86a19-177">Perform any necessary activities in your event consumer.</span></span>

    <span data-ttu-id="86a19-178">Essa etapa deve conter a maior parte do seu código e incluir atividades como exibir eventos em uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="86a19-178">This step should contain most of your code and include such activities as displaying events to a user interface.</span></span>

5.  <span data-ttu-id="86a19-179">Quando terminar, cancele o registro do consumidor de evento temporário com uma chamada para o evento [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="86a19-179">When finished, unregister the temporary event consumer with a call to the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) event.</span></span>

    <span data-ttu-id="86a19-180">Independentemente de a chamada para [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) ter êxito ou falhar, não exclua o objeto de coletor até que a contagem de referência de objeto chegue a zero.</span><span class="sxs-lookup"><span data-stu-id="86a19-180">Regardless of whether the call to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) succeeds or fails, do not delete the sink object until the object reference count reaches zero.</span></span> <span data-ttu-id="86a19-181">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="86a19-181">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 
