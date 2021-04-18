---
title: atributo out
description: O atributo \ out \ identifica os parâmetros de ponteiro que são retornados do procedimento chamado para o procedimento de chamada (do servidor para o cliente).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- MIDL do atributo out
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105780531"
---
# <a name="out-attribute"></a><span data-ttu-id="a1e84-104">atributo out</span><span class="sxs-lookup"><span data-stu-id="a1e84-104">out attribute</span></span>

<span data-ttu-id="a1e84-105">O \[  \] atributo out identifica os parâmetros de ponteiro que são retornados do procedimento chamado para o procedimento de chamada (do servidor para o cliente).</span><span class="sxs-lookup"><span data-stu-id="a1e84-105">The \[**out**\] attribute identifies pointer parameters that are returned from the called procedure to the calling procedure (from the server to the client).</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a><span data-ttu-id="a1e84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1e84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e84-107">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="a1e84-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e84-108">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="a1e84-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="a1e84-109">Os atributos de função válidos são \[ [**retorno de chamada**](callback.md) \] , \[ [**local**](local.md) \] ; o atributo de ponteiro \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] ou \[ [**PTR**](ptr.md) \] ; e a cadeia de caracteres de atributos de uso \[ [](string.md) \] , \[ [**ignorar**](ignore.md) \] e \[ [**\_ identificador de contexto**](context-handle.md) \] .</span><span class="sxs-lookup"><span data-stu-id="a1e84-109">Valid function attributes are \[[**callback**](callback.md)\], \[[**local**](local.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**string**](string.md)\], \[[**ignore**](ignore.md)\], and \[[**context\_handle**](context-handle.md)\].</span></span>

</dd> <dt>

<span data-ttu-id="a1e84-110">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="a1e84-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e84-111">Especifica um tipo de [base \_](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="a1e84-111">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="a1e84-112">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="a1e84-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="a1e84-113">*Declarador de ponteiro*</span><span class="sxs-lookup"><span data-stu-id="a1e84-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e84-114">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="a1e84-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="a1e84-115">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="a1e84-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1e84-116">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="a1e84-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e84-117">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a1e84-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a1e84-118">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="a1e84-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e84-119">Especifica zero ou mais atributos apropriados para um tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="a1e84-119">Specifies zero or more attributes appropriate for a specified parameter type.</span></span> <span data-ttu-id="a1e84-120">Atributos de parâmetro com o \[ atributo **out** \] também podem pegar o atributo direcional \[ **out** \] ; os atributos Field \[ [**First \_ são**](first-is.md) \] , \[ [**Last \_ is**](last-is.md) \] , \[ [**length \_ is**](length-is.md) \] , \[ [**Max \_ is**](max-is.md) \] , \[ [**Size \_ is**](size-is.md) \] e \[ [**switch \_ Type**](switch-type.md) \] ; o atributo ponteiro \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] ou \[ [**PTR**](ptr.md) \] ; e o \[ [**\_ identificador de contexto**](context-handle.md) e a cadeia de \] \[ [**caracteres**](string.md) \] de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="a1e84-120">Parameter attributes with the \[**out**\] attribute can also take the directional attribute \[**out**\]; the field attributes \[[**first\_is**](first-is.md)\], \[[**last\_is**](last-is.md)\], \[[**length\_is**](length-is.md)\], \[[**max\_is**](max-is.md)\], \[[**size\_is**](size-is.md)\], and \[[**switch\_type**](switch-type.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**context\_handle**](context-handle.md)\] and \[[**string**](string.md)\].</span></span> <span data-ttu-id="a1e84-121">O atributo de uso \[ [**ignore**](ignore.md) \] não pode ser usado como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1e84-121">The usage attribute \[[**ignore**](ignore.md)\] cannot be used as a parameter attribute.</span></span> <span data-ttu-id="a1e84-122">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a1e84-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a1e84-123">*Declarador*</span><span class="sxs-lookup"><span data-stu-id="a1e84-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e84-124">Especifica os declaradores padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="a1e84-124">Specifies the standard declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="a1e84-125">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="a1e84-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="a1e84-126">O Declarador de parâmetro no Declarador de função, como o nome do parâmetro, é opcional.</span><span class="sxs-lookup"><span data-stu-id="a1e84-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1e84-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1e84-127">Remarks</span></span>

<span data-ttu-id="a1e84-128">O \[  \] atributo out indica que um parâmetro que atua como um ponteiro e seus dados associados na memória são passados de volta do procedimento chamado para o procedimento de chamada.</span><span class="sxs-lookup"><span data-stu-id="a1e84-128">The \[**out**\] attribute indicates that a parameter that acts as a pointer and its associated data in memory are to be passed back from the called procedure to the calling procedure.</span></span>

<span data-ttu-id="a1e84-129">O \[ atributo **out** \] deve ser um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="a1e84-129">The \[**out**\] attribute must be a pointer.</span></span> <span data-ttu-id="a1e84-130">Os compiladores de IDL do DCE exigem a presença de um \* Declarador de ponteiro explícito na declaração de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1e84-130">DCE IDL compilers require the presence of an explicit \* as a pointer declarator in the parameter declaration.</span></span> <span data-ttu-id="a1e84-131">O Microsoft IDL oferece uma extensão que descarta esse requisito e permite uma matriz ou um tipo de ponteiro definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a1e84-131">Microsoft IDL offers an extension that drops this requirement and allows an array or a previously defined pointer type.</span></span>

<span data-ttu-id="a1e84-132">Um atributo relacionado, \[ [**no**](in.md) \] , indica que o parâmetro é passado do procedimento de chamada para o procedimento chamado.</span><span class="sxs-lookup"><span data-stu-id="a1e84-132">A related attribute, \[[**in**](in.md)\], indicates that the parameter is passed from the calling procedure to the called procedure.</span></span> <span data-ttu-id="a1e84-133">Os \[  \] atributos in e \[ **out** \] especificam a direção na qual os parâmetros são passados.</span><span class="sxs-lookup"><span data-stu-id="a1e84-133">The \[**in**\] and \[**out**\] attributes specify the direction in which the parameters are passed.</span></span> <span data-ttu-id="a1e84-134">Um parâmetro pode ser definido como \[ somente **entrada**, \] \[ somente **out** \] ou \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="a1e84-134">A parameter can be defined as \[**in**\]-only, \[**out**\]-only, or \[**in**, **out**\].</span></span>

<span data-ttu-id="a1e84-135">Um \[  \] parâmetro out-only é considerado indefinido quando o procedimento remoto é chamado e a memória do objeto é alocada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="a1e84-135">An \[**out**\]-only parameter is assumed to be undefined when the remote procedure is called and memory for the object is allocated by the server.</span></span> <span data-ttu-id="a1e84-136">Como os parâmetros/ponteiros de nível superior sempre devem apontar para um armazenamento válido e, portanto, não podem ser **nulos**, \[  \] não podem ser aplicados a ponteiros de nível superior \[ [](unique.md) \] ou \[ [**PTR**](ptr.md) \] .</span><span class="sxs-lookup"><span data-stu-id="a1e84-136">Since top-level pointer/parameters must always point to valid storage, and therefore cannot be **NULL**, \[**out**\] cannot be applied to top-level \[[**unique**](unique.md)\] or \[[**ptr**](ptr.md)\] pointers.</span></span> <span data-ttu-id="a1e84-137">Parâmetros que são \[  \] ponteiros exclusivos ou \[ **PTR** \] devem estar \[ [**no**](in.md) \] ou \[ **nos** parâmetros de **saída** \] .</span><span class="sxs-lookup"><span data-stu-id="a1e84-137">Parameters that are \[**unique**\] or \[**ptr**\] pointers must be either \[[**in**](in.md)\] or \[**in**, **out**\] parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="a1e84-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1e84-138">Examples</span></span>

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a><span data-ttu-id="a1e84-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1e84-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e84-140">**Storage**</span><span class="sxs-lookup"><span data-stu-id="a1e84-140">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="a1e84-141">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="a1e84-141">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a1e84-142">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="a1e84-142">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="a1e84-143">**const**</span><span class="sxs-lookup"><span data-stu-id="a1e84-143">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="a1e84-144">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="a1e84-144">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a1e84-145">**enumera**</span><span class="sxs-lookup"><span data-stu-id="a1e84-145">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="a1e84-146">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="a1e84-146">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="a1e84-147">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="a1e84-147">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="a1e84-148">**no**</span><span class="sxs-lookup"><span data-stu-id="a1e84-148">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="a1e84-149">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="a1e84-149">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="a1e84-150">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="a1e84-150">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="a1e84-151">**local**</span><span class="sxs-lookup"><span data-stu-id="a1e84-151">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="a1e84-152">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="a1e84-152">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="a1e84-153">**ptr**</span><span class="sxs-lookup"><span data-stu-id="a1e84-153">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="a1e84-154">**ref**</span><span class="sxs-lookup"><span data-stu-id="a1e84-154">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="a1e84-155">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="a1e84-155">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="a1e84-156">**string**</span><span class="sxs-lookup"><span data-stu-id="a1e84-156">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="a1e84-157">**struct**</span><span class="sxs-lookup"><span data-stu-id="a1e84-157">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="a1e84-158">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="a1e84-158">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="a1e84-159">**unida**</span><span class="sxs-lookup"><span data-stu-id="a1e84-159">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="a1e84-160">**diferente**</span><span class="sxs-lookup"><span data-stu-id="a1e84-160">**unique**</span></span>](unique.md)
</dt> </dl>

 

 