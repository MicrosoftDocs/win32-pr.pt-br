---
description: As funções a seguir são usadas na vinculação dinâmica.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: funções Dynamic-Link biblioteca do Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521c9200b3fa6585ec2804d76ac385845dcd6fb56ef4e7b70a7a3d9bd59150c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070576"
---
# <a name="dynamic-link-library-functions"></a>funções Dynamic-Link biblioteca do Dynamic-Link

As funções a seguir são usadas na vinculação dinâmica.



| Função                                                       | Descrição                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Adiciona um diretório ao caminho de pesquisa de DLL do processo.                                                                                                               |
| [**Disablethreadlibrarycalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Desabilita as notificações de anexação de thread e de desacoplar thread para a DLL especificada.                                                                                  |
| [**Dllmain**](dllmain.md)                                     | Um ponto de entrada opcional em uma DLL.                                                                                                                            |
| [**Freelibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Diminui a contagem de referência da DLL carregada. Quando a contagem de referência atinge zero, o módulo é não mapeado do espaço de endereço do processo de chamada. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Diminui a contagem de referência de uma DLL carregada em um e, em seguida, chama [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) para encerrar o thread de chamada.                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Recupera a parte específica do aplicativo do caminho de pesquisa usado para localizar DLLs para o aplicativo.                                                         |
| [**Getmodulefilename**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Recupera o caminho totalmente qualificado para o arquivo que contém o módulo especificado.                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Recupera o caminho totalmente qualificado para o arquivo que contém o módulo especificado.                                                                               |
| [**Getmodulehandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Recupera um alça de módulo para o módulo especificado.                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Recupera um alça de módulo para o módulo especificado.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Recupera o endereço de uma função ou variável exportada da DLL especificada.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Mapas módulo executável especificado no espaço de endereço do processo de chamada.                                                                            |
| [**Loadlibraryex**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Mapas módulo executável especificado no espaço de endereço do processo de chamada.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Mapas módulo empacotado especificado e suas dependências no espaço de endereço do processo de chamada. Somente Windows aplicativos da Store podem chamar essa função.         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Remove um diretório que foi adicionado ao caminho de pesquisa de DLL do processo usando [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Especifica um conjunto padrão de diretórios a ser pesquisado quando o processo de chamada carrega uma DLL.                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Modifica o caminho de pesquisa usado para localizar DLLs para o aplicativo.                                                                                              |



 

## <a name="obsolete-functions"></a>Funções obsoletas

Essas funções são fornecidas apenas para compatibilidade com versões de 16 bits do Windows.

[**Loadmodule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
