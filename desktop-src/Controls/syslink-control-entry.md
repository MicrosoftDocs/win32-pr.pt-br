---
title: SysLink
description: Esta seção contém informações sobre os elementos de programação usados com controles SysLink.
ms.assetid: 13a7b6d0-4bf1-480f-b447-838a550a5866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9bbfaea9b86c2d8dc42c84d050e5bec997ceb18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916112"
---
# <a name="syslink"></a><span data-ttu-id="2da6b-103">SysLink</span><span class="sxs-lookup"><span data-stu-id="2da6b-103">SysLink</span></span>

<span data-ttu-id="2da6b-104">Esta seção contém informações sobre os elementos de programação usados com controles SysLink.</span><span class="sxs-lookup"><span data-stu-id="2da6b-104">This section contains information about the programming elements used with SysLink controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="2da6b-105">Visões gerais</span><span class="sxs-lookup"><span data-stu-id="2da6b-105">Overviews</span></span>



| <span data-ttu-id="2da6b-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="2da6b-106">Topic</span></span>                                    | <span data-ttu-id="2da6b-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="2da6b-107">Contents</span></span>                                                                                       |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2da6b-108">Controles SysLink</span><span class="sxs-lookup"><span data-stu-id="2da6b-108">SysLink Controls</span></span>](syslink-overview.md) | <span data-ttu-id="2da6b-109">O controle SysLink fornece uma maneira conveniente de inserir links de hipertexto em uma janela.</span><span class="sxs-lookup"><span data-stu-id="2da6b-109">The SysLink control provides a convenient way to embed hypertext links in a window.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="2da6b-110">Mensagens</span><span class="sxs-lookup"><span data-stu-id="2da6b-110">Messages</span></span>



| <span data-ttu-id="2da6b-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="2da6b-111">Topic</span></span>                                           | <span data-ttu-id="2da6b-112">Sumário</span><span class="sxs-lookup"><span data-stu-id="2da6b-112">Contents</span></span>                                                                             |
|-------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="2da6b-113">**\_GETIDEALHEIGHT LM**</span><span class="sxs-lookup"><span data-stu-id="2da6b-113">**LM\_GETIDEALHEIGHT**</span></span>](lm-getidealheight.md) | <span data-ttu-id="2da6b-114">Recupera a altura preferida de um link para a largura atual do controle.</span><span class="sxs-lookup"><span data-stu-id="2da6b-114">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="2da6b-115">**\_GETIDEALSIZE LM**</span><span class="sxs-lookup"><span data-stu-id="2da6b-115">**LM\_GETIDEALSIZE**</span></span>](lm-getidealsize.md)     | <span data-ttu-id="2da6b-116">Recupera a altura preferida de um link para a largura atual do controle.</span><span class="sxs-lookup"><span data-stu-id="2da6b-116">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="2da6b-117">**\_GETITEM LM**</span><span class="sxs-lookup"><span data-stu-id="2da6b-117">**LM\_GETITEM**</span></span>](lm-getitem.md)               | <span data-ttu-id="2da6b-118">Recupera os Estados e atributos de um item.</span><span class="sxs-lookup"><span data-stu-id="2da6b-118">Retrieves the states and attributes of an item.</span></span><br/>                           |
| [<span data-ttu-id="2da6b-119">**HITTEST do LM \_**</span><span class="sxs-lookup"><span data-stu-id="2da6b-119">**LM\_HITTEST**</span></span>](lm-hittest.md)               | <span data-ttu-id="2da6b-120">Determina se o usuário clicou no link especificado.</span><span class="sxs-lookup"><span data-stu-id="2da6b-120">Determines whether the user clicked the specified link.</span></span><br/>                   |
| [<span data-ttu-id="2da6b-121">**\_SETITEM LM**</span><span class="sxs-lookup"><span data-stu-id="2da6b-121">**LM\_SETITEM**</span></span>](lm-setitem.md)               | <span data-ttu-id="2da6b-122">Define os Estados e atributos de um item.</span><span class="sxs-lookup"><span data-stu-id="2da6b-122">Sets the states and attributes of an item.</span></span><br/>                                |



 

### <a name="structures"></a><span data-ttu-id="2da6b-123">Estruturas</span><span class="sxs-lookup"><span data-stu-id="2da6b-123">Structures</span></span>



| <span data-ttu-id="2da6b-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="2da6b-124">Topic</span></span>                                | <span data-ttu-id="2da6b-125">Sumário</span><span class="sxs-lookup"><span data-stu-id="2da6b-125">Contents</span></span>                                                                                                                                                                           |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2da6b-126">**LHITTESTINFO**</span><span class="sxs-lookup"><span data-stu-id="2da6b-126">**LHITTESTINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lhittestinfo) | <span data-ttu-id="2da6b-127">Usado para obter informações sobre o link correspondente a um determinado local.</span><span class="sxs-lookup"><span data-stu-id="2da6b-127">Used to get information about the link corresponding to a given location.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="2da6b-128">**LITEm**</span><span class="sxs-lookup"><span data-stu-id="2da6b-128">**LITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-litem)               | <span data-ttu-id="2da6b-129">Usado para definir e recuperar informações sobre um item de link.</span><span class="sxs-lookup"><span data-stu-id="2da6b-129">Used to set and retrieve information about a link item.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="2da6b-130">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="2da6b-130">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)             | <span data-ttu-id="2da6b-131">O [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) contém informações de notificação.</span><span class="sxs-lookup"><span data-stu-id="2da6b-131">The [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) Contains notification information.</span></span> <span data-ttu-id="2da6b-132">Envie essa estrutura com as mensagens de [ \_ retorno](nm-return.md) do [nm \_ Click](nm-click-syslink.md) ou nm.</span><span class="sxs-lookup"><span data-stu-id="2da6b-132">Send this structure with the [NM\_CLICK](nm-click-syslink.md) or [NM\_RETURN](nm-return.md) messages.</span></span><br/> |



 

 

 





