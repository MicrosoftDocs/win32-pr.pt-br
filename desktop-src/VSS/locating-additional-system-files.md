---
description: Ao executar um backup ou restauração do VSS, o estado do sistema do Windows é definido como sendo uma coleção de vários elementos principais do sistema operacional e seus arquivos. Esses elementos devem ser sempre tratados como uma unidade por operações de backup e restauração.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Fazendo backup e restaurando o estado do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661892"
---
# <a name="backing-up-and-restoring-system-state"></a><span data-ttu-id="a88b1-104">Fazendo backup e restaurando o estado do sistema</span><span class="sxs-lookup"><span data-stu-id="a88b1-104">Backing Up and Restoring System State</span></span>

> [!Note]  
> <span data-ttu-id="a88b1-105">Este tópico aplica-se ao Windows Vista, Windows Server 2008 e posterior.</span><span class="sxs-lookup"><span data-stu-id="a88b1-105">This topic applies to Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="a88b1-106">Para obter informações sobre o Windows Server 2003, consulte [fazendo backup e restaurando o estado do sistema no Windows server 2003 R2 e no Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span><span class="sxs-lookup"><span data-stu-id="a88b1-106">For information about Windows Server 2003, see [Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span></span>

 

<span data-ttu-id="a88b1-107">Ao executar um backup ou restauração do VSS, o estado do sistema do Windows é definido como sendo uma coleção de vários elementos principais do sistema operacional e seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="a88b1-107">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="a88b1-108">Esses elementos devem ser sempre tratados como uma unidade por operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="a88b1-108">These elements should always be treated as a unit by backup and restore operations.</span></span>

> [!Note]  
> <span data-ttu-id="a88b1-109">A Microsoft não fornece suporte técnico de desenvolvedor ou profissional de ti para implementar restaurações de estado do sistema online no Windows (todas as versões).</span><span class="sxs-lookup"><span data-stu-id="a88b1-109">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

 

<span data-ttu-id="a88b1-110">Durante o backup e a recuperação do estado do sistema, a estratégia recomendada é fazer backup e recuperar os volumes do sistema e de inicialização, além dos arquivos enumerados pelos gravadores do estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="a88b1-110">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span> <span data-ttu-id="a88b1-111">Os gravadores de estado do sistema são gravadores que têm o atributo de [**\_ \_ tipo de uso do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) definido como VSS \_ UT \_ BOOTABLESYSTEMSTATE ou VSS \_ UT \_ SYSTEMSERVICE.</span><span class="sxs-lookup"><span data-stu-id="a88b1-111">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a88b1-112">Se um gravador VSS for identificado por seu [**\_ \_ tipo de uso do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) como um gravador de estado do sistema, ele deverá ser incluído em um backup de estado do sistema, mesmo se ele for selecionável.</span><span class="sxs-lookup"><span data-stu-id="a88b1-112">If a VSS Writer is identified by its [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) as a system state writer it must be included in a system state backup even if it is selectable.</span></span>

 

<span data-ttu-id="a88b1-113">Além do sistema operacional enumerado e dos arquivos binários de driver que são enumerados pelos gravadores de estado do sistema, há alguns outros arquivos que devem ser submetidos a backup como parte do estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="a88b1-113">In addition to the enumerated operating system and driver binary files that are enumerated by the system state writers, there are certain other files that must be backed up as part of system state.</span></span>

<span data-ttu-id="a88b1-114">Todos os componentes relatados por um gravador de estado do sistema VSS fazem parte do estado do sistema, exceto aqueles para os quais o sinalizador de estado do sistema do CF do VSS \_ \_ não \_ \_ está definido.</span><span class="sxs-lookup"><span data-stu-id="a88b1-114">All the components reported by a VSS system state writer are part of system state except those for which the VSS\_CF\_NOT\_SYSTEM\_STATE flag is set.</span></span>

<span data-ttu-id="a88b1-115">Os programas de backup também devem definir a chave do registro **LastRestoreId** .</span><span class="sxs-lookup"><span data-stu-id="a88b1-115">Backup programs should also set the **LastRestoreId** registry key.</span></span> <span data-ttu-id="a88b1-116">Para obter mais informações, consulte [chaves e valores do registro para backup e restauração](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="a88b1-116">For more information, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

> [!Note]  
> <span data-ttu-id="a88b1-117">No Windows Vista, no Windows Server 2008 e posterior, os nomes e locais de alguns arquivos do sistema foram alterados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="a88b1-117">In Windows Vista, Windows Server 2008, and later, the names and locations of some system files have been changed as follows.</span></span>

 

## <a name="system-state"></a><span data-ttu-id="a88b1-118">Estado do Sistema</span><span class="sxs-lookup"><span data-stu-id="a88b1-118">System State</span></span>

<span data-ttu-id="a88b1-119">Para o Windows Server 2012 e posterior, além dos arquivos relatados pelos vários gravadores do estado do sistema VSS, somente os seguintes arquivos de licenciamento precisam ser incluídos explicitamente, e os seguintes arquivos DRM precisam ser excluídos explicitamente.</span><span class="sxs-lookup"><span data-stu-id="a88b1-119">For Windows Server 2012 and later, in addition to the files reported by the various VSS system-state writers, only the following licensing files need to be included explicitly, and the following DRM files need to be excluded explicitly.</span></span>

## <a name="windows-media-digital-rights-management-files"></a><span data-ttu-id="a88b1-120">Arquivos de Rights Management digital do Windows Media</span><span class="sxs-lookup"><span data-stu-id="a88b1-120">Windows Media Digital Rights Management Files</span></span>

<span data-ttu-id="a88b1-121">No Windows Server 2008 e posterior, os seguintes arquivos, incluindo todos os subdiretórios no caminho a seguir, são excluídos do estado do sistema e não devem ser submetidos a backup:</span><span class="sxs-lookup"><span data-stu-id="a88b1-121">In Windows Server 2008 and later, the following files, including all subdirectories under the following path, are excluded from system state and must not be backed up:</span></span>

-   <span data-ttu-id="a88b1-122">% ProgramData% \\ Microsoft \\ Windows \\ DRM</span><span class="sxs-lookup"><span data-stu-id="a88b1-122">%ProgramData%\\Microsoft\\Windows\\DRM</span></span>\\

<span data-ttu-id="a88b1-123">Isso substitui as informações na seção Rights Management digital do Windows Media do [trabalho com sistema de arquivos e recursos de segurança](working-with-file-system-and-security-features.md).</span><span class="sxs-lookup"><span data-stu-id="a88b1-123">This supersedes the information in the Windows Media Digital Rights Management section of [Working with File System and Security Features](working-with-file-system-and-security-features.md).</span></span>

## <a name="performance-counter-configuration-files"></a><span data-ttu-id="a88b1-124">Arquivos de configuração do contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="a88b1-124">Performance Counter Configuration Files</span></span>

<span data-ttu-id="a88b1-125">Os arquivos de configuração do contador de desempenho estão localizados no diretório% SystemRoot% \\ System32 \\ e têm os seguintes nomes:</span><span class="sxs-lookup"><span data-stu-id="a88b1-125">The performance counter configuration files are located in the %SystemRoot%\\System32\\ directory and have the following names:</span></span>

<dl> <span data-ttu-id="a88b1-126">Perf? 00?. DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-126">Perf?00?.dat</span></span>  
<span data-ttu-id="a88b1-127">??. Perfc0 DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-127">Perfc0??.dat</span></span>  
<span data-ttu-id="a88b1-128">??. Perfd0 DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-128">Perfd0??.dat</span></span>  
<span data-ttu-id="a88b1-129">??. Perfh0 DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-129">Perfh0??.dat</span></span>  
<span data-ttu-id="a88b1-130">??. Perfi0 DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-130">Perfi0??.dat</span></span>  
<span data-ttu-id="a88b1-131">???. Prfc0 DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-131">Prfc0???.dat</span></span>  
<span data-ttu-id="a88b1-132">???. Prfd0 DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-132">Prfd0???.dat</span></span>  
<span data-ttu-id="a88b1-133">???. Prfh0 DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-133">Prfh0???.dat</span></span>  
<span data-ttu-id="a88b1-134">???. Prfi0 DATs</span><span class="sxs-lookup"><span data-stu-id="a88b1-134">Prfi0???.dat</span></span>  
</dl>

<span data-ttu-id="a88b1-135">Esses arquivos são modificados apenas durante a instalação do aplicativo e devem ser armazenados em backup e restaurados durante as restaurações e backups de estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="a88b1-135">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

## <a name="iis-configuration-files"></a><span data-ttu-id="a88b1-136">Arquivos de configuração do IIS</span><span class="sxs-lookup"><span data-stu-id="a88b1-136">IIS Configuration Files</span></span>

> [!Note]  
> <span data-ttu-id="a88b1-137">No Windows Vista com Service Pack 1 (SP1) e posterior, você não deve fazer backup desses arquivos.</span><span class="sxs-lookup"><span data-stu-id="a88b1-137">In Windows Vista with Service Pack 1 (SP1) and later, you should not back up these files.</span></span> <span data-ttu-id="a88b1-138">Em vez disso, use o gravador de configuração do IIS in-box.</span><span class="sxs-lookup"><span data-stu-id="a88b1-138">Instead, use the in-box IIS configuration writer.</span></span> <span data-ttu-id="a88b1-139">Para obter mais informações sobre esse gravador, consulte [gravadores VSS in-box](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="a88b1-139">For more information about this writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

<span data-ttu-id="a88b1-140">Os arquivos de configuração relevantes do IIS e seus locais são listados abaixo:</span><span class="sxs-lookup"><span data-stu-id="a88b1-140">The relevant IIS configuration files and their locations are listed below:</span></span>

-   <span data-ttu-id="a88b1-141">O arquivo de machine.config do .NET FX está localizado no diretório da versão do Framework.</span><span class="sxs-lookup"><span data-stu-id="a88b1-141">The .NET FX machine.config file is located in the framework version directory.</span></span>
-   <span data-ttu-id="a88b1-142">O arquivo de web.config raiz ASP.NET está localizado no diretório da versão do Framework.</span><span class="sxs-lookup"><span data-stu-id="a88b1-142">The ASP.NET root web.config file is located in the framework version directory.</span></span>
    > [!Note]  
    > <span data-ttu-id="a88b1-143">Os arquivos de configuração para .NET FX e ASP.NET estão no diretório da versão do Framework.</span><span class="sxs-lookup"><span data-stu-id="a88b1-143">The configuration files for both .NET FX and ASP.NET are in the framework version directory.</span></span> <span data-ttu-id="a88b1-144">Se várias versões do Framework estiverem instaladas no computador, esse diretório conterá um arquivo de configuração para cada versão instalada.</span><span class="sxs-lookup"><span data-stu-id="a88b1-144">If multiple versions of the framework are installed on the computer, this directory will contain one configuration file for each installed version.</span></span>

     

-   <span data-ttu-id="a88b1-145">O arquivo de configuração central do IIS applicationHost.config está localizado no diretório% windir% \\ System32 \\ inetsrv \\ config.</span><span class="sxs-lookup"><span data-stu-id="a88b1-145">The IIS applicationHost.config central configuration file is located in the %windir%\\system32\\inetsrv\\config directory.</span></span> <span data-ttu-id="a88b1-146">Para que o servidor entenda esse arquivo de configuração, há arquivos de esquema que determinam sua gramática e estrutura.</span><span class="sxs-lookup"><span data-stu-id="a88b1-146">For the server to understand this configuration file, there are schema files that determine its grammar and structure.</span></span> <span data-ttu-id="a88b1-147">Esses arquivos estão localizados no diretório de esquema de configuração% windir% \\ System32 \\ inetsrv \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="a88b1-147">These files are located in the %windir%\\system32\\inetsrv\\config\\schema directory.</span></span>

<span data-ttu-id="a88b1-148">O caminho do diretório da versão do Framework é armazenado na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="a88b1-148">The framework version directory path is stored in the following registry key:</span></span>

<span data-ttu-id="a88b1-149">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ . NETFramework \\ InstallRoot**</span><span class="sxs-lookup"><span data-stu-id="a88b1-149">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\.NETFramework\\InstallRoot**</span></span>

<span data-ttu-id="a88b1-150">Além disso, deve ser feito o backup das seguintes chaves de criptografia:</span><span class="sxs-lookup"><span data-stu-id="a88b1-150">In addition, the following cryptography keys must be backed up:</span></span><dl> <span data-ttu-id="a88b1-151">% ProgramData% \\ Microsoft \\ crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="a88b1-151">%ProgramData%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span>  
<span data-ttu-id="a88b1-152">% SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="a88b1-152">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
</dl>

## <a name="framework-files"></a><span data-ttu-id="a88b1-153">Arquivos do Framework</span><span class="sxs-lookup"><span data-stu-id="a88b1-153">Framework Files</span></span>

<span data-ttu-id="a88b1-154">É necessário fazer backup de todas as versões do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a88b1-154">All versions of the .NET framework must be backed up.</span></span> <span data-ttu-id="a88b1-155">Os arquivos estão localizados em um ou nos dois diretórios a seguir:</span><span class="sxs-lookup"><span data-stu-id="a88b1-155">The files are located in one or both of the following directories:</span></span>

<dl> <span data-ttu-id="a88b1-156">% WINDIR% \\ Microsoft.NET \\ Framework</span><span class="sxs-lookup"><span data-stu-id="a88b1-156">%windir%\\Microsoft.Net\\Framework</span></span>  
<span data-ttu-id="a88b1-157">% WINDIR% \\ Microsoft.NET \\ Framework64</span><span class="sxs-lookup"><span data-stu-id="a88b1-157">%windir%\\Microsoft.Net\\Framework64</span></span>  
</dl>

<span data-ttu-id="a88b1-158">Além disso, o backup dos arquivos de assembly deve ser feito.</span><span class="sxs-lookup"><span data-stu-id="a88b1-158">In addition, the assembly files must be backed up.</span></span> <span data-ttu-id="a88b1-159">Esses arquivos estão localizados no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="a88b1-159">These files are located in the following directory:</span></span><dl> <span data-ttu-id="a88b1-160">assembly% windir% \\</span><span class="sxs-lookup"><span data-stu-id="a88b1-160">%windir%\\assembly</span></span>  
</dl>

## <a name="task-scheduler-task-files"></a><span data-ttu-id="a88b1-161">Agendador de Tarefas arquivos de tarefa</span><span class="sxs-lookup"><span data-stu-id="a88b1-161">Task Scheduler Task Files</span></span>

<span data-ttu-id="a88b1-162">É necessário fazer backup dos arquivos de tarefa do Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a88b1-162">The task scheduler's task files must be backed up.</span></span> <span data-ttu-id="a88b1-163">Os arquivos estão localizados em um ou nos dois locais a seguir:</span><span class="sxs-lookup"><span data-stu-id="a88b1-163">The files are located in one or both of the following locations:</span></span>

<dl> <span data-ttu-id="a88b1-164">tarefas% windir% \\ System32 \\ e quaisquer subdiretórios (recursivamente)</span><span class="sxs-lookup"><span data-stu-id="a88b1-164">%windir%\\system32\\tasks and any subdirectories (recursively)</span></span>  
<span data-ttu-id="a88b1-165">tarefas de% windir% \\ (sem subdiretórios)</span><span class="sxs-lookup"><span data-stu-id="a88b1-165">%windir%\\tasks (no subdirectories)</span></span>  
</dl>

 

 
