---
description: Para habilitar a transferência de arquivos de aplicativo, o COMREPL gerencia automaticamente conjuntos de pastas de sistema de arquivos na origem e no destino. Essas pastas COMREPL estão todas com raiz na replicação com% systemdir% \\ \\ .
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Gerenciamento de arquivos (serviços de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500894"
---
# <a name="file-management"></a><span data-ttu-id="457bc-104">Gerenciamento de Arquivos</span><span class="sxs-lookup"><span data-stu-id="457bc-104">File Management</span></span>

<span data-ttu-id="457bc-105">Para habilitar a transferência de arquivos de aplicativo, o COMREPL gerencia automaticamente conjuntos de pastas de sistema de arquivos na origem e no destino.</span><span class="sxs-lookup"><span data-stu-id="457bc-105">To enable the transfer of application files, COMREPL automatically manages sets of file system folders on the source and target.</span></span> <span data-ttu-id="457bc-106">Essas pastas COMREPL estão todas com raiz na replicação com% systemdir% \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="457bc-106">These COMREPL folders are all rooted in %systemdir%\\com\\replication.</span></span>

## <a name="source-folders"></a><span data-ttu-id="457bc-107">Pastas de origem</span><span class="sxs-lookup"><span data-stu-id="457bc-107">Source folders</span></span>



| <span data-ttu-id="457bc-108">Pasta</span><span class="sxs-lookup"><span data-stu-id="457bc-108">Folder</span></span>                   | <span data-ttu-id="457bc-109">Finalidade</span><span class="sxs-lookup"><span data-stu-id="457bc-109">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="457bc-110">Replicar</span><span class="sxs-lookup"><span data-stu-id="457bc-110">ReplicaSource</span></span><br/> | <span data-ttu-id="457bc-111">Os aplicativos exportados durante a fase de preparação são armazenados aqui.</span><span class="sxs-lookup"><span data-stu-id="457bc-111">Applications exported during the prepare phase are stored here.</span></span><br/> <span data-ttu-id="457bc-112">Essa pasta é substituída sempre que a fase de preparação é executada em um determinado computador de origem.</span><span class="sxs-lookup"><span data-stu-id="457bc-112">This folder is overwritten each time the prepare phase is executed against a given source computer.</span></span> <span data-ttu-id="457bc-113">Essa pasta nunca é excluída explicitamente, portanto, a replicação para destinos pode ocorrer a qualquer momento depois que a origem é preparada.</span><span class="sxs-lookup"><span data-stu-id="457bc-113">This folder is never explicitly deleted, so replication to targets can take place at any time after the source is prepared.</span></span><br/> <span data-ttu-id="457bc-114">Cada aplicativo é armazenado em sua própria subpasta denominada <appName> + <appID> .</span><span class="sxs-lookup"><span data-stu-id="457bc-114">Each application is stored in its own subfolder named <appName>+<appID>.</span></span><br/> |



 

## <a name="target-folders"></a><span data-ttu-id="457bc-115">Pastas de destino</span><span class="sxs-lookup"><span data-stu-id="457bc-115">Target folders</span></span>



| <span data-ttu-id="457bc-116">Pasta</span><span class="sxs-lookup"><span data-stu-id="457bc-116">Folder</span></span>                    | <span data-ttu-id="457bc-117">Finalidade</span><span class="sxs-lookup"><span data-stu-id="457bc-117">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="457bc-118">ReplicaNew</span><span class="sxs-lookup"><span data-stu-id="457bc-118">ReplicaNew</span></span><br/>     | <span data-ttu-id="457bc-119">A fase de cópia copia todos os arquivos e subpastas de Réplicaname na origem para ReplicaNew no destino.</span><span class="sxs-lookup"><span data-stu-id="457bc-119">The copy phase copies all files and subfolders from ReplicaSource on the source to ReplicaNew on the target.</span></span> <span data-ttu-id="457bc-120">Qualquer conteúdo anterior de ReplicaNew é excluído sempre que a fase de cópia é executada em relação a um determinado destino.</span><span class="sxs-lookup"><span data-stu-id="457bc-120">Any previous contents of ReplicaNew are deleted each time the copy phase is run against a given target.</span></span><br/> <span data-ttu-id="457bc-121">Essa pasta só existe enquanto o processo de replicação está em execução.</span><span class="sxs-lookup"><span data-stu-id="457bc-121">This folder exists only while the replication process is running.</span></span> <span data-ttu-id="457bc-122">(Consulte ReplicaCurrent.)</span><span class="sxs-lookup"><span data-stu-id="457bc-122">(See ReplicaCurrent.)</span></span><br/>           |
| <span data-ttu-id="457bc-123">ReplicaCurrent</span><span class="sxs-lookup"><span data-stu-id="457bc-123">ReplicaCurrent</span></span><br/> | <span data-ttu-id="457bc-124">Os aplicativos replicados atualmente instalados no destino são armazenados aqui.</span><span class="sxs-lookup"><span data-stu-id="457bc-124">The replicated applications currently installed on the target are stored here.</span></span><br/> <span data-ttu-id="457bc-125">Quando a fase de instalação é iniciada, a pasta ReplicaNew é renomeada como ReplicaCurrent.</span><span class="sxs-lookup"><span data-stu-id="457bc-125">When the install phase is started, the ReplicaNew folder is renamed to ReplicaCurrent.</span></span> <span data-ttu-id="457bc-126">Se houver uma pasta ReplicaCurrent existente, ela será renomeada para ReplicaOld.</span><span class="sxs-lookup"><span data-stu-id="457bc-126">If there is an existing ReplicaCurrent folder, it is renamed to ReplicaOld.</span></span> <span data-ttu-id="457bc-127">Se houver uma pasta ReplicaOld existente, seu conteúdo será excluído.</span><span class="sxs-lookup"><span data-stu-id="457bc-127">If there is an existing ReplicaOld folder, its contents are deleted.</span></span><br/> |
| <span data-ttu-id="457bc-128">ReplicaOld</span><span class="sxs-lookup"><span data-stu-id="457bc-128">ReplicaOld</span></span><br/>     | <span data-ttu-id="457bc-129">Salva os arquivos de aplicativo instalados durante o próximo à última replicação.</span><span class="sxs-lookup"><span data-stu-id="457bc-129">Saves the application files installed during the next to last replication.</span></span> <span data-ttu-id="457bc-130">Esses arquivos são salvos somente para fins de backup.</span><span class="sxs-lookup"><span data-stu-id="457bc-130">These files are saved for backup purposes only.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="457bc-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="457bc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="457bc-132">Registro em log e relatório de erros</span><span class="sxs-lookup"><span data-stu-id="457bc-132">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="457bc-133">Fases de replicação</span><span class="sxs-lookup"><span data-stu-id="457bc-133">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="457bc-134">Usando COMREPL</span><span class="sxs-lookup"><span data-stu-id="457bc-134">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="457bc-135">O que é replicado</span><span class="sxs-lookup"><span data-stu-id="457bc-135">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 




