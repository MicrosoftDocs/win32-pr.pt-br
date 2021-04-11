---
description: A ação InstallExecute executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação InstallExecute ou ação de InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Ação InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089986"
---
# <a name="installexecute-action"></a><span data-ttu-id="677b0-103">Ação InstallExecute</span><span class="sxs-lookup"><span data-stu-id="677b0-103">InstallExecute Action</span></span>

<span data-ttu-id="677b0-104">A ação InstallExecute executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação InstallExecute ou ação de [InstallExecuteAgain](installexecuteagain-action.md).</span><span class="sxs-lookup"><span data-stu-id="677b0-104">The InstallExecute action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecute action or [InstallExecuteAgain action](installexecuteagain-action.md).</span></span> <span data-ttu-id="677b0-105">A ação InstallExecute atualiza o sistema sem encerrar a transação.</span><span class="sxs-lookup"><span data-stu-id="677b0-105">The InstallExecute action updates the system without ending the transaction.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="677b0-106">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="677b0-106">Sequence Restrictions</span></span>

<span data-ttu-id="677b0-107">A ação InstallExecute vem entre a [ação InstallInitialize](installinitialize-action.md) e a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="677b0-107">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="677b0-108">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="677b0-108">ActionData Messages</span></span>

<span data-ttu-id="677b0-109">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="677b0-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="677b0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="677b0-110">Remarks</span></span>

<span data-ttu-id="677b0-111">A [ação InstallExecuteAgain](installexecuteagain-action.md) faz a mesma coisa que a ação InstallExecute.</span><span class="sxs-lookup"><span data-stu-id="677b0-111">The [InstallExecuteAgain action](installexecuteagain-action.md) does the same thing as the InstallExecute action.</span></span> <span data-ttu-id="677b0-112">Como as tabelas de sequência têm apenas uma chave primária, a coluna Action, a mesma ação não pode ser repetida em uma tabela de sequência específica.</span><span class="sxs-lookup"><span data-stu-id="677b0-112">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="677b0-113">Existem duas ações que fazem a mesma coisa, InstallExecute e InstallExecuteAgain, para casos em que a funcionalidade de InstallExecute é necessária duas vezes na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="677b0-113">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="677b0-114">Para obter mais informações, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="677b0-114">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



