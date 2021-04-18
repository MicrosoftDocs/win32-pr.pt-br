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
# <a name="loading-vds"></a>Carregando VDS

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

**Para carregar e inicializar o VDS**

1.  Liberar interfaces não nulas.
2.  Chame a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)ou [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) para obter um ponteiro para o objeto do carregador de serviço.

    **CLSCTX \_ DISABLE \_ AAA** não pode ser especificado nesta chamada. Se [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) for chamado, **EOAC \_ desabilitar \_ AAA** não poderá ser especificado no parâmetro *dwCapabilities* .

3.  Chame o método [**IVdsServiceLoader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) para carregar o VDS.

    Passar **NULL** como o primeiro parâmetro carrega e INICIALIZA o VDS no host local.

4.  Chame o método [**IVdsService:: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) para aguardar a conclusão da inicialização do VDS.

O exemplo de código a seguir inicializa o serviço que retorna um ponteiro para o objeto de serviço.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando VDS](using-vds.md)
</dt> <dt>

[**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[**IVdsServiceLoader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Objetos de instalação e de serviço](startup-and-service-objects.md)
</dt> </dl>

 

 
