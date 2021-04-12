---
title: atributo de retorno de chamada
description: O atributo \ callback \ declara uma função de retorno de chamada estática que existe no lado do cliente do aplicativo distribuído. As funções de retorno de chamada fornecem uma maneira para o servidor executar código no cliente.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- atributo de retorno de chamada MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365950"
---
# <a name="callback-attribute"></a><span data-ttu-id="c6af4-105">atributo de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="c6af4-105">callback attribute</span></span>

<span data-ttu-id="c6af4-106">O atributo de **\[ retorno de chamada \]** declara uma função de retorno de chamada estática que existe no lado do cliente do aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="c6af4-106">The **\[callback\]** attribute declares a static callback function that exists on the client side of the distributed application.</span></span> <span data-ttu-id="c6af4-107">As funções de retorno de chamada fornecem uma maneira para o servidor executar código no cliente.</span><span class="sxs-lookup"><span data-stu-id="c6af4-107">Callback functions provide a way for the server to execute code on the client.</span></span>

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="c6af4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6af4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6af4-109">*função-attr-lista*</span><span class="sxs-lookup"><span data-stu-id="c6af4-109">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c6af4-110">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="c6af4-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="c6af4-111">Os atributos de função válidos são **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="c6af4-111">Valid function attributes are **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span> <span data-ttu-id="c6af4-112">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="c6af4-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c6af4-113">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="c6af4-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="c6af4-114">Especifica um [ \_ tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="c6af4-114">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="c6af4-115">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="c6af4-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="c6af4-116">*Declarador de PTR*</span><span class="sxs-lookup"><span data-stu-id="c6af4-116">*ptr-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="c6af4-117">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="c6af4-117">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="c6af4-118">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="c6af4-118">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6af4-119">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="c6af4-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c6af4-120">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="c6af4-120">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="c6af4-121">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="c6af4-121">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c6af4-122">Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="c6af4-122">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="c6af4-123">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="c6af4-123">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c6af4-124">*Declarador*</span><span class="sxs-lookup"><span data-stu-id="c6af4-124">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="c6af4-125">Especifica um Declarador C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="c6af4-125">Specifies a standard C declarator such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="c6af4-126">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="c6af4-126">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="c6af4-127">O identificador de nome de parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c6af4-127">The parameter-name identifier is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6af4-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6af4-128">Remarks</span></span>

<span data-ttu-id="c6af4-129">A função de **\[ retorno de chamada \]** é útil quando o servidor deve obter informações do cliente.</span><span class="sxs-lookup"><span data-stu-id="c6af4-129">The **\[callback\]** function is useful when the server must obtain information from the client.</span></span> <span data-ttu-id="c6af4-130">Se os aplicativos de servidor tiverem suporte no Windows 3. *x*, o servidor pode fazer uma chamada para um procedimento remoto no Windows 3. *x* Server para obter as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="c6af4-130">If server applications were supported on Windows 3.*x*, the server could make a call to a remote procedure on the Windows 3.*x* server to obtain the needed information.</span></span> <span data-ttu-id="c6af4-131">A função de retorno de chamada realiza a mesma finalidade e permite que o servidor consulte o cliente para obter informações no contexto da chamada original.</span><span class="sxs-lookup"><span data-stu-id="c6af4-131">The callback function accomplishes the same purpose and lets the server query the client for information in the context of the original call.</span></span>

<span data-ttu-id="c6af4-132">Os retornos de chamada são casos especiais de chamadas remotas que são executadas como parte de um único thread.</span><span class="sxs-lookup"><span data-stu-id="c6af4-132">Callbacks are special cases of remote calls that execute as part of a single thread.</span></span> <span data-ttu-id="c6af4-133">Um retorno de chamada é emitido no contexto de uma chamada remota.</span><span class="sxs-lookup"><span data-stu-id="c6af4-133">A callback is issued in the context of a remote call.</span></span> <span data-ttu-id="c6af4-134">Qualquer procedimento remoto definido como parte da mesma interface que a função de retorno de chamada estática pode chamar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c6af4-134">Any remote procedure defined as part of the same interface as the static callback function can call the callback function.</span></span>

<span data-ttu-id="c6af4-135">É importante observar que o uso de retorno de \[ chamada \] não é recomendado na programação de vários threads.</span><span class="sxs-lookup"><span data-stu-id="c6af4-135">It is important to note that the use of \[callback\] is not recommended in multi-thread programming.</span></span> <span data-ttu-id="c6af4-136">Como uma função de programação de thread único, ele não está equipado para dar suporte às demandas de segurança que um ambiente de vários threads fornece.</span><span class="sxs-lookup"><span data-stu-id="c6af4-136">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

<span data-ttu-id="c6af4-137">A função **RpcCancelThread** não pode ser usada para cancelar uma chamada que pode enviar um retorno de chamada estático.</span><span class="sxs-lookup"><span data-stu-id="c6af4-137">The **RpcCancelThread** function cannot be used to cancel a call that may dispatch a static callback.</span></span> <span data-ttu-id="c6af4-138">Se uma chamada de procedimento remoto específica nunca resultar em um retorno de chamada, ela poderá ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="c6af4-138">If a particular remote procedure call will never result in a callback, then it can be canceled.</span></span> <span data-ttu-id="c6af4-139">Caso contrário, uma chamada poderá ser cancelada somente se puder ter certeza de que um retorno de chamada para ele não foi emitido.</span><span class="sxs-lookup"><span data-stu-id="c6af4-139">Otherwise, a call can be canceled only if it can be guaranteed that a callback for it has not been issued.</span></span>

<span data-ttu-id="c6af4-140">Somente as sequências orientadas a conexão e de protocolo local dão suporte ao atributo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c6af4-140">Only the connection-oriented and local-protocol sequences support the callback attribute.</span></span> <span data-ttu-id="c6af4-141">O tamanho dos \[ dados de saída \] para retornos de chamada na sequência de protocolo local é limitado a 150 bytes.</span><span class="sxs-lookup"><span data-stu-id="c6af4-141">The size of the \[out\] data for callbacks over the local-protocol sequence is limited to 150 bytes.</span></span> <span data-ttu-id="c6af4-142">Se uma interface RPC usar uma sequência de protocolo sem conexão (datagrama), as chamadas para procedimentos com o atributo de retorno de chamada falharão.</span><span class="sxs-lookup"><span data-stu-id="c6af4-142">If an RPC interface uses a connectionless (datagram) protocol sequence, calls to procedures with the callback attribute will fail.</span></span>

<span data-ttu-id="c6af4-143">Identificadores não podem ser usados como parâmetros em funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c6af4-143">Handles cannot be used as parameters in callback functions.</span></span> <span data-ttu-id="c6af4-144">Como os retornos de chamadas são sempre executados no contexto de uma chamada, o identificador de associação usado pelo cliente para fazer a chamada para o servidor também é usado como o identificador de ligação do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="c6af4-144">Because callbacks always execute in the context of a call, the binding handle used by the client to make the call to the server is also used as the binding handle from the server to the client.</span></span>

<span data-ttu-id="c6af4-145">Os retornos de chamada podem ser aninhados em qualquer profundidade.</span><span class="sxs-lookup"><span data-stu-id="c6af4-145">Callbacks can nest to any depth.</span></span>

## <a name="examples"></a><span data-ttu-id="c6af4-146">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6af4-146">Examples</span></span>

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a><span data-ttu-id="c6af4-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6af4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6af4-148">**Storage**</span><span class="sxs-lookup"><span data-stu-id="c6af4-148">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="c6af4-149">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="c6af4-149">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="c6af4-150">**const**</span><span class="sxs-lookup"><span data-stu-id="c6af4-150">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="c6af4-151">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="c6af4-151">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="c6af4-152">**enumera**</span><span class="sxs-lookup"><span data-stu-id="c6af4-152">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="c6af4-153">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="c6af4-153">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c6af4-154">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="c6af4-154">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="c6af4-155">**local**</span><span class="sxs-lookup"><span data-stu-id="c6af4-155">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="c6af4-156">**/osf**</span><span class="sxs-lookup"><span data-stu-id="c6af4-156">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="c6af4-157">**ref**</span><span class="sxs-lookup"><span data-stu-id="c6af4-157">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="c6af4-158">**ptr**</span><span class="sxs-lookup"><span data-stu-id="c6af4-158">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="c6af4-159">**string**</span><span class="sxs-lookup"><span data-stu-id="c6af4-159">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="c6af4-160">**struct**</span><span class="sxs-lookup"><span data-stu-id="c6af4-160">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="c6af4-161">**unida**</span><span class="sxs-lookup"><span data-stu-id="c6af4-161">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="c6af4-162">**diferente**</span><span class="sxs-lookup"><span data-stu-id="c6af4-162">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="c6af4-163">**RpcCancelThread**</span><span class="sxs-lookup"><span data-stu-id="c6af4-163">**RpcCancelThread**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 