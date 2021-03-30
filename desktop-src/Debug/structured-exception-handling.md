---
description: Uma exceção é um evento que ocorre durante a execução de um programa e requer a execução de código fora do fluxo de controle normal.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Tratamento de exceções estruturado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826167"
---
# <a name="structured-exception-handling"></a><span data-ttu-id="cffed-103">Tratamento de exceções estruturado</span><span class="sxs-lookup"><span data-stu-id="cffed-103">Structured Exception Handling</span></span>

<span data-ttu-id="cffed-104">Uma *exceção* é um evento que ocorre durante a execução de um programa e requer a execução de código fora do fluxo de controle normal.</span><span class="sxs-lookup"><span data-stu-id="cffed-104">An *exception* is an event that occurs during the execution of a program, and requires the execution of code outside the normal flow of control.</span></span> <span data-ttu-id="cffed-105">Há dois tipos de exceções: exceções de hardware e exceções de software.</span><span class="sxs-lookup"><span data-stu-id="cffed-105">There are two kinds of exceptions: hardware exceptions and software exceptions.</span></span> <span data-ttu-id="cffed-106">As *exceções de hardware* são iniciadas pela CPU.</span><span class="sxs-lookup"><span data-stu-id="cffed-106">*Hardware exceptions* are initiated by the CPU.</span></span> <span data-ttu-id="cffed-107">Eles podem resultar da execução de determinadas sequências de instrução, como divisão por zero ou uma tentativa de acessar um endereço de memória inválido.</span><span class="sxs-lookup"><span data-stu-id="cffed-107">They can result from the execution of certain instruction sequences, such as division by zero or an attempt to access an invalid memory address.</span></span> <span data-ttu-id="cffed-108">As *exceções de software* são iniciadas explicitamente por aplicativos ou pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cffed-108">*Software exceptions* are initiated explicitly by applications or the operating system.</span></span> <span data-ttu-id="cffed-109">Por exemplo, o sistema pode detectar quando um valor de parâmetro inválido é especificado.</span><span class="sxs-lookup"><span data-stu-id="cffed-109">For example, the system can detect when an invalid parameter value is specified.</span></span>

<span data-ttu-id="cffed-110">A *manipulação de exceção estruturada* é um mecanismo para lidar com exceções de hardware e software.</span><span class="sxs-lookup"><span data-stu-id="cffed-110">*Structured exception handling* is a mechanism for handling both hardware and software exceptions.</span></span> <span data-ttu-id="cffed-111">Portanto, seu código tratará as exceções de hardware e software de forma idêntica.</span><span class="sxs-lookup"><span data-stu-id="cffed-111">Therefore, your code will handle hardware and software exceptions identically.</span></span> <span data-ttu-id="cffed-112">A manipulação de exceção estruturada permite que você tenha controle total sobre a manipulação de exceções, fornece suporte para depuradores e é utilizável em todas as linguagens de programação e computadores.</span><span class="sxs-lookup"><span data-stu-id="cffed-112">Structured exception handling enables you to have complete control over the handling of exceptions, provides support for debuggers, and is usable across all programming languages and machines.</span></span> <span data-ttu-id="cffed-113">A *manipulação de exceção em vetor* é uma extensão da manipulação de exceção estruturada.</span><span class="sxs-lookup"><span data-stu-id="cffed-113">*Vectored exception handling* is an extension to structured exception handling.</span></span>

<span data-ttu-id="cffed-114">O sistema também dá suporte ao *tratamento de terminação*, o que permite que você garanta que sempre que um corpo de código protegido for executado, um bloco de código de encerramento especificado também será executado.</span><span class="sxs-lookup"><span data-stu-id="cffed-114">The system also supports *termination handling*, which enables you to ensure that whenever a guarded body of code is executed, a specified block of termination code is also executed.</span></span> <span data-ttu-id="cffed-115">O código de encerramento é executado independentemente de como o fluxo de controle deixa o corpo protegido.</span><span class="sxs-lookup"><span data-stu-id="cffed-115">The termination code is executed regardless of how the flow of control leaves the guarded body.</span></span> <span data-ttu-id="cffed-116">Por exemplo, um manipulador de encerramento pode garantir que as tarefas de limpeza sejam executadas mesmo se uma exceção ou algum outro erro ocorrer enquanto o corpo de código protegido estiver sendo executado.</span><span class="sxs-lookup"><span data-stu-id="cffed-116">For example, a termination handler can guarantee that clean-up tasks are performed even if an exception or some other error occurs while the guarded body of code is being executed.</span></span>

-   [<span data-ttu-id="cffed-117">Sobre manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="cffed-117">About Structured Exception Handling</span></span>](about-structured-exception-handling.md)
-   [<span data-ttu-id="cffed-118">Usando manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="cffed-118">Using Structured Exception Handling</span></span>](using-structured-exception-handling.md)
-   [<span data-ttu-id="cffed-119">Referência de manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="cffed-119">Structured Exception Handling Reference</span></span>](structured-exception-handling-reference.md)

 

 



