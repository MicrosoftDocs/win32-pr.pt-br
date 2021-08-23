---
description: Escrevendo propriedades de objeto
ms.assetid: f762a571-83ea-4999-ad49-a51044bc790d
title: Escrevendo propriedades de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e140563c6cf17235d3709e0d53cbfda9ab602076c3e72c010570b004429c96e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657326"
---
# <a name="writing-object-properties"></a>Escrevendo propriedades de objeto

Os serviços geralmente contêm objetos filho que pertencem a um dos formatos aos quais cada serviço dá suporte. Por exemplo, um serviço Contatos pode dar suporte a vários objetos de contato do formato Contato Abstrato. Cada objeto de contato é descrito por propriedades relacionadas (nome de contato, número de telefone, endereço de email e assim por diante).

O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode atualizar a propriedade name para um objeto filho do serviço Contacts determinado. Este exemplo usa as seguintes interfaces WPD.



| Interface                                                      | Descrição                                                                                                                                                          |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)       | Usado para recuperar a interface **IPortableDeviceContent2** para acessar os métodos de serviço com suporte.                                                                  |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)     | Fornece acesso aos métodos específicos do conteúdo.                                                                                                                     |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Usado para gravar os valores de propriedade do objeto e determinar se uma determinada propriedade pode ser escrita                                                                    |
| [**IPortableDeviceValues**](iportabledevicevalues.md)         | Usado para manter os valores de propriedade a serem gravados, determinar os resultados da operação de gravação e recuperar atributos de propriedades (ao determinar a capacidade de gravação). |



 

Quando o usuário escolhe a opção "8" na linha de comando, o aplicativo invoca o método **WriteContentProperties** encontrado no módulo ContentProperties.cpp. Esse método solicita que o usuário insira um identificador de objeto para que a propriedade seja atualizada. O usuário identifica o objeto e o método solicita que o usuário especifique um novo nome. Depois que esse nome é especificado, o método atualiza a propriedade Name para o objeto especificado.

Observe que, antes de escrever as propriedades do objeto, o aplicativo de exemplo abre um serviço Contatos em um dispositivo conectado.

O código a seguir para o método **WriteContentProperties** demonstra como o aplicativo usa a interface [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) para recuperar uma interface [**IPortableDeviceProperties.**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) Ao passar PROPERTYKEYS das propriedades solicitadas para o método [**IPortableDeviceProperties::SetValues,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) **WriteContentProperties** atualiza a propriedade name.


```C++
void WriteContentProperties(
 IPortableDeviceService* pService)
{
 if (pService == NULL)
 {
  printf("! A NULL IPortableDeviceService interface pointer was received\n");
  return;
 }

 HRESULT          hr       = S_OK;
 WCHAR         wszSelection[81]  = {0};
 WCHAR         wszNewObjectName[81] = {0};
 CComPtr<IPortableDeviceProperties> pProperties;
 CComPtr<IPortableDeviceContent2>   pContent;
 CComPtr<IPortableDeviceValues>  pObjectPropertiesToWrite;
 CComPtr<IPortableDeviceValues>  pPropertyWriteResults;
 CComPtr<IPortableDeviceValues>  pAttributes;
 BOOL          bCanWrite   = FALSE;

 // Prompt user to enter an object identifier on the device to write properties on.
 printf("Enter the identifer of the object you wish to write properties on.\n>");
 hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
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

 // 3) Check the property attributes to see if we can write/change the NAME_GenericObj_Name property.
 if (SUCCEEDED(hr))
 {
  hr = pProperties->GetPropertyAttributes(wszSelection,
            PKEY_GenericObj_Name,
            &pAttributes);
  if (SUCCEEDED(hr))
  {
   hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
   if (SUCCEEDED(hr))
   {
    if (bCanWrite)
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports TRUE\nThis means that the property can be changed/updated\n\n");
    }
    else
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports FALSE\nThis means that the property cannot be changed/updated\n\n");
    }
   }
   else
   {
    printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value for PKEY_GenericObj_Name on object '%ws', hr = 0x%lx\n", wszSelection, hr);
   }
  }
 }

 // 4) Prompt the user for the new value of the NAME_GenericObj_Name property only if the property attributes report
 // that it can be changed/updated.
 if (bCanWrite)
 {
  printf("Enter the new PKEY_GenericObj_Name property for the object '%ws'.\n>",wszSelection);
  hr = StringCbGetsW(wszNewObjectName,sizeof(wszNewObjectName));
  if (FAILED(hr))
  {
   printf("An invalid PKEY_GenericObj_Name was specified, aborting property writing\n");
  }

  // 5) CoCreate an IPortableDeviceValues interface to hold the property values
  // we wish to write.
  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(CLSID_PortableDeviceValues,
          NULL,
          CLSCTX_INPROC_SERVER,
          IID_IPortableDeviceValues,
          (VOID**) &pObjectPropertiesToWrite);
   if (SUCCEEDED(hr))
   {
    if (pObjectPropertiesToWrite != NULL)
    {
     hr = pObjectPropertiesToWrite->SetStringValue(PKEY_GenericObj_Name, wszNewObjectName);
     if (FAILED(hr))
     {
      printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceValues, hr= 0x%lx\n", hr);
     }
    }
   }
  }

  // 6) Call SetValues() passing the collection of specified PROPERTYKEYs.
  if (SUCCEEDED(hr))
  {
   hr = pProperties->SetValues(wszSelection,      // The object whose properties we are reading
          pObjectPropertiesToWrite,   // The properties we want to read
          &pPropertyWriteResults); // Driver supplied property result values for the property read operation
   if (FAILED(hr))
   {
    printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", wszSelection, hr);
   }
   else
   {
    printf("The PKEY_GenericObj_Name property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", wszSelection);
   }
  }
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

 

 



