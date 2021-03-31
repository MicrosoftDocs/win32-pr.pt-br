---
title: O modelo de RPC
description: A RPC (chamada de procedimento remoto) para as linguagens de programação C e C++ foi projetada para ajudar a atender às necessidades dos desenvolvedores que trabalham na próxima geração de software para sistemas operacionais Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Chamada de procedimento remoto RPC, descrito, o modelo de RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641628"
---
# <a name="the-rpc-model"></a><span data-ttu-id="876ed-104">O modelo de RPC</span><span class="sxs-lookup"><span data-stu-id="876ed-104">The RPC Model</span></span>

<span data-ttu-id="876ed-105">A RPC (chamada de procedimento remoto) para as linguagens de programação C e C++ foi projetada para ajudar a atender às necessidades dos desenvolvedores que trabalham na próxima geração de software para sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="876ed-105">Remote Procedure Call (RPC) for the C and C++ programming languages is designed to help meet the needs of developers working on the next generation of software for Windows operating systems.</span></span>

<span data-ttu-id="876ed-106">O RPC é um mecanismo de IPC (comunicação entre processos) eficiente, robusto, eficiente e seguro que permite a troca de dados e a invocação de funcionalidades que residem em um processo diferente.</span><span class="sxs-lookup"><span data-stu-id="876ed-106">RPC is a powerful, robust, efficient, and secure interprocess communication (IPC) mechanism that enables data exchange and invocation of functionality residing in a different process.</span></span> <span data-ttu-id="876ed-107">Esse processo diferente pode estar no mesmo computador, na rede local ou na Internet.</span><span class="sxs-lookup"><span data-stu-id="876ed-107">That different process can be on the same machine, on the local area network, or across the Internet.</span></span> <span data-ttu-id="876ed-108">Esta seção explica o modelo de programação RPC e o modelo para sistemas distribuídos que podem ser implementados usando RPC.</span><span class="sxs-lookup"><span data-stu-id="876ed-108">This section explains the RPC programming model and the model for distributed systems that can be implemented using RPC.</span></span>

<span data-ttu-id="876ed-109">O RPC dá suporte total ao Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="876ed-109">RPC fully supports 64-bit Windows.</span></span> <span data-ttu-id="876ed-110">Há três tipos de processos: processos nativos de 32 bits, processos nativos de 64 bits e processos de 32 bits em execução no emulador de processo de 32 bits em um sistema de 64 bits (geralmente conhecido como processos WOW64).</span><span class="sxs-lookup"><span data-stu-id="876ed-110">There are three types of processes: native 32-bit processes, native 64-bit processes, and 32-bit processes running under the 32-bit process emulator on a 64-bit system (often referred to as WOW64 processes).</span></span> <span data-ttu-id="876ed-111">Para obter mais informações sobre o WOW64, consulte [executando aplicativos de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications).</span><span class="sxs-lookup"><span data-stu-id="876ed-111">For more information about WOW64, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span> <span data-ttu-id="876ed-112">Usando o RPC, os desenvolvedores podem se comunicar de forma transparente entre diferentes tipos de processo; O RPC gerencia automaticamente as diferenças de processo nos bastidores.</span><span class="sxs-lookup"><span data-stu-id="876ed-112">Using RPC, developers can transparently communicate between different types of process; RPC automatically manages process differences behind the scenes.</span></span>

<span data-ttu-id="876ed-113">O RPC foi inicialmente desenvolvido como uma extensão para uso RPC.</span><span class="sxs-lookup"><span data-stu-id="876ed-113">RPC was initially developed as an extension to OSF RPC.</span></span> <span data-ttu-id="876ed-114">Com exceção de alguns de seus recursos avançados, o RPC é interoperável com implementações de outros fornecedores de RPC uso.</span><span class="sxs-lookup"><span data-stu-id="876ed-114">With the exception of some of its advanced features, RPC is interoperable with other vendors' implementations of OSF RPC.</span></span>

<span data-ttu-id="876ed-115">Esta seção também fornece uma visão geral dos componentes RPC e sua operação.</span><span class="sxs-lookup"><span data-stu-id="876ed-115">This section also provides an overview of RPC components and their operation.</span></span> <span data-ttu-id="876ed-116">As informações são apresentadas nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="876ed-116">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="876ed-117">O modelo de programação</span><span class="sxs-lookup"><span data-stu-id="876ed-117">The Programming Model</span></span>](the-programming-model.md)
-   [<span data-ttu-id="876ed-118">O modelo para sistemas distribuídos</span><span class="sxs-lookup"><span data-stu-id="876ed-118">The Model for Distributed Systems</span></span>](the-model-for-distributed-systems.md)
-   [<span data-ttu-id="876ed-119">Como funciona o RPC</span><span class="sxs-lookup"><span data-stu-id="876ed-119">How RPC Works</span></span>](how-rpc-works.md)
-   [<span data-ttu-id="876ed-120">Componentes RPC da Microsoft</span><span class="sxs-lookup"><span data-stu-id="876ed-120">Microsoft RPC Components</span></span>](microsoft-rpc-components.md)

 

 