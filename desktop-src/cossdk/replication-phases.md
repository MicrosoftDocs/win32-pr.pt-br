---
description: COMREPL faz seu trabalho em três fases.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fases de replicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813763"
---
# <a name="replication-phases"></a><span data-ttu-id="130b8-103">Fases de replicação</span><span class="sxs-lookup"><span data-stu-id="130b8-103">Replication Phases</span></span>

<span data-ttu-id="130b8-104">COMREPL faz seu trabalho em três fases.</span><span class="sxs-lookup"><span data-stu-id="130b8-104">COMREPL does its work in three phases.</span></span> <span data-ttu-id="130b8-105">O processo de replicação é dividido em fases distintas pelos dois motivos a seguir:</span><span class="sxs-lookup"><span data-stu-id="130b8-105">The replication process is divided into distinct phases for the following two reasons:</span></span>

-   <span data-ttu-id="130b8-106">Para separar o trabalho feito para preparar a origem do trabalho que é feito em cada destino</span><span class="sxs-lookup"><span data-stu-id="130b8-106">To separate work done to prepare the source from work that is done on each target</span></span>
-   <span data-ttu-id="130b8-107">Para atrasar a modificação do destino até que todos os dados tenham sido adquiridos da origem</span><span class="sxs-lookup"><span data-stu-id="130b8-107">To delay modification of the target until all data has been acquired from the source</span></span>

<span data-ttu-id="130b8-108">As fases de replicação são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="130b8-108">The replication phases are as follows.</span></span>



| <span data-ttu-id="130b8-109">Fase</span><span class="sxs-lookup"><span data-stu-id="130b8-109">Phase</span></span>         | <span data-ttu-id="130b8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="130b8-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="130b8-111">Fase de preparo</span><span class="sxs-lookup"><span data-stu-id="130b8-111">Prepare phase</span></span> | <span data-ttu-id="130b8-112">Exporta todos os aplicativos instalados localmente no computador de origem.</span><span class="sxs-lookup"><span data-stu-id="130b8-112">Exports all the installed applications locally on the source computer.</span></span> <span data-ttu-id="130b8-113">Essa fase não toca na configuração de nenhum destino.</span><span class="sxs-lookup"><span data-stu-id="130b8-113">This phase does not touch the configuration of any targets.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="130b8-114">Fase de cópia</span><span class="sxs-lookup"><span data-stu-id="130b8-114">Copy phase</span></span>    | <span data-ttu-id="130b8-115">Copia dados para um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="130b8-115">Copies data to a target computer.</span></span> <span data-ttu-id="130b8-116">Todos os aplicativos exportados na origem são copiados para o destino.</span><span class="sxs-lookup"><span data-stu-id="130b8-116">All applications exported on the source are copied to the target.</span></span> <span data-ttu-id="130b8-117">Esta é uma operação de cópia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="130b8-117">This is a file copy operation.</span></span> <span data-ttu-id="130b8-118">(Consulte [Gerenciamento de arquivos](file-management.md).) Essa etapa também adquire alguns dados do computador de origem que não estão encapsulados em arquivos de aplicativo exportados (por exemplo, identidades de aplicativo).</span><span class="sxs-lookup"><span data-stu-id="130b8-118">(See [File Management](file-management.md).) This step also acquires some data from the source computer that is not encapsulated within exported application files (for example, application identities).</span></span> <span data-ttu-id="130b8-119">Esses dados são mantidos na memória no COMREPL.</span><span class="sxs-lookup"><span data-stu-id="130b8-119">This data is held in memory within COMREPL.</span></span> <span data-ttu-id="130b8-120">Essa fase não toca na configuração de nenhum computador de destino.</span><span class="sxs-lookup"><span data-stu-id="130b8-120">This phase does not touch the configuration of any target computers.</span></span>                                                                               |
| <span data-ttu-id="130b8-121">Fase de instalação</span><span class="sxs-lookup"><span data-stu-id="130b8-121">Install phase</span></span> | <span data-ttu-id="130b8-122">Instala o catálogo de origem em um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="130b8-122">Installs source catalog on a target computer.</span></span> <span data-ttu-id="130b8-123">Quando essa etapa é iniciada, todos os dados necessários para reconfigurar o destino estão dentro dos arquivos de aplicativo no sistema de arquivos do destino ou são mantidos como dados de instância no COMREPL.</span><span class="sxs-lookup"><span data-stu-id="130b8-123">When this step is initiated, all data required to reconfigure the target is within application files in the target's file system or is held as instance data within COMREPL.</span></span> <span data-ttu-id="130b8-124">Esta fase excluirá todos os aplicativos instalados no destino (exceto os aplicativos descritos em [o que é replicado](what-gets-replicated.md)) antes da instalação dos aplicativos copiados da origem.</span><span class="sxs-lookup"><span data-stu-id="130b8-124">This phase will delete all the installed applications on the target (except the applications described in [What Gets Replicated](what-gets-replicated.md)) prior to installing the applications copied from the source.</span></span> <span data-ttu-id="130b8-125">O COMREPL é instalado em vários destinos simultaneamente usando um thread de instalação por destino.</span><span class="sxs-lookup"><span data-stu-id="130b8-125">COMREPL installs on multiple targets concurrently by using an install thread per target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="130b8-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="130b8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="130b8-127">Gerenciamento de Arquivos</span><span class="sxs-lookup"><span data-stu-id="130b8-127">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="130b8-128">Registro em log e relatório de erros</span><span class="sxs-lookup"><span data-stu-id="130b8-128">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="130b8-129">Usando COMREPL</span><span class="sxs-lookup"><span data-stu-id="130b8-129">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="130b8-130">O que é replicado</span><span class="sxs-lookup"><span data-stu-id="130b8-130">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



