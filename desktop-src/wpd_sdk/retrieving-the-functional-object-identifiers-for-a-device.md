---
description: Recuperando os identificadores de objeto funcional para um dispositivo
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Recuperando os identificadores de objeto funcional para um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815556"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a><span data-ttu-id="99e25-103">Recuperando os identificadores de objeto funcional para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="99e25-103">Retrieving the Functional Object Identifiers for a Device</span></span>

<span data-ttu-id="99e25-104">Conforme observado no tópico [recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , os dispositivos portáteis do Windows podem dar suporte a uma ou mais categorias funcionais.</span><span class="sxs-lookup"><span data-stu-id="99e25-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="99e25-105">Qualquer categoria funcional específica pode dar suporte a um ou mais objetos funcionais.</span><span class="sxs-lookup"><span data-stu-id="99e25-105">Any given functional category may support one or more functional objects.</span></span> <span data-ttu-id="99e25-106">Por exemplo, a categoria de armazenamento pode dar suporte a três objetos de armazenamento funcional, cada um dos quais é identificado por uma cadeia de caracteres de identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="99e25-106">For example, the storage category may support three functional storage objects, each of which is identified by a unique identifier string.</span></span> <span data-ttu-id="99e25-107">O primeiro objeto de armazenamento pode ser identificado pela cadeia de caracteres "Storage1", o segundo pela cadeia de caracteres "Storage2" e o terceiro pela cadeia de caracteres "Storage3".</span><span class="sxs-lookup"><span data-stu-id="99e25-107">The first storage object may then be identified by the string "Storage1", the second by the string "Storage2", and the third by the string "Storage3".</span></span>

<span data-ttu-id="99e25-108">A função ListFunctionalObjects no módulo DeviceCapabilities. cpp demonstra a recuperação de tipos de conteúdo para as categorias funcionais com suporte de um dispositivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="99e25-108">The ListFunctionalObjects function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="99e25-109">Seu aplicativo pode recuperar as categorias funcionais com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="99e25-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="99e25-110">Interface</span><span class="sxs-lookup"><span data-stu-id="99e25-110">Interface</span></span>                                                                                      | <span data-ttu-id="99e25-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="99e25-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="99e25-112">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="99e25-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="99e25-113">Fornece acesso aos métodos de recuperação de categoria funcional.</span><span class="sxs-lookup"><span data-stu-id="99e25-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="99e25-114">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="99e25-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="99e25-115">Usado para enumerar e armazenar dados de categoria funcional.</span><span class="sxs-lookup"><span data-stu-id="99e25-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="99e25-116">O código encontrado na função ListFunctionalObjects é quase idêntico ao código encontrado na função ListFunctionalCategories.</span><span class="sxs-lookup"><span data-stu-id="99e25-116">The code found in the ListFunctionalObjects function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="99e25-117">(Consulte o tópico [recuperando categorias funcionais com suporte em um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) .) A única diferença é a chamada para o método [**IPortableDeviceCapabilities:: GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) , que aparece dentro do loop que itera pelas categorias funcionais.</span><span class="sxs-lookup"><span data-stu-id="99e25-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method, which appears within the loop that iterates through the functional categories.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="99e25-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="99e25-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99e25-119">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="99e25-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="99e25-120">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="99e25-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="99e25-121">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="99e25-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="99e25-122">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="99e25-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



