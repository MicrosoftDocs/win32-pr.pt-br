---
title: Sinalizadores de notificação de alteração
description: Sinalizadores de notificação de alteração
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Alteração
- Sinalizadores de notificação de alteração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292262"
---
# <a name="change-notification-flags"></a><span data-ttu-id="2b4d5-105">Sinalizadores de notificação de alteração</span><span class="sxs-lookup"><span data-stu-id="2b4d5-105">Change Notification Flags</span></span>



| <span data-ttu-id="2b4d5-106">Constante</span><span class="sxs-lookup"><span data-stu-id="2b4d5-106">Constant</span></span>                         | <span data-ttu-id="2b4d5-107">Valor</span><span class="sxs-lookup"><span data-stu-id="2b4d5-107">Value</span></span>      | <span data-ttu-id="2b4d5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b4d5-108">Description</span></span>                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b4d5-109">\_tipos de \_ alteração de número RTM \_</span><span class="sxs-lookup"><span data-stu-id="2b4d5-109">RTM\_NUM\_CHANGE\_TYPES</span></span>          | <span data-ttu-id="2b4d5-110">3</span><span class="sxs-lookup"><span data-stu-id="2b4d5-110">3</span></span>          | <span data-ttu-id="2b4d5-111">Especifica o número de tipos de alteração que são usados atualmente pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-111">Specifies the number of change types that are currently used by the routing table manager.</span></span>                                                                            |
| <span data-ttu-id="2b4d5-112">tipo de alteração de RTM \_ \_ \_ tudo</span><span class="sxs-lookup"><span data-stu-id="2b4d5-112">RTM\_CHANGE\_TYPE\_ALL</span></span>           | <span data-ttu-id="2b4d5-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="2b4d5-113">0x0001</span></span>     | <span data-ttu-id="2b4d5-114">Notifica o cliente sobre qualquer alteração em um destino.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-114">Notifies the client of any change to a destination.</span></span>                                                                                                                   |
| <span data-ttu-id="2b4d5-115">\_ \_ melhor tipo de alteração de RTM \_</span><span class="sxs-lookup"><span data-stu-id="2b4d5-115">RTM\_CHANGE\_TYPE\_BEST</span></span>          | <span data-ttu-id="2b4d5-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="2b4d5-116">0x0002</span></span>     | <span data-ttu-id="2b4d5-117">Notifica o cliente sobre as alterações na melhor rota ou quando a melhor rota é alterada.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-117">Notifies the client of changes to the best route, or when the best route changes.</span></span>                                                                                     |
| <span data-ttu-id="2b4d5-118">\_ \_ encaminhamento de tipo de alteração RTM \_</span><span class="sxs-lookup"><span data-stu-id="2b4d5-118">RTM\_CHANGE\_TYPE\_FORWARDING</span></span>    | <span data-ttu-id="2b4d5-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="2b4d5-119">0x0004</span></span>     | <span data-ttu-id="2b4d5-120">Notifica o cliente sobre as melhores alterações de rota que afetam o encaminhamento (como alterações do próximo salto).</span><span class="sxs-lookup"><span data-stu-id="2b4d5-120">Notifies the client of any best route changes that affect forwarding (such as next hop changes).</span></span>                                                                      |
| <span data-ttu-id="2b4d5-121">o RTM \_ notifica \_ apenas os \_ \_ dests marcados</span><span class="sxs-lookup"><span data-stu-id="2b4d5-121">RTM\_NOTIFY\_ONLY\_MARKED\_DESTS</span></span> | <span data-ttu-id="2b4d5-122">0x00010000</span><span class="sxs-lookup"><span data-stu-id="2b4d5-122">0x00010000</span></span> | <span data-ttu-id="2b4d5-123">Notifica o cliente sobre as alterações nos destinos que o cliente marcou.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-123">Notifies the client of changes to destinations that the client has marked.</span></span> <span data-ttu-id="2b4d5-124">Se esse sinalizador não for especificado, as mensagens de notificação de alteração para todos os destinos serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="2b4d5-124">If this flag is not specified, change notification messages for all destinations are sent.</span></span> |



 

 

 




