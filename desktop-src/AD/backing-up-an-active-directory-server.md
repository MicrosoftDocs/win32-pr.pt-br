---
title: Fazendo backup de um servidor de Active Directory
description: Um backup do Active Directory Server exige que você faça backup do banco de dados e dos logs de transação. Este tópico fornece uma explicação de como um aplicativo de backup faz backup do serviço de diretório Active Directory.
ms.assetid: 250b2f40-6d43-4aa5-a588-b0cd4839828d
ms.tgt_platform: multiple
keywords:
- fazendo backup Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5affde952ee543afe1bb9b794cce074a74382aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004819"
---
# <a name="backing-up-an-active-directory-server"></a><span data-ttu-id="a3b00-105">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3b00-105">Backing Up an Active Directory Server</span></span>

<span data-ttu-id="a3b00-106">Um backup do Active Directory Server exige que você faça backup do banco de dados e dos logs de transação.</span><span class="sxs-lookup"><span data-stu-id="a3b00-106">An Active Directory server backup requires you to back up the database and the transaction logs.</span></span> <span data-ttu-id="a3b00-107">Este tópico fornece uma explicação de como um aplicativo de backup faz backup do serviço de diretório Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3b00-107">This topic provides a walkthrough of how a backup application backs up the Active Directory directory service.</span></span>

<span data-ttu-id="a3b00-108">O chamador dessas funções de backup deve ter o **privilégio \_ \_ nome de backup se** .</span><span class="sxs-lookup"><span data-stu-id="a3b00-108">The caller of these backup functions must have the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="a3b00-109">Você pode usar a função [**DsSetAuthIdentity**](dssetauthidentity.md) para definir o contexto de segurança no qual as funções de backup/restauração do diretório são chamadas.</span><span class="sxs-lookup"><span data-stu-id="a3b00-109">You can use the [**DsSetAuthIdentity**](dssetauthidentity.md) function to set the security context under which the directory backup/restore functions are called.</span></span>

<span data-ttu-id="a3b00-110">**Para fazer backup de um servidor de Active Directory, execute as seguintes etapas**</span><span class="sxs-lookup"><span data-stu-id="a3b00-110">**To backup an Active Directory server, perform the following steps**</span></span>

1.  <span data-ttu-id="a3b00-111">Chame a função [**DsIsNTDSOnline**](dsisntdsonline.md) para determinar se Active Directory Domain Services estão em execução.</span><span class="sxs-lookup"><span data-stu-id="a3b00-111">Call the [**DsIsNTDSOnline**](dsisntdsonline.md) function to determine if Active Directory Domain Services are running.</span></span>
2.  <span data-ttu-id="a3b00-112">Se Active Directory Domain Services estiver em execução, chame a função [**DsBackupPrepare**](dsbackupprepare.md) para inicializar um identificador de contexto de backup.</span><span class="sxs-lookup"><span data-stu-id="a3b00-112">If Active Directory Domain Services are running, call the [**DsBackupPrepare**](dsbackupprepare.md) function to initialize a backup context handle.</span></span> <span data-ttu-id="a3b00-113">Se Active Directory Domain Services não estiverem em execução, não será possível fazer backup dele e o aplicativo de backup deverá falhar na operação de backup.</span><span class="sxs-lookup"><span data-stu-id="a3b00-113">If Active Directory Domain Services are not running, it cannot be backed up and the backup application must fail the backup operation.</span></span>
3.  <span data-ttu-id="a3b00-114">Chame a função [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) para obter uma lista de arquivos para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="a3b00-114">Call the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function to get a list of files to back up.</span></span> <span data-ttu-id="a3b00-115">Para liberar a memória retornada por essa função, chame a função [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b00-115">To release the memory returned by this function, call the [**DsBackupFree**](dsbackupfree.md) function.</span></span>
4.  <span data-ttu-id="a3b00-116">Para cada nome na lista de arquivos retornada, chame a função [**DsBackupOpenFile**](dsbackupopenfile.md) seguida por chamadas repetidas para a função [**DsBackupRead**](dsbackupread.md) até que o arquivo inteiro tenha sido lido.</span><span class="sxs-lookup"><span data-stu-id="a3b00-116">For each name in the returned list of files, call the [**DsBackupOpenFile**](dsbackupopenfile.md) function followed by repeated calls to the [**DsBackupRead**](dsbackupread.md) function until the entire file has been read.</span></span> <span data-ttu-id="a3b00-117">Quando terminar de ler o arquivo, chame a função [**DsBackupClose**](dsbackupclose.md) para fechá-lo.</span><span class="sxs-lookup"><span data-stu-id="a3b00-117">When you have finished reading the file, call the [**DsBackupClose**](dsbackupclose.md) function to close it.</span></span>
5.  <span data-ttu-id="a3b00-118">Depois de fazer backup de todos os arquivos de banco de dados, chame a função [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) para obter uma lista de logs de transação.</span><span class="sxs-lookup"><span data-stu-id="a3b00-118">After all database files are backed up, call the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function to get a list of transaction logs.</span></span> <span data-ttu-id="a3b00-119">Essa lista é tratada da mesma forma que a lista de arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a3b00-119">This list is handled just like the list of database files.</span></span>
6.  <span data-ttu-id="a3b00-120">Quando terminar de fazer backup do log de transações, chame a função [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) para excluir todos os logs de transações confirmados dos quais foi feito backup.</span><span class="sxs-lookup"><span data-stu-id="a3b00-120">When you have finished backing up the transaction log, call the [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) function to delete all committed transaction logs that were backed up.</span></span>
7.  <span data-ttu-id="a3b00-121">Salve o conteúdo do token de expiração fornecido pela função [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b00-121">Save the contents of the expiry token provided by the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span> <span data-ttu-id="a3b00-122">Isso pode ser salvo em um arquivo ou em alguma outra memória persistente.</span><span class="sxs-lookup"><span data-stu-id="a3b00-122">This can be saved in a file or some other persistent memory.</span></span> <span data-ttu-id="a3b00-123">Esse token deve ser passado para a função [**DsRestorePrepare**](dsrestoreprepare.md) para iniciar uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="a3b00-123">This token must be passed to the [**DsRestorePrepare**](dsrestoreprepare.md) function to initiate a restore operation.</span></span>
8.  <span data-ttu-id="a3b00-124">Libere a memória para o token de expiração passando o ponteiro de token para a função [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b00-124">Free the memory for the expiry token by passing the token pointer to the [**DsBackupFree**](dsbackupfree.md) function.</span></span>
9.  <span data-ttu-id="a3b00-125">Por fim, chame a função [**DsBackupEnd**](dsbackupend.md) para liberar todos os recursos associados ao identificador de contexto de backup.</span><span class="sxs-lookup"><span data-stu-id="a3b00-125">Finally, call the [**DsBackupEnd**](dsbackupend.md) function to release all resources associated with the backup context handle.</span></span>

 

 




