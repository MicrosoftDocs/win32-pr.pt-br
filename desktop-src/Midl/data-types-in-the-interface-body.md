---
title: Tipos de dados no corpo da interface
description: O corpo da interface, que é colocado entre chaves (), contém os tipos de dados que serão usados em chamadas de procedimento remoto e protótipos para as funções que serão executadas remotamente.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- MIDL de interfaces, tipos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757798"
---
# <a name="data-types-in-the-interface-body"></a><span data-ttu-id="5bc91-104">Tipos de dados no corpo da interface</span><span class="sxs-lookup"><span data-stu-id="5bc91-104">Data Types in the Interface Body</span></span>

<span data-ttu-id="5bc91-105">O corpo da interface, que está entre chaves ({}), contém os tipos de dados que serão usados em chamadas de procedimento remoto e protótipos para as funções que serão executadas remotamente.</span><span class="sxs-lookup"><span data-stu-id="5bc91-105">The interface body, which is enclosed in braces ({ }), contains the data types that will be used in remote procedure calls and prototypes for the functions that will be executed remotely.</span></span> <span data-ttu-id="5bc91-106">Um corpo de interface pode conter importações, pragmas, declarações constantes, declarações de tipo e declarações de função.</span><span class="sxs-lookup"><span data-stu-id="5bc91-106">An interface body can contain imports, pragmas, constant declarations, type declarations, and function declarations.</span></span> <span data-ttu-id="5bc91-107">Exceto no modo de compatibilidade com uso, o compilador MIDL também permite declarações implícitas na forma de definições de variáveis.</span><span class="sxs-lookup"><span data-stu-id="5bc91-107">Except in OSF-compatibility mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="5bc91-108">Observe que a especificação uso-DCE para interfaces RPC não permite várias interfaces em um único arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5bc91-108">Note that the OSF-DCE specification for RPC interfaces does not allow multiple interfaces in a single IDL file.</span></span> <span data-ttu-id="5bc91-109">Portanto, se você estiver compilando no modo de compatibilidade uso ( [**/OSF**](-osf.md)) do MIDL, o arquivo IDL poderá conter apenas uma interface.</span><span class="sxs-lookup"><span data-stu-id="5bc91-109">Therefore, if you are compiling in MIDL's OSF-compatibility mode ( [**/osf**](-osf.md)), your IDL file can contain only one interface.</span></span>

<span data-ttu-id="5bc91-110">Para obter detalhes sobre como usar o compilador MIDL para produzir bibliotecas de tipos, consulte [gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md).</span><span class="sxs-lookup"><span data-stu-id="5bc91-110">For details on using the MIDL compiler to produce type libraries, see [Generating a Type Library with MIDL](generating-a-type-library-with-midl-2.md).</span></span>

<span data-ttu-id="5bc91-111">No Microsoft RPC, um arquivo IDL pode conter várias interfaces e essas interfaces podem ser encaminhadas declaradas (dentro do arquivo IDL que as define).</span><span class="sxs-lookup"><span data-stu-id="5bc91-111">In Microsoft RPC, an IDL file can contain multiple interfaces and these interfaces can be forward declared (within the IDL file that defines them).</span></span> <span data-ttu-id="5bc91-112">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5bc91-112">For example:</span></span>

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




