---
description: O gravador de Active Directory não requer ações especiais durante as operações de backup.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Backup e restauração do VSS do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501735"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a><span data-ttu-id="6ab10-103">Backup e restauração do VSS do Active Directory</span><span class="sxs-lookup"><span data-stu-id="6ab10-103">VSS Backup and Restore of the Active Directory</span></span>

<span data-ttu-id="6ab10-104">O gravador de Active Directory não requer ações especiais durante as operações de backup.</span><span class="sxs-lookup"><span data-stu-id="6ab10-104">The Active Directory writer requires no special actions during backup operations.</span></span> <span data-ttu-id="6ab10-105">O gravador fornecerá o solicitante com informações de componente e conjunto de arquivos, e o solicitante usará essas informações para decidir quais arquivos serão copiados para a mídia de backup.</span><span class="sxs-lookup"><span data-stu-id="6ab10-105">The writer will provide the requester with component and file set information, and the requester uses that information to decide which files to copy to backup media.</span></span> <span data-ttu-id="6ab10-106">Não é necessário usar nenhuma API especial para fazer backup do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ab10-106">There is no need to use any special APIs to back up the Active Directory.</span></span>

<span data-ttu-id="6ab10-107">A forma como uma restauração é executada depende de o Active Directory ser restaurado como parte de uma operação de recuperação de desastre ou se a restauração é feita em um sistema no qual o Active Directory está em execução.</span><span class="sxs-lookup"><span data-stu-id="6ab10-107">How a restore is performed depends on whether the Active Directory is be restored as part of a disaster recovery operation, or if the restore is to a system on which the Active Directory is running.</span></span> <span data-ttu-id="6ab10-108">Além disso, a idade da cópia de backup do estado de Active Directory pode ser um problema devido à Active Directory marcas de exclusão.</span><span class="sxs-lookup"><span data-stu-id="6ab10-108">In addition, the age of the backup copy of the Active Directory state may be an issue because of Active Directory tombstones.</span></span>

## <a name="active-directory-restoration-following-disaster-recovery"></a><span data-ttu-id="6ab10-109">Restauração de Active Directory após a recuperação de desastre</span><span class="sxs-lookup"><span data-stu-id="6ab10-109">Active Directory Restoration following Disaster Recovery</span></span>

<span data-ttu-id="6ab10-110">Após uma falha exigindo a recuperação de desastre, o Active Directory pode ser restaurado como parte da restauração do estado do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6ab10-110">Following a crash requiring disaster recovery, the Active Directory can be restored as part of the restoration of the operating system state.</span></span>

<span data-ttu-id="6ab10-111">Essa operação de restauração é essencialmente uma restauração não-gravação.</span><span class="sxs-lookup"><span data-stu-id="6ab10-111">This restore operation is essentially a writerless restore.</span></span>

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a><span data-ttu-id="6ab10-112">Active Directory a restauração no sistema em que ele está em execução</span><span class="sxs-lookup"><span data-stu-id="6ab10-112">Active Directory Restoration on the System where It Is Running</span></span>

<span data-ttu-id="6ab10-113">O sistema deve ser reinicializado no modo de restauração dos serviços de diretório se o Active Directory estiver sendo executado no servidor.</span><span class="sxs-lookup"><span data-stu-id="6ab10-113">The system must be rebooted in Directory Services Restore mode if the Active Directory is currently running on the server.</span></span>

<span data-ttu-id="6ab10-114">O sistema operacional será executado sem o Active Directory, e toda a validação do usuário ocorrerá por meio do SAM (Gerenciador de contas de segurança) no registro.</span><span class="sxs-lookup"><span data-stu-id="6ab10-114">The operating system will then be running without the Active Directory, and all user validation occurs through the Security Accounts Manager (SAM) in the registry.</span></span> <span data-ttu-id="6ab10-115">Somente o administrador tem permissão para recuperar o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ab10-115">Only the administrator has permission to recover the Active Directory.</span></span>

<span data-ttu-id="6ab10-116">Uma vez no modo de restauração do serviço de diretório, uma restauração do VSS pode continuar normalmente.</span><span class="sxs-lookup"><span data-stu-id="6ab10-116">Once in Directory Service Restore mode, a VSS restore can proceed normally.</span></span> <span data-ttu-id="6ab10-117">Não há motivo para usar APIs de Active Directory do Win32 não VSS para restaurar o estado de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ab10-117">There is no reason to use non-VSS Win32 Active Directory APIs to restore the Active Directory state.</span></span>

## <a name="active-directory-restores-and-active-directory-tombstones"></a><span data-ttu-id="6ab10-118">Active Directory restaura e Active Directory marcas para exclusão</span><span class="sxs-lookup"><span data-stu-id="6ab10-118">Active Directory Restores and Active Directory Tombstones</span></span>

<span data-ttu-id="6ab10-119">Qualquer plano de recuperação deve garantir que a idade do backup não deve exceder o tempo de vida de Active Directory marca de exclusão (o padrão é 60 dias).</span><span class="sxs-lookup"><span data-stu-id="6ab10-119">Any recovery plan should ensure that the age of the backup should not exceed the Active Directory Tombstone Lifetime (default is 60 days).</span></span>

<span data-ttu-id="6ab10-120">A restauração de um backup mais antigo que a marca para exclusão fará com que um controlador de domínio tenha objetos que não são replicados para os outros servidores.</span><span class="sxs-lookup"><span data-stu-id="6ab10-120">Restoration of a backup older than the tombstone will cause a domain controller to have objects that are not replicated to the other servers.</span></span>

<span data-ttu-id="6ab10-121">Os objetos que não forem replicados não serão excluídos automaticamente nesse controlador de domínio (restaurado) porque as marcas para exclusão desses objetos em outras réplicas já foram excluídas.</span><span class="sxs-lookup"><span data-stu-id="6ab10-121">Those objects that are not replicated will not be deleted automatically on that (restored) domain controller because the tombstones of those objects on the other replicas have already been deleted.</span></span>

<span data-ttu-id="6ab10-122">Um administrador precisará excluir manualmente cada um dos objetos no controlador de domínio restaurado que não são replicados.</span><span class="sxs-lookup"><span data-stu-id="6ab10-122">An administrator will have to manually delete each of the objects on the restored domain controller that are not replicated.</span></span> <span data-ttu-id="6ab10-123">Não há suporte para backups incrementais do Active Directory; um backup completo é necessário.</span><span class="sxs-lookup"><span data-stu-id="6ab10-123">Incremental backups of the Active Directory are not supported; a full backup is required.</span></span>

 

 



