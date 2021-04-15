---
description: A ação ExecuteAction inicia a sequência de execução usando a propriedade EXECUTEaction para determinar qual tipo de instalação deve ser executada.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Ação ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461226"
---
# <a name="executeaction-action"></a><span data-ttu-id="0aa4d-103">Ação ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="0aa4d-103">ExecuteAction Action</span></span>

<span data-ttu-id="0aa4d-104">A ação ExecuteAction inicia a sequência de execução usando a propriedade [**ExecuteAction**](executeaction.md) para determinar qual tipo de instalação deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-104">The ExecuteAction action initiates the execution sequence using the [**EXECUTEACTION**](executeaction.md) property to determine which type of installation to perform.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0aa4d-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="0aa4d-105">Sequence Restrictions</span></span>

<span data-ttu-id="0aa4d-106">Essa ação deve ser sequenciada depois de todas as coletas de informações necessárias para começar a instalação ser concluída.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-106">This action should be sequenced after all information collection necessary to begin the installation is complete.</span></span> <span data-ttu-id="0aa4d-107">Ações adicionais podem ser sequenciadas após a ação ExecuteAction na [tabela InstallUISequence](installuisequence-table.md)e a [tabela AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4d-107">Additional actions may be sequenced after ExecuteAction action in the [InstallUISequence table](installuisequence-table.md), and [AdminUISequence table](adminuisequence-table.md).</span></span> <span data-ttu-id="0aa4d-108">Normalmente, uma sequência começará com ações de [*custo*](c-gly.md) , como a [ação CostInitialize](costinitialize-action.md), seguida pelas ações da interface do usuário e a ação ExecuteAction.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-108">A sequence will typically begin with [*costing*](c-gly.md) actions, such as the [CostInitialize action](costinitialize-action.md), followed by the user interface actions, and then the ExecuteAction action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0aa4d-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="0aa4d-109">ActionData Messages</span></span>

<span data-ttu-id="0aa4d-110">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa4d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0aa4d-111">Remarks</span></span>

<span data-ttu-id="0aa4d-112">A ação ExecuteAction é executada com privilégios de sistema se o serviço do instalador estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-112">The ExecuteAction action is run with system privileges if the installer service is enabled.</span></span> <span data-ttu-id="0aa4d-113">As ações de nível superior, como a ação de [instalação](install-action.md), a [ação de anúncio](advertise-action.md)e a ação de [administrador](admin-action.md) incluem lógica interna que determina se a chamada da ação ExecuteAction exige que a sequência de execução ou a sequência da interface do usuário seja executada.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-113">The top-level actions, such as the [INSTALL action](install-action.md), [ADVERTISE action](advertise-action.md), and [ADMIN action](admin-action.md) include internal logic that determines whether calling the ExecuteAction action requires either the execution sequence or the user interface sequence to run.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aa4d-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0aa4d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aa4d-115">Tabela InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="0aa4d-115">InstallUISequence table</span></span>](installuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="0aa4d-116">Tabela AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="0aa4d-116">AdminUISequence table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="0aa4d-117">Ação CostInitialize</span><span class="sxs-lookup"><span data-stu-id="0aa4d-117">CostInitialize action</span></span>](costinitialize-action.md)
</dt> </dl>

 

 



