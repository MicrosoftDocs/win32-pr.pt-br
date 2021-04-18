---
title: Reutilizando objetos
description: Reutilizando objetos
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/08/2020
ms.locfileid: "104499013"
---
# <a name="reusing-objects"></a><span data-ttu-id="51d73-103">Reutilizando objetos</span><span class="sxs-lookup"><span data-stu-id="51d73-103">Reusing Objects</span></span>

<span data-ttu-id="51d73-104">Um objetivo importante de qualquer modelo de objeto é permitir que os autores de objetos reutilizem e estendam objetos fornecidos por outras pessoas como partes de suas próprias implementações.</span><span class="sxs-lookup"><span data-stu-id="51d73-104">An important goal of any object model is to enable object authors to reuse and extend objects provided by others as pieces of their own implementations.</span></span> <span data-ttu-id="51d73-105">Uma maneira de fazer isso na Microsoft Visual C++ e em outras linguagens é usar a *herança de implementação*, que permite que um objeto herde ("subclasse") algumas de suas funções de outro objeto ao substituir outras funções.</span><span class="sxs-lookup"><span data-stu-id="51d73-105">One way to do this in Microsoft Visual C++ and other languages is by using *implementation inheritance*, which allows an object to inherit ("subclass") some of its functions from another object while overriding other functions.</span></span>

<span data-ttu-id="51d73-106">O problema para a interação de objetos de todo o uso da herança de implementação tradicional é que o contrato (a interface) entre objetos em uma hierarquia de implementação não é claramente definido.</span><span class="sxs-lookup"><span data-stu-id="51d73-106">The problem for systemwide object interaction using traditional implementation inheritance is that the contract (the interface) between objects in an implementation hierarchy is not clearly defined.</span></span> <span data-ttu-id="51d73-107">Na verdade, ele é implícito e ambíguo.</span><span class="sxs-lookup"><span data-stu-id="51d73-107">In fact, it is implicit and ambiguous.</span></span> <span data-ttu-id="51d73-108">Quando o objeto pai ou filho altera sua implementação, o comportamento dos componentes relacionados pode se tornar indefinido ou unstably implementado.</span><span class="sxs-lookup"><span data-stu-id="51d73-108">When the parent or child object changes its implementation, the behavior of related components might become undefined or unstably implemented.</span></span> <span data-ttu-id="51d73-109">Em qualquer aplicativo único, onde a implementação pode ser gerenciada por uma única equipe de engenharia que atualiza todos os componentes ao mesmo tempo, isso nem sempre é uma grande preocupação.</span><span class="sxs-lookup"><span data-stu-id="51d73-109">In any single application, where the implementation can be managed by a single engineering team that updates all of the components at the same time, this is not always a major concern.</span></span> <span data-ttu-id="51d73-110">Em um ambiente em que os componentes de uma equipe são criados por meio da reutilização da caixa preta de outros componentes criados por outras equipes, esse tipo de instabilidade compromete a reutilização.</span><span class="sxs-lookup"><span data-stu-id="51d73-110">In an environment where the components of one team are built through black-box reuse of other components built by other teams, this type of instability jeopardizes reuse.</span></span> <span data-ttu-id="51d73-111">Além disso, a herança de implementação geralmente funciona apenas dentro dos limites do processo.</span><span class="sxs-lookup"><span data-stu-id="51d73-111">Additionally, implementation inheritance usually works only within process boundaries.</span></span> <span data-ttu-id="51d73-112">Isso torna a herança de implementação tradicional impraticável para sistemas grandes e em evolução compostos por componentes de software criados por muitas equipes de engenharia.</span><span class="sxs-lookup"><span data-stu-id="51d73-112">This makes traditional implementation inheritance impractical for large, evolving systems composed of software components built by many engineering teams.</span></span>

<span data-ttu-id="51d73-113">A chave para a criação de componentes reutilizáveis é poder tratar o objeto como uma caixa opaca.</span><span class="sxs-lookup"><span data-stu-id="51d73-113">The key to building reusable components is to be able to treat the object as an opaque box.</span></span> <span data-ttu-id="51d73-114">Isso significa que a parte do código que tenta reutilizar outro objeto não sabe nada e precisa saber nada, sobre a estrutura interna ou a implementação do componente que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="51d73-114">This means that the piece of code attempting to reuse another object knows nothing, and needs to know nothing, about the internal structure or implementation of the component being used.</span></span> <span data-ttu-id="51d73-115">Em outras palavras, o código que tenta reutilizar um componente depende do comportamento do objeto e não da sua implementação exata.</span><span class="sxs-lookup"><span data-stu-id="51d73-115">In other words, the code attempting to reuse a component depends on the behavior of the object and not its exact implementation.</span></span>

<span data-ttu-id="51d73-116">Para obter a reutilização de caixa preta, o COM adota outros mecanismos de reusabilidade estabelecidos, como *contenção/delegação* e *agregação*.</span><span class="sxs-lookup"><span data-stu-id="51d73-116">To achieve black-box reusability, COM adopts other established reusability mechanisms such as *containment/delegation* and *aggregation*.</span></span>

> [!NOTE]  
> <span data-ttu-id="51d73-117">Para sua conveniência, o objeto que está sendo reutilizado é chamado de *objeto interno* e o objeto que faz uso desse objeto interno é o *objeto externo*.</span><span class="sxs-lookup"><span data-stu-id="51d73-117">For convenience, the object being reused is called the *inner object* and the object making use of that inner object is the *outer object*.</span></span>

 

<span data-ttu-id="51d73-118">É importante lembrar-se de ambos os mecanismos como o objeto externo aparece para seus clientes.</span><span class="sxs-lookup"><span data-stu-id="51d73-118">It is important to remember in both these mechanisms how the outer object appears to its clients.</span></span> <span data-ttu-id="51d73-119">No que diz respeito aos clientes, ambos os objetos implementam qualquer interface para a qual o cliente possa obter um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="51d73-119">As far as the clients are concerned, both objects implement any interfaces to which the client can get a pointer.</span></span> <span data-ttu-id="51d73-120">O cliente trata o objeto externo como uma caixa opaca e, portanto, não se importa, nem precisa se preocupar com a estrutura interna do objectâ externo. "o cliente se preocupa apenas com o comportamento.</span><span class="sxs-lookup"><span data-stu-id="51d73-120">The client treats the outer object as an opaque box and therefore does not care, nor does it need to care, about the internal structure of the outer objectâ€”the client cares only about behavior.</span></span>

<span data-ttu-id="51d73-121">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="51d73-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="51d73-122">Contenção/delegação</span><span class="sxs-lookup"><span data-stu-id="51d73-122">Containment/Delegation</span></span>](containment-delegation.md)
-   [<span data-ttu-id="51d73-123">Agregação</span><span class="sxs-lookup"><span data-stu-id="51d73-123">Aggregation</span></span>](aggregation.md)

 

 




