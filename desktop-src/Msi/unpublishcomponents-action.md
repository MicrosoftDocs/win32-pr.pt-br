---
description: A ação UnpublishComponents gerencia o desanúncio de componentes listados na tabela PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Ação UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104370910"
---
# <a name="unpublishcomponents-action"></a><span data-ttu-id="6708e-103">Ação UnpublishComponents</span><span class="sxs-lookup"><span data-stu-id="6708e-103">UnpublishComponents Action</span></span>

<span data-ttu-id="6708e-104">A ação UnpublishComponents gerencia o desanúncio de componentes listados na tabela PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="6708e-104">The UnpublishComponents action manages the unadvertisement of components listed in the PublishComponent table.</span></span> <span data-ttu-id="6708e-105">Esses são componentes que podem ter falhado em outros produtos.</span><span class="sxs-lookup"><span data-stu-id="6708e-105">These are components that may be faulted in by other products.</span></span> <span data-ttu-id="6708e-106">Essa ação remove informações sobre os componentes publicados da [tabela PublishComponent](publishcomponent-table.md) para a qual o recurso correspondente está selecionado no momento para ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="6708e-106">This action removes information about published components from the [PublishComponent table](publishcomponent-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6708e-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="6708e-107">Sequence Restrictions</span></span>

<span data-ttu-id="6708e-108">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="6708e-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6708e-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="6708e-109">ActionData Messages</span></span>



| <span data-ttu-id="6708e-110">Campo</span><span class="sxs-lookup"><span data-stu-id="6708e-110">Field</span></span> | <span data-ttu-id="6708e-111">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="6708e-111">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="6708e-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6708e-112">\[1\]</span></span> | <span data-ttu-id="6708e-113">GUID que representa a ID do componente de um recurso anunciado.</span><span class="sxs-lookup"><span data-stu-id="6708e-113">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="6708e-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="6708e-114">\[2\]</span></span> | <span data-ttu-id="6708e-115">Qualificador da ID do componente.</span><span class="sxs-lookup"><span data-stu-id="6708e-115">Qualifier of the component ID.</span></span>                               |



 

