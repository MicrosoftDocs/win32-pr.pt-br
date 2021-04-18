---
description: O sistema operacional Windows inclui um conjunto de gravadores do VSS responsáveis por enumerar os dados exigidos por vários recursos do Windows. Eles são chamados de &\# 0034;&s in box \# 0034; gravadores.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: Gravadores do VSS In-Box
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763415"
---
# <a name="in-box-vss-writers"></a><span data-ttu-id="cb1ce-104">Gravadores do VSS In-Box</span><span class="sxs-lookup"><span data-stu-id="cb1ce-104">In-Box VSS Writers</span></span>

<span data-ttu-id="cb1ce-105">O sistema operacional Windows inclui um conjunto de gravadores do VSS responsáveis por enumerar os dados exigidos por vários recursos do Windows.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-105">The Windows operating system includes a set of VSS writers that are responsible for enumerating the data that is required by various Windows features.</span></span> <span data-ttu-id="cb1ce-106">Eles são chamados de gravadores "in-box".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-106">These are referred to as "in-box" writers.</span></span>

> [!Note]  
> <span data-ttu-id="cb1ce-107">O gravador in-box do MSDE não está disponível no Windows Vista, no Windows Server 2008 e posterior.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-107">The MSDE in-box writer is not available in Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="cb1ce-108">Em vez disso, o gravador do SQL deve ser usado para fazer backup de bancos de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-108">Instead, the SQL Writer should be used to back up SQL Server databases.</span></span> <span data-ttu-id="cb1ce-109">Somente SQL Server 2005 SP2 e posterior têm suporte no Windows Vista, no Windows Server 2008 e posterior.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-109">Only SQL Server 2005 SP2 and later are supported on Windows Vista, Windows Server 2008, and later.</span></span>

 

-   [<span data-ttu-id="cb1ce-110">Gravador VSS do Active Directory Domain Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-110">Active Directory Domain Services (NTDS) VSS Writer</span></span>](#active-directory-domain-services-ntds-vss-writer)
-   [<span data-ttu-id="cb1ce-111">Gravador de Serviços de Federação do Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-111">Active Directory Federation Services Writer</span></span>](#active-directory-federation-services-writer)
-   [<span data-ttu-id="cb1ce-112">Gravador VSS do serviços AD LDS (LDS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-112">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [<span data-ttu-id="cb1ce-113">Gravador de Active Directory Rights Management Services (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-113">Active Directory Rights Management Services (AD RMS) Writer</span></span>](#active-directory-rights-management-services-ad-rms-writer)
-   [<span data-ttu-id="cb1ce-114">Gravador ASR (recuperação automatizada do sistema)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-114">Automated System Recovery (ASR) Writer</span></span>](#automated-system-recovery-asr-writer)
-   [<span data-ttu-id="cb1ce-115">Gravador de Serviço de Transferência Inteligente em Segundo Plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-115">Background Intelligent Transfer Service (BITS) Writer</span></span>](#background-intelligent-transfer-service-bits-writer)
-   [<span data-ttu-id="cb1ce-116">Gravador de autoridade de certificação</span><span class="sxs-lookup"><span data-stu-id="cb1ce-116">Certificate Authority Writer</span></span>](#certificate-authority-writer)
-   [<span data-ttu-id="cb1ce-117">Gravador do serviço de cluster</span><span class="sxs-lookup"><span data-stu-id="cb1ce-117">Cluster Service Writer</span></span>](#cluster-service-writer)
-   [<span data-ttu-id="cb1ce-118">Gravador VSS de Volume Compartilhado Clusterizado (CSV)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-118">Cluster Shared Volume (CSV) VSS Writer</span></span>](#cluster-shared-volume-csv-vss-writer)
-   [<span data-ttu-id="cb1ce-119">Gravador de banco de dados de registro de classe COM+</span><span class="sxs-lookup"><span data-stu-id="cb1ce-119">COM+ Class Registration Database Writer</span></span>](#com-class-registration-database-writer)
-   [<span data-ttu-id="cb1ce-120">Gravador de eliminação de duplicação de dados</span><span class="sxs-lookup"><span data-stu-id="cb1ce-120">Data Deduplication Writer</span></span>](#data-deduplication-writer)
-   [<span data-ttu-id="cb1ce-121">Replicação de Sistema de Arquivos Distribuído (DFSR)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-121">Distributed File System Replication (DFSR)</span></span>](#distributed-file-system-replication-dfsr)
-   [<span data-ttu-id="cb1ce-122">Gravador DHCP (protocolo de configuração dinâmica de hosts)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-122">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>](#dynamic-host-configuration-protocol-dhcp-writer)
-   [<span data-ttu-id="cb1ce-123">FRS (Serviço de Replicação de Arquivos)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-123">File Replication Service (FRS)</span></span>](#file-replication-service-frs)
-   [<span data-ttu-id="cb1ce-124">Gravador FSRM (Gerenciador de recursos de servidor de arquivos)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-124">File Server Resource Manager (FSRM) Writer</span></span>](#file-server-resource-manager-fsrm-writer)
-   [<span data-ttu-id="cb1ce-125">Gravador do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="cb1ce-125">Hyper-V Writer</span></span>](#hyper-v-writer)
-   [<span data-ttu-id="cb1ce-126">Gravador de configuração do IIS</span><span class="sxs-lookup"><span data-stu-id="cb1ce-126">IIS Configuration Writer</span></span>](#iis-configuration-writer)
-   [<span data-ttu-id="cb1ce-127">Gravador de metabase do IIS</span><span class="sxs-lookup"><span data-stu-id="cb1ce-127">IIS Metabase Writer</span></span>](#iis-metabase-writer)
-   [<span data-ttu-id="cb1ce-128">Gravador MSMQ (enfileiramento de mensagens da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-128">Microsoft Message Queuing (MSMQ) Writer</span></span>](#microsoft-message-queuing-msmq-writer)
-   [<span data-ttu-id="cb1ce-129">Gravador de serviço MSSearch</span><span class="sxs-lookup"><span data-stu-id="cb1ce-129">MSSearch Service Writer</span></span>](#mssearch-service-writer)
-   [<span data-ttu-id="cb1ce-130">Gravador VSS do NPS</span><span class="sxs-lookup"><span data-stu-id="cb1ce-130">NPS VSS Writer</span></span>](#nps-vss-writer)
-   [<span data-ttu-id="cb1ce-131">Gravador de contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="cb1ce-131">Performance Counters Writer</span></span>](#performance-counters-writer)
-   [<span data-ttu-id="cb1ce-132">Gravador do registro</span><span class="sxs-lookup"><span data-stu-id="cb1ce-132">Registry Writer</span></span>](#registry-writer)
-   [<span data-ttu-id="cb1ce-133">Gravador VSS do gateway de Serviços de Área de Trabalho Remota (serviços de terminal)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-133">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [<span data-ttu-id="cb1ce-134">Gravador VSS de licenciamento do Serviços de Área de Trabalho Remota (serviços de terminal)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-134">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [<span data-ttu-id="cb1ce-135">Gravador de otimização de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cb1ce-135">Shadow Copy Optimization Writer</span></span>](#shadow-copy-optimization-writer)
-   [<span data-ttu-id="cb1ce-136">Gravador do serviço de compartilhamento de sincronização</span><span class="sxs-lookup"><span data-stu-id="cb1ce-136">Sync Share Service Writer</span></span>](#sync-share-service-writer)
-   [<span data-ttu-id="cb1ce-137">Gravador do sistema</span><span class="sxs-lookup"><span data-stu-id="cb1ce-137">System Writer</span></span>](#system-writer)
-   [<span data-ttu-id="cb1ce-138">Gravador de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cb1ce-138">Task Scheduler Writer</span></span>](#task-scheduler-writer)
-   [<span data-ttu-id="cb1ce-139">Gravador de repositório de metadados do VSS</span><span class="sxs-lookup"><span data-stu-id="cb1ce-139">VSS Metadata Store Writer</span></span>](#vss-metadata-store-writer)
-   [<span data-ttu-id="cb1ce-140">Gravador do WDS (serviços de implantação do Windows)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-140">Windows Deployment Services (WDS) Writer</span></span>](#windows-deployment-services-wds-writer)
-   [<span data-ttu-id="cb1ce-141">Gravador do banco de dados interno do Windows (WID)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-141">Windows Internal Database (WID) Writer</span></span>](#windows-internal-database-wid-writer)
-   [<span data-ttu-id="cb1ce-142">Gravador WINS (serviço de cadastramento na Internet do Windows)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-142">Windows Internet Name Service (WINS) Writer</span></span>](#windows-internet-name-service-wins-writer)
-   [<span data-ttu-id="cb1ce-143">Gravador WMI</span><span class="sxs-lookup"><span data-stu-id="cb1ce-143">WMI Writer</span></span>](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a><span data-ttu-id="cb1ce-144">Gravador VSS do Active Directory Domain Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-144">Active Directory Domain Services (NTDS) VSS Writer</span></span>

<span data-ttu-id="cb1ce-145">Esse gravador relata o arquivo de banco de dados NTDS (Ntds. dit) e os arquivos de log associados.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-145">This writer reports the NTDS database file (ntds.dit) and the associated log files.</span></span> <span data-ttu-id="cb1ce-146">Esses arquivos são necessários para restaurar o Active Directory corretamente.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-146">These files are required to restore the Active Directory correctly.</span></span>

<span data-ttu-id="cb1ce-147">Há apenas um arquivo NTDS. dit por controlador de domínio e é relatado nos metadados do gravador, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="cb1ce-147">There is only one ntds.dit file per domain controller, and it is reported in the writer metadata as in the following example:</span></span>

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

<span data-ttu-id="cb1ce-148">Aqui está um exemplo que mostra como listar os componentes nos metadados do gravador:</span><span class="sxs-lookup"><span data-stu-id="cb1ce-148">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="cb1ce-149">No momento do backup, o gravador define o tempo de expiração de backup nos metadados de backup do gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-149">At backup time, the writer sets the backup expiration time in the writer's backup metadata.</span></span> <span data-ttu-id="cb1ce-150">Os solicitantes devem recuperar esses metadados usando [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar se o banco de dados expirou.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-150">Requesters should retrieve this metadata by using [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) to determine whether the database has expired.</span></span> <span data-ttu-id="cb1ce-151">Bancos de dados expirados não podem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-151">Expired databases cannot be restored.</span></span>

<span data-ttu-id="cb1ce-152">Se o computador que contém o banco de dados NTDS for um controlador de domínio, o aplicativo de backup sempre deverá executar um backup de estado do sistema em todos os volumes que contenham informações críticas do estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-152">If the computer that contains the NTDS database is a domain controller, the backup application should always perform a system state backup across all volumes containing critical system state information.</span></span> <span data-ttu-id="cb1ce-153">No momento da restauração, o aplicativo deve primeiro reiniciar o computador em Modo de Restauração dos Serviços de Diretório e, em seguida, executar uma restauração de estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-153">At restore time, the application should first restart the computer in Directory Services Restore Mode and then perform a system state restore.</span></span>

<span data-ttu-id="cb1ce-154">A cadeia de caracteres do nome do gravador para esse gravador é "NTDS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-154">The writer name string for this writer is "NTDS".</span></span>

<span data-ttu-id="cb1ce-155">A ID do gravador para este gravador é B2014C9E-8711-4C5C-A5A9-3CF384484757.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-155">The writer ID for this writer is B2014C9E-8711-4C5C-A5A9-3CF384484757.</span></span>

## <a name="active-directory-federation-services-writer"></a><span data-ttu-id="cb1ce-156">Gravador de Serviços de Federação do Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-156">Active Directory Federation Services Writer</span></span>

<span data-ttu-id="cb1ce-157">Esse gravador relata os arquivos de dados do Serviços de Federação do Active Directory (AD FS) (ADFS).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-157">This writer reports the Active Directory Federation Services (ADFS) data files.</span></span>

<span data-ttu-id="cb1ce-158">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-158">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-159">A cadeia de caracteres do nome do gravador para esse gravador é "gravador VSS do ADFS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-159">The writer name string for this writer is "ADFS VSS Writer".</span></span>

<span data-ttu-id="cb1ce-160">A ID do gravador para este gravador é 772C45F8-AE01-4F94-940C-94961864ACAD.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-160">The writer ID for this writer is 772C45F8-AE01-4F94-940C-94961864ACAD.</span></span>

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a><span data-ttu-id="cb1ce-161">Gravador VSS do serviços AD LDS (LDS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-161">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>

<span data-ttu-id="cb1ce-162">Esse gravador relata o arquivo de banco de dados ADAM (Adamntds. dit) e os arquivos de log associados para cada instância em% Program Files% \\ Microsoft Adam \\ Instance *n* \\ data, em que *N* é o número da instância do Adam.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-162">This writer reports the ADAM database file (adamntds.dit) and the associated log files for each instance in %program files%\\Microsoft ADAM\\instance *N*\\data, where *N* is the ADAM instance number.</span></span> <span data-ttu-id="cb1ce-163">Esses arquivos de log de banco de dados são necessários para restaurar instâncias do ADAM.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-163">These database log files are required to restore ADAM instances.</span></span>

<span data-ttu-id="cb1ce-164">**Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-164">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-165">Aqui está um exemplo que mostra como listar os componentes nos metadados do gravador:</span><span class="sxs-lookup"><span data-stu-id="cb1ce-165">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="cb1ce-166">No momento do backup, o gravador define o tempo de expiração de backup nos metadados de backup.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-166">At backup time, the writer sets the backup expiration time in the backup metadata.</span></span> <span data-ttu-id="cb1ce-167">Os aplicativos de backup devem recuperar esses metadados usando o método [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar se o banco de dados expirou.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-167">Backup applications should retrieve this metadata by using the [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) method to determine whether the database has expired.</span></span> <span data-ttu-id="cb1ce-168">Bancos de dados expirados não podem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-168">Expired databases cannot be restored.</span></span>

<span data-ttu-id="cb1ce-169">A cadeia de caracteres do nome do gravador para esse gravador é "ADAM (Instance *N*) Writer", em que *N* é o número da instância do Adam, por exemplo, "Adam (instance1) Writer", "Adam (Instance2) Writer" e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-169">The writer name string for this writer is "ADAM (instance *N*) Writer", where *N* is the ADAM instance number, for example, "ADAM (instance1) Writer", "ADAM (instance2) Writer", and so on.</span></span>

<span data-ttu-id="cb1ce-170">A ID do gravador para este gravador é DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-170">The writer ID for this writer is DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span></span> <span data-ttu-id="cb1ce-171">Essa ID de gravador é a mesma para todas as instâncias.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-171">This writer ID is the same for all instances.</span></span>

## <a name="active-directory-rights-management-services-ad-rms-writer"></a><span data-ttu-id="cb1ce-172">Gravador de Active Directory Rights Management Services (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-172">Active Directory Rights Management Services (AD RMS) Writer</span></span>

<span data-ttu-id="cb1ce-173">Esse gravador relata os arquivos de dados do AD RMS (serviço de Active Directory Rights Management).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-173">This writer reports the Active Directory Rights Management Service (AD RMS) data files.</span></span>

<span data-ttu-id="cb1ce-174">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-174">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-175">A cadeia de caracteres do nome do gravador para este gravador é "gravador de AD RMS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-175">The writer name string for this writer is "AD RMS Writer".</span></span>

<span data-ttu-id="cb1ce-176">A ID do gravador para este gravador é 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-176">The writer ID for this writer is 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span></span>

## <a name="automated-system-recovery-asr-writer"></a><span data-ttu-id="cb1ce-177">Gravador ASR (recuperação automatizada do sistema)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-177">Automated System Recovery (ASR) Writer</span></span>

<span data-ttu-id="cb1ce-178">O gravador ASR armazena a configuração de discos no sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-178">The ASR writer stores the configuration of disks on the system.</span></span> <span data-ttu-id="cb1ce-179">Esse gravador relata o banco de dados de configuração de inicialização (BCD) e também é responsável por desmontar o hive do registro que representa o BCD durante a criação da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-179">This writer reports the Boot Configuration Database (BCD) and is also responsible for dismounting the registry hive that represents the BCD during shadow copy creation.</span></span> <span data-ttu-id="cb1ce-180">O gravador ASR deve ser incluído em todos os backups necessários para a recuperação bare-metal.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-180">The ASR writer must be included in any backups required for bare-metal recovery.</span></span> <span data-ttu-id="cb1ce-181">Para obter mais informações sobre o ASR, consulte [usando a recuperação automatizada do sistema VSS para recuperação de desastre](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-181">For more information about ASR, see [Using VSS Automated System Recovery for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span>

<span data-ttu-id="cb1ce-182">**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-182">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-183">A cadeia de caracteres do nome do gravador para este gravador é "gravador ASR".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-183">The writer name string for this writer is "ASR Writer".</span></span>

<span data-ttu-id="cb1ce-184">A ID do gravador para o gravador de ASR é BE000CBE-11FE-4426-9C58-531AA6355FC4.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-184">The writer ID for the ASR writer is BE000CBE-11FE-4426-9C58-531AA6355FC4.</span></span>

## <a name="background-intelligent-transfer-service-bits-writer"></a><span data-ttu-id="cb1ce-185">Gravador de Serviço de Transferência Inteligente em Segundo Plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-185">Background Intelligent Transfer Service (BITS) Writer</span></span>

<span data-ttu-id="cb1ce-186">O gravador BITS usa a chave do registro **FilesNotToBackup** para excluir arquivos da pasta de cache bits.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-186">The BITS writer uses the **FilesNotToBackup** registry key to exclude files from the BITS cache folder.</span></span> <span data-ttu-id="cb1ce-187">O local do cache padrão é% AllUsersProfile% \\ do cache do Microsoft \\ Network \\ Downloader \\ .</span><span class="sxs-lookup"><span data-stu-id="cb1ce-187">The default cache location is %AllUsersProfile%\\Microsoft\\Network\\Downloader\\Cache.</span></span>

<span data-ttu-id="cb1ce-188">**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-188">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-189">Além disso, o gravador BITS exclui os seguintes arquivos do backup: os arquivos de estado do BITS (Qmgr0. dat e Qmgr1. dat), o arquivo de log de depuração BITS e os arquivos parcialmente baixados do BITS.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-189">In addition, the BITS writer excludes the following files from backup: the BITS state files (qmgr0.dat and qmgr1.dat), the BITS debug log file, and BITS partially downloaded files.</span></span>

<span data-ttu-id="cb1ce-190">Se o arquivo de destino do download do BITS for um arquivo SMB, a conta do cliente deverá ter uma relação de confiança com o servidor ou os backups poderão falhar.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-190">If the BITS download destination file is an SMB file, the client account must have a trust relationship to the server, or else backups may fail.</span></span>

<span data-ttu-id="cb1ce-191">A cadeia de caracteres do nome do gravador para este gravador é "gravador BITS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-191">The writer name string for this writer is "BITS Writer".</span></span>

<span data-ttu-id="cb1ce-192">A ID do gravador para o gravador BITS é 4969D978-BE47-48B0-B100-F328F07AC1E0.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-192">The writer ID for the BITS writer is 4969D978-BE47-48B0-B100-F328F07AC1E0.</span></span>

## <a name="certificate-authority-writer"></a><span data-ttu-id="cb1ce-193">Gravador de autoridade de certificação</span><span class="sxs-lookup"><span data-stu-id="cb1ce-193">Certificate Authority Writer</span></span>

<span data-ttu-id="cb1ce-194">Esse gravador é responsável por enumerar os arquivos de dados para o servidor de certificado.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-194">This writer is responsible for enumerating the data files for the Certificate Server.</span></span>

<span data-ttu-id="cb1ce-195">A cadeia de caracteres do nome do gravador para esse gravador é "autoridade de certificação".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-195">The writer name string for this writer is "Certificate Authority".</span></span>

<span data-ttu-id="cb1ce-196">**Windows XP:** A cadeia de caracteres do nome do gravador para esse gravador é "gravador do servidor de certificado".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-196">**Windows XP:** The writer name string for this writer is "Certificate Server Writer".</span></span>

<span data-ttu-id="cb1ce-197">A ID do gravador para o gravador é 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-197">The writer ID for the writer is 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span></span>

## <a name="cluster-service-writer"></a><span data-ttu-id="cb1ce-198">Gravador do serviço de cluster</span><span class="sxs-lookup"><span data-stu-id="cb1ce-198">Cluster Service Writer</span></span>

<span data-ttu-id="cb1ce-199">O gravador VSS do serviço de cluster está documentado na documentação da API do [serviço de cluster](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .</span><span class="sxs-lookup"><span data-stu-id="cb1ce-199">The Cluster Service VSS writer is documented in the [Cluster Service](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API documentation.</span></span>

<span data-ttu-id="cb1ce-200">**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com Service Pack 1 (SP1) e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-200">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span>

## <a name="cluster-shared-volume-csv-vss-writer"></a><span data-ttu-id="cb1ce-201">Gravador VSS de Volume Compartilhado Clusterizado (CSV)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-201">Cluster Shared Volume (CSV) VSS Writer</span></span>

<span data-ttu-id="cb1ce-202">Esse gravador relata os arquivos de dados de Volume Compartilhado Clusterizado (CSV).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-202">This writer reports the Cluster Shared Volume (CSV) data files.</span></span> <span data-ttu-id="cb1ce-203">Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-203">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="cb1ce-204">**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-204">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-205">A cadeia de caracteres do nome do gravador para este gravador é "Volume Compartilhado Clusterizado gravador VSS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-205">The writer name string for this writer is "Cluster Shared Volume VSS Writer".</span></span>

<span data-ttu-id="cb1ce-206">A ID do gravador para o gravador é 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-206">The writer ID for the writer is 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span></span>

## <a name="com-class-registration-database-writer"></a><span data-ttu-id="cb1ce-207">Gravador de banco de dados de registro de classe COM+</span><span class="sxs-lookup"><span data-stu-id="cb1ce-207">COM+ Class Registration Database Writer</span></span>

<span data-ttu-id="cb1ce-208">Esse gravador é responsável pelo conteúdo do diretório de registro% SystemRoot% \\ .</span><span class="sxs-lookup"><span data-stu-id="cb1ce-208">This writer is responsible for the contents of the %SystemRoot%\\Registration directory.</span></span> <span data-ttu-id="cb1ce-209">O catálogo COM+ é um arquivo no registro de% SystemRoot% \\ com um nome que segue o padrão R *xxxxxxxxxxxx*. CLB, em que *xxxxxxxxxxxx* é um número hexadecimal de 12 dígitos.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-209">The COM+ catalog is a file in %SystemRoot%\\Registration with a name that follows the pattern R *xxxxxxxxxxxx*.clb, where *xxxxxxxxxxxx* is a 12-digit hexadecimal number.</span></span> <span data-ttu-id="cb1ce-210">Potencialmente, pode haver vários arquivos desse tipo se os aplicativos COM+ tiverem sido configurados no computador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-210">There can potentially be multiple such files if COM+ applications have been configured on the computer.</span></span> <span data-ttu-id="cb1ce-211">O arquivo que contém o catálogo COM+ atual é o arquivo com o maior valor de *xxxxxxxxxxxx*.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-211">The file that contains the current COM+ catalog is the file with the largest value of *xxxxxxxxxxxx*.</span></span>

<span data-ttu-id="cb1ce-212">**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-212">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-213">O banco de dados de registro de classe COM+ depende de uma chave de registro que está sendo submetida a backup e, portanto, precisa de backup e restauração junto com o registro.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-213">The COM+ class registration database depends on a registry key being backed up and hence needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="cb1ce-214">Para restaurar o banco de dados de registro do COM+, um aplicativo de backup (solicitante) deve chamar o método [**ICOMAdminCatalog:: RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="cb1ce-214">To restore the COM+ Registration Database, a backup application (requester) must call the [**ICOMAdminCatalog::RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="cb1ce-215">A cadeia de caracteres do nome do gravador para este gravador é "COM+ REGDB Writer".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-215">The writer name string for this writer is "COM+ REGDB Writer".</span></span>

<span data-ttu-id="cb1ce-216">A ID do gravador do gravador de banco de dados de registro de classe COM+ é 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-216">The writer ID for the COM+ class registration database writer is 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span></span>

## <a name="data-deduplication-writer"></a><span data-ttu-id="cb1ce-217">Gravador de eliminação de duplicação de dados</span><span class="sxs-lookup"><span data-stu-id="cb1ce-217">Data Deduplication Writer</span></span>

<span data-ttu-id="cb1ce-218">O gravador VSS de eliminação de duplicação de dados está documentado na documentação da API de [eliminação de duplicação de dados](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) .</span><span class="sxs-lookup"><span data-stu-id="cb1ce-218">The Data Deduplication VSS writer is documented in the [Data Deduplication](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API documentation.</span></span> <span data-ttu-id="cb1ce-219">Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-219">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="cb1ce-220">**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-220">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

## <a name="distributed-file-system-replication-dfsr"></a><span data-ttu-id="cb1ce-221">Replicação de Sistema de Arquivos Distribuído (DFSR)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-221">Distributed File System Replication (DFSR)</span></span>

<span data-ttu-id="cb1ce-222">O componente a seguir inclui um gravador VSS: [replicação de sistema de arquivos distribuído (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-222">The following component includes a VSS writer: [Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span></span>

<span data-ttu-id="cb1ce-223">**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-223">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a><span data-ttu-id="cb1ce-224">Gravador DHCP (protocolo de configuração dinâmica de hosts)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-224">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>

<span data-ttu-id="cb1ce-225">Esse gravador é responsável por enumerar os arquivos necessários para a função de servidor DHCP.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-225">This writer is responsible for enumerating files required for the DHCP server role.</span></span> <span data-ttu-id="cb1ce-226">Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-226">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="cb1ce-227">A cadeia de caracteres do nome do gravador para este gravador é "gravador Jet do DHCP".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-227">The writer name string for this writer is "Dhcp Jet Writer".</span></span>

<span data-ttu-id="cb1ce-228">A ID do gravador para este gravador é BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-228">The writer ID for this writer is BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span></span>

## <a name="file-replication-service-frs"></a><span data-ttu-id="cb1ce-229">FRS (Serviço de Replicação de Arquivos)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-229">File Replication Service (FRS)</span></span>

<span data-ttu-id="cb1ce-230">O gravador do serviço de replicação de arquivo está documentado em [backup e restauração de uma pasta FRS-Replicated SYSVOL](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-230">The File Replication Service writer is documented in [Backing Up and Restoring an FRS-Replicated SYSVOL Folder](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span></span>

<span data-ttu-id="cb1ce-231">**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-231">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="file-server-resource-manager-fsrm-writer"></a><span data-ttu-id="cb1ce-232">Gravador FSRM (Gerenciador de recursos de servidor de arquivos)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-232">File Server Resource Manager (FSRM) Writer</span></span>

<span data-ttu-id="cb1ce-233">Esse gravador enumera os arquivos de configuração do FSRM que são usados para o backup do estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-233">This writer enumerates the FSRM configuration files that are used for system state backup.</span></span> <span data-ttu-id="cb1ce-234">Durante as operações de restauração, ela impede alterações na configuração do FSRM e interrompe temporariamente a imposição de cotas e de triagens de arquivos.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-234">During restore operations it prevents changes in FSRM configuration and temporarily halts enforcement of quotas and file screens.</span></span> <span data-ttu-id="cb1ce-235">Depois que a restauração for concluída, o gravador atualizará o FSRM com a configuração restaurada.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-235">After the restore is complete, the writer refreshes FSRM with the configuration that was restored.</span></span> <span data-ttu-id="cb1ce-236">Esse gravador só está presente quando o FSRM (parte da função de serviços de arquivos) está instalado e em execução.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-236">This writer is only present when FSRM (part of File Services role) is both installed and running.</span></span> <span data-ttu-id="cb1ce-237">Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-237">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="cb1ce-238">**Windows Server 2003:** Esse gravador não tem suporte até o Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-238">**Windows Server 2003:** This writer is not supported until Windows Server 2003 R2.</span></span>

<span data-ttu-id="cb1ce-239">A cadeia de caracteres do nome do gravador para esse gravador é "gravador FSRM".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-239">The writer name string for this writer is "FSRM Writer".</span></span>

<span data-ttu-id="cb1ce-240">A ID do gravador para este gravador é 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-240">The writer ID for this writer is 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span></span>

## <a name="hyper-v-writer"></a><span data-ttu-id="cb1ce-241">Gravador do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="cb1ce-241">Hyper-V Writer</span></span>

<span data-ttu-id="cb1ce-242">O gravador VSS do Hyper-V está documentado na documentação da API do [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) .</span><span class="sxs-lookup"><span data-stu-id="cb1ce-242">The Hyper-V VSS writer is documented in the [Hyper-V](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API documentation.</span></span> <span data-ttu-id="cb1ce-243">Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-243">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="cb1ce-244">**Windows Server 2003:** Esse gravador não tem suporte até o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-244">**Windows Server 2003:** This writer is not supported until Windows Server 2008.</span></span>

## <a name="iis-configuration-writer"></a><span data-ttu-id="cb1ce-245">Gravador de configuração do IIS</span><span class="sxs-lookup"><span data-stu-id="cb1ce-245">IIS Configuration Writer</span></span>

<span data-ttu-id="cb1ce-246">O gravador de configuração do IIS é responsável por enumerar os arquivos de configuração do IIS.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-246">The IIS configuration writer is responsible for enumerating the IIS configuration files.</span></span>

<span data-ttu-id="cb1ce-247">**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-247">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="cb1ce-248">Os solicitantes são necessários para fazer backup dos arquivos de configuração do IIS, incluindo o arquivo de machine.config do .NET FX ou o arquivo de web.config raiz do ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-248">Requesters are required to back up the IIS configuration files, including the .NET FX machine.config file or the ASP.NET root web.config file.</span></span>

<span data-ttu-id="cb1ce-249">Esse gravador não faz backup do arquivo de machine.config do .NET FX ou do arquivo de web.config raiz ASP.NET porque esses arquivos são enumerados pelo gravador do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-249">This writer does not back up the .NET FX machine.config file or the ASP.NET root web.config file because these files are enumerated by the System Writer.</span></span>

<span data-ttu-id="cb1ce-250">Esse gravador faz backup de todos os arquivos que estão nos diretórios de configuração% windir% \\ System32 \\ inetsrv \\ \\ e% WINDIR% \\ System32 \\ inetsrv \\ , exceto pelos arquivos enumerados pelo gravador do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-250">This writer backs up all files that are in the %windir%\\system32\\inetsrv\\config\\schema and %windir%\\system32\\inetsrv\\config directories, except for files that are enumerated by the System Writer.</span></span>

<span data-ttu-id="cb1ce-251">A ID do gravador para o gravador de configuração do IIS é 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-251">The writer ID for the IIS configuration writer is 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span></span>

## <a name="iis-metabase-writer"></a><span data-ttu-id="cb1ce-252">Gravador de metabase do IIS</span><span class="sxs-lookup"><span data-stu-id="cb1ce-252">IIS Metabase Writer</span></span>

<span data-ttu-id="cb1ce-253">O gravador de metabase do IIS (servidor de informações da Internet) é responsável por enumerar o arquivo de metabase do IIS.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-253">The Internet Information Server (IIS) metabase writer is responsible for enumerating the IIS metabase file.</span></span>

<span data-ttu-id="cb1ce-254">**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-254">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="cb1ce-255">Os solicitantes são necessários para fazer backup do arquivo da metabase do IIS.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-255">Requesters are required to back up the IIS metabase file.</span></span>

<span data-ttu-id="cb1ce-256">A ID do gravador para o gravador da metabase do IIS é 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-256">The writer ID for the IIS metabase writer is 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span></span>

## <a name="microsoft-message-queuing-msmq-writer"></a><span data-ttu-id="cb1ce-257">Gravador MSMQ (enfileiramento de mensagens da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-257">Microsoft Message Queuing (MSMQ) Writer</span></span>

<span data-ttu-id="cb1ce-258">Esse gravador relata os arquivos de dados do MSMQ (enfileiramento de mensagens da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-258">This writer reports the Microsoft Message Queuing (MSMQ) data files.</span></span>

<span data-ttu-id="cb1ce-259">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-259">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-260">A cadeia de caracteres do nome do gravador para esse gravador é "MSMQ Writer (*SvcName*)", em que *SvcName* é o nome do serviço MSMQ ao qual o gravador está associado.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-260">The writer name string for this writer is "MSMQ Writer (*SvcName*)", where *SvcName* is the name of the MSMQ service the writer is associated with.</span></span> <span data-ttu-id="cb1ce-261">Para a instalação padrão, o nome do serviço é "MSMQ".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-261">For default installation, the service name is "MSMQ".</span></span> <span data-ttu-id="cb1ce-262">Para instâncias clusterizadas, o nome do serviço é MSMQ $*resourceName*, em que *resourceName* é o nome do recurso MSMQ clusterizado.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-262">For clustered instances, the service name is MSMQ$*ResourceName*, where *ResourceName* is the clustered MSMQ resource name.</span></span>

<span data-ttu-id="cb1ce-263">A ID do gravador para este gravador é 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-263">The writer ID for this writer is 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span></span>

## <a name="mssearch-service-writer"></a><span data-ttu-id="cb1ce-264">Gravador de serviço MSSearch</span><span class="sxs-lookup"><span data-stu-id="cb1ce-264">MSSearch Service Writer</span></span>

<span data-ttu-id="cb1ce-265">Esse gravador existe para excluir arquivos de índice de pesquisa de cópias de sombra após a criação.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-265">This writer exists to delete search index files from shadow copies after creation.</span></span> <span data-ttu-id="cb1ce-266">Isso é feito para minimizar o impacto da e/s de cópia em gravação durante e/s regular nesses arquivos no volume copiado por sombra.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-266">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span>

<span data-ttu-id="cb1ce-267">**Windows Server 2003:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-267">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-268">Para instalar esse gravador no servidor, você deve instalar a função serviços de arquivo e habilitar a Serviço de Pesquisa do Windows.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-268">To install this writer on the server, you must install the File Services role and enable the Windows Search Service.</span></span>

<span data-ttu-id="cb1ce-269">A cadeia de caracteres do nome do gravador para esse gravador é "gravador de serviço MSSearch".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-269">The writer name string for this writer is "MSSearch Service Writer".</span></span>

<span data-ttu-id="cb1ce-270">A ID do gravador para o gravador de serviço MSSearch é CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-270">The writer ID for the MSSearch service writer is CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span></span>

## <a name="nps-vss-writer"></a><span data-ttu-id="cb1ce-271">Gravador VSS do NPS</span><span class="sxs-lookup"><span data-stu-id="cb1ce-271">NPS VSS Writer</span></span>

<span data-ttu-id="cb1ce-272">O gravador do NPS é responsável por enumerar os arquivos de configuração do NPS (servidor de diretivas de rede) para servidores que têm a função de serviços de acesso e política de rede instalada.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-272">The NPS writer is responsible for enumerating the Network Policy Server (NPS) configuration files for servers that have the Network Policy and Access Services role installed.</span></span>

<span data-ttu-id="cb1ce-273">**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-273">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

<span data-ttu-id="cb1ce-274">A cadeia de caracteres do nome do gravador para esse gravador é "gravador VSS do NPS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-274">The writer name string for this writer is "NPS VSS Writer".</span></span>

<span data-ttu-id="cb1ce-275">A ID do gravador para o gravador VSS do NPS é 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-275">The writer ID for the NPS VSS writer is 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span></span>

## <a name="performance-counters-writer"></a><span data-ttu-id="cb1ce-276">Gravador de contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="cb1ce-276">Performance Counters Writer</span></span>

<span data-ttu-id="cb1ce-277">Esse gravador relata os arquivos de configuração do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-277">This writer reports the performance counter configuration files.</span></span> <span data-ttu-id="cb1ce-278">Esses arquivos são modificados apenas durante a instalação do aplicativo e devem ser armazenados em backup e restaurados durante as restaurações e backups de estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-278">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

<span data-ttu-id="cb1ce-279">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-279">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="cb1ce-280">Os solicitantes são necessários para fazer backup desses arquivos manualmente.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-280">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="cb1ce-281">(Consulte [fazendo backup e restaurando o estado do sistema](locating-additional-system-files.md).)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-281">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="cb1ce-282">A cadeia de caracteres do nome do gravador para esse gravador é "gravador de contadores de desempenho".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-282">The writer name string for this writer is "Performance Counters Writer".</span></span>

<span data-ttu-id="cb1ce-283">A ID do gravador para o gravador de contadores de desempenho é 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-283">The writer ID for the Performance Counters Writer is 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span></span>

## <a name="registry-writer"></a><span data-ttu-id="cb1ce-284">Gravador do registro</span><span class="sxs-lookup"><span data-stu-id="cb1ce-284">Registry Writer</span></span>

<span data-ttu-id="cb1ce-285">O gravador do registro informa os arquivos de registro do Windows para habilitar backups in-loco e restaurações do registro.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-285">The registry writer is reports the Windows registry files to enable in-place backups and restores of the registry.</span></span> <span data-ttu-id="cb1ce-286">Ele não relata hives de usuário.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-286">It does not report user hives.</span></span>

<span data-ttu-id="cb1ce-287">**Windows Server 2003:** No Windows Server 2003, esse gravador usa um arquivo de repositório intermediário (às vezes chamado de "arquivo saliva") para armazenar os dados do registro.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-287">**Windows Server 2003:** In Windows Server 2003, this writer uses an intermediate repository file (sometimes called a "spit file") to store registry data.</span></span> <span data-ttu-id="cb1ce-288">(Consulte [operações de backup e restauração do registro em VSS](registry-backup-and-restore-operations-under-vss.md).)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-288">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="cb1ce-289">**Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-289">**Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="cb1ce-290">(Consulte [operações de backup e restauração do registro em VSS](registry-backup-and-restore-operations-under-vss.md).)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-290">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="cb1ce-291">A cadeia de caracteres do nome do gravador para esse gravador é "gravador do registro".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-291">The writer name string for this writer is "Registry Writer".</span></span>

<span data-ttu-id="cb1ce-292">A ID do gravador para o gravador do registro é AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-292">The writer ID for the registry writer is AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span></span>

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a><span data-ttu-id="cb1ce-293">Gravador VSS do gateway de Serviços de Área de Trabalho Remota (serviços de terminal)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-293">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>

<span data-ttu-id="cb1ce-294">Esse gravador é responsável por enumerar os arquivos de gateway de Serviços de Área de Trabalho Remota (serviços de terminal) para servidores que têm Área de Trabalho Remota gateway, uma subfunção de Serviços de Área de Trabalho Remota função, instalada.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-294">This writer is responsible for enumerating the Remote Desktop Services (Terminal Services) Gateway files for servers that have Remote Desktop Gateway, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="cb1ce-295">**Windows Server 2003:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-295">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-296">Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-296">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="cb1ce-297">O gateway de Serviços de Área de Trabalho Remota depende de várias chaves do registro cujo backup está sendo feito e, portanto, precisa de backup e restauração junto com o registro.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-297">The Remote Desktop Services Gateway depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="cb1ce-298">A cadeia de caracteres do nome do gravador para esse gravador é "gravador de Gateway TS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-298">The writer name string for this writer is "TS Gateway Writer".</span></span>

<span data-ttu-id="cb1ce-299">A ID do gravador para este gravador é 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-299">The writer ID for this writer is 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span></span>

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a><span data-ttu-id="cb1ce-300">Gravador VSS de licenciamento do Serviços de Área de Trabalho Remota (serviços de terminal)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-300">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="cb1ce-301">Esse gravador é responsável por enumerar os arquivos de licenciamento de Serviços de Área de Trabalho Remota (Licenciamento RD) ou licenciamento de serviços de terminal (Licenciamento TS) para servidores que têm Área de Trabalho Remota licenciamento, uma subfunção de Serviços de Área de Trabalho Remota função instalada.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-301">This writer is responsible for enumerating the Remote Desktop Services Licensing (RD Licensing) or Terminal Services Licensing (TS Licensing) files for servers that have Remote Desktop Licensing, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="cb1ce-302">**Windows Server 2003:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-302">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-303">Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-303">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="cb1ce-304">Serviços de Área de Trabalho Remota licenciamento depende de várias chaves do registro cujo backup está sendo feito e, portanto, precisa de backup e restauração junto com o registro.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-304">Remote Desktop Services Licensing depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="cb1ce-305">A cadeia de caracteres do nome do gravador para este gravador é "TermServLicensing".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-305">The writer name string for this writer is "TermServLicensing".</span></span>

<span data-ttu-id="cb1ce-306">A ID do gravador para este gravador é 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-306">The writer ID for this writer is 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span></span>

## <a name="shadow-copy-optimization-writer"></a><span data-ttu-id="cb1ce-307">Gravador de otimização de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cb1ce-307">Shadow Copy Optimization Writer</span></span>

<span data-ttu-id="cb1ce-308">Esse gravador exclui determinados arquivos de cópias de sombra de volume.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-308">This writer deletes certain files from volume shadow copies.</span></span> <span data-ttu-id="cb1ce-309">Isso é feito para minimizar o impacto da e/s de cópia em gravação durante e/s regular nesses arquivos no volume copiado por sombra.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-309">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span> <span data-ttu-id="cb1ce-310">Os arquivos que são excluídos normalmente são arquivos temporários ou arquivos que não contêm o estado do sistema ou do usuário.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-310">The files that are deleted are typically temporary files or files that do not contain user or system state.</span></span>

<span data-ttu-id="cb1ce-311">**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-311">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-312">A cadeia de caracteres do nome do gravador para este gravador é "gravador de otimização de cópia de sombra".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-312">The writer name string for this writer is "Shadow Copy Optimization Writer".</span></span>

<span data-ttu-id="cb1ce-313">A ID do gravador para o gravador de otimização de cópia de sombra é 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-313">The writer ID for the shadow copy optimization writer is 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span></span>

## <a name="sync-share-service-writer"></a><span data-ttu-id="cb1ce-314">Gravador do serviço de compartilhamento de sincronização</span><span class="sxs-lookup"><span data-stu-id="cb1ce-314">Sync Share Service Writer</span></span>

<span data-ttu-id="cb1ce-315">**Windows Server 2012 R2:** Esse gravador está incluído no Windows Server 2012 R2 e nas versões mais recentes do servidor.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-315">**Windows Server 2012 R2:** This writer is included with Windows Server 2012 R2 and newer server versions.</span></span> <span data-ttu-id="cb1ce-316">Ele não é compatível com as versões da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-316">It is not compatible with desktop versions.</span></span>

<span data-ttu-id="cb1ce-317">Esse gravador é responsável por enumerar os compartilhamentos de sincronização em servidores que têm o serviço de compartilhamento de sincronização instalado e para garantir que seus metadados e dados permaneçam consistentes durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-317">This writer is responsible for enumerating the sync shares on servers that have the Sync Share Service installed, and for ensuring that their metadata and data remain consistent during backup and restore.</span></span>

<span data-ttu-id="cb1ce-318">Esse gravador só estará presente quando o serviço de compartilhamento de sincronização estiver instalado e em execução.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-318">This writer is only present when Sync Share Service is both installed and running.</span></span>

<span data-ttu-id="cb1ce-319">Haverá um componente do gravador VSS para cada compartilhamento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-319">There will be one VSS writer component for each sync share.</span></span> <span data-ttu-id="cb1ce-320">Isso inclui os metadados e os caminhos de dados.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-320">This includes the metadata and data paths.</span></span> <span data-ttu-id="cb1ce-321">Esses backups devem ser feitos juntos para fins de consistência.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-321">These must be backed up together for consistency.</span></span>

<span data-ttu-id="cb1ce-322">A cadeia de caracteres do nome do gravador é "gravador VSS do serviço de compartilhamento de sincronização".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-322">The writer name string is "Sync Share Service VSS writer".</span></span>

<span data-ttu-id="cb1ce-323">A ID do gravador é D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-323">The writer ID is D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span></span>

## <a name="system-writer"></a><span data-ttu-id="cb1ce-324">Gravador do sistema</span><span class="sxs-lookup"><span data-stu-id="cb1ce-324">System Writer</span></span>

<span data-ttu-id="cb1ce-325">O gravador do sistema enumera todos os binários do sistema operacional e do driver e é necessário para um backup do estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-325">The system writer enumerates all operating system and driver binaries and it is required for a system state backup.</span></span>

<span data-ttu-id="cb1ce-326">**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-326">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-327">Esse gravador é executado como parte do serviço de serviços de criptografia (CryptSvc).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-327">This writer runs as part of the Cryptographic Services (CryptSvc) service.</span></span> <span data-ttu-id="cb1ce-328">O gravador do sistema gera uma lista de arquivos que contém os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="cb1ce-328">The system writer generates a file list that contains the following files:</span></span>

-   <span data-ttu-id="cb1ce-329">Todos os arquivos estáticos que foram instalados.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-329">All static files that have been installed.</span></span> <span data-ttu-id="cb1ce-330">Um arquivo estático é um arquivo listado no manifesto do componente com o atributo de arquivo **writeableType** definido como "Static" ou "".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-330">A static file is a file that is listed in the component manifest with the **writeableType** file attribute set to "static" or "".</span></span> <span data-ttu-id="cb1ce-331">Os arquivos estáticos incluem todos os arquivos protegidos pelo Proteção de Recursos do Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-331">Static files include all files that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="cb1ce-332">No entanto, nem todos os arquivos estáticos são arquivos protegidos por WRP.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-332">However, not all static files are WRP-protected files.</span></span> <span data-ttu-id="cb1ce-333">Por exemplo, os arquivos de jogos são estáticos, mas não protegidos por WRP para que os administradores possam alterar as configurações de controle dos pais.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-333">For example, game files are static but not WRP-protected so that administrators can change parental control settings.</span></span>
-   <span data-ttu-id="cb1ce-334">O conteúdo do diretório do Windows lado a lado (WinSxS), incluindo todos os manifestos, componentes opcionais e arquivos Win32 de terceiros.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-334">The contents of the Windows Side-by-Side (WinSxS) directory, including all manifests, optional components, and third-party Win32 files.</span></span>
    > [!Note]  
    > <span data-ttu-id="cb1ce-335">Muitos dos arquivos no diretório% windir% \\ System32 são links físicos para arquivos no diretório WinSxS.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-335">Many of the files in the %windir%\\system32 directory are hard links to files in the WinSxS directory.</span></span>

     

-   <span data-ttu-id="cb1ce-336">Todos os arquivos PnP para drivers instalados (pertencentes a PnP).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-336">All PnP files for installed drivers (owned by PnP).</span></span>
-   <span data-ttu-id="cb1ce-337">Todos os serviços de modo de usuário e drivers não-PnP.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-337">All user-mode services and non-PnP drivers.</span></span>
-   <span data-ttu-id="cb1ce-338">Todos os catálogos de propriedade de CryptSvc.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-338">All catalogs owned by CryptSvc.</span></span>

<span data-ttu-id="cb1ce-339">O aplicativo de restauração é responsável por dispor os arquivos e o registro e definir as ACLs para corresponder à cópia de sombra do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-339">The restore application is responsible for laying down the files and registry and setting ACLs to match the system shadow copy.</span></span> <span data-ttu-id="cb1ce-340">Os links físicos apropriados também devem ser criados para que uma restauração de estado do sistema seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-340">The appropriate hard links must also be created for a system state restore to succeed.</span></span>

<span data-ttu-id="cb1ce-341">A cadeia de caracteres do nome do gravador para este gravador é "gravador do sistema".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-341">The writer name string for this writer is "System Writer".</span></span>

<span data-ttu-id="cb1ce-342">A ID do gravador para o gravador do sistema é E8132975-6F93-4464-A53E-1050253AE220.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-342">The writer ID for the system writer is E8132975-6F93-4464-A53E-1050253AE220.</span></span>

## <a name="task-scheduler-writer"></a><span data-ttu-id="cb1ce-343">Gravador de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cb1ce-343">Task Scheduler Writer</span></span>

<span data-ttu-id="cb1ce-344">Esse gravador relata os arquivos de tarefa do Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-344">This writer reports the task scheduler's task files.</span></span>

<span data-ttu-id="cb1ce-345">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-345">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="cb1ce-346">Os solicitantes são necessários para fazer backup desses arquivos manualmente.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-346">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="cb1ce-347">(Consulte [fazendo backup e restaurando o estado do sistema](locating-additional-system-files.md).)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-347">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="cb1ce-348">A cadeia de caracteres do nome do gravador para este gravador é "gravador de Agendador de Tarefas".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-348">The writer name string for this writer is "Task Scheduler Writer".</span></span>

<span data-ttu-id="cb1ce-349">A ID do gravador para o gravador é D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-349">The writer ID for the writer is D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span></span>

## <a name="vss-metadata-store-writer"></a><span data-ttu-id="cb1ce-350">Gravador de repositório de metadados do VSS</span><span class="sxs-lookup"><span data-stu-id="cb1ce-350">VSS Metadata Store Writer</span></span>

<span data-ttu-id="cb1ce-351">Esse gravador relata os arquivos de metadados do gravador para todos os gravadores Express do VSS.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-351">This writer reports the writer metadata files for all VSS express writers.</span></span>

<span data-ttu-id="cb1ce-352">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-352">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-353">A cadeia de caracteres do nome do gravador para esse gravador é "gravador do repositório de metadados do VSS Express Writer".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-353">The writer name string for this writer is "VSS Express Writer Metadata Store Writer".</span></span>

<span data-ttu-id="cb1ce-354">A ID do gravador para o gravador é 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-354">The writer ID for the writer is 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span></span>

## <a name="windows-deployment-services-wds-writer"></a><span data-ttu-id="cb1ce-355">Gravador do WDS (serviços de implantação do Windows)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-355">Windows Deployment Services (WDS) Writer</span></span>

<span data-ttu-id="cb1ce-356">Esse gravador relata os arquivos de dados do WDS (serviços de implantação do Windows).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-356">This writer reports the Windows Deployment Services (WDS) data files.</span></span>

<span data-ttu-id="cb1ce-357">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-357">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-358">A cadeia de caracteres do nome do gravador para esse gravador é "gravador VSS do WDS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-358">The writer name string for this writer is "WDS VSS Writer".</span></span>

<span data-ttu-id="cb1ce-359">A ID do gravador para este gravador é 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-359">The writer ID for this writer is 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span></span>

## <a name="windows-internal-database-wid-writer"></a><span data-ttu-id="cb1ce-360">Gravador do banco de dados interno do Windows (WID)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-360">Windows Internal Database (WID) Writer</span></span>

<span data-ttu-id="cb1ce-361">Esse gravador relata os arquivos de dados do banco de dados interno do Windows (WID).</span><span class="sxs-lookup"><span data-stu-id="cb1ce-361">This writer reports the Windows Internal Database (WID) data files.</span></span>

<span data-ttu-id="cb1ce-362">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-362">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-363">A cadeia de caracteres do nome do gravador para este gravador é "WIDWriter".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-363">The writer name string for this writer is "WIDWriter".</span></span>

<span data-ttu-id="cb1ce-364">A ID do gravador para este gravador é 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-364">The writer ID for this writer is 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span></span>

## <a name="windows-internet-name-service-wins-writer"></a><span data-ttu-id="cb1ce-365">Gravador WINS (serviço de cadastramento na Internet do Windows)</span><span class="sxs-lookup"><span data-stu-id="cb1ce-365">Windows Internet Name Service (WINS) Writer</span></span>

<span data-ttu-id="cb1ce-366">Esse gravador é responsável por enumerar os arquivos necessários para o WINS.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-366">This writer is responsible for enumerating files required for WINS.</span></span>

<span data-ttu-id="cb1ce-367">**Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-367">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-368">A cadeia de caracteres do nome do gravador para este gravador é "gravador Jet do WINS".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-368">The writer name string for this writer is "WINS Jet Writer".</span></span>

<span data-ttu-id="cb1ce-369">A ID do gravador para este gravador é F08C1483-8407-4A26-8C26-6C267A629741.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-369">The writer ID for this writer is F08C1483-8407-4A26-8C26-6C267A629741.</span></span>

## <a name="wmi-writer"></a><span data-ttu-id="cb1ce-370">Gravador WMI</span><span class="sxs-lookup"><span data-stu-id="cb1ce-370">WMI Writer</span></span>

<span data-ttu-id="cb1ce-371">Esse gravador é usado para identificar dados e estado específicos do WMI durante operações de backup.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-371">This writer is used for identifying WMI-specific state and data during backup operations.</span></span> <span data-ttu-id="cb1ce-372">Os dados incluem arquivos do repositório do WBEM.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-372">The data includes files from the WBEM repository.</span></span>

<span data-ttu-id="cb1ce-373">**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-373">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="cb1ce-374">A cadeia de caracteres do nome do gravador para este gravador é "gravador WMI".</span><span class="sxs-lookup"><span data-stu-id="cb1ce-374">The writer name string for this writer is "WMI Writer".</span></span>

<span data-ttu-id="cb1ce-375">A ID do gravador para este gravador é A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span><span class="sxs-lookup"><span data-stu-id="cb1ce-375">The writer ID for this writer is A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span></span>

 

 
