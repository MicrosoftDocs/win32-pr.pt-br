---
title: Mensagens comunicadas por meio de interfaces do usuário
description: Este tópico lista as mensagens que um serviço de diretório pode enviar de uma interface do usuário.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Mensagens comunicadas por meio de interfaces do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004912"
---
# <a name="messages-communicated-through-user-interfaces"></a><span data-ttu-id="90530-104">Mensagens comunicadas por meio de interfaces do usuário</span><span class="sxs-lookup"><span data-stu-id="90530-104">Messages Communicated through User Interfaces</span></span>

<span data-ttu-id="90530-105">Este tópico lista as mensagens que um serviço de diretório pode enviar de uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="90530-105">This topic lists messages that a directory service can send from a user interface.</span></span>

## <a name="common-query-page-messages"></a><span data-ttu-id="90530-106">Mensagens comuns da página de consulta</span><span class="sxs-lookup"><span data-stu-id="90530-106">Common Query Page Messages</span></span>

<span data-ttu-id="90530-107">As seguintes mensagens são enviadas para uma página de extensão do formulário de consulta do serviço de diretório na função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :</span><span class="sxs-lookup"><span data-stu-id="90530-107">The following messages are sent to a directory service query form extension page in the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function:</span></span>

-   [<span data-ttu-id="90530-108">**CQPM \_ CLEARFORM**</span><span class="sxs-lookup"><span data-stu-id="90530-108">**CQPM\_CLEARFORM**</span></span>](cqpm-clearform.md)
-   [<span data-ttu-id="90530-109">**CQPM \_ habilitar**</span><span class="sxs-lookup"><span data-stu-id="90530-109">**CQPM\_ENABLE**</span></span>](cqpm-enable.md)
-   [<span data-ttu-id="90530-110">**\_Parameters CQPM**</span><span class="sxs-lookup"><span data-stu-id="90530-110">**CQPM\_GETPARAMETERS**</span></span>](cqpm-getparameters.md)
-   [<span data-ttu-id="90530-111">**CQPM \_ HANDLERSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="90530-111">**CQPM\_HANDLERSPECIFIC**</span></span>](cqpm-handlerspecific.md)
-   [<span data-ttu-id="90530-112">**ajuda do CQPM \_**</span><span class="sxs-lookup"><span data-stu-id="90530-112">**CQPM\_HELP**</span></span>](cqpm-help.md)
-   [<span data-ttu-id="90530-113">**CQPM \_ inicializar**</span><span class="sxs-lookup"><span data-stu-id="90530-113">**CQPM\_INITIALIZE**</span></span>](cqpm-initialize.md)
-   [<span data-ttu-id="90530-114">**CQPM \_ persistir**</span><span class="sxs-lookup"><span data-stu-id="90530-114">**CQPM\_PERSIST**</span></span>](cqpm-persist.md)
-   [<span data-ttu-id="90530-115">**\_versão CQPM**</span><span class="sxs-lookup"><span data-stu-id="90530-115">**CQPM\_RELEASE**</span></span>](cqpm-release.md)
-   [<span data-ttu-id="90530-116">**CQPM \_ SETpadrãoparameters**</span><span class="sxs-lookup"><span data-stu-id="90530-116">**CQPM\_SETDEFAULTPARAMETERS**</span></span>](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a><span data-ttu-id="90530-117">Mensagens diversas</span><span class="sxs-lookup"><span data-stu-id="90530-117">Miscellaneous Messages</span></span>

<span data-ttu-id="90530-118">A tabela a seguir lista as mensagens que um serviço de diretório pode enviar.</span><span class="sxs-lookup"><span data-stu-id="90530-118">The following table lists messages that a directory service can send.</span></span>



| <span data-ttu-id="90530-119">Mensagem</span><span class="sxs-lookup"><span data-stu-id="90530-119">Message</span></span>                  | <span data-ttu-id="90530-120">Valor</span><span class="sxs-lookup"><span data-stu-id="90530-120">Value</span></span>                     | <span data-ttu-id="90530-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="90530-121">Description</span></span>                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90530-122">DSPROP \_ ATTRCHANGED \_ msg</span><span class="sxs-lookup"><span data-stu-id="90530-122">DSPROP\_ATTRCHANGED\_MSG</span></span> | <span data-ttu-id="90530-123">"DsPropAttrChanged"</span><span class="sxs-lookup"><span data-stu-id="90530-123">"DsPropAttrChanged"</span></span>       | <span data-ttu-id="90530-124">Uma mensagem enviada para sincronizar páginas de propriedades e as ferramentas de administração do serviço de diretório, declarada em DSClient. h.</span><span class="sxs-lookup"><span data-stu-id="90530-124">A message sent for synchronizing property pages and the directory service administration tools, declared in Dsclient.h.</span></span>                                                                                                                       |
| <span data-ttu-id="90530-125">DSQPM \_ GETclasslist</span><span class="sxs-lookup"><span data-stu-id="90530-125">DSQPM\_GETCLASSLIST</span></span>      | <span data-ttu-id="90530-126">CQPM \_ HANDLERSPECIFIC + 0</span><span class="sxs-lookup"><span data-stu-id="90530-126">CQPM\_HANDLERSPECIFIC+0</span></span>   | <span data-ttu-id="90530-127">Uma mensagem de página enviada para as páginas de formulário para recuperar uma lista de classes para consulta, usada pelo seletor de campo e Propriedade bem para criar sua lista de classes de exibição.</span><span class="sxs-lookup"><span data-stu-id="90530-127">A page message sent to the form pages for retrieving a list of classes for query, used by the field selector and property well to build its list of display classes.</span></span> <span data-ttu-id="90530-128">wParam = flags e lParam = LPLPDSQUERYCLASSLIST, declarados em DSQuery. h.</span><span class="sxs-lookup"><span data-stu-id="90530-128">wParam = flags and lParam = LPLPDSQUERYCLASSLIST, declared in Dsquery.h.</span></span> |
| <span data-ttu-id="90530-129">DSQPM \_ HELPTOPICS</span><span class="sxs-lookup"><span data-stu-id="90530-129">DSQPM\_HELPTOPICS</span></span>        | <span data-ttu-id="90530-130">(CQPM \_ HANDLERSPECIFIC + 1)</span><span class="sxs-lookup"><span data-stu-id="90530-130">(CQPM\_HANDLERSPECIFIC+1)</span></span> | <span data-ttu-id="90530-131">Uma mensagem de página enviada para as páginas de formulário para manipular a solicitação "tópicos da ajuda".</span><span class="sxs-lookup"><span data-stu-id="90530-131">A page message sent to the form pages for handling the "Help Topics" request.</span></span> <span data-ttu-id="90530-132">wParam = 0, lParam = hWndParent, declarado em DSQuery. h.</span><span class="sxs-lookup"><span data-stu-id="90530-132">wParam = 0, lParam = hWndParent, declared in Dsquery.h.</span></span>                                                                                                         |



 

 

 




