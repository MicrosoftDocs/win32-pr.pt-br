---
title: Ponteiros (RPC)
description: Ponteiros
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cabf5109506bc1e194a39c809bfb43a8f952fbf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085049"
---
# <a name="pointers-rpc"></a><span data-ttu-id="49dea-103">Ponteiros (RPC)</span><span class="sxs-lookup"><span data-stu-id="49dea-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="49dea-104">Ponteiros comuns</span><span class="sxs-lookup"><span data-stu-id="49dea-104">Common Pointers</span></span>

<span data-ttu-id="49dea-105">Um ponteiro comum é definido como tudo que não seja ponteiros de interface e ponteiros de contagem de bytes.</span><span class="sxs-lookup"><span data-stu-id="49dea-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="49dea-106">Há dois layouts possíveis para a descrição:</span><span class="sxs-lookup"><span data-stu-id="49dea-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="49dea-107">–ou–</span><span class="sxs-lookup"><span data-stu-id="49dea-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="49dea-108">O primeiro formato será usado se o ponteiro for um ponteiro para um tipo simples ou um ponteiro de cadeia de caracteres não-dimensionado.</span><span class="sxs-lookup"><span data-stu-id="49dea-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="49dea-109">O segundo formato é usado para ponteiros para todos os outros tipos.</span><span class="sxs-lookup"><span data-stu-id="49dea-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="49dea-110">Atributos de ponteiro indicam qual layout de descrição é com o \_ sinalizador de ponteiro simples do FC \_ .</span><span class="sxs-lookup"><span data-stu-id="49dea-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="49dea-111">\_o tipo de ponteiro<1> é um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="49dea-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="49dea-112">Formatar caractere</span><span class="sxs-lookup"><span data-stu-id="49dea-112">Format character</span></span> | <span data-ttu-id="49dea-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="49dea-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="49dea-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="49dea-114">FC\_RP</span></span>           | <span data-ttu-id="49dea-115">Um ponteiro de referência.</span><span class="sxs-lookup"><span data-stu-id="49dea-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="49dea-116">FC \_ para cima</span><span class="sxs-lookup"><span data-stu-id="49dea-116">FC\_UP</span></span>           | <span data-ttu-id="49dea-117">Um ponteiro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="49dea-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="49dea-118">\_FP FC</span><span class="sxs-lookup"><span data-stu-id="49dea-118">FC\_FP</span></span>           | <span data-ttu-id="49dea-119">Um ponteiro completo.</span><span class="sxs-lookup"><span data-stu-id="49dea-119">A full pointer.</span></span>                          |
| <span data-ttu-id="49dea-120">\_op FC</span><span class="sxs-lookup"><span data-stu-id="49dea-120">FC\_OP</span></span>           | <span data-ttu-id="49dea-121">Um ponteiro exclusivo em uma interface de objeto.</span><span class="sxs-lookup"><span data-stu-id="49dea-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="49dea-122">O motivo para distinguir o FC \_ op é semântico: em interfaces de objeto, um \[ ponteiro de entrada \] deve ser liberado antes de desempacotar um novo objeto e atribuir um novo valor de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="49dea-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="49dea-123">Os \_ atributos de ponteiro<1> podem ter qualquer um dos sinalizadores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="49dea-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="49dea-124">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="49dea-124">Flag</span></span> | <span data-ttu-id="49dea-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="49dea-125">Description</span></span>              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49dea-126">01</span><span class="sxs-lookup"><span data-stu-id="49dea-126">01</span></span>   | <span data-ttu-id="49dea-127">\_alocar \_ todos os nós de FC \_</span><span class="sxs-lookup"><span data-stu-id="49dea-127">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="49dea-128">O ponteiro é uma parte de um esquema de alocação alocar (todos os \_ nós).</span><span class="sxs-lookup"><span data-stu-id="49dea-128">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="49dea-129">02</span><span class="sxs-lookup"><span data-stu-id="49dea-129">02</span></span>   | <span data-ttu-id="49dea-130">FC \_ não \_ livre</span><span class="sxs-lookup"><span data-stu-id="49dea-130">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="49dea-131">Um ponteiro de alocação (não \_ livre).</span><span class="sxs-lookup"><span data-stu-id="49dea-131">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="49dea-132">04</span><span class="sxs-lookup"><span data-stu-id="49dea-132">04</span></span>   | <span data-ttu-id="49dea-133">FC \_ alocado \_ na \_ pilha</span><span class="sxs-lookup"><span data-stu-id="49dea-133">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="49dea-134">Um ponteiro cujo Referent é alocado na pilha do stub.</span><span class="sxs-lookup"><span data-stu-id="49dea-134">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="49dea-135">08</span><span class="sxs-lookup"><span data-stu-id="49dea-135">08</span></span>   | <span data-ttu-id="49dea-136">\_ponteiro simples do FC \_</span><span class="sxs-lookup"><span data-stu-id="49dea-136">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="49dea-137">Um ponteiro para um tipo simples ou cadeia de caracteres de conformidade não dimensionável.</span><span class="sxs-lookup"><span data-stu-id="49dea-137">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="49dea-138">Esse sinalizador sendo definido indica o layout da descrição do ponteiro como o layout do ponteiro simples descrito acima, caso contrário, o formato do descritor com o deslocamento será indicado.</span><span class="sxs-lookup"><span data-stu-id="49dea-138">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="49dea-139">10</span><span class="sxs-lookup"><span data-stu-id="49dea-139">10</span></span>   | <span data-ttu-id="49dea-140">ponteiro de FC \_ \_ DEREF</span><span class="sxs-lookup"><span data-stu-id="49dea-140">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="49dea-141">Um ponteiro que deve ser desreferenciado antes de manipular o Referent do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="49dea-141">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="49dea-142">Ponteiros com tamanho \_ é (), o número máximo de \_ is (), length \_ é (), Last \_ is () e/ou First \_ is () aplicado a eles têm descrições de cadeia de caracteres de formato idênticas a um ponteiro para uma matriz do tipo apropriado (por exemplo, uma matriz compatível se o tamanho for \_ () for aplicado, uma matriz de variação em conformidade se o tamanho \_ for () e o comprimento \_ for aplicado</span><span class="sxs-lookup"><span data-stu-id="49dea-142">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="49dea-143">Ponteiros de interface</span><span class="sxs-lookup"><span data-stu-id="49dea-143">Interface Pointers</span></span>

<span data-ttu-id="49dea-144">Uma cadeia de caracteres de formato de ponteiro de interface de objeto tem um dos dois formatos, dependendo se o IID correspondente é conhecido pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="49dea-144">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="49dea-145">Um ponteiro de interface com uma IID de constante tem a seguinte descrição:</span><span class="sxs-lookup"><span data-stu-id="49dea-145">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="49dea-146">O IID<de 16> parte é o IID real para o ponteiro da interface.</span><span class="sxs-lookup"><span data-stu-id="49dea-146">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="49dea-147">O IID é gravado na cadeia de caracteres de formato em um formato idêntico à estrutura de dados GUID: longo, curto, curto, Char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="49dea-147">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="49dea-148">A descrição de um ponteiro de interface com IID \_ é () aplicada a ele é:</span><span class="sxs-lookup"><span data-stu-id="49dea-148">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="49dea-149">A descrição de IID \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="49dea-149">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="49dea-150">O valor calculado pela função **NdrComputeConformance** é o ponteiro de IID.</span><span class="sxs-lookup"><span data-stu-id="49dea-150">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="49dea-151">Ponteiros de contagem de bytes</span><span class="sxs-lookup"><span data-stu-id="49dea-151">Byte Count Pointers</span></span>

<span data-ttu-id="49dea-152">Os ponteiros de contagem de bytes estão relacionados a um atributo de otimização especial chamado \[ **\_ contagem de bytes** \] .</span><span class="sxs-lookup"><span data-stu-id="49dea-152">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="49dea-153">Os seguintes formatos são usados:</span><span class="sxs-lookup"><span data-stu-id="49dea-153">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="49dea-154">e</span><span class="sxs-lookup"><span data-stu-id="49dea-154">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="49dea-155">A descrição de contagem de bytes \_ \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="49dea-155">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="49dea-156">A descrição do ponto \_<> é uma descrição do tipo de ponto.</span><span class="sxs-lookup"><span data-stu-id="49dea-156">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
