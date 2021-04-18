---
description: Gravando Propriedades do objeto
ms.assetid: f762a571-83ea-4999-ad49-a51044bc790d
title: Gravando Propriedades do objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb061288cbfde93f2baea1860581c25c61a8a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752154"
---
# <a name="writing-object-properties"></a><span data-ttu-id="cd703-103">Gravando Propriedades do objeto</span><span class="sxs-lookup"><span data-stu-id="cd703-103">Writing Object Properties</span></span>

<span data-ttu-id="cd703-104">Os serviços geralmente contêm objetos filho que pertencem a um dos formatos aos quais cada serviço dá suporte.</span><span class="sxs-lookup"><span data-stu-id="cd703-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="cd703-105">Por exemplo, um serviço de contatos pode dar suporte a vários objetos de contato do formato de contato abstrato.</span><span class="sxs-lookup"><span data-stu-id="cd703-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="cd703-106">Cada objeto de contato é descrito pelas propriedades relacionadas (nome do contato, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="cd703-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="cd703-107">O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode atualizar a propriedade Name para um objeto filho do serviço Contacts fornecido.</span><span class="sxs-lookup"><span data-stu-id="cd703-107">The WpdServicesApiSample application includes code that demonstrates how an application can update the name property for a child object of the given Contacts service.</span></span> <span data-ttu-id="cd703-108">Este exemplo usa as seguintes interfaces WPD.</span><span class="sxs-lookup"><span data-stu-id="cd703-108">This sample uses the following WPD interfaces.</span></span>



|                                                                |                                                                                                                                                                      |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd703-109">Interface</span><span class="sxs-lookup"><span data-stu-id="cd703-109">Interface</span></span>                                                      | <span data-ttu-id="cd703-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd703-110">Description</span></span>                                                                                                                                                          |
| [<span data-ttu-id="cd703-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="cd703-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)       | <span data-ttu-id="cd703-112">Usado para recuperar a interface **IPortableDeviceContent2** para acessar os métodos de serviço com suporte.</span><span class="sxs-lookup"><span data-stu-id="cd703-112">Used to retrieve the **IPortableDeviceContent2** interface to access the supported service methods.</span></span>                                                                  |
| [<span data-ttu-id="cd703-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="cd703-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)     | <span data-ttu-id="cd703-114">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cd703-114">Provides access to the content-specific methods.</span></span>                                                                                                                     |
| [<span data-ttu-id="cd703-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="cd703-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="cd703-116">Usado para gravar os valores de propriedade de objeto e para determinar se uma determinada propriedade pode ser gravada</span><span class="sxs-lookup"><span data-stu-id="cd703-116">Used to write the object property values and to determine whether a given property can be written</span></span>                                                                    |
| [<span data-ttu-id="cd703-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="cd703-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="cd703-118">Usado para manter os valores de propriedade a serem gravados, determinar os resultados da operação de gravação e recuperar atributos de Propriedades (ao determinar o recurso de gravação).</span><span class="sxs-lookup"><span data-stu-id="cd703-118">Used to hold the property values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="cd703-119">Quando o usuário escolhe a opção "8" na linha de comando, o aplicativo invoca o método **WriteContentProperties** encontrado no módulo contentproperties. cpp.</span><span class="sxs-lookup"><span data-stu-id="cd703-119">When the user chooses option "8" at the command line, the application invokes the **WriteContentProperties** method that is found in the ContentProperties.cpp module.</span></span> <span data-ttu-id="cd703-120">Esse método solicita que o usuário insira um identificador de objeto para a propriedade a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="cd703-120">This method prompts the user to enter an object identifier for the property to be updated.</span></span> <span data-ttu-id="cd703-121">O usuário identifica o objeto e o método solicita que o usuário especifique um novo nome.</span><span class="sxs-lookup"><span data-stu-id="cd703-121">The user identifies the object, and the method prompts the user to specify a new name.</span></span> <span data-ttu-id="cd703-122">Depois que esse nome for especificado, o método atualizará a propriedade Name para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="cd703-122">After this name is specified, the method updates the Name property for the given object.</span></span>

<span data-ttu-id="cd703-123">Observe que, antes de gravar as propriedades do objeto, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="cd703-123">Note that prior to writing the object properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="cd703-124">O código a seguir para o método **WriteContentProperties** demonstra como o aplicativo usa a interface [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) para recuperar uma interface [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) .</span><span class="sxs-lookup"><span data-stu-id="cd703-124">The following code for the **WriteContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="cd703-125">Ao passar o PROPERTYKEYS das propriedades solicitadas para o método [**IPortableDeviceProperties:: SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , o **WriteContentProperties** atualiza a propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="cd703-125">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **WriteContentProperties** updates the name property.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cd703-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd703-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd703-127">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="cd703-127">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="cd703-128">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="cd703-128">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="cd703-129">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="cd703-129">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



