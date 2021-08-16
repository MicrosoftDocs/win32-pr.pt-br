---
description: Recuperando as categorias funcionais com suporte de um dispositivo
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Recuperando as categorias funcionais com suporte de um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410788616cc20563b914a293afcd8e2bbbd87099f738ae21463d2092c620597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842688"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>Recuperando as categorias funcionais com suporte de um dispositivo

Windows Os dispositivos portáteis podem oferecer suporte a uma ou mais categorias funcionais. Essas categorias são descritas na tabela a seguir.



| Categoria                    | Descrição                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| Captura de áudio               | O dispositivo pode ser usado para gravar áudio.                                              |
| Informações de renderização       | O dispositivo fornece dados que descrevem os arquivos de mídia que são capazes de renderizar. |
| SMS (serviço de mensagens curtas) | O dispositivo dá suporte a mensagens de texto.                                                  |
| Captura de imagem ainda         | O dispositivo pode ser usado para capturar imagens ainda.                                      |
| Armazenamento                     | O dispositivo pode ser usado para armazenar arquivos.                                               |



 

A função ListFunctionalCategories no módulo DeviceCapabilities. cpp demonstra a recuperação de categorias funcionais para um dispositivo selecionado.

Seu aplicativo pode recuperar as categorias funcionais com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornece acesso aos métodos de recuperação de categoria funcional. |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usado para enumerar e armazenar dados de categoria funcional.         |



 

A primeira tarefa realizada pelo aplicativo de exemplo é a recuperação de um objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , que é usado para recuperar as categorias funcionais no dispositivo selecionado.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

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
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



As categorias recuperadas são armazenadas em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

A próxima etapa é a enumeração e a exibição das categorias com suporte. A primeira etapa que o aplicativo de exemplo realiza é recuperar a contagem de categorias com suporte. Em seguida, ele usa essa contagem para iterar por meio do objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém as categorias com suporte.


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
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

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
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

 

 



