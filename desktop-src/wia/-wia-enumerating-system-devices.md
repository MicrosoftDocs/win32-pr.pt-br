---
description: Use o método IWiaDevMgr::EnumDeviceInfo (ou IWiaDevMgr2::EnumDeviceInfo) para enumerar os dispositivos WIA (Aquisição de Imagem) do Windows instalados em um sistema.
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Enumerando dispositivos do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60b6587d88b2836e057f0b6d7e31bd7f22d79c6220c51b407b621370d8524b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814256"
---
# <a name="enumerating-system-devices"></a>Enumerando dispositivos do sistema

Use o método [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (ou [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) para enumerar os dispositivos WIA (Aquisição de Imagem) do Windows instalados em um sistema. Esse método cria um objeto de enumeração para as propriedades dos dispositivos e retorna um ponteiro para a interface [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) compatível com o objeto de enumeração.

Em seguida, você pode usar os métodos da interface [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obter um ponteiro de interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo instalado no sistema.

O código a seguir do aplicativo de exemplo WiaSSamp demonstra como criar um objeto de enumeração para os dispositivos em um sistema e iterar por meio desses dispositivos:


```
    HRESULT EnumerateWiaDevices( IWiaDevMgr *pWiaDevMgr ) //XP or earlier
    HRESULT EnumerateWiaDevices( IWiaDevMgr2 *pWiaDevMgr ) //Vista or later
    
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Get a device enumerator interface
        //
        IEnumWIA_DEV_INFO *pWiaEnumDevInfo = NULL;
        HRESULT hr = pWiaDevMgr->EnumDeviceInfo( WIA_DEVINFO_ENUM_LOCAL, &pWiaEnumDevInfo );
        if (SUCCEEDED(hr))
        {
            //
            // Loop until you get an error or pWiaEnumDevInfo->Next returns
            // S_FALSE to signal the end of the list.
            //
            while (S_OK == hr)
            {
                //
                // Get the next device's property storage interface pointer
                //
                IWiaPropertyStorage *pWiaPropertyStorage = NULL;
                hr = pWiaEnumDevInfo->Next( 1, &pWiaPropertyStorage, NULL );

                //
                // pWiaEnumDevInfo->Next will return S_FALSE when the list is
                // exhausted, so check for S_OK before using the returned
                // value.
                //
                if (hr == S_OK)
                {
                    //
                    // Do something with the device's IWiaPropertyStorage*
                    //

                    //
                    // Release the device's IWiaPropertyStorage*
                    //
                    pWiaPropertyStorage->Release();
                    pWiaPropertyStorage = NULL;
                }
            }

            //
            // If the result of the enumeration is S_FALSE (which
            // is normal), change it to S_OK.
            //
            if (S_FALSE == hr)
            {
                hr = S_OK;
            }

            //
            // Release the enumerator
            //
            pWiaEnumDevInfo->Release();
            pWiaEnumDevInfo = NULL;
        }

        //
        // Return the result of the enumeration
        //
        return hr;
    }
```



WIA \_ DEVINFO \_ ENUM \_ LOCAL é uma constante WIA que representa o único valor válido para esse parâmetro.

No exemplo, o parâmetro **pWiaDevMgr** aponta para uma instância da interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) após uma chamada anterior para [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

O  aplicativo chama o método [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (ou [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) do ponteiro [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) que preenche **pWiaEnumDevInfo** com o endereço de um ponteiro para a interface [**IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)

Se a chamada for bem-sucedida, o aplicativo chamará o método [**IEnumWIA \_ DEV \_ INFO::Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) do ponteiro [**IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) A **variável pWiaEnumDevInfo** garante que a enumeração seja iniciada no início.

Se essa chamada for bem-sucedida, o aplicativo itera pelos dispositivos no sistema chamando repetidamente o método [**IEnumWIA \_ DEV \_ INFO::Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) do ponteiro [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **pWiaEnumDevInfo** até que o método não retorne mais S OK, indicando que a \_ enumeração foi concluída.

Cada chamada para **pWiaEnumDevInfo->Next** preenche **pWiaPropertyStorage** com um ponteiro para a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) que contém informações de propriedade para um dispositivo específico.

 

 
