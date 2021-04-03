---
title: represent_as atributo
description: O atributo \ represente \_ como \ ACF associa um tipo de local nomeado no idioma de destino repr com um tipo de transferência denominado-Type que é transferido entre cliente e servidor.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as do atributo MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006278"
---
# <a name="represent_as-attribute"></a><span data-ttu-id="dff66-104">representar \_ como atributo</span><span class="sxs-lookup"><span data-stu-id="dff66-104">represent\_as attribute</span></span>

<span data-ttu-id="dff66-105">O atributo **\[ represente \_ como \]** ACF associa um tipo de local nomeado no idioma de destino *repr* com um tipo de transferência *denominado-Type* que é transferido entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="dff66-105">The **\[represent\_as\]** ACF attribute associates a named local type in the target language *repr-type* with a transfer type *named-type* that is transferred between client and server.</span></span>

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a><span data-ttu-id="dff66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dff66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff66-107">*tipo nomeado*</span><span class="sxs-lookup"><span data-stu-id="dff66-107">*named-type*</span></span> 
</dt> <dd>

<span data-ttu-id="dff66-108">Especifica o tipo de dados de transferência nomeado que é transferido entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="dff66-108">Specifies the named transfer data type that is transferred between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="dff66-109">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="dff66-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dff66-110">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="dff66-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="dff66-111">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="dff66-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="dff66-112">*repr-tipo*</span><span class="sxs-lookup"><span data-stu-id="dff66-112">*repr-type*</span></span> 
</dt> <dd>

<span data-ttu-id="dff66-113">Especifica o tipo local representado no idioma de destino que é apresentado aos aplicativos cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="dff66-113">Specifies the represented local type in the target language that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dff66-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dff66-114">Remarks</span></span>

<span data-ttu-id="dff66-115">Ao usar **\[ representar \_ como \]**, você deve fornecer rotinas que são convertidas entre os tipos local e de transferência e a memória livre usada para manter os dados convertidos.</span><span class="sxs-lookup"><span data-stu-id="dff66-115">When using **\[represent\_as\]**, you must supply routines that convert between the local and the transfer types and that free memory used to hold the converted data.</span></span> <span data-ttu-id="dff66-116">O atributo **\[ representar \_ como \]** instrui os stubs a chamar as rotinas de conversão fornecidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="dff66-116">The **\[represent\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="dff66-117">O tipo de *nome* transferido deve ser resolvido para um tipo base de MIDL, tipo predefinido ou para um identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="dff66-117">The transferred type *named-type* must resolve to a MIDL base type, predefined type, or to a type identifier.</span></span> <span data-ttu-id="dff66-118">Para obter mais informações, consulte [tipos base de MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="dff66-118">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="dff66-119">Você deve fornecer as seguintes rotinas:</span><span class="sxs-lookup"><span data-stu-id="dff66-119">You must supply the following routines:</span></span>



| <span data-ttu-id="dff66-120">Nome da rotina</span><span class="sxs-lookup"><span data-stu-id="dff66-120">Routine name</span></span>                   | <span data-ttu-id="dff66-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="dff66-121">Description</span></span>                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dff66-122">*\_tipo nomeado \* \* \* \_ do \_ local*\*</span><span class="sxs-lookup"><span data-stu-id="dff66-122">*named\_type\*\*\*\_from\_local*\*</span></span> | <span data-ttu-id="dff66-123">Converte dados do tipo local para o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="dff66-123">Converts data from the local type to the network type.</span></span> <span data-ttu-id="dff66-124">A rotina aloca memória para o tipo de dados de rede, incluindo memória para todos os dados referenciados por ponteiros no tipo de dados de rede.</span><span class="sxs-lookup"><span data-stu-id="dff66-124">The routine allocates memory for the network data type, including memory for any data referenced by pointers in the network data type.</span></span>              |
| <span data-ttu-id="dff66-125">*\_tipo nomeado \* \* \* \_ para \_ local*\*</span><span class="sxs-lookup"><span data-stu-id="dff66-125">*named\_type\*\*\*\_to\_local*\*</span></span>   | <span data-ttu-id="dff66-126">Converte dados do tipo de rede para o tipo local.</span><span class="sxs-lookup"><span data-stu-id="dff66-126">Converts data from the network type to the local type.</span></span> <span data-ttu-id="dff66-127">A rotina é responsável por alocar memória para os dados referenciados por ponteiros no tipo local.</span><span class="sxs-lookup"><span data-stu-id="dff66-127">The routine is responsible for allocating memory for data referenced by pointers in the local type.</span></span> <span data-ttu-id="dff66-128">O RPC aloca memória para o tipo local em si.</span><span class="sxs-lookup"><span data-stu-id="dff66-128">RPC allocates memory for the local type itself.</span></span> |
| <span data-ttu-id="dff66-129">*\_tipo nomeado \* \* \* \_ \_ local livre*\*</span><span class="sxs-lookup"><span data-stu-id="dff66-129">*named\_type\*\*\*\_free\_local*\*</span></span> | <span data-ttu-id="dff66-130">Libera memória alocada para dados referenciados por ponteiros no tipo local.</span><span class="sxs-lookup"><span data-stu-id="dff66-130">Frees memory allocated for data referenced by pointers in the local type.</span></span> <span data-ttu-id="dff66-131">O RPC libera a memória para o próprio tipo</span><span class="sxs-lookup"><span data-stu-id="dff66-131">RPC frees memory for the type itself</span></span>                                                                                             |
| <span data-ttu-id="dff66-132">*\_tipo nomeado \* \* \* \_ \_ Inst gratuito*\*</span><span class="sxs-lookup"><span data-stu-id="dff66-132">*named\_type\*\*\*\_free\_inst*\*</span></span>  | <span data-ttu-id="dff66-133">Libera memória alocada para os dados referenciados por ponteiros no tipo de rede e para o próprio tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="dff66-133">Frees memory allocated for the data referenced by pointers in the network type and for the network type itself.</span></span>                                                                                            |



 

<span data-ttu-id="dff66-134">O stub de cliente chama o *tipo nomeado \* \* \* \_ de \_ local*\* para alocar espaço para o tipo transmitido e para converter os dados do tipo local para o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="dff66-134">The client stub calls *named-type\*\*\*\_from\_local*\* to allocate space for the transmitted type and to translate the data from the local type to the network type.</span></span> <span data-ttu-id="dff66-135">O stub do servidor aloca espaço para o tipo de dados original e chama o *tipo nomeado \* \* \* \_ para \_ local*\* para converter os dados do tipo de rede para o tipo local.</span><span class="sxs-lookup"><span data-stu-id="dff66-135">The server stub allocates space for the original data type and calls *named-type\*\*\*\_to\_local*\* to translate the data from the network type to the local type.</span></span>

<span data-ttu-id="dff66-136">Após o retorno do código do aplicativo, os stubs do cliente e do servidor chamam o *tipo nomeado \* \* \* \_ Free \_ Inst*\* para desalocar o armazenamento para o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="dff66-136">Upon return from the application code, the client and server stubs call *named-type\*\*\*\_free\_inst*\* to deallocate the storage for network type.</span></span> <span data-ttu-id="dff66-137">O stub de cliente chama o *tipo nomeado \* \* \_ \* \_ local \* gratuito* para desalocar o armazenamento retornado pela rotina.</span><span class="sxs-lookup"><span data-stu-id="dff66-137">The client stub calls *named-type\*\*\*\_free\_local*\* to deallocate storage returned by the routine.</span></span>

<span data-ttu-id="dff66-138">Os tipos a seguir não podem ter um atributo " **\[ representar \_ como \]** ":</span><span class="sxs-lookup"><span data-stu-id="dff66-138">The following types cannot have a **\[represent\_as\]** attribute:</span></span>

-   <span data-ttu-id="dff66-139">Matrizes em conformidade, variável ou em conformidade</span><span class="sxs-lookup"><span data-stu-id="dff66-139">Conformant, varying, or conformant-varying arrays</span></span>
-   <span data-ttu-id="dff66-140">Estruturas nas quais o último membro é uma matriz de conformidade (uma estrutura compatível)</span><span class="sxs-lookup"><span data-stu-id="dff66-140">Structures in which the last member is a conformant array (a conformant structure)</span></span>
-   <span data-ttu-id="dff66-141">Ponteiros ou tipos que contêm um ponteiro</span><span class="sxs-lookup"><span data-stu-id="dff66-141">Pointers or types that contain a pointer</span></span>
-   <span data-ttu-id="dff66-142">Pipes ou tipos que contêm pipes</span><span class="sxs-lookup"><span data-stu-id="dff66-142">Pipes or types that contain pipes</span></span>
-   <span data-ttu-id="dff66-143">Tipos que são usados como o tipo base para um pipe</span><span class="sxs-lookup"><span data-stu-id="dff66-143">Types that are used as the base type for a pipe</span></span>
-   <span data-ttu-id="dff66-144">Tipos predefinidos [**manipulam \_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="dff66-144">Predefined types [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>
-   <span data-ttu-id="dff66-145">Tipos que têm o atributo [**\[ Handle \]**](handle.md)</span><span class="sxs-lookup"><span data-stu-id="dff66-145">Types that have the [**\[handle\]**](handle.md) attribute</span></span>

## <a name="examples"></a><span data-ttu-id="dff66-146">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dff66-146">Examples</span></span>

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a><span data-ttu-id="dff66-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="dff66-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff66-148">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="dff66-148">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="dff66-149">**Storage**</span><span class="sxs-lookup"><span data-stu-id="dff66-149">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="dff66-150">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="dff66-150">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="dff66-151">**lidar com \_ t**</span><span class="sxs-lookup"><span data-stu-id="dff66-151">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="dff66-152">**typedef**</span><span class="sxs-lookup"><span data-stu-id="dff66-152">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="dff66-153">**void**</span><span class="sxs-lookup"><span data-stu-id="dff66-153">**void**</span></span>](void.md)
</dt> </dl>

 

 




