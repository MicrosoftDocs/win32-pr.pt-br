---
title: Inserindo o estado passivo
description: Inserindo o estado passivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822950"
---
# <a name="entering-the-passive-state"></a><span data-ttu-id="bfbdc-103">Inserindo o estado passivo</span><span class="sxs-lookup"><span data-stu-id="bfbdc-103">Entering the Passive State</span></span>

<span data-ttu-id="bfbdc-104">O fechamento do objeto força um objeto incorporado ou vinculado ao estado passivo.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-104">Object closure forces an embedded or linked object into the passive state.</span></span> <span data-ttu-id="bfbdc-105">Normalmente, ele é iniciado a partir da interface do usuário do aplicativo de servidor OLE, como quando o usuário seleciona o comando File Close.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-105">It is typically initiated from the OLE server application's user interface, such as when the user selects the File Close command.</span></span> <span data-ttu-id="bfbdc-106">Nesse caso, o aplicativo de servidor OLE notifica o contêiner, que libera sua contagem de referência no objeto.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-106">In this case, the OLE server application notifies the container, which releases its reference count on the object.</span></span> <span data-ttu-id="bfbdc-107">Quando todas as referências ao objeto forem liberadas, o objeto poderá ser liberado.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-107">When all references to the object have been released, the object can be freed.</span></span> <span data-ttu-id="bfbdc-108">Quando todos os objetos forem liberados, o aplicativo do servidor OLE poderá ser encerrado com segurança.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-108">When all objects have been freed, the OLE server application can safely terminate.</span></span>

<span data-ttu-id="bfbdc-109">Um aplicativo de contêiner também pode iniciar o fechamento do objeto.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-109">A container application can also initiate object closure.</span></span> <span data-ttu-id="bfbdc-110">Para fechar um objeto, o contêiner libera sua contagem de referência depois de concluir uma operação de salvamento opcional.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-110">To close an object, the container releases its reference count after completing an optional save operation.</span></span> <span data-ttu-id="bfbdc-111">Você pode criar contêineres para liberar objetos quando eles estiverem sendo desativados após uma sessão de ativação in-loco, permitindo que o usuário clique fora do objeto sem perder a sessão de edição ativa.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-111">You can design containers to release objects when they are deactivating after an in-place activation session, allowing the user to click outside the object without losing the active editing session.</span></span>

 

 




