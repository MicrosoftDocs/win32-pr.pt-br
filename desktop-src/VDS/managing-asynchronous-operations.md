---
description: Gerenciando operações assíncronas
ms.assetid: e5136e15-3ae1-4e0a-ae97-fcf16203b21d
title: Gerenciando operações assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537a52a41e73bae7035789176bb65b125c105f691bf654ed3c0ded4e6a73f70d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999438"
---
# <a name="managing-asynchronous-operations"></a>Gerenciando operações assíncronas

\[Começando com Windows 8 e Windows Server 2012, o [Serviço](virtual-disk-service-portal.md) de Disco Virtual é sobressalido pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O exemplo de código a seguir demonstra como um chamador funciona com um objeto assíncrono. Aqui, a **função SynchronousCreateLun** chama o método [**assíncrono IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) usando os parâmetros determinados. A função aguardará o objeto assíncrono para que a chamada de método **CreateLun** assíncrona seja finalada. Quando o método [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) retorna, **SynchronousCreateLun** obtém a interface [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) para o LUN recém-criado e a retorna como um argumento out.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando VDS](using-vds.md)
</dt> <dt>

[Objetos auxiliares](helper-objects.md)
</dt> <dt>

[**IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun)
</dt> <dt>

[**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> </dl>

 

 
