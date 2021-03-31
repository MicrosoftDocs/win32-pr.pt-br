---
title: Objetos e interfaces COM
description: Objetos e interfaces COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634997"
---
# <a name="com-objects-and-interfaces"></a><span data-ttu-id="21b0f-103">Objetos e interfaces COM</span><span class="sxs-lookup"><span data-stu-id="21b0f-103">COM Objects and Interfaces</span></span>

<span data-ttu-id="21b0f-104">O COM é uma tecnologia que permite que os objetos interajam entre os limites do processo e do computador tão facilmente quanto em um único processo.</span><span class="sxs-lookup"><span data-stu-id="21b0f-104">COM is a technology that allows objects to interact across process and computer boundaries as easily as within a single process.</span></span> <span data-ttu-id="21b0f-105">COM habilita isso especificando que a única maneira de manipular os dados associados a um objeto é por meio de uma *interface* no objeto.</span><span class="sxs-lookup"><span data-stu-id="21b0f-105">COM enables this by specifying that the only way to manipulate the data associated with an object is through an *interface* on the object.</span></span> <span data-ttu-id="21b0f-106">Quando este termo é usado nesta documentação, ele se refere a uma implementação no código de uma interface compatível com binário com, que está associada a um objeto.</span><span class="sxs-lookup"><span data-stu-id="21b0f-106">When this term is used in this documentation, it refers to an implementation in code of a COM binary-compliant interface that is associated with an object.</span></span>

<span data-ttu-id="21b0f-107">O COM usa a *interface* do Word de forma diferente da que normalmente é usada em Visual C++ programação.</span><span class="sxs-lookup"><span data-stu-id="21b0f-107">COM uses the word *interface* in a sense different from that typically used in Visual C++ programming.</span></span> <span data-ttu-id="21b0f-108">Uma interface C++ refere-se a todas as funções às quais uma classe dá suporte e que os clientes de um objeto podem chamar para interagir com ela.</span><span class="sxs-lookup"><span data-stu-id="21b0f-108">A C++ interface refers to all of the functions that a class supports and that clients of an object can call to interact with it.</span></span> <span data-ttu-id="21b0f-109">Uma interface COM refere-se a um grupo predefinido de funções relacionadas que uma classe COM implementa, mas uma interface específica não representa necessariamente todas as funções às quais a classe dá suporte.</span><span class="sxs-lookup"><span data-stu-id="21b0f-109">A COM interface refers to a predefined group of related functions that a COM class implements, but a specific interface does not necessarily represent all the functions that the class supports.</span></span>

<span data-ttu-id="21b0f-110">Fazer referência a um objeto que *implementa* uma interface significa que o objeto usa código que implementa cada método da interface e fornece ponteiros compatíveis com binários com para essas funções para a biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="21b0f-110">Referring to an object *implementing* an interface means that the object uses code that implements each method of the interface and provides COM binary-compliant pointers to those functions to the COM library.</span></span> <span data-ttu-id="21b0f-111">COM, o COM torna essas funções disponíveis para qualquer cliente que solicite um ponteiro para a interface, se o cliente está dentro ou fora do processo que implementa essas funções.</span><span class="sxs-lookup"><span data-stu-id="21b0f-111">COM then makes those functions available to any client who asks for a pointer to the interface, whether the client is inside or outside of the process that implements those functions.</span></span>

<span data-ttu-id="21b0f-112">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="21b0f-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="21b0f-113">Interfaces e implementações de interface</span><span class="sxs-lookup"><span data-stu-id="21b0f-113">Interfaces and Interface Implementations</span></span>](interfaces-and-interface-implementations.md)
-   [<span data-ttu-id="21b0f-114">Ponteiros de interface e interfaces</span><span class="sxs-lookup"><span data-stu-id="21b0f-114">Interface Pointers and Interfaces</span></span>](interface-pointers-and-interfaces.md)
-   [<span data-ttu-id="21b0f-115">IUnknown e herança de interface</span><span class="sxs-lookup"><span data-stu-id="21b0f-115">IUnknown and Interface Inheritance</span></span>](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a><span data-ttu-id="21b0f-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="21b0f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21b0f-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="21b0f-117">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 




