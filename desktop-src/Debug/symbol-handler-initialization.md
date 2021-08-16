---
description: O manipulador de símbolos foi projetado para rastrear vários conjuntos de arquivos de símbolos.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Inicialização do manipulador de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d3664a564b0198d97549f2815abebf0e5e6058beb197ed33ca191a64407f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406076"
---
# <a name="symbol-handler-initialization"></a>Inicialização do manipulador de símbolo

O manipulador de símbolos foi projetado para rastrear vários conjuntos de arquivos de símbolos.

Para inicializar o manipulador de símbolo, chame a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . O parâmetro *hProcess* pode ser um número arbitrário exclusivo, um valor retornado da função [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) ou o identificador de qualquer processo em execução. O parâmetro *fInvadeProcess* indica se o manipulador de símbolo deve enumerar os módulos carregados pelo processo e carregar os símbolos para cada um de seus módulos. Se *fInvadeProcess* for **true**, o parâmetro *hProcess* deverá ser o valor retornado de **GetCurrentProcess** ou o identificador de um processo existente. Para atualizar essa lista, use a função [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .

Usar o *fInvadeProcess* é uma maneira simples de carregar todos os arquivos de símbolo para um processo. No entanto, o manipulador de símbolo não tentará carregar símbolos para módulos posteriormente carregados pela função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Você deve usar a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) nesse caso.

 

 
