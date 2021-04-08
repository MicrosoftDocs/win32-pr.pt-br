---
description: Os termos a seguir são usados ao descrever a depuração.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminologia de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920118"
---
# <a name="debugging-terminology"></a><span data-ttu-id="7e904-103">Terminologia de depuração</span><span class="sxs-lookup"><span data-stu-id="7e904-103">Debugging Terminology</span></span>

<span data-ttu-id="7e904-104">Os termos a seguir são usados ao descrever a depuração.</span><span class="sxs-lookup"><span data-stu-id="7e904-104">The following terms are used when describing debugging.</span></span>

<dl> <dt>

<span data-ttu-id="7e904-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Tela azul</span><span class="sxs-lookup"><span data-stu-id="7e904-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blue screen</span></span>
</dt> <dd>

<span data-ttu-id="7e904-106">Quando o sistema encontra um problema de hardware, inconsistência de dados ou erro semelhante, ele pode exibir uma tela azul contendo informações que podem ser usadas para determinar a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="7e904-106">When the system encounters a hardware problem, data inconsistency, or similar error, it may display a blue screen containing information that can be used to determine the cause of the error.</span></span> <span data-ttu-id="7e904-107">Essas informações incluem o código de parada e se um arquivo de despejo de memória foi criado.</span><span class="sxs-lookup"><span data-stu-id="7e904-107">This information includes the STOP code and whether a crash dump file was created.</span></span> <span data-ttu-id="7e904-108">Ele também pode incluir uma lista de Drivers carregados e um rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="7e904-108">It may also include a list of loaded drivers and a stack trace.</span></span>

</dd> <dt>

<span data-ttu-id="7e904-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Arquivo de despejo de memória</span><span class="sxs-lookup"><span data-stu-id="7e904-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Crash dump file</span></span>
</dt> <dd>

<span data-ttu-id="7e904-110">Você pode configurar o sistema para gravar informações em um arquivo de despejo de memória no disco rígido sempre que um código de parada for gerado.</span><span class="sxs-lookup"><span data-stu-id="7e904-110">You can configure the system to write information to a crash dump file on your hard disk whenever a STOP code is generated.</span></span> <span data-ttu-id="7e904-111">O arquivo contém informações que o depurador pode usar para analisar o erro.</span><span class="sxs-lookup"><span data-stu-id="7e904-111">The file contains information the debugger can use to analyze the error.</span></span> <span data-ttu-id="7e904-112">Esse arquivo pode ser tão grande quanto a memória física contida no computador.</span><span class="sxs-lookup"><span data-stu-id="7e904-112">This file can be as big as the physical memory contained in the computer.</span></span>

</dd> <dt>

<span data-ttu-id="7e904-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Depurador</span><span class="sxs-lookup"><span data-stu-id="7e904-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span></span>
</dt> <dd>

<span data-ttu-id="7e904-114">Um programa projetado para ajudar a detectar, localizar e corrigir erros em outro programa.</span><span class="sxs-lookup"><span data-stu-id="7e904-114">A program designed to help detect, locate, and correct errors in another program.</span></span> <span data-ttu-id="7e904-115">Ele permite que o desenvolvedor percorra a execução do processo e seus threads, memória de monitoramento, variáveis e outros elementos de contexto de processo e thread.</span><span class="sxs-lookup"><span data-stu-id="7e904-115">It allows the developer to step through the execution of the process and its threads, monitoring memory, variables, and other elements of process and thread context.</span></span>

</dd> <dt>

<span data-ttu-id="7e904-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Modo kernel</span><span class="sxs-lookup"><span data-stu-id="7e904-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel mode</span></span>
</dt> <dd>

<span data-ttu-id="7e904-117">O modo do processador no qual os serviços do sistema e os drivers de dispositivo são executados.</span><span class="sxs-lookup"><span data-stu-id="7e904-117">The processor mode in which system services and device drivers run.</span></span> <span data-ttu-id="7e904-118">Todas as interfaces e instruções de CPU estão disponíveis e toda a memória está acessível.</span><span class="sxs-lookup"><span data-stu-id="7e904-118">All interfaces and CPU instructions are available, and all memory is accessible.</span></span>

</dd> <dt>

<span data-ttu-id="7e904-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Arquivo de minidespejo</span><span class="sxs-lookup"><span data-stu-id="7e904-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidump file</span></span>
</dt> <dd>

<span data-ttu-id="7e904-120">Os aplicativos podem produzir arquivos de minidespejo de modo de usuário, que contêm um subconjunto útil das informações contidas em um arquivo de despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="7e904-120">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="7e904-121">Para obter mais informações, consulte [arquivos de minidespejo](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="7e904-121">For more information, see [Minidump Files](minidump-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e904-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>Código de parada</span><span class="sxs-lookup"><span data-stu-id="7e904-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>STOP code</span></span>
</dt> <dd>

<span data-ttu-id="7e904-123">O código de erro que identifica o erro que interrompeu o kernel do sistema de continuar a execução.</span><span class="sxs-lookup"><span data-stu-id="7e904-123">The error code that identifies the error that stopped the system kernel from continuing to run.</span></span>

</dd> <dt>

<span data-ttu-id="7e904-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Arquivos de símbolo</span><span class="sxs-lookup"><span data-stu-id="7e904-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol files</span></span>
</dt> <dd>

<span data-ttu-id="7e904-125">Todos os aplicativos de sistema, drivers e DLLs são criados de forma que suas informações de depuração residam em arquivos separados conhecidos como arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="7e904-125">All system applications, drivers, and DLLs are built such that their debugging information resides in separate files known as symbol files.</span></span> <span data-ttu-id="7e904-126">Portanto, o sistema é menor e mais rápido, embora ainda possa ser depurado se os arquivos de símbolo estiverem instalados.</span><span class="sxs-lookup"><span data-stu-id="7e904-126">Therefore, the system is smaller and faster, yet it can still be debugged if the symbol files are installed.</span></span> <span data-ttu-id="7e904-127">Para obter mais informações, consulte [Symbol files](symbol-files.md).</span><span class="sxs-lookup"><span data-stu-id="7e904-127">For more information, see [Symbol Files](symbol-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e904-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Modo de usuário</span><span class="sxs-lookup"><span data-stu-id="7e904-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>User mode</span></span>
</dt> <dd>

<span data-ttu-id="7e904-129">O modo de processador no qual os aplicativos são executados.</span><span class="sxs-lookup"><span data-stu-id="7e904-129">The processor mode in which applications run.</span></span> <span data-ttu-id="7e904-130">Um conjunto limitado de interfaces está disponível nesse modo e o acesso aos dados do sistema é limitado.</span><span class="sxs-lookup"><span data-stu-id="7e904-130">A limited set of interfaces are available in this mode, and access to system data is limited.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7e904-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e904-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e904-132">Configurando a depuração automática</span><span class="sxs-lookup"><span data-stu-id="7e904-132">Configuring Automatic Debugging</span></span>](configuring-automatic-debugging.md)
</dt> </dl>

 

 



