---
description: A ação CostInitialize inicia o processo de custos de instalação.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Ação CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768475"
---
# <a name="costinitialize-action"></a><span data-ttu-id="aa019-103">Ação CostInitialize</span><span class="sxs-lookup"><span data-stu-id="aa019-103">CostInitialize Action</span></span>

<span data-ttu-id="aa019-104">A ação CostInitialize inicia o processo de [*custos*](c-gly.md) de instalação.</span><span class="sxs-lookup"><span data-stu-id="aa019-104">The CostInitialize action initiates the installation [*costing*](c-gly.md) process.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="aa019-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="aa019-105">Sequence Restrictions</span></span>

<span data-ttu-id="aa019-106">Todas as ações padrão ou [personalizadas](custom-actions.md) que afetam o custo devem ser sequenciadas antes da ação CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="aa019-106">Any standard or [custom](custom-actions.md) actions that affect costing should be sequenced before the CostInitialize action.</span></span> <span data-ttu-id="aa019-107">Chame a ação [filecost](filecost-action.md) imediatamente após a ação CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="aa019-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action.</span></span> <span data-ttu-id="aa019-108">Em seguida, chame a ação [CostFinalize](costfinalize-action.md) seguindo a ação de ação CostInitialize para disponibilizar todos os cálculos de custo final para o instalador por meio da tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="aa019-108">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="aa019-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="aa019-109">ActionData Messages</span></span>

<span data-ttu-id="aa019-110">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="aa019-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa019-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa019-111">Remarks</span></span>

<span data-ttu-id="aa019-112">A ação CostInitialize carrega a tabela de componentes e a tabela de [recursos](feature-table.md) na memória.</span><span class="sxs-lookup"><span data-stu-id="aa019-112">The CostInitialize action loads the Component table and [Feature](feature-table.md) table into memory.</span></span>

<span data-ttu-id="aa019-113">Para obter mais informações sobre o processo de [*custos*](c-gly.md) no instalador, consulte [custos de arquivo](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="aa019-113">For more information on the [*costing*](c-gly.md) process in the installer, see [File Costing](file-costing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa019-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa019-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa019-115">Custo do arquivo</span><span class="sxs-lookup"><span data-stu-id="aa019-115">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



