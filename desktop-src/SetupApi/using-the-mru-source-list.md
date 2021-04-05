---
description: A função SetupSetSourceList será aberta ou criará uma lista de origem no sistema de usuários.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Usando a lista de origem MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921405"
---
# <a name="using-the-mru-source-list"></a><span data-ttu-id="a0b5f-103">Usando a lista de origem MRU</span><span class="sxs-lookup"><span data-stu-id="a0b5f-103">Using the MRU Source List</span></span>

<span data-ttu-id="a0b5f-104">A função [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) será aberta ou criará uma lista de origem no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0b5f-104">The [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) function will open or create a source list on the user's system.</span></span> <span data-ttu-id="a0b5f-105">Você pode especificar para definir a lista de usuários, a lista do sistema, uma combinação das listas de usuários e do sistema ou uma lista temporária como a lista de origem do MRU.</span><span class="sxs-lookup"><span data-stu-id="a0b5f-105">You can specify to set the user list, the system list, a combination of the user and system lists, or a temporary list as the MRU source list.</span></span> <span data-ttu-id="a0b5f-106">Se uma lista temporária for usada, ela será a única lista disponível para o aplicativo de instalação até que [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) seja chamado ou **SetupSetSourceList** seja chamado uma segunda vez.</span><span class="sxs-lookup"><span data-stu-id="a0b5f-106">If a temporary list is used, it will be the only list available to the setup application until [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) is called, or **SetupSetSourceList** is called a second time.</span></span>

<span data-ttu-id="a0b5f-107">Depois que uma lista é definida, você pode consultar a lista de origem usando [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) para obter uma matriz dos caminhos de origem.</span><span class="sxs-lookup"><span data-stu-id="a0b5f-107">After a list is set, you can query the source list by using [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) to obtain an array of the source paths.</span></span> <span data-ttu-id="a0b5f-108">Quando a matriz da lista de origem não for mais necessária, você deverá chamar a função [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) para liberar os recursos alocados pelo [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span><span class="sxs-lookup"><span data-stu-id="a0b5f-108">When the source list array is no longer needed, you must call the [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) function to free the resources allocated by [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span></span>

<span data-ttu-id="a0b5f-109">Para adicionar um caminho a uma lista de origem, seja um que seja residente no sistema do usuário ou uma lista temporária, chame [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span><span class="sxs-lookup"><span data-stu-id="a0b5f-109">To add a path to a source list, either one that is resident on the user's system, or a temporary list, call [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span></span> <span data-ttu-id="a0b5f-110">Se a lista de origem especificada não for temporária, essa fonte permanecerá no sistema do usuário e poderá ser acessada por instalações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a0b5f-110">If the source list specified is not temporary, that source will remain on the user's system and is accessible to subsequent installations.</span></span>

<span data-ttu-id="a0b5f-111">Para remover um caminho do caminho de origem, chame a função [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .</span><span class="sxs-lookup"><span data-stu-id="a0b5f-111">To remove a path from the source path, call the [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) function.</span></span>

 

 



