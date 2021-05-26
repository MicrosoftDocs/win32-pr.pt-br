---
title: Recuperando as propriedades do objeto WPD
description: Recuperando propriedades do objeto
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c206b6e3afe75144ce10de615657e788d6d1c
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424056"
---
# <a name="retrieving-wpd-object-properties"></a>Recuperando as propriedades do objeto WPD

Os serviços geralmente contêm objetos filho que pertencem a um dos formatos aos quais cada serviço dá suporte. Por exemplo, um serviço de contatos pode dar suporte a vários objetos de contato do formato de contato abstrato. Cada objeto de contato é descrito pelas propriedades relacionadas (nome do contato, número de telefone, endereço de email e assim por diante).

O aplicativo WpdServiceApiSample inclui código que demonstra como um aplicativo pode recuperar as propriedades de objeto de conteúdo com suporte em um determinado serviço de contatos. Este exemplo usa as seguintes interfaces.



| Interface | Descrição    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Recupera a interface **IPortableDeviceContent2** para acessar os métodos de serviço com suporte. |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Fornece acesso aos métodos específicos de conteúdo.                                             |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | Recupera os valores de Propriedade do objeto.                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)               | Mantém os valores de propriedade que foram lidos para esse objeto.                                    |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) | Contém os parâmetros para um determinado método.                                                  |



 

Quando o usuário escolhe a opção "7" na linha de comando, o aplicativo invoca o método **ReadContentProperties** encontrado no módulo contentproperties. cpp.

Esse método recupera as quatro propriedades a seguir para o objeto de contato especificado.



| Propriedade                     | Descrição                                                                                                                                                                                                      | PROPERTYKEY dos Serviços de Dispositivos     | WPD \_ PROPERTYKEY equivalente         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| Identificador de objeto pai     | Uma cadeia de caracteres que especifica o identificador do pai do objeto especificado.                                                                                                                                            | PKEY \_ GenericObj \_ ParentID      | ID PAI \_ \_ DO OBJETO \_ WPD             |
| Nome do objeto                  | Uma cadeia de caracteres que especifica o nome do objeto especificado                                                                                                                                                             | Nome \_ GenericObj de PKEY \_          | NOME DO OBJETO WPD \_ \_                   |
| Identificador exclusivo persistente | Uma cadeia de caracteres que especifica um identificador exclusivo para o objeto especificado. Esse identificador é persistente entre sessões, ao contrário do identificador de objeto. Para serviços, isso precisa ser uma representação de cadeia de caracteres de um GUID. | PKEY \_ GenericObj \_ PersistentUID | ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD |
| Formato do objeto                | Um GUID (identificador global exclusivo) que especifica o formato do arquivo correspondente a um determinado objeto                                                                                                        | \_ObjectFormat de PKEY GenericObj \_  | FORMATO DE OBJETO WPD \_ \_                 |



 

-   ID pai
-   Name
-   PersistentUID
-   Formatar

Observe que, antes de recuperar as propriedades de conteúdo, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.

O código a seguir para o método **ReadContentProperties** demonstra como o aplicativo usa a interface [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) para recuperar uma interface [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) . Ao passar o PROPERTYKEYS das propriedades solicitadas para o método [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **ReadContentProperties** recupera os valores solicitados e os exibe na janela do console.


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



