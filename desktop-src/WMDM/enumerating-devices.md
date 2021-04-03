---
title: Enumerando dispositivos Windows Media Gerenciador de Dispositivos
description: Enumerando dispositivos
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows Media Gerenciador de Dispositivos, enumerando dispositivos
- Gerenciador de Dispositivos, enumerando dispositivos
- Guia de programação, enumerando dispositivos
- aplicativos de desktop, enumerando dispositivos
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, enumerando dispositivos
- Enumerando dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3584e625f54ea4e5c601f2a32865515c824cfcd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104084281"
---
# <a name="enumerating-windows-media-device-manager-devices"></a><span data-ttu-id="40041-109">Enumerando dispositivos Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="40041-109">Enumerating Windows Media Device Manager devices</span></span>

<span data-ttu-id="40041-110">Depois de autenticar um aplicativo, você pode começar a enumerar os dispositivos detectados pelo Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="40041-110">After authenticating an application, you can begin to enumerate the devices detected by Windows Media Device Manager.</span></span> <span data-ttu-id="40041-111">A enumeração é feita usando uma interface de enumeração, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtida com o uso de [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) ou [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span><span class="sxs-lookup"><span data-stu-id="40041-111">Enumeration is done by using an enumeration interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtained by using either [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) or [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span></span> <span data-ttu-id="40041-112">Se houver suporte, use o método **EnumDevices2** , porque a versão anterior retornou apenas interfaces herdadas em dispositivos, enquanto a nova versão retorna as interfaces herdadas e novas.</span><span class="sxs-lookup"><span data-stu-id="40041-112">If supported, use the **EnumDevices2** method, because the earlier version only returned legacy interfaces on devices, whereas the new version returns both the legacy and the new interfaces.</span></span>

<span data-ttu-id="40041-113">Antes de obter um enumerador, você deve decidir qual exibição de enumeração deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="40041-113">Before obtaining an enumerator, you should decide what enumeration view to use.</span></span> <span data-ttu-id="40041-114">Alguns dispositivos expõem cada armazenamento como um dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="40041-114">Some devices expose each storage as a different device.</span></span> <span data-ttu-id="40041-115">Por exemplo, dois cartões de memória flash em um dispositivo serão enumerados como se fossem dispositivos separados.</span><span class="sxs-lookup"><span data-stu-id="40041-115">For example, two flash memory cards on a device will enumerate as if they were separate devices.</span></span> <span data-ttu-id="40041-116">Você pode especificar que todos os armazenamentos em um dispositivo sejam enumerados juntos como um único dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40041-116">You can specify that all storages on a device are enumerated together as a single device.</span></span> <span data-ttu-id="40041-117">Você pode definir essa preferência somente uma vez no aplicativo; Se você quiser alterá-lo, deverá desligar o aplicativo e reiniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="40041-117">You can set this preference only once in your application; if you want to change it, you must shut down the application and restart it.</span></span> <span data-ttu-id="40041-118">No entanto, observe que os dispositivos herdados às vezes irão ignorar uma solicitação para enumerar armazenamentos de dispositivo separados como um único dispositivo e continuar a enumerá-los separadamente.</span><span class="sxs-lookup"><span data-stu-id="40041-118">However, note that legacy devices will sometimes ignore a request to enumerate separate device storages as a single device, and continue to enumerate them separately.</span></span>

<span data-ttu-id="40041-119">As etapas a seguir mostram como enumerar dispositivos conectados:</span><span class="sxs-lookup"><span data-stu-id="40041-119">The following steps show how to enumerate connected devices:</span></span>

1.  <span data-ttu-id="40041-120">Defina a preferência de enumeração de dispositivo usando [**IWMDeviceManager3:: SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span><span class="sxs-lookup"><span data-stu-id="40041-120">Set the device enumeration preference using [**IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span></span> <span data-ttu-id="40041-121">Se esse método não for chamado, o método padrão será mostrar armazenamentos como dispositivos separados.</span><span class="sxs-lookup"><span data-stu-id="40041-121">If this method is not called, the default method is to show storages as separate devices.</span></span> <span data-ttu-id="40041-122">Para determinar se "dispositivos" individuais são, na verdade, armazenamentos no mesmo dispositivo, chame [**IWMDMDevice2:: Getcanôniconame**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); os armazenamentos do mesmo dispositivo retornarão valores idênticos, exceto o dígito final após o último sinal "$".</span><span class="sxs-lookup"><span data-stu-id="40041-122">To determine whether individual "devices" are actually storages on the same device, call [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); storages from the same device will return identical values, except for the final digit after the last "$" sign.</span></span>
2.  <span data-ttu-id="40041-123">Consulte para [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) ou [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)e, em seguida, chame [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) para obter a interface do enumerador de dispositivo, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span><span class="sxs-lookup"><span data-stu-id="40041-123">Query for [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) or [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), and then call [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) to obtain the device enumerator interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span></span> <span data-ttu-id="40041-124">(Se houver suporte, use **EnumDevices2**, que é mais eficiente, já que a versão anterior pode não retornar dispositivos MTP).</span><span class="sxs-lookup"><span data-stu-id="40041-124">(If supported, use **EnumDevices2**, which is more efficient, as the earlier version may not return MTP devices).</span></span>
3.  <span data-ttu-id="40041-125">Chame o método [**IWMDMEnumDevices:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) para recuperar um ou mais dispositivos de cada vez.</span><span class="sxs-lookup"><span data-stu-id="40041-125">Call the [**IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) method to retrieve one or more devices at a time.</span></span> <span data-ttu-id="40041-126">Continue a chamar esse método até que o método retorne S \_ false ou uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="40041-126">Continue to call this method until the method returns S\_FALSE or an error message.</span></span> <span data-ttu-id="40041-127">Se recuperar apenas um dispositivo por vez, você não precisará alocar uma matriz para manter os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="40041-127">If retrieving only one device at a time, you do not need to allocate an array to hold the devices.</span></span>

<span data-ttu-id="40041-128">Como os usuários podem anexar ou remover dispositivos do computador enquanto seu aplicativo está em execução, é uma boa ideia implementar a notificação de conexão ou remoção do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40041-128">Because users can attach or remove devices from the computer while your application is running, it is a good idea to implement notification of device connection or removal.</span></span> <span data-ttu-id="40041-129">Isso é feito implementando a interface [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) e registrando-a.</span><span class="sxs-lookup"><span data-stu-id="40041-129">This is done by implementing the [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) interface and registering it.</span></span> <span data-ttu-id="40041-130">Para obter mais informações sobre isso, consulte [habilitando notificações](enabling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="40041-130">For more information on this, see [Enabling Notifications](enabling-notifications.md).</span></span>

<span data-ttu-id="40041-131">O código C++ a seguir enumera os dispositivos e solicita informações sobre cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40041-131">The following C++ code enumerates devices and requests information about each device.</span></span>


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="40041-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40041-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40041-133">**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="40041-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




