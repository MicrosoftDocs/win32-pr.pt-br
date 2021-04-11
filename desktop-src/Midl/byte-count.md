---
title: byte_count atributo
description: O atributo \ contagem de \ bytes \_ \ ACF é um atributo de parâmetro que associa um tamanho, em bytes, à área de memória indicada pelo ponteiro.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count do atributo MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293296"
---
# <a name="byte_count-attribute"></a><span data-ttu-id="65c29-104">atributo de contagem de bytes \_</span><span class="sxs-lookup"><span data-stu-id="65c29-104">byte\_count attribute</span></span>

<span data-ttu-id="65c29-105">O atributo ACF de **\[ \_ contagem \] de bytes** é um atributo de parâmetro que associa um tamanho, em bytes, à área de memória indicada pelo ponteiro.</span><span class="sxs-lookup"><span data-stu-id="65c29-105">The **\[byte\_count\]** ACF attribute is a parameter attribute that associates a size, in bytes, with the memory area indicated by the pointer.</span></span>

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a><span data-ttu-id="65c29-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65c29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c29-107">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="65c29-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="65c29-108">Especifica zero ou mais atributos de função de ACF.</span><span class="sxs-lookup"><span data-stu-id="65c29-108">Specifies zero or more ACF function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="65c29-109">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="65c29-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65c29-110">Especifica o nome da função definida no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="65c29-110">Specifies the name of the function defined in the IDL file.</span></span> <span data-ttu-id="65c29-111">O nome da função é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="65c29-111">The function name is required.</span></span>

</dd> <dt>

<span data-ttu-id="65c29-112">*nome-variável de comprimento*</span><span class="sxs-lookup"><span data-stu-id="65c29-112">*length-variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65c29-113">Especifica o nome do parâmetro [**\[ em \]**](in.md)apenas que especifica o tamanho, em bytes, da área de memória referenciada pelo *nome do parâmetro*.</span><span class="sxs-lookup"><span data-stu-id="65c29-113">Specifies the name of the [**\[in\]**](in.md)-only parameter that specifies the size, in bytes, of the memory area referenced by *parameter-name*.</span></span>

</dd> <dt>

<span data-ttu-id="65c29-114">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="65c29-114">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65c29-115">Especifica o nome do parâmetro de ponteiro somente [**\[ out \]**](out-idl.md)definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="65c29-115">Specifies the name of the [**\[out\]**](out-idl.md)-only pointer parameter defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65c29-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="65c29-116">Remarks</span></span>

<span data-ttu-id="65c29-117">A **\[ \_ contagem \] de bytes** do atributo ACF representa uma extensão da Microsoft para o DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="65c29-117">The ACF attribute **\[byte\_count\]** represents a Microsoft extension to DCE IDL.</span></span> <span data-ttu-id="65c29-118">Portanto, esse atributo não está disponível quando você usa o switch do compilador MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="65c29-118">Therefore, this attribute is not available when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

> [!Note]  
> <span data-ttu-id="65c29-119">Não há mais suporte para o atributo **\[ contagem \] de bytes** na sintaxe NDR64 devido à dificuldade de estimar o tamanho necessário para todos os parâmetros de [**\[ saída \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="65c29-119">The **\[byte count\]** attribute is no longer supported in NDR64 syntax due to the difficulty in estimating the size required for all [**\[out\]**](out-idl.md) parameters.</span></span>

 

<span data-ttu-id="65c29-120">A memória referenciada pelo parâmetro Pointer é contígua e não é alocada ou liberada pelos stubs do cliente.</span><span class="sxs-lookup"><span data-stu-id="65c29-120">Memory referenced by the pointer parameter is contiguous and is not allocated or freed by the client stubs.</span></span> <span data-ttu-id="65c29-121">Esse recurso do atributo **\[ \_ contagem \] de bytes** permite que você crie uma área de buffer persistente na memória do cliente que pode ser reutilizada durante mais de uma chamada para o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="65c29-121">This feature of the **\[byte\_count\]** attribute lets you create a persistent buffer area in client memory that can be reused during more than one call to the remote procedure.</span></span>

<span data-ttu-id="65c29-122">A capacidade de desativar a alocação de memória de stub de cliente permite que você ajuste o aplicativo para ter eficiência.</span><span class="sxs-lookup"><span data-stu-id="65c29-122">The ability to turn off the client stub memory allocation lets you tune the application for efficiency.</span></span> <span data-ttu-id="65c29-123">Por exemplo, o atributo **\[ \_ contagem \] de bytes** pode ser usado por funções de provedor de serviço que usam o Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="65c29-123">For example, the **\[byte\_count\]** attribute can be used by service-provider functions that use Microsoft RPC.</span></span> <span data-ttu-id="65c29-124">Quando um aplicativo de usuário chama a API do provedor de serviço e envia um ponteiro para um buffer, o provedor de serviços pode passar o ponteiro de buffer para a função remota.</span><span class="sxs-lookup"><span data-stu-id="65c29-124">When a user application calls the service-provider API and sends a pointer to a buffer, the service provider can pass the buffer pointer on to the remote function.</span></span> <span data-ttu-id="65c29-125">O provedor de serviços pode reutilizar o buffer durante várias chamadas remotas sem forçar o usuário a realocar a área de memória.</span><span class="sxs-lookup"><span data-stu-id="65c29-125">The service provider can reuse the buffer during multiple remote calls without forcing the user to reallocate the memory area.</span></span>

<span data-ttu-id="65c29-126">A área memória pode conter estruturas de dados complexas que consistem em vários ponteiros.</span><span class="sxs-lookup"><span data-stu-id="65c29-126">The memory area can contain complex data structures that consist of multiple pointers.</span></span> <span data-ttu-id="65c29-127">Como a área de memória é contígua, o aplicativo não precisa fazer várias chamadas para liberar individualmente cada ponteiro e estrutura.</span><span class="sxs-lookup"><span data-stu-id="65c29-127">Because the memory area is contiguous, the application does not have to make several calls to individually free each pointer and structure.</span></span> <span data-ttu-id="65c29-128">Em vez disso, ele pode alocar ou liberar a área de memória com uma chamada para a alocação de memória ou a rotina gratuita.</span><span class="sxs-lookup"><span data-stu-id="65c29-128">Instead, it can allocate or free the memory area with one call to the memory allocation or free routine.</span></span>

<span data-ttu-id="65c29-129">O buffer deve ser um parâmetro somente [**\[ out \]**](out-idl.md), enquanto o comprimento do buffer em bytes deve ser um parâmetro somente [**\[ no \]**](in.md).</span><span class="sxs-lookup"><span data-stu-id="65c29-129">The buffer must be an [**\[out\]**](out-idl.md)-only parameter, while the buffer length in bytes must be an [**\[in\]**](in.md)-only parameter.</span></span>

<span data-ttu-id="65c29-130">Especifique um buffer que seja grande o suficiente para conter todos os parâmetros de [**\[ saída \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="65c29-130">Specify a buffer that is large enough to contain all the [**\[out\]**](out-idl.md) parameters.</span></span> <span data-ttu-id="65c29-131">Devido ao preenchimento oculto, use estimativas em vez de contagens exatas.</span><span class="sxs-lookup"><span data-stu-id="65c29-131">Because of hidden padding, use overestimates rather than exact counts.</span></span> <span data-ttu-id="65c29-132">Por exemplo, ponteiros de 4 bytes não são empacotados em um limite alinhado de 4 bytes em plataformas de 32 bits e ponteiros de 8 bytes em um limite de 8 bytes em plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="65c29-132">For example, 4-byte pointers are unmarshaled on a 4-byte aligned boundary on 32-bit platforms and 8-byte pointers on an 8-byte boundary on 64-bit platforms.</span></span> <span data-ttu-id="65c29-133">Portanto, o preenchimento de alinhamento que os stubs executará deve ser contabilizado no espaço para o buffer.</span><span class="sxs-lookup"><span data-stu-id="65c29-133">Therefore, the alignment padding the stubs will perform must be accounted for in the space for the buffer.</span></span> <span data-ttu-id="65c29-134">Além disso, os níveis de embalagem usados durante a compilação de linguagem C podem variar.</span><span class="sxs-lookup"><span data-stu-id="65c29-134">In addition, packing levels used during C-language compilation can vary.</span></span> <span data-ttu-id="65c29-135">Use um valor de contagem de bytes que leva em conta os bytes de empacotamento adicionais adicionados para o nível de embalagem usado durante a compilação em linguagem C.</span><span class="sxs-lookup"><span data-stu-id="65c29-135">Use a byte count value that accounts for additional packing bytes added for the packing level used during C-language compilation.</span></span> <span data-ttu-id="65c29-136">Uma prática segura que abrange plataformas de 32 bits e plataformas de 64 bits é assumir que cada objeto que entra no bloco de memória grande começa em um endereço que é um múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="65c29-136">A safe practice that covers both 32 bit platforms and 64 bit platforms is to assume that each object going into the big memory block starts at an address that is a multiple of 8.</span></span>

## <a name="examples"></a><span data-ttu-id="65c29-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65c29-137">Examples</span></span>

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a><span data-ttu-id="65c29-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="65c29-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c29-139">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="65c29-139">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="65c29-140">**no**</span><span class="sxs-lookup"><span data-stu-id="65c29-140">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="65c29-141">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="65c29-141">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="65c29-142">**/osf**</span><span class="sxs-lookup"><span data-stu-id="65c29-142">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="65c29-143">**fora**</span><span class="sxs-lookup"><span data-stu-id="65c29-143">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="65c29-144">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="65c29-144">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 




