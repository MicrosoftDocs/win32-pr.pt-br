---
description: Há uma variedade de funções para obter informações sobre processos.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Obtendo informações de processo adicionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98b4ed87fca02dfcee4cbcd36621fffb9920a3f320cfeac771507748a151cf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032116"
---
# <a name="obtaining-additional-process-information"></a>Obtendo informações de processo adicionais

Há uma variedade de funções para obter informações sobre processos. Algumas dessas funções podem ser usadas apenas para o processo de chamada, porque não têm um alçamento de processo como um parâmetro. Você pode usar funções que usam um handle de processo para obter informações sobre outros processos.

-   Para obter a cadeia de caracteres de linha de comando para o processo atual, use a [**função GetCommandLine.**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)
-   Para recuperar a [**estrutura STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) especificada quando o processo atual foi criado, use a [**função GetStartupInfo.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)
-   Para obter as informações de versão do header executável, use a [**função GetProcessVersion.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)
-   Para obter o caminho completo e o nome do arquivo executável que contém o código do processo, use a [**função GetModuleFileName.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
-   Para obter a contagem de alças para objetos gui (interface gráfica do usuário) em uso, use a [**função GetGuiResources.**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)
-   Para determinar se um processo está sendo depurado, use a [**função IsDebuggerPresent.**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
-   Para recuperar informações de contabilidade de todas as operações de E/S executadas pelo processo, use a [**função GetProcessIoCounters.**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)

 

 
