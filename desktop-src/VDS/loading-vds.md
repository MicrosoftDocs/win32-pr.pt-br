---
description: Carregando VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Carregando VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c66685668641f3036739c57bd7353f72052c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784989"
---
# <a name="loading-vds"></a><span data-ttu-id="5ed57-103">Carregando VDS</span><span class="sxs-lookup"><span data-stu-id="5ed57-103">Loading VDS</span></span>

<span data-ttu-id="5ed57-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5ed57-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="5ed57-105">**Para carregar e inicializar o VDS**</span><span class="sxs-lookup"><span data-stu-id="5ed57-105">**To load and initialize VDS**</span></span>

1.  <span data-ttu-id="5ed57-106">Liberar interfaces não nulas.</span><span class="sxs-lookup"><span data-stu-id="5ed57-106">Release non-null interfaces.</span></span>
2.  <span data-ttu-id="5ed57-107">Chame a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)ou [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) para obter um ponteiro para o objeto do carregador de serviço.</span><span class="sxs-lookup"><span data-stu-id="5ed57-107">Call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex), or [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) function to obtain a pointer to the service loader object.</span></span>

    <span data-ttu-id="5ed57-108">**CLSCTX \_ DISABLE \_ AAA** não pode ser especificado nesta chamada.</span><span class="sxs-lookup"><span data-stu-id="5ed57-108">**CLSCTX\_DISABLE\_AAA** cannot be specified in this call.</span></span> <span data-ttu-id="5ed57-109">Se [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) for chamado, **EOAC \_ desabilitar \_ AAA** não poderá ser especificado no parâmetro *dwCapabilities* .</span><span class="sxs-lookup"><span data-stu-id="5ed57-109">If [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is called, **EOAC\_DISABLE\_AAA** cannot be specified in the *dwCapabilities* parameter.</span></span>

3.  <span data-ttu-id="5ed57-110">Chame o método [**IVdsServiceLoader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) para carregar o VDS.</span><span class="sxs-lookup"><span data-stu-id="5ed57-110">Call the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method to load VDS.</span></span>

    <span data-ttu-id="5ed57-111">Passar **NULL** como o primeiro parâmetro carrega e INICIALIZA o VDS no host local.</span><span class="sxs-lookup"><span data-stu-id="5ed57-111">Passing **NULL** as the first parameter loads and initializes VDS on the local host.</span></span>

4.  <span data-ttu-id="5ed57-112">Chame o método [**IVdsService:: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) para aguardar a conclusão da inicialização do VDS.</span><span class="sxs-lookup"><span data-stu-id="5ed57-112">Call the [**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) method to wait for VDS initialization to complete.</span></span>

<span data-ttu-id="5ed57-113">O exemplo de código a seguir inicializa o serviço que retorna um ponteiro para o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="5ed57-113">The following code example initializes the service that returns a pointer to the service object.</span></span>


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="5ed57-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ed57-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed57-115">Usando VDS</span><span class="sxs-lookup"><span data-stu-id="5ed57-115">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="5ed57-116">**IVdsService::WaitForServiceReady**</span><span class="sxs-lookup"><span data-stu-id="5ed57-116">**IVdsService::WaitForServiceReady**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[<span data-ttu-id="5ed57-117">**IVdsServiceLoader:: loadservice**</span><span class="sxs-lookup"><span data-stu-id="5ed57-117">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="5ed57-118">Objetos de instalação e de serviço</span><span class="sxs-lookup"><span data-stu-id="5ed57-118">Setup and Service Objects</span></span>](startup-and-service-objects.md)
</dt> </dl>

 

 
