---
title: O manipulador padrão e os manipuladores personalizados
description: O manipulador padrão e os manipuladores personalizados
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916095"
---
# <a name="the-default-handler-and-custom-handlers"></a><span data-ttu-id="8ab9b-103">O manipulador padrão e os manipuladores personalizados</span><span class="sxs-lookup"><span data-stu-id="8ab9b-103">The Default Handler and Custom Handlers</span></span>

<span data-ttu-id="8ab9b-104">O manipulador padrão, uma implementação fornecida pelo OLE, é usado pela maioria dos aplicativos como o manipulador.</span><span class="sxs-lookup"><span data-stu-id="8ab9b-104">The default handler, an implementation provided by OLE, is used by most applications as the handler.</span></span> <span data-ttu-id="8ab9b-105">Um aplicativo implementa um manipulador personalizado quando os recursos do manipulador padrão são insuficientes.</span><span class="sxs-lookup"><span data-stu-id="8ab9b-105">An application implements a custom handler when the default handler's capabilities are insufficient.</span></span> <span data-ttu-id="8ab9b-106">Um manipulador personalizado pode substituir completamente o manipulador padrão ou usar partes da funcionalidade que ele fornece quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="8ab9b-106">A custom handler can either completely replace the default handler or use parts of the functionality it provides where appropriate.</span></span> <span data-ttu-id="8ab9b-107">No último caso, o manipulador de aplicativos é implementado como um objeto de agregação composto por um novo objeto de controle e o manipulador padrão.</span><span class="sxs-lookup"><span data-stu-id="8ab9b-107">In the latter case, the application handler is implemented as an aggregate object composed of a new control object and the default handler.</span></span> <span data-ttu-id="8ab9b-108">Os manipuladores de aplicativo/padrão de combinação também são conhecidos como *manipuladores em processo*.</span><span class="sxs-lookup"><span data-stu-id="8ab9b-108">Combination application/default handlers are also known as *in-process handlers*.</span></span> <span data-ttu-id="8ab9b-109">O *manipulador de comunicação remota* é usado para objetos que não são atribuídos a um CLSID no registro do sistema ou que não têm nenhum manipulador especificado.</span><span class="sxs-lookup"><span data-stu-id="8ab9b-109">The *remoting handler* is used for objects that are not assigned a CLSID in the system registry or that have no specified handler.</span></span> <span data-ttu-id="8ab9b-110">Tudo o que é necessário a partir de um manipulador para esses tipos de objetos é que eles passam informações entre o limite do processo.</span><span class="sxs-lookup"><span data-stu-id="8ab9b-110">All that is required from a handler for these types of objects is that they pass information across the process boundary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ab9b-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ab9b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ab9b-112">Manipuladores de objetos</span><span class="sxs-lookup"><span data-stu-id="8ab9b-112">Object Handlers</span></span>](object-handlers.md)
</dt> </dl>

 

 




