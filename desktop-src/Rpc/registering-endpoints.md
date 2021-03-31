---
title: Registrando pontos de extremidade
description: O registro do programa do servidor no mapa do ponto de extremidade do computador host do servidor permite que os programas cliente determinem qual ponto de extremidade (geralmente uma porta TCP/IP ou um pipe nomeado) o programa do servidor está escutando.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Chamada de procedimento remoto RPC, tarefas, registrando pontos de extremidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634844"
---
# <a name="registering-endpoints"></a><span data-ttu-id="dd41c-104">Registrando pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="dd41c-104">Registering Endpoints</span></span>

<span data-ttu-id="dd41c-105">O registro do programa do servidor no mapa do ponto de extremidade do computador host do servidor permite que os programas cliente determinem qual ponto de extremidade (geralmente uma porta TCP/IP ou um pipe nomeado) o programa do servidor está escutando.</span><span class="sxs-lookup"><span data-stu-id="dd41c-105">Registering the server program in the endpoint map of the server host computer enables client programs to determine which endpoint (usually a TCP/IP port or a named pipe) the server program is listening to.</span></span> <span data-ttu-id="dd41c-106">Para se registrar no mapa de ponto de extremidade do sistema host do servidor, um programa de servidor chama a função [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) , conforme mostrado no fragmento de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="dd41c-106">To register itself in the server host system's endpoint map, a server program calls the [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) function as shown in the following code fragment:</span></span>


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



<span data-ttu-id="dd41c-107">O primeiro parâmetro para [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) é a estrutura que representa a interface.</span><span class="sxs-lookup"><span data-stu-id="dd41c-107">The first parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is the structure that represents the interface.</span></span> <span data-ttu-id="dd41c-108">Você pode encontrá-lo no arquivo de cabeçalho que o compilador MIDL gerou do arquivo MIDL para esse aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="dd41c-108">You can find it in the header file that the MIDL compiler generated from your MIDL file for this distributed application.</span></span> <span data-ttu-id="dd41c-109">Consulte [desenvolvendo a interface](developing-the-interface.md).</span><span class="sxs-lookup"><span data-stu-id="dd41c-109">See [Developing the Interface](developing-the-interface.md).</span></span> <span data-ttu-id="dd41c-110">Em seguida, **RpcEpRegister** precisa que seu aplicativo passe um conjunto de identificadores de ligação que são armazenados em um vetor de associação.</span><span class="sxs-lookup"><span data-stu-id="dd41c-110">Next, **RpcEpRegister** needs your application to pass a set of binding handles that are stored in a binding vector.</span></span>

<span data-ttu-id="dd41c-111">Além de registrar nomes de interface, o aplicativo de servidor também pode registrar UUIDs de objeto no mapa do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dd41c-111">In addition to registering interface names, your server application can also register object UUIDs in the endpoint map.</span></span> <span data-ttu-id="dd41c-112">Neste exemplo, não há UUIDs de objeto para registrar, portanto, o terceiro parâmetro para [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) é definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dd41c-112">In this example, there are no object UUIDs to register, so the third parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is set to **NULL**.</span></span>

<span data-ttu-id="dd41c-113">O último parâmetro é uma cadeia de caracteres de comentário.</span><span class="sxs-lookup"><span data-stu-id="dd41c-113">The last parameter is a comment string.</span></span> <span data-ttu-id="dd41c-114">Embora a biblioteca de tempo de execução RPC não use essa cadeia de caracteres, é recomendável definir a cadeia de caracteres, pois ela melhora a capacidade de gerenciamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="dd41c-114">Although the RPC run-time library does not use this string, setting the string is recommended, as it improves manageability of the system.</span></span> <span data-ttu-id="dd41c-115">Um administrador do sistema pode usar a cadeia de caracteres para detectar quais portas são usadas por quais aplicativos, que podem ser usados para determinar quais portas serão gerenciadas por firewalls.</span><span class="sxs-lookup"><span data-stu-id="dd41c-115">A system administrator can use the string to detect which ports are used by which applications, which can then be used to determine which ports to be managed by firewalls.</span></span>

 

 




