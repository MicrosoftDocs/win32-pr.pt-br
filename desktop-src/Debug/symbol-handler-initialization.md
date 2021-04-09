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
# <a name="symbol-handler-initialization"></a><span data-ttu-id="0fa48-103">Inicialização do manipulador de símbolo</span><span class="sxs-lookup"><span data-stu-id="0fa48-103">Symbol Handler Initialization</span></span>

<span data-ttu-id="0fa48-104">O manipulador de símbolos foi projetado para rastrear vários conjuntos de arquivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="0fa48-104">The symbol handler is designed to track various sets of symbol files.</span></span>

<span data-ttu-id="0fa48-105">Para inicializar o manipulador de símbolo, chame a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="0fa48-105">To initialize the symbol handler, call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="0fa48-106">O parâmetro *hProcess* pode ser um número arbitrário exclusivo, um valor retornado da função [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) ou o identificador de qualquer processo em execução.</span><span class="sxs-lookup"><span data-stu-id="0fa48-106">The *hProcess* parameter can be a unique arbitrary number, a value returned from the [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) function, or the identifier of any running process.</span></span> <span data-ttu-id="0fa48-107">O parâmetro *fInvadeProcess* indica se o manipulador de símbolo deve enumerar os módulos carregados pelo processo e carregar os símbolos para cada um de seus módulos.</span><span class="sxs-lookup"><span data-stu-id="0fa48-107">The *fInvadeProcess* parameter indicates whether the symbol handler should enumerate the modules loaded by the process and load symbols for each of its modules.</span></span> <span data-ttu-id="0fa48-108">Se *fInvadeProcess* for **true**, o parâmetro *hProcess* deverá ser o valor retornado de **GetCurrentProcess** ou o identificador de um processo existente.</span><span class="sxs-lookup"><span data-stu-id="0fa48-108">If *fInvadeProcess* is **TRUE**, the *hProcess* parameter must be the value returned from **GetCurrentProcess** or the identifier of an existing process.</span></span> <span data-ttu-id="0fa48-109">Para atualizar essa lista, use a função [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .</span><span class="sxs-lookup"><span data-stu-id="0fa48-109">To refresh this list, use the [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) function.</span></span>

<span data-ttu-id="0fa48-110">Usar o *fInvadeProcess* é uma maneira simples de carregar todos os arquivos de símbolo para um processo.</span><span class="sxs-lookup"><span data-stu-id="0fa48-110">Using *fInvadeProcess* is a simple way to load all symbol files for a process.</span></span> <span data-ttu-id="0fa48-111">No entanto, o manipulador de símbolo não tentará carregar símbolos para módulos posteriormente carregados pela função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="0fa48-111">However, the symbol handler will not attempt to load symbols for modules subsequently loaded by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="0fa48-112">Você deve usar a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) nesse caso.</span><span class="sxs-lookup"><span data-stu-id="0fa48-112">You must use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function in this case.</span></span>

 

 
