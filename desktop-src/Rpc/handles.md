---
title: Alças
description: Até duas partes na descrição da cadeia de caracteres de formato de identificadores de endereço de procedimento.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294370"
---
# <a name="handles"></a><span data-ttu-id="da191-103">Alças</span><span class="sxs-lookup"><span data-stu-id="da191-103">Handles</span></span>

<span data-ttu-id="da191-104">Até duas partes na descrição da cadeia de caracteres de formato de identificadores de endereço de procedimento.</span><span class="sxs-lookup"><span data-stu-id="da191-104">As many as two parts in the format string description of a procedure address handles.</span></span> <span data-ttu-id="da191-105">A primeira parte é o tipo de identificador \_<1> campo da descrição de um procedimento, usado para indicar identificadores implícitos.</span><span class="sxs-lookup"><span data-stu-id="da191-105">The first part is the handle\_type<1> field of a procedure's description, used to indicate implicit handles.</span></span> <span data-ttu-id="da191-106">Esta parte está sempre presente.</span><span class="sxs-lookup"><span data-stu-id="da191-106">This part is always present.</span></span> <span data-ttu-id="da191-107">A segunda parte é uma descrição de parâmetro de qualquer identificador explícito no procedimento.</span><span class="sxs-lookup"><span data-stu-id="da191-107">The second part is a parameter description of any explicit handle in the procedure.</span></span> <span data-ttu-id="da191-108">Ambos são explicados nas seções a seguir, juntamente com uma discussão sobre o suporte adicional do compilador MIDL da estrutura do descritor de stub para problemas de identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="da191-108">Both are explained in the following sections, along with a discussion of the additional MIDL compiler support of the Stub Descriptor structure for binding handle issues.</span></span>

## <a name="implicit-handles"></a><span data-ttu-id="da191-109">Identificadores implícitos</span><span class="sxs-lookup"><span data-stu-id="da191-109">Implicit Handles</span></span>

<span data-ttu-id="da191-110">Se um procedimento usar um identificador implícito para associação, o tipo de identificador \_<1> campo da descrição do procedimento conterá um dos três valores válidos de zero.</span><span class="sxs-lookup"><span data-stu-id="da191-110">If a procedure uses an implicit handle for binding, the handle\_type<1> field of the procedure's description contains one of three valid nonzero values.</span></span> <span data-ttu-id="da191-111">O suporte do compilador MIDL para identificadores implícitos é encontrado no \_ \_ campo informações do identificador implícito da estrutura do descritor de stub:</span><span class="sxs-lookup"><span data-stu-id="da191-111">MIDL compiler support for implicit handles is found in the IMPLICIT\_HANDLE\_INFO field of the Stub Descriptor structure:</span></span>

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

<span data-ttu-id="da191-112">Se o procedimento usar um identificador automático, o membro **pAutoHandle** conterá o endereço do stub definido – variável de identificador auto.</span><span class="sxs-lookup"><span data-stu-id="da191-112">If the procedure uses an auto handle, the **pAutoHandle** member contains the address of the stub defined–auto handle variable.</span></span>

<span data-ttu-id="da191-113">Se o procedimento usar um identificador primitivo implícito, o membro **pPrimitiveHandle** conterá o endereço do stub definido – variável de identificador primitivo.</span><span class="sxs-lookup"><span data-stu-id="da191-113">If the procedure uses an implicit primitive handle, the **pPrimitiveHandle** member contains the address of the stub defined–primitive handle variable.</span></span>

<span data-ttu-id="da191-114">Por fim, se o procedimento usar um identificador genérico implícito, o membro **pGenericBindingInfo** manterá o endereço do ponteiro para a estrutura de **\_ \_ informações de associação genérica** correspondente.</span><span class="sxs-lookup"><span data-stu-id="da191-114">Finally, if the procedure uses an implicit generic handle, the **pGenericBindingInfo** member holds the address of the pointer to the corresponding **GENERIC\_BINDING\_INFO** structure.</span></span> <span data-ttu-id="da191-115">A estrutura de dados do **stub de MIDL \_ \_** contém um ponteiro para uma coleção de estruturas de **\_ \_ par de ligação genérica** .</span><span class="sxs-lookup"><span data-stu-id="da191-115">The data structure **MIDL\_STUB\_DESC** contains a pointer to a collection of **GENERIC\_BINDING\_PAIR** structures.</span></span> <span data-ttu-id="da191-116">A entrada na posição zero dessa coleção é reservada para as rotinas **de associação e** **desvinculação** correspondentes ao identificador de associação genérico referenciado por **PGenericBindingInfo** nas **\_ \_ informações do identificador implícito**.</span><span class="sxs-lookup"><span data-stu-id="da191-116">The entry in the zero position of this collection is reserved for the **bind** and **unbind** routines corresponding to the generic binding handle referenced by **pGenericBindingInfo** in **IMPLICIT\_HANDLE\_INFO**.</span></span> <span data-ttu-id="da191-117">O tipo de identificador de ligação implícita é indicado na cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="da191-117">The type of implicit binding handle is indicated in the format string.</span></span>

## <a name="explicit-handles"></a><span data-ttu-id="da191-118">Identificadores explícitos</span><span class="sxs-lookup"><span data-stu-id="da191-118">Explicit Handles</span></span>

<span data-ttu-id="da191-119">Há três tipos de identificador explícitos possíveis: contexto, genérico e primitivo.</span><span class="sxs-lookup"><span data-stu-id="da191-119">There are three possible explicit handle types: context, generic, and primitive.</span></span> <span data-ttu-id="da191-120">No caso de um identificador explícito (ou um \[  \] identificador de contexto somente out, que é manipulado da mesma maneira), as informações do identificador de associação são exibidas como um dos parâmetros do procedimento.</span><span class="sxs-lookup"><span data-stu-id="da191-120">In the case of an explicit handle (or an \[**out**\] only context handle, which is handled in the same way), the binding handle information appears as one of the procedure's parameters.</span></span> <span data-ttu-id="da191-121">As três descrições possíveis são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="da191-121">The three possible descriptions are as follows.</span></span>

<span data-ttu-id="da191-122">Primitiva</span><span class="sxs-lookup"><span data-stu-id="da191-122">Primitive</span></span>

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

<span data-ttu-id="da191-123">O sinalizador<1> indica se o identificador é passado por um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="da191-123">The flag<1> indicates whether the handle is passed by a pointer.</span></span>

<span data-ttu-id="da191-124">O deslocamento<2> fornece o deslocamento desde o início da pilha até o identificador primitivo.</span><span class="sxs-lookup"><span data-stu-id="da191-124">The offset<2> provides the offset from the beginning of the stack to the primitive handle.</span></span>

> [!Note]  
> <span data-ttu-id="da191-125">Uma descrição do identificador primitivo na cadeia de caracteres de formato de tipo é reduzida para uma única \_ ignorar FC.</span><span class="sxs-lookup"><span data-stu-id="da191-125">A primitive handle description in the type format string is reduced to a single FC\_IGNORE.</span></span>

 

<span data-ttu-id="da191-126">Genérico</span><span class="sxs-lookup"><span data-stu-id="da191-126">Generic</span></span>

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

<span data-ttu-id="da191-127">O sinalizador \_ e \_ o tamanho<1> tem o sinal superior Nibble e o tamanho inferior Nibble.</span><span class="sxs-lookup"><span data-stu-id="da191-127">The flag\_and \_size<1> has the upper flag nibble and the lower size nibble.</span></span> <span data-ttu-id="da191-128">O sinalizador indica se o identificador é passado por um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="da191-128">The flag indicates whether the handle is passed by a pointer.</span></span> <span data-ttu-id="da191-129">O campo tamanho fornece o tamanho do tipo de identificador genérico definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="da191-129">The size field provides the size of the user defined–generic handle type.</span></span> <span data-ttu-id="da191-130">Esse tamanho é limitado a 1, 2 ou 4 bytes em sistemas de 32 bits e 1, 2, 4 ou 8 bytes em sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="da191-130">This size is limited to be 1, 2 or 4 bytes on 32-bit systems and 1, 2, 4 or 8 bytes on 64-bit systems.</span></span>

<span data-ttu-id="da191-131">O campo deslocamento<2> fornece o deslocamento do início da pilha do ponteiro até os dados do tamanho fornecido.</span><span class="sxs-lookup"><span data-stu-id="da191-131">The offset<2> field provides the offset from the beginning of the stack of the pointer to the data of the size given.</span></span>

<span data-ttu-id="da191-132">O índice de par de rotina de associação \_ \_ \_<campo 1> fornece ao índice o campo aGenericBindingRoutinePairs do descritor de stub para os ponteiros de função de rotina de **Associação** e **desassociação** para o identificador genérico.</span><span class="sxs-lookup"><span data-stu-id="da191-132">The binding\_routine\_pair\_index<1> field gives the index into the aGenericBindingRoutinePairs field of the Stub Descriptor to the **bind** and **unbind** routine function pointers for the generic handle.</span></span>

> [!Note]  
> <span data-ttu-id="da191-133">Uma descrição de identificador genérico no formato de tipo é a descrição somente do tipo de dados relacionado.</span><span class="sxs-lookup"><span data-stu-id="da191-133">A generic handle description in the type format is the description of the related data type only.</span></span>

 

<span data-ttu-id="da191-134">Contexto</span><span class="sxs-lookup"><span data-stu-id="da191-134">Context</span></span>

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

<span data-ttu-id="da191-135">Os sinalizadores<1> indicam como o identificador é passado e qual é o tipo.</span><span class="sxs-lookup"><span data-stu-id="da191-135">The flags<1> indicate how the handle is passed and what type it is.</span></span> <span data-ttu-id="da191-136">Os sinalizadores válidos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="da191-136">Valid flags are shown in the following table.</span></span>



| <span data-ttu-id="da191-137">Hex</span><span class="sxs-lookup"><span data-stu-id="da191-137">Hex</span></span> | <span data-ttu-id="da191-138">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="da191-138">Flag</span></span>                                   |
|-----|----------------------------------------|
| <span data-ttu-id="da191-139">80</span><span class="sxs-lookup"><span data-stu-id="da191-139">80</span></span>  | <span data-ttu-id="da191-140">o identificador de \_ parâmetro \_ é \_ via \_ PTR</span><span class="sxs-lookup"><span data-stu-id="da191-140">HANDLE\_PARAM\_IS\_VIA\_PTR</span></span>            |
| <span data-ttu-id="da191-141">40</span><span class="sxs-lookup"><span data-stu-id="da191-141">40</span></span>  | <span data-ttu-id="da191-142">o \_ parâmetro Handle \_ está \_ em</span><span class="sxs-lookup"><span data-stu-id="da191-142">HANDLE\_PARAM\_IS\_IN</span></span>                  |
| <span data-ttu-id="da191-143">20</span><span class="sxs-lookup"><span data-stu-id="da191-143">20</span></span>  | <span data-ttu-id="da191-144">o \_ parâmetro Handle \_ está \_ fora</span><span class="sxs-lookup"><span data-stu-id="da191-144">HANDLE\_PARAM\_IS\_OUT</span></span>                 |
| <span data-ttu-id="da191-145">21</span><span class="sxs-lookup"><span data-stu-id="da191-145">21</span></span>  | <span data-ttu-id="da191-146">o \_ parâmetro Handle \_ é \_ retornado</span><span class="sxs-lookup"><span data-stu-id="da191-146">HANDLE\_PARAM\_IS\_RETURN</span></span>              |
| <span data-ttu-id="da191-147">08</span><span class="sxs-lookup"><span data-stu-id="da191-147">08</span></span>  | <span data-ttu-id="da191-148">\_identificador de \_ contexto \_ estrito NDR</span><span class="sxs-lookup"><span data-stu-id="da191-148">NDR\_STRICT\_CONTEXT\_HANDLE</span></span>           |
| <span data-ttu-id="da191-149">04</span><span class="sxs-lookup"><span data-stu-id="da191-149">04</span></span>  | <span data-ttu-id="da191-150">\_manipulador de contexto NDR \_ \_ sem \_ serialização</span><span class="sxs-lookup"><span data-stu-id="da191-150">NDR\_CONTEXT\_HANDLE\_NO\_SERIALIZE</span></span>    |
| <span data-ttu-id="da191-151">02</span><span class="sxs-lookup"><span data-stu-id="da191-151">02</span></span>  | <span data-ttu-id="da191-152">\_serialização de \_ identificador de contexto NDR \_</span><span class="sxs-lookup"><span data-stu-id="da191-152">NDR\_CONTEXT\_HANDLE\_SERIALIZE</span></span>        |
| <span data-ttu-id="da191-153">01</span><span class="sxs-lookup"><span data-stu-id="da191-153">01</span></span>  | <span data-ttu-id="da191-154">o \_ identificador de contexto NDR \_ \_ não pode \_ ser \_ nulo</span><span class="sxs-lookup"><span data-stu-id="da191-154">NDR\_CONTEXT\_HANDLE\_CANNOT\_BE\_NULL</span></span> |



 

<span data-ttu-id="da191-155">Os quatro primeiros sinalizadores sempre estão presentes, os últimos quatro foram adicionados ao Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="da191-155">The first four flags have always been present, the last four were added in Windows 2000.</span></span>

<span data-ttu-id="da191-156">O campo deslocamento<2> fornece o deslocamento desde o início da pilha até o identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="da191-156">The offset<2> field provides the offset from the start of the stack to the context handle.</span></span>

<span data-ttu-id="da191-157">O índice de rotina de encerramento de contexto \_ \_ \_<1> fornece um índice para o campo **apfnNdrRundownRoutines** do descritor de stub para a rotina de encerramento usada para esse identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="da191-157">The context\_rundown\_routine\_index<1> provides an index into the **apfnNdrRundownRoutines** field of the Stub Descriptor to the rundown routine used for this context handle.</span></span> <span data-ttu-id="da191-158">O compilador sempre gera um índice.</span><span class="sxs-lookup"><span data-stu-id="da191-158">The compiler always generates an index.</span></span> <span data-ttu-id="da191-159">Para rotinas que não têm uma rotina de encerramento, esse é um índice para uma posição de tabela que contém NULL.</span><span class="sxs-lookup"><span data-stu-id="da191-159">For routines that do not have a rundown routine, this is an index to a table position that holds null.</span></span>

<span data-ttu-id="da191-160">Para stubs internos **– Oi2**, o param \_ num<1> fornece a contagem ordinal, começando em zero, especificando qual identificador de contexto está no procedimento fornecido.</span><span class="sxs-lookup"><span data-stu-id="da191-160">For stubs built in **–Oi2**, the param\_num<1> provides the ordinal count, starting at zero, specifying which context handle it is in the given procedure.</span></span>

<span data-ttu-id="da191-161">Para versões anteriores do interpretador, o param \_ num<1> fornece o número do parâmetro do identificador de contexto, começando em zero, em seu procedimento.</span><span class="sxs-lookup"><span data-stu-id="da191-161">For previous versions of the interpreter, the param\_num<1> provides the context handle's parameter number, starting at zero, in its procedure.</span></span>

> [!Note]  
> <span data-ttu-id="da191-162">Uma descrição de identificador de contexto na cadeia de caracteres de formato de tipo não terá o deslocamento<2> na descrição.</span><span class="sxs-lookup"><span data-stu-id="da191-162">A context handle description in the type format string will not have the offset<2> in the description.</span></span>

 

## <a name="the-new-oif-header"></a><span data-ttu-id="da191-163">O cabeçalho New – OIF</span><span class="sxs-lookup"><span data-stu-id="da191-163">The New –Oif Header</span></span>

<span data-ttu-id="da191-164">Conforme mencionado anteriormente, o cabeçalho [**– OIF**](/windows/desktop/Midl/-oi) se expande no cabeçalho **– Oi** .</span><span class="sxs-lookup"><span data-stu-id="da191-164">As mentioned previously, the [**–Oif**](/windows/desktop/Midl/-oi) header expands on the **–Oi** header.</span></span> <span data-ttu-id="da191-165">Para sua conveniência, todos os campos são mostrados aqui:</span><span class="sxs-lookup"><span data-stu-id="da191-165">For convenience, all fields are shown here:</span></span>

<span data-ttu-id="da191-166">(O cabeçalho antigo)</span><span class="sxs-lookup"><span data-stu-id="da191-166">(The old header)</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="da191-167">(As extensões [**– OIF**](/windows/desktop/Midl/-oi) )</span><span class="sxs-lookup"><span data-stu-id="da191-167">(The [**–Oif**](/windows/desktop/Midl/-oi) extensions)</span></span>

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

<span data-ttu-id="da191-168">O \_ \_ tamanho de buffer de cliente constante \_<2> fornece o tamanho do buffer de marshaling que poderia ter sido previamente computado pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="da191-168">The constant\_client\_buffer\_size<2> provides the size of the marshaling buffer that could have been pre-computed by the compiler.</span></span> <span data-ttu-id="da191-169">Isso pode ser apenas um tamanho parcial, pois o sinalizador ClientMustSize aciona o dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="da191-169">This may be only a partial size, as the ClientMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="da191-170">O \_ tamanho do buffer do servidor constante \_ \_<2> fornece o tamanho do buffer de marshaling como pré-compilado pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="da191-170">The constant\_server\_buffer\_size<2> provides the size of the marshaling buffer as precomputed by the compiler.</span></span> <span data-ttu-id="da191-171">Isso pode ser apenas um tamanho parcial, pois o sinalizador ServerMustSize aciona o dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="da191-171">This may be only a partial size, as the ServerMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="da191-172">Os sinalizadores de \_ consentimento do intérprete \_ são definidos em Ndrtypes. h:</span><span class="sxs-lookup"><span data-stu-id="da191-172">The INTERPRETER\_OPT\_FLAGS are defined in Ndrtypes.h:</span></span>

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   <span data-ttu-id="da191-173">O bit ServerMustSize será definido se o servidor precisar executar uma passagem de dimensionamento de buffer.</span><span class="sxs-lookup"><span data-stu-id="da191-173">The ServerMustSize bit is set if the server needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="da191-174">O bit ClientMustSize será definido se o cliente precisar executar uma passagem de dimensionamento de buffer.</span><span class="sxs-lookup"><span data-stu-id="da191-174">The ClientMustSize bit is set if the client needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="da191-175">O bit HasReturn será definido se o procedimento tiver um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="da191-175">The HasReturn bit is set if the procedure has a return value.</span></span>
-   <span data-ttu-id="da191-176">O bit HasPipes será definido se o pacote de pipe precisar ser usado para dar suporte a um argumento de pipe.</span><span class="sxs-lookup"><span data-stu-id="da191-176">The HasPipes bit is set if the pipe package needs to be used to support a pipe argument.</span></span>
-   <span data-ttu-id="da191-177">O bit HasAsyncUuid será definido se o procedimento for um procedimento DCOM assíncrono.</span><span class="sxs-lookup"><span data-stu-id="da191-177">The HasAsyncUuid bit is set if the procedure is an asynchronous DCOM procedure.</span></span>
-   <span data-ttu-id="da191-178">O bit HasExtensions indica que o Windows 2000 e extensões posteriores são usados.</span><span class="sxs-lookup"><span data-stu-id="da191-178">The HasExtensions bit indicates that Windows 2000 and later extensions are used.</span></span>
-   <span data-ttu-id="da191-179">O bit HasAsyncHandle indica um procedimento RPC assíncrono.</span><span class="sxs-lookup"><span data-stu-id="da191-179">The HasAsyncHandle bit indicates an asynchronous RPC procedure.</span></span>

<span data-ttu-id="da191-180">O HasAsyncHandle bit foi usado inicialmente para uma implementação de DCOM diferente do suporte assíncrono e, portanto, não pôde ser usado para o suporte assíncrono de estilo atual no DCOM.</span><span class="sxs-lookup"><span data-stu-id="da191-180">The HasAsyncHandle bit has been initially used for a different DCOM implementation of async support, and hence could not be used for the current style async support in DCOM.</span></span> <span data-ttu-id="da191-181">O bit HasAsyncUuid atualmente indica isso.</span><span class="sxs-lookup"><span data-stu-id="da191-181">The HasAsyncUuid bit currently indicates this.</span></span>

 

 