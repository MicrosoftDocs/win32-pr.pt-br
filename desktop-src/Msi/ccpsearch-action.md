---
description: A ação CCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de uma instalação de atualização ser executada.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Ação CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747784"
---
# <a name="ccpsearch-action"></a><span data-ttu-id="c91f0-103">Ação CCPSearch</span><span class="sxs-lookup"><span data-stu-id="c91f0-103">CCPSearch Action</span></span>

<span data-ttu-id="c91f0-104">A ação CCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de uma instalação de atualização ser executada.</span><span class="sxs-lookup"><span data-stu-id="c91f0-104">The CCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c91f0-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="c91f0-105">Sequence Restrictions</span></span>

<span data-ttu-id="c91f0-106">A ação CCPSearch deve ser criada na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c91f0-106">CCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="c91f0-107">O instalador impede que a ação CCPSearch seja executada na sequência InstallExecuteSequence se a ação já tiver sido executada na sequência InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="c91f0-107">The installer prevents the CCPSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span> <span data-ttu-id="c91f0-108">A ação CCPSearch deve vir antes da ação [RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c91f0-108">The CCPSearch action must come before the [RMCCPSearch](rmccpsearch-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c91f0-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="c91f0-109">ActionData Messages</span></span>

<span data-ttu-id="c91f0-110">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="c91f0-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="c91f0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c91f0-111">Remarks</span></span>

<span data-ttu-id="c91f0-112">A ação CCPSearch procura por assinaturas de arquivo listadas na tabela CCPSearch no sistema usando as seguintes tabelas em ordem: assinatura, CompLocator, RegLocator, IniLocator e DrLocator.</span><span class="sxs-lookup"><span data-stu-id="c91f0-112">The CCPSearch action searches for file signatures listed in the CCPSearch table on the system using the following tables in order: Signature, CompLocator, RegLocator, IniLocator, and DrLocator.</span></span>

<span data-ttu-id="c91f0-113">Se alguma assinatura for determinada para existir, a **propriedade \_ êxito do CCP** será definida como 1 e a ação CCPSearch terminará.</span><span class="sxs-lookup"><span data-stu-id="c91f0-113">If any signature is determined to exist, the **CCP\_Success** property is set to 1 and the CCPSearch action terminates.</span></span>

<span data-ttu-id="c91f0-114">A ausência da assinatura da tabela de assinatura denota um diretório.</span><span class="sxs-lookup"><span data-stu-id="c91f0-114">The absence of the signature from the Signature table denotes a directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c91f0-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c91f0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c91f0-116">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="c91f0-116">CCPSearch</span></span>](ccpsearch-table.md)
</dt> <dt>

[<span data-ttu-id="c91f0-117">Signature</span><span class="sxs-lookup"><span data-stu-id="c91f0-117">Signature</span></span>](signature-table.md)
</dt> <dt>

[<span data-ttu-id="c91f0-118">CompLocator</span><span class="sxs-lookup"><span data-stu-id="c91f0-118">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="c91f0-119">RegLocator</span><span class="sxs-lookup"><span data-stu-id="c91f0-119">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="c91f0-120">IniLocator</span><span class="sxs-lookup"><span data-stu-id="c91f0-120">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="c91f0-121">DrLocator</span><span class="sxs-lookup"><span data-stu-id="c91f0-121">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



