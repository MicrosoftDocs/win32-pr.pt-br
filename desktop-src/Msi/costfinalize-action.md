---
description: A ação CostFinalize encerra o processo de custo de instalação interno iniciado pela ação CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Ação CostFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755087"
---
# <a name="costfinalize-action"></a><span data-ttu-id="e3d93-103">Ação CostFinalize</span><span class="sxs-lookup"><span data-stu-id="e3d93-103">CostFinalize Action</span></span>

<span data-ttu-id="e3d93-104">A ação CostFinalize encerra o processo de [*custo*](c-gly.md) de instalação interno iniciado pela ação [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e3d93-104">The CostFinalize action ends the internal installation [*costing*](c-gly.md) process begun by the [CostInitialize](costinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e3d93-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="e3d93-105">Sequence Restrictions</span></span>

<span data-ttu-id="e3d93-106">Todas as ações padrão ou [personalizadas](custom-actions.md) que afetam o custo devem ser sequenciadas antes da ação [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e3d93-106">Any standard or [custom actions](custom-actions.md) that affect costing should be sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="e3d93-107">Chame a ação [filecost](filecost-action.md) imediatamente após a ação CostInitialize e, em seguida, chame a ação CostFinalize para disponibilizar todos os cálculos de custo final para o instalador por meio da tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e3d93-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action and then call the CostFinalize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="e3d93-108">A ação CostFinalize deve ser executada antes de iniciar qualquer sequência de interface do usuário que permita ao usuário exibir ou modificar as seleções ou diretórios de tabela de [recursos](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e3d93-108">The CostFinalize action must be executed before starting any user interface sequence which allows the user to view or modify [Feature](feature-table.md) table selections or directories.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e3d93-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="e3d93-109">ActionData Messages</span></span>

<span data-ttu-id="e3d93-110">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="e3d93-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3d93-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3d93-111">Remarks</span></span>

<span data-ttu-id="e3d93-112">A ação CostFinalize consulta a tabela de [condição](condition-table.md) para determinar quais recursos estão agendados para instalação.</span><span class="sxs-lookup"><span data-stu-id="e3d93-112">The CostFinalize action queries the [Condition](condition-table.md) table to determine which features are scheduled to be installed.</span></span> <span data-ttu-id="e3d93-113">O custo é feito para cada componente na tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e3d93-113">Costing is done for each component in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="e3d93-114">A ação CostFinalize também verifica se todos os diretórios de destino são graváveis antes de permitir que a instalação continue.</span><span class="sxs-lookup"><span data-stu-id="e3d93-114">The CostFinalize action also verifies that all the target directories are writable before allowing the installation to continue.</span></span>

> [!Note]  
> <span data-ttu-id="e3d93-115">Durante uma [instalação administrativa](administrative-installation.md), o CostFinalize define todos os recursos para instalação, exceto os recursos com 0 criados na coluna nível da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e3d93-115">During an [administrative installation](administrative-installation.md), CostFinalize sets all features for installation except features having 0 authored in the Level column of the [Feature table](feature-table.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e3d93-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3d93-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3d93-117">Custo do arquivo</span><span class="sxs-lookup"><span data-stu-id="e3d93-117">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



