---
description: No Windows Vista e no Windows Server 2008 e posterior, o desenvolvedor de um gravador ou aplicativo VSS pode optar por excluir determinados arquivos das cópias de sombra.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Excluindo arquivos de cópias de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171809"
---
# <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="b2fda-103">Excluindo arquivos de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="b2fda-103">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="b2fda-104">No Windows Vista e no Windows Server 2008 e posterior, o desenvolvedor de um gravador ou aplicativo VSS pode optar por excluir determinados arquivos das cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="b2fda-104">In Windows Vista and Windows Server 2008 and later, the developer of a VSS writer or application may choose to exclude certain files from shadow copies.</span></span>

<span data-ttu-id="b2fda-105">O impacto no desempenho e a área de armazenamento de cópia de sombra (também chamada de "área de comparação") o uso de um arquivo em uma cópia de sombra estão diretamente relacionados à quantidade de alterações no conteúdo do arquivo depois que a cópia de sombra é criada.</span><span class="sxs-lookup"><span data-stu-id="b2fda-105">The performance impact and shadow copy storage area (also called "diff area") usage of a file in a shadow copy are directly related to the amount of change in the file's contents after the shadow copy is created.</span></span> <span data-ttu-id="b2fda-106">Além disso, a exclusão de arquivos de cópias de sombra pode retardar a criação da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="b2fda-106">In addition, excluding files from shadow copies may slow down shadow copy creation.</span></span>

<span data-ttu-id="b2fda-107">Por esses motivos, um arquivo deve ser excluído das cópias de sombra somente se for grande, passa por uma alteração significativa entre uma cópia de sombra e a próxima, e não precisa de backup.</span><span class="sxs-lookup"><span data-stu-id="b2fda-107">For these reasons, a file should be excluded from shadow copies only if it is large, undergoes significant change between one shadow copy and the next, and does not need to be backed up.</span></span>

<span data-ttu-id="b2fda-108">Você só deve excluir arquivos que pertençam ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b2fda-108">You should only exclude files that belong to your application.</span></span>

<span data-ttu-id="b2fda-109">Se o \_ sinalizador de \_ não-recuperação do VSS VOLSNAP \_ não \_ for definido no contexto de cópia de sombra, isso significará que a recuperação automática está desabilitada e nenhum arquivo pode ser excluído da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="b2fda-109">If the VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY flag is set in the shadow copy context, this means that auto-recovery is disabled, and no files can be excluded from the shadow copy.</span></span> <span data-ttu-id="b2fda-110">Para obter mais informações, consulte a enumeração de [**\_ \_ atributos de \_ instantâneo \_ de volume do VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) .</span><span class="sxs-lookup"><span data-stu-id="b2fda-110">For more information, see the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration.</span></span>

## <a name="using-the-addexcludefilesfromsnapshot-method"></a><span data-ttu-id="b2fda-111">Usando o método AddExcludeFilesFromSnapshot</span><span class="sxs-lookup"><span data-stu-id="b2fda-111">Using the AddExcludeFilesFromSnapshot Method</span></span>

<span data-ttu-id="b2fda-112">Um gravador VSS pode excluir arquivos de uma cópia de sombra da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b2fda-112">A VSS writer can exclude files from a shadow copy as follows:</span></span>

1.  <span data-ttu-id="b2fda-113">Chame o método [**IVssCreateWriterMetadataEx:: AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) para relatar os arquivos a serem excluídos.</span><span class="sxs-lookup"><span data-stu-id="b2fda-113">Call the [**IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) method to report the files to be excluded.</span></span>
2.  <span data-ttu-id="b2fda-114">No método [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) do gravador, exclua os arquivos da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="b2fda-114">In the writer's [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) method, delete the files from the shadow copy.</span></span>

## <a name="using-the-filesnottosnapshot-registry-key"></a><span data-ttu-id="b2fda-115">Usando a chave do registro FilesNotToSnapshot</span><span class="sxs-lookup"><span data-stu-id="b2fda-115">Using the FilesNotToSnapshot Registry Key</span></span>

> [!Note]  
> <span data-ttu-id="b2fda-116">A chave do Registro **FilesNotToSnapshot** deve ser usada somente por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b2fda-116">The **FilesNotToSnapshot** registry key is intended to be used only by applications.</span></span> <span data-ttu-id="b2fda-117">Os usuários que tentarem usá-lo encontrarão limitações, como as seguintes:</span><span class="sxs-lookup"><span data-stu-id="b2fda-117">Users who attempt to use it will encounter limitations such as the following:</span></span>
>
> -   <span data-ttu-id="b2fda-118">Ela não pode excluir arquivos de uma cópia de sombra criada em um Windows Server usando o recurso Versões Anteriores.</span><span class="sxs-lookup"><span data-stu-id="b2fda-118">It cannot delete files from a shadow copy that was created on a Windows Server by using the Previous Versions feature.</span></span>
> -   <span data-ttu-id="b2fda-119">Ela não pode excluir arquivos de cópias de sombra para pastas compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="b2fda-119">It cannot delete files from shadow copies for shared folders.</span></span>
> -   <span data-ttu-id="b2fda-120">Ele pode excluir arquivos de uma cópia de sombra que foi criada usando o utilitário [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) , mas não pode excluir arquivos de uma cópia de sombra que foi criada usando o utilitário [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="b2fda-120">It can delete files from a shadow copy that was created by using the [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) utility, but it cannot delete files from a shadow copy that was created by using the [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) utility.</span></span>
> -   <span data-ttu-id="b2fda-121">Os arquivos são excluídos de uma cópia de sombra com base no melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="b2fda-121">Files are deleted from a shadow copy on a best-effort basis.</span></span> <span data-ttu-id="b2fda-122">Isso significa que não há garantia de exclusão.</span><span class="sxs-lookup"><span data-stu-id="b2fda-122">This means that they are not guaranteed to be deleted.</span></span>

 

<span data-ttu-id="b2fda-123">Um aplicativo VSS pode excluir arquivos de uma cópia de sombra durante a criação da cópia de sombra usando a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="b2fda-123">A VSS application can delete files from a shadow copy during shadow copy creation by using the following registry key:</span></span>

<span data-ttu-id="b2fda-124">**HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToSnapshot**</span><span class="sxs-lookup"><span data-stu-id="b2fda-124">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\BackupRestore\\FilesNotToSnapshot**</span></span>

<span data-ttu-id="b2fda-125">Essa chave do registro tem \_ \_ valores de reg multi sz para cada aplicativo cujos arquivos podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="b2fda-125">This registry key has REG\_MULTI\_SZ values for each application whose files can be excluded.</span></span> <span data-ttu-id="b2fda-126">Os arquivos são especificados por caminhos totalmente qualificados, que podem conter o \* curinga.</span><span class="sxs-lookup"><span data-stu-id="b2fda-126">The files are specified by fully qualified paths, which can contain the \* wildcard.</span></span>

<span data-ttu-id="b2fda-127">Em todos os casos, a entrada será ignorada se não houver nenhum arquivo que corresponda à cadeia de caracteres do caminho.</span><span class="sxs-lookup"><span data-stu-id="b2fda-127">In all cases, the entry is ignored if there are no files that match the path string.</span></span>

<span data-ttu-id="b2fda-128">Depois que um arquivo é adicionado ao valor apropriado da chave do registro, ele é excluído da cópia de sombra durante a criação pelo gravador de otimização de cópia de sombra em uma base de melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="b2fda-128">After a file is added to the appropriate registry key value, it is deleted from the shadow copy during creation by the shadow copy optimization writer on a best-effort basis.</span></span>

<span data-ttu-id="b2fda-129">Se um caminho totalmente qualificado não puder ser especificado, um caminho também poderá ser implícito usando a variável $UserProfile $ ou $AllVolumes $.</span><span class="sxs-lookup"><span data-stu-id="b2fda-129">If a fully qualified path cannot be specified, then a path can also be implied by using the $UserProfile$ or $AllVolumes$ variable.</span></span> <span data-ttu-id="b2fda-130">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b2fda-130">For example:</span></span>

-   <span data-ttu-id="b2fda-131">Nome de arquivo de subdiretório $UserProfile $ \\ Directory \\ \\ .\*</span><span class="sxs-lookup"><span data-stu-id="b2fda-131">$UserProfile$\\Directory\\Subdirectory\\FileName.\*</span></span>
-   <span data-ttu-id="b2fda-132">$AllVolumes $ \\ TemporaryFiles \\ \* .\*</span><span class="sxs-lookup"><span data-stu-id="b2fda-132">$AllVolumes$\\TemporaryFiles\\\*.\*</span></span>

<span data-ttu-id="b2fda-133">Para tornar o caminho recursivo, acrescente "/s" ao final.</span><span class="sxs-lookup"><span data-stu-id="b2fda-133">To make the path recursive, append " /s" to the end.</span></span> <span data-ttu-id="b2fda-134">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b2fda-134">For example:</span></span>

-   <span data-ttu-id="b2fda-135">Nome de \\ arquivo do subdiretório do $USERPROFILE $ Directory \\ \\ . \* /s</span><span class="sxs-lookup"><span data-stu-id="b2fda-135">$UserProfile$\\Directory\\Subdirectory\\FileName.\* /s</span></span>
-   <span data-ttu-id="b2fda-136">$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s</span><span class="sxs-lookup"><span data-stu-id="b2fda-136">$AllVolumes$\\TemporaryFiles\\\*.\* /s</span></span>

<span data-ttu-id="b2fda-137">A variável $UserProfile $ faz com que a cadeia de caracteres do caminho seja aplicada a todos os perfis de usuário no computador.</span><span class="sxs-lookup"><span data-stu-id="b2fda-137">The $UserProfile$ variable causes the path string to be applied to all user profiles on the computer.</span></span> <span data-ttu-id="b2fda-138">Os perfis de usuário são enumerados examinando a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="b2fda-138">The user profiles are enumerated by examining the following registry key:</span></span>

<span data-ttu-id="b2fda-139">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ createfilelist**</span><span class="sxs-lookup"><span data-stu-id="b2fda-139">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\ProfileList**</span></span>

<span data-ttu-id="b2fda-140">A variável $AllVolumes $ faz com que a cadeia de caracteres do caminho seja aplicada a todas as cópias de sombra no computador.</span><span class="sxs-lookup"><span data-stu-id="b2fda-140">The $AllVolumes$ variable causes the path string to be applied to all shadow copies on the computer.</span></span> <span data-ttu-id="b2fda-141">Por exemplo, suponha que o caminho seja "$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s ", e o computador tem três volumes: C:, D: e E:.</span><span class="sxs-lookup"><span data-stu-id="b2fda-141">For example, suppose the path is "$AllVolumes$\\TemporaryFiles\\\*.\* /s", and the computer has three volumes: C:, D:, and E:.</span></span> <span data-ttu-id="b2fda-142">Se C: e E: contiver o caminho " \\ TemporaryFiles \\ " e o volume D: contiver apenas o caminho d: \\ Data \\ , a árvore de diretórios C: \\ TemporaryFiles \\ será excluída das cópias de sombra de C:, e a árvore de diretórios e: \\ TemporaryFiles \\ será excluída das cópias de sombra de E:.</span><span class="sxs-lookup"><span data-stu-id="b2fda-142">If C: and E: contain the path "\\TemporaryFiles\\", and volume D: contains only the path D:\\Data\\, the directory tree C:\\TemporaryFiles\\ is deleted from shadow copies of C:, and the directory tree E:\\TemporaryFiles\\ is deleted from shadow copies of E:.</span></span>

<span data-ttu-id="b2fda-143">Os administradores podem desabilitar a expansão da variável $UserProfile $ usando a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="b2fda-143">Administrators can disable expansion of the $UserProfile$ variable by using the following registry key:</span></span>

<span data-ttu-id="b2fda-144">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ configurações de VSS \\**</span><span class="sxs-lookup"><span data-stu-id="b2fda-144">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Vss\\Settings**</span></span>

<span data-ttu-id="b2fda-145">Nessa chave do registro, especifique DisableUserProfileExpansion para o nome do valor, REG \_ DWORD para o tipo de valor e um valor diferente de zero para os dados do valor.</span><span class="sxs-lookup"><span data-stu-id="b2fda-145">Under this registry key, specify DisableUserProfileExpansion for the value name, REG\_DWORD for the value type, and a nonzero value for the value data.</span></span>

## <a name="about-the-filesnottobackup-registry-key"></a><span data-ttu-id="b2fda-146">Sobre a chave do Registro FilesNotToBackup</span><span class="sxs-lookup"><span data-stu-id="b2fda-146">About the FilesNotToBackup Registry Key</span></span>

<span data-ttu-id="b2fda-147">A chave do registro **FilesNotToBackup** pode ser usada para especificar os nomes dos arquivos e diretórios nos quais os aplicativos de backup não devem fazer backup ou restaurar.</span><span class="sxs-lookup"><span data-stu-id="b2fda-147">The **FilesNotToBackup** registry key can be used to specify the names of the files and directories that backup applications should not backup or restore.</span></span> <span data-ttu-id="b2fda-148">No entanto, ele não exclui esses arquivos das cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="b2fda-148">However, it does not exclude those files from shadow copies.</span></span> <span data-ttu-id="b2fda-149">Para obter mais informações sobre essa chave do registro, consulte [chaves e valores do registro para backup e restauração](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="b2fda-149">For more information about this registry key, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

 

 
