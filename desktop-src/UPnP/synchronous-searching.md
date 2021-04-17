---
title: Pesquisa síncrona
description: O objeto localizador de dispositivo permite pesquisas síncronas e assíncronas. As pesquisas síncronas são concluídas e retornam o controle para o aplicativo de chamada somente depois que todos os dispositivos disponíveis forem encontrados.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783721"
---
# <a name="synchronous-searching"></a><span data-ttu-id="4ff64-104">Pesquisa síncrona</span><span class="sxs-lookup"><span data-stu-id="4ff64-104">Synchronous Searching</span></span>

<span data-ttu-id="4ff64-105">O objeto localizador de dispositivo permite pesquisas síncronas e assíncronas.</span><span class="sxs-lookup"><span data-stu-id="4ff64-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="4ff64-106">As pesquisas síncronas são concluídas e retornam o controle para o aplicativo de chamada somente depois que todos os dispositivos disponíveis forem encontrados.</span><span class="sxs-lookup"><span data-stu-id="4ff64-106">Synchronous searches are completed and return control to the calling application only after all available devices are found.</span></span> <span data-ttu-id="4ff64-107">Para executar uma pesquisa síncrona, use um dos métodos de pesquisa síncrona da interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .</span><span class="sxs-lookup"><span data-stu-id="4ff64-107">To perform a synchronous search, use one of the synchronous search methods of the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface.</span></span>

> [!Note]  
> <span data-ttu-id="4ff64-108">As pesquisas síncronas levam pelo menos nove segundos para serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="4ff64-108">Synchronous searches take at least nine seconds to return.</span></span> <span data-ttu-id="4ff64-109">O atraso é causado porque a mensagem de pesquisa UDP inicial deve ser enviada várias vezes.</span><span class="sxs-lookup"><span data-stu-id="4ff64-109">The delay is caused because the initial UDP search message must be sent multiple times.</span></span> <span data-ttu-id="4ff64-110">Essa duplicação conta com a inconfiabilidade do protocolo de rede subjacente.</span><span class="sxs-lookup"><span data-stu-id="4ff64-110">This duplication accounts for the unreliability of the underlying network protocol.</span></span> <span data-ttu-id="4ff64-111">As pesquisas síncronas são melhores para interfaces de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4ff64-111">Synchronous searches are best for command-line interfaces.</span></span> <span data-ttu-id="4ff64-112">Elas não são recomendadas para interfaces gráficas do usuário.</span><span class="sxs-lookup"><span data-stu-id="4ff64-112">They are not recommended for graphical user interfaces.</span></span>

 

<span data-ttu-id="4ff64-113">O método [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) pesquisa por dispositivo ou tipo de serviço.</span><span class="sxs-lookup"><span data-stu-id="4ff64-113">The [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method searches by device or service type.</span></span> <span data-ttu-id="4ff64-114">Esse método usa um URI de tipo como um parâmetro de entrada e retorna uma coleção de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ff64-114">This method takes a type URI as an input parameter and returns a collection of Device objects.</span></span> <span data-ttu-id="4ff64-115">Um objeto de dispositivo representa um dispositivo individual.</span><span class="sxs-lookup"><span data-stu-id="4ff64-115">A Device object represents an individual device.</span></span>

<span data-ttu-id="4ff64-116">Os exemplos a seguir demonstram como executar uma pesquisa síncrona para dispositivos em VBScript.</span><span class="sxs-lookup"><span data-stu-id="4ff64-116">The following examples demonstrate how to perform a synchronous search for devices in VBScript.</span></span> <span data-ttu-id="4ff64-117">Cada script usa [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), chamado com o URI de tipo (ID do serviço) para o tipo de dispositivo do player de mídia, *urn: schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*.</span><span class="sxs-lookup"><span data-stu-id="4ff64-117">Each script uses [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), called with the type URI (service ID) for the media player device type, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*.</span></span> <span data-ttu-id="4ff64-118">O método retorna uma coleção de objetos de dispositivo que corresponde aos dispositivos do player de mídia que foram encontrados.</span><span class="sxs-lookup"><span data-stu-id="4ff64-118">The method returns a collection of Device objects that corresponds to media player devices that were found.</span></span> <span data-ttu-id="4ff64-119">Para obter informações sobre como extrair objetos de dispositivo individuais de uma coleção, consulte [coleções de dispositivos retornadas por pesquisas síncronas](device-collections-returned-by-synchronous-searches.md).</span><span class="sxs-lookup"><span data-stu-id="4ff64-119">For information on extracting individual device objects from a collection, see [Device Collections Returned By Synchronous Searches](device-collections-returned-by-synchronous-searches.md).</span></span>

## <a name="search-for-devices-by-type-in-vbscript"></a><span data-ttu-id="4ff64-120">Pesquisar dispositivos por tipo em VBScript</span><span class="sxs-lookup"><span data-stu-id="4ff64-120">Search for Devices by Type in VBScript</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a><span data-ttu-id="4ff64-121">Pesquisar dispositivo por tipo em C++</span><span class="sxs-lookup"><span data-stu-id="4ff64-121">Search for Device by Type in C++</span></span>

<span data-ttu-id="4ff64-122">O exemplo a seguir demonstra uma pesquisa síncrona para dispositivos de player de mídia usando C++.</span><span class="sxs-lookup"><span data-stu-id="4ff64-122">The following example demonstrates a synchronous search for media player devices using C++.</span></span> <span data-ttu-id="4ff64-123">A função usa um ponteiro para a interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) como entrada e retorna o ponteiro de interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="4ff64-123">The function takes a pointer to the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface as input, and returns the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface pointer.</span></span>

<span data-ttu-id="4ff64-124">O exemplo primeiro aloca um **BSTR** para representar o URI do tipo de dispositivo e, em seguida, passa isso para o método [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) .</span><span class="sxs-lookup"><span data-stu-id="4ff64-124">The example first allocates a **BSTR** to represent the device type URI and then passes this to the [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method.</span></span> <span data-ttu-id="4ff64-125">Ele também passa o endereço de um ponteiro [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) local no buffer no qual o método, em seguida, armazena a coleção de dispositivos encontrados.</span><span class="sxs-lookup"><span data-stu-id="4ff64-125">It also passes the address of a local [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) pointer in the buffer in which the method then stores the collection of devices found.</span></span> <span data-ttu-id="4ff64-126">Se a chamada de função for bem-sucedida, ela retornará o ponteiro para essa coleção.</span><span class="sxs-lookup"><span data-stu-id="4ff64-126">If the function call is successful, it returns the pointer to this collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




