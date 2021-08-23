---
description: Recuperando os identificadores de objeto funcional para um dispositivo
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Recuperando os identificadores de objeto funcional para um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d0cc686a6997c10e26e3d83190503bba09fe15afc7f4e0cf75e297f0d905f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262996"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a>Recuperando os identificadores de objeto funcional para um dispositivo

conforme observado no tópico [recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , Windows dispositivos portáteis podem dar suporte a uma ou mais categorias funcionais. Qualquer categoria funcional específica pode dar suporte a um ou mais objetos funcionais. Por exemplo, a categoria de armazenamento pode dar suporte a três objetos de armazenamento funcional, cada um dos quais é identificado por uma cadeia de caracteres de identificador exclusivo. O primeiro objeto de armazenamento pode ser identificado pela cadeia de caracteres "Storage1", o segundo pela cadeia de caracteres "Storage2" e o terceiro pela cadeia de caracteres "Storage3".

A função ListFunctionalObjects no módulo DeviceCapabilities. cpp demonstra a recuperação de tipos de conteúdo para as categorias funcionais com suporte de um dispositivo selecionado.

Seu aplicativo pode recuperar as categorias funcionais com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornece acesso aos métodos de recuperação de categoria funcional. |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usado para enumerar e armazenar dados de categoria funcional.         |



 

O código encontrado na função ListFunctionalObjects é quase idêntico ao código encontrado na função ListFunctionalCategories. (Consulte o tópico [recuperando categorias funcionais com suporte em um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) .) A única diferença é a chamada para o método [**IPortableDeviceCapabilities:: GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) , que aparece dentro do loop que itera pelas categorias funcionais.


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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

 

 



