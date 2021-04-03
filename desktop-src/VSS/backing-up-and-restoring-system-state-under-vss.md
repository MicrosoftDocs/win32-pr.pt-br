---
description: Observação Este tópico se aplica somente ao Windows Server 2003 R2 e ao Windows Server 2003 com Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Fazendo backup e restaurando o estado do sistema no Windows Server 2003 R2 e no Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922718"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a><span data-ttu-id="053be-103">Fazendo backup e restaurando o estado do sistema no Windows Server 2003 R2 e no Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="053be-103">Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1</span></span>

> [!Note]  
> <span data-ttu-id="053be-104">Este tópico se aplica somente ao Windows Server 2003 R2 e ao Windows Server 2003 com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="053be-104">This topic only applies to Windows Server 2003 R2 and Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="053be-105">Para obter informações sobre outras versões de sistema operacional, consulte [fazendo backup e restaurando o estado do sistema](locating-additional-system-files.md).</span><span class="sxs-lookup"><span data-stu-id="053be-105">For information about other operating system versions, see [Backing Up and Restoring System State](locating-additional-system-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="053be-106">A Microsoft não fornece suporte técnico de desenvolvedor ou profissional de ti para implementar restaurações de estado do sistema online no Windows (todas as versões).</span><span class="sxs-lookup"><span data-stu-id="053be-106">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span> <span data-ttu-id="053be-107">Para obter informações sobre como usar as APIs e os procedimentos fornecidos pela Microsoft para implementar restaurações de estado do sistema online, consulte os recursos da Comunidade disponíveis no [msdn Community Center](https://msdn.microsoft.com/community/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="053be-107">For information about using Microsoft-provided APIs and procedures to implement online system state restores, see the community resources available at the [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).</span></span>

 

<span data-ttu-id="053be-108">Ao executar um backup ou restauração do VSS, o estado do sistema do Windows é definido como sendo uma coleção de vários elementos principais do sistema operacional e seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="053be-108">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="053be-109">Esses elementos sempre devem ser tratados por operações de backup e restauração como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="053be-109">These elements should always be treated by backup and restore operations as a unit.</span></span>

<span data-ttu-id="053be-110">No Windows Server 2003 R2 e no Windows Server 2003 com SP1, não há nenhuma API do Windows criada para tratar esses objetos como um, portanto, é recomendável que os solicitantes tenham seu próprio objeto de estado do sistema para que possam processar esses componentes de forma consistente.</span><span class="sxs-lookup"><span data-stu-id="053be-110">In Windows Server 2003 R2 and Windows Server 2003 with SP1, there is no Windows API designed to treat these objects as one, so it is recommended that requesters have their own system state object so that they can process these components in a consistent manner.</span></span>

<span data-ttu-id="053be-111">Como o VSS é executado em versões do Windows em que o WFP ( [*proteção de arquivo do sistema*](vssgloss-s.md) ) protege os arquivos de estado do sistema contra corrupção, são necessárias etapas especiais para fazer backup e restaurar o estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="053be-111">Because VSS runs on versions of Windows where [*System File Protection*](vssgloss-s.md) (WFP) protects system state files from corruption, special steps are needed to back up and restore system state.</span></span>

<span data-ttu-id="053be-112">O estado do sistema consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="053be-112">System state consists of the following:</span></span>

-   <span data-ttu-id="053be-113">Todos os arquivos protegidos por WFP, arquivos de inicialização, incluindo NTLDR, NTDETECT e configurações de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="053be-113">All files protected by WFP, boot files including ntldr, ntdetect, and performance counter configurations</span></span>
-   <span data-ttu-id="053be-114">O Active Directory (ADSI) (em sistemas que são controladores de domínio)</span><span class="sxs-lookup"><span data-stu-id="053be-114">The Active Directory (ADSI) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="053be-115">A pasta de volume do sistema (SYSVOL) que é replicada pelo FRS (serviço de replicação de arquivo) (em sistemas que são controladores de domínio)</span><span class="sxs-lookup"><span data-stu-id="053be-115">The System Volume Folder (SYSVOL) that is replicated by the File Replication Service (FRS) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="053be-116">Servidor de certificado (em sistemas que fornecem autoridade de certificação)</span><span class="sxs-lookup"><span data-stu-id="053be-116">Certificate server (on systems that provide Certification Authority)</span></span>
-   <span data-ttu-id="053be-117">Banco de dados de cluster (em sistemas que são um nó de um cluster do Windows)</span><span class="sxs-lookup"><span data-stu-id="053be-117">Cluster database (on systems that are a node of a Windows cluster)</span></span>
-   <span data-ttu-id="053be-118">Serviço de Registro</span><span class="sxs-lookup"><span data-stu-id="053be-118">Registry service</span></span>
-   <span data-ttu-id="053be-119">Banco de dados de registro de classe COM+</span><span class="sxs-lookup"><span data-stu-id="053be-119">COM+ class registration database</span></span>

<span data-ttu-id="053be-120">O backup do estado do sistema pode ser feito em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="053be-120">The system state can be backed up in any order.</span></span>

<span data-ttu-id="053be-121">No entanto, a restauração do estado do sistema deve substituir os arquivos de inicialização primeiro e confirmar a seção do sistema (Hive) do registro como uma etapa final no processo e pode ocorrer na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="053be-121">However, the restoration of the system state should replace boot files first and commit the system section (hive) of the registry as a final step in the process, and might occur in the following order:</span></span>

1.  <span data-ttu-id="053be-122">Restaure os arquivos de inicialização.</span><span class="sxs-lookup"><span data-stu-id="053be-122">Restore the boot files.</span></span>
2.  <span data-ttu-id="053be-123">Banco de dados de registro de classe COM+</span><span class="sxs-lookup"><span data-stu-id="053be-123">COM+ class registration database</span></span>
3.  <span data-ttu-id="053be-124">Restaurar SYSVOL, servidor de certificado e bancos de dados de cluster (se necessário).</span><span class="sxs-lookup"><span data-stu-id="053be-124">Restore SYSVOL, Certificate Server, and Cluster databases (if needed).</span></span>
4.  <span data-ttu-id="053be-125">Restaurar Active Directory (se necessário).</span><span class="sxs-lookup"><span data-stu-id="053be-125">Restore Active Directory (if needed).</span></span>
5.  <span data-ttu-id="053be-126">Restaure o registro.</span><span class="sxs-lookup"><span data-stu-id="053be-126">Restore the registry.</span></span>

<span data-ttu-id="053be-127">Alguns serviços do sistema, como a autoridade de certificação, têm gravadores VSS convencionais e seguem os algoritmos de backup e restauração do VSS.</span><span class="sxs-lookup"><span data-stu-id="053be-127">Some system services, such as the Certification Authority, have conventional VSS writers and follow the VSS backup and restore algorithms.</span></span> <span data-ttu-id="053be-128">Outros, como o registro, exigem operações de backup ou restauração personalizadas; para obter mais informações, consulte [backups e restaurações personalizadas](custom-backups-and-restores.md).</span><span class="sxs-lookup"><span data-stu-id="053be-128">Others, such as the registry, require custom backup or restore operations; for more information, see [Custom Backups and Restores](custom-backups-and-restores.md).</span></span>

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a><span data-ttu-id="053be-129">Backup e restaurações do VSS de arquivos de inicialização e do sistema</span><span class="sxs-lookup"><span data-stu-id="053be-129">VSS Backup and Restores of Boot and System Files</span></span>

<span data-ttu-id="053be-130">Os arquivos de inicialização e de sistema devem ser armazenados em backup e restaurados somente como uma única entidade.</span><span class="sxs-lookup"><span data-stu-id="053be-130">The boot and system files should be backed up and restored only as a single entity.</span></span>

<span data-ttu-id="053be-131">Um solicitante pode usar com segurança as versões de cópia de sombra desses arquivos e deve ter certeza de que o volume do sistema e o dispositivo de inicialização sejam [*copiados em sombra*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="053be-131">A requester can safely use shadow-copied versions of these files, and should be sure that the system volume and boot device are [*shadow copied*](vssgloss-s.md).</span></span>

<span data-ttu-id="053be-132">Os arquivos do sistema e de inicialização incluem:</span><span class="sxs-lookup"><span data-stu-id="053be-132">The system and boot files include:</span></span>

-   <span data-ttu-id="053be-133">Os principais arquivos de inicialização:</span><span class="sxs-lookup"><span data-stu-id="053be-133">The core boot files:</span></span> <dl> <span data-ttu-id="053be-134">NtLdr.exe</span><span class="sxs-lookup"><span data-stu-id="053be-134">NtLdr.exe</span></span>  
    <span data-ttu-id="053be-135">Boot.ini</span><span class="sxs-lookup"><span data-stu-id="053be-135">Boot.ini</span></span>  
    <span data-ttu-id="053be-136">NtDetect.com</span><span class="sxs-lookup"><span data-stu-id="053be-136">NtDetect.com</span></span>  
    <span data-ttu-id="053be-137">NtBootDD.sys (se presente)</span><span class="sxs-lookup"><span data-stu-id="053be-137">NtBootDD.sys (if present)</span></span>  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> <span data-ttu-id="053be-138">% SystemRoot% \\ System32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span><span class="sxs-lookup"><span data-stu-id="053be-138">%SystemRoot%\\System32\\CatRoot\\{F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span></span> </dl><span data-ttu-id="053be-139">
-   Todos os arquivos protegidos pela [\*proteção de arquivo do sistema*](vssgloss-s.md) e enumerados pelo [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (consulte operações de restauração do VSS de arquivos protegidos por WFP) -   os arquivos de configuração do contador de desempenho:</span><span class="sxs-lookup"><span data-stu-id="053be-139">
-   All files protected by [\*System File Protection*](vssgloss-s.md) and enumerated by [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (see VSS Restore Operations of WFP Protected Files) -   The Performance Counter Configuration files:</span></span> <dl> <span data-ttu-id="053be-140">% SystemRoot% \\ System32 \\ perf? 00?. DATs</span><span class="sxs-lookup"><span data-stu-id="053be-140">%SystemRoot%\\System32\\Perf?00?.dat</span></span>  
    <span data-ttu-id="053be-141">% SystemRoot% \\ System32 \\ perf? 00?. Bak</span><span class="sxs-lookup"><span data-stu-id="053be-141">%SystemRoot%\\System32\\Perf?00?.bak</span></span> </dl><span data-ttu-id="053be-142">
-   Se estiver presente, o arquivo da metabase do IIS (servidor de informações da Internet) deverá ser incluído nas operações de backup e restauração porque ele contém o estado usado pelo Microsoft Exchange e outros aplicativos de rede.</span><span class="sxs-lookup"><span data-stu-id="053be-142">
-   If present, the Internet Information Server (IIS) metabase file should be included in backup and restore operations because it contains state that is used by Microsoft Exchange and other network applications.</span></span> <span data-ttu-id="053be-143">Esse arquivo pode ser encontrado em:</span><span class="sxs-lookup"><span data-stu-id="053be-143">This file can be found at:</span></span> <dl> <span data-ttu-id="053be-144">% SystemRoot% \\ System32 \\ inetsrv \\ metabase. bin</span><span class="sxs-lookup"><span data-stu-id="053be-144">%SystemRoot%\\System32\\InetSrv\\Metabase.bin</span></span> </dl><span data-ttu-id="053be-145">
-   Se o backup do arquivo da metabase do IIS for feito, as chaves para permitir que os aplicativos leiam determinadas entradas criptografadas devem ser restauradas como parte do estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="053be-145">
-   If the IIS metabase file is backed up, keys to enable applications to read certain encrypted entries should be restored as part of the system state.</span></span> <span data-ttu-id="053be-146">Os arquivos podem ser encontrados em:</span><span class="sxs-lookup"><span data-stu-id="053be-146">The files can be found under:</span></span> <dl> <span data-ttu-id="053be-147">% SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="053be-147">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
    <span data-ttu-id="053be-148">% AllUsersProfile% \\ Microsoft \\ crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="053be-148">%AllUsersProfile%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span> </dl><span data-ttu-id="053be-149">
-Ao fazer backup de arquivos de inicialização e do sistema, pode ser necessário determinar o dispositivo de inicialização do dos fazendo o seguinte: 1. localize a partição do sistema em \*\*HKEY \_ local \_ Machine*\* \\ \*\*System*\* \\ \*\*Setup*\* \\ \*\*SystemPartition\**.</span><span class="sxs-lookup"><span data-stu-id="053be-149">
-   When backing up boot and system files, it may become necessary to determine the DOS boot device by doing the following: 1.  Find the system partition under \*\*HKEY\_LOCAL\_MACHINE\*\*\\*\*System\*\*\\*\*Setup\*\*\\*\*SystemPartition\**.</span></span>
    <span data-ttu-id="053be-150">2.  Passar a variável de ambiente raiz do sistema (% SystemRoot%) para o Gerenciador de montagem para obter o nome do dispositivo NT.</span><span class="sxs-lookup"><span data-stu-id="053be-150">2.  Pass the System Root environment variable (%SystemRoot%) to the mount manager to obtain the NT device name.</span></span>

## <a name="vss-restore-operations-of-wfp-protected-files"></a><span data-ttu-id="053be-151">Operações de restauração do VSS de arquivos protegidos por WFP</span><span class="sxs-lookup"><span data-stu-id="053be-151">VSS Restore Operations of WFP Protected Files</span></span>

<span data-ttu-id="053be-152">O serviço WFP foi projetado para impedir a substituição acidental ou gradual de arquivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="053be-152">The WFP service is designed to prevent accidental or piecemeal replacement of system files.</span></span> <span data-ttu-id="053be-153">Portanto, etapas especiais precisam ser executadas para restaurar dados WFP.</span><span class="sxs-lookup"><span data-stu-id="053be-153">Therefore, special steps need to be undertaken to restore WFP data.</span></span>

<span data-ttu-id="053be-154">O significa que o gravador WFP deve especificar o método de restauração do **VSS \_ RME \_ \_ na \_ reinicialização** ao definir seu documento de metadados do gravador.</span><span class="sxs-lookup"><span data-stu-id="053be-154">The means the WFP writer should specify the **VSS\_RME\_RESTORE\_AT\_REBOOT** restore method when defining its Writer Metadata Document.</span></span> <span data-ttu-id="053be-155">Se um solicitante determinar que o gravador WFP falhou ao especificar esse método de restauração, ele indicará um erro de gravador.</span><span class="sxs-lookup"><span data-stu-id="053be-155">If a requester determines that the WFP writer has failed to specify this restore method, it indicates a writer error.</span></span>

<span data-ttu-id="053be-156">Um solicitante deve implementar um método de restauração do **VSS \_ RME \_ Restore \_ na \_ reinicialização** usando a função do Win32 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) com o **atraso de MoveFile até o parâmetro \_ \_ \_ reboot** para substituir os arquivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="053be-156">A requester should implement a restore method of **VSS\_RME\_RESTORE\_AT\_REBOOT** using the Win32 function [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) with the **MOVEFILE\_DELAY\_UNTIL\_REBOOT** parameter to replace system files.</span></span> <span data-ttu-id="053be-157">Os arquivos restaurados não são copiados para os diretórios de arquivo do sistema real até após a reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="053be-157">The restored files are not copied into the actual system file directories until after system reboot.</span></span> <span data-ttu-id="053be-158">A substituição de arquivos protegidos do sistema ocorrerá somente se o valor da seguinte entrada de registro do **reg \_ Word** for definido como 1:</span><span class="sxs-lookup"><span data-stu-id="053be-158">The overwriting of protected system files will occur only if the value of the following **REG\_WORD** registry entry is set to 1:</span></span>

<span data-ttu-id="053be-159">**HKEY \_ \_** Gerenciador de sessão de controle CurrentControlSet do sistema de máquina local \\  \\  \\  \\  \\ **AllowProtectedRenames** = 1</span><span class="sxs-lookup"><span data-stu-id="053be-159">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Session Manager**\\**AllowProtectedRenames** = 1</span></span>

<span data-ttu-id="053be-160">Esse valor deve ser definido antes de qualquer inicialização em que os arquivos protegidos sejam substituídos via [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) e são excluídos após a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="053be-160">This value must be set before any boot where protected files are to be replaced via [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) and is deleted after reboot.</span></span>

<span data-ttu-id="053be-161">O diretório dllcache do sistema também deve ser submetido a backup ou restaurado, com backup e restauração do volume de inicialização, e está localizado examinando a entrada de registro **reg \_ Expand \_ sz** :</span><span class="sxs-lookup"><span data-stu-id="053be-161">The system dllcache directory should also be backed up or restored, with boot volume backup and restore, and is located by examining the **REG\_EXPAND\_SZ** registry entry:</span></span>

<span data-ttu-id="053be-162">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **SfcDllCache**</span><span class="sxs-lookup"><span data-stu-id="053be-162">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**SfcDllCache**</span></span><dl> <dt>

                  Data type
</dt> <dd>                  <span data-ttu-id="053be-163">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="053be-163">REG\_EXPAND\_SZ</span></span></dd> </dl>

<span data-ttu-id="053be-164">O conteúdo do diretório dllcache do sistema é recriado usando o verificador de arquivos do sistema (SFC) no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="053be-164">The contents of the system dllcache directory are rebuilt by using the System File Checker (SFC) from the command prompt:</span></span>

-   <span data-ttu-id="053be-165">A opção **/SCANONCE** examina todos os arquivos protegidos na próxima inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="053be-165">The **/SCANONCE** option scans all protected files at the next system boot.</span></span>
-   <span data-ttu-id="053be-166">A opção **/scannow** examina todos os arquivos protegidos imediatamente.</span><span class="sxs-lookup"><span data-stu-id="053be-166">The **/SCANNOW** option scans all protected files immediately.</span></span>

<span data-ttu-id="053be-167">Todos os arquivos protegidos serão verificados e todas as versões que não forem válidas serão substituídas no diretório e no local de dllcache.</span><span class="sxs-lookup"><span data-stu-id="053be-167">All protected files will be scanned, and any versions that are not valid will be replaced in both the directory and dllcache location.</span></span>

<span data-ttu-id="053be-168">Há quatro arquivos que fazem parte da WFP que não podem ser restaurados com os arquivos WFP:</span><span class="sxs-lookup"><span data-stu-id="053be-168">There are four files that are part of the WFP that cannot be restored with the WFP files:</span></span>

<dl> <span data-ttu-id="053be-169">Ctl3dv2.dll</span><span class="sxs-lookup"><span data-stu-id="053be-169">Ctl3dv2.dll</span></span>  
<span data-ttu-id="053be-170">DtcSetup.exe</span><span class="sxs-lookup"><span data-stu-id="053be-170">DtcSetup.exe</span></span>  
<span data-ttu-id="053be-171">NtDll.dll</span><span class="sxs-lookup"><span data-stu-id="053be-171">NtDll.dll</span></span>  
<span data-ttu-id="053be-172">Smss.exe</span><span class="sxs-lookup"><span data-stu-id="053be-172">Smss.exe</span></span>  
</dl>

<span data-ttu-id="053be-173">Esses arquivos ajudam no processo de restauração dos arquivos WFP e, como tal, há uma dependência circular.</span><span class="sxs-lookup"><span data-stu-id="053be-173">These files help in the process of restoring the WFP files and as such there is a circular dependency.</span></span> <span data-ttu-id="053be-174">Atualmente, não há como restaurar esses arquivos, exceto para reinstalar o Windows.</span><span class="sxs-lookup"><span data-stu-id="053be-174">Currently, there is no way to restore these files except to reinstall Windows.</span></span>

 

 
