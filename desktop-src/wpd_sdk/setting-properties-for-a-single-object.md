---
description: Definindo propriedades para um único objeto
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: Definindo propriedades para um único objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5649d05ccadfeaef0dd8805abd7d556f7725f175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798172"
---
# <a name="setting-properties-for-a-single-object"></a><span data-ttu-id="b59cc-103">Definindo propriedades para um único objeto</span><span class="sxs-lookup"><span data-stu-id="b59cc-103">Setting Properties for a Single Object</span></span>

<span data-ttu-id="b59cc-104">Depois que o aplicativo recupera um identificador de objeto (consulte o tópico [enumerando conteúdo](enumerating-content.md) ) para um determinado objeto, ele pode definir propriedades para esse objeto chamando métodos nas interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b59cc-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can set properties for that object by calling methods in the interfaces described in the following table.</span></span>



| <span data-ttu-id="b59cc-105">Interface</span><span class="sxs-lookup"><span data-stu-id="b59cc-105">Interface</span></span>                                                                | <span data-ttu-id="b59cc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b59cc-106">Description</span></span>                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b59cc-107">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="b59cc-107">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="b59cc-108">Usado para determinar se uma determinada propriedade pode ser gravada e para enviar a operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="b59cc-108">Used to determine whether a given property can be written and to send the write operation.</span></span>                                                                  |
| [<span data-ttu-id="b59cc-109">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="b59cc-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="b59cc-110">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b59cc-110">Provides access to the content-specific methods.</span></span>                                                                                                            |
| [<span data-ttu-id="b59cc-111">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b59cc-111">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="b59cc-112">Usado para armazenar os valores a serem gravados, determinar os resultados da operação de gravação e recuperar atributos de Propriedades (ao determinar a capacidade de gravação).</span><span class="sxs-lookup"><span data-stu-id="b59cc-112">Used to hold the values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="b59cc-113">Os aplicativos definem propriedades em um objeto primeiro criando um recipiente de propriedades que especifica os novos valores usando a [**interface IPortableDeviceValues**](iportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="b59cc-113">Applications set properties on an object by first creating a property bag that specifies the new values using the [**IPortableDeviceValues interface**](iportabledevicevalues.md).</span></span> <span data-ttu-id="b59cc-114">Depois que o recipiente de propriedades é criado, um aplicativo define essas propriedades chamando o método [**IPortableDeviceProperties:: SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) .</span><span class="sxs-lookup"><span data-stu-id="b59cc-114">Once the property bag is created, an application sets those properties by calling the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) method.</span></span>

<span data-ttu-id="b59cc-115">A `WriteContentProperties` função no módulo contentproperties. cpp do aplicativo de exemplo demonstra como um aplicativo pode definir uma nova propriedade de nome de objeto para um objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="b59cc-115">The `WriteContentProperties` function in the sample application's ContentProperties.cpp module demonstrates how an application could set a new object-name property for a selected object.</span></span>

<span data-ttu-id="b59cc-116">A primeira tarefa realizada pela `WriteContentProperties` função é solicitar ao usuário que insira um identificador de objeto para o objeto para o qual o aplicativo irá gravar o novo nome.</span><span class="sxs-lookup"><span data-stu-id="b59cc-116">The first task accomplished by the `WriteContentProperties` function is to prompt the user to enter an object identifier for the object that the application will write the new name for.</span></span>


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



<span data-ttu-id="b59cc-117">Depois disso, o aplicativo recupera o \_ atributo de propriedade WPD \_ \_ pode \_ gravar valor para a \_ propriedade de nome de objeto WPD \_ para determinar se a propriedade pode ser gravada.</span><span class="sxs-lookup"><span data-stu-id="b59cc-117">After this, the application retrieves the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value for the WPD\_OBJECT\_NAME property to determine whether the property can be written.</span></span> <span data-ttu-id="b59cc-118">(Observe que seu aplicativo pode definir qualquer propriedade para a qual o WPD \_ O \_ atributo de propriedade \_ pode \_ gravar valor é true.)</span><span class="sxs-lookup"><span data-stu-id="b59cc-118">(Note that your application could set any property for which the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value is true.)</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



<span data-ttu-id="b59cc-119">A próxima etapa é solicitar ao usuário a nova cadeia de caracteres de nome.</span><span class="sxs-lookup"><span data-stu-id="b59cc-119">The next step is to prompt the user for the new name string.</span></span> <span data-ttu-id="b59cc-120">(Observe que a chamada para o método [**IPortableDeviceValues:: SetStringValue**](iportabledevicevalues-setstringvalue.md) simplesmente cria o recipiente de propriedades; a propriedade real ainda não foi gravada.)</span><span class="sxs-lookup"><span data-stu-id="b59cc-120">(Note that the call to the [**IPortableDeviceValues::SetStringValue**](iportabledevicevalues-setstringvalue.md) method merely creates the property bag; the actual property has not been written yet.)</span></span>


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



<span data-ttu-id="b59cc-121">Por fim, o novo valor, especificado pelo usuário, é aplicado ao objeto.</span><span class="sxs-lookup"><span data-stu-id="b59cc-121">Finally, the new value, specified by the user, is applied to the object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="b59cc-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b59cc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b59cc-123">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="b59cc-123">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="b59cc-124">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="b59cc-124">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="b59cc-125">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="b59cc-125">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="b59cc-126">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="b59cc-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="b59cc-127">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="b59cc-127">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="b59cc-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b59cc-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="b59cc-129">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="b59cc-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



