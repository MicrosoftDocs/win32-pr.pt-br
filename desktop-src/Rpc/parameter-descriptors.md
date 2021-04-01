---
title: Descritores de parâmetro
description: Como mencionado anteriormente, existem os descritores de parâmetro de estilo \ 8211; Oi e \ 8211; OIF.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641627"
---
# <a name="parameter-descriptors"></a><span data-ttu-id="7b543-103">Descritores de parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b543-103">Parameter Descriptors</span></span>

<span data-ttu-id="7b543-104">Como mencionado [**anteriormente, existem descritores de parâmetro**](/windows/desktop/Midl/-oi) de estilo **OIF** .</span><span class="sxs-lookup"><span data-stu-id="7b543-104">As mentioned previously, [**–Oi**](/windows/desktop/Midl/-oi) and **–Oif** style parameter descriptors exist.</span></span>

## <a name="the-oi-parameter-descriptors"></a><span data-ttu-id="7b543-105">Os descritores de parâmetro – Oi</span><span class="sxs-lookup"><span data-stu-id="7b543-105">The –Oi Parameter Descriptors</span></span>

<span data-ttu-id="7b543-106">Stubs totalmente interpretados exigem informações adicionais para cada um dos parâmetros em uma chamada RPC.</span><span class="sxs-lookup"><span data-stu-id="7b543-106">Fully interpreted stubs require additional information for each of the parameters in an RPC call.</span></span> <span data-ttu-id="7b543-107">As descrições de parâmetro de um procedimento seguem imediatamente após a descrição do procedimento.</span><span class="sxs-lookup"><span data-stu-id="7b543-107">The parameter descriptions of a procedure follow immediately after the description of the procedure.</span></span>

[<span data-ttu-id="7b543-108">**Simples – Oi**</span><span class="sxs-lookup"><span data-stu-id="7b543-108">**Simple –Oi**</span></span>](/windows/desktop/Midl/-oi)

<span data-ttu-id="7b543-109">**Descritores de parâmetro**</span><span class="sxs-lookup"><span data-stu-id="7b543-109">**Parameter Descriptors**</span></span>

<span data-ttu-id="7b543-110">O formato para a descrição de um \[  \] parâmetro de tipo simples in ou Return é:</span><span class="sxs-lookup"><span data-stu-id="7b543-110">The format for the description of an \[**in**\] or return simple type parameter is:</span></span>

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="7b543-111">–ou–</span><span class="sxs-lookup"><span data-stu-id="7b543-111">–or–</span></span>

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="7b543-112">Em que o \_ tipo simples<1> é o token FC que indica o tipo simples.</span><span class="sxs-lookup"><span data-stu-id="7b543-112">Where simple\_type<1> is the FC token indicating the simple type.</span></span> <span data-ttu-id="7b543-113">Os códigos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7b543-113">The codes are as follows:</span></span>

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

<span data-ttu-id="7b543-114">**Outros – Oi**</span><span class="sxs-lookup"><span data-stu-id="7b543-114">**Other –Oi**</span></span>

<span data-ttu-id="7b543-115">**Descritores de parâmetro**</span><span class="sxs-lookup"><span data-stu-id="7b543-115">**Parameter Descriptors**</span></span>

<span data-ttu-id="7b543-116">O formato da descrição para todos os outros tipos de parâmetro é:</span><span class="sxs-lookup"><span data-stu-id="7b543-116">The format for the description for all other parameter types is:</span></span>

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

<span data-ttu-id="7b543-117">Onde a direção do param \_<1> campo para cada uma dessas descrições deve ser um daqueles mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b543-117">Where the param\_direction<1> field for each of these descriptions must be one of those shown in the following table.</span></span>



| <span data-ttu-id="7b543-118">Hex</span><span class="sxs-lookup"><span data-stu-id="7b543-118">Hex</span></span> | <span data-ttu-id="7b543-119">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="7b543-119">Flag</span></span>                          | <span data-ttu-id="7b543-120">Significado</span><span class="sxs-lookup"><span data-stu-id="7b543-120">Meaning</span></span>                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7b543-121">4d</span><span class="sxs-lookup"><span data-stu-id="7b543-121">4d</span></span>  | <span data-ttu-id="7b543-122">FC \_ no \_ param</span><span class="sxs-lookup"><span data-stu-id="7b543-122">FC\_IN\_PARAM</span></span>                 | <span data-ttu-id="7b543-123">Um parâmetro in.</span><span class="sxs-lookup"><span data-stu-id="7b543-123">An in parameter.</span></span>                                            |
| <span data-ttu-id="7b543-124">50</span><span class="sxs-lookup"><span data-stu-id="7b543-124">50</span></span>  | <span data-ttu-id="7b543-125">\_parâmetro FC em \_ saída \_</span><span class="sxs-lookup"><span data-stu-id="7b543-125">FC\_IN\_OUT\_PARAM</span></span>            | <span data-ttu-id="7b543-126">Um parâmetro in/out.</span><span class="sxs-lookup"><span data-stu-id="7b543-126">An in/out parameter.</span></span>                                        |
| <span data-ttu-id="7b543-127">51</span><span class="sxs-lookup"><span data-stu-id="7b543-127">51</span></span>  | <span data-ttu-id="7b543-128">\_parâmetro de saída do FC \_</span><span class="sxs-lookup"><span data-stu-id="7b543-128">FC\_OUT\_PARAM</span></span>                | <span data-ttu-id="7b543-129">Um parâmetro out.</span><span class="sxs-lookup"><span data-stu-id="7b543-129">An out parameter.</span></span>                                           |
| <span data-ttu-id="7b543-130">52</span><span class="sxs-lookup"><span data-stu-id="7b543-130">52</span></span>  | <span data-ttu-id="7b543-131">\_parâmetro de retorno de FC \_</span><span class="sxs-lookup"><span data-stu-id="7b543-131">FC\_RETURN\_PARAM</span></span>             | <span data-ttu-id="7b543-132">Um valor de retorno de procedimento.</span><span class="sxs-lookup"><span data-stu-id="7b543-132">A procedure return value.</span></span>                                   |
| <span data-ttu-id="7b543-133">4F</span><span class="sxs-lookup"><span data-stu-id="7b543-133">4f</span></span>  | <span data-ttu-id="7b543-134">FC \_ em \_ param \_ sem \_ Free \_ Inst</span><span class="sxs-lookup"><span data-stu-id="7b543-134">FC\_IN\_PARAM\_NO\_FREE\_INST</span></span> | <span data-ttu-id="7b543-135">Um em transmissão/representante como um parâmetro para o qual não foi feita nenhuma liberação.</span><span class="sxs-lookup"><span data-stu-id="7b543-135">An in xmit/rep as a parameter for which no freeing is made.</span></span> |



 

<span data-ttu-id="7b543-136">O tamanho da pilha \_<1> é o tamanho do parâmetro na pilha, expresso como o número de inteiros que o parâmetro ocupa na pilha.</span><span class="sxs-lookup"><span data-stu-id="7b543-136">The stack\_size<1> is the size of the parameter on the stack, expressed as the number of integers the parameter occupies on the stack.</span></span>

> [!Note]  
> <span data-ttu-id="7b543-137">Não há suporte para o modo [**– Oi**](/windows/desktop/Midl/-oi) em plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b543-137">The [**–Oi**](/windows/desktop/Midl/-oi) mode is not supported on 64-bit platforms.</span></span>

 

<span data-ttu-id="7b543-138">O \_ campo deslocamento de tipo<2> é o deslocamento na tabela de cadeia de caracteres de formato de tipo, indicando o descritor de tipo para o argumento.</span><span class="sxs-lookup"><span data-stu-id="7b543-138">The type\_offset<2> field is the offset in the type format string table, indicating the type descriptor for the argument.</span></span>

## <a name="the-oif-parameter-descriptors"></a><span data-ttu-id="7b543-139">Os descritores de parâmetro – OIF</span><span class="sxs-lookup"><span data-stu-id="7b543-139">The –Oif Parameter Descriptors</span></span>

<span data-ttu-id="7b543-140">Há dois formatos possíveis para uma descrição de parâmetro, um para tipos base, outro para todos os outros tipos.</span><span class="sxs-lookup"><span data-stu-id="7b543-140">There are two possible formats for a parameter description, one for base types, another for all other types.</span></span>

<span data-ttu-id="7b543-141">Tipos de base:</span><span class="sxs-lookup"><span data-stu-id="7b543-141">Base types:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

<span data-ttu-id="7b543-142">Outros:</span><span class="sxs-lookup"><span data-stu-id="7b543-142">Other:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

<span data-ttu-id="7b543-143">No deslocamento de pilha \_<2> indica o deslocamento na pilha de argumentos virtuais, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7b543-143">In both stack\_offset<2> indicates the offset on the virtual argument stack, in bytes.</span></span> <span data-ttu-id="7b543-144">Para tipos base, o tipo de argumento é fornecido diretamente pelo caractere de formato correspondente ao tipo.</span><span class="sxs-lookup"><span data-stu-id="7b543-144">For base types, the argument type is given directly by the format character corresponding to the type.</span></span> <span data-ttu-id="7b543-145">Para outros tipos, o \_ campo deslocamento de tipo<2> fornece o deslocamento na tabela de cadeia de caracteres de formato de tipo em que o descritor de tipo para o argumento está localizado.</span><span class="sxs-lookup"><span data-stu-id="7b543-145">For other types, the type\_offset<2> field gives the offset in the type format string table where the type descriptor for the argument is located.</span></span>

<span data-ttu-id="7b543-146">O campo atributo de parâmetro é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7b543-146">The parameter attribute field is defined as follows:</span></span>

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   <span data-ttu-id="7b543-147">O bit **MustSize** será definido somente se o parâmetro precisar ser dimensionado.</span><span class="sxs-lookup"><span data-stu-id="7b543-147">The **MustSize** bit is set only if the parameter must be sized.</span></span>
-   <span data-ttu-id="7b543-148">O bit **MustFree** será definido se o servidor precisar chamar a rotina NdrFree do parâmetro \* .</span><span class="sxs-lookup"><span data-stu-id="7b543-148">The **MustFree** bit is set if the server must call the parameter's NdrFree\* routine.</span></span>
-   <span data-ttu-id="7b543-149">O bit **IsSimpleRef** é definido para um parâmetro que é um ponteiro de referência para qualquer coisa diferente de outro ponteiro, e que não tem atributos Allocate.</span><span class="sxs-lookup"><span data-stu-id="7b543-149">The **IsSimpleRef** bit is set for a parameter that is a reference pointer to anything other than another pointer, and which has no allocate attributes.</span></span> <span data-ttu-id="7b543-150">Para esse tipo, o deslocamento de tipo da descrição do parâmetro \_<> campo, com exceção de um ponteiro de referência para um tipo base, fornece o deslocamento para o tipo do Referent; o ponteiro de referência é simplesmente ignorado.</span><span class="sxs-lookup"><span data-stu-id="7b543-150">For such a type, the parameter description's type\_offset<> field, except for a reference pointer to a base type, provides the offset to the referent's type; the reference pointer is simply skipped.</span></span>
-   <span data-ttu-id="7b543-151">O bit **IsDontCallFreeInst** é definido para determinadas representações \_ como parâmetros cujas rotinas de instância gratuita não devem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="7b543-151">The **IsDontCallFreeInst** bit is set for certain represent\_as parameters whose free instance routines should not be called.</span></span>
-   <span data-ttu-id="7b543-152">Os bits de **ServerAllocSize** são diferentes de zero se o parâmetro estiver \[ **fora** \] , \[ **no** \] ponteiro de \[ **saída ou dentro** dele \] para ponteiro, ou ponteiro para enum16, e será inicializado na pilha do intérprete do servidor, em vez de usar uma chamada para **I \_ RpcAllocate**.</span><span class="sxs-lookup"><span data-stu-id="7b543-152">The **ServerAllocSize** bits are nonzero if the parameter is \[**out**\], \[**in**\], or \[**in,out**\] pointer to pointer, or pointer to enum16, and will be initialized on the server interpreter's stack, rather than using a call to **I\_RpcAllocate**.</span></span> <span data-ttu-id="7b543-153">Se for diferente de zero, esse valor será multiplicado por 8 para obter o número de bytes para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7b543-153">If nonzero, this value is multiplied by 8 to get the number of bytes for the parameter.</span></span> <span data-ttu-id="7b543-154">Observe que isso significa que pelo menos 8 bytes sempre são alocados para um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="7b543-154">Note that doing so means at least 8 bytes are always allocated for a pointer.</span></span>
-   <span data-ttu-id="7b543-155">O bit **Isbasetype** é definido para tipos simples que estão sendo empacotados pelo loop do intérprete principal [**– OIF**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="7b543-155">The **IsBasetype** bit is set for simple types that are being marshaled by the main [**–Oif**](/windows/desktop/Midl/-oi) interpreter loop.</span></span> <span data-ttu-id="7b543-156">Em particular, um tipo simples com um atributo de intervalo não é sinalizado como um tipo base para forçar o marshaling da rotina de intervalo por meio de expedição usando um token de intervalo de FC \_ .</span><span class="sxs-lookup"><span data-stu-id="7b543-156">In particular, a simple type with a range attribute on it is not flagged as a base type in order to force the range routine marshaling through dispatching using an FC\_RANGE token.</span></span>
-   <span data-ttu-id="7b543-157">O bit **IsByValue** é definido para os tipos compostos que estão sendo enviados por valor, mas não é definido para tipos simples, independentemente de o argumento ser um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="7b543-157">The **IsByValue** bit is set for compound types being sent by value, but is not set for simple types, regardless of whether the argument is a pointer.</span></span> <span data-ttu-id="7b543-158">Os tipos compostos para os quais ele está definido são estruturas, uniões, [**Transmit \_ como**](/windows/desktop/Midl/transmit-as), [**representam \_ como**](/windows/desktop/Midl/represent-as), [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) e SafeArray.</span><span class="sxs-lookup"><span data-stu-id="7b543-158">The compound types for which it is set are structures, unions, [**transmit\_as**](/windows/desktop/Midl/transmit-as), [**represent\_as**](/windows/desktop/Midl/represent-as), [**wire\_marshal**](/windows/desktop/Midl/wire-marshal) and SAFEARRAY.</span></span> <span data-ttu-id="7b543-159">Em geral, o bit foi introduzido para o benefício do principal loop do interpretador no interpretador [**– Oicf**](/windows/desktop/Midl/-oi) , para garantir que os argumentos não simples (chamados de argumentos de tipo composto) sejam desreferenciados corretamente.</span><span class="sxs-lookup"><span data-stu-id="7b543-159">In general, the bit was introduced for the benefit of the main interpreter loop in the [**–Oicf**](/windows/desktop/Midl/-oi) interpreter, to ensure the nonsimple arguments (referred to as compound type arguments) are properly dereferenced.</span></span> <span data-ttu-id="7b543-160">Esse bit nunca foi usado em versões anteriores do intérprete.</span><span class="sxs-lookup"><span data-stu-id="7b543-160">This bit was never used in previous versions of the interpreter.</span></span>

 

 