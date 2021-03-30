---
title: Desenvolvimento de interface usando identificadores de contexto
description: Normalmente, você cria um identificador de contexto especificando o atributo \ Context \_ Handle \ em uma definição de tipo no arquivo IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641602"
---
# <a name="interface-development-using-context-handles"></a><span data-ttu-id="49981-103">Desenvolvimento de interface usando identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="49981-103">Interface Development Using Context Handles</span></span>

<span data-ttu-id="49981-104">Normalmente, você cria um identificador de contexto especificando o \[ atributo de [**\_ identificador de contexto**](/windows/desktop/Midl/context-handle) \] em uma definição de tipo no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="49981-104">Typically, you create a context handle by specifying the \[[**context\_handle**](/windows/desktop/Midl/context-handle)\] attribute on a type definition in the IDL file.</span></span> <span data-ttu-id="49981-105">A definição de tipo também especifica implicitamente uma rotina de execução de contexto que você deve fornecer.</span><span class="sxs-lookup"><span data-stu-id="49981-105">The type definition also implicitly specifies a context run-down routine, which you must provide.</span></span> <span data-ttu-id="49981-106">Se a comunicação entre o cliente e o servidor for interrompida, o tempo de execução do servidor invoca essa rotina para executar qualquer limpeza necessária.</span><span class="sxs-lookup"><span data-stu-id="49981-106">If communication between the client and server breaks down, the server run time invokes this routine to perform any needed cleanup.</span></span> <span data-ttu-id="49981-107">Para obter mais informações sobre rotinas de execução de contexto, consulte [rotina de execução de contexto de servidor](server-context-run-down-routine.md).</span><span class="sxs-lookup"><span data-stu-id="49981-107">For more information on context run-down routines, see [Server Context Run-down Routine](server-context-run-down-routine.md).</span></span>

<span data-ttu-id="49981-108">Uma interface que usa um identificador de contexto deve ter um identificador de associação para a associação inicial, que precisa ocorrer antes que o servidor possa retornar um identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="49981-108">An interface that uses a context handle must have a binding handle for the initial binding, which has to take place before the server can return a context handle.</span></span> <span data-ttu-id="49981-109">Você pode usar um identificador de associação automático, implícito ou explícito para criar a associação e estabelecer o contexto.</span><span class="sxs-lookup"><span data-stu-id="49981-109">You can use an automatic, implicit, or explicit binding handle to create the binding and establish the context.</span></span>

<span data-ttu-id="49981-110">Um identificador de contexto deve ser do [**tipo \* void**](/windows/desktop/Midl/void) ou um tipo que resolve para [**void \***](/windows/desktop/Midl/void).</span><span class="sxs-lookup"><span data-stu-id="49981-110">A context handle must be of the [**void \***](/windows/desktop/Midl/void) type, or a type that resolves to [**void \***](/windows/desktop/Midl/void).</span></span> <span data-ttu-id="49981-111">O programa do servidor o converte para o tipo necessário.</span><span class="sxs-lookup"><span data-stu-id="49981-111">The server program casts it to the required type.</span></span>

> [!Note]  
> <span data-ttu-id="49981-112">O uso de \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] para parâmetros de identificador de contexto é desencorajado, exceto para rotinas que fecham identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="49981-112">The use of \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] for context handle parameters is discouraged except for routines that close context handles.</span></span> <span data-ttu-id="49981-113">Se o contexto manipula os parâmetros marcados como \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] são usados, não passe um identificador de contexto **nulo** ou não inicializado do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="49981-113">If context handles parameters marked \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] are used, do not pass a **NULL** or uninitialized context handle from the client to the server.</span></span> <span data-ttu-id="49981-114">Em vez disso, um ponteiro **nulo** para um identificador de contexto deve ser passado.</span><span class="sxs-lookup"><span data-stu-id="49981-114">A **NULL** pointer to a context handle should be passed instead.</span></span> <span data-ttu-id="49981-115">Observe que os parâmetros de identificador de contexto marcados \[ [**em**](/windows/desktop/Midl/in) não \] aceitam ponteiros **nulos** .</span><span class="sxs-lookup"><span data-stu-id="49981-115">Please note, context handle parameters marked \[[**in**](/windows/desktop/Midl/in)\] do not accept **NULL** pointers.</span></span>

 

<span data-ttu-id="49981-116">O fragmento a seguir de uma definição de interface de exemplo mostra como um aplicativo distribuído pode usar um identificador de contexto para ter um servidor aberto e atualizar um arquivo de dados para cada cliente.</span><span class="sxs-lookup"><span data-stu-id="49981-116">The following fragment of a sample interface definition shows how a distributed application can use a context handle to have a server open and update a data file for each client.</span></span>

<span data-ttu-id="49981-117">A interface deve conter uma chamada de procedimento remoto para inicializar o identificador e defini-lo como um valor não **nulo** .</span><span class="sxs-lookup"><span data-stu-id="49981-117">The interface must contain a remote procedure call to initialize the handle and set it to a non-**null** value.</span></span> <span data-ttu-id="49981-118">Neste exemplo, a função RemoteOpen executa essa operação.</span><span class="sxs-lookup"><span data-stu-id="49981-118">In this example, the RemoteOpen function performs this operation.</span></span> <span data-ttu-id="49981-119">Especifica o identificador de contexto com um \[ [](/windows/desktop/Midl/out-idl) \] atributo direcional out.</span><span class="sxs-lookup"><span data-stu-id="49981-119">It specifies the context handle with an \[[**out**](/windows/desktop/Midl/out-idl)\] directional attribute.</span></span> <span data-ttu-id="49981-120">Como alternativa, você pode retornar o identificador de contexto como o valor de retorno do procedimento.</span><span class="sxs-lookup"><span data-stu-id="49981-120">Alternatively, you could return the context handle as the procedure's return value.</span></span> <span data-ttu-id="49981-121">No entanto, neste exemplo, passaremos a alça de contexto por meio da lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="49981-121">However in this example, we'll pass the context handle out through the parameter list.</span></span>

<span data-ttu-id="49981-122">Neste exemplo, as informações de contexto são um identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="49981-122">In this example, the context information is a file handle.</span></span> <span data-ttu-id="49981-123">Ele controla o local atual no arquivo.</span><span class="sxs-lookup"><span data-stu-id="49981-123">It keeps track of the current location in the file.</span></span> <span data-ttu-id="49981-124">A interface empacota o identificador de arquivo como um identificador de contexto e o passa como um parâmetro para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="49981-124">The interface packages the file handle as a context handle and passes it as a parameter to remote procedure calls.</span></span> <span data-ttu-id="49981-125">Uma estrutura contém o nome do arquivo e o identificador do arquivo.</span><span class="sxs-lookup"><span data-stu-id="49981-125">A structure contains the file name and the file handle.</span></span>

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

<span data-ttu-id="49981-126">A função RemoteOpen cria um identificador de contexto válido e não **nulo** .</span><span class="sxs-lookup"><span data-stu-id="49981-126">The RemoteOpen function creates a valid, non-**null** context handle.</span></span> <span data-ttu-id="49981-127">Ele passa o identificador de contexto para o cliente.</span><span class="sxs-lookup"><span data-stu-id="49981-127">It passes the context handle to the client.</span></span> <span data-ttu-id="49981-128">As chamadas de procedimento remoto subsequentes, como RemoteRead, usam o identificador de contexto como um ponteiro de entrada.</span><span class="sxs-lookup"><span data-stu-id="49981-128">Subsequent remote procedure calls, such as RemoteRead, use the context handle as an in pointer.</span></span>

<span data-ttu-id="49981-129">Além do procedimento remoto que inicializa o identificador de contexto, a interface deve conter um procedimento que libera o contexto do servidor e define o identificador de contexto como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="49981-129">In addition to the remote procedure that initializes the context handle, the interface must contain a procedure that frees the server context and sets context handle to **NULL**.</span></span> <span data-ttu-id="49981-130">No exemplo anterior, a função RemoteClose executa essa operação.</span><span class="sxs-lookup"><span data-stu-id="49981-130">In the preceding example, the RemoteClose function performs this operation.</span></span>

 

 