---
description: A ação RegisterProgIdInfo gerencia o registro de informações de ProgId de OLE com o sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Ação RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749987"
---
# <a name="registerprogidinfo-action"></a><span data-ttu-id="690f2-103">Ação RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-103">RegisterProgIdInfo Action</span></span>

<span data-ttu-id="690f2-104">A ação RegisterProgIdInfo gerencia o registro de informações de ProgId de OLE com o sistema.</span><span class="sxs-lookup"><span data-stu-id="690f2-104">The RegisterProgIdInfo action manages the registration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="690f2-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="690f2-105">Sequence Restrictions</span></span>

<span data-ttu-id="690f2-106">A ação RegisterProgIdInfo deve vir após a ação [InstallFiles](installfiles-action.md) , a ação [UnregisterProgIdInfo](unregisterprogidinfo-action.md) , a ação [RegisterClassInfo](registerclassinfo-action.md) e a ação [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="690f2-106">The RegisterProgIdInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterProgIdInfo](unregisterprogidinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="690f2-107">O sequenciamento das ações no grupo a seguir é restrito.</span><span class="sxs-lookup"><span data-stu-id="690f2-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="690f2-108">Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:</span><span class="sxs-lookup"><span data-stu-id="690f2-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="690f2-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="690f2-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="690f2-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="690f2-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="690f2-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="690f2-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   <span data-ttu-id="690f2-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-115">RegisterProgIdInfo</span></span>
-   [<span data-ttu-id="690f2-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="690f2-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="690f2-117">Por exemplo, RegisterProgIdInfo deve vir após [RegisterExtensionInfo](registerextensioninfo-action.md) na tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="690f2-117">For example, RegisterProgIdInfo must come after [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="690f2-118">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="690f2-118">ActionData Messages</span></span>



| <span data-ttu-id="690f2-119">Campo</span><span class="sxs-lookup"><span data-stu-id="690f2-119">Field</span></span> | <span data-ttu-id="690f2-120">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="690f2-120">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="690f2-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="690f2-121">\[1\]</span></span> | <span data-ttu-id="690f2-122">Identificador de programa do programa registrado.</span><span class="sxs-lookup"><span data-stu-id="690f2-122">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="690f2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="690f2-123">Remarks</span></span>

<span data-ttu-id="690f2-124">A ação RegisterProgIdInfo registra todas as informações de ProgId para servidores especificados na [tabela ProgID](progid-table.md) e para os quais o servidor de classe ou servidor de extensão correspondente foi selecionado para instalação.</span><span class="sxs-lookup"><span data-stu-id="690f2-124">The RegisterProgIdInfo action registers all ProgId information for servers that are specified in the [ProgId table](progid-table.md) and for which the corresponding class server or extension server has been selected to be installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="690f2-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="690f2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="690f2-126">Tabela de classes</span><span class="sxs-lookup"><span data-stu-id="690f2-126">Class table</span></span>](class-table.md)
</dt> <dt>

[<span data-ttu-id="690f2-127">Tabela de extensão</span><span class="sxs-lookup"><span data-stu-id="690f2-127">Extension table</span></span>](extension-table.md)
</dt> </dl>

 

 



