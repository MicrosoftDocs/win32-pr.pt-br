---
description: Fornecendo retornos de chamada para serviços ELSs
ms.assetid: 48609c55-9e82-4407-ae28-41b07b1e1161
title: Fornecendo retornos de chamada para serviços ELSs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d22091f666649aab43c66f3d532f8e8f971d49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165242"
---
# <a name="providing-callbacks-for-els-services"></a><span data-ttu-id="963c9-103">Fornecendo retornos de chamada para serviços ELSs</span><span class="sxs-lookup"><span data-stu-id="963c9-103">Providing Callbacks for ELS Services</span></span>

<span data-ttu-id="963c9-104">Se seu aplicativo estiver usando operações assíncronas para reconhecimento de texto, ele deverá fornecer uma função de retorno de chamada para o serviço ELS usar.</span><span class="sxs-lookup"><span data-stu-id="963c9-104">If your application is using asynchronous operations for text recognition, it must provide a callback function for the ELS service to use.</span></span> <span data-ttu-id="963c9-105">A função de retorno de chamada é baseada no protótipo do [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc) .</span><span class="sxs-lookup"><span data-stu-id="963c9-105">The callback function is based on the [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc) prototype.</span></span>

<span data-ttu-id="963c9-106">O tópico [solicitando reconhecimento de texto](requesting-text-recognition.md) descreve como seu aplicativo pode solicitar reconhecimento de texto assíncrono de um serviço ELS.</span><span class="sxs-lookup"><span data-stu-id="963c9-106">The [Requesting Text Recognition](requesting-text-recognition.md) topic describes how your application can request asynchronous text recognition from an ELS service.</span></span> <span data-ttu-id="963c9-107">O exemplo a seguir mostra um aplicativo que faz uma chamada assíncrona para [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span><span class="sxs-lookup"><span data-stu-id="963c9-107">The following example shows an application that makes an asynchronous call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="963c9-108">A função de retorno de chamada para reconhecimento de texto é chamada de **RecognizeCallback**.</span><span class="sxs-lookup"><span data-stu-id="963c9-108">The callback function for text recognition is called **RecognizeCallback**.</span></span> <span data-ttu-id="963c9-109">Observe que o aplicativo deve garantir que o recipiente de propriedades, o texto de entrada, as opções e o serviço sejam todos válidos até que a função de chamada de retorno tenha terminado a execução.</span><span class="sxs-lookup"><span data-stu-id="963c9-109">Note that the application must make sure that the property bag, the input text, the options, and the service are all valid until after the callback function has finished executing.</span></span> <span data-ttu-id="963c9-110">Além disso, o aplicativo deve garantir que [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) seja chamado imediatamente depois que a bolsa for consumida pela função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="963c9-110">Additionally, the application must ensure that [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) is called immediately after the bag is consumed by the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="963c9-111">Pode ser uma boa ideia que seu aplicativo use a função de retorno de chamada para liberar os recursos depois de concluir o processamento ou a cópia deles.</span><span class="sxs-lookup"><span data-stu-id="963c9-111">It might be a good idea for your application to use the callback function to free the resources after it has finished processing or copying them.</span></span>

 


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
void RecognizeCallback(
     PMAPPING_PROPERTY_BAG pBag, 
     LPVOID data, DWORD dwDataSize, 
     HRESULT Result); 

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



## <a name="related-topics"></a><span data-ttu-id="963c9-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="963c9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="963c9-113">Usando serviços lingüísticos estendidos</span><span class="sxs-lookup"><span data-stu-id="963c9-113">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="963c9-114">Solicitando reconhecimento de texto</span><span class="sxs-lookup"><span data-stu-id="963c9-114">Requesting Text Recognition</span></span>](requesting-text-recognition.md)
</dt> <dt>

[<span data-ttu-id="963c9-115">**MappingCallbackProc**</span><span class="sxs-lookup"><span data-stu-id="963c9-115">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)
</dt> <dt>

[<span data-ttu-id="963c9-116">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="963c9-116">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[<span data-ttu-id="963c9-117">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="963c9-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



