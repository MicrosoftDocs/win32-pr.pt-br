---
title: O stub do servidor
description: O stub de servidor fornece pontos de entrada substitutos no servidor para cada uma das operações definidas no arquivo IDL de entrada.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL do compilador MIDL, MIDL e prc RPC, interfaces, stub de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005952"
---
# <a name="the-server-stub"></a><span data-ttu-id="232cd-104">O stub do servidor</span><span class="sxs-lookup"><span data-stu-id="232cd-104">The Server Stub</span></span>

<span data-ttu-id="232cd-105">O stub de servidor fornece pontos de entrada substitutos no servidor para cada uma das operações definidas no arquivo IDL de entrada.</span><span class="sxs-lookup"><span data-stu-id="232cd-105">The server stub provides surrogate entry points on the server for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="232cd-106">Quando uma rotina de stub de servidor é invocada pela biblioteca de tempo de execução RPC, ela executa as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="232cd-106">When a server stub routine is invoked by the RPC run-time library, it performs the following functions:</span></span>

-   <span data-ttu-id="232cd-107">Desempacota os argumentos de entrada (descompacta os argumentos de seus formatos transmitidos).</span><span class="sxs-lookup"><span data-stu-id="232cd-107">Unmarshals input arguments (unpacks the arguments from their transmitted formats).</span></span>
-   <span data-ttu-id="232cd-108">Chama a implementação real do procedimento no servidor.</span><span class="sxs-lookup"><span data-stu-id="232cd-108">Calls the actual implementation of the procedure on the server.</span></span>
-   <span data-ttu-id="232cd-109">Realiza marshaling de argumentos de saída (empacota os argumentos nos formulários transmitidos).</span><span class="sxs-lookup"><span data-stu-id="232cd-109">Marshals output arguments (packages the arguments into the transmitted forms).</span></span>

<span data-ttu-id="232cd-110">O compilador MIDL alterna a opção [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) afeta o arquivo stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="232cd-110">The MIDL compiler switches [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

 

 




