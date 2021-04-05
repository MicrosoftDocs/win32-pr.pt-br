---
description: Gerenciando operações assíncronas
ms.assetid: e5136e15-3ae1-4e0a-ae97-fcf16203b21d
title: Gerenciando operações assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d220c5633f9ee044dbf9cdb6a63b563747620afd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922084"
---
# <a name="managing-asynchronous-operations"></a><span data-ttu-id="af433-103">Gerenciando operações assíncronas</span><span class="sxs-lookup"><span data-stu-id="af433-103">Managing Asynchronous Operations</span></span>

<span data-ttu-id="af433-104">\[A partir do Windows 8 e do Windows Server 2012, o [serviço de disco virtual](virtual-disk-service-portal.md) é substituído pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="af433-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="af433-105">O exemplo de código a seguir demonstra como um chamador funciona com um objeto Async.</span><span class="sxs-lookup"><span data-stu-id="af433-105">The code example that follows demonstrates how a caller works with an async object.</span></span> <span data-ttu-id="af433-106">Aqui, a função **SynchronousCreateLun** chama o método [**IVdsSubSystem:: CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) assíncrono usando os parâmetros fornecidos.</span><span class="sxs-lookup"><span data-stu-id="af433-106">Here, the **SynchronousCreateLun** function calls the asynchronous [**IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) method using the given parameters.</span></span> <span data-ttu-id="af433-107">A função aguardará o objeto assíncrono para a chamada do método **CreateLun** assíncrono concluir.</span><span class="sxs-lookup"><span data-stu-id="af433-107">The function will wait on the async object for the asynchronous **CreateLun** method call to finish.</span></span> <span data-ttu-id="af433-108">Quando o método [**IVdsAsync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) retorna, **SynchronousCreateLun** Obtém a interface [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) para o LUN recém-criado e a retorna como um argumento out.</span><span class="sxs-lookup"><span data-stu-id="af433-108">When the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method returns, **SynchronousCreateLun** gets the [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) interface for the newly created LUN and returns it as an out argument.</span></span>


```C++
//
// Simple macro to release non-null interfaces.
//
#include <windows.h>
#include "vds.h"
#include <stdio.h>

#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

HRESULT SynchronousCreateLun(
    IVdsSubSystem *pSubsystem,
    VDS_LUN_TYPE  type,
    ULONGLONG     ullSize,
    VDS_OBJECT_ID *pDriveIdArray,
    LONG          lNumberOfDrives,
    LPWSTR        pwszUnmaskingList,
    VDS_HINTS     *pHints,
    IVdsLun       **ppLun)
{
    HRESULT hResult = S_OK;
    HRESULT hResult2 = S_OK;
    IVdsAsync *pAsync = NULL;
    VDS_ASYNC_OUTPUT AsyncOut;
    IUnknown* pUnknown = NULL;

    ZeroMemory( &AsyncOut, sizeof(VDS_ASYNC_OUTPUT));

    hResult = pSubsystem->CreateLun(
        type,
        ullSize,
        pDriveIdArray,
        lNumberOfDrives,
        pwszUnmaskingList,
        pHints,
        &pAsync);

    if (SUCCEEDED(hResult) && (!pAsync)) {
        hResult = E_UNEXPECTED; // Errant provider, returned S_OK 
                                // with a NULL pointer.
    }

    if (SUCCEEDED(hResult)) {
        // Wait until the Async is done.
        hResult2 = pAsync->Wait( &hResult, &AsyncOut);
        if (SUCCEEDED(hResult) && FAILED(hResult2)) {
            hResult = hResult2;
        }
    }

    if (SUCCEEDED(hResult) && (VDS_ASYNCOUT_CREATELUN != AsyncOut.type)) {
        hResult = E_UNEXPECTED; // Errant provider, returned S_OK  
                                // with an unexpected type.
    }

    if (SUCCEEDED(hResult)) {
        pUnknown = AsyncOut.cl.pLunUnk;
        if (!pUnknown) {
            hResult = E_UNEXPECTED; // Errant provider, returned 
                                    // S_OK with a NULL pointer.
        }
    }

    if (SUCCEEDED(hResult)) {
        hResult = pUnknown->QueryInterface(IID_IVdsLun, (void **)ppLun);
    }

    _SafeRelease(pAsync);
    _SafeRelease(pUnknown);

    return hResult;
}
```



## <a name="related-topics"></a><span data-ttu-id="af433-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af433-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af433-110">Usando VDS</span><span class="sxs-lookup"><span data-stu-id="af433-110">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="af433-111">Objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="af433-111">Helper Objects</span></span>](helper-objects.md)
</dt> <dt>

[<span data-ttu-id="af433-112">**IVdsSubSystem::CreateLun**</span><span class="sxs-lookup"><span data-stu-id="af433-112">**IVdsSubSystem::CreateLun**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun)
</dt> <dt>

[<span data-ttu-id="af433-113">**IVdsAsync:: aguardar**</span><span class="sxs-lookup"><span data-stu-id="af433-113">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="af433-114">**IVdsLun**</span><span class="sxs-lookup"><span data-stu-id="af433-114">**IVdsLun**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> </dl>

 

 
