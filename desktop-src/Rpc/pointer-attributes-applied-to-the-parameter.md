---
title: Atributos de ponteiro aplicados ao parâmetro
description: Cada atributo de ponteiro (\ ref \, \ Unique \ e \ PTR \) tem características que afetam a alocação de memória. A tabela a seguir resume essas características.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007995"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a><span data-ttu-id="a1f0f-104">Atributos de ponteiro aplicados ao parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1f0f-104">Pointer Attributes Applied to the Parameter</span></span>

<span data-ttu-id="a1f0f-105">Cada atributo de ponteiro ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [Unique](/windows/desktop/Midl/unique) \] e \[ [PTR](/windows/desktop/Midl/ptr) \] ) tem características que afetam a alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-105">Each pointer attribute (\[ [ref](/windows/desktop/Midl/ref)\], \[ [unique](/windows/desktop/Midl/unique)\], and \[ [ptr](/windows/desktop/Midl/ptr)\]) has characteristics that affect memory allocation.</span></span> <span data-ttu-id="a1f0f-106">A tabela a seguir resume essas características.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-106">The following table summarizes these characteristics.</span></span>



| <span data-ttu-id="a1f0f-107">Atributo de ponteiro</span><span class="sxs-lookup"><span data-stu-id="a1f0f-107">Pointer attribute</span></span>       | <span data-ttu-id="a1f0f-108">Cliente</span><span class="sxs-lookup"><span data-stu-id="a1f0f-108">Client</span></span>                                                                                                                                                                                                            | <span data-ttu-id="a1f0f-109">Servidor</span><span class="sxs-lookup"><span data-stu-id="a1f0f-109">Server</span></span>                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a1f0f-110">Referência ( \[ **ref** \] )</span><span class="sxs-lookup"><span data-stu-id="a1f0f-110">Reference (\[**ref**\])</span></span> | <span data-ttu-id="a1f0f-111">O aplicativo cliente deve alocar.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-111">Client application must allocate.</span></span>                                                                                                                                                                                 | <span data-ttu-id="a1f0f-112">Tratamento especial necessário para ponteiros de nível nontop somente **\[ out \]**.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-112">Special handling needed for **\[out\]**-only nontop-level pointers.</span></span> |
| <span data-ttu-id="a1f0f-113">Exclusivo ( \[ **exclusivo** \] )</span><span class="sxs-lookup"><span data-stu-id="a1f0f-113">Unique (\[**unique**\])</span></span> | <span data-ttu-id="a1f0f-114">Se um parâmetro, o aplicativo cliente deve alocar; se inserido, pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-114">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="a1f0f-115">A alteração de NULL para non-null faz com que o stub do cliente seja alocado; alterar de não nulo para nulo pode causar órfãos.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-115">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |
| <span data-ttu-id="a1f0f-116">Completo ( \[ **PTR** \] )</span><span class="sxs-lookup"><span data-stu-id="a1f0f-116">Full (\[**ptr**\])</span></span>      | <span data-ttu-id="a1f0f-117">Se um parâmetro, o aplicativo cliente deve alocar; se inserido, pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-117">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="a1f0f-118">A alteração de NULL para non-null faz com que o stub do cliente seja alocado; alterar de não nulo para nulo pode causar órfãos.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-118">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |



 

<span data-ttu-id="a1f0f-119">O atributo **\[ ref \]** indica que o ponteiro aponta para uma memória válida.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-119">The **\[ref\]** attribute indicates that the pointer points to valid memory.</span></span> <span data-ttu-id="a1f0f-120">Por definição, o aplicativo cliente deve alocar toda a memória que os ponteiros de referência exigem.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-120">By definition, the client application must allocate all the memory that the reference pointers require.</span></span>

<span data-ttu-id="a1f0f-121">O ponteiro exclusivo pode mudar de nulo para não nulo.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-121">The unique pointer can change from null to non-null.</span></span> <span data-ttu-id="a1f0f-122">Se o ponteiro exclusivo mudar de nulo para não nulo, a nova memória será alocada no cliente.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-122">If the unique pointer changes from null to non-null, new memory is allocated on the client.</span></span> <span data-ttu-id="a1f0f-123">Se o ponteiro exclusivo mudar de não nulo para nulo, o órfão poderá resultar.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-123">If the unique pointer changes from non-null to null, orphaning can result.</span></span> <span data-ttu-id="a1f0f-124">Para obter mais informações, consulte [órfãos de memória](memory-orphaning.md).</span><span class="sxs-lookup"><span data-stu-id="a1f0f-124">For more information, see [Memory Orphaning](memory-orphaning.md).</span></span>

 

