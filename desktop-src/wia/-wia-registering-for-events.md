---
description: 'o exemplo a seguir usa o método wia (Windows image Acquisition) 1,0 IWiaDevMgr:: RegisterEventCallbackCLSID para se registrar para notificação quando qualquer dispositivo wia (Windows image acquisition) estiver conectado ao sistema.'
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Registrar-se em eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7a72614533ccc7c2f72bb4f2cf105107cc88ef8030cf306d31d6d9ffa5b4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965545"
---
# <a name="registering-for-events"></a>Registrar-se em eventos

o exemplo a seguir usa o método wia (Windows image Acquisition) 1,0 [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) para se registrar para notificação quando qualquer dispositivo wia (Windows image acquisition) estiver conectado ao sistema. Os aplicativos também podem usar WIA 1,0 [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) e WIA 1,0 [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) para registrar eventos. com o Windows Vista e posterior, você pode usar os métodos WIA (Windows Image Acquisition) 2,0 [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)ou [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) para se registrar em eventos.

Supõe-se que o exemplo é obtido de um aplicativo registrado como um objeto de servidor fora do processo Component Object Model (COM).

A chamada para [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (ou [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) é a seguinte:


```
    pWiaDevMgr->RegisterEventCallbackCLSID( WIA_REGISTER_EVENT_CALLBACK,
                                            NULL,
                                            WIA_EVENT_DEVICE_CONNECTED,
                                            pCLSID,
                                            bstrName,
                                            bstrDescription,
                                            bstrIcon
                                            );
```



No código anterior, **pWiaDevMgr** é um ponteiro válido para a interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)), o \_ retorno de chamada de evento de registro WIA \_ \_ é uma constante que especifica que essa chamada é para registrar o evento em oposição ao cancelamento do registro para o evento, \_ o dispositivo de evento WIA \_ \_ conectado é uma constante que especifica que o aplicativo está se registrando para ser notificado sempre que um dispositivo estiver conectado **pCLSID** é um ponteiro para o CLSID registrado do aplicativo, **bstrname** é o nome do aplicativo, **bstrDescription** é uma descrição de texto do aplicativo e **bstrIcon** é o nome de um arquivo de imagem a ser usado para o ícone do registro do aplicativo para o evento.

O aplicativo deve então implementar o método [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) , que é chamado sempre que ocorre um evento para o qual o aplicativo é registrado.

Um aplicativo pode usar o método [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (ou [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) para enumerar as informações sobre eventos para os quais ele está registrado.

 

 



