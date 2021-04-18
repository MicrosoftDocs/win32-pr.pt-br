---
description: Solicitando reconhecimento de texto
ms.assetid: 9db9045d-b289-4c6c-9b17-ddbc2c1d3089
title: Solicitando reconhecimento de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2442cfa1e26185c4c8d882fe71bb178911f4d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796345"
---
# <a name="requesting-text-recognition"></a><span data-ttu-id="847e8-103">Solicitando reconhecimento de texto</span><span class="sxs-lookup"><span data-stu-id="847e8-103">Requesting Text Recognition</span></span>

<span data-ttu-id="847e8-104">O aplicativo chama a função [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) para solicitar reconhecimento de texto de um serviço ELS específico.</span><span class="sxs-lookup"><span data-stu-id="847e8-104">The application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to request text recognition from a specific ELS service.</span></span> <span data-ttu-id="847e8-105">O serviço deve ter sido descoberto em uma chamada anterior para [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), conforme descrito em [**enumerando e liberando serviços**](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="847e8-105">The service must have been discovered in a previous call to [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), as described in [**Enumerating and Freeing Services**](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="847e8-106">A plataforma pode processar chamadas [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="847e8-106">The platform can process [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) calls either synchronously or asynchronously.</span></span>

 

<span data-ttu-id="847e8-107">[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) manipula os seguintes tipos de texto:</span><span class="sxs-lookup"><span data-stu-id="847e8-107">[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) handles the following types of text:</span></span>

-   <span data-ttu-id="847e8-108">Detecção de idioma da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="847e8-108">Microsoft language detection.</span></span> <span data-ttu-id="847e8-109">UTF-16, forma de normalização C, texto para o qual determinar o idioma.</span><span class="sxs-lookup"><span data-stu-id="847e8-109">UTF-16, normalization form C, text for which to determine the language.</span></span>
-   <span data-ttu-id="847e8-110">Detecção de script da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="847e8-110">Microsoft script detection.</span></span> <span data-ttu-id="847e8-111">Texto UTF-16 para o qual determinar intervalos de script.</span><span class="sxs-lookup"><span data-stu-id="847e8-111">UTF-16 text for which to determine script ranges.</span></span>
-   <span data-ttu-id="847e8-112">Serviços de transliteração.</span><span class="sxs-lookup"><span data-stu-id="847e8-112">Transliteration services.</span></span> <span data-ttu-id="847e8-113">Texto UTF-16 gravado no script de origem (sistema de escrita).</span><span class="sxs-lookup"><span data-stu-id="847e8-113">UTF-16 text written in source script (writing system).</span></span>

## <a name="use-synchronous-text-recognition"></a><span data-ttu-id="847e8-114">Usar reconhecimento de texto síncrono</span><span class="sxs-lookup"><span data-stu-id="847e8-114">Use Synchronous Text Recognition</span></span>

<span data-ttu-id="847e8-115">Esta seção fornece instruções para várias maneiras de executar o reconhecimento de texto síncrono.</span><span class="sxs-lookup"><span data-stu-id="847e8-115">This section provides instructions for several ways to perform synchronous text recognition.</span></span>

<span data-ttu-id="847e8-116">**Reconhecimento de texto síncrono com o Microsoft Detecção de Idioma Service**</span><span class="sxs-lookup"><span data-stu-id="847e8-116">**Synchronous Text Recognition with Microsoft Language Detection Service**</span></span>

<span data-ttu-id="847e8-117">O exemplo a seguir ilustra o uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) com o serviço Microsoft detecção de idioma e imprime todos os resultados recuperados pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="847e8-117">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Language Detection service, and prints all the results retrieved by the service.</span></span> <span data-ttu-id="847e8-118">O formato de saída desse serviço é uma estrutura [**de \_ \_ intervalo de dados de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) único com seu membro **pData** apontando para uma matriz de cadeias de caracteres formatada com o registro e com terminação de nulo duplo Unicode.</span><span class="sxs-lookup"><span data-stu-id="847e8-118">The output format of this service is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to a Unicode double-null-terminated, registry-formatted array of strings.</span></span> <span data-ttu-id="847e8-119">Cada cadeia de caracteres da matriz é terminada em nulo e uma cadeia de caracteres vazia é usada para especificar o fim da matriz.</span><span class="sxs-lookup"><span data-stu-id="847e8-119">Every string of the array is null-terminated and an empty string is used to specify the end of the array.</span></span> <span data-ttu-id="847e8-120">O conteúdo da matriz são nomes de idiomas classificados por confiança.</span><span class="sxs-lookup"><span data-stu-id="847e8-120">The contents of the array are language names sorted by confidence.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    WCHAR * p;

    // The return format of the Language Auto-Detection is a
    // double null-terminated registry-formatted array of strings.
    // Every string of the array is null-terminated and there's an
    // empty string specifying the end of the array.
    for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
    {
        printf("%ws\n", p);
    }
}
```



<span data-ttu-id="847e8-121">**Reconhecimento de texto síncrono com o serviço de detecção de scripts da Microsoft**</span><span class="sxs-lookup"><span data-stu-id="847e8-121">**Synchronous Text Recognition with Microsoft Script Detection Service**</span></span>

<span data-ttu-id="847e8-122">O exemplo a seguir ilustra o uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) com o serviço de detecção de scripts da Microsoft e imprime todos os resultados recuperados.</span><span class="sxs-lookup"><span data-stu-id="847e8-122">The next example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Script Detection service, and prints all the retrieved results.</span></span> <span data-ttu-id="847e8-123">O formato de saída desse serviço é uma matriz de estruturas de [**\_ \_ intervalo de dados de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) , cada um especificando o texto escrito no mesmo script.</span><span class="sxs-lookup"><span data-stu-id="847e8-123">The output format of this service is an array of [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structures, each specifying text written in the same script.</span></span> <span data-ttu-id="847e8-124">Os caracteres comuns (Zyyy) são adicionados ao intervalo anterior, ou ao próximo intervalo, se o intervalo anterior não existir.</span><span class="sxs-lookup"><span data-stu-id="847e8-124">Common (Zyyy) characters are added to the previous range, or to the next range if the previous range does not exist.</span></span> <span data-ttu-id="847e8-125">O membro **pData** de cada estrutura aponta para uma cadeia de caracteres Unicode terminada em nulo que contém o nome Unicode padrão do script para o intervalo específico.</span><span class="sxs-lookup"><span data-stu-id="847e8-125">The **pData** member of each structure points to a Unicode null-terminated string containing the standard Unicode name of the script for the particular range.</span></span>

> [!Note]  
> <span data-ttu-id="847e8-126">A partir do Windows 7, o serviço de detecção de scripts da Microsoft está em conformidade com o Unicode 5,1.</span><span class="sxs-lookup"><span data-stu-id="847e8-126">As of Windows 7, the Microsoft Script Detection service complies with Unicode 5.1.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Script Detection GUID to enumerate SD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_SCRIPT_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData);
    }
}
```



<span data-ttu-id="847e8-127">**Reconhecimento de texto síncrono com o serviço de transliteração do Microsoft cirílico para o latim**</span><span class="sxs-lookup"><span data-stu-id="847e8-127">**Synchronous Text Recognition with Microsoft Cyrillic to Latin Transliteration Service**</span></span>

<span data-ttu-id="847e8-128">O exemplo a seguir ilustra o uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) com o serviço de transliteração do Microsoft cirílico para o latim e imprime os resultados recuperados.</span><span class="sxs-lookup"><span data-stu-id="847e8-128">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Cyrillic to Latin transliteration service, and prints the retrieved results.</span></span> <span data-ttu-id="847e8-129">Observe as duas maneiras diferentes de enumerar esse serviço, seja por GUID ou por categoria e script de entrada.</span><span class="sxs-lookup"><span data-stu-id="847e8-129">Note the two different ways to enumerate this service, either by GUID or by category and input script.</span></span>

<span data-ttu-id="847e8-130">O formato de saída é o mesmo para todos os serviços de transliteração disponíveis.</span><span class="sxs-lookup"><span data-stu-id="847e8-130">The output format is the same for all available transliteration services.</span></span> <span data-ttu-id="847e8-131">É uma estrutura de [**\_ \_ intervalo de dados de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) único com seu membro **pData** apontando para uma matriz de caracteres Unicode que representa o texto original transliterado no script de saída aplicando somente as regras do serviço de transliteração específico.</span><span class="sxs-lookup"><span data-stu-id="847e8-131">It is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to an array of Unicode characters representing the original text transliterated into the output script by applying only the rules of the specific transliteration service.</span></span> <span data-ttu-id="847e8-132">Este serviço não termina em nulo, encerrando sua saída se a entrada não contiver o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="847e8-132">This service does not null-terminate its output if the input does not contain the terminating null character.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT (L"Skip The russian word for 'yes' is transliterated to Latin as '\x0434\x0430'.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices;
    DWORD                   dwServicesCount;
    HRESULT                 hResult;

    // 1. Enumerate by GUID:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Use the Cyrl->Latn Transliteration GUID to enumerate only this service:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    printf("--\n");

    // 2. Enumerate by input script and category:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    EnumOptions.pszCategory = L"Transliteration";
    EnumOptions.pszInputScript = L"Cyrl";
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    // We want the result to be null-terminated for display.
    // That's why we will also pass the input null terminator:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT) + 1, USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[0].pData);
}
```



<span data-ttu-id="847e8-133">**Reconhecimento de texto síncrono com uma chamada para todos os serviços disponíveis**</span><span class="sxs-lookup"><span data-stu-id="847e8-133">**Synchronous Text Recognition with a Call to All Available Services**</span></span>

<span data-ttu-id="847e8-134">O exemplo a seguir mostra o uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) com todos os serviços disponíveis e imprime os resultados recuperados para todos os serviços.</span><span class="sxs-lookup"><span data-stu-id="847e8-134">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with all available services, and prints the retrieved results for all the services.</span></span> <span data-ttu-id="847e8-135">Este exemplo fornece uma boa ilustração da operação de cada serviço.</span><span class="sxs-lookup"><span data-stu-id="847e8-135">This example provides a good illustration of the operation of each service.</span></span> <span data-ttu-id="847e8-136">Ao examinar a saída do aplicativo de exemplo, é fácil descobrir o que está acontecendo internamente com os serviços.</span><span class="sxs-lookup"><span data-stu-id="847e8-136">By looking at the output of the example application, it is easy to find out what is happening internally with the services.</span></span> <span data-ttu-id="847e8-137">Este exemplo também mostra que quase todos os códigos usados para chamar qualquer um dos serviços ELSs são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="847e8-137">This example also shows that almost all code used to call any of the ELS services is the same.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    DWORD i;

    // Get all installed ELS services:
    hResult = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service:
            // ... prgServices[i] ...
            if (i > 0)
            {
                printf("--\n");
            }
            hResult = CallMappingRecognizeText(&prgServices[i]);
            if (SUCCEEDED(hResult))
            {
                printf("Calling the service %ws has succeeded!\n",
                    prgServices[i].pszDescription);
            }
            else
            {
                printf("Calling the service %ws has failed, failure = 0x%x!\n",
                    prgServices[i].pszDescription, hResult);
            }
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;
    DWORD dwDataIndex;
    WCHAR c;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        // Currently, we can treat all results as arrays of unicode WCHAR
        // characters, but there can be services in the future
        // that use different formatting, i.e. XML, HTML, etc.
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"");
        for (dwDataIndex = 0; dwDataIndex < pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2; ++dwDataIndex)
        {
            c = ((WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData)[dwDataIndex];
            if (c >= 32 && c < 128 && c != '"') printf("%wc", c);
            else printf("#%x", (unsigned)c);
        }
        printf("\"\n");
    }
}

void CallRecognizeText(LPCWSTR Category, LPCWSTR Text)
{
    HRESULT               Result;
    PMAPPING_SERVICE_INFO rgServices;
    DWORD                 ServicesCount;
    MAPPING_ENUM_OPTIONS  options = {sizeof(MAPPING_ENUM_OPTIONS), (LPWSTR) Category, 0};

    Result = MappingGetServices(&options, &rgServices, &ServicesCount);
    if (Result == S_OK && ServicesCount > 0)
    {
        MAPPING_PROPERTY_BAG bag = { sizeof(MAPPING_PROPERTY_BAG), 0};
        Result = MappingRecognizeText(&rgServices[0], Text, wcslen(Text), 0, NULL, &bag);
        if (Result == S_OK)
        {
            MappingFreePropertyBag(&bag);
        }

        MappingFreeServices(rgServices);
    }
}
int _tmain(int argc, _TCHAR* argv[])
{
    CallRecognizeText(L"Language Detection", L"Text to be recognized");
  
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    return 0;
}
```



## <a name="use-asynchronous-text-recognition"></a><span data-ttu-id="847e8-138">Usar reconhecimento de texto assíncrono</span><span class="sxs-lookup"><span data-stu-id="847e8-138">Use Asynchronous Text Recognition</span></span>

<span data-ttu-id="847e8-139">O exemplo a seguir mostra o uso de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) para reconhecimento de texto assíncrono.</span><span class="sxs-lookup"><span data-stu-id="847e8-139">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) for asynchronous text recognition.</span></span> <span data-ttu-id="847e8-140">Quando o retorno de chamada é usado, o aplicativo deve garantir que o recipiente de propriedades, o texto de entrada, as opções e o serviço sejam todos válidos até que a execução do retorno de chamada seja concluída.</span><span class="sxs-lookup"><span data-stu-id="847e8-140">When the callback is used, the application must make sure that the property bag, the input text, the options, and the service are all valid until after the callback has finished executing.</span></span>

<span data-ttu-id="847e8-141">O aplicativo deve chamar [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) imediatamente depois que a bolsa é consumida pela função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="847e8-141">The application must call [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) immediately after the bag is consumed by the callback function.</span></span> <span data-ttu-id="847e8-142">Para obter mais informações, consulte [fornecendo retornos de chamada para serviços ELSs](providing-callbacks-for-els-services.md).</span><span class="sxs-lookup"><span data-stu-id="847e8-142">For more information, see [Providing Callbacks for ELS Services](providing-callbacks-for-els-services.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG    bag;
    MAPPING_OPTIONS         Options;
    HRESULT                 hResult;
    HANDLE                  SyncEvent;
    DWORD                   dwWaitResult;

    SyncEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    if (SyncEvent == NULL)
    {
        hResult = E_FAIL;
    }
    else
    {
        ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
        bag.Size = sizeof (MAPPING_PROPERTY_BAG);

        ZeroMemory(&Options, sizeof (MAPPING_OPTIONS));
        Options.Size = sizeof (MAPPING_OPTIONS);
        Options.pfnRecognizeCallback = (PFN_MAPPINGCALLBACKPROC)RecognizeCallback;
        Options.pRecognizeCallerData = &SyncEvent;
        Options.dwRecognizeCallerDataSize = sizeof (HANDLE);

        // MappingRecognizeText's dwIndex parameter specifies the first
        // index inside the text from where the recognition should start.
        // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
        // of the input string.
        hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, &Options, &bag);
        if (SUCCEEDED(hResult))
        {
            // We are using an event to synchronize our waiting for the call to end,
            // because some objects have to be valid till the end of the callback call:
            // - the input text
            // - the property bag
            // - the options
            // - the service
            dwWaitResult = WaitForSingleObject(SyncEvent, INFINITE);
            if (dwWaitResult != WAIT_OBJECT_0)
            {
                hResult = E_FAIL;
            }
        }
        CloseHandle(SyncEvent);
    }
    return hResult;
}

void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result)
{
    HANDLE SyncEvent;
    WCHAR * p;

    UNREFERENCED_PARAMETER(dwDataSize);

    if (SUCCEEDED(Result))
    {
        for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
        {
            printf("%ws\n", p);
        }
        MappingFreePropertyBag(pBag);
    }

    SyncEvent = *((HANDLE *)data);
    SetEvent(SyncEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="847e8-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="847e8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="847e8-144">Usando serviços lingüísticos estendidos</span><span class="sxs-lookup"><span data-stu-id="847e8-144">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="847e8-145">Fornecendo retornos de chamada para serviços ELSs</span><span class="sxs-lookup"><span data-stu-id="847e8-145">Providing Callbacks for ELS Services</span></span>](providing-callbacks-for-els-services.md)
</dt> <dt>

[<span data-ttu-id="847e8-146">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="847e8-146">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[<span data-ttu-id="847e8-147">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="847e8-147">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> <dt>

[<span data-ttu-id="847e8-148">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="847e8-148">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



