---
title: Enumerando dispositivos (SDK do WMP)
description: Este código de exemplo mostra uma função que enumera dispositivos criando uma matriz de ponteiros que representam um dispositivo.
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Windows Media Player, dispositivos portáteis
- Windows Media Player de objeto, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Windows Media Player controle ActiveX, dispositivos portáteis
- Controle ActiveX, dispositivos portáteis
- Windows Media Player controle ActiveX móvel, dispositivos portáteis
- Windows Media Player dispositivos móveis e portáteis
- dispositivos portáteis, enumerando
- enumerações, dispositivos portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44f71fa26f40983424ced70280d9c03e0892a00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068433"
---
# <a name="enumerating-devices"></a><span data-ttu-id="51573-112">Enumerando dispositivos</span><span class="sxs-lookup"><span data-stu-id="51573-112">Enumerating Devices</span></span>

<span data-ttu-id="51573-113">Windows Media Player representa dispositivos portáteis usando a interface **IWMPSyncDevice.**</span><span class="sxs-lookup"><span data-stu-id="51573-113">Windows Media Player represents portable devices by using the **IWMPSyncDevice** interface.</span></span> <span data-ttu-id="51573-114">O código de exemplo a seguir mostra uma função que cria uma matriz de ponteiros para **IWMPSyncDevice**.</span><span class="sxs-lookup"><span data-stu-id="51573-114">The following example code shows a function that creates an array of pointers to **IWMPSyncDevice**.</span></span> <span data-ttu-id="51573-115">Cada ponteiro na matriz representa um dispositivo para o qual Windows Media Player tem informações armazenadas.</span><span class="sxs-lookup"><span data-stu-id="51573-115">Each pointer in the array represents a device for which Windows Media Player has stored information.</span></span> <span data-ttu-id="51573-116">Um dispositivo não precisa estar conectado ao computador, nem é necessário ter uma parceria com a instância Windows Media Player atual.</span><span class="sxs-lookup"><span data-stu-id="51573-116">A device is not required to be connected to the computer, nor is it required to have a partnership with the current Windows Media Player instance.</span></span>

<span data-ttu-id="51573-117">Você deve enumerar dispositivos sempre que receber o evento **DeviceConnect** ou **o evento DeviceDisconnect.**</span><span class="sxs-lookup"><span data-stu-id="51573-117">You should enumerate devices whenever you receive the **DeviceConnect** event or the **DeviceDisconnect** event.</span></span>

<span data-ttu-id="51573-118">A função a seguir enumera os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="51573-118">The following function enumerates devices.</span></span> <span data-ttu-id="51573-119">O *parâmetro bConnectedOnly* especifica se apenas os dispositivos conectados ao computador do usuário são enumerados no momento.</span><span class="sxs-lookup"><span data-stu-id="51573-119">The *bConnectedOnly* parameter specifies whether to enumerate only devices currently connected to the user's computer.</span></span>


```C++
STDMETHODIMP CMainDlg::EnumDevices(BOOL bConnectedOnly)
{
    HRESULT hr = S_OK;
    CComPtr<IWMPSyncServices>  spSyncServices;
    long cDeviceArray = 0;  // Size to make the array
    long cAllDevices = 0;  // Count of all devices
    long cDeviceIndex = 0; // Index for adding devices to array.
    CComPtr<IWMPSyncDevice> spTempDevice;
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;

    // Delete any existing array.
    FreeDeviceArray();

    // Retrieve a pointer to IWMPSyncServices.
    hr = m_spPlayer->QueryInterface(&spSyncServices);

    if(SUCCEEDED(hr) && spSyncServices.p)
    {  
        hr = spSyncServices->get_deviceCount(&cAllDevices);
    }

    if(SUCCEEDED(hr) && cAllDevices > 0)
    {
        if(bConnectedOnly)
        {
            // Count the number of connected devices.
            for(long i = 0; i < cAllDevices; i++)
            {     
                spTempDevice.Release();
                hr = spSyncServices->getDevice(i, &spTempDevice);

                if(SUCCEEDED(hr) && spTempDevice.p)
                {
                    spTempDevice->get_connected(&vbIsConnected);

                    if(vbIsConnected == VARIANT_TRUE)
                    {
                        // Count only the connected devices.
                        cDeviceArray++;
                    }
                }
            }
        }
        else
        {
            cDeviceArray = cAllDevices;
        }

        if(cDeviceArray == 0)
        {
            return hr;
        }

        // Cache the device count.
        m_cDevices = cDeviceArray;

        // Create a new device array.
        m_ppWMPDevices = new IWMPSyncDevice*[cDeviceArray];
        if(!m_ppWMPDevices)
        {
            return E_OUTOFMEMORY;
        }
        
        ZeroMemory(m_ppWMPDevices, sizeof (IWMPSyncDevice*) * cDeviceArray);

        // Fill the array.
        for(long i = 0; i < cAllDevices; i++)
        {
            spTempDevice.Release();
            hr = spSyncServices->getDevice(i, &spTempDevice);
            if(SUCCEEDED(hr) && spTempDevice.p)
            {
                spTempDevice->get_connected(&vbIsConnected);

                if( (bConnectedOnly && vbIsConnected == VARIANT_TRUE) ||
                     !bConnectedOnly )
                {
                    // Add the device to the custom array.
                    spTempDevice.CopyTo(&m_ppWMPDevices[cDeviceIndex++]);
                }
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="51573-120">Você pode usar código semelhante para recuperar outras listas de dispositivos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="51573-120">You might use similar code to retrieve other such device lists.</span></span> <span data-ttu-id="51573-121">Por exemplo, você pode usar [o \_ status IWMPSyncDevice::get](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) para criar uma matriz de dispositivos para os quais existe uma parceria.</span><span class="sxs-lookup"><span data-stu-id="51573-121">For example, you could use [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) to create an array of devices for which a partnership exists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51573-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51573-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51573-123">**IWMPEvents2::D eviceConnect**</span><span class="sxs-lookup"><span data-stu-id="51573-123">**IWMPEvents2::DeviceConnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[<span data-ttu-id="51573-124">**IWMPEvents2::D eviceDisconnect**</span><span class="sxs-lookup"><span data-stu-id="51573-124">**IWMPEvents2::DeviceDisconnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[<span data-ttu-id="51573-125">**IWMPSyncDevice Interface**</span><span class="sxs-lookup"><span data-stu-id="51573-125">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="51573-126">**IWMPSyncDevice::get \_ connected**</span><span class="sxs-lookup"><span data-stu-id="51573-126">**IWMPSyncDevice::get\_connected**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[<span data-ttu-id="51573-127">**IWMPSyncServices Interface**</span><span class="sxs-lookup"><span data-stu-id="51573-127">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[<span data-ttu-id="51573-128">**Trabalhando com dispositivos portáteis**</span><span class="sxs-lookup"><span data-stu-id="51573-128">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




