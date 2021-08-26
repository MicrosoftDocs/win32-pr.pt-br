---
description: Recuperando propriedades de um único objeto
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Recuperando propriedades de um único objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0806de3da9cd3f0674057d413a071996f86f5d74a364c0f5db707965fc2220
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054716"
---
# <a name="retrieving-properties-for-a-single-object"></a>Recuperando propriedades de um único objeto

Depois que o aplicativo recupera um identificador de objeto (consulte o tópico [enumerando conteúdo](enumerating-content.md) ) para um determinado objeto, ele pode recuperar informações descritivas sobre esse objeto chamando métodos na [**interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) e na [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).

O método [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) recupera uma lista de propriedades especificadas para um determinado objeto. (O aplicativo também pode chamar o método GetValues e especificar um valor **nulo** para o parâmetro pKeys para recuperar todas as propriedades de um determinado objeto; no entanto, o desempenho desse método pode ser significativamente mais lento ao recuperar todas as propriedades.)

No entanto, antes que seu aplicativo chame GetValues, ele precisa identificar as propriedades a serem recuperadas definindo as chaves correspondentes em um [**objeto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md). Seu aplicativo identificará as propriedades de interesse chamando o método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) e fornecendo um valor PROPERTYKEY que identifica cada propriedade que será recuperada.

A função ReadContentProperties no módulo Contentproperties. cpp do aplicativo de exemplo demonstra como as cinco propriedades foram recuperadas para um objeto selecionado. A tabela a seguir descreve cada uma dessas propriedades e seu valor REFPROPERTYKEY correspondente.



| Propriedade                     | Descrição                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Identificador de objeto pai     | Uma cadeia de caracteres que especifica o identificador para o pai do objeto fornecido.                                                                            | \_ \_ ID pai do objeto WPD \_             |
| Nome do objeto                  | Uma cadeia de caracteres que especifica o nome do objeto fornecido.                                                                                            | \_nome do objeto WPD \_                   |
| Identificador exclusivo persistente | Uma cadeia de caracteres que especifica um identificador exclusivo para o objeto fornecido. (Esse identificador é persistente entre as sessões, ao contrário do identificador de objeto.) | \_ \_ \_ ID exclusiva persistente do objeto WPD \_ |
| Formato do objeto                | Um GUID (identificador global exclusivo) que especifica o formato do arquivo correspondente a um determinado objeto.                                       | \_formato de objeto WPD \_                 |
| Tipo de conteúdo do objeto          | Um GUID que especifica o tipo de conteúdo associado a um determinado objeto.                                                                        | \_tipo de \_ conteúdo de objeto WPD \_          |



 

O trecho a seguir da função ReadContentProperties demonstra como o aplicativo de exemplo usou a [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e o método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) para identificar as propriedades que ele recuperaria.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



Depois que o aplicativo de exemplo definir as chaves apropriadas, ele chamou o método [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) para recuperar os valores especificados para o objeto fornecido.


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



