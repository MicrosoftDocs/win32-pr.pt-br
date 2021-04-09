---
description: A ação InstallExecuteAgain executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação de InstallExecuteAgain ou a última ação de InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Ação InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920833"
---
# <a name="installexecuteagain-action"></a><span data-ttu-id="165f8-103">Ação InstallExecuteAgain</span><span class="sxs-lookup"><span data-stu-id="165f8-103">InstallExecuteAgain Action</span></span>

<span data-ttu-id="165f8-104">A ação InstallExecuteAgain executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação de InstallExecuteAgain ou a última [ação de InstallExecute](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="165f8-104">The InstallExecuteAgain action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecuteAgain action or the last [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="165f8-105">A ação InstallExecute atualiza o sistema sem encerrar a transação.</span><span class="sxs-lookup"><span data-stu-id="165f8-105">The InstallExecute action updates the system without ending the transaction.</span></span> <span data-ttu-id="165f8-106">InstallExecuteAgain executa a mesma operação que a [ação InstallExecute](installexecute-action.md) , mas só deve ser usada após InstallExecute.</span><span class="sxs-lookup"><span data-stu-id="165f8-106">InstallExecuteAgain performs the same operation as the [InstallExecute action](installexecute-action.md) but should only be used after InstallExecute.</span></span>

<span data-ttu-id="165f8-107">InstallExecuteAgain sempre deve ser definido para que ele não seja executado durante a remoção.</span><span class="sxs-lookup"><span data-stu-id="165f8-107">InstallExecuteAgain should always be set so that it does not run during removal.</span></span> <span data-ttu-id="165f8-108">Para obter informações, consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="165f8-108">For information, see [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="165f8-109">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="165f8-109">Sequence Restrictions</span></span>

<span data-ttu-id="165f8-110">A ação InstallExecute vem entre a [ação InstallInitialize](installinitialize-action.md) e a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="165f8-110">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="165f8-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="165f8-111">ActionData Messages</span></span>

<span data-ttu-id="165f8-112">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="165f8-112">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="165f8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="165f8-113">Remarks</span></span>

<span data-ttu-id="165f8-114">A ação InstallExecuteAgain faz a mesma coisa que a [ação InstallExecute](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="165f8-114">The InstallExecuteAgain action does the same thing as the [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="165f8-115">Como as tabelas de sequência têm apenas uma chave primária, a coluna Action, a mesma ação não pode ser repetida em uma tabela de sequência específica.</span><span class="sxs-lookup"><span data-stu-id="165f8-115">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="165f8-116">Existem duas ações que fazem a mesma coisa, InstallExecute e InstallExecuteAgain, para casos em que a funcionalidade de InstallExecute é necessária duas vezes na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="165f8-116">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="165f8-117">Para obter mais informações, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="165f8-117">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



