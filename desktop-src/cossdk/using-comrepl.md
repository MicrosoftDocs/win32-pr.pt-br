---
description: Usando COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Usando COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646434"
---
# <a name="using-comrepl"></a><span data-ttu-id="2ed48-103">Usando COMREPL</span><span class="sxs-lookup"><span data-stu-id="2ed48-103">Using COMREPL</span></span>

<span data-ttu-id="2ed48-104">Para iniciar o utilitário de linha de comando COMREPL, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="2ed48-104">To launch the COMREPL command line utility, use the following steps:</span></span>

1.  <span data-ttu-id="2ed48-105">Adicione% windir% \\ System32 \\ com ao caminho do ambiente padrão digitando o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="2ed48-105">Add %windir%\\system32\\Com to the default environment path by typing the following in the command prompt:</span></span>

    <span data-ttu-id="2ed48-106">**Definir caminho =% PATH%;% WINDIR% \\ System32 \\ com**</span><span class="sxs-lookup"><span data-stu-id="2ed48-106">**set path = %PATH%;%windir%\\system32\\Com**</span></span>

2.  <span data-ttu-id="2ed48-107">Insira o seguinte comando COMREPL:</span><span class="sxs-lookup"><span data-stu-id="2ed48-107">Enter the following COMREPL command:</span></span>

    <span data-ttu-id="2ed48-108">**COMREPL** *sourceComputer* *targetComputerList* **\[ \[ /n \] /v \]**</span><span class="sxs-lookup"><span data-stu-id="2ed48-108">**COMREPL** *sourceComputer* *targetComputerList* **\[/n \[/v\]\]**</span></span>

    <span data-ttu-id="2ed48-109">onde:</span><span class="sxs-lookup"><span data-stu-id="2ed48-109">where:</span></span>

    -   <span data-ttu-id="2ed48-110">*sourceComputer* é o nome do computador da origem</span><span class="sxs-lookup"><span data-stu-id="2ed48-110">*sourceComputer* is the computer name of the source</span></span>

    -   <span data-ttu-id="2ed48-111">*targetComputerList* são os nomes de computador dos destinos separados por espaços</span><span class="sxs-lookup"><span data-stu-id="2ed48-111">*targetComputerList* is the computer names of the targets separated by spaces</span></span>

    -   <span data-ttu-id="2ed48-112">**/n** suprime o prompt de confirmação antes de iniciar a replicação</span><span class="sxs-lookup"><span data-stu-id="2ed48-112">**/n** suppresses confirmation prompt before starting replication</span></span>

    -   <span data-ttu-id="2ed48-113">**/v** ecoa a saída do arquivo de log para o console</span><span class="sxs-lookup"><span data-stu-id="2ed48-113">**/v** echoes log file output to the console</span></span>

## <a name="notes"></a><span data-ttu-id="2ed48-114">Observações</span><span class="sxs-lookup"><span data-stu-id="2ed48-114">Notes</span></span>

-   <span data-ttu-id="2ed48-115">Como o COM+ não é replicado (somente aplicativos e dados de configuração), todos os computadores de destino já devem ter o COM+ instalado.</span><span class="sxs-lookup"><span data-stu-id="2ed48-115">Because COM+ is not replicated (only configuration data and applications), all target computers must already have COM+ installed.</span></span>
-   <span data-ttu-id="2ed48-116">O usuário deve passar as verificações de função para o aplicativo do sistema nos computadores de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="2ed48-116">The user must pass role checks for the system application on both the source and the target computers.</span></span>
-   <span data-ttu-id="2ed48-117">Nenhuma conta de computador local que possa ser usada por funções é replicada.</span><span class="sxs-lookup"><span data-stu-id="2ed48-117">No local machine accounts that may be used by roles are replicated.</span></span>
-   <span data-ttu-id="2ed48-118">O (s) computador (es) de destino devem estar online.</span><span class="sxs-lookup"><span data-stu-id="2ed48-118">The target computer(s) must be online.</span></span>
-   <span data-ttu-id="2ed48-119">O usuário é responsável por replicar todos os dados não-COM + (por exemplo, tabelas de banco de dados, arquivos e assim por diante) para o (s) computador (es) de destino.</span><span class="sxs-lookup"><span data-stu-id="2ed48-119">The user is responsible for replicating all non-COM+ data (for example, database tables, data files, and so forth) to the target computer(s).</span></span>
-   <span data-ttu-id="2ed48-120">Os clusters podem participar da replicação, mas observe que COMREPL replica somente para computadores nomeados.</span><span class="sxs-lookup"><span data-stu-id="2ed48-120">Clusters can participate in replication, but note that COMREPL replicates only to named computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ed48-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ed48-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed48-122">Gerenciamento de Arquivos</span><span class="sxs-lookup"><span data-stu-id="2ed48-122">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="2ed48-123">Registro em log e relatório de erros</span><span class="sxs-lookup"><span data-stu-id="2ed48-123">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="2ed48-124">Fases de replicação</span><span class="sxs-lookup"><span data-stu-id="2ed48-124">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="2ed48-125">O que é replicado</span><span class="sxs-lookup"><span data-stu-id="2ed48-125">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



