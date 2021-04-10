---
description: A ação AppSearch usa assinaturas de arquivo para pesquisar versões existentes de produtos.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Ação AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169206"
---
# <a name="appsearch-action"></a><span data-ttu-id="36257-103">Ação AppSearch</span><span class="sxs-lookup"><span data-stu-id="36257-103">AppSearch Action</span></span>

<span data-ttu-id="36257-104">A ação AppSearch usa assinaturas de arquivo para pesquisar versões existentes de produtos.</span><span class="sxs-lookup"><span data-stu-id="36257-104">The AppSearch action uses file signatures to search for existing versions of products.</span></span> <span data-ttu-id="36257-105">A ação AppSearch pode usar essas informações para determinar onde as atualizações devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="36257-105">The AppSearch action may use this information to determine where upgrades are to be installed.</span></span> <span data-ttu-id="36257-106">A ação AppSearch também pode ser usada para definir uma propriedade para o valor existente de uma entrada de arquivo Registry ou. ini.</span><span class="sxs-lookup"><span data-stu-id="36257-106">The AppSearch action can also be used to set a property to the existing value of an registry or .ini file entry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="36257-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="36257-107">Sequence Restrictions</span></span>

<span data-ttu-id="36257-108">AppSearch deve ser criado na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="36257-108">AppSearch should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="36257-109">O instalador impede que a ação AppSearch seja executada na sequência InstallExecuteSequence se a ação já tiver sido executada na sequência InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="36257-109">The installer prevents the AppSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="36257-110">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="36257-110">ActionData Messages</span></span>



| <span data-ttu-id="36257-111">Campo</span><span class="sxs-lookup"><span data-stu-id="36257-111">Field</span></span> | <span data-ttu-id="36257-112">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="36257-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="36257-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="36257-113">\[1\]</span></span> | <span data-ttu-id="36257-114">Propriedade que mantém o local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="36257-114">Property holding file location.</span></span> |
| <span data-ttu-id="36257-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="36257-115">\[2\]</span></span> | <span data-ttu-id="36257-116">Assinatura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="36257-116">File signature.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="36257-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="36257-117">Remarks</span></span>

<span data-ttu-id="36257-118">A ação AppSearch requer que a tabela de [assinatura](signature-table.md) esteja presente no pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="36257-118">The AppSearch action requires that the [Signature](signature-table.md) table be present in the installation package.</span></span> <span data-ttu-id="36257-119">As assinaturas de arquivo são listadas na tabela de assinatura.</span><span class="sxs-lookup"><span data-stu-id="36257-119">File signatures are listed in the Signature table.</span></span> <span data-ttu-id="36257-120">Uma assinatura que não está na tabela de assinatura denota um diretório e a ação define a propriedade como o caminho do diretório para essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="36257-120">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="36257-121">A ação AppSearch pesquisa assinaturas de arquivo usando a tabela [CompLocator](complocator-table.md) primeiro, a tabela [RegLocator](reglocator-table.md) em seguida, a tabela [IniLocator](inilocator-table.md) e, por fim, a tabela [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="36257-121">The AppSearch action searches for file signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table next, then the [IniLocator](inilocator-table.md) table, and finally the [DrLocator](drlocator-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36257-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36257-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36257-123">AppSearch</span><span class="sxs-lookup"><span data-stu-id="36257-123">AppSearch</span></span>](appsearch-table.md)
</dt> <dt>

[<span data-ttu-id="36257-124">CompLocator</span><span class="sxs-lookup"><span data-stu-id="36257-124">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="36257-125">IniLocator</span><span class="sxs-lookup"><span data-stu-id="36257-125">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="36257-126">RegLocator</span><span class="sxs-lookup"><span data-stu-id="36257-126">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="36257-127">DrLocator</span><span class="sxs-lookup"><span data-stu-id="36257-127">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



