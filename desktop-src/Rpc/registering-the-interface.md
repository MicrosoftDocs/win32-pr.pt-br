---
title: Registrando a interface
description: Registrar a interface que um programa de servidor dá suporte permite que chamadas de procedimento remotos de programas cliente sejam expedidas para a rotina de servidor adequada.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Chamada de procedimento remoto RPC, tarefas, registrando a interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159288"
---
# <a name="registering-the-interface"></a><span data-ttu-id="c40d4-104">Registrando a interface</span><span class="sxs-lookup"><span data-stu-id="c40d4-104">Registering the Interface</span></span>

<span data-ttu-id="c40d4-105">Registrar a interface que um programa de servidor dá suporte permite que chamadas de procedimento remotos de programas cliente sejam expedidas para a rotina de servidor adequada.</span><span class="sxs-lookup"><span data-stu-id="c40d4-105">Registering the interface that a server program supports enables remote procedure calls from client programs to be dispatched to the proper server routine.</span></span> <span data-ttu-id="c40d4-106">Os programas de servidor chamam [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para registrar suas interfaces.</span><span class="sxs-lookup"><span data-stu-id="c40d4-106">Server programs call [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to register their interfaces.</span></span> <span data-ttu-id="c40d4-107">O fragmento de código a seguir demonstra seu uso:</span><span class="sxs-lookup"><span data-stu-id="c40d4-107">The following code fragment demonstrates its use:</span></span>


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



<span data-ttu-id="c40d4-108">O primeiro parâmetro para a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) é uma estrutura que o compilador MIDL gera a partir do arquivo IDL que define a interface (ou interfaces) para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c40d4-108">The first parameter to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is a structure the MIDL compiler generates from the IDL file that defines the interface (or interfaces) for the server.</span></span> <span data-ttu-id="c40d4-109">O segundo e o terceiro parâmetros são um UUID e um vetor de ponto de entrada, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c40d4-109">The second and third parameters are a UUID and an entry-point vector, respectively.</span></span> <span data-ttu-id="c40d4-110">Eles são definidos como **NULL** neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="c40d4-110">They are set to **NULL** in this example.</span></span> <span data-ttu-id="c40d4-111">Em muitos casos, o programa do servidor definirá esses valores de parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c40d4-111">In many instances, your server program will set these parameter values to **NULL**.</span></span> <span data-ttu-id="c40d4-112">Os programas de servidor usam o segundo e o terceiro parâmetros quando fornecem várias implementações dos mesmos procedimentos em uma interface.</span><span class="sxs-lookup"><span data-stu-id="c40d4-112">Server programs use the second and third parameters when they provide multiple implementations of the same procedures in an interface.</span></span> <span data-ttu-id="c40d4-113">Para obter mais informações, consulte [vetores de ponto de entrada](registering-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c40d4-113">For more information, see [Entry-Point Vectors](registering-interfaces.md).</span></span>

<span data-ttu-id="c40d4-114">Os programas de servidor também podem usar o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) para registrar uma interface.</span><span class="sxs-lookup"><span data-stu-id="c40d4-114">Server programs can also use [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) to register an interface.</span></span> <span data-ttu-id="c40d4-115">Uma vantagem de usar essa função é que ela fornece ao aplicativo a capacidade de definir uma função de retorno de chamada de segurança.</span><span class="sxs-lookup"><span data-stu-id="c40d4-115">One advantage of using this function is that it provides your application with the ability to set a security-callback function.</span></span> <span data-ttu-id="c40d4-116">O uso de funções de retorno de chamada de segurança é a abordagem recomendada para proteger uma interface.</span><span class="sxs-lookup"><span data-stu-id="c40d4-116">Using security-callback functions is the recommended approach to securing an interface.</span></span>

> [!Note]  
> <span data-ttu-id="c40d4-117">O MIDL produz duas estruturas muito semelhantes, uma para o cliente e outra para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c40d4-117">MIDL produces two very similar structures, one for the client and one for the server.</span></span> <span data-ttu-id="c40d4-118">A estrutura passada para a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) é a versão do servidor da estrutura gerada pelo MIDL.</span><span class="sxs-lookup"><span data-stu-id="c40d4-118">The structure passed to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is the server version of the MIDL-produced structure.</span></span>

 

 

 




