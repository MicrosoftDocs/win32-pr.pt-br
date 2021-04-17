---
title: Exemplos (RPC)
description: Exemplos que demonstram conceitos de RPC (chamada de procedimento remoto).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- RPC de chamada de procedimento remoto, exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105754299"
---
# <a name="examples-rpc"></a><span data-ttu-id="c8413-104">Exemplos (RPC)</span><span class="sxs-lookup"><span data-stu-id="c8413-104">Examples (RPC)</span></span>

<span data-ttu-id="c8413-105">O SDK (Software Development Kit) da plataforma inclui exemplos que demonstram uma variedade de conceitos de RPC (chamada de procedimento remoto), da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c8413-105">The Platform Software Development Kit (SDK) includes examples that demonstrate a variety of Remote Procedure Call (RPC) concepts, as follows:</span></span>

-   <span data-ttu-id="c8413-106">ASYNCRPC ilustra a estrutura de um aplicativo RPC que usa chamadas de procedimento remoto assíncronas.</span><span class="sxs-lookup"><span data-stu-id="c8413-106">ASYNCRPC illustrates the structure of an RPC application that uses asynchronous remote procedure calls.</span></span> <span data-ttu-id="c8413-107">Ele também demonstra vários métodos de notificação da conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="c8413-107">It also demonstrates various methods of notification of the call's completion.</span></span>
-   <span data-ttu-id="c8413-108">CLUUID demonstra o uso do UUID de objeto de cliente para permitir que um cliente selecione várias implementações de um procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="c8413-108">CLUUID demonstrates use of the client-object UUID to enable a client to select from multiple implementations of a remote procedure.</span></span>
-   <span data-ttu-id="c8413-109">O diretório de dados contém quatro programas: DUNION ilustra uniões discriminadas (não encapsuladas); O Inout demonstra os parâmetros [ \[ de \] ](../midl/in.md) [ \[ saída \] ](../midl/out-idl.md) ; REPAS demonstra a [representação \_ como](/windows/desktop/Midl/represent-as) atributo; TRANSMISSÃO demonstra o atributo [transmitir \_ como](/windows/desktop/Midl/transmit-as) .</span><span class="sxs-lookup"><span data-stu-id="c8413-109">DATA directory contains four programs: DUNION illustrates discriminated (nonencapsulated) unions; INOUT demonstrates [\[in\]](../midl/in.md), [\[out\]](../midl/out-idl.md) parameters; REPAS demonstrates the [represent\_as](/windows/desktop/Midl/represent-as) attribute; XMIT demonstrates the [transmit\_as](/windows/desktop/Midl/transmit-as) attribute.</span></span>
-   <span data-ttu-id="c8413-110">DYNEPT demonstra um aplicativo cliente Gerenciando sua conexão com o servidor por meio de pontos de extremidade dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="c8413-110">DYNEPT demonstrates a client application managing its connection to the server through dynamic endpoints.</span></span>
-   <span data-ttu-id="c8413-111">O diretório FILEREP contém quatro exemplos que ilustram como os desenvolvedores podem escrever um serviço de replicação de arquivo simples, um serviço de replicação de arquivo multiusuário, um serviço que dá suporte a recursos de segurança e um serviço usando pipes assíncronos RPC.</span><span class="sxs-lookup"><span data-stu-id="c8413-111">FILEREP directory contains four samples illustrating how developers can write a simple file replication service, a multi-user file replication service, a service supporting security features, and a service using RPC asynchronous pipes.</span></span>
-   <span data-ttu-id="c8413-112">O diretório HANDLES contém três programas, AUTO, CXHNDL, USRDEF, que demonstram [ \_ identificadores automáticos](/windows/desktop/Midl/auto-handle), \[ \_ identificadores de contexto \] e identificadores genéricos (definidos pelo usuário), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c8413-112">HANDLES directory contains three programs, AUTO, CXHNDL, USRDEF, which demonstrate [auto\_handle](/windows/desktop/Midl/auto-handle), \[context\_handle\], and generic (user-defined) handles, respectively.</span></span>
-   <span data-ttu-id="c8413-113">Olá é uma implementação de cliente/servidor de "Olá, mundo".</span><span class="sxs-lookup"><span data-stu-id="c8413-113">HELLO is a client/server implementation of "Hello, world."</span></span>
-   <span data-ttu-id="c8413-114">O diretório PICKLE contém dois programas: PICKLP demonstra a serialização de procedimento de dados; PICKLT demonstra a serialização de tipo de dados; ambos os programas usam os atributos de [ \[ codificação \] ](../midl/encode.md) e [ \[ decodificação \] ](../midl/decode.md) .</span><span class="sxs-lookup"><span data-stu-id="c8413-114">PICKLE directory contains two programs: PICKLP demonstrates data procedure serialization; PICKLT demonstrates data type serialization; both programs use the [\[encode\]](../midl/encode.md) and [\[decode\]](../midl/decode.md) attributes.</span></span>
-   <span data-ttu-id="c8413-115">Pipes demonstra o uso do construtor de tipo de pipe.</span><span class="sxs-lookup"><span data-stu-id="c8413-115">PIPES demonstrates the use of the pipe-type constructor.</span></span>
-   <span data-ttu-id="c8413-116">RPCSVC demonstra a implementação de um serviço com RPC.</span><span class="sxs-lookup"><span data-stu-id="c8413-116">RPCSVC demonstrates the implementation of a service with RPC.</span></span>
-   <span data-ttu-id="c8413-117">STROUT demonstra como alocar memória em um servidor para um objeto bidimensional (uma matriz de ponteiros) e passá-lo de volta para o cliente como um \[ \] parâmetro somente out.</span><span class="sxs-lookup"><span data-stu-id="c8413-117">STROUT demonstrates how to allocate memory at a server for a two-dimensional object (an array of pointers) and pass it back to the client as an \[out\]-only parameter.</span></span> <span data-ttu-id="c8413-118">Em seguida, o cliente libera a memória.</span><span class="sxs-lookup"><span data-stu-id="c8413-118">The client then frees the memory.</span></span> <span data-ttu-id="c8413-119">Essa técnica permite que o stub chame o servidor sem saber com antecedência a quantidade de dados que será retornada.</span><span class="sxs-lookup"><span data-stu-id="c8413-119">This technique allows the stub to call the server without knowing in advance how much data will be returned.</span></span>

    <span data-ttu-id="c8413-120">Esse programa também permite que o usuário compile para UNICODE ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="c8413-120">This program also allows the user to compile either for UNICODE or ANSI.</span></span>

<span data-ttu-id="c8413-121">Todos os arquivos de origem e os makefiles para esses programas estão localizados no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="c8413-121">All of the source files and makefiles for these programs are located in the Platform SDK.</span></span>

<span data-ttu-id="c8413-122">Para o desenvolvimento de aplicativos RPC básico e exemplos mais simples, consulte os tópicos do [tutorial](tutorial.md) .</span><span class="sxs-lookup"><span data-stu-id="c8413-122">For basic RPC application development and simpler examples, please see the [Tutorial](tutorial.md) topics.</span></span>

 

 
