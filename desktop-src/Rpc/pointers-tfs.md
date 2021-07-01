---
title: Ponteiros (RPC)
description: Saiba mais sobre um ponteiro comum RPC, que é definido como tudo que não seja ponteiros de interface e ponteiros de contagem de byte.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119701"
---
# <a name="pointers-rpc"></a><span data-ttu-id="b7ea7-103">Ponteiros (RPC)</span><span class="sxs-lookup"><span data-stu-id="b7ea7-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="b7ea7-104">Ponteiros comuns</span><span class="sxs-lookup"><span data-stu-id="b7ea7-104">Common Pointers</span></span>

<span data-ttu-id="b7ea7-105">Um ponteiro comum é definido como tudo que não seja ponteiros de interface e ponteiros de contagem de byte.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="b7ea7-106">Há dois layouts possíveis para a descrição:</span><span class="sxs-lookup"><span data-stu-id="b7ea7-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="b7ea7-107">–ou–</span><span class="sxs-lookup"><span data-stu-id="b7ea7-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="b7ea7-108">O primeiro formato será usado se o ponteiro for um ponteiro para um tipo simples ou um ponteiro de cadeia de caracteres nãoized.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="b7ea7-109">O segundo formato é usado para ponteiros para todos os outros tipos.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="b7ea7-110">Atributos de ponteiro indicam qual layout de descrição ele é com o sinalizador FC \_ SIMPLE \_ POINTER.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="b7ea7-111">o \_ tipo de<1> é um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="b7ea7-112">Caractere de formato</span><span class="sxs-lookup"><span data-stu-id="b7ea7-112">Format character</span></span> | <span data-ttu-id="b7ea7-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7ea7-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="b7ea7-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="b7ea7-114">FC\_RP</span></span>           | <span data-ttu-id="b7ea7-115">Um ponteiro de referência.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="b7ea7-116">FC \_ UP</span><span class="sxs-lookup"><span data-stu-id="b7ea7-116">FC\_UP</span></span>           | <span data-ttu-id="b7ea7-117">Um ponteiro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="b7ea7-118">FC \_ FP</span><span class="sxs-lookup"><span data-stu-id="b7ea7-118">FC\_FP</span></span>           | <span data-ttu-id="b7ea7-119">Um ponteiro completo.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-119">A full pointer.</span></span>                          |
| <span data-ttu-id="b7ea7-120">FC \_ OP</span><span class="sxs-lookup"><span data-stu-id="b7ea7-120">FC\_OP</span></span>           | <span data-ttu-id="b7ea7-121">Um ponteiro exclusivo em uma interface de objeto.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="b7ea7-122">O motivo para distinguir o FC OP é semântico: em interfaces de objeto, um ponteiro in,out deve ser liberado antes de desmarcar um novo objeto e atribuir um novo valor \_ \[ de \] ponteiro.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="b7ea7-123">Atributos \_ de ponteiro<1> podem ter qualquer um dos sinalizadores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="b7ea7-124">Atributo</span><span class="sxs-lookup"><span data-stu-id="b7ea7-124">Attribute</span></span> | <span data-ttu-id="b7ea7-125">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="b7ea7-125">Flag</span></span>              | <span data-ttu-id="b7ea7-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7ea7-126">Description</span></span>                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ea7-127">01</span><span class="sxs-lookup"><span data-stu-id="b7ea7-127">01</span></span>   | <span data-ttu-id="b7ea7-128">FC \_ ALLOCATE \_ ALL \_ NODES</span><span class="sxs-lookup"><span data-stu-id="b7ea7-128">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="b7ea7-129">O ponteiro faz parte de um esquema de alocação \_ (todos os nós).</span><span class="sxs-lookup"><span data-stu-id="b7ea7-129">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="b7ea7-130">02</span><span class="sxs-lookup"><span data-stu-id="b7ea7-130">02</span></span>   | <span data-ttu-id="b7ea7-131">FC \_ DONT \_ FREE</span><span class="sxs-lookup"><span data-stu-id="b7ea7-131">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="b7ea7-132">Um ponteiro allocate(don't \_ free).</span><span class="sxs-lookup"><span data-stu-id="b7ea7-132">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="b7ea7-133">04</span><span class="sxs-lookup"><span data-stu-id="b7ea7-133">04</span></span>   | <span data-ttu-id="b7ea7-134">FC \_ ALLOCED \_ ON \_ STACK</span><span class="sxs-lookup"><span data-stu-id="b7ea7-134">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="b7ea7-135">Um ponteiro cujo referent é alocado na pilha do stub.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-135">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="b7ea7-136">08</span><span class="sxs-lookup"><span data-stu-id="b7ea7-136">08</span></span>   | <span data-ttu-id="b7ea7-137">FC \_ SIMPLE \_ POINTER</span><span class="sxs-lookup"><span data-stu-id="b7ea7-137">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="b7ea7-138">Um ponteiro para um tipo simples ou uma cadeia de caracteres não compatível.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-138">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="b7ea7-139">Esse sinalizador que está sendo definido indica o layout da descrição do ponteiro como o layout de ponteiro simples descrito acima, caso contrário, o formato do descritor com o deslocamento é indicado.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-139">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="b7ea7-140">10</span><span class="sxs-lookup"><span data-stu-id="b7ea7-140">10</span></span>   | <span data-ttu-id="b7ea7-141">FC \_ POINTER \_ DEREF</span><span class="sxs-lookup"><span data-stu-id="b7ea7-141">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="b7ea7-142">Um ponteiro que deve ser desreferenciado antes de manipular o referenciamento do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-142">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="b7ea7-143">Os ponteiros que têm tamanho \_ is(), max \_ \_ is(), length is(), last \_ is() e/ou first \_ is() aplicados a \_ \_ eles têm \_ descrições de cadeia de caracteres de formato idênticas a um ponteiro para uma matriz do tipo apropriado (por exemplo, uma matriz compatível se size is() for aplicado, uma matriz variável compatível se size is() e length for aplicado).</span><span class="sxs-lookup"><span data-stu-id="b7ea7-143">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="b7ea7-144">Ponteiros de interface</span><span class="sxs-lookup"><span data-stu-id="b7ea7-144">Interface Pointers</span></span>

<span data-ttu-id="b7ea7-145">Uma cadeia de caracteres de formato de ponteiro de interface de objeto tem um dos dois formatos, dependendo se o IID correspondente é conhecido pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-145">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="b7ea7-146">Um ponteiro de interface com uma IID constante tem a seguinte descrição:</span><span class="sxs-lookup"><span data-stu-id="b7ea7-146">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="b7ea7-147">O iid<16> parte é o IID real para o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-147">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="b7ea7-148">A iid é escrita na cadeia de caracteres de formato em um formato idêntico à estrutura de dados guid: long, short, short, char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="b7ea7-148">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="b7ea7-149">A descrição de um ponteiro de interface com iid \_ is() aplicada a ele é:</span><span class="sxs-lookup"><span data-stu-id="b7ea7-149">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="b7ea7-150">A descrição iid<> é um descritor de correlação e tem 4 ou \_ 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-150">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="b7ea7-151">O valor calculado pela função **NdrComputeConformance** é o ponteiro IID.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-151">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="b7ea7-152">Ponteiros de contagem de byte</span><span class="sxs-lookup"><span data-stu-id="b7ea7-152">Byte Count Pointers</span></span>

<span data-ttu-id="b7ea7-153">Os ponteiros de contagem de byte estão relacionados a um atributo de otimização especial chamado \[ **contagem de \_ byte** \] .</span><span class="sxs-lookup"><span data-stu-id="b7ea7-153">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="b7ea7-154">Os seguintes formatos são usados:</span><span class="sxs-lookup"><span data-stu-id="b7ea7-154">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="b7ea7-155">–e –</span><span class="sxs-lookup"><span data-stu-id="b7ea7-155">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="b7ea7-156">A descrição da contagem de<> é um descritor de correlação e tem 4 ou \_ \_ 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-156">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="b7ea7-157">A descrição \_ do<> é uma descrição do tipo de pointee.</span><span class="sxs-lookup"><span data-stu-id="b7ea7-157">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
