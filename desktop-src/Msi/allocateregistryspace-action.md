---
description: A ação AllocateRegistrySpace garante que a quantidade de espaço livre no Registro especificada pela propriedade AVAILABLEFREEREG exista no registro.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Ação AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764669"
---
# <a name="allocateregistryspace-action"></a><span data-ttu-id="cf98a-103">Ação AllocateRegistrySpace</span><span class="sxs-lookup"><span data-stu-id="cf98a-103">AllocateRegistrySpace Action</span></span>

<span data-ttu-id="cf98a-104">A ação AllocateRegistrySpace garante que a quantidade de espaço livre no Registro especificada pela propriedade [**AVAILABLEFREEREG**](availablefreereg.md) exista no registro.</span><span class="sxs-lookup"><span data-stu-id="cf98a-104">The AllocateRegistrySpace action ensures that the amount of free registry space specified by the [**AVAILABLEFREEREG**](availablefreereg.md) property exists in the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cf98a-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="cf98a-105">Sequence Restrictions</span></span>

<span data-ttu-id="cf98a-106">A ação AllocateRegistrySpace deve ser chamada após [InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="cf98a-106">The AllocateRegistrySpace action must be called after [InstallInitialize](installinitialize-action.md).</span></span> <span data-ttu-id="cf98a-107">É aconselhável agendar o AllocateRegistrySpace antes de todas as outras ações para garantir que haja espaço de registro suficiente disponível para continuar.</span><span class="sxs-lookup"><span data-stu-id="cf98a-107">It is advisable to schedule the AllocateRegistrySpace before all other actions to ensure there is enough registry space available to continue.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cf98a-108">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="cf98a-108">ActionData Messages</span></span>



| <span data-ttu-id="cf98a-109">Campo</span><span class="sxs-lookup"><span data-stu-id="cf98a-109">Field</span></span> | <span data-ttu-id="cf98a-110">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="cf98a-110">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="cf98a-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cf98a-111">\[1\]</span></span> | <span data-ttu-id="cf98a-112">Espaço de registro necessário em KB.</span><span class="sxs-lookup"><span data-stu-id="cf98a-112">Registry space required in KB.</span></span> |



 

 

 



