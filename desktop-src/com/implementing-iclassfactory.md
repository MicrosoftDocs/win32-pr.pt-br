---
title: Implementando IClassFactory
description: Implementando IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366741"
---
# <a name="implementing-iclassfactory"></a><span data-ttu-id="0e4b0-103">Implementando IClassFactory</span><span class="sxs-lookup"><span data-stu-id="0e4b0-103">Implementing IClassFactory</span></span>

<span data-ttu-id="0e4b0-104">Quando um cliente usa um CLSID para solicitar a criação de uma instância de objeto, a primeira etapa é a criação de um objeto de classe, um objeto intermediário que contém uma implementação dos métodos da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) .</span><span class="sxs-lookup"><span data-stu-id="0e4b0-104">When a client uses a CLSID to request the creation of an object instance, the first step is creation of a class object, an intermediate object that contains an implementation of the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface.</span></span> <span data-ttu-id="0e4b0-105">Embora o COM forneça várias funções de criação de instância, a primeira etapa na implementação dessas funções é a criação de um objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-105">While COM provides several instance creation functions, the first step in the implementation of these functions is the creation of a class object.</span></span>

<span data-ttu-id="0e4b0-106">Como resultado, todos os servidores devem implementar os métodos da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , que contém dois métodos:</span><span class="sxs-lookup"><span data-stu-id="0e4b0-106">As a result, all servers must implement the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface, which contains two methods:</span></span>

-   <span data-ttu-id="0e4b0-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="0e4b0-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span></span> <span data-ttu-id="0e4b0-108">Esse método deve criar uma instância não inicializada do objeto e retornar um ponteiro para uma interface solicitada no objeto.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-108">This method must create an uninitialized instance of the object and return a pointer to a requested interface on the object.</span></span>
-   <span data-ttu-id="0e4b0-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span><span class="sxs-lookup"><span data-stu-id="0e4b0-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span></span> <span data-ttu-id="0e4b0-110">Esse método apenas incrementa a contagem de referência no objeto de classe para garantir que o servidor permaneça na memória e não seja desligado antes que o cliente esteja pronto para fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-110">This method just increments the reference count on the class object to ensure that the server stays in memory and does not shut down before the client is ready for it to do so.</span></span>

<span data-ttu-id="0e4b0-111">Para permitir que um servidor seja responsável por seu próprio licenciamento, COM define [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), que herda sua definição de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="0e4b0-111">To enable a server to be responsible for its own licensing, COM defines [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), which inherits its definition from [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="0e4b0-112">Assim, um servidor que implementa **IClassFactory2** deve, por definição, implementar os métodos de **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-112">Thus, a server implementing **IClassFactory2** must, by definition, implement the methods of **IClassFactory**.</span></span>

<span data-ttu-id="0e4b0-113">O COM também fornece funções auxiliares para a implementação de servidores fora do processo.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-113">COM also provides helper functions for implementing out-of-process servers.</span></span> <span data-ttu-id="0e4b0-114">Para obter mais informações, consulte [auxiliares de implementação do servidor fora do processo](out-of-process-server-implementation-helpers.md).</span><span class="sxs-lookup"><span data-stu-id="0e4b0-114">For more information, see [Out-of-Process Server Implementation Helpers](out-of-process-server-implementation-helpers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e4b0-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e4b0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e4b0-116">Responsabilidades do servidor COM</span><span class="sxs-lookup"><span data-stu-id="0e4b0-116">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> <dt>

[<span data-ttu-id="0e4b0-117">Licenciamento e IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="0e4b0-117">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 