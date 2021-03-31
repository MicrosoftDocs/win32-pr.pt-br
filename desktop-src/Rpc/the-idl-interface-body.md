---
title: O corpo da interface IDL
description: O corpo da interface IDL contém tipos de dados usados em chamadas de procedimento remoto e os protótipos de função para os procedimentos remotos.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641442"
---
# <a name="the-idl-interface-body"></a><span data-ttu-id="b62c1-103">O corpo da interface IDL</span><span class="sxs-lookup"><span data-stu-id="b62c1-103">The IDL Interface Body</span></span>

<span data-ttu-id="b62c1-104">O corpo da interface IDL contém tipos de dados usados em chamadas de procedimento remoto e os protótipos de função para os procedimentos remotos.</span><span class="sxs-lookup"><span data-stu-id="b62c1-104">The IDL interface body contains data types used in remote procedure calls and the function prototypes for the remote procedures.</span></span> <span data-ttu-id="b62c1-105">O corpo da interface também pode conter importações, pragmas, declarações constantes e declarações de tipo.</span><span class="sxs-lookup"><span data-stu-id="b62c1-105">The interface body can also contain imports, pragmas, constant declarations, and type declarations.</span></span> <span data-ttu-id="b62c1-106">No modo Microsoft-Extensions, o compilador MIDL também permite declarações implícitas na forma de definições de variáveis.</span><span class="sxs-lookup"><span data-stu-id="b62c1-106">In Microsoft-extensions mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="b62c1-107">O exemplo a seguir mostra um arquivo IDL contendo a definição de uma interface.</span><span class="sxs-lookup"><span data-stu-id="b62c1-107">The following example shows an IDL file containing the definition of an interface.</span></span> <span data-ttu-id="b62c1-108">O corpo da definição de interface, que ocorre entre chaves, contém a definição de uma constante (**bufsize**), um tipo (**\_ \_ tipo de identificador PCONTEXT**) e alguns procedimentos remotos (**RemoteOpen**, **RemoteRead**, **RemoteClose** e **Shutdown**).</span><span class="sxs-lookup"><span data-stu-id="b62c1-108">The body of the interface definition, which occurs between the curly brackets, contains the definition of a constant (**BUFSIZE**), a type (**PCONTEXT\_HANDLE\_TYPE**), and some remote procedures (**RemoteOpen**, **RemoteRead**, **RemoteClose**, and **Shutdown**).</span></span>

``` syntax
[ 
  uuid (ba209999-0c6c-11d2-97cf-00c04f8eea45), 
  version(1.0), 
  pointer_default(unique) 
] 
interface cxhndl 
{ 
 
  const short BUFSIZE = 1024;  
 
  typedef [context_handle] void *PCONTEXT_HANDLE_TYPE; 
 
  short RemoteOpen( 
      [out] PCONTEXT_HANDLE_TYPE *pphContext, 
      [in, string] unsigned char *pszFile 
  ); 
 
   short RemoteRead( 
      [in]  PCONTEXT_HANDLE_TYPE phContext, 
      [out] unsigned char achBuf[BUFSIZE], 
      [out] short *pcbBuf 
  ); 
 
  short RemoteClose( [in, out] PCONTEXT_HANDLE_TYPE *pphContext ); 
 
  void Shutdown(void); 
 
}
```

<span data-ttu-id="b62c1-109">Para obter mais informações, consulte a [referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="b62c1-109">For more information see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 