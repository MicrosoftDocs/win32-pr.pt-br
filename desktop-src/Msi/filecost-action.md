---
description: O filecustoaction inicia as ações de instalação padrão do Dynamic costingof.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Ação de custo de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011875"
---
# <a name="filecost-action"></a><span data-ttu-id="40087-103">Ação de custo de</span><span class="sxs-lookup"><span data-stu-id="40087-103">FileCost Action</span></span>

<span data-ttu-id="40087-104">O filecustaaction inicia o [*custo*](c-gly.md)dinâmico das ações de instalação padrão.</span><span class="sxs-lookup"><span data-stu-id="40087-104">The FileCostaction initiates dynamic [*costing*](c-gly.md)of standard installation actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="40087-105">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="40087-105">ActionData Messages</span></span>

<span data-ttu-id="40087-106">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="40087-106">There are no ActionData messages.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="40087-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="40087-107">Sequence Restrictions</span></span>

<span data-ttu-id="40087-108">Todas as ações padrão ou [personalizadas](custom-actions.md) que afetam o custo devem ser sequenciadas antes da ação [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="40087-108">Any standard or [custom actions](custom-actions.md) that affect costing should sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="40087-109">Chame a ação filecost imediatamente após a ação CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="40087-109">Call the FileCost action immediately following the CostInitialize action.</span></span> <span data-ttu-id="40087-110">Em seguida, chame a ação [CostFinalize](costfinalize-action.md) após a ação CostInitialize para disponibilizar todos os cálculos de custo final para o instalador por meio da tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="40087-110">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="40087-111">A ação [CostInitialize](costinitialize-action.md) deve ser executada antes da ação filecost.</span><span class="sxs-lookup"><span data-stu-id="40087-111">The [CostInitialize](costinitialize-action.md) action must be executed before the FileCost action.</span></span> <span data-ttu-id="40087-112">Em seguida, o instalador determina o custo de espaço em disco de cada arquivo na tabela de [arquivos](file-table.md) , em uma base por componente (consulte a [tabela de componentes](component-table.md)), levando o clustering de [*volume*](v-gly.md) e a presença de arquivos existentes que talvez precisem ser substituídos em conta.</span><span class="sxs-lookup"><span data-stu-id="40087-112">The installer then determines the disk-space cost of every file in the [File](file-table.md) table, on a per-component basis (See [Component Table](component-table.md)), taking both [*volume*](v-gly.md) clustering and the presence of existing files that may need to be overwritten into account.</span></span> <span data-ttu-id="40087-113">Todas as ações que consomem ou liberam espaço em disco também são consideradas.</span><span class="sxs-lookup"><span data-stu-id="40087-113">All actions that consume or release disk space are also considered.</span></span> <span data-ttu-id="40087-114">Se um arquivo existente for encontrado, uma verificação de versão de arquivo será executada para determinar se o novo arquivo realmente precisa ser instalado ou não.</span><span class="sxs-lookup"><span data-stu-id="40087-114">If an existing file is found, a file version check is performed to determine whether the new file actually needs to be installed or not.</span></span> <span data-ttu-id="40087-115">Se o arquivo existente for de um número de versão igual ou maior, o arquivo existente não será substituído e nenhum custo de espaço em disco será incorrido.</span><span class="sxs-lookup"><span data-stu-id="40087-115">If the existing file is of an equal or greater version number, the existing file is not overwritten and no disk-space cost is incurred.</span></span> <span data-ttu-id="40087-116">Em todos os casos, o instalador usa os resultados da verificação de número de versão para definir o estado de instalação de cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="40087-116">In all cases, the installer uses the results of version number checking to set the installation state of each file.</span></span>

<span data-ttu-id="40087-117">A ação filecusto Inicializa o cálculo de custos com o instalador.</span><span class="sxs-lookup"><span data-stu-id="40087-117">The FileCost action initializes cost calculation with theinstaller.</span></span> <span data-ttu-id="40087-118">O [*custo*](c-gly.md) dinâmico real não ocorre até que a ação [CostFinalize](costfinalize-action.md) seja executada.</span><span class="sxs-lookup"><span data-stu-id="40087-118">Actual dynamic [*costing*](c-gly.md) does not occur until the [CostFinalize](costfinalize-action.md) action is executed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40087-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40087-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40087-120">Custo do arquivo</span><span class="sxs-lookup"><span data-stu-id="40087-120">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



