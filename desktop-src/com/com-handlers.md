---
title: Manipuladores COM
description: A finalidade dos manipuladores COM é fornecer algumas \ 0034; inteligente \ 0034; código no espaço de endereço do cliente que pode otimizar chamadas entre um cliente e um servidor. Os manipuladores podem substituir algumas interfaces ao delegar outras pessoas diretamente ao servidor (por meio do proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105766514"
---
# <a name="com-handlers"></a><span data-ttu-id="c22e3-104">Manipuladores COM</span><span class="sxs-lookup"><span data-stu-id="c22e3-104">COM Handlers</span></span>

<span data-ttu-id="c22e3-105">A finalidade dos manipuladores COM é fornecer um código "inteligente" no espaço de endereço do cliente que possa otimizar as chamadas entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="c22e3-105">The purpose of COM handlers is to provide some "smart" code in the client address space that can optimize calls between a client and server.</span></span> <span data-ttu-id="c22e3-106">Os manipuladores podem substituir algumas interfaces ao delegar outras pessoas diretamente ao servidor (por meio do proxy).</span><span class="sxs-lookup"><span data-stu-id="c22e3-106">Handlers can override some interfaces while delegating others directly to the server (through the proxy).</span></span>

<span data-ttu-id="c22e3-107">Há dois tipos de manipuladores COM:</span><span class="sxs-lookup"><span data-stu-id="c22e3-107">There are two types of COM handlers:</span></span>

-   <span data-ttu-id="c22e3-108">[O manipulador OLE](the-ole-handler.md) é uma DLL de alta gramatura que fornece serviços importantes para vinculação e inserção.</span><span class="sxs-lookup"><span data-stu-id="c22e3-108">[The OLE handler](the-ole-handler.md) is a heavyweight DLL that provides important services for linking and embedding.</span></span> <span data-ttu-id="c22e3-109">Normalmente, ele é criado antes de o servidor ser iniciado e é inicializado para que o servidor seja ativado quando o objeto inserido entrar no estado de execução.</span><span class="sxs-lookup"><span data-stu-id="c22e3-109">It is usually created before the server is launched and is initialized so that the server is activated when the embedded object enters the running state.</span></span>
-   <span data-ttu-id="c22e3-110">[O manipulador leve do lado do cliente](the-lightweight-client-side-handler.md) pode ser criado para qualquer finalidade, pode ser muito pequeno e não pode ser criado antes do servidor.</span><span class="sxs-lookup"><span data-stu-id="c22e3-110">[The lightweight client-side handler](the-lightweight-client-side-handler.md) can be created for any purpose, can be very small, and cannot be created before the server.</span></span>

 

 




