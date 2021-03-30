---
title: Criando um objeto por meio de um objeto de classe
description: Criando um objeto por meio de um objeto de classe
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916623"
---
# <a name="creating-an-object-through-a-class-object"></a><span data-ttu-id="c24cf-103">Criando um objeto por meio de um objeto de classe</span><span class="sxs-lookup"><span data-stu-id="c24cf-103">Creating an Object Through a Class Object</span></span>

<span data-ttu-id="c24cf-104">Com a importância cada vez maior das redes de computador, ela se tornou necessária para que clientes e servidores interajam com facilidade e eficiência, independentemente de residirem no mesmo computador ou em uma rede.</span><span class="sxs-lookup"><span data-stu-id="c24cf-104">With the increasing importance of computer networks, it has become necessary for clients and servers to interact easily and efficiently, whether they reside on the same machine or across a network.</span></span> <span data-ttu-id="c24cf-105">Crucialmente para isso é a capacidade do cliente de iniciar um servidor, criar uma instância do objeto do servidor e ter acesso aos métodos das interfaces no objeto.</span><span class="sxs-lookup"><span data-stu-id="c24cf-105">Crucial to this is a client's ability to launch a server, create an instance of the server's object, and have access to the methods of the interfaces on the object.</span></span>

<span data-ttu-id="c24cf-106">O COM fornece extensões para esse processo COM básico que o tornam praticamente contínuo em uma rede.</span><span class="sxs-lookup"><span data-stu-id="c24cf-106">COM provides extensions to this basic COM process that make it virtually seamless across a network.</span></span> <span data-ttu-id="c24cf-107">Se um cliente for capaz de identificar o servidor por meio de seu CLSID, chamar algumas funções simples permitirá que o COM faça todo o trabalho de localizar e iniciar o servidor e ativar o objeto.</span><span class="sxs-lookup"><span data-stu-id="c24cf-107">If a client is able to identify the server through its CLSID, calling a few simple functions permit COM to do all the work of locating and launching the server and activating the object.</span></span> <span data-ttu-id="c24cf-108">As subchaves no registro permitem que os servidores remotos registrem seu local e, portanto, o cliente não precisa dessas informações.</span><span class="sxs-lookup"><span data-stu-id="c24cf-108">Subkeys in the registry allow remote servers to register their location, so the client does not require that information.</span></span> <span data-ttu-id="c24cf-109">Para aplicativos que desejam aproveitar os recursos de rede, as funções de criação de objeto COM permitem mais flexibilidade e eficiência.</span><span class="sxs-lookup"><span data-stu-id="c24cf-109">For applications that want to take advantage of networking features, the COM object creation functions allow more flexibility and efficiency.</span></span>

<span data-ttu-id="c24cf-110">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="c24cf-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c24cf-111">Objetos de classe COM e CLSIDs</span><span class="sxs-lookup"><span data-stu-id="c24cf-111">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
-   [<span data-ttu-id="c24cf-112">Localizando um objeto remoto</span><span class="sxs-lookup"><span data-stu-id="c24cf-112">Locating a Remote Object</span></span>](locating-a-remote-object.md)
-   [<span data-ttu-id="c24cf-113">Funções auxiliares de criação de instância</span><span class="sxs-lookup"><span data-stu-id="c24cf-113">Instance Creation Helper Functions</span></span>](instance-creation-helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="c24cf-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c24cf-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c24cf-115">Clientes e servidores COM</span><span class="sxs-lookup"><span data-stu-id="c24cf-115">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




