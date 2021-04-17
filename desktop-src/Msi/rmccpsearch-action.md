---
description: A ação RMCCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de uma instalação de atualização ser executada.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Ação RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789767"
---
# <a name="rmccpsearch-action"></a><span data-ttu-id="ed317-103">Ação RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="ed317-103">RMCCPSearch Action</span></span>

<span data-ttu-id="ed317-104">A ação RMCCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de uma instalação de atualização ser executada.</span><span class="sxs-lookup"><span data-stu-id="ed317-104">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ed317-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="ed317-105">Sequence Restrictions</span></span>

<span data-ttu-id="ed317-106">A ação RMCCPSearch deve ser criada na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ed317-106">RMCCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="ed317-107">O instalador impede que o RMCCPSearch seja executado na sequência InstallExecuteSequence se a ação já tiver sido executada na sequência InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="ed317-107">The installer prevents RMCCPSearch from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ed317-108">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="ed317-108">ActionData Messages</span></span>

<span data-ttu-id="ed317-109">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="ed317-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed317-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed317-110">Remarks</span></span>

<span data-ttu-id="ed317-111">A ação RMCCPSearch requer que a propriedade da [**\_ unidade CCP**](ccp-drive.md) seja definida como o caminho raiz no [*volume*](v-gly.md) removível que tem a instalação para qualquer um dos produtos qualificados.</span><span class="sxs-lookup"><span data-stu-id="ed317-111">The RMCCPSearch action requires the [**CCP\_DRIVE**](ccp-drive.md) property to be set to the root path on the removable [*volume*](v-gly.md) that has the installation for any of the qualifying products.</span></span>

<span data-ttu-id="ed317-112">Cada assinatura de arquivo na tabela CCPSearch é pesquisada sob o caminho referido pela propriedade da [**\_ unidade CCP**](ccp-drive.md) usando a tabela [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ed317-112">Each file signature in the CCPSearch table is searched for under the path referred to by the [**CCP\_DRIVE**](ccp-drive.md) property using the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="ed317-113">A ausência da assinatura da tabela de [assinatura](signature-table.md) denota um diretório.</span><span class="sxs-lookup"><span data-stu-id="ed317-113">The absence of the signature from the [Signature](signature-table.md) table denotes a directory.</span></span> <span data-ttu-id="ed317-114">Se alguma assinatura for determinada para existir, a ação RMCCPSearch será encerrada.</span><span class="sxs-lookup"><span data-stu-id="ed317-114">If any signature is determined to exist, the RMCCPSearch action terminates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed317-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed317-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed317-116">Tabela CCPSearch</span><span class="sxs-lookup"><span data-stu-id="ed317-116">CCPSearch table</span></span>](ccpsearch-table.md)
</dt> </dl>

 

 



