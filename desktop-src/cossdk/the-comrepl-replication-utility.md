---
description: COMREPL é um utilitário que replicará o catálogo COM+ de um determinado computador de origem para um ou mais computadores de destino.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: O utilitário de replicação COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920512"
---
# <a name="the-comrepl-replication-utility"></a><span data-ttu-id="27cd8-103">O utilitário de replicação COMREPL</span><span class="sxs-lookup"><span data-stu-id="27cd8-103">The COMREPL Replication Utility</span></span>

<span data-ttu-id="27cd8-104">COMREPL é um utilitário que replicará o catálogo COM+ de um determinado computador de origem para um ou mais computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="27cd8-104">COMREPL is a utility that will replicate the COM+ catalog from a given source computer to one or more target computers.</span></span> <span data-ttu-id="27cd8-105">Imagine o computador de origem que representa uma "configuração mestra".</span><span class="sxs-lookup"><span data-stu-id="27cd8-105">Think of the source computer representing a "master configuration."</span></span> <span data-ttu-id="27cd8-106">COMREPL é usado para replicar essa configuração mestre para manter um conjunto de computadores configurados de forma idêntica.</span><span class="sxs-lookup"><span data-stu-id="27cd8-106">COMREPL is used to replicate this master configuration to maintain a set of identically configured computers.</span></span>

<span data-ttu-id="27cd8-107">A unidade de replicação é a configuração COM+ inteira no computador mestre.</span><span class="sxs-lookup"><span data-stu-id="27cd8-107">The unit of replication is the entire COM+ configuration on the master computer.</span></span> <span data-ttu-id="27cd8-108">Todos os aplicativos COM+ no mestre são replicados para os computadores de destino; é tudo ou nada.</span><span class="sxs-lookup"><span data-stu-id="27cd8-108">All COM+ applications on the master are replicated to the target computers; it's all or nothing.</span></span> <span data-ttu-id="27cd8-109">Além disso, todos os aplicativos COM+ instalados anteriormente nos computadores de destino, com exceção dos aplicativos pré-instalados em COM+, serão excluídos como parte do processo de replicação.</span><span class="sxs-lookup"><span data-stu-id="27cd8-109">In addition, all COM+ applications previously installed on the target computers, with the exception of the COM+ preinstalled applications, will be deleted as part of the replication process.</span></span>

<span data-ttu-id="27cd8-110">COMREPL replica somente os dados de configuração do COM+.</span><span class="sxs-lookup"><span data-stu-id="27cd8-110">COMREPL replicates only COM+ configuration data.</span></span> <span data-ttu-id="27cd8-111">Isso inclui aplicativos COM+ e configurações de computador específicas do COM+.</span><span class="sxs-lookup"><span data-stu-id="27cd8-111">This includes COM+ applications and COM+ specific computer settings.</span></span> <span data-ttu-id="27cd8-112">O Microsoft Serviços de Informações da Internet (IIS) tem um utilitário semelhante (IISSync), que utiliza o COMREPL para replicar a configuração do IIS e do COM+.</span><span class="sxs-lookup"><span data-stu-id="27cd8-112">Microsoft Internet Information Services (IIS) has a similar utility (IISSync), which makes use of COMREPL to replicate IIS and COM+ configuration.</span></span>

<span data-ttu-id="27cd8-113">Para obter informações detalhadas sobre como iniciar e usar o COMREPL, consulte os seguintes tópicos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="27cd8-113">For detailed information on launching and using COMREPL, see the following topics in this section:</span></span>

-   [<span data-ttu-id="27cd8-114">Usando COMREPL</span><span class="sxs-lookup"><span data-stu-id="27cd8-114">Using COMREPL</span></span>](using-comrepl.md)
-   [<span data-ttu-id="27cd8-115">O que é replicado</span><span class="sxs-lookup"><span data-stu-id="27cd8-115">What Gets Replicated</span></span>](what-gets-replicated.md)
-   [<span data-ttu-id="27cd8-116">Fases de replicação</span><span class="sxs-lookup"><span data-stu-id="27cd8-116">Replication Phases</span></span>](replication-phases.md)
-   [<span data-ttu-id="27cd8-117">Gerenciamento de Arquivos</span><span class="sxs-lookup"><span data-stu-id="27cd8-117">File Management</span></span>](file-management.md)
-   [<span data-ttu-id="27cd8-118">Registro em log e relatório de erros</span><span class="sxs-lookup"><span data-stu-id="27cd8-118">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)

## <a name="related-topics"></a><span data-ttu-id="27cd8-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27cd8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27cd8-120">Criando pacotes de instalação para aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="27cd8-120">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="27cd8-121">Implantando proxies de aplicativo</span><span class="sxs-lookup"><span data-stu-id="27cd8-121">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="27cd8-122">O catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="27cd8-122">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



