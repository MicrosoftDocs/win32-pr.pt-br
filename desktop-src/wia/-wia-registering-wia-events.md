---
description: 'Os aplicativos podem ser registrados para serem notificados sobre eventos de dispositivo de hardware da aquisição de imagens do Windows (WIA) chamando um dos seguintes métodos de interface IWiaDevMgr ou IWiaDevMgr2: IWiaDevMgr:: RegisterEventCallbackCLSID ou IWiaDevMgr2:: RegisterEventCallbackCLSIDIWiaDevMgr:: RegisterEventCallbackInterface ou IWiaDevMgr2:: RegisterEventCallbackInterfaceIWiaDevMgr:: RegisterEventCallbackProgram ou IWiaDevMgr2:: RegisterEventCallbackProgram'
ms.assetid: 0c142083-835f-4bbd-ab32-eb6130f99c59
title: Registrando eventos WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9fc36540a64211428579bc13b84902490ea103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920945"
---
# <a name="registering-wia-events"></a>Registrando eventos WIA

Os aplicativos podem ser registrados para serem notificados sobre eventos de dispositivo de hardware da aquisição de imagens do Windows (WIA) chamando um dos seguintes métodos de interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) :

-   [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) ou [ **IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)
-   [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) ou [ **IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)
-   [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) ou [ **IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)

Todos esses métodos usam parâmetros que especificam o evento e o dispositivo de hardware para o qual o aplicativo deve ser notificado. Os aplicativos se registram para receber um evento para todos os dispositivos WIA, passando um valor **nulo** para o parâmetro que especifica o dispositivo de hardware.

O método **RegisterEventCallbackInterface** registra um aplicativo para receber um evento de dispositivo de hardware WIA se o aplicativo estiver em execução no momento em que o evento ocorrer. Quando o evento para o qual o aplicativo é registrado ocorre, o WIA chama o método [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) do objeto fornecido pelo aplicativo para transmitir as informações do evento.

O método **RegisterEventCallbackCLSID** registra um aplicativo que é um componente COM (Component Object Model registrado) para receber um evento de dispositivo de hardware WIA, mesmo que o aplicativo não esteja em execução. Além dos parâmetros mencionados anteriormente, esse método usa um parâmetro, *pCLSID*, que especifica a ID de classe do aplicativo. Quando o evento especificado ocorre, o sistema WIA usa a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e a ID de classe especificada por *pCLSID* para criar uma nova instância do aplicativo e chama o método [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) desse aplicativo para transmitir as informações do evento.

O método **RegisterEventCallbackProgram** registra um aplicativo para receber um evento de dispositivo de hardware WIA, mesmo que o aplicativo não esteja em execução quando o evento ocorrer. O aplicativo não precisa ser um componente COM registrado. O WIA inicia o aplicativo com uma instrução de linha de comando. **RegisterEventCallbackProgram** usa um parâmetro, *bstrCommandline*, que especifica o caminho completo e o nome do arquivo do aplicativo executável. **RegisterEventCallbackProgram** existe para compatibilidade com versões anteriores com aplicativos que não foram escritos para WIA e que devem ser evitados. Em vez disso, use **RegisterEventCallbackInterface** ou **RegisterEventCallbackCLSID** .

Para determinar quais manipuladores são registrados para eventos em um dispositivo WIA específico, um aplicativo chama um método [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ou [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) de um item raiz. Esse método cria um objeto de enumeração para as informações de registro. O aplicativo pode usar a interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) desse objeto para enumerar informações sobre os manipuladores registrados para receber eventos para esse dispositivo.

Se ocorrer um evento para o qual um aplicativo em execução é registrado por meio de **RegisterEventCallbackInterface** e **RegisterEventCallbackCLSID** ou **RegisterEventCallbackProgram**, o WIA notifica o aplicativo em execução e não tenta iniciar uma nova instância do aplicativo porque o registro de eventos por meio de **RegisterEventCallbackInterface** tem precedência sobre **RegisterEventCallbackCLSID** e **RegisterEventCallbackProgram**.

> [!Note]  
> Em um aplicativo multi-threaded, não há nenhuma garantia de que o thread em que o retorno de chamada de notificação de eventos retornará é o mesmo thread que registrou o retorno de chamada.

 

 

 
