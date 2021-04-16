---
description: O valor lógico de uma propriedade que foi definida é true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Usando propriedades em instruções condicionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787058"
---
# <a name="using-properties-in-conditional-statements"></a><span data-ttu-id="f625d-103">Usando propriedades em instruções condicionais</span><span class="sxs-lookup"><span data-stu-id="f625d-103">Using Properties in Conditional Statements</span></span>

<span data-ttu-id="f625d-104">O valor lógico de uma propriedade que foi definida é true.</span><span class="sxs-lookup"><span data-stu-id="f625d-104">The logical value of a property that has been set is True.</span></span> <span data-ttu-id="f625d-105">Para determinar se uma propriedade está definida sem realmente obter seu valor, teste a expressão lógica "MyProperty" ou "not MyProperty".</span><span class="sxs-lookup"><span data-stu-id="f625d-105">To determine whether a property is set without actually getting its value, test the logical expression "MyProperty" or "Not MyProperty".</span></span> <span data-ttu-id="f625d-106">Quando a propriedade MyProperty é definida, a anterior é avaliada como true e a última como false.</span><span class="sxs-lookup"><span data-stu-id="f625d-106">When the property MyProperty is set, the former evaluates as True and the latter as False.</span></span>

<span data-ttu-id="f625d-107">Uma ou mais propriedades podem ser combinadas com operadores para formar expressões lógicas usadas em instruções condicionais.</span><span class="sxs-lookup"><span data-stu-id="f625d-107">One or more properties can be combined with operators to form logical expressions used in a conditional statements.</span></span> <span data-ttu-id="f625d-108">Para obter mais informações sobre os operadores que podem ser usados em instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f625d-108">For more information about the operators that can be used in conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="f625d-109">Uma instrução condicional que usa propriedades pode ser inserida na coluna condição da [tabela condição](condition-table.md) para modificar o estado de seleção de qualquer entrada na [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f625d-109">A conditional statement using properties can be entered into the Condition column of the [Condition table](condition-table.md) to modify the selection state of any entry in the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="f625d-110">Instruções condicionais com uma ou mais propriedades são geralmente usadas na coluna condição de tabelas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f625d-110">Conditional statements with one or more properties are commonly used in the Condition column of database tables.</span></span>

<span data-ttu-id="f625d-111">As tabelas a seguir têm uma coluna para expressões condicionais:</span><span class="sxs-lookup"><span data-stu-id="f625d-111">The following tables each have a column for conditional expressions:</span></span>

-   [<span data-ttu-id="f625d-112">Tabela de condição</span><span class="sxs-lookup"><span data-stu-id="f625d-112">Condition table</span></span>](condition-table.md)
-   [<span data-ttu-id="f625d-113">Tabela ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="f625d-113">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="f625d-114">Tabela LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="f625d-114">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="f625d-115">Tabela InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="f625d-115">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="f625d-116">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f625d-116">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="f625d-117">Tabela ControlCondition</span><span class="sxs-lookup"><span data-stu-id="f625d-117">ControlCondition table</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="f625d-118">Tabela AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f625d-118">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="f625d-119">Tabela AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f625d-119">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="f625d-120">Tabela AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="f625d-120">AdminUISequence table</span></span>](adminuisequence-table.md)

<span data-ttu-id="f625d-121">Observe que as seis tabelas de sequência de ação têm campos para uma condição.</span><span class="sxs-lookup"><span data-stu-id="f625d-121">Note that the six action sequence tables have fields for a condition.</span></span> <span data-ttu-id="f625d-122">Se a expressão condicional nesse campo for avaliada como false, o instalador ignorará essa ação.</span><span class="sxs-lookup"><span data-stu-id="f625d-122">If the conditional expression in this field evaluates to False, the installer skips that action.</span></span>

<span data-ttu-id="f625d-123">Se você definir uma [propriedade privada](private-properties.md) na sequência da interface do usuário criando uma ação personalizada em uma das tabelas de sequência da interface do usuário, essa propriedade não será definida na sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="f625d-123">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="f625d-124">Para definir a propriedade na sequência de execução, você também deve colocar uma ação personalizada em uma tabela de sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="f625d-124">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="f625d-125">Como alternativa, você pode tornar a propriedade uma [propriedade pública](public-properties.md) e incluí-la na propriedade [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="f625d-125">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="f625d-126">Para obter mais informações, consulte [usando uma tabela de sequência](using-a-sequence-table.md) ou [usando Propriedades](using-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f625d-126">For more information, see [Using a Sequence Table](using-a-sequence-table.md) or [Using Properties](using-properties.md).</span></span>

 

 



