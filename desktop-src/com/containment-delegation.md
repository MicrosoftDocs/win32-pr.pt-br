---
title: Contenção/delegação
description: O mecanismo mais comum para reutilização de objeto em COM é contenção/delegação.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292778"
---
# <a name="containmentdelegation"></a><span data-ttu-id="4a6e5-103">Contenção/delegação</span><span class="sxs-lookup"><span data-stu-id="4a6e5-103">Containment/Delegation</span></span>

<span data-ttu-id="4a6e5-104">O mecanismo mais comum para reutilização de objeto em COM é *contenção/delegação*.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-104">The most common mechanism for object reuse in COM is *containment/delegation*.</span></span> <span data-ttu-id="4a6e5-105">Esse tipo de reutilização é um conceito familiar encontrado na maioria das linguagens e sistemas orientados a objetos.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-105">This type of reuse is a familiar concept found in most object-oriented languages and systems.</span></span> <span data-ttu-id="4a6e5-106">O objeto externo, que precisa fazer uso do objeto interno, atua como um cliente de objeto para o objeto interno.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-106">The outer object, which needs to make use of the inner object, acts as an object client to the inner object.</span></span> <span data-ttu-id="4a6e5-107">O objeto externo "contém" o objeto interno e, quando o objeto externo requer os serviços do objeto interno, o objeto externo delega a implementação explicitamente para os métodos do objeto interno.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-107">The outer object "contains" the inner object, and when the outer object requires the services of the inner object, the outer object explicitly delegates implementation to the inner object's methods.</span></span> <span data-ttu-id="4a6e5-108">Ou seja, o objeto externo usa os serviços do objeto interno para implementar a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-108">That is, the outer object uses the inner object's services to implement itself.</span></span>

<span data-ttu-id="4a6e5-109">Não é necessário que os objetos externos e internos ofereçam suporte às mesmas interfaces, embora certamente seja razoável conter um objeto que implemente uma interface que o objeto externo não e implemente os métodos do objeto externo simplesmente como chamadas para os métodos correspondentes no objeto interno.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-109">It is not necessary for the outer and inner objects to support the same interfaces, although it certainly is reasonable to contain an object that implements an interface that the outer object does not and implement the methods of the outer object simply as calls to the corresponding methods in the inner object.</span></span> <span data-ttu-id="4a6e5-110">No entanto, quando a complexidade dos objetos externos e internos difere muito, o objeto externo pode implementar alguns dos métodos de suas interfaces delegando chamadas para métodos de interface implementados no objeto interno.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-110">When the complexity of the outer and inner objects differs greatly, however, the outer object may implement some of the methods of its interfaces by delegating calls to interface methods implemented in the inner object.</span></span>

<span data-ttu-id="4a6e5-111">É simples implementar a contenção de um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-111">It is simple to implement containment for an outer object.</span></span> <span data-ttu-id="4a6e5-112">O objeto externo cria os objetos internos que ele precisa para usar como faria com qualquer outro cliente.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-112">The outer object creates the inner objects it needs to use as any other client would.</span></span> <span data-ttu-id="4a6e5-113">Isso não é nada novo – o processo é como um objeto C++ que, por sua vez, contém um objeto de cadeia de caracteres C++ que ele usa para executar determinadas funções de cadeia de caracteres, mesmo que o objeto externo não seja considerado um objeto de cadeia de caracteres em seu próprio direito.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-113">This is nothing new—the process is like a C++ object that itself contains a C++ string object that it uses to perform certain string functions, even if the outer object is not considered a string object in its own right.</span></span> <span data-ttu-id="4a6e5-114">Em seguida, usando seu ponteiro para o objeto interno, uma chamada para um método no objeto externo gera uma chamada para um método de objeto interno.</span><span class="sxs-lookup"><span data-stu-id="4a6e5-114">Then, using its pointer to the inner object, a call to a method in the outer object generates a call to an inner object method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a6e5-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a6e5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a6e5-116">Agregação</span><span class="sxs-lookup"><span data-stu-id="4a6e5-116">Aggregation</span></span>](aggregation.md)
</dt> </dl>

 

 




