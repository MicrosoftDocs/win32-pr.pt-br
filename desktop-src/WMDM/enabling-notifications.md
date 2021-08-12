---
title: Habilitando notificações
description: Habilitando notificações
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows Mídia Gerenciador de Dispositivos, notificações
- Gerenciador de Dispositivos,notificações
- guia de programação, notificações
- aplicativos da área de trabalho, notificações
- criando Windows de Gerenciador de Dispositivos de mídia, notificações
- Notificações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ab1b71482db78571f141b7042d8abc926b0d79ca2f487ee7dc961396993b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585059"
---
# <a name="enabling-notifications"></a>Habilitando notificações

Windows A Gerenciador de Dispositivos de mídia declara quatro interfaces que um aplicativo pode implementar em uma classe COM para receber notificações de eventos. Essas interfaces se enquadram em dois grupos, conforme mostrado na tabela a seguir.



| Interfaces                                                                                                                                                | Descrição                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Notifica o aplicativo quando dispositivos ou mídia de armazenamento estão conectados ou desconectados.                                                                                         |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Um sistema de notificação muito simples para alertar um aplicativo sobre o progresso de qualquer evento. O aplicativo não é necessário para tomar nenhuma ação em resposta a essas mensagens. |



 

**IWMDMNotification**

**IWMDMNotification** alerta o aplicativo quando Plug and Play dispositivos estão conectados ou desconectados do computador Plug and Play, bem como quando uma mídia de armazenamento (como cartões flash) é inserida ou removida do dispositivo. Essas notificações podem ajudar o aplicativo a atualizar sua interface do usuário para refletir as alterações.

Para receber essas notificações, seu aplicativo deve se registrar para recebê-las usando as interfaces **IConnectionPointContainer** e **IConnectionPoint** do SDK da Plataforma. Seu aplicativo deve se registrar para receber eventos quando ele é iniciado e encerrar o registro quando ele for fechado. Siga estas etapas para se registrar para receber essas notificações.

1.  Consulte a interface **IWMDeviceManager** principal que você recebeu ao autenticar seu aplicativo **para IConnectionPointContainer.**
2.  Chame **IConnectionPointContainer::FindConnectionPoint** para recuperar um ponto de conexão de contêiner para interfaces **IWMDMNotification.**
3.  Registre-se para receber eventos chamando **IConnectionPoint::Advise**. Passe a classe que implementa **IWMDMNotification** e recupere um cookie, uma ID exclusiva que identifica o ponto de conexão. Isso deve ser armazenado e usado posteriormente para o registro de notificações de eventos.

O código C++ a seguir demonstra como você pode se registrar para receber notificações de **IWMDMNotification**.


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



Quando o aplicativo for fechado, você deverá encerrar o registro com **o IConnectionPoint** para indicar que ele não deve mais enviar notificações. Siga estas etapas para o registro de notificações:

1.  Consulte a interface **IWMDeviceManager** principal para **IConnectionPointContainer.**
2.  Obter um ponto de conexão **para interfaces IWMDMNotification.**
3.  Desmarque seu aplicativo para notificações de eventos chamando **IConnectionPoint::Unadvise**, passando a ID exclusiva recebida quando você se registrou para receber eventos.

O código C++ a seguir mostra como encerrar o registro de eventos **IWMDMNotification** quando seu aplicativo é fechado.


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



**Usando IWMDMProgress**

Windows Os Gerenciador de Dispositivos de mídia podem enviar mensagens de status do aplicativo quando ações específicas, como transferência de conteúdo, aquisição segura de relógio e encontrar informações de arquivo DRM, ocorrem. Seu aplicativo pode usar essas mensagens para monitorar o status do evento ou cancelar um evento. Para usar essa interface, implemente [**IWMDMProgress,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress) [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)ou [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)e passe-o como um parâmetro para um método que aceitará uma mensagem de progresso. Observe que **IWMDMProgress3** é a interface superior porque fornece um GUID de identificação que especifica qual ação está sendo rastreada. Os métodos de aplicativo a seguir aceitam uma interface de progresso (os métodos de provedor de serviços correspondentes devem ser capazes de enviar notificações para uma interface enviada):

[**IWMDMStorageControl::D elete**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**IWMDMStorageControl::Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**IWMDMStorageControl::Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**IWMDMStorageGlobals::Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)

Exemplos de passagem de uma interface para um método são dados na documentação desses métodos. Para exemplos de implementação das interfaces de retorno de chamada, consulte a documentação dos métodos de **IWMDMProgress,** **IWMDMProgress2** ou **IWMDMProgress3**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um aplicativo Windows de Gerenciador de Dispositivos mídia**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





