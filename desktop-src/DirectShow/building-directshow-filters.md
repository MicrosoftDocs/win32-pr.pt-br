---
description: Criando filtros do DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Criando filtros do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5553c4358f97809214ebbdea23c129aa7c214e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646042"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="24d35-103">Criando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="24d35-103">Building DirectShow Filters</span></span>

<span data-ttu-id="24d35-104">As classes base do DirectShow são recomendadas para a implementação de filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="24d35-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="24d35-105">Para criar com as classes base, execute as etapas a seguir, além das etapas listadas em [Configurando o ambiente de compilação](setting-up-the-build-environment.md):</span><span class="sxs-lookup"><span data-stu-id="24d35-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="24d35-106">Crie a biblioteca de classes base, localizada no diretório Samples \\ Multimedia \\ DirectShow \\ BaseClasses, no diretório raiz do SDK.</span><span class="sxs-lookup"><span data-stu-id="24d35-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="24d35-107">Há duas versões da biblioteca: uma versão comercial (Strmbase. lib) e uma versão de depuração (Strmbasd. lib).</span><span class="sxs-lookup"><span data-stu-id="24d35-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="24d35-108">Inclua o cabeçalho file Streams. h.</span><span class="sxs-lookup"><span data-stu-id="24d35-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="24d35-109">Use a \_ \_ Convenção de chamada stdcall.</span><span class="sxs-lookup"><span data-stu-id="24d35-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="24d35-110">Use a biblioteca de tempo de execução C multithread (depuração ou varejo, conforme apropriado).</span><span class="sxs-lookup"><span data-stu-id="24d35-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="24d35-111">Inclua um arquivo de definição (. def) que exporta as funções de DLL.</span><span class="sxs-lookup"><span data-stu-id="24d35-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="24d35-112">Veja a seguir um exemplo de um arquivo de definição.</span><span class="sxs-lookup"><span data-stu-id="24d35-112">The following is an example of a definition file.</span></span> <span data-ttu-id="24d35-113">Ele pressupõe que o arquivo de saída é nomeado MyFilter.dll.</span><span class="sxs-lookup"><span data-stu-id="24d35-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="24d35-114">Link para os seguintes arquivos lib.</span><span class="sxs-lookup"><span data-stu-id="24d35-114">Link to the following lib files.</span></span>

    |              |                                      |
    |--------------|--------------------------------------|
    | <span data-ttu-id="24d35-115">Depurar compilação</span><span class="sxs-lookup"><span data-stu-id="24d35-115">Debug Build</span></span>  | <span data-ttu-id="24d35-116">Strmbasd. lib, MSVCRTD. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="24d35-116">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="24d35-117">Build de varejo</span><span class="sxs-lookup"><span data-stu-id="24d35-117">Retail Build</span></span> | <span data-ttu-id="24d35-118">Strmbase. lib, msvcrt. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="24d35-118">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="24d35-119">Escolha a opção "ignorar bibliotecas padrão" nas configurações do vinculador.</span><span class="sxs-lookup"><span data-stu-id="24d35-119">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="24d35-120">Declare o ponto de entrada de DLL em seu código-fonte, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="24d35-120">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="24d35-121">Versões anteriores</span><span class="sxs-lookup"><span data-stu-id="24d35-121">Previous Versions</span></span>

<span data-ttu-id="24d35-122">Para versões da biblioteca de classes base antes do DirectShow 9,0, você também deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="24d35-122">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="24d35-123">Para compilações de depuração, defina a depuração do sinalizador de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="24d35-123">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="24d35-124">Esta etapa não é necessária para a versão da biblioteca de classes base que está disponível no DirectShow 9,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="24d35-124">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24d35-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24d35-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24d35-126">Classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="24d35-126">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="24d35-127">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="24d35-127">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



