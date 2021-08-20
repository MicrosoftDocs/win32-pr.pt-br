---
description: este tópico descreve como o aplicativo carrega um módulo de recurso do Win32 PE em qualquer Windows Vista e posterior ou em um sistema operacional anterior. As chamadas são incluídas para liberar o módulo de recurso.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Carregando um módulo de recurso do Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: affcd1cf582d81aafd70f208531e03723ea44b314f92848f35dfd391f950b0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145838"
---
# <a name="loading-a-win32-pe-resource-module"></a>Carregando um módulo de recurso do Win32 PE

este tópico descreve como o aplicativo carrega um módulo de recurso do Win32 PE em qualquer Windows Vista e posterior ou em um sistema operacional anterior. As chamadas são incluídas para liberar o módulo de recurso.

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>carregar o módulo de recurso no Windows Vista e posterior

no Windows Vista e posterior, o aplicativo carrega o módulo de recurso usando uma chamada para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa). A operação recomendada é chamar essa função com ambos os sinalizadores especificados. Veja a seguir um exemplo de código de aplicativo que carrega um módulo com base nas configurações de idioma do sistema.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>carregar o módulo de recurso em sistemas operacionais anteriores ao Windows Vista

em sistemas operacionais anteriores ao Windows Vista, o aplicativo carrega um módulo de recurso com base em uma configuração de idioma compatível com o sistema operacional de destino, bem como Windows Vista e posterior. Para esse tipo de carregamento de módulo, o aplicativo deve chamar as funções de MUI [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localizando recursos do Win32 PE](locating-win32-pe-resources.md)
</dt> <dt>

[MUI: exemplo de Configurações de Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI: exemplo de Configurações de Application-Specific (pré-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
