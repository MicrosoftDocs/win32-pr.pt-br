---
description: A ação LaunchConditions consulta a tabela LaunchCondition e avalia cada instrução condicional gravada lá. Se qualquer uma dessas instruções condicionais falhar, uma mensagem de erro será exibida para o usuário e a instalação será encerrada.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Ação LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789777"
---
# <a name="launchconditions-action"></a><span data-ttu-id="2ca17-104">Ação LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="2ca17-104">LaunchConditions Action</span></span>

<span data-ttu-id="2ca17-105">A ação LaunchConditions consulta a [tabela LaunchCondition](launchcondition-table.md) e avalia cada instrução condicional gravada lá.</span><span class="sxs-lookup"><span data-stu-id="2ca17-105">The LaunchConditions action queries the [LaunchCondition table](launchcondition-table.md) and evaluates each conditional statement recorded there.</span></span> <span data-ttu-id="2ca17-106">Se qualquer uma dessas instruções condicionais falhar, uma mensagem de erro será exibida para o usuário e a instalação será encerrada.</span><span class="sxs-lookup"><span data-stu-id="2ca17-106">If any of these conditional statements fail, an error message is displayed to the user and the installation is terminated.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2ca17-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="2ca17-107">Sequence Restrictions</span></span>

<span data-ttu-id="2ca17-108">A ação LaunchConditions é opcional.</span><span class="sxs-lookup"><span data-stu-id="2ca17-108">The LaunchConditions action is optional.</span></span> <span data-ttu-id="2ca17-109">Essa ação é normalmente a primeira na sequência, mas a [ação AppSearch](appsearch-action.md) pode ser sequenciada antes da ação LaunchConditions.</span><span class="sxs-lookup"><span data-stu-id="2ca17-109">This action is normally the first in the sequence, but the [AppSearch Action](appsearch-action.md) may be sequenced before the LaunchConditions action.</span></span> <span data-ttu-id="2ca17-110">Se houver condições de inicialização que não se aplicam a todos os modos de instalação, a propriedade de modo de instalação apropriada deverá ser usada em uma expressão condicional na tabela de sequência apropriada.</span><span class="sxs-lookup"><span data-stu-id="2ca17-110">If there are launch conditions that do not apply to all installation modes, the appropriate installation mode property should be used in a conditional expression in the appropriate sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2ca17-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="2ca17-111">ActionData Messages</span></span>

<span data-ttu-id="2ca17-112">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="2ca17-112">There are no ActionData messages.</span></span>

 

 



