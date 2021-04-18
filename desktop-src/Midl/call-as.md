---
title: Atributo call_as
description: O atributo \ Call \_ as \ permite mapear uma função que não pode ser chamada remotamente a uma função remota.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as do atributo MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105749809"
---
# <a name="call_as-attribute"></a><span data-ttu-id="807dd-104">chamar \_ como atributo</span><span class="sxs-lookup"><span data-stu-id="807dd-104">call\_as attribute</span></span>

<span data-ttu-id="807dd-105">O atributo **\[ Call \_ \]** as permite mapear uma função que não pode ser chamada remotamente a uma função remota.</span><span class="sxs-lookup"><span data-stu-id="807dd-105">The **\[call\_as\]** attribute enables you to map a function that cannot be called remotely to a remote function.</span></span>

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a><span data-ttu-id="807dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="807dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="807dd-107">*proc local*</span><span class="sxs-lookup"><span data-stu-id="807dd-107">*local-proc*</span></span> 
</dt> <dd>

<span data-ttu-id="807dd-108">Especifica uma rotina definida pela operação.</span><span class="sxs-lookup"><span data-stu-id="807dd-108">Specifies an operation-defined routine.</span></span>

</dd> <dt>

<span data-ttu-id="807dd-109">*Operation-atributo-List*</span><span class="sxs-lookup"><span data-stu-id="807dd-109">*operation-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="807dd-110">Especifica um ou mais atributos que se aplicam à operação.</span><span class="sxs-lookup"><span data-stu-id="807dd-110">Specifies one or more attributes that apply to the operation.</span></span> <span data-ttu-id="807dd-111">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="807dd-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="807dd-112">*nome da operação*</span><span class="sxs-lookup"><span data-stu-id="807dd-112">*operation-name*</span></span> 
</dt> <dd>

<span data-ttu-id="807dd-113">Especifica a operação nomeada apresentada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="807dd-113">Specifies the named operation presented to the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="807dd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="807dd-114">Remarks</span></span>

<span data-ttu-id="807dd-115">A capacidade de mapear uma função que não pode ser chamada remotamente a uma função remota é particularmente útil em interfaces que têm inúmeros tipos de parâmetro que não podem ser transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="807dd-115">The ability to map a function that cannot be called remotely to a remote function is particularly helpful in interfaces that have numerous parameter types that cannot be transmitted across the network.</span></span> <span data-ttu-id="807dd-116">Em vez de usar muitos **\[** [**representações \_ como**](represent-as.md) **\]** e **\[** [**transmitir \_ como**](transmit-as.md) **\]** tipos, você pode combinar todas as conversões usando **\[ Call \_ as \]** rotinas.</span><span class="sxs-lookup"><span data-stu-id="807dd-116">Rather than using many **\[**[**represent\_as**](represent-as.md)**\]** and **\[**[**transmit\_as**](transmit-as.md)**\]** types, you can combine all the conversions using **\[call\_as\]** routines.</span></span> <span data-ttu-id="807dd-117">Você fornece as duas **\[ chamadas \_ como \]** rotinas (lado do cliente e servidor) para associar a rotina entre as chamadas de aplicativo e as chamadas remotas.</span><span class="sxs-lookup"><span data-stu-id="807dd-117">You supply the two **\[call\_as\]** routines (client side and server side) to bind the routine between the application calls and the remote calls.</span></span>

<span data-ttu-id="807dd-118">O atributo **\[ Call \_ \]** as pode ser usado para interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="807dd-118">The **\[call\_as\]** attribute can be used for object interfaces.</span></span> <span data-ttu-id="807dd-119">Nesse caso, a definição de interface pode ser usada para chamadas locais, bem como chamadas remotas, porque a **\[ chamada \_ \]** permite que uma interface que não pode ser acessada remotamente seja mapeada de forma transparente para uma interface remota.</span><span class="sxs-lookup"><span data-stu-id="807dd-119">In this case, the interface definition can be used for local calls as well as remote calls because **\[call\_as\]** allows an interface that can't be accessed remotely to be transparently mapped to a remote interface.</span></span> <span data-ttu-id="807dd-120">O atributo **\[ Call \_ \]** as não pode ser usado com o modo [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="807dd-120">The **\[call\_as\]** attribute cannot be used with [**/osf**](-osf.md) mode.</span></span>

<span data-ttu-id="807dd-121">Por exemplo, suponha que a rotina **F1** na interface de objeto **IFace** exige várias conversões entre as chamadas de usuário e o que realmente é transmitido.</span><span class="sxs-lookup"><span data-stu-id="807dd-121">For example, assume that the routine **f1** in object interface **IFace** requires numerous conversions between the user calls and what is actually transmitted.</span></span> <span data-ttu-id="807dd-122">Os exemplos a seguir descrevem os arquivos IDL e ACF para a interface **IFace**:</span><span class="sxs-lookup"><span data-stu-id="807dd-122">The following examples describe the IDL and ACF files for interface **IFace**:</span></span>

<span data-ttu-id="807dd-123">No arquivo IDL para a interface **IFace**:</span><span class="sxs-lookup"><span data-stu-id="807dd-123">In the IDL file for interface **IFace**:</span></span>

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

<span data-ttu-id="807dd-124">No ACF para a interface **IFace**:</span><span class="sxs-lookup"><span data-stu-id="807dd-124">In the ACF for interface **IFace**:</span></span>

``` syntax
[call_as( f1 )] Remf1();
```

<span data-ttu-id="807dd-125">Isso faz com que o arquivo de cabeçalho gerado defina a interface usando a definição de **F1**, ainda que também forneça stubs para **Remf1**.</span><span class="sxs-lookup"><span data-stu-id="807dd-125">This causes the generated header file to define the interface using the definition of **f1**, yet it also provides stubs for **Remf1**.</span></span>

<span data-ttu-id="807dd-126">O compilador MIDL irá gerar a seguinte vtable no arquivo de cabeçalho para a interface **IFace**:</span><span class="sxs-lookup"><span data-stu-id="807dd-126">The MIDL compiler will generate the following Vtable in the header file for interface **IFace**:</span></span>

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

<span data-ttu-id="807dd-127">O proxy do lado do cliente teria um proxy típico gerado por MIDL para **Remf1**, enquanto o stub do lado do servidor para **Remf1** seria igual ao stub típico gerado por MIDL:</span><span class="sxs-lookup"><span data-stu-id="807dd-127">The client-side proxy would then have a typical MIDL-generated proxy for **Remf1**, while the server side stub for **Remf1** would be the same as the typical MIDL-generated stub:</span></span>

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

<span data-ttu-id="807dd-128">Em seguida, as duas **\[ chamadas \_ como \]** rotinas de acoplamento (lado do cliente e servidor) devem ser codificadas manualmente:</span><span class="sxs-lookup"><span data-stu-id="807dd-128">Then, the two **\[call\_as\]** bond routines (client side and server side) must be manually coded:</span></span>

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

<span data-ttu-id="807dd-129">Para interfaces de objeto, esses são os protótipos para as rotinas de acoplamento.</span><span class="sxs-lookup"><span data-stu-id="807dd-129">For object interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="807dd-130">Para o lado do cliente:</span><span class="sxs-lookup"><span data-stu-id="807dd-130">For client side:</span></span>

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

<span data-ttu-id="807dd-131">Para o lado do servidor:</span><span class="sxs-lookup"><span data-stu-id="807dd-131">For server side:</span></span>

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

<span data-ttu-id="807dd-132">Para interfaces que não são de objeto, esses são os protótipos para as rotinas de acoplamento.</span><span class="sxs-lookup"><span data-stu-id="807dd-132">For nonobject interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="807dd-133">Para o lado do cliente:</span><span class="sxs-lookup"><span data-stu-id="807dd-133">For client side:</span></span>

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

<span data-ttu-id="807dd-134">Para o lado do servidor:</span><span class="sxs-lookup"><span data-stu-id="807dd-134">For server side:</span></span>

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a><span data-ttu-id="807dd-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="807dd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="807dd-136">**/osf**</span><span class="sxs-lookup"><span data-stu-id="807dd-136">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="807dd-137">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="807dd-137">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="807dd-138">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="807dd-138">**transmit\_as**</span></span>](transmit-as.md)
</dt> </dl>

 

 




