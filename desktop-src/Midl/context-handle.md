---
title: context_handle atributo
description: O atributo \ do manipulador de contexto \_ \ identifica um identificador de associação que mantém o contexto, ou informações de estado, no servidor entre chamadas de procedimento remoto.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle do atributo MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640514"
---
# <a name="context_handle-attribute"></a><span data-ttu-id="65bbe-104">atributo de identificador de contexto \_</span><span class="sxs-lookup"><span data-stu-id="65bbe-104">context\_handle attribute</span></span>

<span data-ttu-id="65bbe-105">O atributo **\[ \_ identificador \] de contexto** identifica um identificador de associação que mantém o contexto, ou informações de estado, no servidor entre chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="65bbe-105">The **\[context\_handle\]** attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span>

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a><span data-ttu-id="65bbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65bbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65bbe-107">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="65bbe-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="65bbe-108">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="65bbe-108">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="65bbe-109">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="65bbe-109">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="65bbe-110">Especifica um tipo de ponteiro ou um identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="65bbe-110">Specifies a pointer type or a type identifier.</span></span> <span data-ttu-id="65bbe-111">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="65bbe-111">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="65bbe-112">*Declarador e Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="65bbe-112">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="65bbe-113">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="65bbe-113">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="65bbe-114">O declarador para um identificador de contexto deve incluir pelo menos um Declarador de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="65bbe-114">The declarator for a context handle must include at least one pointer declarator.</span></span> <span data-ttu-id="65bbe-115">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="65bbe-115">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="65bbe-116">A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="65bbe-116">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="65bbe-117">O identificador de nome de parâmetro no Declarador de função é opcional.</span><span class="sxs-lookup"><span data-stu-id="65bbe-117">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="65bbe-118">*função-attr-lista*</span><span class="sxs-lookup"><span data-stu-id="65bbe-118">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="65bbe-119">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="65bbe-119">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="65bbe-120">Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[ \_ identificador \] de contexto**.</span><span class="sxs-lookup"><span data-stu-id="65bbe-120">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="65bbe-121">*declaração de PTR*</span><span class="sxs-lookup"><span data-stu-id="65bbe-121">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="65bbe-122">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="65bbe-122">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="65bbe-123">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do **\*** designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="65bbe-123">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="65bbe-124">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="65bbe-124">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65bbe-125">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="65bbe-125">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="65bbe-126">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="65bbe-126">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="65bbe-127">Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="65bbe-127">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="65bbe-128">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="65bbe-128">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="65bbe-129">*tipo de identificador de contexto*</span><span class="sxs-lookup"><span data-stu-id="65bbe-129">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="65bbe-130">Especifica o identificador que especifica o tipo de identificador de contexto, conforme definido em uma declaração de [**typedef**](typedef.md) que usa o atributo de **\[ \_ identificador \] de contexto** .</span><span class="sxs-lookup"><span data-stu-id="65bbe-130">Specifies the identifier that specifies the context handle type as defined in a [**typedef**](typedef.md) declaration that takes the **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="65bbe-131">A rotina de encerramento é opcional.</span><span class="sxs-lookup"><span data-stu-id="65bbe-131">The rundown routine is optional.</span></span>

<span data-ttu-id="65bbe-132">**Windows Server ServerÂ 2003 e WINDOWSÂ XP:** Uma única interface pode acomodar identificadores de contexto serializados e não serializados, permitindo que um método em uma interface acesse um identificador de contexto exclusivamente (serializado), enquanto outros métodos acessam esse identificador de contexto no modo compartilhado (não serializado).</span><span class="sxs-lookup"><span data-stu-id="65bbe-132">**Windows ServerÂ 2003 and WindowsÂ XP:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="65bbe-133">Esses recursos de acesso são comparáveis a mecanismos de bloqueio de leitura/gravação; os métodos que usam um identificador de contexto serializado são usuários exclusivos (gravadores), enquanto os métodos que usam um identificador de contexto não serializado são usuários compartilhados (leitores).</span><span class="sxs-lookup"><span data-stu-id="65bbe-133">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="65bbe-134">Os métodos que destruim ou modificam o estado de um identificador de contexto devem ser serializados.</span><span class="sxs-lookup"><span data-stu-id="65bbe-134">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="65bbe-135">Os métodos que não modificam o estado de um identificador de contexto, como os métodos que simplesmente lêem de um identificador de contexto, podem ser não serializados.</span><span class="sxs-lookup"><span data-stu-id="65bbe-135">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="65bbe-136">Observe que os métodos de criação são serializados implicitamente.</span><span class="sxs-lookup"><span data-stu-id="65bbe-136">Note that creation methods are implicitly serialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65bbe-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="65bbe-137">Remarks</span></span>

<span data-ttu-id="65bbe-138">O atributo de **\[ \_ identificador \] de contexto** pode aparecer como um atributo de tipo de [**typedef**](typedef.md) de IDL, como um atributo de tipo de retorno de função ou como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="65bbe-138">The **\[context\_handle\]** attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span> <span data-ttu-id="65bbe-139">Quando você aplica o atributo de **\[ \_ identificador \] de contexto** a uma definição de tipo, você também deve fornecer uma rotina de encerramento de contexto.</span><span class="sxs-lookup"><span data-stu-id="65bbe-139">When you apply the **\[context\_handle\]** attribute to a type definition, you must also provide a context rundown routine.</span></span> <span data-ttu-id="65bbe-140">Consulte [rotina de execução de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="65bbe-140">See [Server Context Run-down Routine](/windows/desktop/Rpc/server-context-run-down-routine) for details.</span></span>

<span data-ttu-id="65bbe-141">Quando você usa o compilador MIDL no modo padrão ([**/MS \_ ext**](-ms-ext.md)), um identificador de contexto pode ser qualquer tipo de ponteiro selecionado pelo usuário, desde que ele esteja em conformidade com os requisitos para identificadores de contexto descritos aqui.</span><span class="sxs-lookup"><span data-stu-id="65bbe-141">When you use the MIDL compiler in default ([**/ms\_ext**](-ms-ext.md)) mode, a context handle can be any pointer type selected by the user, as long as it complies with the requirements for context handles described here.</span></span> <span data-ttu-id="65bbe-142">Os dados associados a esse tipo de identificador de contexto não são transmitidos na rede e só devem ser manipulados pelo aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="65bbe-142">The data associated with such a context handle type is not transmitted on the network and should only be manipulated by the server application.</span></span> <span data-ttu-id="65bbe-143">Os compiladores de IDL do DCE restringem identificadores de contexto a ponteiros do tipo [**void**](void.md) **\*** .</span><span class="sxs-lookup"><span data-stu-id="65bbe-143">DCE IDL compilers restrict context handles to pointers of type [**void**](void.md) **\***.</span></span> <span data-ttu-id="65bbe-144">Portanto, esse recurso não está disponível quando você usa a opção [**/OSF**](-osf.md) do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="65bbe-144">Therefore this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="65bbe-145">Assim como ocorre com outros tipos de identificador, o identificador de contexto é opaco para o aplicativo cliente e todos os dados associados a ele não são transmitidos.</span><span class="sxs-lookup"><span data-stu-id="65bbe-145">As with other handle types, the context handle is opaque to the client application, and any data associated with it is not transmitted.</span></span> <span data-ttu-id="65bbe-146">No servidor, o identificador de contexto serve como um identificador no contexto ativo, e todos os dados associados ao tipo de identificador de contexto podem ser acessados.</span><span class="sxs-lookup"><span data-stu-id="65bbe-146">On the server, the context handle serves as a handle on active context, and all data associated with the context handle type is accessible.</span></span>

<span data-ttu-id="65bbe-147">Para criar um identificador de contexto, o cliente passa para o servidor um **\[** [](out-idl.md) **\]** ponteiro out, **\[** [**ref**](ref.md) **\]** para um identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="65bbe-147">To create a context handle, the client passes to the server an **\[**[**out**](out-idl.md)**\]**, **\[**[**ref**](ref.md)**\]** pointer to a context handle.</span></span> <span data-ttu-id="65bbe-148">(O próprio identificador de contexto pode ter um valor **nulo** ou não **nulo** — contanto que seu valor seja consistente com seus atributos de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="65bbe-148">(The context handle itself can have a **NULL** or non-**NULL** value—as long as its value is consistent with its pointer attributes.</span></span> <span data-ttu-id="65bbe-149">Por exemplo, quando o tipo de identificador de contexto tem o **\[** [](ref.md) **\]** atributo ref aplicado a ele, ele não pode ter um valor **nulo** .) Outro identificador de associação deve ser fornecido para realizar a associação até que o identificador de contexto seja criado.</span><span class="sxs-lookup"><span data-stu-id="65bbe-149">For example, when the context handle type has the **\[**[**ref**](ref.md)**\]** attribute applied to it, it cannot have a **NULL** value.) Another binding handle must be supplied to accomplish the binding until the context handle is created.</span></span> <span data-ttu-id="65bbe-150">Quando nenhum identificador explícito é especificado, a associação implícita é usada.</span><span class="sxs-lookup"><span data-stu-id="65bbe-150">When no explicit handle is specified, implicit binding is used.</span></span> <span data-ttu-id="65bbe-151">Quando nenhum **\[** atributo de [**\_ identificador implícito**](implicit-handle.md) **\]** está presente, um identificador automático é usado.</span><span class="sxs-lookup"><span data-stu-id="65bbe-151">When no **\[**[**implicit\_handle**](implicit-handle.md)**\]** attribute is present, an auto handle is used.</span></span>

<span data-ttu-id="65bbe-152">O procedimento remoto no servidor cria um identificador de contexto ativo.</span><span class="sxs-lookup"><span data-stu-id="65bbe-152">The remote procedure on the server creates an active context handle.</span></span> <span data-ttu-id="65bbe-153">O cliente deve usar esse identificador de contexto como um **\[** [](in.md) **\]** parâmetro in ou **\[ in**, **out \]** em chamadas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="65bbe-153">The client must use that context handle as an **\[**[**in**](in.md)**\]** or **\[in**, **out\]** parameter in subsequent calls.</span></span> <span data-ttu-id="65bbe-154">Um identificador de contexto somente **\[ \] no** pode ser usado como um identificador de associação, portanto, ele deve ter um valor não **nulo** .</span><span class="sxs-lookup"><span data-stu-id="65bbe-154">An **\[in\]**-only context handle can be used as a binding handle, so it must have a non-**NULL** value.</span></span> <span data-ttu-id="65bbe-155">Um identificador de contexto somente **\[ no \]** não reflete as alterações de estado no servidor.</span><span class="sxs-lookup"><span data-stu-id="65bbe-155">An **\[in\]**-only context handle does not reflect state changes on the server.</span></span>

<span data-ttu-id="65bbe-156">No servidor, o procedimento chamado pode interpretar o identificador de contexto conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="65bbe-156">On the server, the called procedure can interpret the context handle as needed.</span></span> <span data-ttu-id="65bbe-157">Por exemplo, o procedimento chamado pode alocar o armazenamento de heap e usar o identificador de contexto como um ponteiro para esse armazenamento.</span><span class="sxs-lookup"><span data-stu-id="65bbe-157">For example, the called procedure can allocate heap storage and use the context handle as a pointer to this storage.</span></span>

<span data-ttu-id="65bbe-158">Para fechar um identificador de contexto, o cliente passa o identificador de contexto como um **\[** argumento [**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="65bbe-158">To close a context handle, the client passes the context handle as an **\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]** argument.</span></span> <span data-ttu-id="65bbe-159">O servidor deve retornar um identificador de contexto **nulo** quando ele não estiver mais mantendo o contexto em nome do chamador.</span><span class="sxs-lookup"><span data-stu-id="65bbe-159">The server must return a **NULL** context handle when it is no longer maintaining context on behalf of the caller.</span></span> <span data-ttu-id="65bbe-160">Por exemplo, se o identificador de contexto representar um arquivo aberto e a chamada fechar o arquivo, o servidor deverá definir o identificador de contexto como **nulo** e retorná-lo ao cliente.</span><span class="sxs-lookup"><span data-stu-id="65bbe-160">For example, if the context handle represents an open file and the call closes the file, the server must set the context handle to **NULL** and return it to the client.</span></span> <span data-ttu-id="65bbe-161">Um valor **nulo** é inválido como um identificador de associação em chamadas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="65bbe-161">A **NULL** value is invalid as a binding handle on subsequent calls.</span></span>

<span data-ttu-id="65bbe-162">Um identificador de contexto só é válido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="65bbe-162">A context handle is only valid for one server.</span></span> <span data-ttu-id="65bbe-163">Quando uma função tem dois parâmetros de identificador e o identificador de contexto não é **nulo**, os identificadores de associação devem se referir ao mesmo espaço de endereço.</span><span class="sxs-lookup"><span data-stu-id="65bbe-163">When a function has two handle parameters and the context handle is not **NULL**, the binding handles must refer to the same address space.</span></span>

<span data-ttu-id="65bbe-164">Quando uma função tem um **\[** [](in.md) **\]** manipulador de contexto in ou **\[ in**, **out \]** , seu identificador de contexto pode ser usado como o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="65bbe-164">When a function has an **\[**[**in**](in.md)**\]** or an **\[in**, **out\]** context handle, its context handle can be used as the binding handle.</span></span> <span data-ttu-id="65bbe-165">Nesse caso, a associação implícita não é usada e o **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** ou o atributo de **\[** [**\_ identificador automático**](auto-handle.md) **\]** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="65bbe-165">In this case, implicit binding is not used and the **\[**[**implicit\_handle**](implicit-handle.md)**\]** or **\[**[**auto\_handle**](auto-handle.md)**\]** attribute is ignored.</span></span>

<span data-ttu-id="65bbe-166">As seguintes restrições se aplicam a identificadores de contexto:</span><span class="sxs-lookup"><span data-stu-id="65bbe-166">The following restrictions apply to context handles:</span></span>

-   <span data-ttu-id="65bbe-167">Os identificadores de contexto não podem ser elementos de matriz, membros de estrutura ou membros de União.</span><span class="sxs-lookup"><span data-stu-id="65bbe-167">Context handles cannot be array elements, structure members, or union members.</span></span> <span data-ttu-id="65bbe-168">Eles só podem ser parâmetros.</span><span class="sxs-lookup"><span data-stu-id="65bbe-168">They can only be parameters.</span></span>
-   <span data-ttu-id="65bbe-169">Os identificadores de contexto não podem ter o **\[** atributo [**transmitir \_ como**](transmit-as.md) **\]** ou **\[** [**representar \_ como**](represent-as.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="65bbe-169">Context handles cannot have the **\[**[**transmit\_as**](transmit-as.md)**\]** or **\[**[**represent\_as**](represent-as.md)**\]** attribute.</span></span>
-   <span data-ttu-id="65bbe-170">Os parâmetros que são ponteiros para os **\[** [](out-idl.md) **\]** identificadores de contexto de saída devem ser **\[** [](ref.md) **\]** ponteiros de referência.</span><span class="sxs-lookup"><span data-stu-id="65bbe-170">Parameters that are pointers to **\[**[**out**](out-idl.md)**\]** context handles must be **\[**[**ref**](ref.md)**\]** pointers.</span></span>
-   <span data-ttu-id="65bbe-171">Um **\[** identificador [**de contexto in**](in.md) **\]** pode ser usado como o identificador de associação e não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="65bbe-171">An **\[**[**in**](in.md)**\]** context handle can be used as the binding handle and cannot be **NULL**.</span></span>
-   <span data-ttu-id="65bbe-172">Um identificador **\[ de contexto in**, [**out**](out-idl.md) pode ser **nulo** na entrada, mas somente se o procedimento tiver outro parâmetro de identificador explícito.</span><span class="sxs-lookup"><span data-stu-id="65bbe-172">An **\[in**, [**out**](out-idl.md) context handle can be **NULL** on input, but only if the procedure has another explicit handle parameter.</span></span> <span data-ttu-id="65bbe-173">Se não houver nenhum outro parâmetro de identificador de contexto não **nulo** explícito, o identificador **\[ de contexto in** e **out \]** não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="65bbe-173">If there are no other explicit non-**NULL** context handle parameters, the **\[in**, **out\]** context handle cannot be **NULL**.</span></span>
-   <span data-ttu-id="65bbe-174">Um identificador de contexto não pode ser usado com retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="65bbe-174">A context handle cannot be used with callbacks.</span></span>

## <a name="examples"></a><span data-ttu-id="65bbe-175">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65bbe-175">Examples</span></span>

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a><span data-ttu-id="65bbe-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="65bbe-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65bbe-177">**Storage**</span><span class="sxs-lookup"><span data-stu-id="65bbe-177">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="65bbe-178">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="65bbe-178">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="65bbe-179">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="65bbe-179">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="65bbe-180">Redefinição de contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="65bbe-180">Client Context Reset</span></span>](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[<span data-ttu-id="65bbe-181">**const**</span><span class="sxs-lookup"><span data-stu-id="65bbe-181">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="65bbe-182">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="65bbe-182">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="65bbe-183">**processamento**</span><span class="sxs-lookup"><span data-stu-id="65bbe-183">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="65bbe-184">Associação e identificadores</span><span class="sxs-lookup"><span data-stu-id="65bbe-184">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="65bbe-185">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="65bbe-185">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="65bbe-186">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="65bbe-186">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="65bbe-187">**no**</span><span class="sxs-lookup"><span data-stu-id="65bbe-187">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="65bbe-188">**local**</span><span class="sxs-lookup"><span data-stu-id="65bbe-188">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="65bbe-189">Clientes multithread e identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="65bbe-189">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="65bbe-190">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="65bbe-190">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="65bbe-191">**fora**</span><span class="sxs-lookup"><span data-stu-id="65bbe-191">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="65bbe-192">**ptr**</span><span class="sxs-lookup"><span data-stu-id="65bbe-192">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="65bbe-193">**ref**</span><span class="sxs-lookup"><span data-stu-id="65bbe-193">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="65bbe-194">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="65bbe-194">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="65bbe-195">**RpcSsDestroyClientContext**</span><span class="sxs-lookup"><span data-stu-id="65bbe-195">**RpcSsDestroyClientContext**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[<span data-ttu-id="65bbe-196">Rotina de execução de contexto de servidor</span><span class="sxs-lookup"><span data-stu-id="65bbe-196">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="65bbe-197">**string**</span><span class="sxs-lookup"><span data-stu-id="65bbe-197">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="65bbe-198">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="65bbe-198">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="65bbe-199">**typedef**</span><span class="sxs-lookup"><span data-stu-id="65bbe-199">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="65bbe-200">**diferente**</span><span class="sxs-lookup"><span data-stu-id="65bbe-200">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="65bbe-201">**void**</span><span class="sxs-lookup"><span data-stu-id="65bbe-201">**void**</span></span>](void.md)
</dt> </dl>

 

 