---
title: Registrando um retorno de chamada COM
description: Em vez de sondar alterações no status de um trabalho, você pode se registrar para receber notificações quando o status do trabalho for alterado.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- transferir BITS de trabalho, notificação de eventos
- Registrando para BITS de notificação de eventos
- BITS de notificação de eventos
- BITS de notificação de eventos, retornos de chamada
- BITS de eventos de notificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294246"
---
# <a name="registering-a-com-callback"></a><span data-ttu-id="6414c-108">Registrando um retorno de chamada COM</span><span class="sxs-lookup"><span data-stu-id="6414c-108">Registering a COM Callback</span></span>

<span data-ttu-id="6414c-109">Em vez de [sondar](polling-for-the-status-of-the-job.md) alterações no status de um trabalho, você pode se registrar para receber notificações quando o status do trabalho for alterado.</span><span class="sxs-lookup"><span data-stu-id="6414c-109">Instead of [polling](polling-for-the-status-of-the-job.md) for changes in the status of a job, you can register to receive notification when the job's status changes.</span></span> <span data-ttu-id="6414c-110">Para receber a notificação, você deve implementar a interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) .</span><span class="sxs-lookup"><span data-stu-id="6414c-110">To receive notification, you must implement the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface.</span></span> <span data-ttu-id="6414c-111">A interface contém os seguintes métodos que o BITS chama, dependendo do seu registro:</span><span class="sxs-lookup"><span data-stu-id="6414c-111">The interface contains the following methods that BITS calls, depending on your registration:</span></span>

-   [<span data-ttu-id="6414c-112">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="6414c-112">**JobTransferred**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [<span data-ttu-id="6414c-113">**JobError**</span><span class="sxs-lookup"><span data-stu-id="6414c-113">**JobError**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [<span data-ttu-id="6414c-114">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="6414c-114">**JobModification**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [<span data-ttu-id="6414c-115">**Filetransferiu**</span><span class="sxs-lookup"><span data-stu-id="6414c-115">**FileTransferred**</span></span>](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

<span data-ttu-id="6414c-116">Para obter um exemplo que implementa a interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , consulte o código de exemplo no tópico da interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="6414c-116">For an example that implements the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface, see the example code in the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface topic.</span></span>

<span data-ttu-id="6414c-117">A interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) fornece notificação quando um arquivo é transferido.</span><span class="sxs-lookup"><span data-stu-id="6414c-117">The [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface provides notification when a file is transferred.</span></span> <span data-ttu-id="6414c-118">Normalmente, você usa esse método para validar o arquivo, de modo que o arquivo esteja disponível para os pares baixarem; caso contrário, o arquivo não estará disponível para os pares até que você chame o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="6414c-118">Typically, you use this method to validate the file, so that the file is available for peers to download; otherwise, the file is not available to peers until you call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="6414c-119">Para validar o arquivo, chame o método [**IBackgroundCopyFile3:: Setvalidable**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .</span><span class="sxs-lookup"><span data-stu-id="6414c-119">To validate the file, call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method.</span></span>

<span data-ttu-id="6414c-120">Há dois métodos para registrar um retorno de chamada COM: registrar um objeto de retorno de chamada ou registrar uma ID de classe de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6414c-120">There are two methods for registering a COM callback: registering a callback object, or registering a callback class ID.</span></span> <span data-ttu-id="6414c-121">Usar um objeto de retorno de chamada é mais simples e uma sobrecarga mais baixa; usar um CLSID de retorno de chamada é mais confiável, mas mais complicado.</span><span class="sxs-lookup"><span data-stu-id="6414c-121">Using a callback object is simpler and lower overhead; using a callback CLSID is more reliable, but more complicated.</span></span> <span data-ttu-id="6414c-122">Você pode registrar um, ambos ou nenhum dos BITS usará um objeto de retorno de chamada, se houver, e ainda poderá ser chamado e voltará a criar uma instância de um novo objeto com base em uma ID de classe fornecida se isso falhar.</span><span class="sxs-lookup"><span data-stu-id="6414c-122">You can register either, both, or neither – BITS will use a callback object if one exists and can still be called, and will fall back to instantiating a new object based on a provided class ID if that fails.</span></span>

### <a name="registering-a-callback-object"></a><span data-ttu-id="6414c-123">Registrando um objeto de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="6414c-123">Registering a Callback Object</span></span>

<span data-ttu-id="6414c-124">Para registrar sua implementação com o BITS, chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) .</span><span class="sxs-lookup"><span data-stu-id="6414c-124">To register your implementation with BITS, call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method.</span></span> <span data-ttu-id="6414c-125">Para especificar quais métodos são chamados por BITS, chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).</span><span class="sxs-lookup"><span data-stu-id="6414c-125">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)method.</span></span>

<span data-ttu-id="6414c-126">A interface de notificação torna-se inválida quando o aplicativo é encerrado; O BITS não mantém a interface de notificação.</span><span class="sxs-lookup"><span data-stu-id="6414c-126">The notification interface becomes invalid when your application terminates; BITS does not persist the notify interface.</span></span> <span data-ttu-id="6414c-127">Como resultado, o processo de inicialização do aplicativo deve registrar os trabalhos existentes para os quais você deseja receber a notificação.</span><span class="sxs-lookup"><span data-stu-id="6414c-127">As a result, your application's initialization process should register existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="6414c-128">Se você precisar capturar informações de estado e de progresso ocorridas desde a última vez em que seu aplicativo foi executado, pesquise informações de estado e progresso durante a inicialização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6414c-128">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="6414c-129">Antes de sair, seu aplicativo deve limpar o ponteiro de interface de retorno de chamada (**SetNotifyInterface (NULL)**).</span><span class="sxs-lookup"><span data-stu-id="6414c-129">Before exiting, your application should clear the callback interface pointer (**SetNotifyInterface(NULL)**).</span></span> <span data-ttu-id="6414c-130">É mais eficiente limpar o ponteiro de retorno de chamada do que permitir que o BITS descubra que ele não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="6414c-130">It is more efficient to clear the callback pointer than to let BITS discover that it is no longer valid.</span></span>

<span data-ttu-id="6414c-131">Observe que, se mais de um aplicativo chamar o método [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para definir a interface de notificação para o trabalho, o último aplicativo para chamar o método **SetNotifyInterface** é aquele que receberá notificações – os outros aplicativos não receberão notificações.</span><span class="sxs-lookup"><span data-stu-id="6414c-131">Note that if more than one application calls the [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to set the notification interface for the job, the last application to call the **SetNotifyInterface** method is the one that will receive notifications—the other applications will not receive notifications.</span></span>

<span data-ttu-id="6414c-132">O exemplo a seguir mostra como registrar-se para notificações.</span><span class="sxs-lookup"><span data-stu-id="6414c-132">The following example shows how to register for notifications.</span></span> <span data-ttu-id="6414c-133">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.</span><span class="sxs-lookup"><span data-stu-id="6414c-133">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span> <span data-ttu-id="6414c-134">Para obter detalhes sobre a classe de exemplo CNotifyInterface usada no exemplo a seguir, consulte a interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="6414c-134">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a><span data-ttu-id="6414c-135">Registrando um CLSID de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="6414c-135">Registering a Callback CLSID</span></span>

<span data-ttu-id="6414c-136">Para registrar um CLSID de retorno de chamada com BITS, chame o método [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) com a propriedade da **propriedade de trabalho do bits \_ \_ \_ \_ CLSID de notificação** .</span><span class="sxs-lookup"><span data-stu-id="6414c-136">To register a callback CLSID with BITS, call the [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) method with the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** PropertyId.</span></span> <span data-ttu-id="6414c-137">Para especificar quais métodos são chamados por BITS, chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .</span><span class="sxs-lookup"><span data-stu-id="6414c-137">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method.</span></span>

<span data-ttu-id="6414c-138">Você deve garantir que o CLSID de notificação esteja registrado em um servidor COM fora do processo antes de registrar o CLSID com um trabalho do BITS.</span><span class="sxs-lookup"><span data-stu-id="6414c-138">You must ensure that the notification CLSID is registered to an out-of-process COM server prior to registering the CLSID with a BITS job.</span></span> <span data-ttu-id="6414c-139">A implementação de um [servidor com](/windows/desktop/com/com-server-responsibilities) é significativamente mais complicada do que definir e passar um objeto de retorno de chamada, mas oferece várias vantagens importantes.</span><span class="sxs-lookup"><span data-stu-id="6414c-139">Implementing a [COM server](/windows/desktop/com/com-server-responsibilities) is significantly more complicated than defining and passing a callback object, but offers several important advantages.</span></span> <span data-ttu-id="6414c-140">Um servidor COM permite que o BITS mantenha a associação entre um trabalho do BITS e o código do aplicativo entre reinicializações do sistema e para trabalhos grandes ou de longa duração.</span><span class="sxs-lookup"><span data-stu-id="6414c-140">A COM server allows BITS to maintain the association between a BITS job and your application’s code across system reboots, and for large or long-lived jobs.</span></span> <span data-ttu-id="6414c-141">Um servidor COM também permite que seu aplicativo seja desligado completamente enquanto o BITS continua executando transferências em segundo plano, o que pode melhorar o uso de bateria, CPU e memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="6414c-141">A COM server also allows your application to shut down completely while BITS continues executing transfers in the background, which can improve battery, CPU, and memory usage of the system.</span></span>

<span data-ttu-id="6414c-142">Para fornecer uma notificação que você registrou para receber, o BITS primeiro tenta chamar o método correspondente de qualquer objeto de retorno de chamada existente que você possa ter anexado.</span><span class="sxs-lookup"><span data-stu-id="6414c-142">To provide a notification you have registered to receive, BITS first attempts to call the corresponding method of any existing callback object you may have attached.</span></span> <span data-ttu-id="6414c-143">Se não houver nenhum objeto existente ou se esse objeto existente tiver sido desconectado (normalmente como resultado do encerramento do aplicativo), o BITS chamará CoCreateInstance usando o CLSID de notificação para criar uma instância de um novo objeto de retorno de chamada e usará esse objeto para quaisquer retornos de chamada adicionais até que ele se torne desconectado ou seja substituído por uma nova chamada para [**método ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span><span class="sxs-lookup"><span data-stu-id="6414c-143">If there is no existing object, or if that existing object has become disconnected (typically as a result of your application terminating), BITS will call CoCreateInstance using the notification CLSID to instantiate a new callback object, and will use that object for any further callbacks until it becomes disconnected or it is replaced by a new call to [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span></span>

<span data-ttu-id="6414c-144">Ao contrário dos objetos de retorno de chamada, o CLSID de retorno de chamada será mantido junto com seus trabalhos BITS correspondentes se o serviço BITS ou o sistema forem desligados e reiniciados.</span><span class="sxs-lookup"><span data-stu-id="6414c-144">Unlike callback objects, callback CLSID are persisted alongside their corresponding BITS job(s) if the BITS service or the system are shut down and restarted.</span></span> <span data-ttu-id="6414c-145">Seu aplicativo pode limpar qualquer CLSID de notificação definido anteriormente antes de sair (ou em qualquer outro momento), passando um novo CLSID de notificação de GUID \_ NULL, mas seu aplicativo pode preferir deixar o CLSID de notificação registrado se o seu aplicativo tiver se registrado para fazer com que o com o inicie em resposta a solicitações de CoCreateInstance para seu CLSID.</span><span class="sxs-lookup"><span data-stu-id="6414c-145">Your application may clear any previously-set notification CLSID before exiting (or at any other time) by passing a new notification CLSID of GUID\_NULL, but your application may prefer to leave the notification CLSID registered if your application has registered to have COM start it in response to CoCreateInstance requests for your CLSID.</span></span> <span data-ttu-id="6414c-146">Observe que, se mais de um aplicativo definir o chama a propriedade **CLSID de notificação de \_ Propriedade do trabalho \_ \_ \_ bits** , o último CLSID a ser definido será aquele que o bits usará para instanciar objetos de retorno de chamada – os outros CLSIDs não serão instanciados.</span><span class="sxs-lookup"><span data-stu-id="6414c-146">Note that if more than one application sets the calls the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** property, the last CLSID to be set is the one that BITS will use to instantiate callback objects – the other CLSIDs will not be instantiated.</span></span> <span data-ttu-id="6414c-147">Da mesma forma, se um aplicativo registra um CLSID e outro registra um objeto de retorno de chamada, as regras usuais para o objeto de retorno de chamada estão se aplicando e o CLSID não será usado, a menos que o objeto de retorno de chamada seja limpo ou se torne desconectado.</span><span class="sxs-lookup"><span data-stu-id="6414c-147">Similarly, if one application registers a CLSID and another registers a callback object, the usual rules for the callback object taking precedence apply, and the CLSID will not be used unless the callback object is cleared or becomes disconnected.</span></span>

<span data-ttu-id="6414c-148">O exemplo a seguir mostra como registrar-se para notificações de CLSID.</span><span class="sxs-lookup"><span data-stu-id="6414c-148">The following example shows how to register for CLSID notifications.</span></span> <span data-ttu-id="6414c-149">O exemplo supõe que o ponteiro de interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) é válido e que seu aplicativo já foi registrado como um servidor com fora do processo que implementa a classe CNotifyInterface.</span><span class="sxs-lookup"><span data-stu-id="6414c-149">The example assumes the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface pointer is valid, and that your application has already registered as an out-of-process COM Server which implements the CNotifyInterface class.</span></span> <span data-ttu-id="6414c-150">Para obter detalhes sobre a classe de exemplo CNotifyInterface usada no exemplo a seguir, consulte a interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="6414c-150">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 