---
description: a primeira etapa no uso dos serviços WIA (Windows Image Acquisition) é obter um ponteiro de interface IWiaDevMgr (se você estiver programando para Windows XP ou anterior) ou um ponteiro de interface IWiaDevMgr2 (se você estiver programando para o Windows Vista ou posterior).
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: Criando um Gerenciador de Dispositivos WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b171225062381d5b6951ed536b086fd46a27def108802e34fff82e3527991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035767"
---
# <a name="creating-a-wia-device-manager"></a>Criando um Gerenciador de Dispositivos WIA

a primeira etapa no uso dos serviços WIA (Windows Image Acquisition) é obter um ponteiro de interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (se você estiver programando para Windows XP ou anterior) ou um ponteiro de interface [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (se você estiver programando para o Windows Vista ou posterior). Para fazer isso, chame [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com os parâmetros apropriados. O aplicativo de exemplo WiaSSamp cria um Gerenciador de dispositivos dentro de uma função global implementada pelo seguinte código:


```
    HRESULT CreateWiaDeviceManager( IWiaDevMgr **ppWiaDevMgr ) //XP or earlier
    HRESULT CreateWiaDeviceManager( IWiaDevMgr2 **ppWiaDevMgr ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == ppWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevMgr = NULL;

        //
        // Create an instance of the device manager
        //
        
        //XP or earlier:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr, (void**)ppWiaDevMgr );

        //Vista or later:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr2, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr2, (void**)ppWiaDevMgr ); 

        //
        // Return the result of creating the device manager
        //
        return hr;
    }
```



Neste exemplo, CLSID \_ WiaDevMgr e IID \_ IWiaDevMgr são constantes WIA que representam a ID de classe e a ID de interface de [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), respectivamente. CLSID \_ WiaDevMgr2 e IID \_ IWiaDevMgr2 são constantes WIA que representam a ID de classe e a ID de interface de [**IWiaDevMgr2**](-wia-iwiadevmgr2.md), respectivamente.

O valor do argumento *dwClsContext* da chamada [COCREATEINSTANCE](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) deve ser CLSCTX \_ \_ servidor local. Não há suporte para nenhum outro tipo de servidor e Component Object Model (COM) rejeita qualquer outro valor para esse parâmetro.

 

 
