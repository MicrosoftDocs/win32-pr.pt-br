---
title: atributo de pipe
description: O construtor de tipo de pipe torna possível transmitir um fluxo aberto de dados digitados através de uma chamada de procedimento remoto.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- MIDL do atributo de pipe
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293935"
---
# <a name="pipe-attribute"></a><span data-ttu-id="a4e34-104">atributo de pipe</span><span class="sxs-lookup"><span data-stu-id="a4e34-104">pipe attribute</span></span>

<span data-ttu-id="a4e34-105">O construtor de tipo de **pipe** torna possível transmitir um fluxo aberto de dados digitados através de uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a4e34-105">The **pipe** type constructor makes it possible to transmit an open-ended stream of typed data across a remote procedure call.</span></span>

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a><span data-ttu-id="a4e34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4e34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4e34-107">*tipo de elemento*</span><span class="sxs-lookup"><span data-stu-id="a4e34-107">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a4e34-108">Define o tamanho de um único elemento no buffer de transferência.</span><span class="sxs-lookup"><span data-stu-id="a4e34-108">Defines the size of a single element in the transfer buffer.</span></span> <span data-ttu-id="a4e34-109">O *tipo de elemento* pode ser um [tipo base](midl-base-types.md), um \_ tipo predefinido, um [**struct**](struct.md), uma [**Enumeração 32b**](v1-enum.md)ou um identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="a4e34-109">The *element-type* can be a [base type](midl-base-types.md), predefined\_type, [**struct**](struct.md), [**32b enum**](v1-enum.md), or type identifier.</span></span> <span data-ttu-id="a4e34-110">Várias restrições se aplicam a *\_ tipos de elementos*, conforme descrito em comentários, abaixo.</span><span class="sxs-lookup"><span data-stu-id="a4e34-110">Several restrictions apply to *element\_types*, as described in Remarks, below.</span></span>

</dd> <dt>

<span data-ttu-id="a4e34-111">*Declarador de pipe*</span><span class="sxs-lookup"><span data-stu-id="a4e34-111">*pipe-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="a4e34-112">Especifica um ou mais identificadores ou ponteiros para identificadores.</span><span class="sxs-lookup"><span data-stu-id="a4e34-112">Specifies one or more identifiers or pointers to identifiers.</span></span> <span data-ttu-id="a4e34-113">Separe vários declaradores com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a4e34-113">Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4e34-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4e34-114">Remarks</span></span>

<span data-ttu-id="a4e34-115">Você pode usar o construtor de tipo de **pipe** para transmitir dados em ambas as direções.</span><span class="sxs-lookup"><span data-stu-id="a4e34-115">You can use the **pipe** type constructor to transmit data in both directions.</span></span> <span data-ttu-id="a4e34-116">Um **\[** [](in.md) **\]** parâmetro no pipe permite que o servidor receba o fluxo de dados do cliente durante uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a4e34-116">An **\[**[**in**](in.md)**\]** pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="a4e34-117">Um **\[** [](out-idl.md) **\]** parâmetro out pipe permite que o servidor envie por push o fluxo de dados de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="a4e34-117">An **\[**[**out**](out-idl.md)**\]** pipe parameter allows the server to push the data stream back to the client.</span></span> <span data-ttu-id="a4e34-118">Você fornece as rotinas do lado do cliente para enviar por push e efetuar pull do fluxo de dados e alocar um buffer global para os dados.</span><span class="sxs-lookup"><span data-stu-id="a4e34-118">You supply the client-side routines to push and pull the data stream and to allocate a global buffer for the data.</span></span> <span data-ttu-id="a4e34-119">As rotinas de stub do cliente e do servidor realizam marshaling e unmarshaling de dados e transmitem uma referência para o buffer de volta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4e34-119">The client and server stub routines marshal and unmarshal data and pass a reference to the buffer back to the application.</span></span>

<span data-ttu-id="a4e34-120">As seguintes restrições se aplicam a Pipes:</span><span class="sxs-lookup"><span data-stu-id="a4e34-120">The following restrictions apply to pipes:</span></span>

-   <span data-ttu-id="a4e34-121">Um elemento de pipe não pode ser ou conter um ponteiro, uma matriz em conformidade ou variável, um identificador ou um identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="a4e34-121">A pipe element cannot be or contain a pointer, a conformant or varying array, a handle, or a context handle.</span></span> <span data-ttu-id="a4e34-122">Além disso, na implementação de pipes da Microsoft, um elemento de pipe não pode ser ou conter uma [**Union**](union.md), uma [**Enumeração 16B**](enum.md)ou um [**\_ \_ int3264**](--int3264.md).</span><span class="sxs-lookup"><span data-stu-id="a4e34-122">Also, in the Microsoft implementation of pipes, a pipe element cannot be or contain a [**union**](union.md), a [**16b enum**](enum.md), or an [**\_\_int3264**](--int3264.md).</span></span>
-   <span data-ttu-id="a4e34-123">Você não pode aplicar os **\[** atributos [**transmitir \_ como**](transmit-as.md) **\]** , **\[** [**representar \_ como**](represent-as.md) **\]** , **\[** [**\_ realizar marshaling**](wire-marshal.md) **\]** ou **\[** [**\_ Marshal do usuário**](user-marshal.md) **\]** a um tipo de pipe ou ao *tipo de elemento*.</span><span class="sxs-lookup"><span data-stu-id="a4e34-123">You cannot apply the **\[**[**transmit\_as**](transmit-as.md)**\]**, **\[**[**represent\_as**](represent-as.md)**\]**, **\[**[**wire\_marshal**](wire-marshal.md)**\]**, or **\[**[**user\_marshal**](user-marshal.md)**\]** attributes to a pipe type or to the *element-type*.</span></span>
-   <span data-ttu-id="a4e34-124">Um tipo de pipe não pode ser um membro de uma estrutura ou União, o destino de um ponteiro ou o tipo base de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="a4e34-124">A pipe type cannot be a member of a structure or union, the target of a pointer, or the base type of an array.</span></span>
-   <span data-ttu-id="a4e34-125">Um tipo de dados declarado como um tipo de pipe só pode ser usado como um parâmetro de uma chamada remota.</span><span class="sxs-lookup"><span data-stu-id="a4e34-125">A data type declared to be a pipe type can only be used as a parameter of a remote call.</span></span>
-   <span data-ttu-id="a4e34-126">Você pode passar um parâmetro de pipe em ambas as direções por valor ou por referência ( **\[** ponteiro [**ref**](ref.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="a4e34-126">You can pass a pipe parameter in either direction by value or by reference (**\[**[**ref**](ref.md)**\]** pointer).</span></span> <span data-ttu-id="a4e34-127">No entanto, não é possível aplicar o **\[** [](ptr.md) **\]** atributo PTR a um pipe que é passado por referência.</span><span class="sxs-lookup"><span data-stu-id="a4e34-127">However you cannot apply the **\[**[**ptr**](ptr.md)**\]** attribute to a pipe that is passed by reference.</span></span> <span data-ttu-id="a4e34-128">Você não pode especificar um parâmetro de pipe com um **\[** [](unique.md) **\]** ponteiro exclusivo ou completo, independentemente da direção.</span><span class="sxs-lookup"><span data-stu-id="a4e34-128">You cannot specify a pipe parameter with a **\[**[**unique**](unique.md)**\]** or a full pointer, regardless of direction.</span></span>
-   <span data-ttu-id="a4e34-129">Você não pode usar pipes em interfaces de **\[** [**objeto**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a4e34-129">You cannot use pipes in **\[**[**object**](object.md)**\]** interfaces.</span></span>
-   <span data-ttu-id="a4e34-130">Você não pode aplicar o **\[** [](idempotent.md) **\]** atributo idempotente a uma rotina que tem um parâmetro de pipe.</span><span class="sxs-lookup"><span data-stu-id="a4e34-130">You cannot apply the **\[**[**idempotent**](idempotent.md)**\]** attribute to a routine that has a pipe parameter.</span></span>
-   <span data-ttu-id="a4e34-131">Você não pode usar os atributos de serialização, **\[** [**codificar**](encode.md) **\]** e **\[** [**decodificar**](decode.md) **\]** com pipes.</span><span class="sxs-lookup"><span data-stu-id="a4e34-131">You cannot use the serialization attributes, **\[**[**encode**](encode.md)**\]** and **\[**[**decode**](decode.md)**\]** with pipes.</span></span>
-   <span data-ttu-id="a4e34-132">Você não pode usar identificadores automáticos, por padrão, ou com o **\[** atributo [**\_ identificador automático**](auto-handle.md) **\]** , com pipes.</span><span class="sxs-lookup"><span data-stu-id="a4e34-132">You cannot use automatic handles, either by default, or with the **\[**[**auto\_handle**](auto-handle.md)**\]** attribute, with pipes.</span></span>

> [!Note]  
> <span data-ttu-id="a4e34-133">O compilador MIDL dá suporte somente a pipes no modo [**/OIF**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="a4e34-133">The MIDL compiler supports pipes in [**/Oif**](-oi.md) mode only.</span></span>

 

<span data-ttu-id="a4e34-134">Para obter mais informações sobre como implementar rotinas com parâmetros de pipe, consulte [pipes](/windows/desktop/Rpc/pipes) no guia do programador de RPC e referência.</span><span class="sxs-lookup"><span data-stu-id="a4e34-134">For more information on implementing routines with pipe parameters, see [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer's Guide and Reference.</span></span>

## <a name="examples"></a><span data-ttu-id="a4e34-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4e34-135">Examples</span></span>

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a><span data-ttu-id="a4e34-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4e34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e34-137">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="a4e34-137">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="a4e34-138">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="a4e34-138">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a4e34-139">**RET**</span><span class="sxs-lookup"><span data-stu-id="a4e34-139">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="a4e34-140">**codificado**</span><span class="sxs-lookup"><span data-stu-id="a4e34-140">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="a4e34-141">**enumera**</span><span class="sxs-lookup"><span data-stu-id="a4e34-141">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="a4e34-142">**idempotente**</span><span class="sxs-lookup"><span data-stu-id="a4e34-142">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="a4e34-143">**no**</span><span class="sxs-lookup"><span data-stu-id="a4e34-143">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="a4e34-144">**objeto**</span><span class="sxs-lookup"><span data-stu-id="a4e34-144">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="a4e34-145">**fora**</span><span class="sxs-lookup"><span data-stu-id="a4e34-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="a4e34-146">**ptr**</span><span class="sxs-lookup"><span data-stu-id="a4e34-146">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="a4e34-147">**ref**</span><span class="sxs-lookup"><span data-stu-id="a4e34-147">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="a4e34-148">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="a4e34-148">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="a4e34-149">**struct**</span><span class="sxs-lookup"><span data-stu-id="a4e34-149">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="a4e34-150">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="a4e34-150">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="a4e34-151">**diferente**</span><span class="sxs-lookup"><span data-stu-id="a4e34-151">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="a4e34-152">**Marshal do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="a4e34-152">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="a4e34-153">**\_marshaling de transmissão**</span><span class="sxs-lookup"><span data-stu-id="a4e34-153">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> </dl>

 

 