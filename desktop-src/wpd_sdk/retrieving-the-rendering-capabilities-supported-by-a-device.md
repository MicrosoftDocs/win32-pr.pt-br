---
description: Recuperando os recursos de renderização suportados por um dispositivo
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: Recuperando os recursos de renderização suportados por um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523f1f9bbcaefe1c502c7c74252582fddcadad4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297517"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a><span data-ttu-id="ae307-103">Recuperando os recursos de renderização suportados por um dispositivo</span><span class="sxs-lookup"><span data-stu-id="ae307-103">Retrieving the Rendering Capabilities Supported by a Device</span></span>

<span data-ttu-id="ae307-104">Os dispositivos portáteis do Windows que dão suporte à categoria funcional informações de renderização ( \_ informações de renderização da categoria funcional de WPD \_ \_ \_ ) retornarão informações de renderização quando consultados.</span><span class="sxs-lookup"><span data-stu-id="ae307-104">Windows Portable Devices that support the rendering information functional category (WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION) will return rendering information when queried.</span></span> <span data-ttu-id="ae307-105">As informações de renderização descrevem os requisitos e as restrições impostas em aplicativos que tentam gravar conteúdo em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae307-105">The rendering information describes requirements and restrictions imposed on applications that attempt to write content to a device.</span></span>

<span data-ttu-id="ae307-106">A função ListRenderingCapabilityInformation, a função auxiliar SupportsFunctionalCategory e a função auxiliar ReadProfileInformationProperties no módulo DeviceCapabilities. cpp demonstram a recuperação de recursos de renderização para um dispositivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="ae307-106">The ListRenderingCapabilityInformation function, the SupportsFunctionalCategory helper function, and the ReadProfileInformationProperties helper function in the DeviceCapabilities.cpp module demonstrate the retrieval of rendering capabilities for a selected device.</span></span>

<span data-ttu-id="ae307-107">Seu aplicativo pode recuperar os recursos de renderização com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae307-107">Your application can retrieve the rendering capabilities supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="ae307-108">Interface</span><span class="sxs-lookup"><span data-stu-id="ae307-108">Interface</span></span>                                                                                      | <span data-ttu-id="ae307-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae307-109">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="ae307-110">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="ae307-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="ae307-111">Fornece acesso à interface IPortableDeviceProperties.</span><span class="sxs-lookup"><span data-stu-id="ae307-111">Provides access to the IPortableDeviceProperties interface.</span></span> |
| [<span data-ttu-id="ae307-112">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="ae307-112">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="ae307-113">Fornece acesso aos métodos específicos da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ae307-113">Provides access to the property-specific methods.</span></span>           |
| [<span data-ttu-id="ae307-114">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="ae307-114">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="ae307-115">Usado para armazenar as chaves de propriedade para o perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="ae307-115">Used to store the property keys for the given profile.</span></span>      |
| [<span data-ttu-id="ae307-116">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="ae307-116">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="ae307-117">Usado armazena os valores de propriedade para o perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="ae307-117">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="ae307-118">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ae307-118">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="ae307-119">Usado armazena os valores de propriedade para o perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="ae307-119">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="ae307-120">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="ae307-120">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="ae307-121">Usado armazena os valores de propriedade para o perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="ae307-121">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="ae307-122">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="ae307-122">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="ae307-123">Usado armazena os valores de propriedade para o perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="ae307-123">Used store the property values for the given profile.</span></span>       |



 

<span data-ttu-id="ae307-124">Uma das primeiras tarefas realizadas pelo aplicativo de exemplo é determinar se o dispositivo selecionado é capaz de listar os recursos de renderização.</span><span class="sxs-lookup"><span data-stu-id="ae307-124">One of the first tasks accomplished by the sample application is to determine whether the selected device is capable of listing rendering capabilities.</span></span> <span data-ttu-id="ae307-125">A função auxiliar SupportsFunctionalCategory determina se esse é o caso chamando a função auxiliar ListRenderingCapabilityInformation e passando informações de \_ \_ renderização de categoria funcional WPD \_ \_ como o segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="ae307-125">The SupportsFunctionalCategory helper function determines whether this is the case by calling the ListRenderingCapabilityInformation helper function and passing WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION as the second argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SupportsFunctionalCategory(pDevice, WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION) == FALSE)
{
    printf("This device does not support device rendering information to display\n");
    return;
}
```



<span data-ttu-id="ae307-126">Se o dispositivo for capaz de listar os recursos de renderização, a próxima etapa envolve a recuperação de um objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) e a invocação do método [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) para recuperar um identificador de objeto para o objeto de informações de renderização.</span><span class="sxs-lookup"><span data-stu-id="ae307-126">If the device is capable of listing rendering capabilities, the next step entails retrieving an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object and invoking the [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method to retrieve an object identifier for the rendering-information object.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get the functional object identifier for the rendering information object
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalObjects(WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION, &pRenderingInfoObjects);
    if (FAILED(hr))
    {
        printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="ae307-127">A próxima etapa é armazenar o identificador de objeto de informações de renderização que acabou de ser recuperado em uma variável de cadeia de caracteres (strRenderingInfoObjectID) e, em seguida, chamar a função auxiliar ReadProfileInformationProperties.</span><span class="sxs-lookup"><span data-stu-id="ae307-127">The next step is to store the rendering-information object identifier that was just retrieved in a string variable (strRenderingInfoObjectID), and then to call the ReadProfileInformationProperties helper function.</span></span> <span data-ttu-id="ae307-128">(A variável, strRenderingInfoObjectID, é passada como o segundo argumento para a função auxiliar.)</span><span class="sxs-lookup"><span data-stu-id="ae307-128">(The variable, strRenderingInfoObjectID, is passed as the second argument to the helper function.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SUCCEEDED(hr))
{
    PROPVARIANT pv = {0};
    PropVariantInit(&pv);
    hr = pRenderingInfoObjects->GetAt(0, &pv);
    if ((SUCCEEDED(hr))    &&
        (pv.vt== VT_LPWSTR) )
    {
        strRenderingInfoObjectID = pv.pwszVal;
    }
    else
    {
        printf("! Failed to get first rendering object's identifier, hr = 0x%lx\n", hr);
    }

    PropVariantClear(&pv);
}

if (SUCCEEDED(hr))
{
    hr = ReadProfileInformationProperties(pDevice,
                                          strRenderingInfoObjectID,
                                          &pRenderingInfoProfiles);
    // Error output statements are performed by the helper function, so they
    // are omitted here.
}
```



<span data-ttu-id="ae307-129">Uma das primeiras tarefas realizadas pela função auxiliar é recuperar um objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , que será usado para acessar os métodos específicos do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ae307-129">One of the first tasks accomplished by the helper function is to retrieve an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to access the content-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="ae307-130">Em seguida, a função auxiliar recupera um objeto [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) , que será usado para acessar os métodos específicos da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ae307-130">Next, the helper function retrieves an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) object, which it will use to access the property-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="ae307-131">A próxima etapa é criar um objeto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) no qual as chaves de propriedade das informações de renderização são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="ae307-131">The next step is to create an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object into which the property keys for the rendering information are stored.</span></span> <span data-ttu-id="ae307-132">Depois que o objeto é criado, o método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) é invocado para adicionar as chaves necessárias.</span><span class="sxs-lookup"><span data-stu-id="ae307-132">Once the object is created, the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method is invoked to add the necessary keys.</span></span> <span data-ttu-id="ae307-133">(É necessário adicionar essas chaves para que os perfis de renderização correspondentes possam ser recuperados nas etapas subsequentes.)</span><span class="sxs-lookup"><span data-stu-id="ae307-133">(It is necessary to add these keys so that the corresponding rendering profiles can be retrieved in the subsequent steps.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IPortableDeviceKeyCollection,
                      (VOID**) &pPropertiesToRead);
if (SUCCEEDED(hr))
{
    // Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_RENDERING_INFORMATION_PROFILES);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_RENDERING_INFORMATION_PROFILES to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="ae307-134">A próxima etapa é recuperar os valores de Propriedade do driver de dispositivo chamando o método [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) .</span><span class="sxs-lookup"><span data-stu-id="ae307-134">The next step is to retrieve the property values from the device driver by calling the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(wszFunctionalObjectID, // The object whose properties we are reading
                                pPropertiesToRead,     // The properties we want to read
                                &pObjectProperties);   // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", wszFunctionalObjectID, hr);
    }
}
```



<span data-ttu-id="ae307-135">A próxima etapa recupera o perfil de informações de renderização e o armazena no argumento ppRenderingInfoProfiles.</span><span class="sxs-lookup"><span data-stu-id="ae307-135">The next step retrieves the rendering-information profile and stores it in the ppRenderingInfoProfiles argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pObjectProperties->GetIPortableDeviceValuesCollectionValue(WPD_RENDERING_INFORMATION_PROFILES,
                                                                    &pRenderingInfoProfiles);
    if (FAILED(hr))
    {
        printf("! Failed to get WPD_RENDERING_INFORMATION_PROFILES from rendering information, hr= 0x%lx\n",  hr);
    }
}

// QueryInterface the interface into the out-going parameters.
if (SUCCEEDED(hr))
{
    hr = pRenderingInfoProfiles->QueryInterface(IID_PPV_ARGS(ppRenderingInfoProfiles));
    if (FAILED(hr))
    {
        printf("! Failed to QueryInterface for IPortableDeviceValuesCollection (Rendering information profiles), hr= 0x%lx\n",  hr);
    }
}
```



<span data-ttu-id="ae307-136">Depois que a função auxiliar lê as \_ Propriedades de perfis de informações de RENDERIZAÇÃO WPD \_ \_ , os perfis de renderização são exibidos.</span><span class="sxs-lookup"><span data-stu-id="ae307-136">After the helper function reads the WPD\_RENDERING\_INFORMATION\_PROFILES properties, the rendering profiles are displayed.</span></span> <span data-ttu-id="ae307-137">Esses perfis são exibidos pela função auxiliar DisplayRenderingProfile.</span><span class="sxs-lookup"><span data-stu-id="ae307-137">These profiles are displayed by the DisplayRenderingProfile helper function.</span></span>


```C++
void DisplayRenderingProfile(
    IPortableDeviceValues* pProfile)
{
    HRESULT hr = S_OK;
    if (pProfile == NULL)
    {
        return;
    }

    if (SUCCEEDED(hr))
    {
        DWORD dwTotalBitrate    = 0;
        DWORD dwChannelCount    = 0;
        DWORD dwAudioFormatCode = 0;
        GUID  guidFormat        = WPD_OBJECT_FORMAT_UNSPECIFIED;

        // Display WPD_MEDIA_TOTAL_BITRATE
        hr = pProfile->GetUnsignedIntegerValue(WPD_MEDIA_TOTAL_BITRATE, &dwTotalBitrate);
        if (SUCCEEDED(hr))
        {
            printf("Total Bitrate: %d\n", dwTotalBitrate);
        }

        // If we fail to read the total bitrate as a single value, then it must be
        // a valid value set.  (i.e. returning IPortableDeviceValues as the value which
        // contains properties describing the valid values for this property.)
        if (hr == DISP_E_TYPEMISMATCH)
        {
            CComPtr<IPortableDeviceValues> pExpectedValues;
            hr = pProfile->GetIPortableDeviceValuesValue(WPD_MEDIA_TOTAL_BITRATE, &pExpectedValues);
            if (SUCCEEDED(hr))
            {
                printf("Total Bitrate: ");
                DisplayExpectedValues(pExpectedValues);
            }
        }

        // If we are still a failure here, report the error
        if (FAILED(hr))
        {

            printf("! Failed to get WPD_MEDIA_TOTAL_BITRATE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_CHANNEL_COUNT
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_CHANNEL_COUNT, &dwChannelCount);
        if (SUCCEEDED(hr))
        {
            printf("Channel Count: %d\n", dwChannelCount);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_CHANNEL_COUNT from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_FORMAT_CODE
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_FORMAT_CODE,   &dwAudioFormatCode);
        if (SUCCEEDED(hr))
        {
            printf("Audio Format Code: %d\n", dwAudioFormatCode);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_FORMAT_CODE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_OBJECT_FORMAT
        hr = pProfile->GetGuidValue(WPD_OBJECT_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("Object Format: %ws\n", (LPWSTR)CComBSTR(guidFormat));
        }
        else
        {
            printf("! Failed to get WPD_OBJECT_FORMAT from rendering profile, hr = 0x%lx\n",hr);
        }
    }
}
```



<span data-ttu-id="ae307-138">Observe que, como os perfis de renderização são estáticos, seu aplicativo pode optar por ler os perfis e armazená-los localmente (em vez de acessar o dispositivo cada vez que os dados forem necessários).</span><span class="sxs-lookup"><span data-stu-id="ae307-138">Note that since the rendering profiles are static, your application may choose to read the profiles and store them locally (instead of accessing the device each time the data is needed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae307-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae307-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae307-140">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="ae307-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="ae307-141">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ae307-141">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="ae307-142">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="ae307-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="ae307-143">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="ae307-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="ae307-144">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="ae307-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="ae307-145">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="ae307-145">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> <dt>

[<span data-ttu-id="ae307-146">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="ae307-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



