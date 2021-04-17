---
title: Identificadores de associação explícitos
description: Para obter o controle máximo sobre o processo de associação, os aplicativos cliente/servidor podem usar identificadores de ligação explícitos.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754298"
---
# <a name="explicit-binding-handles"></a><span data-ttu-id="a4ba8-103">Identificadores de associação explícitos</span><span class="sxs-lookup"><span data-stu-id="a4ba8-103">Explicit Binding Handles</span></span>

<span data-ttu-id="a4ba8-104">Para obter o controle máximo sobre o processo de associação, os aplicativos cliente/servidor podem usar identificadores de ligação explícitos.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-104">For maximum control over the binding process, client/server applications may use explicit binding handles.</span></span> <span data-ttu-id="a4ba8-105">Como os identificadores implícitos, os identificadores de ligação explícitos permitem que o aplicativo cliente selecione um servidor para executar suas chamadas.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-105">Like implicit handles, explicit binding handles enable your client application to select a server to execute its calls.</span></span> <span data-ttu-id="a4ba8-106">Além disso, os identificadores de ligação explícitos permitem que o aplicativo cliente/servidor crie uma sessão de comunicação RPC autenticada.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-106">In addition, explicit binding handles enable your client/server application to create an authenticated RPC communication session.</span></span> <span data-ttu-id="a4ba8-107">Com identificadores explícitos, o cliente pode se conectar a mais de um servidor e executar procedimentos remotos em vários servidores.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-107">With explicit handles, your client can connect to more than one server and execute remote procedures on multiple servers.</span></span> <span data-ttu-id="a4ba8-108">Aplicativos cliente multithread e assíncronos podem até mesmo se conectar a vários servidores e executar vários procedimentos remotos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-108">Multithreaded and asynchronous client applications can even connect to multiple servers and execute multiple remote procedures at the same time.</span></span>

<span data-ttu-id="a4ba8-109">Seu aplicativo cliente deve passar o identificador explícito como um parâmetro para cada chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-109">Your client application must pass the explicit handle as a parameter to each remote procedure call.</span></span> <span data-ttu-id="a4ba8-110">Para estar de acordo com o padrão uso, o identificador deve ser especificado como o primeiro parâmetro em cada procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-110">To conform to the OSF standard, the handle should be specified as the first parameter on each remote procedure.</span></span> <span data-ttu-id="a4ba8-111">No entanto, as extensões da Microsoft para RPC permitem que você especifique o identificador de associação em outras posições.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-111">However, the Microsoft extensions to RPC enable you to specify the binding handle in other positions.</span></span> <span data-ttu-id="a4ba8-112">Para obter mais informações, consulte [extensões de Binding-Handle RPC da Microsoft](microsoft-rpc-binding-handle-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a4ba8-112">For more information, see [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span></span>

<span data-ttu-id="a4ba8-113">Para criar um identificador explícito, declare o identificador como um parâmetro para as operações remotas no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-113">To create an explicit handle, declare the handle as a parameter to the remote operations in the IDL file.</span></span> <span data-ttu-id="a4ba8-114">O [exemplo Hello, World](tutorial.md) pode ser redefinido para usar um identificador explícito, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="a4ba8-114">The [Hello, World example](tutorial.md) can be redefined to use an explicit handle as shown:</span></span>

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

<span data-ttu-id="a4ba8-115">Você pode combinar identificadores explícitos e implícitos em uma única interface.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-115">You can combine explicit and implicit handles in a single interface.</span></span> <span data-ttu-id="a4ba8-116">Se uma função tiver um identificador explícito em sua lista de parâmetros, esse identificador será usado.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-116">If a function has an explicit handle in its parameter list, that handle will be used.</span></span> <span data-ttu-id="a4ba8-117">Se uma função em uma interface que usa identificadores implícitos não especificar um identificador explícito, o identificador implícito padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="a4ba8-117">If a function in an interface using implicit handles does not specify an explicit handle, then the default implicit handle will be used.</span></span>

 

 




