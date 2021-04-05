---
description: A função OutputDebugString envia uma cadeia de caracteres do processo que está sendo depurado para o depurador, gerando um evento de depuração de evento de cadeia de depuração de saída \_ \_ \_ . Um processo pode detectar se está sendo depurado chamando a função IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicando-se com o depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826096"
---
# <a name="communicating-with-the-debugger"></a><span data-ttu-id="17192-104">Comunicando-se com o depurador</span><span class="sxs-lookup"><span data-stu-id="17192-104">Communicating with the Debugger</span></span>

<span data-ttu-id="17192-105">A função [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) envia uma cadeia de caracteres do processo que está sendo depurado para o depurador, gerando um evento de depuração de evento de cadeia de depuração de saída \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="17192-105">The [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) function sends a string from the process being debugged to the debugger by generating an OUTPUT\_DEBUG\_STRING\_EVENT debugging event.</span></span> <span data-ttu-id="17192-106">Um processo pode detectar se está sendo depurado chamando a função [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="17192-106">A process can detect whether it is being debugged by calling the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>

<span data-ttu-id="17192-107">A função [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) causa uma exceção de ponto de interrupção no processo atual.</span><span class="sxs-lookup"><span data-stu-id="17192-107">The [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function causes a breakpoint exception in the current process.</span></span> <span data-ttu-id="17192-108">Um ponto de interrupção é um local em um programa em que a execução é interrompida para permitir que o desenvolvedor examine o código, as variáveis e os valores de registro do programa e, conforme necessário, para fazer alterações, continuar a execução ou encerrar a execução.</span><span class="sxs-lookup"><span data-stu-id="17192-108">A breakpoint is a location in a program where execution is stopped to allow the developer to examine the program's code, variables, and register values and, as necessary, to make changes, continue execution, or terminate execution.</span></span>

<span data-ttu-id="17192-109">A função [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) encerra o processo atual e fornece controle de execução para o depurador, mas ao contrário de [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), ele não gera uma exceção.</span><span class="sxs-lookup"><span data-stu-id="17192-109">The [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) function terminates the current process and gives execution control to the debugger, but unlike [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), it does not generate an exception.</span></span> <span data-ttu-id="17192-110">Essa função só deve ser usada como último recurso, pois nem sempre libera a memória do processo nem fecha seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="17192-110">This function should only be used as a last resort, because it does not always free the process's memory or close its files.</span></span>

 

 
