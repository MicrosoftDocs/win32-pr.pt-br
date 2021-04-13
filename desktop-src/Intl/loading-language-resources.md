---
description: Carregando recursos de idioma
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Carregando recursos de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6917f03e773a470288fb4c9577812e0b38868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297710"
---
# <a name="loading-language-resources"></a><span data-ttu-id="f3be1-103">Carregando recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="f3be1-103">Loading Language Resources</span></span>

<span data-ttu-id="f3be1-104">Seu aplicativo carrega todos os recursos de idioma da interface do usuário, além de determinadas cadeias de caracteres de registro redirecionadas, usando chamadas para funções de carregamento de recursos padrão, por exemplo, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)e [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span><span class="sxs-lookup"><span data-stu-id="f3be1-104">Your application loads all user interface language resources, other than certain redirected registry strings, using calls to standard resource loading functions, for example, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), and [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span></span> <span data-ttu-id="f3be1-105">Muitas funções de carregamento de recursos foram modificadas para carregar recursos de arquivos de recursos específicos de idioma automaticamente, tratando os recursos como se eles estivessem no arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="f3be1-105">Many resource loading functions have been modified to load resources from language-specific resource files automatically, treating resources as if they are contained in the LN file.</span></span> <span data-ttu-id="f3be1-106">O exemplo a seguir ilustra o uso de **LoadString** para carregar cadeias de caracteres de linguagem para um aplicativo que siga as configurações de idioma do sistema.</span><span class="sxs-lookup"><span data-stu-id="f3be1-106">The following example illustrates the use of **LoadString** to load language strings for an application that follows system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="f3be1-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3be1-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3be1-108">Localizando recursos do Win32 PE</span><span class="sxs-lookup"><span data-stu-id="f3be1-108">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> </dl>

 

 
