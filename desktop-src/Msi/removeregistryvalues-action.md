---
description: A ação RemoveRegistryValues só pode remover valores do registro do sistema que foram criados na tabela do registro ou na tabela RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Ação RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753437"
---
# <a name="removeregistryvalues-action"></a><span data-ttu-id="499aa-103">Ação RemoveRegistryValues</span><span class="sxs-lookup"><span data-stu-id="499aa-103">RemoveRegistryValues Action</span></span>

<span data-ttu-id="499aa-104">A ação RemoveRegistryValues só pode remover valores do registro do sistema que foram criados na [tabela do registro](registry-table.md) ou na [tabela RemoveRegistry](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="499aa-104">The RemoveRegistryValues action can only remove values from the system registry that have been authored into the [Registry table](registry-table.md) or the [RemoveRegistry table](removeregistry-table.md).</span></span> <span data-ttu-id="499aa-105">Essa ação remove um valor de registro que foi criado na tabela do registro se o componente associado foi instalado localmente ou como executado da origem e agora está definido para ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="499aa-105">This action removes a registry value that has been authored into the Registry table if the associated component was installed locally or as run from source and is now set to be uninstalled.</span></span> <span data-ttu-id="499aa-106">Essa ação remove um valor de registro que foi criado na tabela RemoveRegistry se o componente associado estiver configurado para ser instalado localmente ou como executado da origem.</span><span class="sxs-lookup"><span data-stu-id="499aa-106">This action removes a registry value that has been authored into the RemoveRegistry table if the associated component is set to be installed locally or as run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="499aa-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="499aa-107">Sequence Restrictions</span></span>

<span data-ttu-id="499aa-108">A ação [InstallValidate](installvalidate-action.md) deve ser chamada antes de chamar RemoveRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="499aa-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveRegistryValues.</span></span> <span data-ttu-id="499aa-109">Se uma ação [WriteRegistryValues](writeregistryvalues-action.md) for usada, ela deverá vir após RemoveRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="499aa-109">If a [WriteRegistryValues](writeregistryvalues-action.md) action is used, it must come after RemoveRegistryValues.</span></span> <span data-ttu-id="499aa-110">RemoveRegistryValues deve vir antes de [UnregisterMIMEInfo](unregistermimeinfo-action.md) ou [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="499aa-110">RemoveRegistryValues must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) or [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span></span>

<span data-ttu-id="499aa-111">Uma ação personalizada pode ser usada para adicionar linhas à [tabela do registro](registry-table.md) durante uma instalação, desinstalação ou Repair Transaction.</span><span class="sxs-lookup"><span data-stu-id="499aa-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="499aa-112">Essas linhas não persistem na tabela do registro e as informações só estão disponíveis durante a transação atual.</span><span class="sxs-lookup"><span data-stu-id="499aa-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="499aa-113">A ação personalizada deve, portanto, ser executada em cada instalação, desinstalação ou reparo de transação que exija as informações nessas linhas adicionais.</span><span class="sxs-lookup"><span data-stu-id="499aa-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="499aa-114">A ação personalizada deve vir antes das ações RemoveRegistryValues e [WriteRegistryValues](writeregistryvalues-action.md) na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="499aa-114">The custom action must come before the RemoveRegistryValues and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="499aa-115">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="499aa-115">ActionData Messages</span></span>



| <span data-ttu-id="499aa-116">Campo</span><span class="sxs-lookup"><span data-stu-id="499aa-116">Field</span></span> | <span data-ttu-id="499aa-117">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="499aa-117">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="499aa-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="499aa-118">\[1\]</span></span> | <span data-ttu-id="499aa-119">Caminho do registro para a chave do valor do registro removido.</span><span class="sxs-lookup"><span data-stu-id="499aa-119">Registry path to key of removed registry value.</span></span>     |
| <span data-ttu-id="499aa-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="499aa-120">\[2\]</span></span> | <span data-ttu-id="499aa-121">Cadeia de caracteres formatada do nome do valor do registro removido.</span><span class="sxs-lookup"><span data-stu-id="499aa-121">Formatted string of name of removed registry value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="499aa-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="499aa-122">Remarks</span></span>

<span data-ttu-id="499aa-123">Para remover um valor de registro, registre o valor na coluna valor da tabela de registro.</span><span class="sxs-lookup"><span data-stu-id="499aa-123">To remove a registry value, record the value in the Value column of the Registry table.</span></span> <span data-ttu-id="499aa-124">Se a ação WriteRegistryValues tiver anexado as \_ \_ cadeias de caracteres reg multi sz ao valor na [tabela do registro](registry-table.md), a ação RemoveRegistryValues removerá somente essas cadeias de caracteres do valor do registro.</span><span class="sxs-lookup"><span data-stu-id="499aa-124">If the WriteRegistryValues action has attached REG\_MULTI\_SZ strings to the value in the [Registry table](registry-table.md), then the RemoveRegistryValues action removes only those strings from the registry value.</span></span>

 

 



