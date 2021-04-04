---
title: Atributos de tipo
description: RPC (chamada de procedimento remoto) e os atributos de tipo MIDL que podem ser aplicados a declarações de tipo.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823781"
---
# <a name="type-attributes"></a><span data-ttu-id="2a109-103">Atributos de tipo</span><span class="sxs-lookup"><span data-stu-id="2a109-103">Type Attributes</span></span>

<span data-ttu-id="2a109-104">Atributos de tipo são os atributos MIDL que podem ser aplicados a declarações de tipo:</span><span class="sxs-lookup"><span data-stu-id="2a109-104">Type attributes are the MIDL attributes that can be applied to type declarations:</span></span>

-   <span data-ttu-id="2a109-105">**\[**[**processamento**](/windows/desktop/Midl/handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="2a109-105">**\[**[**handle**](/windows/desktop/Midl/handle)**\]**</span></span>
-   <span data-ttu-id="2a109-106">**\[**[**identificador de contexto \_**](/windows/desktop/Midl/context-handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="2a109-106">**\[**[**context\_handle**](/windows/desktop/Midl/context-handle)**\]**</span></span>
-   <span data-ttu-id="2a109-107">**\[**[**tipo de comutador \_**](/windows/desktop/Midl/switch-type)**\]**</span><span class="sxs-lookup"><span data-stu-id="2a109-107">**\[**[**switch\_type**](/windows/desktop/Midl/switch-type)**\]**</span></span>
-   [<span data-ttu-id="2a109-108">atributos de tipo de ponteiro</span><span class="sxs-lookup"><span data-stu-id="2a109-108">pointer type attributes</span></span>](three-pointer-types.md)

<span data-ttu-id="2a109-109">O atributo **\[ \_ tipo \] de comutador** designa o tipo de um discriminador Union.</span><span class="sxs-lookup"><span data-stu-id="2a109-109">The **\[switch\_type\]** attribute designates the type of a union discriminator.</span></span> <span data-ttu-id="2a109-110">Esse atributo se aplica somente a uma União não encapsulada.</span><span class="sxs-lookup"><span data-stu-id="2a109-110">This attribute applies only to a nonencapsulated union.</span></span>

<span data-ttu-id="2a109-111">Um identificador de contexto é um ponteiro com um atributo de **\[ \_ identificador \] de contexto** .</span><span class="sxs-lookup"><span data-stu-id="2a109-111">A context handle is a pointer with a **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="2a109-112">O atributo **\[ \_ identificador \] de contexto** permite que você escreva procedimentos que mantêm informações de estado entre chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="2a109-112">The **\[context\_handle\]** attribute allows you to write procedures that maintain state information between remote procedure calls.</span></span> <span data-ttu-id="2a109-113">Um identificador de contexto com um valor não nulo representa o contexto salvo e serve para duas finalidades:</span><span class="sxs-lookup"><span data-stu-id="2a109-113">A context handle with a non-null value represents saved context and serves two purposes:</span></span>

-   <span data-ttu-id="2a109-114">No lado do cliente, ele contém as informações necessárias para a biblioteca de tempo de execução RPC para direcionar a chamada para o servidor.</span><span class="sxs-lookup"><span data-stu-id="2a109-114">On the client side, it contains the information needed by the RPC run-time library to direct the call to the server.</span></span>
-   <span data-ttu-id="2a109-115">No lado do servidor, ele serve como um identificador no contexto ativo.</span><span class="sxs-lookup"><span data-stu-id="2a109-115">On the server side, it serves as a handle on active context.</span></span>

<span data-ttu-id="2a109-116">O **\[** [](/windows/desktop/Midl/handle) **\]** atributo Handle especifica que um tipo pode ocorrer como um identificador definido pelo usuário (genérico).</span><span class="sxs-lookup"><span data-stu-id="2a109-116">The **\[**[**handle**](/windows/desktop/Midl/handle)**\]** attribute specifies that a type can occur as a user-defined (generic) handle.</span></span> <span data-ttu-id="2a109-117">Esse recurso permite o design de identificadores que são significativos para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a109-117">This feature permits the design of handles that are meaningful to the application.</span></span> <span data-ttu-id="2a109-118">O usuário deve fornecer associações e desvinculação de rotinas para converter entre o tipo de identificador definido pelo usuário e o tipo de identificador de RPC primitivo, **tratar \_ t**.</span><span class="sxs-lookup"><span data-stu-id="2a109-118">The user must provide binding and unbinding routines to convert between the user-defined handle type and the RPC primitive handle type, **handle\_t**.</span></span> <span data-ttu-id="2a109-119">Um identificador primitivo contém informações de destino significativas para as bibliotecas de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="2a109-119">A primitive handle contains destination information meaningful to the RPC run-time libraries.</span></span> <span data-ttu-id="2a109-120">Um identificador definido pelo usuário só pode ser definido em uma declaração de tipo, não em uma declaração de função.</span><span class="sxs-lookup"><span data-stu-id="2a109-120">A user-defined handle can only be defined in a type declaration, not in a function declaration.</span></span> <span data-ttu-id="2a109-121">Um parâmetro com o atributo **\[ Handle \]** tem uma finalidade dupla.</span><span class="sxs-lookup"><span data-stu-id="2a109-121">A parameter with the **\[handle\]** attribute has a double purpose.</span></span> <span data-ttu-id="2a109-122">Ele é usado para determinar a associação para a chamada e é transmitido para o procedimento chamado como um parâmetro de dados normal.</span><span class="sxs-lookup"><span data-stu-id="2a109-122">It is used to determine the binding for the call, and it is transmitted to the called procedure as a normal data parameter.</span></span>

 

 