---
description: As funções do instalador podem ser usadas para executar ações específicas ou sequências de ação.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Executando ações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766862"
---
# <a name="running-actions"></a><span data-ttu-id="1ee69-103">Executando ações</span><span class="sxs-lookup"><span data-stu-id="1ee69-103">Running Actions</span></span>

<span data-ttu-id="1ee69-104">As funções do instalador podem ser usadas para executar ações específicas ou sequências de ação.</span><span class="sxs-lookup"><span data-stu-id="1ee69-104">The installer functions can be used to run specific actions or action sequences.</span></span> <span data-ttu-id="1ee69-105">Essas ações podem ser ações [padrão](standard-actions.md) ou [personalizadas](custom-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee69-105">These actions can either be [standard](standard-actions.md) or [custom](custom-actions.md) actions.</span></span> <span data-ttu-id="1ee69-106">O procedimento a seguir descreve como executar ações:</span><span class="sxs-lookup"><span data-stu-id="1ee69-106">The following procedure describes how to run actions:</span></span>

<span data-ttu-id="1ee69-107">**Para executar uma sequência de ação**</span><span class="sxs-lookup"><span data-stu-id="1ee69-107">**To run an action sequence**</span></span>

1.  <span data-ttu-id="1ee69-108">Execute uma sequência de ações definidas em uma tabela chamando a função [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .</span><span class="sxs-lookup"><span data-stu-id="1ee69-108">Run a sequence of actions defined in a table by calling the [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) function.</span></span>

    <span data-ttu-id="1ee69-109">O instalador consulta a tabela indicada e executa cada ação se sua expressão condicional for avaliada como TRUE.</span><span class="sxs-lookup"><span data-stu-id="1ee69-109">The installer queries the indicated table and runs each action if its conditional expression evaluates to TRUE.</span></span>

2.  <span data-ttu-id="1ee69-110">Verifique expressões condicionais chamando a função [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="1ee69-110">Check conditional expressions by calling the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>
3.  <span data-ttu-id="1ee69-111">Execute a ação chamando a função [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="1ee69-111">Run the action by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span> <span data-ttu-id="1ee69-112">A ação pode ser uma ação padrão, uma ação personalizada ou uma caixa de diálogo de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1ee69-112">The action can be a standard action, a custom action, or a user interface dialog box.</span></span>
4.  <span data-ttu-id="1ee69-113">Se ocorrer um erro durante a execução dessa ação, chame a função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="1ee69-113">If an error occurred during the execution of this action, call the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="1ee69-114">O instalador processará o erro.</span><span class="sxs-lookup"><span data-stu-id="1ee69-114">The installer will process the error.</span></span>

 

 



