---
title: Responsabilidades do servidor COM
description: Responsabilidades do servidor COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366761"
---
# <a name="com-server-responsibilities"></a><span data-ttu-id="55c9f-103">Responsabilidades do servidor COM</span><span class="sxs-lookup"><span data-stu-id="55c9f-103">COM Server Responsibilities</span></span>

<span data-ttu-id="55c9f-104">Uma das maneiras mais importantes para um cliente obter um ponteiro para um objeto é o cliente solicitar que um servidor seja iniciado e que uma instância do objeto fornecida pelo servidor seja criada e ativada.</span><span class="sxs-lookup"><span data-stu-id="55c9f-104">One of the most important ways for a client to get a pointer to an object is for the client to ask that a server be launched and that an instance of the object provided by the server be created and activated.</span></span> <span data-ttu-id="55c9f-105">É responsabilidade do servidor garantir que isso aconteça corretamente.</span><span class="sxs-lookup"><span data-stu-id="55c9f-105">It is the responsibility of the server to ensure that this happens properly.</span></span> <span data-ttu-id="55c9f-106">Há várias partes importantes para isso.</span><span class="sxs-lookup"><span data-stu-id="55c9f-106">There are several important parts to this.</span></span>

<span data-ttu-id="55c9f-107">O servidor deve implementar o código para um objeto de classe por meio de uma implementação da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .</span><span class="sxs-lookup"><span data-stu-id="55c9f-107">The server must implement code for a class object through an implementation of either the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface.</span></span>

<span data-ttu-id="55c9f-108">O servidor deve registrar seu CLSID no registro do sistema no computador em que ele reside e ainda mais, tem a opção de publicar seu local de computador em outros sistemas em uma rede para permitir que os clientes o chamem sem exigir que o cliente saiba o local do servidor.</span><span class="sxs-lookup"><span data-stu-id="55c9f-108">The server must register its CLSID in the system registry on the machine on which it resides and further, has the option of publishing its machine location to other systems on a network to allow clients to call it without requiring the client to know the server's location.</span></span>

<span data-ttu-id="55c9f-109">O servidor é responsável principalmente pela segurança; ou seja, para a maior parte, o servidor determina se ele fornecerá um ponteiro para um de seus objetos a um cliente.</span><span class="sxs-lookup"><span data-stu-id="55c9f-109">The server is primarily responsible for security; that is, for the most part, the server determines whether it will provide a pointer to one of its objects to a client.</span></span>

<span data-ttu-id="55c9f-110">Os servidores em processo devem implementar e exportar determinadas funções que permitam ao processo do cliente instanciá-las.</span><span class="sxs-lookup"><span data-stu-id="55c9f-110">In-process servers should implement and export certain functions that allow the client process to instantiate them.</span></span>

<span data-ttu-id="55c9f-111">Os tópicos a seguir detalham as responsabilidades do servidor COM:</span><span class="sxs-lookup"><span data-stu-id="55c9f-111">The following topics detail the responsibilities of the COM server:</span></span>

-   [<span data-ttu-id="55c9f-112">Implementando IClassFactory</span><span class="sxs-lookup"><span data-stu-id="55c9f-112">Implementing IClassFactory</span></span>](implementing-iclassfactory.md)
-   [<span data-ttu-id="55c9f-113">Licenciamento e IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="55c9f-113">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
-   [<span data-ttu-id="55c9f-114">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="55c9f-114">Registering COM Servers</span></span>](registering-com-servers.md)
-   [<span data-ttu-id="55c9f-115">Auxiliares de implementação do servidor fora do processo</span><span class="sxs-lookup"><span data-stu-id="55c9f-115">Out-of-Process Server Implementation Helpers</span></span>](out-of-process-server-implementation-helpers.md)
-   [<span data-ttu-id="55c9f-116">Criação e otimizações de GUID</span><span class="sxs-lookup"><span data-stu-id="55c9f-116">GUID Creation and Optimizations</span></span>](guid-creation-and-optimizations.md)

## <a name="related-topics"></a><span data-ttu-id="55c9f-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55c9f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55c9f-118">Clientes e servidores COM</span><span class="sxs-lookup"><span data-stu-id="55c9f-118">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 