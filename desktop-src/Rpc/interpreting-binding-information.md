---
title: Interpretando informações de associação
description: O Microsoft RPC permite que seus programas de cliente e servidor acessem e interpretam as informações em um identificador de ligação.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- Chamada de procedimento remoto RPC, tarefas, interpretando Associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453719"
---
# <a name="interpreting-binding-information"></a><span data-ttu-id="c542f-104">Interpretando informações de associação</span><span class="sxs-lookup"><span data-stu-id="c542f-104">Interpreting Binding Information</span></span>

<span data-ttu-id="c542f-105">O Microsoft RPC permite que seus programas de cliente e servidor acessem e interpretam as informações em um identificador de ligação.</span><span class="sxs-lookup"><span data-stu-id="c542f-105">Microsoft RPC enables your client and server programs access to and interpret the information in a binding handle.</span></span> <span data-ttu-id="c542f-106">Isso não significa que você pode ou deve tentar acessar o conteúdo de um identificador de associação diretamente.</span><span class="sxs-lookup"><span data-stu-id="c542f-106">This does not mean that you can or should try to access the contents of a binding handle directly.</span></span> <span data-ttu-id="c542f-107">O Microsoft RPC fornece funções que definem e recuperam as informações em identificadores de associação.</span><span class="sxs-lookup"><span data-stu-id="c542f-107">Microsoft RPC provides functions that set and retrieve the information in binding handles.</span></span>

<span data-ttu-id="c542f-108">Para obter as informações em um identificador de ligação, passe o identificador para [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="c542f-108">To get the information in a binding handle, pass the handle to [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="c542f-109">Ele retorna as informações de associação como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c542f-109">It returns the binding information as a string.</span></span> <span data-ttu-id="c542f-110">Para cada chamada para **RpcBindingToStringBinding**, você deve ter uma chamada correspondente para a função [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span><span class="sxs-lookup"><span data-stu-id="c542f-110">For every call to **RpcBindingToStringBinding**, you must have a corresponding call to the function [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span></span>

<span data-ttu-id="c542f-111">Você pode chamar a função [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para analisar a cadeia de caracteres Obtida de [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="c542f-111">You can call the function [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to parse the string you obtain from [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="c542f-112">Essa função aloca cadeias de caracteres para conter as informações analisadas.</span><span class="sxs-lookup"><span data-stu-id="c542f-112">This function allocates strings to contain the information it parses.</span></span> <span data-ttu-id="c542f-113">Se você não quiser que ele analise uma parte específica das informações de associação, passe um **NULL** como o valor desse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c542f-113">If you do not want it to parse a particular piece of binding information, pass a **NULL** as the value of that parameter.</span></span> <span data-ttu-id="c542f-114">Certifique-se de chamar [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para cada uma das cadeias de caracteres alocadas.</span><span class="sxs-lookup"><span data-stu-id="c542f-114">Be sure to call [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) for each of the strings it allocates.</span></span>

<span data-ttu-id="c542f-115">O fragmento de código a seguir ilustra como um aplicativo pode chamar essas funções.</span><span class="sxs-lookup"><span data-stu-id="c542f-115">The following code fragment illustrates how an application might call these functions.</span></span>


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



<span data-ttu-id="c542f-116">O código de exemplo anterior chama as funções [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) e [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para obter e analisar as informações em um identificador de associação válido.</span><span class="sxs-lookup"><span data-stu-id="c542f-116">The preceding sample code calls the functions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) and [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to get and parse the information in a valid binding handle.</span></span> <span data-ttu-id="c542f-117">Observe que o valor **NULL** foi passado como o segundo parâmetro para **RpcStringBindingParse**.</span><span class="sxs-lookup"><span data-stu-id="c542f-117">Note that the value **NULL** was passed as the second parameter to **RpcStringBindingParse**.</span></span> <span data-ttu-id="c542f-118">Isso faz com que a função ignore a análise do UUID do objeto.</span><span class="sxs-lookup"><span data-stu-id="c542f-118">This causes that function to skip parsing the object UUID.</span></span> <span data-ttu-id="c542f-119">Como não analisa o UUID, **RpcStringBindingParse** não alocará uma cadeia de caracteres para ele.</span><span class="sxs-lookup"><span data-stu-id="c542f-119">Since it does not parse the UUID, **RpcStringBindingParse** will not allocate a string for it.</span></span> <span data-ttu-id="c542f-120">Essa técnica permite que seu aplicativo aloque apenas memória para as informações que você está interessado em analisar e analisar.</span><span class="sxs-lookup"><span data-stu-id="c542f-120">This technique enables your application to only allocate memory for the information you are interested in parsing and analyzing.</span></span>

 

 




