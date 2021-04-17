---
title: Objeto do restaurador de backup
description: Objeto do restaurador de backup
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- SDK do Windows Media Format, objetos do restaurador de backup
- ASF (Advanced Systems Format), objetos do restaurador de backup
- ASF (formato de sistemas avançados), objetos do restaurador de backup
- objetos, objetos do restaurador de backup
- restaurador de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105759579"
---
# <a name="backup-restorer-object"></a><span data-ttu-id="0dd08-108">Objeto do restaurador de backup</span><span class="sxs-lookup"><span data-stu-id="0dd08-108">Backup Restorer Object</span></span>

<span data-ttu-id="0dd08-109">O restaurador de backup fornece interfaces para lidar com o backup de licenças, normalmente em mídia removível e, em seguida, a restauração dessas licenças em um novo computador.</span><span class="sxs-lookup"><span data-stu-id="0dd08-109">The backup restorer provides interfaces to handle backing up licenses, typically onto removable media, and then restoring those licenses onto a new computer.</span></span>

<span data-ttu-id="0dd08-110">O objeto do restaurador de backup é criado pela função [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) , que define um ponteiro para uma interface [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) .</span><span class="sxs-lookup"><span data-stu-id="0dd08-110">The backup restorer object is created by the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function, which sets a pointer to an [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) interface.</span></span> <span data-ttu-id="0dd08-111">As outras interfaces do objeto do restaurador de backup podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="0dd08-111">The other interfaces of the backup restorer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="0dd08-112">As interfaces a seguir têm suporte do objeto restaurador de backup.</span><span class="sxs-lookup"><span data-stu-id="0dd08-112">The following interfaces are supported by the backup restorer object.</span></span>



| <span data-ttu-id="0dd08-113">Interface</span><span class="sxs-lookup"><span data-stu-id="0dd08-113">Interface</span></span>                                              | <span data-ttu-id="0dd08-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dd08-114">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dd08-115">**IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="0dd08-115">**IWMBackupRestoreProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | <span data-ttu-id="0dd08-116">Define e recupera as propriedades exigidas pelas interfaces [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) e [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) .</span><span class="sxs-lookup"><span data-stu-id="0dd08-116">Sets and retrieves properties required by the [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) and [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) interfaces.</span></span> |
| [<span data-ttu-id="0dd08-117">**IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="0dd08-117">**IWMLicenseBackup**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | <span data-ttu-id="0dd08-118">Faz backup de licenças, normalmente para que elas possam ser restauradas em outro computador.</span><span class="sxs-lookup"><span data-stu-id="0dd08-118">Backs up licenses, typically so that they can be restored onto another computer.</span></span>                                                                          |
| [<span data-ttu-id="0dd08-119">**IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="0dd08-119">**IWMLicenseRestore**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | <span data-ttu-id="0dd08-120">Restaura licenças.</span><span class="sxs-lookup"><span data-stu-id="0dd08-120">Restores licenses.</span></span>                                                                                                                                        |



 

<span data-ttu-id="0dd08-121">A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para usar o objeto de restaurador de backup.</span><span class="sxs-lookup"><span data-stu-id="0dd08-121">The following callback interface must be implemented by the application in order to use the backup restorer object.</span></span>



| <span data-ttu-id="0dd08-122">Interface</span><span class="sxs-lookup"><span data-stu-id="0dd08-122">Interface</span></span>                                      | <span data-ttu-id="0dd08-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dd08-123">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="0dd08-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="0dd08-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="0dd08-125">Recebe mensagens de status de processos que são executados em um thread separado.</span><span class="sxs-lookup"><span data-stu-id="0dd08-125">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0dd08-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0dd08-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dd08-127">**Fazendo backup e restaurando licenças**</span><span class="sxs-lookup"><span data-stu-id="0dd08-127">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> <dt>

[<span data-ttu-id="0dd08-128">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="0dd08-128">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




