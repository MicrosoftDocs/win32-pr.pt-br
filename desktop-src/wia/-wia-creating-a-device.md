---
description: 'Quando um aplicativo tem a ID do dispositivo de um determinado dispositivo, ele pode chamar IWiaDevMgr:: CreateDevice ou IWiaDevMgr2:: CreateDevicemethod, que cria uma árvore hierárquica de objetos IWiaItem ou IWiaItem2 que representam um dispositivo de geração de imagens e os ambientes de verificação de imagem e as pastas contidas nesse dispositivo.'
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Criando um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6319e493c6b99e1f23d8f4ccb9be1e10628fae45e8d4ba7df0aa8112be39dba6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965895"
---
# <a name="creating-a-device"></a>Criando um dispositivo

Quando um aplicativo tem a ID do dispositivo de um determinado dispositivo, ele pode chamar o método [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) ou [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md), que cria uma árvore hierárquica de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) que representam um dispositivo de geração de imagens e os ambientes de verificação de imagem e as pastas contidas nesse dispositivo.

O exemplo a seguir do aplicativo de exemplo WiaSSamp implementa uma função que usa uma ID de dispositivo como um parâmetro. Para obter informações sobre como obter uma ID de dispositivo para um dispositivo específico, consulte [lendo propriedades do dispositivo](-wia-reading-device-properties.md).


```
    //XP or earlier:
    HRESULT CreateWiaDevice( IWiaDevMgr *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem **ppWiaDevice ) 
    //Vista or later:
    HRESULT CreateWiaDevice( IWiaDevMgr2 *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem2 **ppWiaDevice ) 
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr || NULL == bstrDeviceID || NULL == ppWiaDevice)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevice = NULL;

        //
        // Create the WIA Device
        //
        HRESULT hr = pWiaDevMgr->CreateDevice( bstrDeviceID, ppWiaDevice );

        //
        // Return the result of creating the device
        //
        return hr;
    }
```



Neste exemplo, **pWiaDevMgr** é um ponteiro para a interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , e **ppWiaDevice** é uma variável que, após a chamada para [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (ou to [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contém o endereço de um ponteiro para o item raiz da árvore que representa o dispositivo recém-criado.

 

 



