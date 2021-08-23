---
description: Recuperando os recursos de renderização com suporte por um dispositivo
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: Recuperando os recursos de renderização com suporte por um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b5e4fd09417585954ae205fc28fc8cf0e78ab02fdd3add616859b35b4237ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546226"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a>Recuperando os recursos de renderização com suporte por um dispositivo

Windows Dispositivos portáteis que suportam a categoria funcional de informações de renderização (INFORMAÇÕES DE RENDERIZAÇÃO DE CATEGORIA FUNCIONAL WPD) retornarão informações de renderização \_ \_ quando \_ \_ consultados. As informações de renderização descrevem os requisitos e restrições impostos aos aplicativos que tentam gravar conteúdo em um dispositivo.

A função ListRenderingCapabilityInformation, a função auxiliar SupportsFunctionalCategory e a função auxiliar ReadProfileInformationProperties no módulo DeviceCapabilities.cpp demonstram a recuperação de recursos de renderização para um dispositivo selecionado.

Seu aplicativo pode recuperar os recursos de renderização com suporte por um dispositivo usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [**IPortableDeviceContent Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornece acesso à interface IPortableDeviceProperties. |
| [**IPortableDeviceProperties Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Fornece acesso aos métodos específicos da propriedade.           |
| [**IPortableDeviceKeyCollection Interface**](iportabledevicekeycollection.md)                 | Usado para armazenar as chaves de propriedade para o perfil determinado.      |
| [**IPortableDeviceValues Interface**](iportabledevicevalues.md)                               | Usado para armazenar os valores de propriedade para o perfil determinado.       |
| [**IPortableDeviceCapabilities Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Usado para armazenar os valores de propriedade para o perfil determinado.       |
| [**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md) | Usado para armazenar os valores de propriedade para o perfil determinado.       |
| [**IPortableDeviceValuesCollection Interface**](iportabledevicevaluescollection.md)           | Usado para armazenar os valores de propriedade para o perfil determinado.       |



 

Uma das primeiras tarefas realizadas pelo aplicativo de exemplo é determinar se o dispositivo selecionado é capaz de listar recursos de renderização. A função auxiliar SupportsFunctionalCategory determina se esse é o caso chamando a função auxiliar ListRenderingCapabilityInformation e passando INFORMAÇÕES DE RENDERIZAÇÃO DE CATEGORIA FUNCIONAL WPD como o \_ \_ segundo \_ \_ argumento.


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



Se o dispositivo for capaz de listar recursos de renderização, a próxima etapa envolverá a recuperação de um objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) e a invocação do [**método GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) para recuperar um identificador de objeto para o objeto rendering-information.


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



A próxima etapa é armazenar o identificador de objeto rendering-information que acabou de ser recuperado em uma variável de cadeia de caracteres (strRenderingInfoObjectID) e, em seguida, chamar a função auxiliar ReadProfileInformationProperties. (A variável, strRenderingInfoObjectID, é passada como o segundo argumento para a função auxiliar.)


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



Uma das primeiras tarefas realizadas pela função auxiliar é recuperar um objeto [**IPortableDeviceContent,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) que será usado para acessar os métodos específicos do conteúdo.


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



Em seguida, a função auxiliar recupera um [**objeto IPortableDeviceProperties,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) que será usado para acessar os métodos específicos da propriedade.


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



A próxima etapa é criar um [**objeto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) no qual as chaves de propriedade para as informações de renderização são armazenadas. Depois que o objeto é criado, o método [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) é invocado para adicionar as chaves necessárias. (É necessário adicionar essas chaves para que os perfis de renderização correspondentes possam ser recuperados nas etapas subsequentes.)


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



A próxima etapa é recuperar os valores de propriedade do driver de dispositivo chamando o [**método IPortableDeviceProperties::GetValues.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues)


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



Depois que a função auxiliar ler as propriedades DE PERFIS DE INFORMAÇÕES DE RENDERIZAÇÃO \_ \_ WPD, os \_ perfis de renderização serão exibidos. Esses perfis são exibidos pela função auxiliar DisplayRenderingProfile.


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



Observe que, como os perfis de renderização são estáticos, seu aplicativo pode optar por ler os perfis e armazená-los localmente (em vez de acessar o dispositivo sempre que os dados são necessários).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDevice Interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDeviceContent Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection Interface**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**IPortableDeviceValuesCollection Interface**](iportabledevicevaluescollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



