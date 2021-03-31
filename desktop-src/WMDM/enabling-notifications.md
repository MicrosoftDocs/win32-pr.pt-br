---
title: Habilitando notificações
description: Habilitando notificações
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Gerenciador de Dispositivos de mídia do Windows, notificações
- Gerenciador de Dispositivos, notificações
- Guia de programação, notificações
- aplicativos de desktop, notificações
- Criando aplicativos do Windows Media Gerenciador de Dispositivos, notificações
- Notificações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618356c9d63d20a8b6b14e6c99072074cfc75073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635634"
---
# <a name="enabling-notifications"></a><span data-ttu-id="47d3d-109">Habilitando notificações</span><span class="sxs-lookup"><span data-stu-id="47d3d-109">Enabling Notifications</span></span>

<span data-ttu-id="47d3d-110">O Windows Media Gerenciador de Dispositivos declara quatro interfaces que um aplicativo pode implementar em uma classe COM para receber notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="47d3d-110">Windows Media Device Manager declares four interfaces that an application can implement in a COM class to receive event notifications.</span></span> <span data-ttu-id="47d3d-111">Essas interfaces se enquadram em dois grupos, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="47d3d-111">These interfaces fall into two groups, as shown in the following table.</span></span>



| <span data-ttu-id="47d3d-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="47d3d-112">Interfaces</span></span>                                                                                                                                                | <span data-ttu-id="47d3d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="47d3d-113">Description</span></span>                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47d3d-114">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="47d3d-114">**IWMDMNotification**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | <span data-ttu-id="47d3d-115">Notifica o aplicativo quando dispositivos ou mídia de armazenamento estão conectados ou desconectados.</span><span class="sxs-lookup"><span data-stu-id="47d3d-115">Notifies the application when devices or storage media are connected or disconnected.</span></span>                                                                                         |
| [<span data-ttu-id="47d3d-116">**IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="47d3d-116">**IWMDMProgress**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [<span data-ttu-id="47d3d-117">**IWMDMProgress2**</span><span class="sxs-lookup"><span data-stu-id="47d3d-117">**IWMDMProgress2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [<span data-ttu-id="47d3d-118">**IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="47d3d-118">**IWMDMProgress3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | <span data-ttu-id="47d3d-119">Um sistema de notificação muito simples para alertar um aplicativo sobre o progresso de qualquer evento.</span><span class="sxs-lookup"><span data-stu-id="47d3d-119">A very simple notification system to alert an application about the progress of any event.</span></span> <span data-ttu-id="47d3d-120">Não é necessário que o aplicativo execute ações em resposta a essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="47d3d-120">The application is not required to take any actions in response to these messages.</span></span> |



 

<span data-ttu-id="47d3d-121">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="47d3d-121">**IWMDMNotification**</span></span>

<span data-ttu-id="47d3d-122">O **IWMDMNotification** alerta o aplicativo quando plug and Play dispositivos são conectados ou desconectados do computador, bem como quando plug and Play mídia de armazenamento (como cartões flash) são inseridas ou removidas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47d3d-122">**IWMDMNotification** alerts the application when Plug and Play devices are connected or disconnected from the computer, as well as when Plug and Play storage media (such as flash cards) are inserted or removed from the device.</span></span> <span data-ttu-id="47d3d-123">Essas notificações podem ajudar o aplicativo a atualizar sua interface do usuário para refletir as alterações.</span><span class="sxs-lookup"><span data-stu-id="47d3d-123">These notifications can help the application update its user interface to reflect changes.</span></span>

<span data-ttu-id="47d3d-124">Para receber essas notificações, seu aplicativo deve se registrar para recebê-las usando as interfaces **IConnectionPointContainer** e **IConnectionPoint** do SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="47d3d-124">In order to receive these notifications, your application must register to receive them using the Platform SDK **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="47d3d-125">Seu aplicativo deve se registrar para receber eventos quando ele for iniciado e cancelar o registro quando ele fechar.</span><span class="sxs-lookup"><span data-stu-id="47d3d-125">Your application should register to receive events when it starts up, and unregister when it closes.</span></span> <span data-ttu-id="47d3d-126">Siga estas etapas para se registrar para receber essas notificações.</span><span class="sxs-lookup"><span data-stu-id="47d3d-126">Follow these steps to register to receive these notifications.</span></span>

1.  <span data-ttu-id="47d3d-127">Consulte a interface **IWMDeviceManager** principal que você recebeu quando autenticou seu aplicativo para **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="47d3d-127">Query the main **IWMDeviceManager** interface you received when you authenticated your application for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="47d3d-128">Chame **IConnectionPointContainer:: FindConnectionPoint** para recuperar um ponto de conexão de contêiner para interfaces **IWMDMNotification** .</span><span class="sxs-lookup"><span data-stu-id="47d3d-128">Call **IConnectionPointContainer::FindConnectionPoint** to retrieve a container connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="47d3d-129">Registre-se para receber eventos chamando **IConnectionPoint:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="47d3d-129">Register to receive events by calling **IConnectionPoint::Advise**.</span></span> <span data-ttu-id="47d3d-130">Passe a classe que implementa **IWMDMNotification** e recupere um cookie, uma ID exclusiva que identifica o ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="47d3d-130">Pass in the class that implements **IWMDMNotification**, and retrieve a cookie, a unique ID that identifies your connection point.</span></span> <span data-ttu-id="47d3d-131">Isso deve ser armazenado e usado posteriormente para cancelar o registro para notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="47d3d-131">This must be stored, and used later to unregister for event notifications.</span></span>

<span data-ttu-id="47d3d-132">O código C++ a seguir demonstra como você pode se registrar para receber notificações do **IWMDMNotification**.</span><span class="sxs-lookup"><span data-stu-id="47d3d-132">The following C++ code demonstrates how you can register to receive notifications from **IWMDMNotification**.</span></span>


```C++
HRESULT CWMDMController::RegisterForNotifications()
{
    HRESULT hr = S_OK;
    CComPtr<IConnectionPointContainer> pConxnPointCont;
    CComPtr<IConnectionPoint> pIConnPoint;

    // Get the IConnectionPointContainer interface from IWMDeviceManager.
    if (SUCCEEDED (hr = m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer, (void**) & pConxnPointCont)))
    {
        // Get a connection point from the container.
        if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
        {
            // Add ourselves as a callback handler for the connection point.
            // If we succeeded, indicate that by storing the connection point ID.
            DWORD dwCookie;
            if (SUCCEEDED (hr = pIConnPoint->Advise((IUnknown*)((IWMDMNotification*)this), &dwCookie)))
            {
                m_dwNotificationCookie = dwCookie;
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="47d3d-133">Quando seu aplicativo for fechado, você deverá cancelar o registro com **IConnectionPoint** para indicar que ele não deve mais enviar notificações a você.</span><span class="sxs-lookup"><span data-stu-id="47d3d-133">When your application closes, you must unregister with **IConnectionPoint** to indicate that it should no longer send you notifications.</span></span> <span data-ttu-id="47d3d-134">Siga estas etapas para cancelar o registro para notificações:</span><span class="sxs-lookup"><span data-stu-id="47d3d-134">Follow these steps to unregister for notifications:</span></span>

1.  <span data-ttu-id="47d3d-135">Consulte a interface principal do **IWMDeviceManager** para **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="47d3d-135">Query the main **IWMDeviceManager** interface for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="47d3d-136">Obtenha um ponto de conexão para interfaces **IWMDMNotification** .</span><span class="sxs-lookup"><span data-stu-id="47d3d-136">Get a connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="47d3d-137">Cancele o registro do aplicativo para notificações de eventos chamando **IConnectionPoint:: Unadvise**, passando a ID exclusiva recebida quando você se registrou para receber eventos.</span><span class="sxs-lookup"><span data-stu-id="47d3d-137">Unregister your application for event notifications by calling **IConnectionPoint::Unadvise**, passing in the unique ID received when you registered to receive events.</span></span>

<span data-ttu-id="47d3d-138">O código C++ a seguir mostra como cancelar o registro para eventos **IWMDMNotification** quando o aplicativo é fechado.</span><span class="sxs-lookup"><span data-stu-id="47d3d-138">The following C++ code shows how to unregister for **IWMDMNotification** events when your application closes.</span></span>


```C++
HRESULT CWMDMController::UnregisterForNotifications()
{
    HRESULT hr = S_FALSE;

    // On class initialization, we initialized the handle to -1 as a flag 
    // to indicate we had not yet registered for notifications. If registration 
    // never happened, don't bother to unregister.
    if (-1 != m_dwNotificationCookie)
    {
        CComPtr<IConnectionPointContainer> pConxnPointCont;
        CComPtr<IConnectionPoint> pIConnPoint;

        // Get the connection point container from IWMDeviceManager. 
        if (SUCCEEDED (hr = 
           m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer,
           (void**) & pConxnPointCont)))
        {
            // Get a connection point from the container.
            if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
            {
                // Remove ourselves as a callback from the connection point.
                // If successful, reset the ID to a flag value.
                if (SUCCEEDED (hr = 
                    pIConnPoint->Unadvise(m_dwNotificationCookie)))
                {
                    m_dwNotificationCookie = -1;
                    hr = S_OK;
                }
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="47d3d-139">**Usando IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="47d3d-139">**Using IWMDMProgress**</span></span>

<span data-ttu-id="47d3d-140">O Windows Media Gerenciador de Dispositivos pode enviar as mensagens de status do aplicativo quando ações específicas, como transferência de conteúdo, aquisição de clock seguro e ocorrência de informações de arquivo DRM, ocorrem.</span><span class="sxs-lookup"><span data-stu-id="47d3d-140">Windows Media Device Manager can send your application status messages when specific actions, such as content transfer, secure clock acquisition, and encountering DRM file information, occur.</span></span> <span data-ttu-id="47d3d-141">Seu aplicativo pode usar essas mensagens para monitorar o status do evento ou cancelar um evento.</span><span class="sxs-lookup"><span data-stu-id="47d3d-141">Your application can use these messages to monitor the status of the event or cancel an event.</span></span> <span data-ttu-id="47d3d-142">Para usar essa interface, implemente [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)ou [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)e passe-o como um parâmetro para um método que aceitará uma mensagem de progresso.</span><span class="sxs-lookup"><span data-stu-id="47d3d-142">To use this interface, implement [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2), or [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), and pass it in as a parameter to a method that will accept a progress message.</span></span> <span data-ttu-id="47d3d-143">Observe que **IWMDMProgress3** é a interface superior porque fornece um GUID de identificação que especifica qual ação está sendo controlada.</span><span class="sxs-lookup"><span data-stu-id="47d3d-143">Note that **IWMDMProgress3** is the superior interface because it provides an identification GUID that specifies what action is being tracked.</span></span> <span data-ttu-id="47d3d-144">Os métodos de aplicativo a seguir aceitam uma interface de progresso (os métodos do provedor de serviços correspondentes devem ser capazes de enviar notificações para uma interface enviada):</span><span class="sxs-lookup"><span data-stu-id="47d3d-144">The following application methods accept a progress interface (the corresponding service provider methods should be able to send notifications to a submitted interface):</span></span>

[<span data-ttu-id="47d3d-145">**IWMDMStorageControl::D excluir**</span><span class="sxs-lookup"><span data-stu-id="47d3d-145">**IWMDMStorageControl::Delete**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[<span data-ttu-id="47d3d-146">**IWMDMStorageControl:: Insert**</span><span class="sxs-lookup"><span data-stu-id="47d3d-146">**IWMDMStorageControl::Insert**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[<span data-ttu-id="47d3d-147">**IWMDMStorageControl:: mover**</span><span class="sxs-lookup"><span data-stu-id="47d3d-147">**IWMDMStorageControl::Move**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[<span data-ttu-id="47d3d-148">**IWMDMStorageControl:: ler**</span><span class="sxs-lookup"><span data-stu-id="47d3d-148">**IWMDMStorageControl::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[<span data-ttu-id="47d3d-149">**IWMDMStorageControl:: Rename**</span><span class="sxs-lookup"><span data-stu-id="47d3d-149">**IWMDMStorageControl::Rename**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[<span data-ttu-id="47d3d-150">**IWMDMStorageControl2::Insert2**</span><span class="sxs-lookup"><span data-stu-id="47d3d-150">**IWMDMStorageControl2::Insert2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[<span data-ttu-id="47d3d-151">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="47d3d-151">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[<span data-ttu-id="47d3d-152">**IWMDMStorageGlobals:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="47d3d-152">**IWMDMStorageGlobals::Initialize**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[<span data-ttu-id="47d3d-153">**IWMDRMDeviceApp::AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="47d3d-153">**IWMDRMDeviceApp::AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)

<span data-ttu-id="47d3d-154">Exemplos de como passar uma interface em um método são fornecidos na documentação para esses métodos.</span><span class="sxs-lookup"><span data-stu-id="47d3d-154">Examples of passing an interface into a method are given in the documentation for these methods.</span></span> <span data-ttu-id="47d3d-155">Para obter exemplos de como implementar as interfaces de retorno de chamada, consulte a documentação dos métodos de **IWMDMProgress**, **IWMDMProgress2** ou **IWMDMProgress3**.</span><span class="sxs-lookup"><span data-stu-id="47d3d-155">For examples of implementing the callback interfaces, see the documentation for the methods of **IWMDMProgress**, **IWMDMProgress2**, or **IWMDMProgress3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47d3d-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47d3d-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47d3d-157">**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="47d3d-157">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





