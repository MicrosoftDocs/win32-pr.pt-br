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
# <a name="loading-language-resources"></a>Carregando recursos de idioma

Seu aplicativo carrega todos os recursos de idioma da interface do usuário, além de determinadas cadeias de caracteres de registro redirecionadas, usando chamadas para funções de carregamento de recursos padrão, por exemplo, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)e [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea). Muitas funções de carregamento de recursos foram modificadas para carregar recursos de arquivos de recursos específicos de idioma automaticamente, tratando os recursos como se eles estivessem no arquivo LN. O exemplo a seguir ilustra o uso de **LoadString** para carregar cadeias de caracteres de linguagem para um aplicativo que siga as configurações de idioma do sistema.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localizando recursos do Win32 PE](locating-win32-pe-resources.md)
</dt> </dl>

 

 
