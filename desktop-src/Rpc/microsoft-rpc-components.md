---
title: Componentes RPC
description: Componentes de RPC (chamada de procedimento remoto).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- RPC de chamada de procedimento remoto, descrito, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916326"
---
# <a name="rpc-components"></a><span data-ttu-id="d3260-104">Componentes RPC</span><span class="sxs-lookup"><span data-stu-id="d3260-104">RPC Components</span></span>

<span data-ttu-id="d3260-105">O RPC inclui os seguintes componentes principais:</span><span class="sxs-lookup"><span data-stu-id="d3260-105">RPC includes the following major components:</span></span>

-   <span data-ttu-id="d3260-106">Compilador de MIDL</span><span class="sxs-lookup"><span data-stu-id="d3260-106">MIDL compiler</span></span>
-   <span data-ttu-id="d3260-107">Bibliotecas de tempo de execução e arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d3260-107">Run-time libraries and header files</span></span>
-   <span data-ttu-id="d3260-108">Provedor de serviço de nome (às vezes chamado de localizador)</span><span class="sxs-lookup"><span data-stu-id="d3260-108">Name service provider (sometimes referred to as the Locator)</span></span>
-   <span data-ttu-id="d3260-109">Mapeador de ponto de extremidade (às vezes chamado de mapeador de porta)</span><span class="sxs-lookup"><span data-stu-id="d3260-109">Endpoint mapper (sometimes referred to as the port mapper)</span></span>

<span data-ttu-id="d3260-110">No modelo de RPC, você pode especificar formalmente uma interface para os procedimentos remotos usando uma linguagem projetada para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="d3260-110">In the RPC model, you can formally specify an interface to the remote procedures using a language designed for this purpose.</span></span> <span data-ttu-id="d3260-111">Esse idioma é chamado de linguagem de definição de interface, ou IDL.</span><span class="sxs-lookup"><span data-stu-id="d3260-111">This language is called the Interface Definition Language, or IDL.</span></span> <span data-ttu-id="d3260-112">A implementação da Microsoft desse idioma é chamada de linguagem IDL da Microsoft ou MIDL.</span><span class="sxs-lookup"><span data-stu-id="d3260-112">The Microsoft implementation of this language is called the Microsoft Interface Definition Language, or MIDL.</span></span>

<span data-ttu-id="d3260-113">Depois de criar uma interface, você deve passá-la por meio do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="d3260-113">After you create an interface, you must pass it through the MIDL compiler.</span></span> <span data-ttu-id="d3260-114">Esse compilador gera os stubs que convertem chamadas de procedimento local em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="d3260-114">This compiler generates the stubs that translate local procedure calls into remote procedure calls.</span></span> <span data-ttu-id="d3260-115">Os stubs são funções de espaço reservado que fazem as chamadas para as funções de biblioteca de tempo de execução, que gerenciam a chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="d3260-115">Stubs are placeholder functions that make the calls to the run-time library functions, which manage the remote procedure call.</span></span> <span data-ttu-id="d3260-116">A vantagem dessa abordagem é que a rede se torna quase completamente transparente para seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="d3260-116">The advantage of this approach is that the network becomes almost completely transparent to your distributed application.</span></span> <span data-ttu-id="d3260-117">O programa cliente chama o que parece ser procedimentos locais; o trabalho de transformá-los em chamadas remotas é feito automaticamente para você.</span><span class="sxs-lookup"><span data-stu-id="d3260-117">Your client program calls what appear to be local procedures; the work of turning them into remote calls is done for you automatically.</span></span> <span data-ttu-id="d3260-118">Todo o código que traduz dados, acessa a rede e recupera os resultados é gerado para você pelo compilador MIDL e é invisível para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3260-118">All the code that translates data, accesses the network, and retrieves results is generated for you by the MIDL compiler and is invisible to your application.</span></span>

 

 




