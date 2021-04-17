---
description: A ação UnregisterClassInfo gerencia a remoção de informações de classe COM do registro do sistema. Ele usa a tabela AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Ação UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748135"
---
# <a name="unregisterclassinfo-action"></a><span data-ttu-id="29d46-104">Ação UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-104">UnregisterClassInfo Action</span></span>

<span data-ttu-id="29d46-105">A ação UnregisterClassInfo gerencia a remoção de informações de classe COM do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="29d46-105">The UnregisterClassInfo action manages the removal of COM class information from the system registry.</span></span> <span data-ttu-id="29d46-106">Ele usa a [tabela AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="29d46-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="29d46-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="29d46-107">Sequence Restrictions</span></span>

<span data-ttu-id="29d46-108">A ação UnregisterClassInfo deve vir após a ação [InstallInitialize](installinitialize-action.md) e antes da ação [RegisterClassInfo](registerclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="29d46-108">The UnregisterClassInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterClassInfo](registerclassinfo-action.md) action.</span></span>

<span data-ttu-id="29d46-109">[RemoveRegistryValues](removeregistryvalues-action.md) deve vir antes de UnregisterClassInfo na sequência.</span><span class="sxs-lookup"><span data-stu-id="29d46-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterClassInfo in the sequence.</span></span>

<span data-ttu-id="29d46-110">O sequenciamento das ações no grupo a seguir é restrito.</span><span class="sxs-lookup"><span data-stu-id="29d46-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="29d46-111">Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, elas deverão ocorrer na mesma sequência relativa, conforme mostrado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="29d46-111">If any subset of these actions occur together in a sequence table, they must occur in the same relative sequence as shown in the following table:</span></span>

-   <span data-ttu-id="29d46-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-112">UnregisterClassInfo</span></span>
-   [<span data-ttu-id="29d46-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="29d46-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="29d46-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-115">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="29d46-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="29d46-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="29d46-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="29d46-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="29d46-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="29d46-120">Por exemplo, [RegisterExtensionInfo](registerextensioninfo-action.md) deve vir antes de UnregisterClassInfo na tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="29d46-120">For example, [RegisterExtensionInfo](registerextensioninfo-action.md) must come before UnregisterClassInfo in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="29d46-121">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="29d46-121">ActionData Messages</span></span>



| <span data-ttu-id="29d46-122">Campo</span><span class="sxs-lookup"><span data-stu-id="29d46-122">Field</span></span> | <span data-ttu-id="29d46-123">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="29d46-123">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="29d46-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="29d46-124">\[1\]</span></span> | <span data-ttu-id="29d46-125">GUID da classe COM não registrada.</span><span class="sxs-lookup"><span data-stu-id="29d46-125">GUID of unregistered COM class.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="29d46-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="29d46-126">Remarks</span></span>

<span data-ttu-id="29d46-127">O instalador define a propriedade [**OLEAdvtSupport**](oleadvtsupport.md) como true quando o sistema do usuário atual foi atualizado para funcionar com a instalação sob demanda por meio de com.</span><span class="sxs-lookup"><span data-stu-id="29d46-127">The installer sets the [**OLEAdvtSupport**](oleadvtsupport.md) property to true when the current user's system has been upgraded to work with install-on-demand through COM.</span></span> <span data-ttu-id="29d46-128">Se o sistema não oferecer suporte à instalação sob demanda por meio de COM, o UnregisterClassInfo removerá todas as classes COM listadas na [tabela de classes](class-table.md) associada a recursos ou recursos desinstalados instalados como anunciados no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="29d46-128">If the system does not support install-on-demand through COM, UnregisterClassInfo removes all COM classes listed in the [Class table](class-table.md) associated with either uninstalled features or features installed as advertised from the system registry.</span></span> <span data-ttu-id="29d46-129">Caso contrário, essa ação remove apenas as classes COM associadas a recursos selecionados a serem desinstalados do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="29d46-129">Otherwise, this action removes only the COM classes associated with features selected to be uninstalled from the system registry.</span></span>

 

 



