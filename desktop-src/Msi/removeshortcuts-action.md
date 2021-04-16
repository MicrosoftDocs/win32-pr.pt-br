---
description: A ação RemoveShortcuts gerencia a remoção de um atalho anunciado cujo recurso está selecionado para desinstalação ou um atalho não anunciado cujo componente está selecionado para desinstalação. Para obter mais informações, consulte a tabela de atalho.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Ação RemoveShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749986"
---
# <a name="removeshortcuts-action"></a><span data-ttu-id="0d3fc-104">Ação RemoveShortcuts</span><span class="sxs-lookup"><span data-stu-id="0d3fc-104">RemoveShortcuts Action</span></span>

<span data-ttu-id="0d3fc-105">A ação RemoveShortcuts gerencia a remoção de um atalho anunciado cujo recurso está selecionado para desinstalação ou um atalho não anunciado cujo componente está selecionado para desinstalação.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-105">The RemoveShortcuts action manages the removal of an advertised shortcut whose feature is selected for uninstallation or a nonadvertised shortcut whose component is selected for uninstallation.</span></span> <span data-ttu-id="0d3fc-106">Para obter mais informações, consulte a [tabela de atalho](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="0d3fc-106">For more information, see the [Shortcut Table](shortcut-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0d3fc-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="0d3fc-107">Sequence Restrictions</span></span>

<span data-ttu-id="0d3fc-108">A ação RemoveShortcuts deve vir antes da ação [Createshortcuts](createshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0d3fc-108">The RemoveShortcuts action must come before the [CreateShortcuts](createshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0d3fc-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="0d3fc-109">ActionData Messages</span></span>



| <span data-ttu-id="0d3fc-110">Campo</span><span class="sxs-lookup"><span data-stu-id="0d3fc-110">Field</span></span> | <span data-ttu-id="0d3fc-111">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="0d3fc-111">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="0d3fc-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0d3fc-112">\[1\]</span></span> | <span data-ttu-id="0d3fc-113">Identificador do atalho removido.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-113">Identifier of removed shortcut.</span></span> |



 

 

 



