---
description: As operações de backup e restauração do VSS usam um protocolo para a interação dos sistemas que usam gravadores (armazenamento em massa) e os que fazem backup (solicitantes).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Usando o Serviço de Cópias de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501739"
---
# <a name="using-the-volume-shadow-copy-service"></a><span data-ttu-id="a4c11-103">Usando o Serviço de Cópias de Sombra de Volume</span><span class="sxs-lookup"><span data-stu-id="a4c11-103">Using the Volume Shadow Copy Service</span></span>

<span data-ttu-id="a4c11-104">As operações de backup e restauração do VSS usam um protocolo para a interação dos sistemas que usam gravadores (armazenamento em massa) e os que fazem backup (solicitantes).</span><span class="sxs-lookup"><span data-stu-id="a4c11-104">VSS backup and restore operations each use a protocol for the interaction of the systems that use mass storage (writers) and those that back it up (requesters).</span></span>

<span data-ttu-id="a4c11-105">Tanto as operações de backup quanto de restauração são direcionadas principalmente pelo solicitante, que controla o gravador e o comportamento do provedor gerando eventos COM em todo o processador para processar o gravador.</span><span class="sxs-lookup"><span data-stu-id="a4c11-105">Both backup and restore operations are primarily driven by the requester, which controls writer and provider behavior by generating systemwide COM events for the writer to process.</span></span> <span data-ttu-id="a4c11-106">Como os métodos de geração de eventos são assíncronos, os gravadores têm controle limitado no estado do solicitante por meio dos manipuladores assíncronos disponíveis para VSS (consulte [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span><span class="sxs-lookup"><span data-stu-id="a4c11-106">Because event-generating methods are asynchronous, writers do have limited control into the requester's state through the asynchronous handlers available to VSS (see [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span></span>

<span data-ttu-id="a4c11-107">Essa interação requer estruturas de dados básicas que descrevem arquivos e grupos de arquivos ([*componentes*](vssgloss-c.md)), bem como um modelo de metadados para permitir o armazenamento de informações de backup e para permitir a comunicação do gravador/solicitante.</span><span class="sxs-lookup"><span data-stu-id="a4c11-107">This interaction requires basic data structures describing files and groups of files ([*components*](vssgloss-c.md)), as well as a metadata model to allow the storage of backup information and to permit writer/requester communication.</span></span>

-   [<span data-ttu-id="a4c11-108">Compatibilidade do aplicativo VSS</span><span class="sxs-lookup"><span data-stu-id="a4c11-108">VSS Application Compatibility</span></span>](usage-conventions.md)
-   [<span data-ttu-id="a4c11-109">Configurando o VSS</span><span class="sxs-lookup"><span data-stu-id="a4c11-109">Configuring VSS</span></span>](configuring-vss.md)
-   [<span data-ttu-id="a4c11-110">Metadados do VSS</span><span class="sxs-lookup"><span data-stu-id="a4c11-110">VSS Metadata</span></span>](vss-metadata.md)
-   [<span data-ttu-id="a4c11-111">Trabalhando com caminhos lógicos e de seleção</span><span class="sxs-lookup"><span data-stu-id="a4c11-111">Working with Selectability and Logical Paths</span></span>](working-with-selectability-and-logical-paths.md)
-   [<span data-ttu-id="a4c11-112">Visão geral do processamento de um backup no VSS</span><span class="sxs-lookup"><span data-stu-id="a4c11-112">Overview of Processing a Backup Under VSS</span></span>](overview-of-processing-a-backup-under-vss.md)
-   [<span data-ttu-id="a4c11-113">Visão geral do processamento de uma restauração no VSS</span><span class="sxs-lookup"><span data-stu-id="a4c11-113">Overview of Processing a Restore Under VSS</span></span>](overview-of-processing-a-restore-under-vss.md)

 

 



