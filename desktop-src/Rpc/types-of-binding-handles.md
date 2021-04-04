---
title: Tipos de identificadores de associação
description: Os identificadores de associação podem ser automáticos, implícitos ou explícitos.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005880"
---
# <a name="types-of-binding-handles"></a><span data-ttu-id="fc961-103">Tipos de identificadores de associação</span><span class="sxs-lookup"><span data-stu-id="fc961-103">Types of Binding Handles</span></span>

<span data-ttu-id="fc961-104">Os identificadores de associação podem ser automáticos, implícitos ou explícitos.</span><span class="sxs-lookup"><span data-stu-id="fc961-104">Binding handles can be automatic, implicit, or explicit.</span></span> <span data-ttu-id="fc961-105">Elas diferem na quantidade de controle que o aplicativo tem sobre o processo de ligação.</span><span class="sxs-lookup"><span data-stu-id="fc961-105">They differ in the amount of control the application has over the binding process.</span></span> <span data-ttu-id="fc961-106">Como o nome sugere, a ligação automática manipula a vinculação automatizada.</span><span class="sxs-lookup"><span data-stu-id="fc961-106">As the name suggests, automatic binding handles automate binding.</span></span> <span data-ttu-id="fc961-107">Os aplicativos cliente e servidor não precisam de código para lidar com o processo de associação.</span><span class="sxs-lookup"><span data-stu-id="fc961-107">The client and server applications do not need code to handle the binding process.</span></span> <span data-ttu-id="fc961-108">Os identificadores de associação implícitas permitem que os programas cliente configurem o identificador de associação antes que a associação ocorra.</span><span class="sxs-lookup"><span data-stu-id="fc961-108">Implicit binding handles allow client programs to configure the binding handle before the binding takes place.</span></span> <span data-ttu-id="fc961-109">Depois que o cliente estabelece uma associação, a biblioteca de tempo de execução RPC manipula o restante.</span><span class="sxs-lookup"><span data-stu-id="fc961-109">After the client establishes a binding, the RPC run-time library handles the rest.</span></span> <span data-ttu-id="fc961-110">Os identificadores de associação explícitos movem o controle completo sobre o processo de associação no código-fonte do cliente e nos programas do servidor.</span><span class="sxs-lookup"><span data-stu-id="fc961-110">Explicit binding handles move complete control over the binding process into the source code of the client and the server programs.</span></span> <span data-ttu-id="fc961-111">Com esse controle vem maior complexidade.</span><span class="sxs-lookup"><span data-stu-id="fc961-111">With this control comes increased complexity.</span></span> <span data-ttu-id="fc961-112">Seu aplicativo deve chamar funções RPC para gerenciar a associação.</span><span class="sxs-lookup"><span data-stu-id="fc961-112">Your application must call RPC functions to manage the binding.</span></span> <span data-ttu-id="fc961-113">Isso não acontece automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fc961-113">It does not happen automatically.</span></span> <span data-ttu-id="fc961-114">Identificadores de associação explícitos são recomendados.</span><span class="sxs-lookup"><span data-stu-id="fc961-114">Explicit binding handles are recommended.</span></span>

<span data-ttu-id="fc961-115">O diagrama a seguir ilustra as diferenças entre identificadores de associação automáticos, implícitos e explícitos.</span><span class="sxs-lookup"><span data-stu-id="fc961-115">The following diagram illustrates the differences between automatic, implicit, and explicit binding handles.</span></span>

![diferenças entre identificadores de associação automático, implícito e explícito](images/bhand.png)

<span data-ttu-id="fc961-117">Além disso, cada identificador de associação é primitivo ou personalizado.</span><span class="sxs-lookup"><span data-stu-id="fc961-117">In addition, every binding handle is either primitive or custom.</span></span> <span data-ttu-id="fc961-118">Cada tipo de identificador de associação é discutido nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="fc961-118">Each type of binding handle is discussed in the following topics:</span></span>

-   [<span data-ttu-id="fc961-119">Identificadores de associação automática</span><span class="sxs-lookup"><span data-stu-id="fc961-119">Automatic Binding Handles</span></span>](automatic-binding-handles.md)
-   [<span data-ttu-id="fc961-120">Identificadores de associação implícita</span><span class="sxs-lookup"><span data-stu-id="fc961-120">Implicit Binding Handles</span></span>](implicit-binding-handles.md)
-   [<span data-ttu-id="fc961-121">Identificadores de associação explícitos</span><span class="sxs-lookup"><span data-stu-id="fc961-121">Explicit Binding Handles</span></span>](explicit-binding-handles.md)
-   [<span data-ttu-id="fc961-122">Identificadores de associação primitivos e personalizados</span><span class="sxs-lookup"><span data-stu-id="fc961-122">Primitive and Custom Binding Handles</span></span>](primitive-and-custom-binding-handles.md)

 

 




