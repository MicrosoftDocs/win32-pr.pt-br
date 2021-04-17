---
description: Enumerando e liberando serviços
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Enumerando e liberando serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859abe590ccaf2f71df676d5989778d5b391be57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761833"
---
# <a name="enumerating-and-freeing-services"></a>Enumerando e liberando serviços

O aplicativo ELS chama a função [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) para determinar os serviços que estão disponíveis no sistema operacional. A função pode ser usada para enumerar todos os serviços ELSs disponíveis ou para filtrar os serviços com base nos critérios de pesquisa fornecidos pelo aplicativo. Quando os serviços não são mais necessários, o aplicativo chama [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).

## <a name="get-all-supported-services"></a>Obter todos os serviços com suporte

Este exemplo de código ilustra o uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar e, em seguida, liberar todos os serviços disponíveis no sistema operacional. Para fazer isso, o aplicativo passa **nulo** para o parâmetro *pOptions* de **MappingGetServices**.


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    // Get all installed ELS services.
    Result = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="get-specific-services"></a>Obter serviços específicos

O exemplo a seguir ilustra o uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar e, em seguida, liberar todos os serviços da categoria "detecção de idioma". Para obter mais informações sobre essa categoria de serviço, consulte [**Microsoft detecção de idioma**](microsoft-language-detection.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);

    // Use the Language Auto-Detection category to enumerate
    // all language detection services.
    EnumOptions.pszCategory = L"Language Detection";

    // Execute the enumeration:
    Result = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando serviços lingüísticos estendidos](using-extended-linguistic-services.md)
</dt> <dt>

[**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



