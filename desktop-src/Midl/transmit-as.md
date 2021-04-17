---
title: Atributo transmit_as
description: O atributo \ transmitir \_ como \ instrui o compilador a associar o Type-ID, que é um tipo apresentado que os aplicativos cliente e servidor manipulam, com um tipo transmitido tipo de transmissão.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as do atributo MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105755093"
---
# <a name="transmit_as-attribute"></a><span data-ttu-id="4a1d7-104">transmitir \_ como atributo</span><span class="sxs-lookup"><span data-stu-id="4a1d7-104">transmit\_as attribute</span></span>

<span data-ttu-id="4a1d7-105">O atributo **\[ transmitir \_ como \]** instrui o compilador a associar \*\*Type-ID \* \* *,* que é um tipo apresentado que os aplicativos cliente e servidor manipulam, com um tipo transmitido **tipo de transmissão.**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-105">The **\[transmit\_as\]** attribute instructs the compiler to associate \**type-id\*\*\*,* which is a presented type that client and server applications manipulate, with a transmitted type **xmit-type.**</span></span>

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a><span data-ttu-id="4a1d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a1d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a1d7-107">*tipo de transmissão*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-107">*xmit-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4a1d7-108">Especifica o tipo de dados que é transmitido entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-108">Specifies the data type that is transmitted between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="4a1d7-109">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4a1d7-110">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="4a1d7-111">Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md), **\]** referência de atributo de ponteiro **\[** [](ref.md) **\]** , **\[** [**exclusivo**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4a1d7-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="4a1d7-112">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4a1d7-113">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4a1d7-114">Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="4a1d7-115">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="4a1d7-116">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4a1d7-117">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-117">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="4a1d7-118">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4a1d7-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="4a1d7-119">A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-119">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="4a1d7-120">O Declarador de parâmetro no Declarador de função, como o nome do parâmetro, é opcional.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-120">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4a1d7-121">*ID do tipo*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-121">*type-id*</span></span> 
</dt> <dd>

<span data-ttu-id="4a1d7-122">Especifica o nome do tipo de dados que é apresentado aos aplicativos cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-122">Specifies the name of the data type that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a1d7-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a1d7-123">Remarks</span></span>

<span data-ttu-id="4a1d7-124">Para usar o atributo **\[ transmitir \_ como \]** , o usuário deve fornecer rotinas que convertam dados entre os tipos apresentados e transmitidos; essas rotinas também devem liberar memória usada para manter os dados convertidos.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-124">To use the **\[transmit\_as\]** attribute, the user must supply routines that convert data between the presented and the transmitted types; these routines must also free memory used to hold the converted data.</span></span> <span data-ttu-id="4a1d7-125">O atributo **\[ transmitir \_ como \]** instrui os stubs a chamar as rotinas de conversão fornecidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-125">The **\[transmit\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="4a1d7-126">O tipo transmitido tipo *de transmissão* deve ser resolvido para um tipo base de MIDL, tipo predefinido ou um identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-126">The transmitted type *xmit-type* must resolve to a MIDL base type, predefined type, or a type identifier.</span></span> <span data-ttu-id="4a1d7-127">Para obter mais informações, consulte [tipos base de MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="4a1d7-127">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="4a1d7-128">O usuário deve fornecer as rotinas a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-128">The user must supply the following routines.</span></span>



| <span data-ttu-id="4a1d7-129">Nome da rotina</span><span class="sxs-lookup"><span data-stu-id="4a1d7-129">Routine name</span></span>              | <span data-ttu-id="4a1d7-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a1d7-130">Description</span></span>                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1d7-131">*tipo-ID \* \* \* \_ para \_ transmissão*\*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-131">*type-id\*\*\*\_to\_xmit*\*</span></span>   | <span data-ttu-id="4a1d7-132">Converte dados do tipo apresentado para o tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-132">Converts data from the presented type to the transmitted type.</span></span> <span data-ttu-id="4a1d7-133">Essa rotina aloca memória para o tipo transmitido e para todos os dados referenciados por ponteiros no tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-133">This routine allocates memory for the transmitted type and for any data referenced by pointers in the transmitted type.</span></span>                            |
| <span data-ttu-id="4a1d7-134">*tipo-ID \* \* \* \_ da \_ transmissão*\*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-134">*type-id\*\*\*\_from\_xmit*\*</span></span> | <span data-ttu-id="4a1d7-135">Converte dados do tipo transmitido para o tipo apresentado.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-135">Converts data from the transmitted type to the presented type.</span></span> <span data-ttu-id="4a1d7-136">Essa rotina é responsável por alocar memória para dados referenciados por ponteiros no tipo apresentado.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-136">This routine is responsible for allocating memory for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="4a1d7-137">O RPC aloca memória para o próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-137">RPC allocates memory for the type itself.</span></span> |
| <span data-ttu-id="4a1d7-138">*tipo-ID \* \* \* \_ \_ InStr gratuito*\*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-138">*type-id\*\*\*\_free\_inst*\*</span></span> | <span data-ttu-id="4a1d7-139">Libera memória alocada para dados referenciados por ponteiros no tipo apresentado.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-139">Frees memory allocated for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="4a1d7-140">O RPC libera a memória para o próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-140">RPC frees memory for the type itself.</span></span>                                                                                               |
| <span data-ttu-id="4a1d7-141">*tipo-ID \* \* \* \_ \_ transmissão gratuita*\*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-141">*type-id\*\*\*\_free\_xmit*\*</span></span> | <span data-ttu-id="4a1d7-142">Libera o armazenamento usado pelo chamador para o tipo transmitido e para os dados referenciados por ponteiros no tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-142">Frees storage used by the caller for the transmitted type and for data referenced by pointers in the transmitted type.</span></span>                                                                                            |



 

 

<span data-ttu-id="4a1d7-143">O stub do cliente chama *Type-ID \* \* \* \_ para \_ transmissão*\* para alocar espaço para o tipo transmitido e para converter os dados em objetos do tipo *transmissão-tipo.*</span><span class="sxs-lookup"><span data-stu-id="4a1d7-143">The client stub calls *type-id\*\*\*\_to\_xmit*\* to allocate space for the transmitted type and to translate the data into objects of type *xmit-type.*</span></span> <span data-ttu-id="4a1d7-144">O stub de servidor aloca espaço para o tipo de dados original e chama o *tipo de ID \* \* \* \_ de \_ transmissão*\* para converter os dados de seu tipo transmitido para o tipo apresentado.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-144">The server stub allocates space for the original data type and calls *type-id\*\*\*\_from\_xmit*\* to translate the data from its transmitted type to the presented type.</span></span>

<span data-ttu-id="4a1d7-145">Após o retorno do código do aplicativo, o stub do servidor chama o *tipo-ID \* \* \* \_ Free \_ Inst*\* para desalocar o armazenamento para o *tipo ID* no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-145">Upon return from the application code, the server stub calls *type-id\*\*\*\_free\_inst*\* to deallocate the storage for *type-id* on the server side.</span></span> <span data-ttu-id="4a1d7-146">O stub do cliente chama *Type-ID \* \* \_ \* \_ transmissão gratuita*\* para desalocar o armazenamento do *tipo de transmissão* no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-146">The client stub calls *type-id\*\*\*\_free\_xmit*\* to deallocate the *xmit-type* storage on the client side.</span></span>

<span data-ttu-id="4a1d7-147">Os tipos a seguir não podem ter um atributo de **\[ transmissão \_ as \]** :</span><span class="sxs-lookup"><span data-stu-id="4a1d7-147">The following types cannot have a **\[transmit\_as\]** attribute:</span></span>

-   <span data-ttu-id="4a1d7-148">Identificadores de contexto (tipos com o atributo de tipo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** e tipos que são usados como parâmetros com o atributo de **\[ \_ identificador \] de contexto** )</span><span class="sxs-lookup"><span data-stu-id="4a1d7-148">Context handles (types with the **\[**[**context\_handle**](context-handle.md)**\]** type attribute and types that are used as parameters with the **\[context\_handle\]** attribute)</span></span>
-   <span data-ttu-id="4a1d7-149">Tipos que são pipes ou derivados de pipes</span><span class="sxs-lookup"><span data-stu-id="4a1d7-149">Types that are pipes or derived from pipes</span></span>
-   <span data-ttu-id="4a1d7-150">Tipos de dados que são usados como o tipo base de uma definição de pipe</span><span class="sxs-lookup"><span data-stu-id="4a1d7-150">Data types that are used as the base type of a pipe definition</span></span>
-   <span data-ttu-id="4a1d7-151">Parâmetros que são ponteiros ou resolvem para ponteiros</span><span class="sxs-lookup"><span data-stu-id="4a1d7-151">Parameters that are pointers or resolve to pointers</span></span>
-   <span data-ttu-id="4a1d7-152">Parâmetros que são de conformidade, variáveis ou matrizes abertas</span><span class="sxs-lookup"><span data-stu-id="4a1d7-152">Parameters that are conformant, varying, or open arrays</span></span>
-   <span data-ttu-id="4a1d7-153">Estruturas que contêm matrizes de conformidade</span><span class="sxs-lookup"><span data-stu-id="4a1d7-153">Structures that contain conformant arrays</span></span>
-   <span data-ttu-id="4a1d7-154">O identificador de tipo predefinido [**\_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="4a1d7-154">The predefined type [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>

<span data-ttu-id="4a1d7-155">Os tipos transmitidos devem estar de acordo com as seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="4a1d7-155">Types that are transmitted must conform to the following restrictions:</span></span>

-   <span data-ttu-id="4a1d7-156">Eles não devem ser ponteiros ou conter ponteiros.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-156">They must not be pointers or contain pointers.</span></span>
-   <span data-ttu-id="4a1d7-157">Eles não devem ser pipes ou conter pipes.</span><span class="sxs-lookup"><span data-stu-id="4a1d7-157">They must not be pipes or contain pipes.</span></span>

## <a name="examples"></a><span data-ttu-id="4a1d7-158">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4a1d7-158">Examples</span></span>

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a><span data-ttu-id="4a1d7-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a1d7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1d7-160">**Storage**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-160">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-161">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="4a1d7-161">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-162">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-162">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-163">**enumera**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-163">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-164">**processamento**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-164">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-165">**lidar com \_ t**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-165">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-166">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="4a1d7-166">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-167">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-168">**ptr**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-168">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-169">**ref**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-169">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-170">**string**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-170">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-171">**struct**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-171">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-172">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-172">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-173">**typedef**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-173">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-174">**unida**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-174">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-175">**diferente**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-175">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="4a1d7-176">**void**</span><span class="sxs-lookup"><span data-stu-id="4a1d7-176">**void**</span></span>](void.md)
</dt> </dl>

 

 