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
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a>Recuperando os recursos de renderização suportados por um dispositivo

Os dispositivos portáteis do Windows que dão suporte à categoria funcional informações de renderização ( \_ informações de renderização da categoria funcional de WPD \_ \_ \_ ) retornarão informações de renderização quando consultados. As informações de renderização descrevem os requisitos e as restrições impostas em aplicativos que tentam gravar conteúdo em um dispositivo.

A função ListRenderingCapabilityInformation, a função auxiliar SupportsFunctionalCategory e a função auxiliar ReadProfileInformationProperties no módulo DeviceCapabilities. cpp demonstram a recuperação de recursos de renderização para um dispositivo selecionado.

Seu aplicativo pode recuperar os recursos de renderização com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornece acesso à interface IPortableDeviceProperties. |
| [**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Fornece acesso aos métodos específicos da propriedade.           |
| [**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Usado para armazenar as chaves de propriedade para o perfil especificado.      |
| [**Interface IPortableDeviceValues**](iportabledevicevalues.md)                               | Usado armazena os valores de propriedade para o perfil especificado.       |
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Usado armazena os valores de propriedade para o perfil especificado.       |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usado armazena os valores de propriedade para o perfil especificado.       |
| [**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)           | Usado armazena os valores de propriedade para o perfil especificado.       |



 

Uma das primeiras tarefas realizadas pelo aplicativo de exemplo é determinar se o dispositivo selecionado é capaz de listar os recursos de renderização. A função auxiliar SupportsFunctionalCategory determina se esse é o caso chamando a função auxiliar ListRenderingCapabilityInformation e passando informações de \_ \_ renderização de categoria funcional WPD \_ \_ como o segundo argumento.


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



Se o dispositivo for capaz de listar os recursos de renderização, a próxima etapa envolve a recuperação de um objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) e a invocação do método [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) para recuperar um identificador de objeto para o objeto de informações de renderização.


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



A próxima etapa é armazenar o identificador de objeto de informações de renderização que acabou de ser recuperado em uma variável de cadeia de caracteres (strRenderingInfoObjectID) e, em seguida, chamar a função auxiliar ReadProfileInformationProperties. (A variável, strRenderingInfoObjectID, é passada como o segundo argumento para a função auxiliar.)


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



Uma das primeiras tarefas realizadas pela função auxiliar é recuperar um objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , que será usado para acessar os métodos específicos do conteúdo.


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



Em seguida, a função auxiliar recupera um objeto [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) , que será usado para acessar os métodos específicos da propriedade.


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



A próxima etapa é criar um objeto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) no qual as chaves de propriedade das informações de renderização são armazenadas. Depois que o objeto é criado, o método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) é invocado para adicionar as chaves necessárias. (É necessário adicionar essas chaves para que os perfis de renderização correspondentes possam ser recuperados nas etapas subsequentes.)


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



A próxima etapa é recuperar os valores de Propriedade do driver de dispositivo chamando o método [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) .


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



A próxima etapa recupera o perfil de informações de renderização e o armazena no argumento ppRenderingInfoProfiles.


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



Depois que a função auxiliar lê as \_ Propriedades de perfis de informações de RENDERIZAÇÃO WPD \_ \_ , os perfis de renderização são exibidos. Esses perfis são exibidos pela função auxiliar DisplayRenderingProfile.


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



Observe que, como os perfis de renderização são estáticos, seu aplicativo pode optar por ler os perfis e armazená-los localmente (em vez de acessar o dispositivo cada vez que os dados forem necessários).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



