---
description: Se o seu provedor de rede precisar dar suporte à navegação de seus recursos de rede, ele deverá implementar as funções a seguir. O MPR chama essas funções para enumerar os recursos.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Funções de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010430"
---
# <a name="enumeration-functions"></a><span data-ttu-id="2a0a0-104">Funções de enumeração</span><span class="sxs-lookup"><span data-stu-id="2a0a0-104">Enumeration Functions</span></span>

<span data-ttu-id="2a0a0-105">Se o seu provedor de rede precisar dar suporte à navegação de seus recursos de rede, ele deverá implementar as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a0a0-105">If your network provider needs to support browsing of its network resources, it should implement the following functions.</span></span> <span data-ttu-id="2a0a0-106">O MPR chama essas funções para enumerar os recursos.</span><span class="sxs-lookup"><span data-stu-id="2a0a0-106">MPR calls these functions to enumerate the resources.</span></span>

<span data-ttu-id="2a0a0-107">Um provedor de rede não é necessário para implementar nenhuma das funções de enumeração.</span><span class="sxs-lookup"><span data-stu-id="2a0a0-107">A network provider is not required to implement any of the enumeration functions.</span></span> <span data-ttu-id="2a0a0-108">No entanto, se um provedor de rede implementar [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)ou [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), ele também deverá implementar as outras duas funções de enumeração.</span><span class="sxs-lookup"><span data-stu-id="2a0a0-108">If, however, a network provider implements either [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), or [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), it must also implement the other two enumeration functions.</span></span>



| <span data-ttu-id="2a0a0-109">Função</span><span class="sxs-lookup"><span data-stu-id="2a0a0-109">Function</span></span>                                                     | <span data-ttu-id="2a0a0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a0a0-110">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a0a0-111">**NPOpenEnum**</span><span class="sxs-lookup"><span data-stu-id="2a0a0-111">**NPOpenEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | <span data-ttu-id="2a0a0-112">Abre uma enumeração de recursos de rede ou conexões existentes.</span><span class="sxs-lookup"><span data-stu-id="2a0a0-112">Opens an enumeration of network resources or existing connections.</span></span>                                                                                                  |
| [<span data-ttu-id="2a0a0-113">**NPEnumResource**</span><span class="sxs-lookup"><span data-stu-id="2a0a0-113">**NPEnumResource**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | <span data-ttu-id="2a0a0-114">Executa uma enumeração em um identificador retornado por [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span><span class="sxs-lookup"><span data-stu-id="2a0a0-114">Performs an enumeration on a handle returned by [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span></span>                                                                                   |
| [<span data-ttu-id="2a0a0-115">**NPCloseEnum**</span><span class="sxs-lookup"><span data-stu-id="2a0a0-115">**NPCloseEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | <span data-ttu-id="2a0a0-116">Fecha uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="2a0a0-116">Closes an enumeration.</span></span>                                                                                                                                              |
| [<span data-ttu-id="2a0a0-117">**NPGetResourceInformation**</span><span class="sxs-lookup"><span data-stu-id="2a0a0-117">**NPGetResourceInformation**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | <span data-ttu-id="2a0a0-118">Determina se o provedor é o provedor correto para responder a uma solicitação de um recurso de rede especificado e retorna informações sobre o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="2a0a0-118">Determines whether the provider is the correct provider to respond to a request for a specified network resource and returns information about the resource's type.</span></span> |
| [<span data-ttu-id="2a0a0-119">**NPGetResourceParent**</span><span class="sxs-lookup"><span data-stu-id="2a0a0-119">**NPGetResourceParent**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | <span data-ttu-id="2a0a0-120">Retorna o pai de um recurso de rede especificado na hierarquia de procura.</span><span class="sxs-lookup"><span data-stu-id="2a0a0-120">Returns the parent of a specified network resource in the browse hierarchy.</span></span>                                                                                         |



 

 

 



