---
description: Enumerando conteúdo
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Enumerando conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759009"
---
# <a name="enumerating-content"></a>Enumerando conteúdo

O conteúdo em um dispositivo (se esse conteúdo é uma pasta, um catálogo de telefones, um vídeo ou uma imagem ainda) é chamado de objeto na API WPD. Esses objetos são referenciados por identificadores de objeto e descritos por propriedades. Você pode enumerar os objetos em um dispositivo chamando métodos na [**interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), na interface [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)e na [**interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).

O aplicativo de exemplo demonstra a enumeração de conteúdo na função EnumerateAllContent que é encontrada no módulo ContentEnumeration. cpp. Essa função, por sua vez, chama uma função RecursiveEnumerate que percorre a hierarquia de objetos encontrados no dispositivo selecionado e retorna um identificador de objeto para cada objeto.

Como observado, a função RecursiveEnumerate recupera um identificador de objeto para cada objeto encontrado no dispositivo. O identificador de objeto é um valor de cadeia de caracteres. Depois que o aplicativo recupera esse identificador, ele pode obter informações de objeto mais descritivas (como o nome do objeto, o identificador para o pai do objeto e assim por diante). Essas informações descritivas são chamadas de propriedades de objeto (ou metadados). Seu aplicativo pode recuperar essas propriedades chamando membros da [**interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).

A função EnumerateAllContent começa recuperando um ponteiro para uma [**interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent). Ele recupera esse ponteiro chamando o método [**IPortableDevice:: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



Depois de recuperar o ponteiro para a interface IPortableDeviceContent, a função EnumerateAllContent chama a função RecursiveEnumerate, que percorre a hierarquia de objetos encontrados no dispositivo fornecido e retorna um identificador de objeto para cada um.

A função RecursiveEnumerate começa recuperando um ponteiro para uma [**interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids). Essa interface expõe os métodos que um aplicativo usa para navegar na lista de objetos encontrados em um determinado dispositivo.

Neste exemplo, a função RecursiveEnumerate chama o método [**IEnumPortableDeviceObjectIDs:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) para atravessar a lista de objetos.

Cada chamada para o método [**IEnumPortableDeviceObjects:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) solicita um lote de 10 identificadores. (Esse valor é especificado pelo número \_ OBJETOS \_ para \_ solicitar constante que é fornecida como o primeiro argumento.)


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



