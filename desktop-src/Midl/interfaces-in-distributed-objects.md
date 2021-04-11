---
title: Interfaces em objetos distribuídos
description: Na computação distribuída, uma interface é uma coleção de definições e funções remotas que permite que dois ou mais programas interoperem entre diferentes contextos.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- MIDL de interfaces, em objetos distribuídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294012"
---
# <a name="interfaces-in-distributed-objects"></a><span data-ttu-id="94ae9-104">Interfaces em objetos distribuídos</span><span class="sxs-lookup"><span data-stu-id="94ae9-104">Interfaces in Distributed Objects</span></span>

<span data-ttu-id="94ae9-105">Na computação distribuída, uma interface é uma coleção de definições e funções remotas que permite que dois ou mais programas interoperem entre diferentes contextos.</span><span class="sxs-lookup"><span data-stu-id="94ae9-105">In distributed computing, an interface is a collection of definitions and remote functions that enables two or more programs to interoperate between different contexts.</span></span> <span data-ttu-id="94ae9-106">Em um aplicativo RPC, uma interface especifica:</span><span class="sxs-lookup"><span data-stu-id="94ae9-106">In an RPC application, an interface specifies:</span></span>

-   <span data-ttu-id="94ae9-107">Como os aplicativos cliente e servidor se identificam entre si.</span><span class="sxs-lookup"><span data-stu-id="94ae9-107">How client and server applications identify themselves to each other.</span></span>
-   <span data-ttu-id="94ae9-108">Como os dados são transmitidos entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="94ae9-108">How data is transmitted between client and server.</span></span>
-   <span data-ttu-id="94ae9-109">Procedimentos remotos que o aplicativo cliente pode chamar.</span><span class="sxs-lookup"><span data-stu-id="94ae9-109">Remote procedures that the client application can call.</span></span>
-   <span data-ttu-id="94ae9-110">Tipos de dados para os parâmetros e valores de retorno dos procedimentos remotos.</span><span class="sxs-lookup"><span data-stu-id="94ae9-110">Data types for the parameters and return values of the remote procedures.</span></span>

<span data-ttu-id="94ae9-111">O linguagem IDL da Microsoft (MIDL) é para implementar interfaces usadas em aplicativos distribuídos.</span><span class="sxs-lookup"><span data-stu-id="94ae9-111">The Microsoft Interface Definition Language (MIDL) is for implementing interfaces used in distributed applications.</span></span> <span data-ttu-id="94ae9-112">Com MIDL, um aplicativo pode ter uma interface ou muitos.</span><span class="sxs-lookup"><span data-stu-id="94ae9-112">With MIDL, an application can have one interface or many.</span></span> <span data-ttu-id="94ae9-113">Cada interface especifica um contrato distribuído exclusivo entre os programas cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="94ae9-113">Each interface specifies a unique distributed contract between the client and server programs.</span></span> <span data-ttu-id="94ae9-114">Aplicativos baseados em RPC (chamadas de procedimento remoto), Component Object Model (COM) e distribuída Component Object Model (DCOM) especificam suas interfaces usando MIDL.</span><span class="sxs-lookup"><span data-stu-id="94ae9-114">Applications based on remote procedure calls (RPC), Component Object Model (COM), and Distributed Component Object Model (DCOM) specify their interfaces using MIDL.</span></span>

<span data-ttu-id="94ae9-115">O MIDL se assemelha a C e C++ de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="94ae9-115">MIDL resembles C and C++ in many ways.</span></span> <span data-ttu-id="94ae9-116">Para obter uma visão geral da escrita de interfaces MIDL, consulte [desenvolvendo a interface](/windows/desktop/Rpc/developing-the-interface).</span><span class="sxs-lookup"><span data-stu-id="94ae9-116">For an overview of writing MIDL interfaces, see [Developing the Interface](/windows/desktop/Rpc/developing-the-interface).</span></span>

 

 