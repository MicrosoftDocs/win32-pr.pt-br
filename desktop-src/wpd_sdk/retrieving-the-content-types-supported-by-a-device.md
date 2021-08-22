---
description: Recuperando os tipos de conteúdo com suporte de um dispositivo
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Recuperando os tipos de conteúdo com suporte de um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f85366374ec28ed44664a3b86edbee1e046e1a5ee4e331dbe041398bdc48a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083460"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a>Recuperando os tipos de conteúdo com suporte de um dispositivo

conforme observado no tópico [recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , Windows dispositivos portáteis podem dar suporte a uma ou mais categorias funcionais. Qualquer categoria funcional específica pode dar suporte a um ou mais tipos de conteúdo. Por exemplo, a categoria de armazenamento pode dar suporte a tipos de conteúdo de pasta, áudio e imagem.

Para obter uma descrição dos tipos de conteúdo com suporte no WPD, consulte o tópico [**\_ tipo de conteúdo WPD \_ \_ todos**](wpd-content-type-all.md) .

A função ListSupportedContentTypes no módulo DeviceCapabilities. cpp demonstra a recuperação de tipos de conteúdo para as categorias funcionais com suporte de um dispositivo selecionado.

Seu aplicativo pode recuperar as categorias funcionais com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornece acesso aos métodos de recuperação de categoria funcional. |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usado para enumerar e armazenar dados de categoria funcional.         |



 

O código encontrado na função ListSupportedContentTypes é quase idêntico ao código encontrado na função ListFunctionalCategories. (Consulte o tópico [recuperando categorias funcionais com suporte em um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) .) A única diferença é a chamada para o método [**IPortableDeviceCapabilities:: GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) , que aparece dentro do loop que itera pelas categorias funcionais.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



