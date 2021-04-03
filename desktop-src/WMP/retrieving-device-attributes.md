---
title: Recuperando atributos do dispositivo
description: Recuperando atributos do dispositivo
ms.assetid: c553d495-d8fc-4483-a3dc-6679c6b9d1f1
keywords:
- Windows Media Player, dispositivos portáteis
- Modelo de objeto do Windows Media Player, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Controle ActiveX do Windows Media Player, dispositivos portáteis
- Controle ActiveX, dispositivos portáteis
- Controle ActiveX móvel do Windows Media Player, dispositivos portáteis
- Windows Media Player Mobile, dispositivos portáteis
- dispositivos portáteis, recuperando atributos
- atributos, dispositivos portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f486b94fe6a9a5c78f238d78a7f79dec9df3376
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007148"
---
# <a name="retrieving-device-attributes"></a><span data-ttu-id="fc5fc-112">Recuperando atributos do dispositivo</span><span class="sxs-lookup"><span data-stu-id="fc5fc-112">Retrieving Device Attributes</span></span>

<span data-ttu-id="fc5fc-113">O Windows Media Player armazena informações sobre os dispositivos que se conectaram ao Player.</span><span class="sxs-lookup"><span data-stu-id="fc5fc-113">Windows Media Player stores information about devices that have connected to the Player.</span></span> <span data-ttu-id="fc5fc-114">Alguns atributos estão disponíveis chamando métodos individuais de **IWMPSyncDevice**, alguns podem ser recuperados usando **IWMPSyncDevice:: getItemInfo** e alguns podem ser recuperados usando qualquer uma das técnicas.</span><span class="sxs-lookup"><span data-stu-id="fc5fc-114">Some attributes are available by calling individual methods of **IWMPSyncDevice**, some can be retrieved by using **IWMPSyncDevice::getItemInfo**, and some can be retrieved by using either technique.</span></span>

<span data-ttu-id="fc5fc-115">O código de exemplo a seguir preenche um controle de caixa de listagem com os atributos disponíveis para o dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="fc5fc-115">The following example code fills a list box control with the available attributes for the specified device.</span></span> <span data-ttu-id="fc5fc-116">A primeira parte da função recupera as propriedades disponíveis usando métodos específicos.</span><span class="sxs-lookup"><span data-stu-id="fc5fc-116">The first part of the function retrieves properties available by using specific methods.</span></span> <span data-ttu-id="fc5fc-117">A segunda parte da função recupera valores de atributo usando **IWMPSyncDevice:: getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="fc5fc-117">The second part of the function retrieves attribute values by using **IWMPSyncDevice::getItemInfo**.</span></span> <span data-ttu-id="fc5fc-118">O parâmetro de função, *Lindex*, é o índice para o dispositivo em sua matriz de dispositivo personalizada apontada por m \_ ppWMPDevices.</span><span class="sxs-lookup"><span data-stu-id="fc5fc-118">The function parameter, *lIndex*, is the index to the device in your custom device array pointed to by m\_ppWMPDevices.</span></span>


```C++
STDMETHODIMP CMainDlg::ShowDeviceAttributes(long lIndex)
{
    HRESULT hr = S_OK;

    if(!m_ppWMPDevices)
        return S_FALSE;

    // Array of attribute names for devices.
    const TCHAR *szDeviceAttributeNames[16] = {
    _T("Connected"),
    _T("FreeSpace"),
    _T("FriendlyName"),
    _T("LastSyncErrorCount"),
    _T("LastSyncNoFitCount"),
    _T("LastSyncTime"),
    _T("Name"),
    _T("SerialNumber"),
    _T("SupportsAudio"),
    _T("SupportsPhoto"),
    _T("SupportsVideo"),
    _T("SyncIndex"),
    _T("SyncItemCount"),
    _T("SyncPercentComplete"),
    _T("SyncRelationship"),
    _T("TotalSpace")};
    
    // Array of device status strings.
    static const TCHAR *szDeviceStatus[6] = {
    _T("Unknown"),
    _T("Partnership exists"),
    _T("Partnership declined by the user"),
    _T("Partnership with another computer or user"),
    _T("Device only supports manual transfer"),
    _T("New device")};

    // Handle to the list box that displays the information.
    HWND hwndStats = GetDlgItem(IDC_STATS);
    CComBSTR bstrStatistics;  // Contains the display string for each property.
    CComBSTR bstrTemp; // Contains the retrieved value for each property.
    // Retrieve a pointer to the current device.
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]);
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;
    WMPDeviceStatus  wmpDS = wmpdsUnknown;
    
    SendMessage(hwndStats, LB_RESETCONTENT, 0, 0);

    if(NULL == spDevice.p)
    {
        return E_POINTER;
    }
 
    // Status
    spDevice->get_status(&wmpDS);
    bstrStatistics = "Status: ";
    bstrTemp = szDeviceStatus[wmpDS];
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrTemp.Empty();
    
    // Connected?
    spDevice->get_connected(&vbIsConnected);
    bstrStatistics = "Connected: ";
    bstrTemp = (vbIsConnected == VARIANT_TRUE)?"True":"False";
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics));
    bstrTemp.Empty();
    
    // Device ID
    spDevice->get_deviceId(&bstrTemp);
    bstrStatistics = "Device ID: ";
    bstrStatistics += bstrTemp;

    // Calculate the list box width based on text metrics.
    // This assumes Device ID is likely to be the longest string.
    HDC hDC = GetDC();
    SIZE sizeText = {0, 0};
    GetTextExtentPoint32(hDC, (LPCTSTR)COLE2T(bstrStatistics), bstrStatistics.Length(), &sizeText);
    ReleaseDC(hDC);

    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    SendMessage(hwndStats, LB_SETHORIZONTALEXTENT, sizeText.cx, 0);
    bstrTemp.Empty();

    // Friendly name
    spDevice->get_friendlyName(&bstrTemp);
    bstrStatistics = "Friendly name: ";
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrTemp.Empty();

    // Skip a line and label the getItemInfo attributes.
    bstrStatistics = "";
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrStatistics = "--getItemInfo Attributes--";
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 

    // Show the getItemInfo attributes.
    int iArrayBound = sizeof szDeviceAttributeNames / sizeof szDeviceAttributeNames[0];
    for(int i = 0; i < iArrayBound; i++)
    {
        CComBSTR bstrName(szDeviceAttributeNames[i]);
        CComBSTR bstrVal;
        CComBSTR bstrDisplayString;
       
        hr = spDevice->getItemInfo(bstrName, &bstrVal);
  
        if(FAILED(hr))
        {
             bstrVal.Append("Error");
        }  
        
        bstrName.Append(L": ");
        bstrDisplayString.AppendBSTR(bstrName);
        bstrDisplayString += bstrVal;  
 
        SendMessage(hwndStats, LB_ADDSTRING, 0, (LPARAM)(LPCTSTR)COLE2T(bstrDisplayString));
    }    

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fc5fc-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc5fc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc5fc-120">**Enumerando dispositivos**</span><span class="sxs-lookup"><span data-stu-id="fc5fc-120">**Enumerating Devices**</span></span>](enumerating-devices.md)
</dt> <dt>

[<span data-ttu-id="fc5fc-121">**Interface IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="fc5fc-121">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="fc5fc-122">**IWMPSyncDevice::getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="fc5fc-122">**IWMPSyncDevice::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)
</dt> <dt>

[<span data-ttu-id="fc5fc-123">**Trabalhando com dispositivos portáteis**</span><span class="sxs-lookup"><span data-stu-id="fc5fc-123">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




