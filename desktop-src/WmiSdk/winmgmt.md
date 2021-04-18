---
description: Winmgmt é o serviço WMI no processo SVCHOST em execução no &\# 0034; LocalSystem&\# 0034; conta.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: winmgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814054"
---
# <a name="winmgmt"></a><span data-ttu-id="f15a3-103">winmgmt</span><span class="sxs-lookup"><span data-stu-id="f15a3-103">winmgmt</span></span>

<span data-ttu-id="f15a3-104">Winmgmt é o serviço WMI dentro do processo do SVCHOST em execução na conta "LocalSystem".</span><span class="sxs-lookup"><span data-stu-id="f15a3-104">Winmgmt is the WMI service within the SVCHOST process running under the "LocalSystem" account.</span></span>

<span data-ttu-id="f15a3-105">Em todos os casos, o serviço WMI é iniciado automaticamente quando o primeiro aplicativo de gerenciamento ou script solicita conexão a um namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="f15a3-105">In all cases, the WMI service automatically starts when the first management application or script requests connection to a WMI namespace.</span></span> <span data-ttu-id="f15a3-106">Para obter mais informações, confira [Iniciar e interromper o serviço WMI](starting-and-stopping-the-wmi-service.md).</span><span class="sxs-lookup"><span data-stu-id="f15a3-106">For more information, see [Starting and Stopping the WMI Service](starting-and-stopping-the-wmi-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="f15a3-107">O WMI é um componente fundamental do sistema operacional Windows que permite que desenvolvedores e administradores de ti gravem scripts e aplicativos para automatizar determinadas tarefas.</span><span class="sxs-lookup"><span data-stu-id="f15a3-107">WMI is a core component of the Windows operating system that allows developers and IT administrators to write scripts and applications to automate certain tasks.</span></span> <span data-ttu-id="f15a3-108">Winmgmt.exe é o serviço que permite que o WMI seja executado em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="f15a3-108">Winmgmt.exe is the service that allows WMI to run on your local computer.</span></span> <span data-ttu-id="f15a3-109">Para obter mais informações sobre como usar o WMI, consulte [usando o WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f15a3-109">For more information on using WMI, see [Using WMI](using-wmi.md).</span></span> <span data-ttu-id="f15a3-110">Se você recebeu uma mensagem de erro referente a winmgmt.exe, consulte [solução de problemas de WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="f15a3-110">If you have received an error message regarding winmgmt.exe, see [WMI Troubleshooting](wmi-troubleshooting.md).</span></span> <span data-ttu-id="f15a3-111">Para obter mais informações sobre Winmgmt.exe, consulte [usando as ferramentas de gerenciamento do WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="f15a3-111">For more information on Winmgmt.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span>

 

<span data-ttu-id="f15a3-112">Quando executado no prompt de comando, o serviço WMI tem as seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="f15a3-112">When run from the command prompt, the WMI service has the following switches.</span></span>

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a><span data-ttu-id="f15a3-113">Comutadores</span><span class="sxs-lookup"><span data-stu-id="f15a3-113">Switches</span></span>

<dl> <dt>

<span data-ttu-id="f15a3-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>\**/backup\*\*\*<filename>*</span><span class="sxs-lookup"><span data-stu-id="f15a3-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span> **/backup** *<filename>*</span></span> 
</dt> <dd>

<span data-ttu-id="f15a3-115">Faz com que o WMI faça backup do repositório para o nome de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f15a3-115">Causes WMI to back up the repository to the specified file name.</span></span> <span data-ttu-id="f15a3-116">O argumento *filename* deve conter o caminho completo para o local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f15a3-116">The *filename* argument should contain the full path to the file location.</span></span> <span data-ttu-id="f15a3-117">Esse processo requer um bloqueio de gravação no repositório para que as operações de gravação no repositório sejam suspensas até que o processo de backup seja concluído.</span><span class="sxs-lookup"><span data-stu-id="f15a3-117">This process requires a write lock on the repository so that write operations to the repository are suspended until the backup process is completed.</span></span>

<span data-ttu-id="f15a3-118">Se você não especificar um caminho para o arquivo, ele será colocado no diretório% windir% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="f15a3-118">If you do not specify a path for the file, it is put in the %Windir%\\System32 directory.</span></span>

</dd> <dt>

<span data-ttu-id="f15a3-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/Restore** *<filename>\*\*<flag>*</span><span class="sxs-lookup"><span data-stu-id="f15a3-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span> **/restore** *<filename>* *<flag>*</span></span> 
</dt> <dd>

<span data-ttu-id="f15a3-120">Restaura manualmente o repositório WMI do arquivo de backup especificado.</span><span class="sxs-lookup"><span data-stu-id="f15a3-120">Manually restores the WMI repository from the specified backup file.</span></span> <span data-ttu-id="f15a3-121">O argumento *filename* deve conter o caminho completo para o local do arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="f15a3-121">The *filename* argument should contain the full path to the backup file location.</span></span> <span data-ttu-id="f15a3-122">Para executar a operação de restauração, o WMI salva o repositório existente para fazer write-back se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="f15a3-122">To perform the restore operation, WMI saves the existing repository to write back if the operation fails.</span></span> <span data-ttu-id="f15a3-123">Em seguida, o repositório é restaurado do arquivo de backup especificado no argumento *filename* .</span><span class="sxs-lookup"><span data-stu-id="f15a3-123">Then the repository is restored from the backup file that is specified in the *filename* argument.</span></span> <span data-ttu-id="f15a3-124">Se o acesso exclusivo ao repositório não puder ser obtido, os clientes existentes serão desconectados do WMI.</span><span class="sxs-lookup"><span data-stu-id="f15a3-124">If exclusive access to the repository cannot be achieved, existing clients are disconnected from WMI.</span></span>

<span data-ttu-id="f15a3-125">O argumento de *sinalizador* deve ser 1 (forçar a desconexão de usuários e restauração) ou 0 (restauração padrão, se nenhum usuário estiver conectado) e especificar o modo de restauração.</span><span class="sxs-lookup"><span data-stu-id="f15a3-125">The *flag* argument must be a 1 (force   disconnect users and restore) or 0 (default   restore if no users connected) and specifies the restore mode.</span></span>

</dd> <dt>

<span data-ttu-id="f15a3-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<winmgmt-Service-process-id>*</span><span class="sxs-lookup"><span data-stu-id="f15a3-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span> **/resyncperf** *<winmgmt-service-process-id>*</span></span> 
</dt> <dd>

<span data-ttu-id="f15a3-127">Registra as bibliotecas de desempenho do computador com o WMI.</span><span class="sxs-lookup"><span data-stu-id="f15a3-127">Registers the computer's performance libraries with WMI.</span></span> <span data-ttu-id="f15a3-128">A PID do WMI é a ID do processo do serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="f15a3-128">WMI PID is the process ID for the WMI service.</span></span>

<span data-ttu-id="f15a3-129">Necessário somente se as classes do monitor de desempenho não retornarem resultados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="f15a3-129">Only needed if the performance monitor classes are not returning reliable results.</span></span>

</dd> <dt>

<span data-ttu-id="f15a3-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]</span><span class="sxs-lookup"><span data-stu-id="f15a3-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[*<level>*\]</span></span>
</dt> <dd>

<span data-ttu-id="f15a3-131">Move o serviço Winmgmt para um processo autônomo do svchost que tem um ponto de extremidade DCOM fixo.</span><span class="sxs-lookup"><span data-stu-id="f15a3-131">Moves the Winmgmt service to a standalone Svchost process that has a fixed DCOM endpoint.</span></span> <span data-ttu-id="f15a3-132">O ponto de extremidade padrão é "ncacn \_ IP \_ TCP. 0.24158".</span><span class="sxs-lookup"><span data-stu-id="f15a3-132">The default endpoint is "ncacn\_ip\_tcp.0.24158".</span></span> <span data-ttu-id="f15a3-133">No entanto, o ponto de extremidade pode ser alterado executando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="f15a3-133">However, the endpoint may be changed by running Dcomcnfg.exe.</span></span> <span data-ttu-id="f15a3-134">Para obter mais informações sobre como configurar uma porta fixa para o WMI, consulte [Configurando uma porta fixa para o WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f15a3-134">For more information about setting up a fixed port for WMI, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="f15a3-135">O argumento de *nível* é o nível de autenticação para o processo Svchost.</span><span class="sxs-lookup"><span data-stu-id="f15a3-135">The *level* argument is the authentication level for the Svchost process.</span></span> <span data-ttu-id="f15a3-136">O WMI normalmente é executado como parte de um host de serviço compartilhado e você não pode aumentar o nível de autenticação somente para WMI.</span><span class="sxs-lookup"><span data-stu-id="f15a3-136">WMI normally runs as part of a shared service host and you cannot increase the authentication level for WMI alone.</span></span> <span data-ttu-id="f15a3-137">Se o *nível* não for especificado, o padrão será 4 (**RPC \_ C \_ Authn \_ nível \_ PKT** ou **WbemAuthenticationLevelPkt**).</span><span class="sxs-lookup"><span data-stu-id="f15a3-137">If *level* is not specified, the default is 4 (**RPC\_C\_AUTHN\_LEVEL\_PKT** or **WbemAuthenticationLevelPkt**).</span></span>

<span data-ttu-id="f15a3-138">Você pode executar o WMI com mais segurança, aumentando o nível de autenticação para privacidade de pacote (**privacidade do PCT no \_ nível de \_ autenticação RPC \_ \_ \_ C** ou **WbemAuthenticationLevelPktPrivacy**).</span><span class="sxs-lookup"><span data-stu-id="f15a3-138">You can run WMI more securely by increasing the authentication level to Packet Privacy (**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or **WbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="f15a3-139">Os níveis de autenticação para Visual Basic e script são descritos em [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="f15a3-139">The authentication levels for Visual Basic and scripting are described in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span> <span data-ttu-id="f15a3-140">Para C++, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="f15a3-140">For C++, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span> <span data-ttu-id="f15a3-141">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="f15a3-141">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="f15a3-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span><span class="sxs-lookup"><span data-stu-id="f15a3-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span></span>
</dt> <dd>

<span data-ttu-id="f15a3-143">Move o serviço Winmgmt para o processo compartilhado do svchost.</span><span class="sxs-lookup"><span data-stu-id="f15a3-143">Moves the Winmgmt service into the shared Svchost process.</span></span>

</dd> <dt>

<span data-ttu-id="f15a3-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>\**/verifyrepository\*\*\*<path>*</span><span class="sxs-lookup"><span data-stu-id="f15a3-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span> **/verifyrepository** *<path>*</span></span> 
</dt> <dd>

<span data-ttu-id="f15a3-145">Executa uma verificação de consistência no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="f15a3-145">Performs a consistency check on the WMI repository.</span></span> <span data-ttu-id="f15a3-146">Quando você adiciona a opção **/verifyrepository** sem o *<path>* argumento, o repositório ao vivo atualmente usado pelo WMI é verificado.</span><span class="sxs-lookup"><span data-stu-id="f15a3-146">When you add the **/verifyrepository** switch without the *<path>* argument, then the live repository currently used by WMI is verified.</span></span> <span data-ttu-id="f15a3-147">Ao especificar o argumento *path* , você pode verificar qualquer cópia salva do repositório.</span><span class="sxs-lookup"><span data-stu-id="f15a3-147">When you specify the *path* argument, you can verify any saved copy of the repository.</span></span> <span data-ttu-id="f15a3-148">Nesse caso, o argumento de caminho deve conter o caminho completo para a cópia de repositório salva.</span><span class="sxs-lookup"><span data-stu-id="f15a3-148">In this case, the path argument should contain the full path to the saved repository copy.</span></span> <span data-ttu-id="f15a3-149">O repositório salvo deve ser uma cópia de toda a pasta do repositório.</span><span class="sxs-lookup"><span data-stu-id="f15a3-149">The saved repository should be a copy of the entire repository folder.</span></span> <span data-ttu-id="f15a3-150">Para obter mais informações sobre os erros retornados por esse comando, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="f15a3-150">For more information about errors returned by this command, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="f15a3-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span><span class="sxs-lookup"><span data-stu-id="f15a3-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span></span>
</dt> <dd>

<span data-ttu-id="f15a3-152">Executa uma verificação de consistência no repositório do WMI e, se uma inconsistência for detectada, recria o repositório.</span><span class="sxs-lookup"><span data-stu-id="f15a3-152">Performs a consistency check on the WMI repository, and if an inconsistency is detected, rebuilds the repository.</span></span> <span data-ttu-id="f15a3-153">O conteúdo do repositório inconsistente é mesclado no repositório recriado, se ele puder ser lido.</span><span class="sxs-lookup"><span data-stu-id="f15a3-153">The content of the inconsistent repository is merged into the rebuilt repository, if it can be read.</span></span> <span data-ttu-id="f15a3-154">A operação Salvage sempre funciona com o repositório que o serviço WMI está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="f15a3-154">The salvage operation always works with the repository that the WMI service is currently using.</span></span> <span data-ttu-id="f15a3-155">Para obter mais informações sobre os erros retornados por esse comando, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="f15a3-155">For more information about errors returned by this command, see the Remarks section.</span></span>

<span data-ttu-id="f15a3-156">% Arquivos MOF que contêm a instrução de pré-processador de [**\# recuperação automática de pragma**](pragma-autorecover.md) são restaurados no repositório.</span><span class="sxs-lookup"><span data-stu-id="f15a3-156">% MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> <dt>

<span data-ttu-id="f15a3-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span><span class="sxs-lookup"><span data-stu-id="f15a3-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span></span>
</dt> <dd>

<span data-ttu-id="f15a3-158">O repositório é redefinido para o estado inicial quando o sistema operacional é instalado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="f15a3-158">The repository is reset to the initial state when the operating system is first installed.</span></span> <span data-ttu-id="f15a3-159">Os arquivos MOF que contêm a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) são restaurados no repositório.</span><span class="sxs-lookup"><span data-stu-id="f15a3-159">MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f15a3-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="f15a3-160">Remarks</span></span>

<span data-ttu-id="f15a3-161">Essa ferramenta está localizada no diretório% windir% \\ System32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="f15a3-161">This tool is located in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="f15a3-162">Para obter uma lista das opções disponíveis, digite `WinMgmt /?` no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="f15a3-162">For a list of the available switches, type `WinMgmt /?` at the command prompt.</span></span>

<span data-ttu-id="f15a3-163">O repositório WMI, também conhecido como repositório CIM, não é apenas um único arquivo, mas uma coleção de arquivos dentro da pasta de repositório que funciona em conjunto como um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f15a3-163">The WMI repository, also known as the CIM repository, is not just a single file, but a collection of files within the Repository folder that work together as a database.</span></span> <span data-ttu-id="f15a3-164">Quando você usa a opção **/backup** para fazer backup do repositório, o backup resultante é um arquivo compactado único.</span><span class="sxs-lookup"><span data-stu-id="f15a3-164">When you use the **/backup** switch to backup the repository, the resulting backup is a single compressed file.</span></span>

<span data-ttu-id="f15a3-165">O WMI retornará o **erro de erro \_ interno do \_ BD \_** (net helpmsg 1358) se uma operação de verificação indicar que o repositório não está em um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="f15a3-165">WMI returns the error **ERROR\_INTERNAL\_DB\_CORRUPTION** (net helpmsg 1358) if a verification operation indicates that the repository is not in a consistent state.</span></span> <span data-ttu-id="f15a3-166">Esse erro pode ser retornado de qualquer comando que executa a verificação do repositório, como **/verifyrepository** ou **/salvagerepository**.</span><span class="sxs-lookup"><span data-stu-id="f15a3-166">This error can be returned from any command which performs repository verification, such as **/verifyrepository** or **/salvagerepository**.</span></span>

> [!Note]
>
> <span data-ttu-id="f15a3-167">Se o WMI retornar mensagens de erro, lembre-se de que eles podem não indicar problemas no serviço WMI ou em provedores WMI.</span><span class="sxs-lookup"><span data-stu-id="f15a3-167">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="f15a3-168">As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI.</span><span class="sxs-lookup"><span data-stu-id="f15a3-168">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="f15a3-169">Em qualquer circunstância, não exclua o repositório WMI como uma primeira ação, pois a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.</span><span class="sxs-lookup"><span data-stu-id="f15a3-169">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="f15a3-170">Para obter mais informações sobre a origem do problema, baixe e execute a ferramenta de linha de comando de diagnóstico [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="f15a3-170">For more information about the source of the problem, download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="f15a3-171">Essa ferramenta produz um relatório que, em geral, pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo.</span><span class="sxs-lookup"><span data-stu-id="f15a3-171">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="f15a3-172">O relatório também ajuda os serviços de suporte da Microsoft para ajudá-lo.</span><span class="sxs-lookup"><span data-stu-id="f15a3-172">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="f15a3-173">Você pode baixar o [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="f15a3-173">You can download the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f15a3-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f15a3-174">Requirements</span></span>



| <span data-ttu-id="f15a3-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="f15a3-175">Requirement</span></span> | <span data-ttu-id="f15a3-176">Valor</span><span class="sxs-lookup"><span data-stu-id="f15a3-176">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f15a3-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f15a3-177">Minimum supported client</span></span><br/> | <span data-ttu-id="f15a3-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f15a3-178">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f15a3-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f15a3-179">Minimum supported server</span></span><br/> | <span data-ttu-id="f15a3-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f15a3-180">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f15a3-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="f15a3-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15a3-182">Solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="f15a3-182">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="f15a3-183">Conectando-se ao WMI remotamente a partir do vista</span><span class="sxs-lookup"><span data-stu-id="f15a3-183">Connecting to WMI Remotely Starting with Vista</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

