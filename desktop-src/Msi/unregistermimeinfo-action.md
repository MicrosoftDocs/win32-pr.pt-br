---
description: A ação UnregisterMIMEInfo cancela o registro das informações do registro relacionadas a MIME do sistema. A ação cancela o registro de informações de MIME para servidores da tabela MIME para a qual o recurso correspondente está selecionado no momento para ser desinstalado.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Ação UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172161"
---
# <a name="unregistermimeinfo-action"></a><span data-ttu-id="86bdc-104">Ação UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-104">UnregisterMIMEInfo Action</span></span>

<span data-ttu-id="86bdc-105">A ação UnregisterMIMEInfo cancela o registro das informações do registro relacionadas a MIME do sistema.</span><span class="sxs-lookup"><span data-stu-id="86bdc-105">The UnregisterMIMEInfo action unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="86bdc-106">A ação cancela o registro de informações de MIME para servidores da [tabela MIME](mime-table.md) para a qual o recurso correspondente está selecionado no momento para ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="86bdc-106">The action unregisters MIME information for servers from the [MIME table](mime-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="86bdc-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="86bdc-107">Sequence Restrictions</span></span>

<span data-ttu-id="86bdc-108">A ação UnregisterMIMEInfo deve vir após a ação [InstallInitialize](installinitialize-action.md) , a ação [UnregisterClassInfo](unregisterclassinfo-action.md) , a ação [UnregisterExtensionInfo](unregisterextensioninfo-action.md) e antes da ação [RegisterMIMEInfo](registermimeinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="86bdc-108">The UnregisterMIMEInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action, and before the [RegisterMIMEInfo](registermimeinfo-action.md) action.</span></span>

<span data-ttu-id="86bdc-109">[RemoveRegistryValues](removeregistryvalues-action.md) deve vir antes de UnregisterMIMEInfo na sequência.</span><span class="sxs-lookup"><span data-stu-id="86bdc-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterMIMEInfo in the sequence.</span></span>

<span data-ttu-id="86bdc-110">O sequenciamento das ações no grupo a seguir é restrito.</span><span class="sxs-lookup"><span data-stu-id="86bdc-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="86bdc-111">Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:</span><span class="sxs-lookup"><span data-stu-id="86bdc-111">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="86bdc-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-112">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="86bdc-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="86bdc-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   <span data-ttu-id="86bdc-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-115">UnregisterMIMEInfo</span></span>
-   [<span data-ttu-id="86bdc-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="86bdc-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="86bdc-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="86bdc-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="86bdc-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="86bdc-120">Por exemplo, UnregisterMIMEInfo deve vir antes de [RegisterExtensionInfo](registerextensioninfo-action.md) na tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="86bdc-120">For example, UnregisterMIMEInfo must come before [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="86bdc-121">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="86bdc-121">ActionData Messages</span></span>



| <span data-ttu-id="86bdc-122">Campo</span><span class="sxs-lookup"><span data-stu-id="86bdc-122">Field</span></span> | <span data-ttu-id="86bdc-123">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="86bdc-123">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="86bdc-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="86bdc-124">\[1\]</span></span> | <span data-ttu-id="86bdc-125">Identificador do tipo de conteúdo MIME não registrado.</span><span class="sxs-lookup"><span data-stu-id="86bdc-125">Identifier of unregistered MIME content type.</span></span> |
| <span data-ttu-id="86bdc-126">\[2\]</span><span class="sxs-lookup"><span data-stu-id="86bdc-126">\[2\]</span></span> | <span data-ttu-id="86bdc-127">Extensão associada ao tipo de conteúdo MIME.</span><span class="sxs-lookup"><span data-stu-id="86bdc-127">Extension associated with MIME content type.</span></span>  |



 

 

 



