---
description: Para coletar informações de rastreamento para a infraestrutura do VSS, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Usando ferramentas de rastreamento com VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164497"
---
# <a name="using-tracing-tools-with-vss"></a><span data-ttu-id="d4a9a-103">Usando ferramentas de rastreamento com VSS</span><span class="sxs-lookup"><span data-stu-id="d4a9a-103">Using Tracing Tools with VSS</span></span>

<span data-ttu-id="d4a9a-104">Para coletar informações de rastreamento para a infraestrutura do VSS, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta tracelog.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-104">To collect tracing information for the VSS infrastructure, you can use the VssTrace tool, the Logman tool, or the Tracelog tool.</span></span> <span data-ttu-id="d4a9a-105">O VssTrace está disponível no SDK (Software Development Kit) do Microsoft Windows e pode ser usado para rastrear aplicativos VSS no Windows 7 e versões posteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-105">VssTrace is available in the Microsoft Windows Software Development Kit (SDK) and can be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="d4a9a-106">Logman é um controlador de rastreamento para eventos de rastreamento e contadores de desempenho; Ele também pode ser usado para rastrear aplicativos VSS no Windows 7 e versões posteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-106">Logman is a trace controller for trace events and performance counters; it can also be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="d4a9a-107">O tracelog está incluído no Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="d4a9a-107">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="d4a9a-108">Para usar as ferramentas de rastreamento com o [ASR (recuperação automatizada do sistema)](using-vss-automated-system-recovery-for-disaster-recovery.md), consulte [usando ferramentas de rastreamento com aplicativos ASR](using-tracing-tools-with-vss-asr-applications.md).</span><span class="sxs-lookup"><span data-stu-id="d4a9a-108">To use tracing tools with [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), see [Using Tracing Tools with ASR Applications](using-tracing-tools-with-vss-asr-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="d4a9a-109">VssTrace, logman e tracelog All exigem privilégio de administrador.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-109">VssTrace, Logman, and Tracelog all require administrator privilege.</span></span>

 

<span data-ttu-id="d4a9a-110">Para obter informações sobre cada ferramenta, consulte as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-110">For information about each tool, see the following sections:</span></span>

-   [<span data-ttu-id="d4a9a-111">Usando VssTrace</span><span class="sxs-lookup"><span data-stu-id="d4a9a-111">Using VssTrace</span></span>](#using-vsstrace)
    -   [<span data-ttu-id="d4a9a-112">Opções de Command-Line de VssTrace</span><span class="sxs-lookup"><span data-stu-id="d4a9a-112">VssTrace Command-Line Options</span></span>](#vsstrace-command-line-options)
-   [<span data-ttu-id="d4a9a-113">Usando logman</span><span class="sxs-lookup"><span data-stu-id="d4a9a-113">Using Logman</span></span>](#using-logman)
-   [<span data-ttu-id="d4a9a-114">Usando tracelog</span><span class="sxs-lookup"><span data-stu-id="d4a9a-114">Using Tracelog</span></span>](#using-tracelog)

## <a name="using-vsstrace"></a><span data-ttu-id="d4a9a-115">Usando VssTrace</span><span class="sxs-lookup"><span data-stu-id="d4a9a-115">Using VssTrace</span></span>

<span data-ttu-id="d4a9a-116">Para executar a ferramenta VssTrace na linha de comando, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-116">To run the VssTrace tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="d4a9a-117"> *Opções de linha de comando* vsstrace</span><span class="sxs-lookup"><span data-stu-id="d4a9a-117">**vsstrace** *command-line-options*</span></span>

<span data-ttu-id="d4a9a-118">Para exibir a ajuda de linha de comando concisa para a ferramenta VssTrace, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-118">To display concise command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="d4a9a-119">**vsstrace-ajuda**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-119">**vsstrace -help**</span></span>

<span data-ttu-id="d4a9a-120">Para exibir a ajuda de linha de comando detalhada para a ferramenta VssTrace, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-120">To display detailed command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="d4a9a-121">**vsstrace-ajuda de tudo**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-121">**vsstrace -help all**</span></span>

### <a name="vsstrace-command-line-options"></a><span data-ttu-id="d4a9a-122">Opções de Command-Line de VssTrace</span><span class="sxs-lookup"><span data-stu-id="d4a9a-122">VssTrace Command-Line Options</span></span>

<span data-ttu-id="d4a9a-123">A ferramenta VssTrace usa as seguintes opções de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-123">The VssTrace tool uses the following command-line options:</span></span>

<dl> <dt>

<span data-ttu-id="d4a9a-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *Flags*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-125">Habilite os módulos cujos sinalizadores são especificados pelo bitmask dos *sinalizadores* .</span><span class="sxs-lookup"><span data-stu-id="d4a9a-125">Enable the modules whose flags are specified by the *Flags* bitmask.</span></span> <span data-ttu-id="d4a9a-126">Cada sinalizador corresponde a um módulo VSS.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-126">Each flag corresponds to a VSS module.</span></span> <span data-ttu-id="d4a9a-127">Se *flags* for zero, nenhum módulo será habilitado.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-127">If *Flags* is zero, no modules are enabled.</span></span> <span data-ttu-id="d4a9a-128">Observe que a maioria dos módulos está habilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-128">Note that most modules are enabled by default.</span></span> <span data-ttu-id="d4a9a-129">Essa opção pode ser combinada com a **+** opção de _módulo_ .</span><span class="sxs-lookup"><span data-stu-id="d4a9a-129">This option can be combined with the **+**_Module_ option.</span></span> <span data-ttu-id="d4a9a-130">Por exemplo, **vsstrace-f 0 + Writer + coord** desabilita o rastreamento de todos os módulos que estão habilitados por padrão e habilita o rastreamento de gravadores VSS e o serviço VSS.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-130">For example, **vsstrace -f 0 +WRITER +COORD** disables tracing of all of the modules that are enabled by default and enables tracing of VSS writers and the VSS service.</span></span> <span data-ttu-id="d4a9a-131">Como alternativa, **vsstrace + f 0xFFFF-coord** habilita o rastreamento de todos os módulos, exceto o serviço VSS.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-131">Alternatively, **vsstrace +f 0xffff -COORD** enables tracing of all modules except the VSS service.</span></span>

> [!Note]  
> <span data-ttu-id="d4a9a-132">Se você usar a opção **-f** junto com a **+** opção de _módulo_ , o **-f** deverá aparecer antes da opção de **+** _módulo_ .</span><span class="sxs-lookup"><span data-stu-id="d4a9a-132">If you use the **-f** option together with the **+**_Module_ option, the **-f** must appear before the **+**_Module_ option.</span></span>

 

<span data-ttu-id="d4a9a-133">A tabela a seguir lista o nome do módulo e o sinalizador para cada módulo disponível.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-133">The following table lists the module name and flag for each available module.</span></span>

| <span data-ttu-id="d4a9a-134">Módulo</span><span class="sxs-lookup"><span data-stu-id="d4a9a-134">Module</span></span> | <span data-ttu-id="d4a9a-135">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="d4a9a-135">Flag</span></span>       | <span data-ttu-id="d4a9a-136">Habilitado por padrão</span><span class="sxs-lookup"><span data-stu-id="d4a9a-136">Enabled by default</span></span> | <span data-ttu-id="d4a9a-137">Itens rastreados</span><span class="sxs-lookup"><span data-stu-id="d4a9a-137">Items traced</span></span>                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a9a-138">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="d4a9a-138">EXCEPT</span></span> | <span data-ttu-id="d4a9a-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d4a9a-139">0x00000001</span></span> | <span data-ttu-id="d4a9a-140">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-140">Yes</span></span>                | <span data-ttu-id="d4a9a-141">Manipulação de exceção de C++.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-141">C++ exception handling.</span></span>                                                                                                                       |
| <span data-ttu-id="d4a9a-142">COORD</span><span class="sxs-lookup"><span data-stu-id="d4a9a-142">COORD</span></span>  | <span data-ttu-id="d4a9a-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d4a9a-143">0x00000002</span></span> | <span data-ttu-id="d4a9a-144">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-144">Yes</span></span>                | <span data-ttu-id="d4a9a-145">O serviço VSS, que também é chamado de coordenador VSS.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-145">The VSS service, which is also called the VSS coordinator.</span></span>                                                                                    |
| <span data-ttu-id="d4a9a-146">SWPRV</span><span class="sxs-lookup"><span data-stu-id="d4a9a-146">SWPRV</span></span>  | <span data-ttu-id="d4a9a-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d4a9a-147">0x00000004</span></span> | <span data-ttu-id="d4a9a-148">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-148">Yes</span></span>                | <span data-ttu-id="d4a9a-149">O serviço do provedor de cópia de sombra do sistema do VSS.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-149">The VSS System Shadow Copy Provider service.</span></span>                                                                                                  |
| <span data-ttu-id="d4a9a-150">BUCOMP</span><span class="sxs-lookup"><span data-stu-id="d4a9a-150">BUCOMP</span></span> | <span data-ttu-id="d4a9a-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d4a9a-151">0x00000008</span></span> | <span data-ttu-id="d4a9a-152">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-152">Yes</span></span>                | <span data-ttu-id="d4a9a-153">O solicitante do VSS e o processamento de metadados de backup.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-153">The VSS requester and backup metadata processing.</span></span>                                                                                             |
| <span data-ttu-id="d4a9a-154">WRITER</span><span class="sxs-lookup"><span data-stu-id="d4a9a-154">WRITER</span></span> | <span data-ttu-id="d4a9a-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4a9a-155">0x00000010</span></span> | <span data-ttu-id="d4a9a-156">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-156">Yes</span></span>                | <span data-ttu-id="d4a9a-157">Operações do gravador VSS e implementações do gravador hospedado do VSS, como o gravador de registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-157">VSS writer operations and VSS hosted writer implementations, such as the Windows Registry writer.</span></span>                                             |
| <span data-ttu-id="d4a9a-158">VSSAPI</span><span class="sxs-lookup"><span data-stu-id="d4a9a-158">VSSAPI</span></span> | <span data-ttu-id="d4a9a-159">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d4a9a-159">0x00000020</span></span> | <span data-ttu-id="d4a9a-160">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-160">Yes</span></span>                | <span data-ttu-id="d4a9a-161">Funções diversas da API do VSS exportadas pelo VSSAPI.DLL.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-161">Miscellaneous functions of the VSS API exported by VSSAPI.DLL.</span></span>                                                                                |
| <span data-ttu-id="d4a9a-162">HWDIAG</span><span class="sxs-lookup"><span data-stu-id="d4a9a-162">HWDIAG</span></span> | <span data-ttu-id="d4a9a-163">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d4a9a-163">0x00000040</span></span> | <span data-ttu-id="d4a9a-164">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-164">Yes</span></span>                | <span data-ttu-id="d4a9a-165">Infraestrutura e operações do provedor de hardware do VSS.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-165">VSS hardware provider infrastructure and operations.</span></span>                                                                                          |
| <span data-ttu-id="d4a9a-166">ADMIN</span><span class="sxs-lookup"><span data-stu-id="d4a9a-166">ADMIN</span></span>  | <span data-ttu-id="d4a9a-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d4a9a-167">0x00000080</span></span> | <span data-ttu-id="d4a9a-168">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-168">Yes</span></span>                | <span data-ttu-id="d4a9a-169">Utilitários de linha de comando do VSS, como VSSADMIN.EXE e DISKSHADOW.EXE.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-169">VSS command line utilities such as VSSADMIN.EXE and DISKSHADOW.EXE.</span></span>                                                                           |
| <span data-ttu-id="d4a9a-170">VSSUI</span><span class="sxs-lookup"><span data-stu-id="d4a9a-170">VSSUI</span></span>  | <span data-ttu-id="d4a9a-171">0x00000100</span><span class="sxs-lookup"><span data-stu-id="d4a9a-171">0x00000100</span></span> | <span data-ttu-id="d4a9a-172">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-172">Yes</span></span>                | <span data-ttu-id="d4a9a-173">A interface do usuário de configuração do Cópias de Sombra para Pastas Compartilhadas (UI).</span><span class="sxs-lookup"><span data-stu-id="d4a9a-173">The Shadow Copies for Shared Folders configuration user interface (UI).</span></span> <span data-ttu-id="d4a9a-174">A interface do usuário está disponível apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-174">The UI is available only on Windows Server operating systems.</span></span>         |
| <span data-ttu-id="d4a9a-175">TEST</span><span class="sxs-lookup"><span data-stu-id="d4a9a-175">TEST</span></span>   | <span data-ttu-id="d4a9a-176">0x00000200</span><span class="sxs-lookup"><span data-stu-id="d4a9a-176">0x00000200</span></span> | <span data-ttu-id="d4a9a-177">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-177">Yes</span></span>                | <span data-ttu-id="d4a9a-178">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-178">Not applicable.</span></span> <span data-ttu-id="d4a9a-179">(Este módulo de rastreamento está reservado.)</span><span class="sxs-lookup"><span data-stu-id="d4a9a-179">(This tracing module is reserved.)</span></span>                                                                                            |
| <span data-ttu-id="d4a9a-180">IOCTL</span><span class="sxs-lookup"><span data-stu-id="d4a9a-180">IOCTL</span></span>  | <span data-ttu-id="d4a9a-181">0x00000400</span><span class="sxs-lookup"><span data-stu-id="d4a9a-181">0x00000400</span></span> | <span data-ttu-id="d4a9a-182">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-182">Yes</span></span>                | <span data-ttu-id="d4a9a-183">Detalhes das operações FSCTL e IOCTL que o serviço VSS iniciou chamando a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="d4a9a-183">Details of FSCTL and IOCTL operations that the VSS service has initiated by calling the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span> |
| <span data-ttu-id="d4a9a-184">GERAL</span><span class="sxs-lookup"><span data-stu-id="d4a9a-184">GEN</span></span>    | <span data-ttu-id="d4a9a-185">0x00000800</span><span class="sxs-lookup"><span data-stu-id="d4a9a-185">0x00000800</span></span> | <span data-ttu-id="d4a9a-186">Sim</span><span class="sxs-lookup"><span data-stu-id="d4a9a-186">Yes</span></span>                | <span data-ttu-id="d4a9a-187">Funções gerais do utilitário VSS, como alocadores, classes de cadeia de caracteres e operações de registro e volume.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-187">General VSS utility functions, such as allocators, string classes, and registry and volume operations.</span></span>                                        |
| <span data-ttu-id="d4a9a-188">WRXML</span><span class="sxs-lookup"><span data-stu-id="d4a9a-188">WRXML</span></span>  | <span data-ttu-id="d4a9a-189">0x00001000</span><span class="sxs-lookup"><span data-stu-id="d4a9a-189">0x00001000</span></span> | <span data-ttu-id="d4a9a-190">Não</span><span class="sxs-lookup"><span data-stu-id="d4a9a-190">No</span></span>                 | <span data-ttu-id="d4a9a-191">Processamento de XML para metadados do gravador.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-191">XML processing for writer metadata.</span></span> <span data-ttu-id="d4a9a-192">Este módulo tem um nível muito alto de ruído.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-192">This module has a very high level of noise.</span></span>                                                               |
| <span data-ttu-id="d4a9a-193">VSSXML</span><span class="sxs-lookup"><span data-stu-id="d4a9a-193">VSSXML</span></span> | <span data-ttu-id="d4a9a-194">0x00002000</span><span class="sxs-lookup"><span data-stu-id="d4a9a-194">0x00002000</span></span> | <span data-ttu-id="d4a9a-195">Não</span><span class="sxs-lookup"><span data-stu-id="d4a9a-195">No</span></span>                 | <span data-ttu-id="d4a9a-196">Classes base de processamento XML.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-196">XML processing base classes.</span></span> <span data-ttu-id="d4a9a-197">Este módulo tem um nível muito alto de ruído.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-197">This module has a very high level of noise.</span></span>                                                                      |



 

</dd> <dt>

<span data-ttu-id="d4a9a-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Modulo_</span><span class="sxs-lookup"><span data-stu-id="d4a9a-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-199">Habilite o módulo especificado pelo *módulo*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-199">Enable the module specified by *Module*.</span></span> <span data-ttu-id="d4a9a-200">Mais de um módulo pode ser habilitado por vez.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-200">More than one module can be enabled at a time.</span></span> <span data-ttu-id="d4a9a-201">Para listar os módulos disponíveis, digite **vsstrace – módulos de ajuda** no prompt de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-201">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Modulo_</span><span class="sxs-lookup"><span data-stu-id="d4a9a-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-203">Desabilite o módulo especificado pelo *módulo*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-203">Disable the module specified by *Module*.</span></span> <span data-ttu-id="d4a9a-204">Para listar os módulos disponíveis, digite **vsstrace – módulos de ajuda** no prompt de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-204">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ pid** *ProcessId*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-206">Habilite o processo especificado por *ProcessId*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-206">Enable the process specified by *ProcessId*.</span></span> <span data-ttu-id="d4a9a-207">Para habilitar todos os processos, use " \* " para o valor de *ProcessId*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-207">To enable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="d4a9a-208">Mais de uma opção de **pid** pode ser especificada de cada vez.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-208">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="d4a9a-209">A ordem das opções determina quais processos estão habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-209">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="d4a9a-210">Por exemplo, para habilitar apenas o processo cujo identificador de processo é 0xe8c, use **vsstrace-PID \* + pid 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-210">For example, to enable only the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-212">Desabilite o processo especificado por *ProcessId*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-212">Disable the process specified by *ProcessId*.</span></span> <span data-ttu-id="d4a9a-213">Para desabilitar todos os processos, use " \* " para o valor de *ProcessId*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-213">To disable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="d4a9a-214">Mais de uma opção de **pid** pode ser especificada de cada vez.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-214">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="d4a9a-215">A ordem das opções determina quais processos estão habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-215">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="d4a9a-216">Por exemplo, para desabilitar todos os processos, exceto o processo cujo identificador de processo é 0xe8c, use **vsstrace-PID \* + pid 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-216">For example, to disable all processes except the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ tid** *ThreadID*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-218">Habilite o thread especificado por *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-218">Enable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="d4a9a-219">Para habilitar todos os threads, use " \* " para o valor de *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-219">To enable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="d4a9a-220">Mais de uma opção de **tid** pode ser especificada de cada vez.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-220">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="d4a9a-221">A ordem das opções determina quais threads estão habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-221">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="d4a9a-222">Por exemplo, para habilitar apenas o thread cujo identificador de processo é 0x31a, use **vsstrace-tid \* + tid 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-222">For example, to enable only the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadID*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-224">Desabilite o thread especificado por *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-224">Disable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="d4a9a-225">Para desabilitar todos os threads, use " \* " para o valor de *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-225">To disable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="d4a9a-226">Mais de uma opção de **tid** pode ser especificada de cada vez.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-226">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="d4a9a-227">A ordem das opções determina quais threads estão habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-227">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="d4a9a-228">Por exemplo, para desabilitar todos os threads, exceto o thread cujo identificador de processo é 0x31a, use **vsstrace-tid \* + tid 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-228">For example, to disable all threads except the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *nível*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Level*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-230">Use o nível de rastreamento especificado por *nível*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-230">Use the tracing level specified by *Level*.</span></span> <span data-ttu-id="d4a9a-231">Quanto mais alto o nível, mais detalhada será a saída de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-231">The higher the level, the more verbose the trace output.</span></span> <span data-ttu-id="d4a9a-232">Cada nível inclui todos os níveis inferiores.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-232">Each level includes all of the lower levels.</span></span> <span data-ttu-id="d4a9a-233">O nível padrão é 170.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-233">The default level is 170.</span></span> <span data-ttu-id="d4a9a-234">Os níveis a seguir estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-234">The following levels are available.</span></span>



| <span data-ttu-id="d4a9a-235">Nível</span><span class="sxs-lookup"><span data-stu-id="d4a9a-235">Level</span></span> | <span data-ttu-id="d4a9a-236">Informações incluídas na saída do rastreamento</span><span class="sxs-lookup"><span data-stu-id="d4a9a-236">Information included in the trace output</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d4a9a-237">000</span><span class="sxs-lookup"><span data-stu-id="d4a9a-237">000</span></span>   | <span data-ttu-id="d4a9a-238">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d4a9a-238">None</span></span>                                     |
| <span data-ttu-id="d4a9a-239">020</span><span class="sxs-lookup"><span data-stu-id="d4a9a-239">020</span></span>   | <span data-ttu-id="d4a9a-240">Erros fatais</span><span class="sxs-lookup"><span data-stu-id="d4a9a-240">Fatal errors</span></span>                             |
| <span data-ttu-id="d4a9a-241">030</span><span class="sxs-lookup"><span data-stu-id="d4a9a-241">030</span></span>   | <span data-ttu-id="d4a9a-242">Exceções sem tratamento</span><span class="sxs-lookup"><span data-stu-id="d4a9a-242">Unhandled exceptions</span></span>                     |
| <span data-ttu-id="d4a9a-243">040</span><span class="sxs-lookup"><span data-stu-id="d4a9a-243">040</span></span>   | <span data-ttu-id="d4a9a-244">Errors</span><span class="sxs-lookup"><span data-stu-id="d4a9a-244">Errors</span></span>                                   |
| <span data-ttu-id="d4a9a-245">050</span><span class="sxs-lookup"><span data-stu-id="d4a9a-245">050</span></span>   | <span data-ttu-id="d4a9a-246">Asserções</span><span class="sxs-lookup"><span data-stu-id="d4a9a-246">Assertions</span></span>                               |
| <span data-ttu-id="d4a9a-247">060</span><span class="sxs-lookup"><span data-stu-id="d4a9a-247">060</span></span>   | <span data-ttu-id="d4a9a-248">Warnings</span><span class="sxs-lookup"><span data-stu-id="d4a9a-248">Warnings</span></span>                                 |
| <span data-ttu-id="d4a9a-249">080</span><span class="sxs-lookup"><span data-stu-id="d4a9a-249">080</span></span>   | <span data-ttu-id="d4a9a-250">Tratamento de exceções</span><span class="sxs-lookup"><span data-stu-id="d4a9a-250">Exception handling</span></span>                       |
| <span data-ttu-id="d4a9a-251">100</span><span class="sxs-lookup"><span data-stu-id="d4a9a-251">100</span></span>   | <span data-ttu-id="d4a9a-252">Atividade de log de eventos</span><span class="sxs-lookup"><span data-stu-id="d4a9a-252">Event Log activity</span></span>                       |
| <span data-ttu-id="d4a9a-253">120</span><span class="sxs-lookup"><span data-stu-id="d4a9a-253">120</span></span>   | <span data-ttu-id="d4a9a-254">Informações gerais</span><span class="sxs-lookup"><span data-stu-id="d4a9a-254">General information</span></span>                      |
| <span data-ttu-id="d4a9a-255">140</span><span class="sxs-lookup"><span data-stu-id="d4a9a-255">140</span></span>   | <span data-ttu-id="d4a9a-256">fluxo de código</span><span class="sxs-lookup"><span data-stu-id="d4a9a-256">Code flow</span></span>                                |
| <span data-ttu-id="d4a9a-257">160</span><span class="sxs-lookup"><span data-stu-id="d4a9a-257">160</span></span>   | <span data-ttu-id="d4a9a-258">Função Enter e Exit</span><span class="sxs-lookup"><span data-stu-id="d4a9a-258">Function enter and exit</span></span>                  |
| <span data-ttu-id="d4a9a-259">170</span><span class="sxs-lookup"><span data-stu-id="d4a9a-259">170</span></span>   | <span data-ttu-id="d4a9a-260">Valores de retorno de função</span><span class="sxs-lookup"><span data-stu-id="d4a9a-260">Function return values</span></span>                   |
| <span data-ttu-id="d4a9a-261">180</span><span class="sxs-lookup"><span data-stu-id="d4a9a-261">180</span></span>   | <span data-ttu-id="d4a9a-262">Parâmetros de função (conciso)</span><span class="sxs-lookup"><span data-stu-id="d4a9a-262">Function parameters (terse)</span></span>              |
| <span data-ttu-id="d4a9a-263">190</span><span class="sxs-lookup"><span data-stu-id="d4a9a-263">190</span></span>   | <span data-ttu-id="d4a9a-264">Parâmetros de função (detalhado)</span><span class="sxs-lookup"><span data-stu-id="d4a9a-264">Function parameters (verbose)</span></span>            |
| <span data-ttu-id="d4a9a-265">200</span><span class="sxs-lookup"><span data-stu-id="d4a9a-265">200</span></span>   | <span data-ttu-id="d4a9a-266">Nível de informações detalhadas 1</span><span class="sxs-lookup"><span data-stu-id="d4a9a-266">Verbose information level 1</span></span>              |
| <span data-ttu-id="d4a9a-267">210</span><span class="sxs-lookup"><span data-stu-id="d4a9a-267">210</span></span>   | <span data-ttu-id="d4a9a-268">Nível de informações detalhadas 2</span><span class="sxs-lookup"><span data-stu-id="d4a9a-268">Verbose information level 2</span></span>              |
| <span data-ttu-id="d4a9a-269">220</span><span class="sxs-lookup"><span data-stu-id="d4a9a-269">220</span></span>   | <span data-ttu-id="d4a9a-270">Nível de Informação Detalhado 3</span><span class="sxs-lookup"><span data-stu-id="d4a9a-270">Verbose information level 3</span></span>              |
| <span data-ttu-id="d4a9a-271">230</span><span class="sxs-lookup"><span data-stu-id="d4a9a-271">230</span></span>   | <span data-ttu-id="d4a9a-272">Nível de código rápido 1</span><span class="sxs-lookup"><span data-stu-id="d4a9a-272">Fast Code Level 1</span></span>                        |
| <span data-ttu-id="d4a9a-273">240</span><span class="sxs-lookup"><span data-stu-id="d4a9a-273">240</span></span>   | <span data-ttu-id="d4a9a-274">Nível de código rápido 2</span><span class="sxs-lookup"><span data-stu-id="d4a9a-274">Fast Code Level 2</span></span>                        |
| <span data-ttu-id="d4a9a-275">250</span><span class="sxs-lookup"><span data-stu-id="d4a9a-275">250</span></span>   | <span data-ttu-id="d4a9a-276">Nível de código rápido 3</span><span class="sxs-lookup"><span data-stu-id="d4a9a-276">Fast Code Level 3</span></span>                        |
| <span data-ttu-id="d4a9a-277">255</span><span class="sxs-lookup"><span data-stu-id="d4a9a-277">255</span></span>   | <span data-ttu-id="d4a9a-278">Todos</span><span class="sxs-lookup"><span data-stu-id="d4a9a-278">All</span></span>                                      |



 

</dd> <dt>

<span data-ttu-id="d4a9a-279"><span id="_indent"></span><span id="_INDENT"></span>**+ recuar**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-279"><span id="_indent"></span><span id="_INDENT"></span>**+indent**</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-280">Recue a saída de rastreamento formatada em cada função e limite de subfunção.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-280">Indent the formatted trace output at each function and subfunction boundary.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-281"><span id="-indent"></span><span id="-INDENT"></span>**-recuar**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-281"><span id="-indent"></span><span id="-INDENT"></span>**-indent**</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-282">Não recue a saída de rastreamento formatada.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-282">Do not indent the formatted trace output.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *EtlFile*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-284">Converta o arquivo de saída logman especificado por *EtlFile* em um formato de texto legível.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-284">Convert the Logman output file specified by *EtlFile* into a readable text format.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *arquivo_de_saída*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-286">Salve as informações de rastreamento no arquivo de saída especificado pelo *OutputFile*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-286">Save the tracing information to the output file specified by *OutputFile*.</span></span> <span data-ttu-id="d4a9a-287">Para obter o melhor desempenho, o arquivo de saída deve estar localizado em um volume que não faz parte da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-287">For best performance, the output file should be located on a volume that is not part of the shadow copy.</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-ajuda** *HelpOption*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*</span></span>
</dt> <dd>

<span data-ttu-id="d4a9a-289">Exiba a ajuda da linha de comando conforme especificado por *HelpOption*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-289">Display the command-line help as specified by *HelpOption*.</span></span> <span data-ttu-id="d4a9a-290">Os valores de *HelpOption* válidos são **módulos**, **níveis** e **todos**.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-290">The valid *HelpOption* values are **modules**, **levels**, and **all**.</span></span> <span data-ttu-id="d4a9a-291">A especificação de **módulos** faz com que os módulos sejam listados.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-291">Specifying **modules** causes the modules to be listed.</span></span> <span data-ttu-id="d4a9a-292">A especificação de **níveis** faz com que os níveis disponíveis sejam listados.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-292">Specifying **levels** causes the available levels to be listed.</span></span> <span data-ttu-id="d4a9a-293">Especificar **All** faz com que a ajuda detalhada seja exibida.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-293">Specifying **all** causes detailed help to be displayed.</span></span> <span data-ttu-id="d4a9a-294">Se nenhuma opção for usada, a ajuda concisa será exibida.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-294">If no options are used, concise help is displayed.</span></span>

</dd> </dl>

## <a name="using-logman"></a><span data-ttu-id="d4a9a-295">Usando logman</span><span class="sxs-lookup"><span data-stu-id="d4a9a-295">Using Logman</span></span>

<span data-ttu-id="d4a9a-296">O procedimento a seguir descreve como usar o logman com seu aplicativo VSS.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-296">The following procedure describes how to use Logman with your VSS application.</span></span>

<span data-ttu-id="d4a9a-297">**Para usar logman com seu aplicativo VSS**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-297">**To use Logman with your VSS application**</span></span>

1.  <span data-ttu-id="d4a9a-298">Use o seguinte comando para iniciar o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-298">Use the following command to start tracing:</span></span>

    <span data-ttu-id="d4a9a-299">**logman start VSS-o** *x: \\ \* \* \* VSS. etl-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xFFF 170*\*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-299">**logman start vss -o** *x:\\*\*\*vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="d4a9a-300">Substitua "x: \\ " pelo caminho para o diretório em que você deseja que o arquivo de log de rastreamento seja armazenado.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-300">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

2.  <span data-ttu-id="d4a9a-301">Use o seguinte comando para interromper o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-301">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="d4a9a-302">**logman parar VSS-ETS**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-302">**logman stop vss -ets**</span></span>

<span data-ttu-id="d4a9a-303">O arquivo de log de rastreamento é *x: \\* VSS. etl.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-303">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="d4a9a-304">Para obter mais informações sobre a ferramenta Logman, consulte [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="d4a9a-304">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="d4a9a-305">Usando tracelog</span><span class="sxs-lookup"><span data-stu-id="d4a9a-305">Using Tracelog</span></span>

<span data-ttu-id="d4a9a-306">O procedimento a seguir descreve como usar o tracelog.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-306">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="d4a9a-307">**Para usar o tracelog**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-307">**To use Tracelog**</span></span>

1.  <span data-ttu-id="d4a9a-308">Crie um arquivo de texto chamado VSS. CTL que contenha apenas o seguinte texto:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-308">Create a text file named vss.ctl that contains only the following text:</span></span>

    <span data-ttu-id="d4a9a-309">**VSS 9138500e-3648-4edb-aa4c-859e9f7b7c38**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**</span></span>

2.  <span data-ttu-id="d4a9a-310">Use o seguinte comando para iniciar o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-310">Use the following command to start tracing:</span></span>

    <span data-ttu-id="d4a9a-311">**tracelog-iniciar VSS-f** *x: \\ \* \* \* VSS. etl-GUID VSS. CTL-Flag 0xAA de nível 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-311">**tracelog -start vss -f** *x:\\*\*\*vss.etl -guid vss.ctl -flag 0xff -level 0xaa*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="d4a9a-312">Substitua "x: \\ " pelo caminho para o diretório em que você deseja que o arquivo de log de rastreamento seja armazenado.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-312">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

3.  <span data-ttu-id="d4a9a-313">Use o seguinte comando para interromper o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="d4a9a-313">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="d4a9a-314">**tracelog-parar VSS**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-314">**tracelog -stop vss**</span></span>

<span data-ttu-id="d4a9a-315">O arquivo de log de rastreamento é *x: \\* VSS. etl.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-315">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="d4a9a-316">Para obter mais informações sobre a ferramenta tracelog, consulte [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4a9a-316">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
