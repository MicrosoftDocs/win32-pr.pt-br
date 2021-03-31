---
title: Fazendo backup e restaurando licenças
description: Fazendo backup e restaurando licenças
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- SDK do Windows Media Format, fazendo backup de licenças
- SDK do Windows Media Format, restaurando licenças
- SDK do Windows Media Format, backup e restauração de licenças
- ASF (Advanced Systems Format), fazendo backup de licenças
- ASF (formato de sistemas avançados), fazendo backup de licenças
- ASF (Advanced Systems Format), restaurando licenças
- ASF (formato de sistemas avançados), restaurando licenças
- ASF (Advanced Systems Format), backup de licença e restauração
- ASF (formato de sistemas avançados), backup e restauração de licenças
- DRM (gerenciamento de direitos digitais), fazendo backup de licenças
- DRM (gerenciamento de direitos digitais), fazendo backup de licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), backup e restauração de licenças
- DRM (gerenciamento de direitos digitais), backup e restauração de licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640153"
---
# <a name="backing-up-and-restoring-licenses"></a><span data-ttu-id="6f274-118">Fazendo backup e restaurando licenças</span><span class="sxs-lookup"><span data-stu-id="6f274-118">Backing Up and Restoring Licenses</span></span>

<span data-ttu-id="6f274-119">Os processos de backup e restauração são assíncronos.</span><span class="sxs-lookup"><span data-stu-id="6f274-119">The backup and restore processes are asynchronous.</span></span> <span data-ttu-id="6f274-120">Elas são disparadas quando o usuário seleciona um comando de menu ou uma opção no aplicativo para fazer backup ou restaurar licenças.</span><span class="sxs-lookup"><span data-stu-id="6f274-120">They are triggered when the user selects a menu command or option in the application to back up or restore licenses.</span></span> <span data-ttu-id="6f274-121">Você deve permitir que o usuário especifique os locais em que as licenças devem ser armazenadas em backup e restauradas.</span><span class="sxs-lookup"><span data-stu-id="6f274-121">You should allow the user to specify the locations where licenses must be backed up to and restored from.</span></span>

<span data-ttu-id="6f274-122">Para fazer backup de licenças:</span><span class="sxs-lookup"><span data-stu-id="6f274-122">To back up licenses:</span></span>

1.  <span data-ttu-id="6f274-123">Use a função [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) para criar o objeto de restaurador de backup.</span><span class="sxs-lookup"><span data-stu-id="6f274-123">Use the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="6f274-124">Chame o método [**IWMBackupRestoreProps:: SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) para definir o caminho de backup (o local onde você irá gravar os arquivos, como: \\ ou D: \\ licenças).</span><span class="sxs-lookup"><span data-stu-id="6f274-124">Call the [**IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) method to set the backup path (the location where you will write the files, such as A:\\ or D:\\Licenses).</span></span>
3.  <span data-ttu-id="6f274-125">Chame o método [**IWMLicenseBackup:: BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) para fazer backup das licenças no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="6f274-125">Call the [**IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) method to back up the licenses to the specified path.</span></span>

<span data-ttu-id="6f274-126">Os eventos a seguir são enviados para o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :</span><span class="sxs-lookup"><span data-stu-id="6f274-126">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="6f274-127">**WMT \_ BACKUPRESTORE \_ begin** indica que o processo de backup foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="6f274-127">**WMT\_BACKUPRESTORE\_BEGIN** indicates the backup process has started.</span></span>
-   <span data-ttu-id="6f274-128">**WMT \_ BACKUPRESTORE \_ end** indica que o processo de backup foi concluído.</span><span class="sxs-lookup"><span data-stu-id="6f274-128">**WMT\_BACKUPRESTORE\_END** indicates the backup process has been completed.</span></span>
-   <span data-ttu-id="6f274-129">**WMT \_ \_Licença restrita** indica que uma ou mais licenças não podem ser submetidas a backup porque o direito não foi permitido pelo proprietário do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6f274-129">**WMT\_RESTRICTED\_LICENSE** indicates that one or more licenses cannot be backed up because the right has been disallowed by the content owner.</span></span>

<span data-ttu-id="6f274-130">A ID da chave também é incluída nesta mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f274-130">The key ID is also included in this message.</span></span> <span data-ttu-id="6f274-131">Se você tiver implementado um banco de dados para arquivos protegidos que incluam a ID de chave e os metadados, você poderá exibir uma mensagem para o usuário com o título específico (como um título de música) para o qual não é possível fazer backup da licença.</span><span class="sxs-lookup"><span data-stu-id="6f274-131">If you have implemented a database for protected files that includes the key ID and metadata, you can display a message to the user with the specific title (such as a song title) for which the license cannot be backed up.</span></span> <span data-ttu-id="6f274-132">Caso contrário, a mensagem deve ser genérica e informar ao usuário que não é possível fazer backup de algumas licenças.</span><span class="sxs-lookup"><span data-stu-id="6f274-132">Otherwise, the message must be generic and inform the user that some licenses cannot be backed up.</span></span>

<span data-ttu-id="6f274-133">Para restaurar licenças:</span><span class="sxs-lookup"><span data-stu-id="6f274-133">To restore licenses:</span></span>

1.  <span data-ttu-id="6f274-134">Use a função **WMCreateBackupRestorer** para criar o objeto de restaurador de backup.</span><span class="sxs-lookup"><span data-stu-id="6f274-134">Use the **WMCreateBackupRestorer** function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="6f274-135">Chame o método **IWMBackupRestoreProps:: SetProp** para definir o caminho de restauração para o local onde são feitos o backup das licenças.</span><span class="sxs-lookup"><span data-stu-id="6f274-135">Call the **IWMBackupRestoreProps::SetProp** method to set the restore path to the location where licenses are backed up.</span></span>
3.  <span data-ttu-id="6f274-136">Chame o método [**IWMLicenseRestore:: RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) para restaurar licenças desse local.</span><span class="sxs-lookup"><span data-stu-id="6f274-136">Call the [**IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) method to restore licenses from that location.</span></span>

<span data-ttu-id="6f274-137">Os eventos a seguir são enviados para o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :</span><span class="sxs-lookup"><span data-stu-id="6f274-137">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="6f274-138">**WMT \_ BACKUPRESTORE \_ conexão** indica que o aplicativo está se conectando ao serviço de gerenciamento de licenças.</span><span class="sxs-lookup"><span data-stu-id="6f274-138">**WMT\_BACKUPRESTORE\_CONNECTING** indicates that the application is connecting to the License Management Service.</span></span>
-   <span data-ttu-id="6f274-139">**WMT \_ A \_ DESconexão do BACKUPRESTORE** indica que o aplicativo está desconectando do serviço de gerenciamento de licenças.</span><span class="sxs-lookup"><span data-stu-id="6f274-139">**WMT\_BACKUPRESTORE\_DISCONNECTING** indicates that the application is disconnecting from the License Management Service.</span></span>
-   <span data-ttu-id="6f274-140">**WMT \_ BACKUPRESTORE \_ begin** indica que o processo de restauração foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="6f274-140">**WMT\_BACKUPRESTORE\_BEGIN** indicates the restore process has started.</span></span>
-   <span data-ttu-id="6f274-141">**WMT \_ BACKUPRESTORE \_ end** indica que o processo de restauração foi concluído.</span><span class="sxs-lookup"><span data-stu-id="6f274-141">**WMT\_BACKUPRESTORE\_END** indicates the restore process has been completed.</span></span>

> [!Note]  
> <span data-ttu-id="6f274-142">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="6f274-142">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6f274-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f274-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f274-144">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="6f274-144">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="6f274-145">**Interface IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="6f274-145">**IWMBackupRestoreProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[<span data-ttu-id="6f274-146">**Interface IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="6f274-146">**IWMLicenseBackup Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[<span data-ttu-id="6f274-147">**Interface IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="6f274-147">**IWMLicenseRestore Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




