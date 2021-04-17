---
description: As operações de backup e restauração normalmente copiam arquivos de um local padrão específico no disco para a mídia de backup e, em seguida, restauram essa mídia para o mesmo local padrão no disco.
ms.assetid: 7609c392-d5f8-48c2-8e7e-f35f56cf94f8
title: Locais de backup e restauração não padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c809b886886c1d84de1cc3960163a7cc94179cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811385"
---
# <a name="non-default-backup-and-restore-locations"></a><span data-ttu-id="e96af-103">Locais de backup e restauração não padrão</span><span class="sxs-lookup"><span data-stu-id="e96af-103">Non-Default Backup and Restore Locations</span></span>

<span data-ttu-id="e96af-104">As operações de backup e restauração normalmente copiam arquivos de um local padrão específico no disco para a mídia de backup e, em seguida, restauram essa mídia para o mesmo local padrão no disco.</span><span class="sxs-lookup"><span data-stu-id="e96af-104">Backup and restore operations typically copy files from a given, default location on disk to backup media and then restore from that media to the same default location on disk.</span></span>

<span data-ttu-id="e96af-105">Há muitas razões, especialmente ao lidar com processos em execução, não seguir este modelo simples.</span><span class="sxs-lookup"><span data-stu-id="e96af-105">There are many reasons, particularly when dealing with running processes, not to follow this simple model.</span></span> <span data-ttu-id="e96af-106">O VSS dá suporte ao uso de fontes não padrão para backup e destinos alternativos para restauração e inclui mecanismos para trabalhar com subconjuntos de arquivos e remapear arquivos.</span><span class="sxs-lookup"><span data-stu-id="e96af-106">VSS supports using nonstandard sources for backup and alternate destinations for restore, and includes mechanisms to work with subsets of files and to remap files.</span></span>

-   [<span data-ttu-id="e96af-107">Trabalhando com caminhos alternativos durante o backup</span><span class="sxs-lookup"><span data-stu-id="e96af-107">Working with Alternate Paths during Backup</span></span>](working-with-alternate-paths-during-backup.md)
-   [<span data-ttu-id="e96af-108">Trabalhando com locais alternativos durante a restauração</span><span class="sxs-lookup"><span data-stu-id="e96af-108">Working with Alternate Locations during Restore</span></span>](working-with-alternate-locations-during-restore.md)
-   [<span data-ttu-id="e96af-109">Trabalhando com novos destinos durante a restauração</span><span class="sxs-lookup"><span data-stu-id="e96af-109">Working with New Targets during Restore</span></span>](working-with-new-targets-during-restore.md)
-   [<span data-ttu-id="e96af-110">Trabalhando com arquivos parciais</span><span class="sxs-lookup"><span data-stu-id="e96af-110">Working with Partial Files</span></span>](working-with-partial-files.md)
-   [<span data-ttu-id="e96af-111">Trabalhando com destinos direcionados</span><span class="sxs-lookup"><span data-stu-id="e96af-111">Working with Directed Targets</span></span>](working-with-directed-targets.md)

 

 



