---
description: Este tópico descreve como o aplicativo carrega um módulo de recurso do Win32 PE no Windows Vista e posterior ou em um sistema operacional anterior. As chamadas são incluídas para liberar o módulo de recurso.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Carregando um módulo de recurso do Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c4c1906a4fc09dc39b805e8ad5a875d96fae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780970"
---
# <a name="loading-a-win32-pe-resource-module"></a><span data-ttu-id="5b0e4-104">Carregando um módulo de recurso do Win32 PE</span><span class="sxs-lookup"><span data-stu-id="5b0e4-104">Loading a Win32 PE Resource Module</span></span>

<span data-ttu-id="5b0e4-105">Este tópico descreve como o aplicativo carrega um módulo de recurso do Win32 PE no Windows Vista e posterior ou em um sistema operacional anterior.</span><span class="sxs-lookup"><span data-stu-id="5b0e4-105">This topic describes how the application loads a Win32 PE resource module on either Windows Vista and later or on an earlier operating system.</span></span> <span data-ttu-id="5b0e4-106">As chamadas são incluídas para liberar o módulo de recurso.</span><span class="sxs-lookup"><span data-stu-id="5b0e4-106">Calls are included for releasing the resource module.</span></span>

## <a name="load-the-resource-module-on-windows-vista-and-later"></a><span data-ttu-id="5b0e4-107">Carregar o módulo de recurso no Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="5b0e4-107">Load the Resource Module on Windows Vista and Later</span></span>

<span data-ttu-id="5b0e4-108">No Windows Vista e posterior, o aplicativo carrega o módulo de recurso usando uma chamada para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="5b0e4-108">On Windows Vista and later, the application loads the resource module using a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span> <span data-ttu-id="5b0e4-109">A operação recomendada é chamar essa função com ambos os sinalizadores especificados.</span><span class="sxs-lookup"><span data-stu-id="5b0e4-109">The recommended operation is to call this function with both flags specified.</span></span> <span data-ttu-id="5b0e4-110">Veja a seguir um exemplo de código de aplicativo que carrega um módulo com base nas configurações de idioma do sistema.</span><span class="sxs-lookup"><span data-stu-id="5b0e4-110">The following is an example of application code that loads a module based on system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="5b0e4-111">Carregar o módulo de recurso em sistemas operacionais anteriores ao Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b0e4-111">Load the Resource Module on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="5b0e4-112">Em sistemas operacionais anteriores ao Windows Vista, o aplicativo carrega um módulo de recurso com base em uma configuração de idioma compatível com o sistema operacional de destino, bem como no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="5b0e4-112">On pre-Windows Vista operating systems, the application loads a resource module based on a language setting that is compatible with the target operating system, as well as Windows Vista and later.</span></span> <span data-ttu-id="5b0e4-113">Para esse tipo de carregamento de módulo, o aplicativo deve chamar as funções de MUI [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span><span class="sxs-lookup"><span data-stu-id="5b0e4-113">For this type of module loading, the application must call the MUI functions [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span></span>


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="5b0e4-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b0e4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b0e4-115">Localizando recursos do Win32 PE</span><span class="sxs-lookup"><span data-stu-id="5b0e4-115">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> <dt>

[<span data-ttu-id="5b0e4-116">MUI: exemplo de configurações de Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="5b0e4-116">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="5b0e4-117">MUI: exemplo de configurações de Application-Specific (pré-Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="5b0e4-117">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
