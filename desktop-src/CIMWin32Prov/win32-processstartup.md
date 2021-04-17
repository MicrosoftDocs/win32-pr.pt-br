---
description: A \_ classe WMI abstrata do Win32 ProcessStartup representa a configuração de inicialização de um processo baseado no Windows.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Classe Win32_ProcessStartup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187915"
---
# <a name="win32_processstartup-class"></a><span data-ttu-id="158ca-103">\_Classe Win32 ProcessStartup</span><span class="sxs-lookup"><span data-stu-id="158ca-103">Win32\_ProcessStartup class</span></span>

<span data-ttu-id="158ca-104">A [classe WMI](../wmisdk/retrieving-a-class.md) abstrata do **Win32 \_ ProcessStartup** representa a configuração de inicialização de um processo baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="158ca-104">The **Win32\_ProcessStartup** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the startup configuration of a Windows-based process.</span></span> <span data-ttu-id="158ca-105">A classe é definida como uma definição de tipo de método, o que significa que ela é usada apenas para passar informações para o método [**Create**](create-method-in-class-win32-process.md) da classe [**\_ process do Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="158ca-105">The class is defined as a method type definition, which means that it is only used for passing information to the [**Create**](create-method-in-class-win32-process.md) method of the [**Win32\_Process**](win32-process.md) class.</span></span>

<span data-ttu-id="158ca-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="158ca-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="158ca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="158ca-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a><span data-ttu-id="158ca-108">Membros</span><span class="sxs-lookup"><span data-stu-id="158ca-108">Members</span></span>

<span data-ttu-id="158ca-109">A classe **Win32 \_ ProcessStartup** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="158ca-109">The **Win32\_ProcessStartup** class has these types of members:</span></span>

-   [<span data-ttu-id="158ca-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="158ca-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="158ca-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="158ca-111">Properties</span></span>

<span data-ttu-id="158ca-112">A classe **Win32 \_ ProcessStartup** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="158ca-112">The **Win32\_ProcessStartup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="158ca-113">**CreateFlags**</span><span class="sxs-lookup"><span data-stu-id="158ca-113">**CreateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-116">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de processo e thread win32api \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags")</span><span class="sxs-lookup"><span data-stu-id="158ca-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)\|dwCreationFlags")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-117">Valores adicionais que controlam a classe de prioridade e a criação do processo.</span><span class="sxs-lookup"><span data-stu-id="158ca-117">Additional values that control the priority class and the creation of the process.</span></span> <span data-ttu-id="158ca-118">Os seguintes valores de criação podem ser especificados em qualquer combinação, exceto quando observado.</span><span class="sxs-lookup"><span data-stu-id="158ca-118">The following creation values can be specified in any combination, except as noted.</span></span>

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span data-ttu-id="158ca-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Depurar \_ Processo** (1)</span><span class="sxs-lookup"><span data-stu-id="158ca-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug\_Process** (1)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-120">Se esse sinalizador for definido, o processo de chamada será tratado como um depurador e o novo processo será depurado.</span><span class="sxs-lookup"><span data-stu-id="158ca-120">If this flag is set, the calling process is treated as a debugger, and the new process is being debugged.</span></span> <span data-ttu-id="158ca-121">O sistema notifica o depurador de todos os eventos de depuração que ocorrem no processo que está sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="158ca-121">The system notifies the debugger of all debug events that occur in the process being debugged.</span></span>

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span data-ttu-id="158ca-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Depurar \_ Somente \_ este \_ processo** (2)</span><span class="sxs-lookup"><span data-stu-id="158ca-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug\_Only\_This\_Process** (2)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-123">Se esse sinalizador não for definido e o processo de chamada estiver sendo depurado, o novo processo se tornará outro processo sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="158ca-123">If this flag is not set and the calling process is being debugged, the new process becomes another process being debugged.</span></span> <span data-ttu-id="158ca-124">Se o processo de chamada não for um processo de ser depurado, nenhuma ação relacionada à depuração ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="158ca-124">If the calling process is not a process of being debugged, no debugging-related actions occur.</span></span>

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span data-ttu-id="158ca-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Criar \_ Suspenso** (4)</span><span class="sxs-lookup"><span data-stu-id="158ca-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Create\_Suspended** (4)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-126">O thread principal do novo processo é criado em um estado suspenso e não é executado até que o método [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="158ca-126">The primary thread of the new process is created in a suspended state and does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) method is called.</span></span>

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span data-ttu-id="158ca-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>Desanexado **\_ Processo** (8)</span><span class="sxs-lookup"><span data-stu-id="158ca-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Detached\_Process** (8)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-128">Para processos de console, o novo processo não tem acesso ao console do processo pai.</span><span class="sxs-lookup"><span data-stu-id="158ca-128">For console processes, the new process does not have access to the console of the parent process.</span></span> <span data-ttu-id="158ca-129">Esse sinalizador não poderá ser usado se o sinalizador **criar \_ novo \_ console** estiver definido.</span><span class="sxs-lookup"><span data-stu-id="158ca-129">This flag cannot be used if the **Create\_New\_Console** flag is set.</span></span>

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span data-ttu-id="158ca-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Criar \_ Novo \_ console** (16)</span><span class="sxs-lookup"><span data-stu-id="158ca-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Create\_New\_Console** (16)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-131">Esse novo processo tem um novo console, em vez de herdar o console pai.</span><span class="sxs-lookup"><span data-stu-id="158ca-131">This new process has a new console, instead of inheriting the parent console.</span></span> <span data-ttu-id="158ca-132">Esse sinalizador não pode ser usado com o sinalizador de **\_ processo desanexado** .</span><span class="sxs-lookup"><span data-stu-id="158ca-132">This flag cannot be used with the **Detached\_Process** flag.</span></span>

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span data-ttu-id="158ca-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Criar \_ Novo \_ \_ grupo de processos** (512)</span><span class="sxs-lookup"><span data-stu-id="158ca-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Create\_New\_Process\_Group** (512)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-134">Esse novo processo é o processo raiz de um novo grupo de processos.</span><span class="sxs-lookup"><span data-stu-id="158ca-134">This new process is the root process of a new process group.</span></span> <span data-ttu-id="158ca-135">O grupo de processos inclui todos os processos que são descendentes desse processo raiz.</span><span class="sxs-lookup"><span data-stu-id="158ca-135">The process group includes all of the processes that are descendants of this root process.</span></span> <span data-ttu-id="158ca-136">O identificador de processo do novo grupo de processos é o mesmo que o identificador de processo retornado na propriedade **ProcessId** da classe [**\_ process do Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="158ca-136">The process identifier of the new process group is the same as the process identifier that is returned in the **ProcessID** property of the [**Win32\_Process**](win32-process.md) class.</span></span> <span data-ttu-id="158ca-137">Os grupos de processos são usados pelo método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) para habilitar o envio de um sinal CTRL + C ou um sinal CTRL + BREAK para um grupo de processos de console.</span><span class="sxs-lookup"><span data-stu-id="158ca-137">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable the sending of either a CTRL+C signal or a CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span data-ttu-id="158ca-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Criar \_ \_Ambiente Unicode** (1024)</span><span class="sxs-lookup"><span data-stu-id="158ca-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Create\_Unicode\_Environment** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-139">As configurações de ambiente listadas na propriedade **EnvironmentVariables** usam caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="158ca-139">The environment settings listed in the **EnvironmentVariables** property use Unicode characters.</span></span> <span data-ttu-id="158ca-140">Se esse sinalizador não for definido, o bloco de ambiente usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="158ca-140">If this flag is not set, the environment block uses ANSI characters.</span></span>

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span data-ttu-id="158ca-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Criar \_ \_ \_ Modo de erro padrão** (67108864)</span><span class="sxs-lookup"><span data-stu-id="158ca-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Create\_Default\_Error\_Mode** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-142">Processos recém-criados recebem o modo de erro padrão do sistema do processo de chamada em vez de herdar o modo de erro do processo pai.</span><span class="sxs-lookup"><span data-stu-id="158ca-142">Newly created processes are given the system default error mode of the calling process instead of inheriting the error mode of the parent process.</span></span> <span data-ttu-id="158ca-143">Esse sinalizador é útil para aplicativos de shell multithread que são executados com erros de hardware desabilitados.</span><span class="sxs-lookup"><span data-stu-id="158ca-143">This flag is useful for multithreaded shell applications that run with hard errors disabled.</span></span>

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span data-ttu-id="158ca-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Criar \_ BREAKAWAY \_ do \_ trabalho** (16777216)</span><span class="sxs-lookup"><span data-stu-id="158ca-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE\_BREAKAWAY\_FROM\_JOB** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-145">Usado para o processo criado não ser limitado pelo objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="158ca-145">Used for the created process not to be limited by the job object.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="158ca-146">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="158ca-146">**EnvironmentVariables**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-147">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="158ca-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="158ca-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-149">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ user \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="158ca-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_CURRENT\_USER\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-150">Lista de configurações para a configuração de um computador.</span><span class="sxs-lookup"><span data-stu-id="158ca-150">List of settings for the configuration of a computer.</span></span> <span data-ttu-id="158ca-151">Variáveis de ambiente especificam caminhos de pesquisa para arquivos, diretórios para arquivos temporários, opções específicas de aplicativo e outras informações semelhantes.</span><span class="sxs-lookup"><span data-stu-id="158ca-151">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="158ca-152">O sistema mantém um bloco de configurações de ambiente para cada usuário e um para o computador.</span><span class="sxs-lookup"><span data-stu-id="158ca-152">The system maintains a block of environment settings for each user and one for the computer.</span></span> <span data-ttu-id="158ca-153">O bloco de ambiente do sistema representa variáveis de ambiente para todos os usuários de um computador específico.</span><span class="sxs-lookup"><span data-stu-id="158ca-153">The system environment block represents environment variables for all of the users of a specific computer.</span></span> <span data-ttu-id="158ca-154">O bloco de ambiente de um usuário representa as variáveis de ambiente que o sistema mantém para um usuário específico e inclui o conjunto de variáveis de ambiente do sistema.</span><span class="sxs-lookup"><span data-stu-id="158ca-154">A user's environment block represents the environment variables that the system maintains for a specific user, and includes the set of system environment variables.</span></span> <span data-ttu-id="158ca-155">Por padrão, cada processo recebe uma cópia do bloco de ambiente para seu processo pai.</span><span class="sxs-lookup"><span data-stu-id="158ca-155">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="158ca-156">Normalmente, esse é o bloco de ambiente para o usuário que fez logon.</span><span class="sxs-lookup"><span data-stu-id="158ca-156">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="158ca-157">Um processo pode especificar diferentes blocos de ambiente para seus processos filhos.</span><span class="sxs-lookup"><span data-stu-id="158ca-157">A process can specify different environment blocks for its child processes.</span></span>

</dd> <dt>

<span data-ttu-id="158ca-158">**ErrorMode**</span><span class="sxs-lookup"><span data-stu-id="158ca-158">**ErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-159">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="158ca-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-161">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Error Functions \| SetError")</span><span class="sxs-lookup"><span data-stu-id="158ca-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Error Functions\|SetErrorMode")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-162">Em alguns processadores não x86, referências de memória desalinhadas causam uma exceção de falha de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="158ca-162">On some non-x86 processors, misaligned memory references cause an alignment fault exception.</span></span> <span data-ttu-id="158ca-163">O **sinalizador \_ sem \_ falhas \_ de alinhamento** permite que você controle se um sistema operacional corrige ou não automaticamente essas falhas de alinhamento ou as torna visíveis para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="158ca-163">The **No\_Alignment\_Fault\_Except** flag lets you control whether or not an operating system automatically fixes such alignment faults, or makes them visible to an application.</span></span> <span data-ttu-id="158ca-164">Em uma plataforma de milhões de instruções por segundo (MIPS), um aplicativo deve chamar explicitamente [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) com **a \_ falha sem alinhamento \_ \_ , exceto** o sinalizador, para que o sistema operacional corrija automaticamente as falhas de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="158ca-164">On a millions of instructions per second (MIPS) platform, an application must explicitly call [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) with the **No\_Alignment\_Fault\_Except** flag to have the operating system automatically fix alignment faults.</span></span>

<span data-ttu-id="158ca-165">Como um sistema operacional processa vários tipos de erros graves.</span><span class="sxs-lookup"><span data-stu-id="158ca-165">How an operating system processes several types of serious errors.</span></span> <span data-ttu-id="158ca-166">Você pode especificar que o sistema operacional tenha erros de processo ou que um aplicativo possa receber e processar erros.</span><span class="sxs-lookup"><span data-stu-id="158ca-166">You can specify that the operating system process errors, or an application can receive and process errors.</span></span>

<span data-ttu-id="158ca-167">A configuração padrão é para o sistema operacional tornar as falhas de alinhamento visíveis para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="158ca-167">The default setting is for the operating system to make alignment faults visible to an application.</span></span> <span data-ttu-id="158ca-168">Como a plataforma x86 não torna as falhas de alinhamento visíveis para um aplicativo, o **sinalizador \_ sem \_ falhas \_ de alinhamento** não faz com que o sistema operacional gere um erro de falha de alinhamento — mesmo que o sinalizador não esteja definido.</span><span class="sxs-lookup"><span data-stu-id="158ca-168">Because the x86 platform does not make alignment faults visible to an application, the **No\_Alignment\_Fault\_Except** flag does not make the operating system raise an alignment fault error—even if the flag is not set.</span></span> <span data-ttu-id="158ca-169">O estado padrão de [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) é definir todos os sinalizadores como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="158ca-169">The default state for [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) is to set all of the flags to 0 (zero).</span></span>

<dt>



 <span data-ttu-id="158ca-170">(1)</span><span class="sxs-lookup"><span data-stu-id="158ca-170">(1)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="158ca-171">Default</span></span>

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span data-ttu-id="158ca-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Falha \_ \_Erros críticos** (2)</span><span class="sxs-lookup"><span data-stu-id="158ca-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fail\_Critical\_Errors** (2)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-173">Se esse sinalizador for definido, o sistema operacional não exibirá a caixa de mensagem de identificador de erro crítico quando esse erro ocorrer.</span><span class="sxs-lookup"><span data-stu-id="158ca-173">If this flag is set, the operating system does not display the critical error handler message box when such an error occurs.</span></span> <span data-ttu-id="158ca-174">Em vez disso, o sistema operacional envia o erro para o processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="158ca-174">Instead, the operating system sends the error to the calling process.</span></span>

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span data-ttu-id="158ca-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Não \_ Falha de alinhamento \_ \_ , exceto** (4)</span><span class="sxs-lookup"><span data-stu-id="158ca-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No\_Alignment\_Fault\_Except** (4)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-176">Se esse sinalizador for definido, o sistema operacional corrigirá automaticamente as falhas de alinhamento de memória e as tornará invisíveis para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="158ca-176">If this flag is set, the operating system automatically fixes memory alignment faults and makes them invisible to the application.</span></span> <span data-ttu-id="158ca-177">Ele faz isso para os processos de chamada e descendentes.</span><span class="sxs-lookup"><span data-stu-id="158ca-177">It does this for the calling and descendant processes.</span></span> <span data-ttu-id="158ca-178">Esse sinalizador se aplica somente ao RISC (computação de conjunto de instruções) e não tem nenhum efeito sobre os processadores x86.</span><span class="sxs-lookup"><span data-stu-id="158ca-178">This flag applies to reduced instruction set computing (RISC) only, and has no effect on x86 processors.</span></span>

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span data-ttu-id="158ca-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Não \_ \_Caixa de \_ erro \_ de falha de GP** (8)</span><span class="sxs-lookup"><span data-stu-id="158ca-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No\_GP\_Fault\_Error\_Box** (8)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-180">Se esse sinalizador for definido, o sistema operacional não exibirá a caixa de mensagem de falha de proteção geral (GP) quando ocorrer um erro GP.</span><span class="sxs-lookup"><span data-stu-id="158ca-180">If this flag is set, the operating system does not display the general protection (GP) fault message box when a GP error occurs.</span></span> <span data-ttu-id="158ca-181">Esse sinalizador só deve ser definido pela depuração de aplicativos que lidam com erros de GP.</span><span class="sxs-lookup"><span data-stu-id="158ca-181">This flag should only be set by debugging applications that handle GP errors.</span></span>

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span data-ttu-id="158ca-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Não \_ \_Caixa de \_ erro \_ Abrir arquivo** (16)</span><span class="sxs-lookup"><span data-stu-id="158ca-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No\_Open\_File\_Error\_Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-183">Se esse sinalizador for definido, o sistema operacional não exibirá uma caixa de mensagem quando falhar em localizar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="158ca-183">If this flag is set, the operating system does not display a message box when it fails to find a file.</span></span> <span data-ttu-id="158ca-184">Em vez disso, o erro é retornado para o processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="158ca-184">Instead, the error is returned to the calling process.</span></span> <span data-ttu-id="158ca-185">Esse sinalizador é ignorado no momento.</span><span class="sxs-lookup"><span data-stu-id="158ca-185">This flag is currently ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="158ca-186">**Fillattribute**</span><span class="sxs-lookup"><span data-stu-id="158ca-186">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-187">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-188">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-189">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")</span><span class="sxs-lookup"><span data-stu-id="158ca-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwFillAttribute")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-190">As cores do texto e do plano de fundo se uma nova janela do console for criada em um aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="158ca-190">The text and background colors if a new console window is created in a console application.</span></span> <span data-ttu-id="158ca-191">Esses valores são ignorados em aplicativos de GUI (interface gráfica do usuário).</span><span class="sxs-lookup"><span data-stu-id="158ca-191">These values are ignored in graphical user interface (GUI) applications.</span></span> <span data-ttu-id="158ca-192">Para especificar as cores de primeiro plano e de segundo plano, adicione os valores juntos.</span><span class="sxs-lookup"><span data-stu-id="158ca-192">To specify both foreground and background colors, add the values together.</span></span> <span data-ttu-id="158ca-193">Por exemplo, para ter o tipo vermelho (4) em um plano de fundo azul (16), defina Fillattribute como 20.</span><span class="sxs-lookup"><span data-stu-id="158ca-193">For example, to have red type (4) on a blue background (16), set the FillAttribute to 20.</span></span>

<dt>

<span data-ttu-id="158ca-194">1</span><span class="sxs-lookup"><span data-stu-id="158ca-194">1</span></span>
</dt> <dd>

<span data-ttu-id="158ca-195">Azul em primeiro plano \_</span><span class="sxs-lookup"><span data-stu-id="158ca-195">Foreground\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="158ca-196">2</span><span class="sxs-lookup"><span data-stu-id="158ca-196">2</span></span>
</dt> <dd>

<span data-ttu-id="158ca-197">Primeiro plano \_ verde</span><span class="sxs-lookup"><span data-stu-id="158ca-197">Foreground\_Green</span></span>

</dd> <dt>

<span data-ttu-id="158ca-198">4</span><span class="sxs-lookup"><span data-stu-id="158ca-198">4</span></span>
</dt> <dd>

<span data-ttu-id="158ca-199">Vermelho em primeiro plano \_</span><span class="sxs-lookup"><span data-stu-id="158ca-199">Foreground\_Red</span></span>

</dd> <dt>

<span data-ttu-id="158ca-200">8</span><span class="sxs-lookup"><span data-stu-id="158ca-200">8</span></span>
</dt> <dd>

<span data-ttu-id="158ca-201">Intensidade do primeiro plano \_</span><span class="sxs-lookup"><span data-stu-id="158ca-201">Foreground\_Intensity</span></span>

</dd> <dt>

<span data-ttu-id="158ca-202">16</span><span class="sxs-lookup"><span data-stu-id="158ca-202">16</span></span>
</dt> <dd>

<span data-ttu-id="158ca-203">Azul em segundo plano \_</span><span class="sxs-lookup"><span data-stu-id="158ca-203">Background\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="158ca-204">32</span><span class="sxs-lookup"><span data-stu-id="158ca-204">32</span></span>
</dt> <dd>

<span data-ttu-id="158ca-205">Plano de fundo \_ verde</span><span class="sxs-lookup"><span data-stu-id="158ca-205">Background\_Green</span></span>

</dd> <dt>

<span data-ttu-id="158ca-206">64</span><span class="sxs-lookup"><span data-stu-id="158ca-206">64</span></span>
</dt> <dd>

<span data-ttu-id="158ca-207">Vermelho em segundo plano \_</span><span class="sxs-lookup"><span data-stu-id="158ca-207">Background\_Red</span></span>

</dd> <dt>

<span data-ttu-id="158ca-208">128</span><span class="sxs-lookup"><span data-stu-id="158ca-208">128</span></span>
</dt> <dd>

<span data-ttu-id="158ca-209">Intensidade do plano de fundo \_</span><span class="sxs-lookup"><span data-stu-id="158ca-209">Background\_Intensity</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="158ca-210">**PriorityClass**</span><span class="sxs-lookup"><span data-stu-id="158ca-210">**PriorityClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-211">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-212">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-212">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-213">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de processo e thread de win32api \| [**JOBOBJECT \_ \_ \_ informações básicas de limite**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")</span><span class="sxs-lookup"><span data-stu-id="158ca-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information)\|PriorityClass")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-214">Classe de prioridade do novo processo.</span><span class="sxs-lookup"><span data-stu-id="158ca-214">Priority class of the new process.</span></span> <span data-ttu-id="158ca-215">Use essa propriedade para determinar as prioridades de agendamento dos threads no processo.</span><span class="sxs-lookup"><span data-stu-id="158ca-215">Use this property to determine the schedule priorities of the threads in the process.</span></span> <span data-ttu-id="158ca-216">Se a propriedade for deixada como nula, a classe de prioridade padrão será normal — a menos que a classe de prioridade do processo de criação esteja ociosa ou abaixo do \_ normal.</span><span class="sxs-lookup"><span data-stu-id="158ca-216">If the property is left null, the priority class defaults to Normal—unless the priority class of the creating process is Idle or Below\_Normal.</span></span> <span data-ttu-id="158ca-217">Nesses casos, o processo filho recebe a classe de prioridade padrão do processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="158ca-217">In these cases, the child process receives the default priority class of the calling process.</span></span>

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="158ca-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="158ca-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-219">Indica um processo normal sem necessidade de agendamento especial.</span><span class="sxs-lookup"><span data-stu-id="158ca-219">Indicates a normal process with no special schedule needs.</span></span>

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="158ca-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Ocioso** (64)</span><span class="sxs-lookup"><span data-stu-id="158ca-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-221">Indica um processo com threads que são executados somente quando o sistema está ocioso e são preempçãos pelos threads de qualquer processo em execução em uma classe de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="158ca-221">Indicates a process with threads that run only when the system is idle and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="158ca-222">Um exemplo é uma proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="158ca-222">An example is a screen saver.</span></span> <span data-ttu-id="158ca-223">A classe de prioridade ociosa é herdada por processos filho.</span><span class="sxs-lookup"><span data-stu-id="158ca-223">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="158ca-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (128)</span><span class="sxs-lookup"><span data-stu-id="158ca-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (128)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-225">Indica um processo que executa tarefas de tempo crítico que devem ser executadas imediatamente para serem executadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="158ca-225">Indicates a process that performs time-critical tasks that must be executed immediately to run correctly.</span></span> <span data-ttu-id="158ca-226">Os threads de um processo de classe de alta prioridade apropriam os threads de processos de classe de prioridade normal ou de prioridade ociosa.</span><span class="sxs-lookup"><span data-stu-id="158ca-226">The threads of a high-priority class process preempt the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="158ca-227">Um exemplo é o Windows Lista de Tarefas, que deve responder rapidamente quando chamado pelo usuário, independentemente da carga no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="158ca-227">An example is Windows Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="158ca-228">Use extrema atenção ao usar a classe de alta prioridade, porque um aplicativo associado à CPU de classe de alta prioridade pode usar quase todos os ciclos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="158ca-228">Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all of the available cycles.</span></span> <span data-ttu-id="158ca-229">Somente uma prioridade em tempo real apropria os threads definidos para esse nível.</span><span class="sxs-lookup"><span data-stu-id="158ca-229">Only a real-time priority preempts threads set to this level.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="158ca-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo real** (256)</span><span class="sxs-lookup"><span data-stu-id="158ca-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-231">Indica um processo que tem a maior prioridade possível.</span><span class="sxs-lookup"><span data-stu-id="158ca-231">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="158ca-232">Os threads de um processo de classe de prioridade em tempo real apropriam os threads de todos os outros processos, incluindo threads de alta prioridade e processos do sistema operacional executando tarefas importantes.</span><span class="sxs-lookup"><span data-stu-id="158ca-232">The threads of a real-time priority class process preempt the threads of all other processes—including high-priority threads and operating system processes performing important tasks.</span></span> <span data-ttu-id="158ca-233">Por exemplo, um processo em tempo real que é executado por mais de um intervalo muito curto pode fazer com que os caches de disco não sejam liberados ou fazer com que um mouse não responda.</span><span class="sxs-lookup"><span data-stu-id="158ca-233">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush, or cause a mouse to be unresponsive.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="158ca-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Abaixo \_ Normal** (16384)</span><span class="sxs-lookup"><span data-stu-id="158ca-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below\_Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-235">Indica um processo que tem uma prioridade maior que o valor ocioso, mas menor do que o normal.</span><span class="sxs-lookup"><span data-stu-id="158ca-235">Indicates a process that has a priority higher than Idle but lower than Normal.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="158ca-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Acima \_ Normal** (32768)</span><span class="sxs-lookup"><span data-stu-id="158ca-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above\_Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="158ca-237">Indica um processo que tem uma prioridade maior que o normal, mas inferior a alta.</span><span class="sxs-lookup"><span data-stu-id="158ca-237">Indicates a process that has a priority higher than Normal but lower than High.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="158ca-238">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="158ca-238">**ShowWindow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-239">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="158ca-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-240">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-240">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-241">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")</span><span class="sxs-lookup"><span data-stu-id="158ca-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|wShowWindow")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-242">Como a janela é exibida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="158ca-242">How the window is displayed to the user.</span></span> <span data-ttu-id="158ca-243">Pode ser qualquer um dos valores que podem ser especificados no parâmetro *nCmdShow* para a função de [janela](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="158ca-243">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="158ca-244">**Título**</span><span class="sxs-lookup"><span data-stu-id="158ca-244">**Title**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-245">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="158ca-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-246">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-246">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-247">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")</span><span class="sxs-lookup"><span data-stu-id="158ca-247">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpTitle")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-248">Texto exibido na barra de título quando uma nova janela de console é criada; usado para processos de console.</span><span class="sxs-lookup"><span data-stu-id="158ca-248">Text displayed in the title bar when a new console window is created; used for console processes.</span></span> <span data-ttu-id="158ca-249">Se for **NULL**, o nome do arquivo executável será usado como o título da janela.</span><span class="sxs-lookup"><span data-stu-id="158ca-249">If **NULL**, the name of the executable file is used as the window title.</span></span> <span data-ttu-id="158ca-250">Essa propriedade deve ser **nula** para processos de GUI ou console que não criem uma nova janela de console.</span><span class="sxs-lookup"><span data-stu-id="158ca-250">This property must be **NULL** for GUI or console processes that do not create a new console window.</span></span>

</dd> <dt>

<span data-ttu-id="158ca-251">**WinstationDesktop**</span><span class="sxs-lookup"><span data-stu-id="158ca-251">**WinstationDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="158ca-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-253">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-254">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")</span><span class="sxs-lookup"><span data-stu-id="158ca-254">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpDesktop")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-255">O nome da área de trabalho ou o nome da estação de trabalho e do Windows para o processo.</span><span class="sxs-lookup"><span data-stu-id="158ca-255">The name of the desktop or the name of both the desktop and window station for the process.</span></span> <span data-ttu-id="158ca-256">Uma barra invertida na cadeia de caracteres indica que a cadeia de caracteres inclui nomes de estações de trabalho e de janelas.</span><span class="sxs-lookup"><span data-stu-id="158ca-256">A backslash in the string indicates that the string includes both desktop and window station names.</span></span> <span data-ttu-id="158ca-257">Se **WinstationDesktop** for **nulo**, o novo processo herdará a área de trabalho e a estação de janela de seu processo pai.</span><span class="sxs-lookup"><span data-stu-id="158ca-257">If **WinstationDesktop** is **NULL**, the new process inherits the desktop and window station of its parent process.</span></span> <span data-ttu-id="158ca-258">Se **WinstationDesktop** for uma cadeia de caracteres vazia, o processo não herdará a área de trabalho e a estação de janela do processo pai.</span><span class="sxs-lookup"><span data-stu-id="158ca-258">If **WinstationDesktop** is an empty string, the process does not inherit the desktop and window station of its parent process.</span></span> <span data-ttu-id="158ca-259">O sistema determina se um novo desktop e estação de janela devem ser criados.</span><span class="sxs-lookup"><span data-stu-id="158ca-259">The system determines if a new desktop and window station must be created.</span></span> <span data-ttu-id="158ca-260">Uma estação de janela é um objeto seguro que contém uma área de transferência, um conjunto de átomos globais e um grupo de objetos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="158ca-260">A window station is a secure object that contains a clipboard, a set of global atoms, and a group of desktop objects.</span></span> <span data-ttu-id="158ca-261">A estação de janela interativa que é atribuída à sessão de logon do usuário interativo também contém o teclado, o mouse e o dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="158ca-261">The interactive window station that is assigned to the logon session of the interactive user also contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="158ca-262">Uma área de trabalho é um objeto seguro contido em uma estação de janela.</span><span class="sxs-lookup"><span data-stu-id="158ca-262">A desktop is a secure object contained within a window station.</span></span> <span data-ttu-id="158ca-263">Uma área de trabalho tem uma superfície de exibição lógica e contém janelas, menus e ganchos.</span><span class="sxs-lookup"><span data-stu-id="158ca-263">A desktop has a logical display surface and contains windows, menus, and hooks.</span></span> <span data-ttu-id="158ca-264">Uma estação de janela pode ter várias áreas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="158ca-264">A window station can have multiple desktops.</span></span> <span data-ttu-id="158ca-265">Somente as áreas de trabalho da estação de janela interativa podem ser visíveis e receber entradas do usuário.</span><span class="sxs-lookup"><span data-stu-id="158ca-265">Only the desktops of the interactive window station can be visible and receive user input.</span></span>

</dd> <dt>

<span data-ttu-id="158ca-266">**X**</span><span class="sxs-lookup"><span data-stu-id="158ca-266">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-267">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-268">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-269">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX")</span><span class="sxs-lookup"><span data-stu-id="158ca-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwX")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-270">O deslocamento X do canto superior esquerdo de uma janela se uma nova janela for criada — em pixels.</span><span class="sxs-lookup"><span data-stu-id="158ca-270">The X offset of the upper left corner of a window if a new window is created—in pixels.</span></span> <span data-ttu-id="158ca-271">Os deslocamentos são do canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="158ca-271">The offsets are from the upper left corner of the screen.</span></span> <span data-ttu-id="158ca-272">Para processos de GUI, a posição especificada é usada na primeira vez que o novo processo chama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela sobreposta se o parâmetro *X* de **CreateWindow** for **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="158ca-272">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *X* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="158ca-273">\[! Observação X\]</span><span class="sxs-lookup"><span data-stu-id="158ca-273">\[!Note  X\]</span></span>  
> <span data-ttu-id="158ca-274">e **Y** não pode ser especificado de forma independente.</span><span class="sxs-lookup"><span data-stu-id="158ca-274">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="158ca-275">**XCountChars**</span><span class="sxs-lookup"><span data-stu-id="158ca-275">**XCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-276">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-276">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-277">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-277">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-278">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")</span><span class="sxs-lookup"><span data-stu-id="158ca-278">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|XCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-279">Largura do buffer de tela em colunas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="158ca-279">Screen buffer width in character columns.</span></span> <span data-ttu-id="158ca-280">Essa propriedade é usada para processos que criam uma janela de console e é ignorada em processos de GUI.</span><span class="sxs-lookup"><span data-stu-id="158ca-280">This property is used for processes that create a console window, and is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="158ca-281">**XCountChars** e **YCountChars** não podem ser especificados de forma independente.</span><span class="sxs-lookup"><span data-stu-id="158ca-281">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="158ca-282">**XSize**</span><span class="sxs-lookup"><span data-stu-id="158ca-282">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-283">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-284">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-284">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-285">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")</span><span class="sxs-lookup"><span data-stu-id="158ca-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwXSize")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-286">Largura de pixel de uma janela se uma nova janela for criada.</span><span class="sxs-lookup"><span data-stu-id="158ca-286">Pixel width of a window if a new window is created.</span></span> <span data-ttu-id="158ca-287">Para processos de GUI, isso é usado apenas na primeira vez que o novo processo chama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela sobreposta se o parâmetro NWidth de **CreateWindow** for **\_ USEDEFAULT de peso variável**.</span><span class="sxs-lookup"><span data-stu-id="158ca-287">For GUI processes, this is only used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the nWidth parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="158ca-288">**XSize** e **YSize** não podem ser especificados de forma independente.</span><span class="sxs-lookup"><span data-stu-id="158ca-288">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="158ca-289">**S**</span><span class="sxs-lookup"><span data-stu-id="158ca-289">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-290">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-291">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-291">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-292">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwY")</span><span class="sxs-lookup"><span data-stu-id="158ca-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwY")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-293">Deslocamento de pixel do canto superior esquerdo de uma janela se uma nova janela for criada.</span><span class="sxs-lookup"><span data-stu-id="158ca-293">Pixel offset of the upper-left corner of a window if a new window is created.</span></span> <span data-ttu-id="158ca-294">Os deslocamentos são do canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="158ca-294">The offsets are from the upper-left corner of the screen.</span></span> <span data-ttu-id="158ca-295">Para processos de GUI, a posição especificada é usada na primeira vez que o novo processo chama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela sobreposta se o parâmetro *y* de **CreateWindow** for **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="158ca-295">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *y* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="158ca-296">\[! Observação X\]</span><span class="sxs-lookup"><span data-stu-id="158ca-296">\[!Note  X\]</span></span>  
> <span data-ttu-id="158ca-297">e **Y** não pode ser especificado de forma independente.</span><span class="sxs-lookup"><span data-stu-id="158ca-297">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="158ca-298">**YCountChars**</span><span class="sxs-lookup"><span data-stu-id="158ca-298">**YCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-299">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-300">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-301">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")</span><span class="sxs-lookup"><span data-stu-id="158ca-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|YCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-302">Altura do buffer de tela em linhas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="158ca-302">Screen buffer height in character rows.</span></span> <span data-ttu-id="158ca-303">Essa propriedade é usada para processos que criam uma janela de console, mas são ignoradas em processos de GUI.</span><span class="sxs-lookup"><span data-stu-id="158ca-303">This property is used for processes that create a console window, but is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="158ca-304">**XCountChars** e **YCountChars** não podem ser especificados de forma independente.</span><span class="sxs-lookup"><span data-stu-id="158ca-304">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="158ca-305">**YSize**</span><span class="sxs-lookup"><span data-stu-id="158ca-305">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158ca-306">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="158ca-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="158ca-307">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="158ca-307">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="158ca-308">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")</span><span class="sxs-lookup"><span data-stu-id="158ca-308">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwYSize")</span></span>
</dt> </dl>

<span data-ttu-id="158ca-309">Altura de pixel de uma janela se uma nova janela for criada.</span><span class="sxs-lookup"><span data-stu-id="158ca-309">Pixel height of a window if a new window is created.</span></span> <span data-ttu-id="158ca-310">Para processos de GUI, isso é usado apenas na primeira vez que o novo processo chama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela sobreposta se o parâmetro *nWidth* de **CreateWindow** for **\_ USEDEFAULT de peso variável**.</span><span class="sxs-lookup"><span data-stu-id="158ca-310">For GUI processes, this is used only the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *nWidth* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="158ca-311">**XSize** e **YSize** não podem ser especificados de forma independente.</span><span class="sxs-lookup"><span data-stu-id="158ca-311">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="158ca-312">Comentários</span><span class="sxs-lookup"><span data-stu-id="158ca-312">Remarks</span></span>

<span data-ttu-id="158ca-313">Essa classe é derivada do [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md).</span><span class="sxs-lookup"><span data-stu-id="158ca-313">This class is derived from [**Win32\_MethodParameterClass**](win32-methodparameterclass.md).</span></span>

<span data-ttu-id="158ca-314">Visão geral</span><span class="sxs-lookup"><span data-stu-id="158ca-314">Overview</span></span>

<span data-ttu-id="158ca-315">O método [**Create**](create-method-in-class-win32-process.md) do [**\_ processo do Win32**](win32-process.md) permite configurar opções de inicialização para qualquer processo novo em execução em um computador.</span><span class="sxs-lookup"><span data-stu-id="158ca-315">The [**Win32\_Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) method enables you to configure startup options for any new process running on a computer.</span></span> <span data-ttu-id="158ca-316">Por exemplo, você pode configurar um processo para que ele seja iniciado em uma janela "oculta", o que impede que um usuário veja e, possivelmente, interrompa-o.</span><span class="sxs-lookup"><span data-stu-id="158ca-316">For example, you can configure a process so that it starts in a "hidden" window, which prevents a user from seeing, and possibly interrupting, it.</span></span> <span data-ttu-id="158ca-317">Se o processo for executado em uma janela de comando, você poderá configurar o tamanho, o título e as cores de primeiro plano e de plano de fundo da janela.</span><span class="sxs-lookup"><span data-stu-id="158ca-317">If the process runs in a command window, you can configure the size, title, and foreground and background colors of the window.</span></span>

<span data-ttu-id="158ca-318">As opções de inicialização são configuradas usando a classe **Win32 \_ ProcessStartup** .</span><span class="sxs-lookup"><span data-stu-id="158ca-318">Startup options are configured using the **Win32\_ProcessStartup** class.</span></span> <span data-ttu-id="158ca-319">**Win32 \_ ProcessStartup** é uma classe de tipo de método; a classe de tipo de método existe apenas para passar informações para um método.</span><span class="sxs-lookup"><span data-stu-id="158ca-319">**Win32\_ProcessStartup** is a Method Type class; the Method Type class exists solely to pass information to a method.</span></span> <span data-ttu-id="158ca-320">Nesse caso, todas as propriedades de uma instância do **Win32 \_ ProcessStartup** são passadas para uma instância do [**\_ processo Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="158ca-320">In this case, all the properties of an instance of **Win32\_ProcessStartup** are passed to an instance of [**Win32\_Process**](win32-process.md).</span></span>

<span data-ttu-id="158ca-321">**Usando o Win32 \_ ProcessStartup**</span><span class="sxs-lookup"><span data-stu-id="158ca-321">**Using Win32\_ProcessStartup**</span></span>

1.  <span data-ttu-id="158ca-322">Crie uma instância do **Win32 \_ ProcessStartup**.</span><span class="sxs-lookup"><span data-stu-id="158ca-322">Create an instance of **Win32\_ProcessStartup**.</span></span>
2.  <span data-ttu-id="158ca-323">Configure as propriedades da nova instância.</span><span class="sxs-lookup"><span data-stu-id="158ca-323">Configure the properties of the new instance.</span></span>
3.  <span data-ttu-id="158ca-324">Inclua a instância como parte do método de criação do [**\_ processo Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="158ca-324">Include the instance as part of the [**Win32\_Process**](win32-process.md) Create method.</span></span>

<span data-ttu-id="158ca-325">Por exemplo, se você tiver criado uma instância do **Win32 \_ ProcessStartup** chamada objConfig, passaria o nome do objeto no método Create da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="158ca-325">For example, if you have created a **Win32\_ProcessStartup** instance named objConfig, you would pass the object name in the Create method as follows:</span></span>

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a><span data-ttu-id="158ca-326">Exemplos</span><span class="sxs-lookup"><span data-stu-id="158ca-326">Examples</span></span>

<span data-ttu-id="158ca-327">Você pode usar a classe **Win32 \_ ProcessStartup** para configurar várias opções de inicialização para um processo.</span><span class="sxs-lookup"><span data-stu-id="158ca-327">You can use the **Win32\_ProcessStartup** class to configure various startup options for a process.</span></span> <span data-ttu-id="158ca-328">Essas opções incluem, mas não se limitam a, como criar um processo em uma janela oculta e criar um processo de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="158ca-328">These options include, but are not limited to, such things as creating a process in a hidden window and creating a higher-priority process.</span></span> <span data-ttu-id="158ca-329">O VBScript a seguir cria um processo em uma janela oculta.</span><span class="sxs-lookup"><span data-stu-id="158ca-329">The following VBScript creates a process in a hidden window.</span></span>


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



<span data-ttu-id="158ca-330">O VBScript a seguir cria um processo de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="158ca-330">The following VBScript creates a higher-priority process.</span></span>


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



<span data-ttu-id="158ca-331">O exemplo de código VBScript a seguir cria um processo do bloco de notas no computador local.</span><span class="sxs-lookup"><span data-stu-id="158ca-331">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="158ca-332">**Win32 \_ ProcessStartup** é usado para definir as configurações do processo.</span><span class="sxs-lookup"><span data-stu-id="158ca-332">**Win32\_ProcessStartup** is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="158ca-333">Requisitos</span><span class="sxs-lookup"><span data-stu-id="158ca-333">Requirements</span></span>



| <span data-ttu-id="158ca-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="158ca-334">Requirement</span></span> | <span data-ttu-id="158ca-335">Valor</span><span class="sxs-lookup"><span data-stu-id="158ca-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="158ca-336">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="158ca-336">Minimum supported client</span></span><br/> | <span data-ttu-id="158ca-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="158ca-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="158ca-338">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="158ca-338">Minimum supported server</span></span><br/> | <span data-ttu-id="158ca-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="158ca-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="158ca-340">Namespace</span><span class="sxs-lookup"><span data-stu-id="158ca-340">Namespace</span></span><br/>                | <span data-ttu-id="158ca-341">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="158ca-341">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="158ca-342">MOF</span><span class="sxs-lookup"><span data-stu-id="158ca-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="158ca-343"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="158ca-343"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="158ca-344">DLL</span><span class="sxs-lookup"><span data-stu-id="158ca-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="158ca-345"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="158ca-345"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="158ca-346">Confira também</span><span class="sxs-lookup"><span data-stu-id="158ca-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="158ca-347">**\_MethodParameterClass Win32**</span><span class="sxs-lookup"><span data-stu-id="158ca-347">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md)
</dt> <dt>

[<span data-ttu-id="158ca-348">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="158ca-348">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="158ca-349">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="158ca-349">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="158ca-350">**\_\_ProviderHostQuotaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="158ca-350">**\_\_ProviderHostQuotaConfiguration**</span></span>](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[<span data-ttu-id="158ca-351">Tarefas do WMI: processos</span><span class="sxs-lookup"><span data-stu-id="158ca-351">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
