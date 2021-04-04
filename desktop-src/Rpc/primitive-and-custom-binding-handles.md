---
title: Identificadores de associação primitivos e personalizados
description: Todos os identificadores declarados com os \_ tipos de identificador de associação t ou RPC \_ \_ são identificadores de associação primitivos.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008049"
---
# <a name="primitive-and-custom-binding-handles"></a><span data-ttu-id="1700a-103">Identificadores de associação primitivos e personalizados</span><span class="sxs-lookup"><span data-stu-id="1700a-103">Primitive and Custom Binding Handles</span></span>

<span data-ttu-id="1700a-104">Todos os identificadores declarados com os tipos de [**\_ \_ identificador de associação**](rpc-binding-handle.md) [ \_ t](/windows/desktop/Midl/handle-t) ou RPC são identificadores de associação primitivos.</span><span class="sxs-lookup"><span data-stu-id="1700a-104">All handles declared with the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types are primitive binding handles.</span></span> <span data-ttu-id="1700a-105">Você pode estender os tipos de [**identificador de \_ Associação \_**](rpc-binding-handle.md) [ \_ t](/windows/desktop/Midl/handle-t) ou RPC para incluir mais ou informações diferentes do que o tipo de identificador primitivo contém.</span><span class="sxs-lookup"><span data-stu-id="1700a-105">You can extend the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types to include more or different information than the primitive handle type contains.</span></span> <span data-ttu-id="1700a-106">Ao fazer isso, você cria um identificador de ligação personalizado.</span><span class="sxs-lookup"><span data-stu-id="1700a-106">When you do, you create a custom binding handle.</span></span>

<span data-ttu-id="1700a-107">Para fazer um identificador de ligação personalizado para seu aplicativo distribuído, você precisará criar seu próprio tipo de dados e especificar o \[ [](/windows/desktop/Midl/handle) \] atributo Handle em uma definição de tipo em seu arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="1700a-107">To make a custom binding handle for your distributed application, you will need to create your own data type and specify the \[ [handle](/windows/desktop/Midl/handle)\] attribute on a type definition in your IDL file.</span></span> <span data-ttu-id="1700a-108">Por fim, os arquivos stub mapeiam identificadores de associação personalizados para identificadores primitivos.</span><span class="sxs-lookup"><span data-stu-id="1700a-108">Ultimately, the stub files map custom binding handles to primitive handles.</span></span>

<span data-ttu-id="1700a-109">Se você criar seu próprio tipo de identificador de associação, também deverá fornecer rotinas de ligação e desvinculação que o stub de cliente usa para mapear um identificador personalizado para um identificador primitivo.</span><span class="sxs-lookup"><span data-stu-id="1700a-109">If you do create your own binding handle type, you must also supply bind and unbind routines that the client stub uses to map a custom handle to a primitive handle.</span></span> <span data-ttu-id="1700a-110">O stub chama suas rotinas BIND e Unbind no início e no final de cada chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="1700a-110">The stub calls your bind and unbind routines at the beginning and end of each remote procedure call.</span></span> <span data-ttu-id="1700a-111">As rotinas de associação e desvinculação devem estar de acordo com os seguintes protótipos de função.</span><span class="sxs-lookup"><span data-stu-id="1700a-111">The bind and unbind routines must conform to the following function prototypes.</span></span>



| <span data-ttu-id="1700a-112">Protótipo da função</span><span class="sxs-lookup"><span data-stu-id="1700a-112">Function prototype</span></span>                     | <span data-ttu-id="1700a-113">Description</span><span class="sxs-lookup"><span data-stu-id="1700a-113">Description</span></span>       |
|----------------------------------------|-------------------|
| <span data-ttu-id="1700a-114">tratar \_ \_ Associação de tipo t (*tipo*)</span><span class="sxs-lookup"><span data-stu-id="1700a-114">handle\_t type\_bind(*type*)</span></span>           | <span data-ttu-id="1700a-115">Rotina de associação</span><span class="sxs-lookup"><span data-stu-id="1700a-115">Binding routine</span></span>   |
| <span data-ttu-id="1700a-116">tipo void \_ desassociar (*tipo*, *identificador \_ t*)</span><span class="sxs-lookup"><span data-stu-id="1700a-116">void type\_unbind(*type*, *handle\_t*)</span></span> | <span data-ttu-id="1700a-117">Desassociando rotina</span><span class="sxs-lookup"><span data-stu-id="1700a-117">Unbinding routine</span></span> |



 

<span data-ttu-id="1700a-118">O exemplo a seguir mostra como um identificador de ligação personalizado pode ser definido no arquivo IDL:</span><span class="sxs-lookup"><span data-stu-id="1700a-118">The following example shows how a custom binding handle can be defined in the IDL file:</span></span>

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

<span data-ttu-id="1700a-119">Se a rotina de associação encontrar um erro, ela deverá gerar uma exceção usando a função [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) .</span><span class="sxs-lookup"><span data-stu-id="1700a-119">If the bind routine encounters an error, it should raise an exception using the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function.</span></span> <span data-ttu-id="1700a-120">O stub do cliente será limpo e permitirá que a exceção seja filtrada para o bloco de exceção em torno da chamada de procedimento remoto no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="1700a-120">The client stub will then clean up, and let the exception filter through to the exception block surrounding the remote procedure call on the client side.</span></span> <span data-ttu-id="1700a-121">Se a rotina de associação simplesmente retornar **NULL**, o código do cliente receberá uma associação de RPC \_ S \_ inválida \_ .</span><span class="sxs-lookup"><span data-stu-id="1700a-121">If the bind routine simply returns **NULL**, the client code gets error RPC\_S\_INVALID\_BINDING.</span></span> <span data-ttu-id="1700a-122">Embora isso possa ser aceitável em determinadas situações, outras situações (como memória insuficiente) não respondem bem.</span><span class="sxs-lookup"><span data-stu-id="1700a-122">While this might be acceptable in certain situations, other situations (such as being out of memory) do not respond well.</span></span> <span data-ttu-id="1700a-123">A rotina de desassociar deve ser projetada para que não falhe.</span><span class="sxs-lookup"><span data-stu-id="1700a-123">The unbind routine should be designed so that it does not fail.</span></span> <span data-ttu-id="1700a-124">A rotina de desassociar não deve gerar exceções.</span><span class="sxs-lookup"><span data-stu-id="1700a-124">The unbind routine should not raise exceptions.</span></span>

<span data-ttu-id="1700a-125">As rotinas de associação e desvinculação definidas pelo programador aparecem no aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="1700a-125">The programmer-defined bind and unbind routines appear in the client application.</span></span> <span data-ttu-id="1700a-126">No exemplo a seguir, a rotina BIND chama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para converter as informações de associação de cadeia de caracteres em um identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="1700a-126">In the following example, the bind routine calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to convert the string-binding information to a binding handle.</span></span> <span data-ttu-id="1700a-127">A rotina desassociar chama [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="1700a-127">The unbind routine calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to free the binding handle.</span></span>

<span data-ttu-id="1700a-128">O nome do identificador de associação definido pelo programador, o \_ tipo de identificador de dados \_ , aparece como parte do nome das funções.</span><span class="sxs-lookup"><span data-stu-id="1700a-128">The name of the programmer-defined binding handle, DATA\_HANDLE\_TYPE, appears as part of the name of the functions.</span></span> <span data-ttu-id="1700a-129">Ele também é usado como o tipo de parâmetro nos parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="1700a-129">It is also used as the parameter type in the function parameters.</span></span>

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

<span data-ttu-id="1700a-130">Os identificadores de ligação implícitos e explícitos podem ser identificadores primitivos ou personalizados.</span><span class="sxs-lookup"><span data-stu-id="1700a-130">Both implicit and explicit binding handles can either be primitive or custom handles.</span></span> <span data-ttu-id="1700a-131">Ou seja, um identificador pode ser:</span><span class="sxs-lookup"><span data-stu-id="1700a-131">That is, a handle may be:</span></span>

-   <span data-ttu-id="1700a-132">Primitivo e implícito</span><span class="sxs-lookup"><span data-stu-id="1700a-132">Primitive and implicit</span></span>
-   <span data-ttu-id="1700a-133">Personalizado e implícito</span><span class="sxs-lookup"><span data-stu-id="1700a-133">Custom and implicit</span></span>
-   <span data-ttu-id="1700a-134">Primitivo e explícito</span><span class="sxs-lookup"><span data-stu-id="1700a-134">Primitive and explicit</span></span>
-   <span data-ttu-id="1700a-135">Personalizado e explícito</span><span class="sxs-lookup"><span data-stu-id="1700a-135">Custom and explicit</span></span>

 

 