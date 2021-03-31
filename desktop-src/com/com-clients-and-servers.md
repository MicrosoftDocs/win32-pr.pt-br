---
title: Clientes e servidores COM
description: Um aspecto crítico do COM é como os clientes e servidores interagem.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636058"
---
# <a name="com-clients-and-servers"></a><span data-ttu-id="b2aea-103">Clientes e servidores COM</span><span class="sxs-lookup"><span data-stu-id="b2aea-103">COM Clients and Servers</span></span>

<span data-ttu-id="b2aea-104">Um aspecto crítico do COM é como os clientes e servidores interagem.</span><span class="sxs-lookup"><span data-stu-id="b2aea-104">A critical aspect of COM is how clients and servers interact.</span></span> <span data-ttu-id="b2aea-105">Um *cliente com* é qualquer código ou objeto que obtém um ponteiro para um servidor com e usa seus serviços chamando os métodos de suas interfaces.</span><span class="sxs-lookup"><span data-stu-id="b2aea-105">A *COM client* is whatever code or object gets a pointer to a COM server and uses its services by calling the methods of its interfaces.</span></span> <span data-ttu-id="b2aea-106">Um *servidor com* é qualquer objeto que forneça serviços aos clientes; esses serviços estão na forma de implementações de interface COM que podem ser chamadas por qualquer cliente capaz de obter um ponteiro para uma das interfaces no objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="b2aea-106">A *COM server* is any object that provides services to clients; these services are in the form of COM interface implementations that can be called by any client that is able to get a pointer to one of the interfaces on the server object.</span></span>

<span data-ttu-id="b2aea-107">Há dois tipos principais de servidores, *em processo* e *fora de processo*.</span><span class="sxs-lookup"><span data-stu-id="b2aea-107">There are two main types of servers, *in-process* and *out-of-process*.</span></span> <span data-ttu-id="b2aea-108">Os servidores em processo são implementados em uma DLL (biblioteca vinculada dinâmica) e os servidores fora do processo são implementados em um arquivo executável (EXE).</span><span class="sxs-lookup"><span data-stu-id="b2aea-108">In-process servers are implemented in a dynamic linked library (DLL), and out-of-process servers are implemented in an executable file (EXE).</span></span> <span data-ttu-id="b2aea-109">Os servidores fora do processo podem residir no computador local ou em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="b2aea-109">Out-of-process servers can reside either on the local computer or on a remote computer.</span></span> <span data-ttu-id="b2aea-110">Além disso, o COM fornece um mecanismo que permite que um servidor em processo (uma DLL) seja executado em um processo EXE substituto para obter a vantagem de poder executar o processo em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="b2aea-110">In addition, COM provides a mechanism that allows an in-process server (a DLL) to run in a surrogate EXE process to gain the advantage of being able to run the process on a remote computer.</span></span> <span data-ttu-id="b2aea-111">Para obter mais informações, consulte [substitutos de dll](dll-surrogates.md).</span><span class="sxs-lookup"><span data-stu-id="b2aea-111">For more information, see [DLL Surrogates](dll-surrogates.md).</span></span>

<span data-ttu-id="b2aea-112">Agora, o modelo de programação COM e as construções foram estendidos para que os clientes e servidores COM possam trabalhar juntos na rede, não apenas dentro de um determinado computador.</span><span class="sxs-lookup"><span data-stu-id="b2aea-112">The COM programming model and constructs have now been extended so that COM clients and servers can work together across the network, not just within a given computer.</span></span> <span data-ttu-id="b2aea-113">Isso permite que os aplicativos existentes interajam com novos aplicativos e entre si em redes com administração adequada e novos aplicativos possam ser escritos para tirar proveito dos recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="b2aea-113">This enables existing applications to interact with new applications and with each other across networks with proper administration, and new applications can be written to take advantage of networking features.</span></span>

<span data-ttu-id="b2aea-114">Os aplicativos cliente COM não precisam saber como os objetos de servidor são empacotados, se eles são empacotados como objetos em processo (em DLLs) ou como objetos locais ou remotos (em EXEs).</span><span class="sxs-lookup"><span data-stu-id="b2aea-114">COM client applications do not need to be aware of how server objects are packaged, whether they are packaged as in-process objects (in DLLs) or as local or remote objects (in EXEs).</span></span> <span data-ttu-id="b2aea-115">O COM distribuído ainda permite que os objetos sejam empacotados como aplicativos de serviço, sincronizando COM com os avançados recursos administrativos e de integração do sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="b2aea-115">Distributed COM further allows objects to be packaged as service applications, synchronizing COM with the rich administrative and system-integration capabilities of Windows.</span></span>

> [!Note]  
> <span data-ttu-id="b2aea-116">Ao longo desta documentação, o acrônimo COM é usado em preferência ao DCOM.</span><span class="sxs-lookup"><span data-stu-id="b2aea-116">Throughout this documentation the acronym COM is used in preference to DCOM.</span></span> <span data-ttu-id="b2aea-117">Isso ocorre porque o DCOM não é separado; é apenas com uma transmissão mais longa.</span><span class="sxs-lookup"><span data-stu-id="b2aea-117">This is because DCOM is not separate;it is just COM with a longer wire.</span></span> <span data-ttu-id="b2aea-118">Nos casos em que o que está sendo descrito é especificamente uma operação remota, o termo *com distribuído* é usado.</span><span class="sxs-lookup"><span data-stu-id="b2aea-118">In cases where what is being described is specifically a remote operation, the term *distributed COM* is used.</span></span>

 

<span data-ttu-id="b2aea-119">O COM foi projetado para possibilitar a adição do suporte à transparência de local que se estende por uma rede.</span><span class="sxs-lookup"><span data-stu-id="b2aea-119">COM is designed to make it possible to add the support for location transparency that extends across a network.</span></span> <span data-ttu-id="b2aea-120">Ele permite que os aplicativos escritos para computadores únicos sejam executados em uma rede e fornece recursos que estendem esses recursos e que aumentam a segurança necessária em uma rede.</span><span class="sxs-lookup"><span data-stu-id="b2aea-120">It allows applications written for single computers to run across a network and provides features that extend these capabilities and add to the security necessary in a network.</span></span> <span data-ttu-id="b2aea-121">(Para obter mais informações, consulte [segurança em com](security-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="b2aea-121">(For more information, see [Security in COM](security-in-com.md).)</span></span>

<span data-ttu-id="b2aea-122">COM especifica um mecanismo pelo qual o código de classe pode ser usado por vários aplicativos diferentes.</span><span class="sxs-lookup"><span data-stu-id="b2aea-122">COM specifies a mechanism by which the class code can be used by many different applications.</span></span>

<span data-ttu-id="b2aea-123">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="b2aea-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b2aea-124">Obtendo um ponteiro para um objeto</span><span class="sxs-lookup"><span data-stu-id="b2aea-124">Getting a Pointer to an Object</span></span>](getting-a-pointer-to-an-object.md)
-   [<span data-ttu-id="b2aea-125">Criando um objeto por meio de um objeto de classe</span><span class="sxs-lookup"><span data-stu-id="b2aea-125">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
-   [<span data-ttu-id="b2aea-126">Responsabilidades do servidor COM</span><span class="sxs-lookup"><span data-stu-id="b2aea-126">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
-   [<span data-ttu-id="b2aea-127">Estado de objeto persistente</span><span class="sxs-lookup"><span data-stu-id="b2aea-127">Persistent Object State</span></span>](persistent-object-state.md)
-   [<span data-ttu-id="b2aea-128">Fornecendo informações de classe</span><span class="sxs-lookup"><span data-stu-id="b2aea-128">Providing Class Information</span></span>](providing-class-information.md)
-   [<span data-ttu-id="b2aea-129">Comunicação entre objetos</span><span class="sxs-lookup"><span data-stu-id="b2aea-129">Inter-Object Communication</span></span>](inter-object-communication.md)

## <a name="related-topics"></a><span data-ttu-id="b2aea-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2aea-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2aea-131">Sincronização de chamadas</span><span class="sxs-lookup"><span data-stu-id="b2aea-131">Call Synchronization</span></span>](call-synchronization.md)
</dt> <dt>

[<span data-ttu-id="b2aea-132">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="b2aea-132">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




