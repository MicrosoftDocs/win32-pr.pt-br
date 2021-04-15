---
description: Há uma variedade de funções para obter informações sobre processos.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Obtendo informações adicionais sobre o processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505873"
---
# <a name="obtaining-additional-process-information"></a>Obtendo informações adicionais sobre o processo

Há uma variedade de funções para obter informações sobre processos. Algumas dessas funções podem ser usadas somente para o processo de chamada, pois não usam um identificador de processo como parâmetro. Você pode usar funções que usam um identificador de processo para obter informações sobre outros processos.

-   Para obter a cadeia de caracteres de linha de comando para o processo atual, use a função [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .
-   Para recuperar a estrutura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) especificada quando o processo atual foi criado, use a função [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .
-   Para obter as informações de versão do cabeçalho executável, use a função [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .
-   Para obter o caminho completo e o nome do arquivo executável que contém o código do processo, use a função [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .
-   Para obter a contagem de identificadores para objetos GUI (interface gráfica do usuário) em uso, use a função [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .
-   Para determinar se um processo está sendo depurado, use a função [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .
-   Para recuperar informações de estatísticas de todas as operações de e/s executadas pelo processo, use a função [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .

 

 
