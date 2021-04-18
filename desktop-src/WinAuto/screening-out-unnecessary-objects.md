---
title: Triagem de objetos desnecessários
description: Se você usar inspecionar para examinar um controle simples, como um botão de ação OK no acessório do Microsoft WordPad, poderá ver que esses objetos de janela pai também contêm vários objetos filho invisíveis.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105786130"
---
# <a name="screening-out-unnecessary-objects"></a><span data-ttu-id="7ced6-103">Triagem de objetos desnecessários</span><span class="sxs-lookup"><span data-stu-id="7ced6-103">Screening Out Unnecessary Objects</span></span>

<span data-ttu-id="7ced6-104">Se você usar [inspecionar](inspect-objects.md) para examinar um controle simples, como um botão de ação OK no acessório do Microsoft WordPad, poderá ver que esses objetos de janela pai também contêm vários objetos filho invisíveis.</span><span class="sxs-lookup"><span data-stu-id="7ced6-104">If you use [Inspect](inspect-objects.md) to examine a simple control such as an OK push button in the Microsoft WordPad accessory, you can see that these parent window objects also contain several invisible child objects.</span></span> <span data-ttu-id="7ced6-105">Esses objetos invisíveis têm o mesmo nome de classe de janela que o controle e têm a [propriedade State](state-property.md) do [**sistema de estado \_ \_ invisível**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7ced6-105">These invisible objects have the same window class name as the control and have the [State property](state-property.md) of [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> <span data-ttu-id="7ced6-106">A tabela a seguir lista os objetos filho invisíveis que o Microsoft Acessibilidade Ativa cria para o controle.</span><span class="sxs-lookup"><span data-stu-id="7ced6-106">The following table lists the invisible child objects that Microsoft Active Accessibility creates for the control.</span></span>



| <span data-ttu-id="7ced6-107">Name</span><span class="sxs-lookup"><span data-stu-id="7ced6-107">Name</span></span>          | <span data-ttu-id="7ced6-108">Função</span><span class="sxs-lookup"><span data-stu-id="7ced6-108">Role</span></span>                                                                  | <span data-ttu-id="7ced6-109">ChildCount</span><span class="sxs-lookup"><span data-stu-id="7ced6-109">ChildCount</span></span> |
|---------------|-----------------------------------------------------------------------|------------|
| <span data-ttu-id="7ced6-110">Sistema</span><span class="sxs-lookup"><span data-stu-id="7ced6-110">"System"</span></span>      | [<span data-ttu-id="7ced6-111">**\_BarraDeMenu do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7ced6-111">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="7ced6-112">0</span><span class="sxs-lookup"><span data-stu-id="7ced6-112">0</span></span>          |
| <span data-ttu-id="7ced6-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7ced6-113">None</span></span>          | [<span data-ttu-id="7ced6-114">**\_TITLEBAR do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7ced6-114">**ROLE\_SYSTEM\_TITLEBAR**</span></span>](object-roles.md)   | <span data-ttu-id="7ced6-115">5</span><span class="sxs-lookup"><span data-stu-id="7ced6-115">5</span></span>          |
| <span data-ttu-id="7ced6-116">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="7ced6-116">"Application"</span></span> | [<span data-ttu-id="7ced6-117">**\_BarraDeMenu do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7ced6-117">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="7ced6-118">0</span><span class="sxs-lookup"><span data-stu-id="7ced6-118">0</span></span>          |
| <span data-ttu-id="7ced6-119">Vertical</span><span class="sxs-lookup"><span data-stu-id="7ced6-119">"Vertical"</span></span>    | [<span data-ttu-id="7ced6-120">**\_barra de rolagem do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7ced6-120">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="7ced6-121">5</span><span class="sxs-lookup"><span data-stu-id="7ced6-121">5</span></span>          |
| <span data-ttu-id="7ced6-122">Na</span><span class="sxs-lookup"><span data-stu-id="7ced6-122">"Horizontal"</span></span>  | [<span data-ttu-id="7ced6-123">**\_barra de rolagem do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7ced6-123">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="7ced6-124">5</span><span class="sxs-lookup"><span data-stu-id="7ced6-124">5</span></span>          |
| <span data-ttu-id="7ced6-125">"Dimensionar caixa"</span><span class="sxs-lookup"><span data-stu-id="7ced6-125">"Size Box"</span></span>    | [<span data-ttu-id="7ced6-126">**\_alça do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7ced6-126">**ROLE\_SYSTEM\_GRIP**</span></span>](object-roles.md)           | <span data-ttu-id="7ced6-127">0</span><span class="sxs-lookup"><span data-stu-id="7ced6-127">0</span></span>          |



 

<span data-ttu-id="7ced6-128">Os desenvolvedores de cliente devem identificar e filtrar esses objetos de janela pai e objetos filho invisíveis, pois eles não fornecem informações significativas para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="7ced6-128">Client developers must identify and filter out these parent window objects and invisible child objects because they do not provide meaningful information to end users.</span></span>

 

 




