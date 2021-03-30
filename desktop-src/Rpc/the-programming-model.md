---
title: O modelo de programação
description: Nos primórdios da programação do computador, cada programa foi escrito como uma grande parte monolítica, preenchida com instruções GoTo.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636033"
---
# <a name="the-programming-model"></a><span data-ttu-id="c9efb-103">O modelo de programação</span><span class="sxs-lookup"><span data-stu-id="c9efb-103">The Programming Model</span></span>

<span data-ttu-id="c9efb-104">Nos primórdios da programação do computador, cada programa foi escrito como uma grande parte monolítica, preenchida com instruções **goto** .</span><span class="sxs-lookup"><span data-stu-id="c9efb-104">In the early days of computer programming, each program was written as a large monolithic chunk, filled with **goto** statements.</span></span> <span data-ttu-id="c9efb-105">Cada programa tinha que gerenciar sua própria entrada e saída para diferentes dispositivos de hardware.</span><span class="sxs-lookup"><span data-stu-id="c9efb-105">Each program had to manage its own input and output to different hardware devices.</span></span> <span data-ttu-id="c9efb-106">À medida que a disciplina de programação amadureceu, esse código monolítico foi organizado em procedimentos, com os procedimentos mais usados empacotados em bibliotecas para compartilhamento e reutilização.</span><span class="sxs-lookup"><span data-stu-id="c9efb-106">As the programming discipline matured, this monolithic code was organized into procedures, with the most commonly used procedures packed in libraries for sharing and reuse.</span></span>

![instruções GoTo monolíticos versus procedimentos empacotados em bibliotecas compartilhadas](images/prog-a06.png)

<span data-ttu-id="c9efb-108">A linguagem de programação C dá suporte à programação orientada por procedimento.</span><span class="sxs-lookup"><span data-stu-id="c9efb-108">The C programming language supports procedure-oriented programming.</span></span> <span data-ttu-id="c9efb-109">Em C, o procedimento principal está relacionado a todos os outros procedimentos como caixas pretas.</span><span class="sxs-lookup"><span data-stu-id="c9efb-109">In C, the main procedure relates to all other procedures as black boxes.</span></span> <span data-ttu-id="c9efb-110">Por exemplo, o procedimento principal não consegue descobrir como os procedimentos A, B e X fazem seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9efb-110">For example, the main procedure cannot find out how procedures A, B, and X do their work.</span></span> <span data-ttu-id="c9efb-111">O procedimento principal só chama outro procedimento; Ele não tem informações sobre como esse procedimento é implementado.</span><span class="sxs-lookup"><span data-stu-id="c9efb-111">The main procedure only calls another procedure; it has no information about how that procedure is implemented.</span></span>

![isolamento de atividades executadas em procedimentos externos](images/prog-a08.png)

<span data-ttu-id="c9efb-113">Linguagens de programação orientadas a procedimento fornecem mecanismos simples para especificar e escrever procedimentos.</span><span class="sxs-lookup"><span data-stu-id="c9efb-113">Procedure-oriented programming languages provide simple mechanisms for specifying and writing procedures.</span></span> <span data-ttu-id="c9efb-114">Por exemplo, o protótipo de função C-padrão ANSI é um constructo usado para especificar o nome de um procedimento, o tipo do resultado que ele retorna (se houver) e o número, a sequência e o tipo de seus parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c9efb-114">For example, the ANSI-standard C-function prototype is a construct used to specify the name of a procedure, the type of the result it returns (if any) and the number, sequence, and type of its parameters.</span></span> <span data-ttu-id="c9efb-115">Usar o protótipo de função é uma maneira formal de especificar uma interface entre procedimentos.</span><span class="sxs-lookup"><span data-stu-id="c9efb-115">Using the function prototype is a formal way to specify an interface between procedures.</span></span>

<span data-ttu-id="c9efb-116">O Microsoft RPC se baseia nesse modelo de programação, permitindo que os procedimentos, agrupados em interfaces, residam em processos diferentes do chamador.</span><span class="sxs-lookup"><span data-stu-id="c9efb-116">Microsoft RPC builds on that programming model by allowing procedures, grouped together in interfaces, to reside in different processes than the caller.</span></span> <span data-ttu-id="c9efb-117">O Microsoft RPC também adiciona uma abordagem mais formal à definição de procedimento que permite que o chamador e a rotina chamada adotem um contrato para a troca remota de dados e a invocação de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="c9efb-117">Microsoft RPC also adds a more formal approach to procedure definition that allows the caller and the called routine to adopt a contract for remotely exchanging data and invoking functionality.</span></span> <span data-ttu-id="c9efb-118">No modelo de programação RPC da Microsoft, as chamadas de função tradicionais são complementadas com dois elementos adicionais.</span><span class="sxs-lookup"><span data-stu-id="c9efb-118">In the Microsoft RPC programming model, traditional function calls are supplemented with two additional elements.</span></span>

-   <span data-ttu-id="c9efb-119">O primeiro elemento é um arquivo. idl/. ACF que descreve precisamente a troca de dados e o mecanismo de passagem de parâmetros entre o chamador e o procedimento chamado.</span><span class="sxs-lookup"><span data-stu-id="c9efb-119">The first element is an .idl/.acf file that precisely describes the data exchange and parameter-passing mechanism between the caller and called procedure.</span></span>
-   <span data-ttu-id="c9efb-120">O segundo elemento é um conjunto de APIs de tempo de execução que fornece aos desenvolvedores um controle granular da chamada de procedimento remoto, incluindo aspectos de segurança, gerenciamento de estado no servidor, especificando quais clientes podem se comunicar com o servidor e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c9efb-120">The second element is a set of run-time APIs that provide developers with granular control of the remote procedure call, including security aspects, managing state on the server, specifying which clients can talk to the server, and so on.</span></span>

 

 




