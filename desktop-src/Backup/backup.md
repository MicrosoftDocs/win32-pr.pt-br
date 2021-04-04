---
title: Backup
description: Permitir que aplicativos de backup se comuniquem com outros aplicativos e serviços sobre operações de backup e restauração. Execute o backup em fita, inicialize a fita e recupere as informações da unidade de fita. Manter arquivos duplicados com o SIS (armazenamento de instância única).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- Backup de backup
- Backup de backup, página inicial
- Backup de operações de restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084721"
---
# <a name="backup"></a><span data-ttu-id="b5870-108">Backup</span><span class="sxs-lookup"><span data-stu-id="b5870-108">Backup</span></span>

<span data-ttu-id="b5870-109">As chaves do registro para backup e restauração permitem que aplicativos de backup se comuniquem com outros aplicativos e serviços sobre operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="b5870-109">Registry keys for backup and restore allow backup applications to communicate with other applications and services about backup and restore operations.</span></span> <span data-ttu-id="b5870-110">Para obter mais informações, consulte [chaves e valores do registro para backup e restauração](registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="b5870-110">For more information, see [Registry Keys and Values for Backup and Restore](registry-keys-for-backup-and-restore.md).</span></span>

<span data-ttu-id="b5870-111">A API de backup em fita permite que os aplicativos de backup leiam e gravem em uma fita, inicializem uma fita e recuperem informações de fita ou unidade de fita.</span><span class="sxs-lookup"><span data-stu-id="b5870-111">The tape backup API enables backup applications to read from and write to a tape, initialize a tape, and retrieve tape or tape drive information.</span></span> <span data-ttu-id="b5870-112">Para obter mais informações, consulte [backup em fita](tape-backup.md).</span><span class="sxs-lookup"><span data-stu-id="b5870-112">For more information, see [Tape Backup](tape-backup.md).</span></span>

<span data-ttu-id="b5870-113">O SIS (armazenamento de instância única) é uma arquitetura projetada para manter arquivos duplicados com um mínimo de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="b5870-113">Single-instance store (SIS) is an architecture designed to maintain duplicate files with a minimum of overhead.</span></span> <span data-ttu-id="b5870-114">Aplicativo de backup use a API de backup do SIS para acessar a arquitetura do SIS.</span><span class="sxs-lookup"><span data-stu-id="b5870-114">Backup application use the SIS backup API to access the SIS architecture.</span></span> <span data-ttu-id="b5870-115">Para obter mais informações, consulte [armazenamento de instância única e backup do SIS](single-instance-store-and-sis-backup.md).</span><span class="sxs-lookup"><span data-stu-id="b5870-115">For more information, see [Single-Instance Store and SIS Backup](single-instance-store-and-sis-backup.md).</span></span>

<span data-ttu-id="b5870-116">O backup e a restauração de arquivos criptografados são habilitados pela API de criptografia bruta, que lê e grava arquivos criptografados enquanto mantém os dados em formato criptografado.</span><span class="sxs-lookup"><span data-stu-id="b5870-116">Backup and restore of encrypted files is enabled by the raw encryption API, which reads and writes encrypted files while keeping the data in encrypted format.</span></span> <span data-ttu-id="b5870-117">A API permite que os dados criptografados nesses arquivos sejam armazenados em backup e restaurados, ao mesmo tempo em que atendem às metas de manutenção da segurança dos dados de backup e que podem ser usados por um aplicativo que não tem permissão para usar as chaves de criptografia no arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5870-117">The API allows the encrypted data in these files to be backed up and restored, while meeting the goals of maintaining the security of the backed up data, and being usable by an application that lacks permission to use the encryption keys on the file.</span></span> <span data-ttu-id="b5870-118">Para obter mais informações, consulte [backup e restauração de arquivos criptografados](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span><span class="sxs-lookup"><span data-stu-id="b5870-118">For more information, see [Backup and Restore of Encrypted Files](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span></span>

<span data-ttu-id="b5870-119">A ferramenta Srdelayed pode permitir que aplicativos de recuperação de estado do sistema movam, excluam e definam o nome curto dos arquivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="b5870-119">The Srdelayed tool can enable system state recovery applications to move, delete, and set the short name of system files.</span></span> <span data-ttu-id="b5870-120">Para obter mais informações, consulte [Srdelayed.exe](srdelayed-exe.md).</span><span class="sxs-lookup"><span data-stu-id="b5870-120">For more information, see [Srdelayed.exe](srdelayed-exe.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5870-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5870-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5870-122">Referência de backup</span><span class="sxs-lookup"><span data-stu-id="b5870-122">Backup Reference</span></span>](backup-reference.md)
</dt> </dl>

 

 