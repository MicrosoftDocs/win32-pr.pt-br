---
description: Transferindo um objeto Properties-Only para o dispositivo
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Transferindo um objeto Properties-Only para o dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662805"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a><span data-ttu-id="f5a71-103">Transferindo um objeto Properties-Only para o dispositivo</span><span class="sxs-lookup"><span data-stu-id="f5a71-103">Transferring a Properties-Only Object to the Device</span></span>

<span data-ttu-id="f5a71-104">Embora o exemplo no tópico anterior tenha demonstrado a criação de conteúdo em um dispositivo que consiste em Propriedades e dados, este tópico se concentra na criação de um objeto somente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f5a71-104">While the example in the previous topic demonstrated the creation of content on a device consisting of both properties and data, this topic focuses on the creation of a properties-only object.</span></span>

<span data-ttu-id="f5a71-105">Transferências somente de propriedade são realizadas usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f5a71-105">Property-only transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="f5a71-106">Interface</span><span class="sxs-lookup"><span data-stu-id="f5a71-106">Interface</span></span>                                                          | <span data-ttu-id="f5a71-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5a71-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f5a71-108">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="f5a71-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | <span data-ttu-id="f5a71-109">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f5a71-109">Provides access to the content-specific methods.</span></span>       |
| [<span data-ttu-id="f5a71-110">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f5a71-110">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)   | <span data-ttu-id="f5a71-111">Usado para recuperar propriedades que descrevem o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f5a71-111">Used to retrieve properties that describe the content.</span></span> |



 

<span data-ttu-id="f5a71-112">A `TransferContactToDevice` função no módulo ContentTransfer. cpp do aplicativo de exemplo demonstra como um aplicativo pode transferir informações de contato de um PC para um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="f5a71-112">The `TransferContactToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a PC to a connected device.</span></span> <span data-ttu-id="f5a71-113">Neste exemplo específico, o nome do contato transferido é um "John Kane" embutido em código e o número de telefone de contato transferido é sempre "425-555-0123".</span><span class="sxs-lookup"><span data-stu-id="f5a71-113">In this particular sample, the transferred contact name is a hard-coded "John Kane" and the transferred contact phone number is always "425-555-0123".</span></span>

<span data-ttu-id="f5a71-114">A primeira tarefa realizada pela `TransferContactToDevice` função é solicitar que o usuário insira um identificador de objeto para o objeto pai no dispositivo (sob o qual o conteúdo será transferido).</span><span class="sxs-lookup"><span data-stu-id="f5a71-114">The first task accomplished by the `TransferContactToDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="f5a71-115">A próxima etapa é a recuperação das propriedades de contato, que serão usadas quando o exemplo gravar o novo contato no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5a71-115">The next step is the retrieval of contact properties, which will be used when the sample writes the new contact to the device.</span></span> <span data-ttu-id="f5a71-116">A recuperação de propriedades de contato é executada pela `GetRequiredPropertiesForPropertiesOnlyContact` função auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f5a71-116">The retrieval of contact properties is performed by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function.</span></span>


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="f5a71-117">Essa função grava os dados a seguir em um objeto **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="f5a71-117">This function writes the following data to an **IPortableDeviceValues** object.</span></span>

-   <span data-ttu-id="f5a71-118">O identificador de objeto para o pai do contato no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5a71-118">The object identifier for the contact's parent on the device.</span></span> <span data-ttu-id="f5a71-119">(Esse é o destino onde o dispositivo armazenará o objeto.)</span><span class="sxs-lookup"><span data-stu-id="f5a71-119">(This is the destination where the device will store the object.)</span></span>
-   <span data-ttu-id="f5a71-120">O tipo de objeto (um contato).</span><span class="sxs-lookup"><span data-stu-id="f5a71-120">The object type (a contact).</span></span>
-   <span data-ttu-id="f5a71-121">O nome do contato (uma cadeia de caracteres embutida em código de "John Kane").</span><span class="sxs-lookup"><span data-stu-id="f5a71-121">The contact name (a hard coded string of "John Kane").</span></span>
-   <span data-ttu-id="f5a71-122">O número de telefone de contato (uma cadeia de caracteres embutida em código de "425-555-0123").</span><span class="sxs-lookup"><span data-stu-id="f5a71-122">The contact phone number (a hard-coded string of "425-555-0123").</span></span>

<span data-ttu-id="f5a71-123">A etapa final cria o objeto somente propriedades no dispositivo (usando as propriedades definidas pela `GetRequiredPropertiesForPropertiesOnlyContact` função auxiliar).</span><span class="sxs-lookup"><span data-stu-id="f5a71-123">The final step creates the properties-only object on the device (using the properties set by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function).</span></span> <span data-ttu-id="f5a71-124">Isso é feito chamando o método **IPortableDeviceContent:: CreateObjectWithPropertiesOnly** .</span><span class="sxs-lookup"><span data-stu-id="f5a71-124">This is accomplished by calling the **IPortableDeviceContent::CreateObjectWithPropertiesOnly** method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a><span data-ttu-id="f5a71-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5a71-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5a71-126">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="f5a71-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="f5a71-127">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="f5a71-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="f5a71-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f5a71-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f5a71-129">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="f5a71-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



