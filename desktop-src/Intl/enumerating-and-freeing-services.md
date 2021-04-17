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
# <a name="enumerating-and-freeing-services"></a><span data-ttu-id="70026-103">Enumerando e liberando serviços</span><span class="sxs-lookup"><span data-stu-id="70026-103">Enumerating and Freeing Services</span></span>

<span data-ttu-id="70026-104">O aplicativo ELS chama a função [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) para determinar os serviços que estão disponíveis no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="70026-104">The ELS application calls the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function to determine the services that are available on the operating system.</span></span> <span data-ttu-id="70026-105">A função pode ser usada para enumerar todos os serviços ELSs disponíveis ou para filtrar os serviços com base nos critérios de pesquisa fornecidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70026-105">The function can be used either to enumerate all available ELS services, or to filter the services based on application-provided search criteria.</span></span> <span data-ttu-id="70026-106">Quando os serviços não são mais necessários, o aplicativo chama [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span><span class="sxs-lookup"><span data-stu-id="70026-106">When services are no longer needed, the application calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span></span>

## <a name="get-all-supported-services"></a><span data-ttu-id="70026-107">Obter todos os serviços com suporte</span><span class="sxs-lookup"><span data-stu-id="70026-107">Get All Supported Services</span></span>

<span data-ttu-id="70026-108">Este exemplo de código ilustra o uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar e, em seguida, liberar todos os serviços disponíveis no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="70026-108">This code example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all available services on the operating system.</span></span> <span data-ttu-id="70026-109">Para fazer isso, o aplicativo passa **nulo** para o parâmetro *pOptions* de **MappingGetServices**.</span><span class="sxs-lookup"><span data-stu-id="70026-109">To do this, the application passes **NULL** for the *pOptions* parameter of **MappingGetServices**.</span></span>


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



## <a name="get-specific-services"></a><span data-ttu-id="70026-110">Obter serviços específicos</span><span class="sxs-lookup"><span data-stu-id="70026-110">Get Specific Services</span></span>

<span data-ttu-id="70026-111">O exemplo a seguir ilustra o uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) e [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar e, em seguida, liberar todos os serviços da categoria "detecção de idioma".</span><span class="sxs-lookup"><span data-stu-id="70026-111">The next example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all services of category "Language Detection".</span></span> <span data-ttu-id="70026-112">Para obter mais informações sobre essa categoria de serviço, consulte [**Microsoft detecção de idioma**](microsoft-language-detection.md).</span><span class="sxs-lookup"><span data-stu-id="70026-112">For more information about this service category, see [**Microsoft Language Detection**](microsoft-language-detection.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="70026-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70026-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70026-114">Usando serviços lingüísticos estendidos</span><span class="sxs-lookup"><span data-stu-id="70026-114">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="70026-115">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="70026-115">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[<span data-ttu-id="70026-116">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="70026-116">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



