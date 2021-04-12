---
title: Depurando WOW64
description: Aplicativos em execução no WOW64 podem ser depurados com um depurador hospedado em x86 ou um depurador nativo.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- Programação WOW64 de 64 bits do Windows, depuração
- Depurando programação de WOW64 de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366574"
---
# <a name="debugging-wow64"></a><span data-ttu-id="06024-105">Depurando WOW64</span><span class="sxs-lookup"><span data-stu-id="06024-105">Debugging WOW64</span></span>

<span data-ttu-id="06024-106">Os aplicativos em execução no WOW64 podem ser depurados de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="06024-106">Applications running under WOW64 can be debugged two ways:</span></span>

-   <span data-ttu-id="06024-107">Use um depurador hospedado em x86, como o NTSD, o WinDbg ou o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="06024-107">Use an x86-hosted debugger such as NTSD, WinDbg, or Visual Studio.</span></span> <span data-ttu-id="06024-108">O NTSD de 32 bits é instalado em% SystemRoot% \\ SysWOW64 em instalações de varejo.</span><span class="sxs-lookup"><span data-stu-id="06024-108">The 32-bit NTSD is installed to %systemroot%\\syswow64 on retail installations.</span></span> <span data-ttu-id="06024-109">Observe que os depuradores x86 podem ser usados para depurar código x86, mas não podem ser usados para desmontar ou definir pontos de interrupção dentro da camada de conversão WOW64 porque ele é um código nativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="06024-109">Note that x86 debuggers can be used to debug x86 code, but cannot be used to disassemble or set breakpoints within the WOW64 thunk layer because it is 64-bit native code.</span></span>
-   <span data-ttu-id="06024-110">Use um depurador nativo como o CDB, o NTSD ou o WinDbg e a extensão do depurador WOW64, Wow64exts.dll.</span><span class="sxs-lookup"><span data-stu-id="06024-110">Use a native debugger such as CDB, NTSD, or WinDbg and the WOW64 debugger extension, Wow64exts.dll.</span></span> <span data-ttu-id="06024-111">Se o depurador nativo for interrompido enquanto o processador estiver no modo x86, o depurador apresentará o processo como um processo x86.</span><span class="sxs-lookup"><span data-stu-id="06024-111">If the native debugger breaks while the processor is in x86 mode, the debugger presents the process as an x86 process.</span></span> <span data-ttu-id="06024-112">Se o processador estiver no modo nativo, o depurador apresentará o processo como nativo.</span><span class="sxs-lookup"><span data-stu-id="06024-112">If the processor is in native mode, the debugger presents the process as native.</span></span>

<span data-ttu-id="06024-113">O CDB, o NTSD e o WinDbg estão incluídos nas ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="06024-113">CDB, NTSD, and WinDbg are included in Debugging Tools for Windows.</span></span> <span data-ttu-id="06024-114">Para obter mais informações, consulte a documentação sobre [ferramentas de depuração para Windows](/windows-hardware/drivers/debugger/) .</span><span class="sxs-lookup"><span data-stu-id="06024-114">For more information, see the [Debugging Tools for Windows](/windows-hardware/drivers/debugger/) documentation.</span></span>

<span data-ttu-id="06024-115">A extensão do depurador do Wow64exts é instalada com o WinDbg.</span><span class="sxs-lookup"><span data-stu-id="06024-115">The Wow64exts debugger extension is installed with WinDbg.</span></span> <span data-ttu-id="06024-116">Use o comando! load wow64exts para carregar a extensão do depurador.</span><span class="sxs-lookup"><span data-stu-id="06024-116">Use the !load wow64exts command to load the debugger extension.</span></span> <span data-ttu-id="06024-117">A tabela a seguir lista os comandos de extensão do depurador! wow64exts.</span><span class="sxs-lookup"><span data-stu-id="06024-117">The following table lists the !wow64exts debugger extension commands.</span></span>



| <span data-ttu-id="06024-118">Comando</span><span class="sxs-lookup"><span data-stu-id="06024-118">Command</span></span>                | <span data-ttu-id="06024-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="06024-119">Description</span></span>                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06024-120">! wow64exts. SW</span><span class="sxs-lookup"><span data-stu-id="06024-120">!wow64exts.sw</span></span>          | <span data-ttu-id="06024-121">Alterna entre o modo x86 e nativo.</span><span class="sxs-lookup"><span data-stu-id="06024-121">Switches between x86 and native mode.</span></span>                                                                                                    |
| <span data-ttu-id="06024-122">! *contagem* de wow64exts. k</span><span class="sxs-lookup"><span data-stu-id="06024-122">!wow64exts.k *count*</span></span>   | <span data-ttu-id="06024-123">Despeja um rastreamento de pilha de 32 bits/64 bits combinado.</span><span class="sxs-lookup"><span data-stu-id="06024-123">Dumps a combined 32-bit/64-bit stack trace.</span></span> <span data-ttu-id="06024-124">Se *Count* for especificado, o comando despejará os primeiros endereços de *contagem* em cada rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="06024-124">If *count* is specified, the command dumps the first *count* addresses in each stack trace.</span></span>  |
| <span data-ttu-id="06024-125">! wow64exts.info</span><span class="sxs-lookup"><span data-stu-id="06024-125">!wow64exts.info</span></span>        | <span data-ttu-id="06024-126">Despeja informações básicas sobre o PEB do processo, o TEB do thread atual e os slots de armazenamento local de thread (TLS) usados pelo WOW64.</span><span class="sxs-lookup"><span data-stu-id="06024-126">Dumps basic information about the PEB of the process, the TEB of the current thread, and thread local storage (TLS) slots used by WOW64.</span></span> |
| <span data-ttu-id="06024-127">! wow64exts. r *Address*</span><span class="sxs-lookup"><span data-stu-id="06024-127">!wow64exts.r *address*</span></span> | <span data-ttu-id="06024-128">Despeja o contexto para o endereço especificado.</span><span class="sxs-lookup"><span data-stu-id="06024-128">Dumps context for the specified address.</span></span> <span data-ttu-id="06024-129">Se o *endereço* não for especificado, o comando despejará o contexto do processador.</span><span class="sxs-lookup"><span data-stu-id="06024-129">If *address* is not specified, the command dumps context for the processor.</span></span>                     |



 

 

 