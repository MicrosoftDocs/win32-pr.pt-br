---
description: As funções a seguir são usadas na vinculação dinâmica.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Dynamic-Link funções de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47ce37b6f91570ce9f3314fc329b5e85cde310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837009"
---
# <a name="dynamic-link-library-functions"></a>Dynamic-Link funções de biblioteca

As funções a seguir são usadas na vinculação dinâmica.



| Função                                                       | Descrição                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Adiciona um diretório ao caminho de pesquisa da DLL do processo.                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Desabilita a anexação de threads e notificações de desanexação de thread para a DLL especificada.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Um ponto de entrada opcional em uma DLL.                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Decrementa a contagem de referência da DLL carregada. Quando a contagem de referência chega a zero, o módulo não é mapeado do espaço de endereço do processo de chamada. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Decrementa a contagem de referência de uma DLL carregada por uma e, em seguida, chama [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) para encerrar o thread de chamada.                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Recupera a parte específica do aplicativo do caminho de pesquisa usado para localizar DLLs para o aplicativo.                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Recupera o caminho totalmente qualificado para o arquivo que contém o módulo especificado.                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Recupera o caminho totalmente qualificado para o arquivo que contém o módulo especificado.                                                                               |
| [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Recupera um identificador de módulo para o módulo especificado.                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Recupera um identificador de módulo para o módulo especificado.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Recupera o endereço de uma função ou variável exportada da DLL especificada.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Mapeia o módulo executável especificado no espaço de endereço do processo de chamada.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Mapeia o módulo executável especificado no espaço de endereço do processo de chamada.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Mapeia o módulo de pacote especificado e suas dependências no espaço de endereço do processo de chamada. Somente os aplicativos da Windows Store podem chamar essa função.         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Remove um diretório que foi adicionado ao caminho de pesquisa de DLL do processo usando [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Especifica um conjunto padrão de diretórios a serem pesquisados quando o processo de chamada carregar uma DLL.                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Modifica o caminho de pesquisa usado para localizar DLLs para o aplicativo.                                                                                              |



 

## <a name="obsolete-functions"></a>Funções obsoletas

Essas funções são fornecidas apenas para compatibilidade com versões de 16 bits do Windows.

[**LoadModule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
