---
title: O stub do cliente
description: O módulo stub de cliente fornece pontos de entrada substitutos no cliente para cada uma das operações definidas no arquivo IDL de entrada.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL de MIDL e RPC, interfaces, stub de cliente
- MIDL de interfaces
- interfaces MIDL, MIDL e RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292533"
---
# <a name="the-client-stub"></a><span data-ttu-id="18764-106">O stub do cliente</span><span class="sxs-lookup"><span data-stu-id="18764-106">The Client Stub</span></span>

<span data-ttu-id="18764-107">O módulo stub de cliente fornece pontos de entrada substitutos no cliente para cada uma das operações definidas no arquivo IDL de entrada.</span><span class="sxs-lookup"><span data-stu-id="18764-107">The client stub module provides surrogate entry points on the client for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="18764-108">Quando o aplicativo cliente faz uma chamada para o procedimento remoto, sua chamada primeiro vai para a rotina substituta no arquivo stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="18764-108">When the client application makes a call to the remote procedure, its call first goes to the surrogate routine in the client stub file.</span></span> <span data-ttu-id="18764-109">A rotina de stub do cliente executa as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="18764-109">The client stub routine performs the following functions:</span></span>

-   <span data-ttu-id="18764-110">Realiza marshaling de argumentos.</span><span class="sxs-lookup"><span data-stu-id="18764-110">Marshals arguments.</span></span> <span data-ttu-id="18764-111">O stub de cliente empacota os argumentos de entrada em um formulário que pode ser transmitido para o servidor.</span><span class="sxs-lookup"><span data-stu-id="18764-111">The client stub packages input arguments into a form that can be transmitted to the server.</span></span>
-   <span data-ttu-id="18764-112">Chama a biblioteca de tempo de execução do cliente para transmitir argumentos para o espaço de endereço remoto e invoca o procedimento remoto no espaço de endereço do servidor.</span><span class="sxs-lookup"><span data-stu-id="18764-112">Calls the client run-time library to transmit arguments to the remote address space and invokes the remote procedure in the server address space.</span></span>
-   <span data-ttu-id="18764-113">Desempacota os argumentos de saída.</span><span class="sxs-lookup"><span data-stu-id="18764-113">Unmarshals output arguments.</span></span> <span data-ttu-id="18764-114">O stub de cliente desempacota os argumentos de saída e retorna ao chamador.</span><span class="sxs-lookup"><span data-stu-id="18764-114">The client stub unpacks output arguments and returns to the caller.</span></span>

<span data-ttu-id="18764-115">O compilador MIDL alterna [**/Client**](-client.md), [**/cstub**](-cstub.md)e [**/out**](-out.md) afeta o arquivo stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="18764-115">The MIDL compiler switches [**/client**](-client.md), [**/cstub**](-cstub.md), and [**/out**](-out.md) affect the client stub file.</span></span>

 

 




