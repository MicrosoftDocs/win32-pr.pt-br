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
# <a name="enabling-notifications"></a>Habilitando notificações

O Windows Media Gerenciador de Dispositivos declara quatro interfaces que um aplicativo pode implementar em uma classe COM para receber notificações de eventos. Essas interfaces se enquadram em dois grupos, conforme mostrado na tabela a seguir.



| Interfaces                                                                                                                                                | Descrição                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Notifica o aplicativo quando dispositivos ou mídia de armazenamento estão conectados ou desconectados.                                                                                         |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Um sistema de notificação muito simples para alertar um aplicativo sobre o progresso de qualquer evento. Não é necessário que o aplicativo execute ações em resposta a essas mensagens. |



 

**IWMDMNotification**

O **IWMDMNotification** alerta o aplicativo quando plug and Play dispositivos são conectados ou desconectados do computador, bem como quando plug and Play mídia de armazenamento (como cartões flash) são inseridas ou removidas do dispositivo. Essas notificações podem ajudar o aplicativo a atualizar sua interface do usuário para refletir as alterações.

Para receber essas notificações, seu aplicativo deve se registrar para recebê-las usando as interfaces **IConnectionPointContainer** e **IConnectionPoint** do SDK da plataforma. Seu aplicativo deve se registrar para receber eventos quando ele for iniciado e cancelar o registro quando ele fechar. Siga estas etapas para se registrar para receber essas notificações.

1.  Consulte a interface **IWMDeviceManager** principal que você recebeu quando autenticou seu aplicativo para **IConnectionPointContainer**.
2.  Chame **IConnectionPointContainer:: FindConnectionPoint** para recuperar um ponto de conexão de contêiner para interfaces **IWMDMNotification** .
3.  Registre-se para receber eventos chamando **IConnectionPoint:: Advise**. Passe a classe que implementa **IWMDMNotification** e recupere um cookie, uma ID exclusiva que identifica o ponto de conexão. Isso deve ser armazenado e usado posteriormente para cancelar o registro para notificações de eventos.

O código C++ a seguir demonstra como você pode se registrar para receber notificações do **IWMDMNotification**.


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



Quando seu aplicativo for fechado, você deverá cancelar o registro com **IConnectionPoint** para indicar que ele não deve mais enviar notificações a você. Siga estas etapas para cancelar o registro para notificações:

1.  Consulte a interface principal do **IWMDeviceManager** para **IConnectionPointContainer**.
2.  Obtenha um ponto de conexão para interfaces **IWMDMNotification** .
3.  Cancele o registro do aplicativo para notificações de eventos chamando **IConnectionPoint:: Unadvise**, passando a ID exclusiva recebida quando você se registrou para receber eventos.

O código C++ a seguir mostra como cancelar o registro para eventos **IWMDMNotification** quando o aplicativo é fechado.


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

O Windows Media Gerenciador de Dispositivos pode enviar as mensagens de status do aplicativo quando ações específicas, como transferência de conteúdo, aquisição de clock seguro e ocorrência de informações de arquivo DRM, ocorrem. Seu aplicativo pode usar essas mensagens para monitorar o status do evento ou cancelar um evento. Para usar essa interface, implemente [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)ou [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)e passe-o como um parâmetro para um método que aceitará uma mensagem de progresso. Observe que **IWMDMProgress3** é a interface superior porque fornece um GUID de identificação que especifica qual ação está sendo controlada. Os métodos de aplicativo a seguir aceitam uma interface de progresso (os métodos do provedor de serviços correspondentes devem ser capazes de enviar notificações para uma interface enviada):

[**IWMDMStorageControl::D excluir**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**IWMDMStorageControl:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**IWMDMStorageControl:: mover**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**IWMDMStorageControl:: ler**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**IWMDMStorageControl:: Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**IWMDMStorageGlobals:: Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)

Exemplos de como passar uma interface em um método são fornecidos na documentação para esses métodos. Para obter exemplos de como implementar as interfaces de retorno de chamada, consulte a documentação dos métodos de **IWMDMProgress**, **IWMDMProgress2** ou **IWMDMProgress3**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





