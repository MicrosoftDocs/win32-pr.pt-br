---
title: Desvantagens
description: Desvantagens
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498783"
---
# <a name="disadvantages"></a><span data-ttu-id="1067c-103">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="1067c-103">Disadvantages</span></span>

<span data-ttu-id="1067c-104">Os servidores em processo fornecem a velocidade e a vantagem do tamanho de um manipulador de objetos com a capacidade de edição de um servidor local.</span><span class="sxs-lookup"><span data-stu-id="1067c-104">In-process servers provide the speed and size advantage of an object handler with the editing capability of a local server.</span></span> <span data-ttu-id="1067c-105">Então, por que você iria optar por implementar seu aplicativo OLE como um servidor local em vez de um servidor em processo?</span><span class="sxs-lookup"><span data-stu-id="1067c-105">So why would you ever choose to implement your OLE application as a local server rather than an in-process server?</span></span> <span data-ttu-id="1067c-106">Há vários motivos:</span><span class="sxs-lookup"><span data-stu-id="1067c-106">There are several reasons:</span></span>

-   <span data-ttu-id="1067c-107">Segurança.</span><span class="sxs-lookup"><span data-stu-id="1067c-107">Security.</span></span> <span data-ttu-id="1067c-108">Somente um servidor local tem seu espaço de endereço isolado do cliente.</span><span class="sxs-lookup"><span data-stu-id="1067c-108">Only a local server has its address space isolated from that of the client.</span></span> <span data-ttu-id="1067c-109">Um servidor em processo compartilha o espaço de endereço e o contexto do processo do cliente e, portanto, pode ser menos robusto diante de falhas ou programação mal-intencionada.</span><span class="sxs-lookup"><span data-stu-id="1067c-109">An in-process server shares the address space and process context of the client and can therefore be less robust in the face of faults or malicious programming.</span></span>
-   <span data-ttu-id="1067c-110">Granularidade.</span><span class="sxs-lookup"><span data-stu-id="1067c-110">Granularity.</span></span> <span data-ttu-id="1067c-111">Um servidor local pode hospedar várias instâncias de seu objeto em vários clientes diferentes, compartilhando o estado do servidor entre objetos em vários clientes de maneiras que seriam difíceis ou impossíveis se implementadas como um servidor em processo, que é simplesmente uma DLL carregada em cada cliente.</span><span class="sxs-lookup"><span data-stu-id="1067c-111">A local server can host multiple instances of its object across many different clients, sharing server state between objects in multiple clients in ways that would be difficult or impossible if implemented as an in-process server, which is simply a DLL loaded into each client.</span></span>
-   <span data-ttu-id="1067c-112">Compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="1067c-112">Compatibility.</span></span> <span data-ttu-id="1067c-113">Se você optar por implementar um servidor em processo, você cederá a compatibilidade com o OLE 1, que não oferece suporte a esses servidores.</span><span class="sxs-lookup"><span data-stu-id="1067c-113">If you choose to implement an in-process server, you relinquish compatibility with OLE 1, which does not support such servers.</span></span> <span data-ttu-id="1067c-114">Isso não será uma consideração para muitos desenvolvedores, mas, se for, será uma preocupação importante.</span><span class="sxs-lookup"><span data-stu-id="1067c-114">This will not be a consideration for many developers, but if it is, then it is of critical concern.</span></span>
-   <span data-ttu-id="1067c-115">Incapacidade de dar suporte a links.</span><span class="sxs-lookup"><span data-stu-id="1067c-115">Inability to support links.</span></span> <span data-ttu-id="1067c-116">Um servidor em processo não pode servir como uma fonte de link.</span><span class="sxs-lookup"><span data-stu-id="1067c-116">An in-process server cannot serve as a link source.</span></span> <span data-ttu-id="1067c-117">Como uma DLL não pode ser executada por si só, não é possível criar um objeto de arquivo a ser vinculado.</span><span class="sxs-lookup"><span data-stu-id="1067c-117">Since a DLL cannot run by itself, it cannot create a file object to be linked to.</span></span>

<span data-ttu-id="1067c-118">Apesar dessas desvantagens, um servidor em processo pode ser uma opção excelente para sua velocidade e tamanho — se atender a todos os seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="1067c-118">Despite these disadvantages, an in-process server can be an excellent choice for its speed and size — if it fits all your other requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1067c-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1067c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1067c-120">Vantagens</span><span class="sxs-lookup"><span data-stu-id="1067c-120">Advantages</span></span>](advantages.md)
</dt> <dt>

[<span data-ttu-id="1067c-121">Servidores em processo</span><span class="sxs-lookup"><span data-stu-id="1067c-121">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




