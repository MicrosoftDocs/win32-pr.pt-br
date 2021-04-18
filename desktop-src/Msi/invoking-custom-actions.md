---
description: As ações personalizadas são invocadas da mesma maneira que as ações padrão, seja por invocação explícita ou durante a execução de uma tabela de sequência.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Invocando ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758623"
---
# <a name="invoking-custom-actions"></a><span data-ttu-id="9cfd4-103">Invocando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="9cfd4-103">Invoking Custom Actions</span></span>

<span data-ttu-id="9cfd4-104">As ações personalizadas são invocadas da mesma maneira que as ações padrão, seja por invocação explícita ou durante a execução de uma tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-104">Custom actions are invoked in the same manner as standard actions, either by explicit invocation or during the execution of a sequence table.</span></span> <span data-ttu-id="9cfd4-105">Há dois métodos para chamar ações:</span><span class="sxs-lookup"><span data-stu-id="9cfd4-105">There are two methods for calling actions:</span></span>

-   <span data-ttu-id="9cfd4-106">Você chama a ação especificada diretamente com a função [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="9cfd4-106">You call the specified action directly with the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span>
-   <span data-ttu-id="9cfd4-107">Uma ação de nível superior chama a tabela de sequência que contém a ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-107">A top-level action calls the sequence table containing the custom action.</span></span> <span data-ttu-id="9cfd4-108">Para obter mais informações sobre como agendar uma ação personalizada em uma tabela de sequência, consulte [sequenciando ações personalizadas](sequencing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9cfd4-108">For more information about scheduling a custom action in a sequence table, see [Sequencing Custom Actions](sequencing-custom-actions.md).</span></span>

<span data-ttu-id="9cfd4-109">Quando o instalador obtém um nome de ação da função [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou de uma tabela de sequência, ele primeiro procura uma ação padrão desse nome.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-109">When the installer obtains an action name from the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function, or from a sequence table, it first searches for a standard action of that name.</span></span> <span data-ttu-id="9cfd4-110">Se não for possível localizar a ação padrão, o instalador consultará a [tabela CustomAction](customaction-table.md) para verificar se a ação especificada é uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-110">If it cannot find the standard action, then the installer queries the [CustomAction table](customaction-table.md) to check if the specified action is a custom action.</span></span> <span data-ttu-id="9cfd4-111">Se a ação especificada não for uma ação personalizada, o instalador consultará a [tabela de diálogo](dialog-table.md) em busca de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-111">If the specified action is not a custom action, then the installer queries the [Dialog table](dialog-table.md) for a dialog box.</span></span>

 

 



