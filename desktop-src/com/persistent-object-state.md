---
title: Estado de objeto persistente
description: Estado de objeto persistente
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291934"
---
# <a name="persistent-object-state"></a><span data-ttu-id="f989d-103">Estado de objeto persistente</span><span class="sxs-lookup"><span data-stu-id="f989d-103">Persistent Object State</span></span>

<span data-ttu-id="f989d-104">Alguns objetos COM podem salvar seu estado interno quando solicitados a fazer isso por um cliente.</span><span class="sxs-lookup"><span data-stu-id="f989d-104">Some COM objects can save their internal state when asked to do so by a client.</span></span>

<span data-ttu-id="f989d-105">COM define padrões por meio dos quais os clientes podem solicitar que os objetos sejam inicializados, carregados e salvos em e de um armazenamento de dados (por exemplo, arquivo simples, armazenamento estruturado ou memória).</span><span class="sxs-lookup"><span data-stu-id="f989d-105">COM defines standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="f989d-106">É responsabilidade do cliente gerenciar o local onde os dados persistentes do objeto são armazenados, mas não o formato dos dados.</span><span class="sxs-lookup"><span data-stu-id="f989d-106">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span> <span data-ttu-id="f989d-107">Objetos COM que aderem a esses padrões são chamados de *objetos persistentes*.</span><span class="sxs-lookup"><span data-stu-id="f989d-107">COM objects that adhere to these standards are called *persistent objects*.</span></span>

<span data-ttu-id="f989d-108">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f989d-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f989d-109">Interfaces de objeto persistentes</span><span class="sxs-lookup"><span data-stu-id="f989d-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
-   [<span data-ttu-id="f989d-110">Inicializando objetos persistentes</span><span class="sxs-lookup"><span data-stu-id="f989d-110">Initializing Persistent Objects</span></span>](initializing-persistent-objects.md)

## <a name="related-topics"></a><span data-ttu-id="f989d-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f989d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f989d-112">Clientes e servidores COM</span><span class="sxs-lookup"><span data-stu-id="f989d-112">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




