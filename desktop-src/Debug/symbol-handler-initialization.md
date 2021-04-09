---
description: O manipulador de símbolos foi projetado para rastrear vários conjuntos de arquivos de símbolos.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Inicialização do manipulador de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088955"
---
# <a name="symbol-handler-initialization"></a>Inicialização do manipulador de símbolo

O manipulador de símbolos foi projetado para rastrear vários conjuntos de arquivos de símbolos.

Para inicializar o manipulador de símbolo, chame a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . O parâmetro *hProcess* pode ser um número arbitrário exclusivo, um valor retornado da função [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) ou o identificador de qualquer processo em execução. O parâmetro *fInvadeProcess* indica se o manipulador de símbolo deve enumerar os módulos carregados pelo processo e carregar os símbolos para cada um de seus módulos. Se *fInvadeProcess* for **true**, o parâmetro *hProcess* deverá ser o valor retornado de **GetCurrentProcess** ou o identificador de um processo existente. Para atualizar essa lista, use a função [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .

Usar o *fInvadeProcess* é uma maneira simples de carregar todos os arquivos de símbolo para um processo. No entanto, o manipulador de símbolo não tentará carregar símbolos para módulos posteriormente carregados pela função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Você deve usar a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) nesse caso.

 

 
