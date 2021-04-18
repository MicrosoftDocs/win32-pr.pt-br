---
description: A primeira etapa no uso dos serviços de aquisição de imagem do Windows (WIA) é obter um ponteiro de interface IWiaDevMgr (se você estiver programando para o Windows XP ou anterior) ou um ponteiro de interface IWiaDevMgr2 (se você estiver programando para o Windows Vista ou posterior).
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: Criando um Gerenciador de Dispositivos WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e315939566eea6fe8a4acabeb5fd8afe247c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788964"
---
# <a name="creating-a-wia-device-manager"></a><span data-ttu-id="c519d-103">Criando um Gerenciador de Dispositivos WIA</span><span class="sxs-lookup"><span data-stu-id="c519d-103">Creating a WIA Device Manager</span></span>

<span data-ttu-id="c519d-104">A primeira etapa no uso dos serviços de aquisição de imagem do Windows (WIA) é obter um ponteiro de interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (se você estiver programando para o Windows XP ou anterior) ou um ponteiro de interface [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (se você estiver programando para o Windows Vista ou posterior).</span><span class="sxs-lookup"><span data-stu-id="c519d-104">The first step in using Windows Image Acquisition (WIA) services is to obtain an [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) interface pointer (if you are programming for Windows XP or earlier) or an [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface pointer (if you are programming for Windows Vista or later).</span></span> <span data-ttu-id="c519d-105">Para fazer isso, chame [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com os parâmetros apropriados.</span><span class="sxs-lookup"><span data-stu-id="c519d-105">To do this, call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the appropriate parameters.</span></span> <span data-ttu-id="c519d-106">O aplicativo de exemplo WiaSSamp cria um Gerenciador de dispositivos dentro de uma função global implementada pelo seguinte código:</span><span class="sxs-lookup"><span data-stu-id="c519d-106">The sample application WiaSSamp creates a device manager within a global function implemented by the following code:</span></span>


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



<span data-ttu-id="c519d-107">Neste exemplo, CLSID \_ WiaDevMgr e IID \_ IWiaDevMgr são constantes WIA que representam a ID de classe e a ID de interface de [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c519d-107">In this example, CLSID\_WiaDevMgr and IID\_IWiaDevMgr are WIA constants that represent the class ID and the interface ID of [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), respectively.</span></span> <span data-ttu-id="c519d-108">CLSID \_ WiaDevMgr2 e IID \_ IWiaDevMgr2 são constantes WIA que representam a ID de classe e a ID de interface de [**IWiaDevMgr2**](-wia-iwiadevmgr2.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c519d-108">CLSID\_WiaDevMgr2 and IID\_IWiaDevMgr2 are WIA constants that represent the class ID and the interface ID of [**IWiaDevMgr2**](-wia-iwiadevmgr2.md), respectively.</span></span>

<span data-ttu-id="c519d-109">O valor do argumento *dwClsContext* da chamada [COCREATEINSTANCE](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) deve ser CLSCTX \_ \_ servidor local.</span><span class="sxs-lookup"><span data-stu-id="c519d-109">The value for the *dwClsContext* argument of the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call must be CLSCTX\_LOCAL\_SERVER.</span></span> <span data-ttu-id="c519d-110">Não há suporte para nenhum outro tipo de servidor e Component Object Model (COM) rejeita qualquer outro valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c519d-110">No other server type is supported, and Component Object Model (COM) rejects any other value for this parameter.</span></span>

 

 
