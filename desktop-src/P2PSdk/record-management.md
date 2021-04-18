---
description: Para gerenciar registros, você pode trabalhar com informações armazenadas em estruturas de registro de pares \_ .
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gerenciamento de registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780938"
---
# <a name="record-management"></a><span data-ttu-id="9d54f-103">Gerenciamento de registros</span><span class="sxs-lookup"><span data-stu-id="9d54f-103">Record Management</span></span>

<span data-ttu-id="9d54f-104">Para gerenciar registros, você pode trabalhar com informações armazenadas em estruturas de [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="9d54f-104">To manage records, you can work with information that is stored in [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structures.</span></span> <span data-ttu-id="9d54f-105">Quando os registros são criados, atualizados ou excluídos, as alterações feitas em um grafo são replicadas para todos os nós.</span><span class="sxs-lookup"><span data-stu-id="9d54f-105">When records are created, updated, or deleted, the changes made to a graph are replicated to all nodes.</span></span> <span data-ttu-id="9d54f-106">A tabela a seguir identifica as regras para atualizar e atualizar automaticamente os registros.</span><span class="sxs-lookup"><span data-stu-id="9d54f-106">The following table identifies the rules for updating and automatically refreshing records.</span></span>



| <span data-ttu-id="9d54f-107">Tarefa de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="9d54f-107">Management Task</span></span>     | <span data-ttu-id="9d54f-108">Regra</span><span class="sxs-lookup"><span data-stu-id="9d54f-108">Rule</span></span>                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d54f-109">Atualizando um registro</span><span class="sxs-lookup"><span data-stu-id="9d54f-109">Updating a record</span></span>   | <span data-ttu-id="9d54f-110">Mantenha o tempo de expiração o mesmo ou aumente.</span><span class="sxs-lookup"><span data-stu-id="9d54f-110">Keep the expiration time the same or increase it.</span></span> <span data-ttu-id="9d54f-111">Não é possível diminuir o tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="9d54f-111">You cannot decrease the expiration time.</span></span>                                                                                                                      |
| <span data-ttu-id="9d54f-112">Atualizando um registro</span><span class="sxs-lookup"><span data-stu-id="9d54f-112">Refreshing a record</span></span> | <span data-ttu-id="9d54f-113">Use o sinalizador de [**registro de pares par \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_record) atualização automática para atualizar automaticamente um registro.</span><span class="sxs-lookup"><span data-stu-id="9d54f-113">Use the [**PEER\_RECORD\_FLAG\_AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) flag to automatically refresh a record.</span></span> <span data-ttu-id="9d54f-114">Use esse sinalizador somente quando o nó que está publicando um registro estiver online.</span><span class="sxs-lookup"><span data-stu-id="9d54f-114">Only use this flag when the node that is publishing a record is online.</span></span> <span data-ttu-id="9d54f-115">Caso contrário, não use esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="9d54f-115">Otherwise, do not use this flag.</span></span> |



 

 

 



