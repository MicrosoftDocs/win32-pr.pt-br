---
description: A ação UnregisterProgIdInfo gerencia o cancelamento do registro de informações de ProgId do OLE com o sistema.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Ação UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837398"
---
# <a name="unregisterprogidinfo-action"></a><span data-ttu-id="7c123-103">Ação UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="7c123-103">UnregisterProgIdInfo Action</span></span>

<span data-ttu-id="7c123-104">A ação UnregisterProgIdInfo gerencia o cancelamento do registro de informações de ProgId do OLE com o sistema.</span><span class="sxs-lookup"><span data-stu-id="7c123-104">The UnregisterProgIdInfo action manages the unregistration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7c123-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="7c123-105">Sequence Restrictions</span></span>

<span data-ttu-id="7c123-106">A ação UnregisterProgIdInfo deve vir após a ação [InstallInitialize](installinitialize-action.md) , a ação [UnregisterClassInfo](unregisterclassinfo-action.md) , a ação [UnregisterExtensioninfo](unregisterextensioninfo-action.md) e antes da ação [RegisterProgIdInfo](registerprogidinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7c123-106">The UnregisterProgIdInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action, and before the [RegisterProgIdInfo](registerprogidinfo-action.md) action.</span></span>

<span data-ttu-id="7c123-107">[RemoveRegistryValues](removeregistryvalues-action.md) deve vir antes de UnregisterProgIdInfo na sequência.</span><span class="sxs-lookup"><span data-stu-id="7c123-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterProgIdInfo in the sequence.</span></span>

<span data-ttu-id="7c123-108">O sequenciamento das ações no grupo a seguir é restrito.</span><span class="sxs-lookup"><span data-stu-id="7c123-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="7c123-109">Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:</span><span class="sxs-lookup"><span data-stu-id="7c123-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="7c123-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="7c123-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="7c123-111">UnregisterExtensioninfo</span><span class="sxs-lookup"><span data-stu-id="7c123-111">UnregisterExtensioninfo</span></span>](unregisterextensioninfo-action.md)
-   <span data-ttu-id="7c123-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="7c123-112">UnregisterProgIdInfo</span></span>
-   [<span data-ttu-id="7c123-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="7c123-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="7c123-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="7c123-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="7c123-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="7c123-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="7c123-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="7c123-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="7c123-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="7c123-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="7c123-118">Por exemplo, UnregisterProgIdInfo deve vir antes de [UnregisterMIMEInfo](unregistermimeinfo-action.md) na tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="7c123-118">For example, UnregisterProgIdInfo must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7c123-119">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="7c123-119">ActionData Messages</span></span>



| <span data-ttu-id="7c123-120">Campo</span><span class="sxs-lookup"><span data-stu-id="7c123-120">Field</span></span> | <span data-ttu-id="7c123-121">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="7c123-121">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="7c123-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7c123-122">\[1\]</span></span> | <span data-ttu-id="7c123-123">Identificador de programa do programa registrado.</span><span class="sxs-lookup"><span data-stu-id="7c123-123">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7c123-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c123-124">Remarks</span></span>

<span data-ttu-id="7c123-125">A ação UnregisterProgIdInfo remove informações de ProgId do registro ([tabela ProgID](progid-table.md)) para os recursos que estão conectados às informações de extensão ([tabela de extensão](extension-table.md)) ou as informações de classe (tabela de[classe](class-table.md)) e estão selecionadas para serem desinstaladas no momento.</span><span class="sxs-lookup"><span data-stu-id="7c123-125">The UnregisterProgIdInfo action removes ProgId information from the registry ([ProgId Table](progid-table.md)) for features that are connected to the extension information ([Extension table](extension-table.md)) or the Class information ([Class table](class-table.md)) and are currently selected to be uninstalled.</span></span>

 

 



