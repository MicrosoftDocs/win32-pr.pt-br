---
description: A ação WriteRegistryValues configura as informações de registro de um aplicativo.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Ação WriteRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768712"
---
# <a name="writeregistryvalues-action"></a><span data-ttu-id="b2bfe-103">Ação WriteRegistryValues</span><span class="sxs-lookup"><span data-stu-id="b2bfe-103">WriteRegistryValues Action</span></span>

<span data-ttu-id="b2bfe-104">A ação WriteRegistryValues configura as informações de registro de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-104">The WriteRegistryValues action sets up an application's registry information.</span></span> <span data-ttu-id="b2bfe-105">As informações do registro são restringidas pela [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b2bfe-105">The registry information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="b2bfe-106">Um valor de registro será gravado no registro se o componente correspondente tiver sido configurado para ser instalado localmente ou como executado da origem.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-106">A registry value is written to the registry if the corresponding component has been set to be installed either locally or as run from source.</span></span> <span data-ttu-id="b2bfe-107">Para obter mais informações, consulte [tabela do registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="b2bfe-107">For more information, see [Registry table](registry-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b2bfe-108">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="b2bfe-108">Sequence Restrictions</span></span>

<span data-ttu-id="b2bfe-109">A [ação InstallValidate](installvalidate-action.md) deve vir antes da ação WriteRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-109">The [InstallValidate action](installvalidate-action.md) must come before the WriteRegistryValues action.</span></span> <span data-ttu-id="b2bfe-110">Se houver uma [ação RemoveRegistryValues](removeregistryvalues-action.md), ela deverá vir antes da ação WriteRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-110">If there is a [RemoveRegistryValues action](removeregistryvalues-action.md), then it must come before the WriteRegistryValues action.</span></span>

<span data-ttu-id="b2bfe-111">Uma ação personalizada pode ser usada para adicionar linhas à [tabela do registro](registry-table.md) durante uma instalação, desinstalação ou Repair Transaction.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="b2bfe-112">Essas linhas não persistem na tabela do registro e as informações só estão disponíveis durante a transação atual.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="b2bfe-113">A ação personalizada deve, portanto, ser executada em cada instalação, desinstalação ou reparo de transação que exija as informações nessas linhas adicionais.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="b2bfe-114">A ação personalizada deve vir antes das ações [RemoveRegistryValues](removeregistryvalues-action.md) e WriteRegistryValues na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-114">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and WriteRegistryValues actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b2bfe-115">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="b2bfe-115">ActionData Messages</span></span>



| <span data-ttu-id="b2bfe-116">Campo</span><span class="sxs-lookup"><span data-stu-id="b2bfe-116">Field</span></span> | <span data-ttu-id="b2bfe-117">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="b2bfe-117">Description of action data</span></span>                               |
|-------|----------------------------------------------------------|
| <span data-ttu-id="b2bfe-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b2bfe-118">\[1\]</span></span> | <span data-ttu-id="b2bfe-119">Caminho para a chave do registro do valor gravado no registro.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-119">Path to registry key of value written to registry.</span></span>       |
| <span data-ttu-id="b2bfe-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="b2bfe-120">\[2\]</span></span> | <span data-ttu-id="b2bfe-121">Nome da cadeia de caracteres de texto formatado do valor gravado no registro.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-121">Formatted text string name of value written to registry.</span></span> |
| <span data-ttu-id="b2bfe-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="b2bfe-122">\[3\]</span></span> | <span data-ttu-id="b2bfe-123">Cadeia de texto formatada de valor gravado no registro.</span><span class="sxs-lookup"><span data-stu-id="b2bfe-123">Formatted text string of value written to registry.</span></span>      |



 

 

 



