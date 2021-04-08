---
description: 'Use o método IWiaDevMgr:: EnumDeviceInfo (ou IWiaDevMgr2:: EnumDeviceInfo) para enumerar os dispositivos de aquisição de imagem do Windows (WIA) instalados em um sistema.'
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Enumerando dispositivos do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d65879cd1fc8466f4ada638281ef496636b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921805"
---
# <a name="enumerating-system-devices"></a><span data-ttu-id="28e58-103">Enumerando dispositivos do sistema</span><span class="sxs-lookup"><span data-stu-id="28e58-103">Enumerating System Devices</span></span>

<span data-ttu-id="28e58-104">Use o método [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (ou [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) para enumerar os dispositivos de aquisição de imagem do Windows (WIA) instalados em um sistema.</span><span class="sxs-lookup"><span data-stu-id="28e58-104">Use the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method to enumerate the Windows Image Acquisition (WIA) devices installed on a system.</span></span> <span data-ttu-id="28e58-105">Esse método cria um objeto de enumeração para as propriedades dos dispositivos e retorna um ponteiro para a interface [**de \_ \_ informações de desenvolvimento IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) que o objeto de enumeração suporta.</span><span class="sxs-lookup"><span data-stu-id="28e58-105">This method creates an enumeration object for the properties of the devices, and returns a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface that the enumeration object supports.</span></span>

<span data-ttu-id="28e58-106">Em seguida, você pode usar os métodos da interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obter um ponteiro de interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="28e58-106">You can then use the methods of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface to obtain an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface pointer for each device installed on the system.</span></span>

<span data-ttu-id="28e58-107">O código a seguir do aplicativo de exemplo WiaSSamp demonstra como criar um objeto de enumeração para os dispositivos em um sistema e iterar por meio desses dispositivos:</span><span class="sxs-lookup"><span data-stu-id="28e58-107">The following code from the WiaSSamp sample application demonstrates how to create an enumeration object for the devices on a system and iterate through those devices:</span></span>


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



<span data-ttu-id="28e58-108">WIA \_ DevInfo de \_ enumeração \_ local é uma constante WIA que representa o único valor válido para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="28e58-108">WIA\_DEVINFO\_ENUM\_LOCAL is a WIA constant that represents the only valid value for this parameter.</span></span>

<span data-ttu-id="28e58-109">No exemplo, o parâmetro **pWiaDevMgr** aponta para uma instância da interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) após uma chamada anterior para [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="28e58-109">In the example, the parameter **pWiaDevMgr** points to an instance of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface after a previous call to [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="28e58-110">O aplicativo chama o [**método IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (ou [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) do ponteiro [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) **pWiaDevMgr** que preenche **pWiaEnumDevInfo** com o endereço de um ponteiro para a interface [**de \_ \_ informações de desenvolvimento IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="28e58-110">The application calls the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) pointer **pWiaDevMgr** that fills **pWiaEnumDevInfo** with the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

<span data-ttu-id="28e58-111">Se a chamada for realizada com sucesso, o aplicativo chamará o método [**IEnumWIA \_ dev \_ info:: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) do ponteiro de [**\_ \_ informações de desenvolvimento do IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="28e58-111">If the call succeeds, the application then calls the [**IEnumWIA\_DEV\_INFO::Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer.</span></span> <span data-ttu-id="28e58-112">A variável **pWiaEnumDevInfo** garante que a enumeração comece no início.</span><span class="sxs-lookup"><span data-stu-id="28e58-112">The **pWiaEnumDevInfo** variable ensures that the enumeration starts at the beginning.</span></span>

<span data-ttu-id="28e58-113">Se essa chamada for bem sucedido, o aplicativo itera pelos dispositivos no sistema chamando repetidamente o método [**IEnumWIA \_ dev \_ info:: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) do ponteiro de [**\_ \_ informações do IEnumWIA dev**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **pWiaEnumDevInfo** até que o método não retorne S \_ OK, indicando que a enumeração foi concluída.</span><span class="sxs-lookup"><span data-stu-id="28e58-113">If this call succeeds, the application iterates through the devices on the system by repeatedly calling the [**IEnumWIA\_DEV\_INFO::Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer **pWiaEnumDevInfo** until the method no longer returns S\_OK, indicating that the enumeration is complete.</span></span>

<span data-ttu-id="28e58-114">Cada chamada para **pWiaEnumDevInfo->Next** preenche **pWiaPropertyStorage** com um ponteiro para a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) que contém informações de propriedade para um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="28e58-114">Each call to **pWiaEnumDevInfo->Next** fills **pWiaPropertyStorage** with a pointer to the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface that contains property information for a specific device.</span></span>

 

 
