---
description: Recuperando um identificador de objeto de um identificador exclusivo persistente
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Recuperando uma ID de objeto de uma ID exclusiva persistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791416"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a><span data-ttu-id="f9992-103">Recuperando uma ID de objeto de uma ID exclusiva persistente</span><span class="sxs-lookup"><span data-stu-id="f9992-103">Retrieving an Object Id from a Persistent Unique Id</span></span>

<span data-ttu-id="f9992-104">Identificadores de objeto só têm a garantia de serem exclusivos para uma determinada sessão de dispositivo; Se o usuário estabelecer uma nova conexão, os identificadores de uma sessão anterior poderão não corresponder a identificadores da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="f9992-104">Object identifiers are only guaranteed to be unique for a given device session; if the user establishes a new connection, identifiers from a previous session may not match identifiers for the current session.</span></span> <span data-ttu-id="f9992-105">Para resolver esse problema, a API WPD dá suporte a PUIDs (identificadores exclusivos persistentes), que persistem entre sessões de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9992-105">To resolve this issue, the WPD API supports persistent unique identifiers (PUIDs), which persist across device sessions.</span></span>

<span data-ttu-id="f9992-106">Alguns dispositivos armazenam seus PUIDs nativamente com um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="f9992-106">Some devices store their PUIDs natively with a given object.</span></span> <span data-ttu-id="f9992-107">Outros podem gerar o PUID com base em um hash dos dados do objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="f9992-107">Others may generate the PUID based on a hash of selected object data.</span></span> <span data-ttu-id="f9992-108">Outros podem tratar identificadores de objeto como PUIDs (porque eles podem garantir que esses identificadores nunca sejam alterados).</span><span class="sxs-lookup"><span data-stu-id="f9992-108">Others may treat object identifiers as PUIDs (because they can guarantee that these identifiers never change).</span></span>

<span data-ttu-id="f9992-109">A função GetObjectIdentifierFromPersistentUniqueIdentifier no módulo Contentproperties. cpp demonstra a recuperação de um identificador de objeto para um determinado PUID.</span><span class="sxs-lookup"><span data-stu-id="f9992-109">The GetObjectIdentifierFromPersistentUniqueIdentifier function in the ContentProperties.cpp module demonstrates the retrieval of an object identifier for a given PUID.</span></span>

<span data-ttu-id="f9992-110">Seu aplicativo pode recuperar um identificador de objeto para um PUID correspondente usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9992-110">Your application can retrieve an object identifier for a corresponding PUID using the interfaces described in the following table.</span></span>



| <span data-ttu-id="f9992-111">Interface</span><span class="sxs-lookup"><span data-stu-id="f9992-111">Interface</span></span>                                                                                      | <span data-ttu-id="f9992-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9992-112">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9992-113">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="f9992-113">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="f9992-114">Fornece acesso ao método de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f9992-114">Provides access to the retrieval method.</span></span>                                                            |
| [<span data-ttu-id="f9992-115">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="f9992-115">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="f9992-116">Usado para armazenar o identificador de objeto e o identificador exclusivo persistente (PUID) correspondente.</span><span class="sxs-lookup"><span data-stu-id="f9992-116">Used to store both the object identifier and the corresponding persistent unique identifier (PUID).</span></span> |



 

<span data-ttu-id="f9992-117">A primeira tarefa que o aplicativo de exemplo realiza é obter um PUID do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9992-117">The first task that the sample application accomplishes is to obtain a PUID from the user.</span></span>


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



<span data-ttu-id="f9992-118">Depois disso, o aplicativo de exemplo recupera um objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , que será usado para invocar o método [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="f9992-118">After this, the sample application retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to invoke the [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="f9992-119">Em seguida, ele cria um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que irá conter o PUID fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f9992-119">Next, it creates an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that will hold the PUID supplied by the user.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



<span data-ttu-id="f9992-120">Depois que as três etapas anteriores forem executadas, o exemplo estará pronto para recuperar o identificador de objeto que corresponde ao PUID fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f9992-120">Once the previous three steps are taken, the sample is ready to retrieve the object identifier that matches the PUID supplied by the user.</span></span> <span data-ttu-id="f9992-121">Isso é feito chamando o método [**IPortableDeviceContent:: GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="f9992-121">This is accomplished by calling the [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span> <span data-ttu-id="f9992-122">Antes de chamar esse método, o exemplo Inicializa uma estrutura PROPVARIANT, grava o PUID fornecido pelo usuário para essa estrutura e o adiciona ao objeto IPortableDevicePropVariantCollection no qual pPersistentUniqueIDs aponta.</span><span class="sxs-lookup"><span data-stu-id="f9992-122">Prior to calling this method, the sample initializes a PROPVARIANT structure, writes the PUID supplied by the user to this structure, and adds it to the IPortableDevicePropVariantCollection object at which pPersistentUniqueIDs points.</span></span> <span data-ttu-id="f9992-123">Esse ponteiro é passado como o primeiro argumento para o método GetObjectIDsFromPersistentUniqueIDs.</span><span class="sxs-lookup"><span data-stu-id="f9992-123">This pointer is passed as the first argument to the GetObjectIDsFromPersistentUniqueIDs method.</span></span> <span data-ttu-id="f9992-124">O segundo argumento de GetObjectIDsFromPersistentUniqueIDs é um objeto IPortableDevicePropVariantCollection que recebe o identificador de objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="f9992-124">The second argument of GetObjectIDsFromPersistentUniqueIDs is an IPortableDevicePropVariantCollection object that receives the matching object identifier.</span></span>


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="f9992-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9992-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9992-126">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="f9992-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="f9992-127">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="f9992-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="f9992-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="f9992-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="f9992-129">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="f9992-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



