---
description: Recuperando formatos de serviço com suporte
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Recuperando formatos de serviço com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766491"
---
# <a name="retrieving-supported-service-formats"></a>Recuperando formatos de serviço com suporte

O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode recuperar os formatos com suporte de um determinado serviço Contacts chamando métodos das interfaces na tabela a seguir.



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interface                                                                            | Descrição                                                                                           |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Usado para recuperar a interface **IPortableDeviceServiceCapabilities** para acessar os eventos com suporte. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fornece acesso aos eventos e atributos de evento com suporte.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contém a lista de formatos com suporte.                                                               |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contém os atributos de um determinado formato.                                                           |



 

Quando o usuário escolhe a opção "3" na linha de comando, o aplicativo invoca o método **ListSupportedFormats** encontrado no módulo percapabilities. cpp.

Observe que, antes de recuperar a lista de eventos, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.

Em WPD, um formato é descrito por atributos que especificam o nome e (opcionalmente) o tipo MIME de um determinado formato. Esses atributos são definidos no arquivo de cabeçalho thePortableDevice. h. Para obter uma descrição dos atributos com suporte, consulte o tópico [atributos](attributes.md) .

No caso do aplicativo de exemplo, se o WpdServiceSampleDriver for o único dispositivo instalado, o driver retornará dois formatos com suporte para seu serviço de contato: "AbstractContactFormat" e "VCard2Format". Esses formatos correspondem ao **\_ \_ \_ \_ contato abstrato do formato de objeto WPD** e aos atributos **\_ \_ \_ VCARD2 de formato de objeto WPD** encontrados em PortableDevice. h.

Dois métodos no módulo percapabilities. cpp oferecem suporte à recuperação de formatos com suporte para o serviço de contatos: **ListSupportedFormats** e **DisplayFormat**. O primeiro recupera o identificador GUID para cada formato com suporte. O último converte esse GUID em uma cadeia de caracteres amigável.

O método **ListSupportedFormats** invoca o método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Usando essa interface, ele recupera os formatos com suporte chamando o método [**IPortableDeviceServiceCapabilities:: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) . O método **GetSupportedFormats** recupera o GUID para cada formato suportado pelo serviço e copia esse GUID em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

O código a seguir usa o método **ListSupportedFormats** .


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



Depois que o método **ListSupportedFormats** recupera o GUID para cada formato suportado pelo serviço fornecido, ele invoca o método **DisplayFormat** para exibir o nome amigável do script para cada formato; por exemplo, "VCard2".

O método **DisplayFormat** invoca o método [**IPortableDeviceServiceCapabilities:: getformatattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) recuperar uma coleção de atributos para o GUID de formato fornecido. Em seguida, ele chama o método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) e solicita que o driver retorne um nome amigável para o script para o formato fornecido.

O código a seguir usa o método **DisplayFormat** .


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



