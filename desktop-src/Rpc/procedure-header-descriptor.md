---
title: Descritor de cabeçalho de procedimento
description: O cabeçalho foi estendido várias vezes ao longo da vida útil do mecanismo de NDR. O compilador atual ainda gera cabeçalhos diferentes dependendo do modo do compilador. No entanto, os cabeçalhos mais recentes são um superconjunto dos mais antigos.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454261"
---
# <a name="procedure-header-descriptor"></a><span data-ttu-id="a0153-105">Descritor de cabeçalho de procedimento</span><span class="sxs-lookup"><span data-stu-id="a0153-105">Procedure Header Descriptor</span></span>

<span data-ttu-id="a0153-106">O cabeçalho foi estendido várias vezes ao longo da vida útil do mecanismo de NDR.</span><span class="sxs-lookup"><span data-stu-id="a0153-106">The header has been extended several times over the life of the NDR engine.</span></span> <span data-ttu-id="a0153-107">O compilador atual ainda gera cabeçalhos diferentes dependendo do modo do compilador.</span><span class="sxs-lookup"><span data-stu-id="a0153-107">The current compiler still generates different headers depending on the mode of the compiler.</span></span> <span data-ttu-id="a0153-108">No entanto, os cabeçalhos mais recentes são um superconjunto dos mais antigos.</span><span class="sxs-lookup"><span data-stu-id="a0153-108">However, more recent headers are a superset of the older ones.</span></span>

## <a name="the-old-oi-header"></a><span data-ttu-id="a0153-109">O cabeçalho antigo-Oi</span><span class="sxs-lookup"><span data-stu-id="a0153-109">The Old –Oi Header</span></span>

<span data-ttu-id="a0153-110">O cabeçalho tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a0153-110">The header has the following format:</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="a0153-111">Em que \_ tipo de identificador<1> pode ser um dos valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a0153-111">Where handle\_type<1> can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="a0153-112">Hex</span><span class="sxs-lookup"><span data-stu-id="a0153-112">Hex</span></span> | <span data-ttu-id="a0153-113">Handle</span><span class="sxs-lookup"><span data-stu-id="a0153-113">Handle</span></span>               |
|-----|----------------------|
| <span data-ttu-id="a0153-114">31</span><span class="sxs-lookup"><span data-stu-id="a0153-114">31</span></span>  | <span data-ttu-id="a0153-115">FC \_ ligar \_ genérico</span><span class="sxs-lookup"><span data-stu-id="a0153-115">FC\_BIND\_GENERIC</span></span>    |
| <span data-ttu-id="a0153-116">32</span><span class="sxs-lookup"><span data-stu-id="a0153-116">32</span></span>  | <span data-ttu-id="a0153-117">\_primitivo de ligação FC \_</span><span class="sxs-lookup"><span data-stu-id="a0153-117">FC\_BIND\_PRIMITIVE</span></span>  |
| <span data-ttu-id="a0153-118">33</span><span class="sxs-lookup"><span data-stu-id="a0153-118">33</span></span>  | <span data-ttu-id="a0153-119">\_identificador auto do FC \_</span><span class="sxs-lookup"><span data-stu-id="a0153-119">FC\_AUTO\_HANDLE</span></span>     |
| <span data-ttu-id="a0153-120">34</span><span class="sxs-lookup"><span data-stu-id="a0153-120">34</span></span>  | <span data-ttu-id="a0153-121">\_identificador de retorno de chamada FC \_</span><span class="sxs-lookup"><span data-stu-id="a0153-121">FC\_CALLBACK\_HANDLE</span></span> |
| <span data-ttu-id="a0153-122">0</span><span class="sxs-lookup"><span data-stu-id="a0153-122">0</span></span>   | <span data-ttu-id="a0153-123">(identificador explícito)</span><span class="sxs-lookup"><span data-stu-id="a0153-123">(explicit handle)</span></span>    |



 

<span data-ttu-id="a0153-124">Se o tipo de identificador \_<1> campo for diferente de zero, o procedimento usará um identificador implícito do tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="a0153-124">If the handle\_type<1> field is nonzero, then the procedure uses an implicit handle of the indicated kind.</span></span> <span data-ttu-id="a0153-125">Consulte o tópico [identificadores](handles.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a0153-125">See the [Handles](handles.md) topic for a more information.</span></span> <span data-ttu-id="a0153-126">Se o tipo de identificador \_<1> campo for zero, o identificador usado para associação será um dos parâmetros do procedimento.</span><span class="sxs-lookup"><span data-stu-id="a0153-126">If the handle\_type<1> field is zero, the handle used for binding is one of the procedure's parameters.</span></span>

<span data-ttu-id="a0153-127">Identificadores explícitos podem ser primitivos, genéricos e de contexto; a última tem o token de FC a seguir.</span><span class="sxs-lookup"><span data-stu-id="a0153-127">Explicit handles can be primitive, generic, and context; the last one has the following FC token.</span></span>



| <span data-ttu-id="a0153-128">Hex</span><span class="sxs-lookup"><span data-stu-id="a0153-128">Hex</span></span> | <span data-ttu-id="a0153-129">Handle</span><span class="sxs-lookup"><span data-stu-id="a0153-129">Handle</span></span>            |
|-----|-------------------|
| <span data-ttu-id="a0153-130">30</span><span class="sxs-lookup"><span data-stu-id="a0153-130">30</span></span>  | <span data-ttu-id="a0153-131">\_contexto de ligação FC \_</span><span class="sxs-lookup"><span data-stu-id="a0153-131">FC\_BIND\_CONTEXT</span></span> |



 

<span data-ttu-id="a0153-132">Por convenção, o tipo de identificador para interfaces DCOM é o \_ identificador auto do FC \_ .</span><span class="sxs-lookup"><span data-stu-id="a0153-132">By convention, the handle type for DCOM interfaces is FC\_AUTO\_HANDLE.</span></span>

<span data-ttu-id="a0153-133">O \_ campo Oi flags<1> é uma máscara de 8 bits dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a0153-133">The Oi\_flags<1> field is an 8-bit mask of the following flags.</span></span>



| <span data-ttu-id="a0153-134">Hex</span><span class="sxs-lookup"><span data-stu-id="a0153-134">Hex</span></span> | <span data-ttu-id="a0153-135">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="a0153-135">Flag</span></span>                         | <span data-ttu-id="a0153-136">Significado</span><span class="sxs-lookup"><span data-stu-id="a0153-136">Meaning</span></span>                                  |
|-----|------------------------------|------------------------------------------|
| <span data-ttu-id="a0153-137">01</span><span class="sxs-lookup"><span data-stu-id="a0153-137">01</span></span>  | <span data-ttu-id="a0153-138">Oi \_ \_ PTR completo \_ usado</span><span class="sxs-lookup"><span data-stu-id="a0153-138">Oi\_FULL\_PTR\_USED</span></span>          | <span data-ttu-id="a0153-139">Usa o pacote de ponteiro completo.</span><span class="sxs-lookup"><span data-stu-id="a0153-139">Uses the full pointer package.</span></span>           |
| <span data-ttu-id="a0153-140">02</span><span class="sxs-lookup"><span data-stu-id="a0153-140">02</span></span>  | <span data-ttu-id="a0153-141">A \_ alocação do Oi RPCSS foi \_ \_ usada</span><span class="sxs-lookup"><span data-stu-id="a0153-141">Oi\_RPCSS\_ALLOC\_USED</span></span>       | <span data-ttu-id="a0153-142">Usa o pacote de memória do RpcSs.</span><span class="sxs-lookup"><span data-stu-id="a0153-142">Uses the RpcSs memory package.</span></span>           |
| <span data-ttu-id="a0153-143">04</span><span class="sxs-lookup"><span data-stu-id="a0153-143">04</span></span>  | <span data-ttu-id="a0153-144">\_Proc de objeto Oi \_</span><span class="sxs-lookup"><span data-stu-id="a0153-144">Oi\_OBJECT\_PROC</span></span>             | <span data-ttu-id="a0153-145">Um procedimento em uma interface de objeto.</span><span class="sxs-lookup"><span data-stu-id="a0153-145">A procedure in an object interface.</span></span>      |
| <span data-ttu-id="a0153-146">08</span><span class="sxs-lookup"><span data-stu-id="a0153-146">08</span></span>  | <span data-ttu-id="a0153-147">Oi \_ tem \_ RPCFLAGS</span><span class="sxs-lookup"><span data-stu-id="a0153-147">Oi\_HAS\_RPCFLAGS</span></span>            | <span data-ttu-id="a0153-148">O procedimento tem sinalizadores de RPC diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="a0153-148">The procedure has nonzero Rpc flags.</span></span>     |
| <span data-ttu-id="a0153-149">10</span><span class="sxs-lookup"><span data-stu-id="a0153-149">10</span></span>  | <span data-ttu-id="a0153-150">Oi\_\*</span><span class="sxs-lookup"><span data-stu-id="a0153-150">Oi\_\*</span></span>                       | <span data-ttu-id="a0153-151">Sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="a0153-151">Overloaded.</span></span>                              |
| <span data-ttu-id="a0153-152">20</span><span class="sxs-lookup"><span data-stu-id="a0153-152">20</span></span>  | <span data-ttu-id="a0153-153">Oi\_\*</span><span class="sxs-lookup"><span data-stu-id="a0153-153">Oi\_\*</span></span>                       | <span data-ttu-id="a0153-154">Sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="a0153-154">Overloaded.</span></span>                              |
| <span data-ttu-id="a0153-155">40</span><span class="sxs-lookup"><span data-stu-id="a0153-155">40</span></span>  | <span data-ttu-id="a0153-156">Oi \_ usar \_ novas \_ \_ rotinas de inicialização</span><span class="sxs-lookup"><span data-stu-id="a0153-156">Oi\_USE\_NEW\_INIT\_ROUTINES</span></span> | <span data-ttu-id="a0153-157">Usa rotinas do Windows NT 3.5 beta2 + init.</span><span class="sxs-lookup"><span data-stu-id="a0153-157">Uses Windows NT3.5 Beta2+ init routines.</span></span> |
| <span data-ttu-id="a0153-158">80</span><span class="sxs-lookup"><span data-stu-id="a0153-158">80</span></span>  |                              | <span data-ttu-id="a0153-159">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="a0153-159">Unused.</span></span>                                  |



 

<span data-ttu-id="a0153-160">Os sinalizadores a seguir estão sobrecarregados.</span><span class="sxs-lookup"><span data-stu-id="a0153-160">The following flags are overloaded.</span></span>



| <span data-ttu-id="a0153-161">Hex</span><span class="sxs-lookup"><span data-stu-id="a0153-161">Hex</span></span> | <span data-ttu-id="a0153-162">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="a0153-162">Flag</span></span>                                    | <span data-ttu-id="a0153-163">Significado</span><span class="sxs-lookup"><span data-stu-id="a0153-163">Meaning</span></span>                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="a0153-164">10</span><span class="sxs-lookup"><span data-stu-id="a0153-164">10</span></span>  | <span data-ttu-id="a0153-165">a codificação \_ é \_ usada</span><span class="sxs-lookup"><span data-stu-id="a0153-165">ENCODE\_IS\_USED</span></span>                        | <span data-ttu-id="a0153-166">Usado apenas na escolha.</span><span class="sxs-lookup"><span data-stu-id="a0153-166">Used only in pickling.</span></span>                              |
| <span data-ttu-id="a0153-167">20</span><span class="sxs-lookup"><span data-stu-id="a0153-167">20</span></span>  | <span data-ttu-id="a0153-168">a decodificação \_ é \_ usada</span><span class="sxs-lookup"><span data-stu-id="a0153-168">DECODE\_IS\_USED</span></span>                        | <span data-ttu-id="a0153-169">Usado apenas na escolha.</span><span class="sxs-lookup"><span data-stu-id="a0153-169">Used only in pickling.</span></span>                              |
| <span data-ttu-id="a0153-170">10</span><span class="sxs-lookup"><span data-stu-id="a0153-170">10</span></span>  | <span data-ttu-id="a0153-171">Oi \_ ignorar \_ \_ manipulação de exceção de objeto \_</span><span class="sxs-lookup"><span data-stu-id="a0153-171">Oi\_IGNORE\_OBJECT\_EXCEPTION\_HANDLING</span></span> | <span data-ttu-id="a0153-172">Não é mais usado (OLE antigo).</span><span class="sxs-lookup"><span data-stu-id="a0153-172">Not used anymore (old OLE).</span></span>                         |
| <span data-ttu-id="a0153-173">20</span><span class="sxs-lookup"><span data-stu-id="a0153-173">20</span></span>  | <span data-ttu-id="a0153-174">Oi \_ tem \_ comunicação \_ ou \_ falha</span><span class="sxs-lookup"><span data-stu-id="a0153-174">Oi\_HAS\_COMM\_OR\_FAULT</span></span>                | <span data-ttu-id="a0153-175">Em somente RPC bruto, \[ comunicação \_ , status de falha \_ \] .</span><span class="sxs-lookup"><span data-stu-id="a0153-175">In raw RPC only, \[comm \_, fault\_status\].</span></span>        |
| <span data-ttu-id="a0153-176">20</span><span class="sxs-lookup"><span data-stu-id="a0153-176">20</span></span>  | <span data-ttu-id="a0153-177">O \_ \_ \_ \_ interpretador de uso de Oi obj v2</span><span class="sxs-lookup"><span data-stu-id="a0153-177">Oi\_OBJ\_USE\_V2\_INTERPRETER</span></span>           | <span data-ttu-id="a0153-178">Somente no DCOM, use o interpretador [**– OIF**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="a0153-178">In DCOM only, use [**–Oif**](/windows/desktop/Midl/-oi) interpreter.</span></span> |



 

<span data-ttu-id="a0153-179">O \_ campo sinalizadores de rpc<4> descreve como definir o campo **RpcFlags** da estrutura [**de \_ mensagens RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) .</span><span class="sxs-lookup"><span data-stu-id="a0153-179">The rpc\_flags<4> field describes how to set the **RpcFlags** field of the [**RPC\_MESSAGE**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) structure.</span></span> <span data-ttu-id="a0153-180">Este campo só estará presente se os \_ sinalizadores oi<1> campo tiver Oi \_ \_ RPCFLAGS definido.</span><span class="sxs-lookup"><span data-stu-id="a0153-180">This field is only present if the Oi\_flags<1> field has Oi\_HAD\_RPCFLAGS set.</span></span> <span data-ttu-id="a0153-181">Se esse campo não estiver presente, os sinalizadores de RPC para o procedimento remoto serão zero.</span><span class="sxs-lookup"><span data-stu-id="a0153-181">If this field is not present, then the RPC flags for the remote procedure are zero.</span></span>

> [!Note]  
> <span data-ttu-id="a0153-182">Para o desempenho, os interpretadores assíncronos sempre têm os sinalizadores de RPC \_<4> campo presente.</span><span class="sxs-lookup"><span data-stu-id="a0153-182">For performance, the async interpreters always have the rpc\_flags<4> field present.</span></span>

 

<span data-ttu-id="a0153-183">O \_ campo proc num<2> fornece o número do procedimento do procedimento.</span><span class="sxs-lookup"><span data-stu-id="a0153-183">The proc\_num<2> field provides the procedure's procedure number.</span></span>

<span data-ttu-id="a0153-184">O tamanho da pilha \_<2> fornece o tamanho total de todos os parâmetros na pilha, incluindo qualquer ponteiro e/ou valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a0153-184">The stack\_size<2> provides the total size of all parameters on the stack, including any this pointer and/or return value.</span></span>

<span data-ttu-id="a0153-185">A descrição explícita do \_ identificador \_<> campo é descrita mais adiante neste documento.</span><span class="sxs-lookup"><span data-stu-id="a0153-185">The explicit\_handle\_description<> field is described later in this document.</span></span> <span data-ttu-id="a0153-186">Esse campo não estará presente se o procedimento usar um identificador implícito.</span><span class="sxs-lookup"><span data-stu-id="a0153-186">This field is not present if the procedure uses an implicit handle.</span></span>

 

 