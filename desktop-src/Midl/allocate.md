---
title: alocar atributo
description: O atributo \ Allocate \ ACF permite que você personalize a alocação de memória e a desalocação de um tipo definido no arquivo IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- alocar o atributo MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823195"
---
# <a name="allocate-attribute"></a><span data-ttu-id="56b3a-104">alocar atributo</span><span class="sxs-lookup"><span data-stu-id="56b3a-104">allocate attribute</span></span>

<span data-ttu-id="56b3a-105">O atributo **\[ ALLOCATE \]** ACF permite que você personalize a alocação de memória e a desalocação de um tipo definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="56b3a-105">The **\[allocate\]** ACF attribute lets you customize memory allocation and deallocation for a type defined in the IDL file.</span></span>

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="56b3a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56b3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b3a-107">*lista de opções de alocação*</span><span class="sxs-lookup"><span data-stu-id="56b3a-107">*allocate-option-list*</span></span> 
</dt> <dd>

<span data-ttu-id="56b3a-108">Especifica uma ou mais opções de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="56b3a-108">Specifies one or more memory-allocation options.</span></span> <span data-ttu-id="56b3a-109">Selecione um dos nós **únicos \_** ou **todos, \_** ou uma das opções **gratuito** ou **não \_ livre**, ou um de cada par.</span><span class="sxs-lookup"><span data-stu-id="56b3a-109">Select one of either **single\_node** or **all\_nodes**, or one of either **free** or **dont\_free**, or one from each pair.</span></span> <span data-ttu-id="56b3a-110">Quando você especificar mais de uma opção, separe as opções com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="56b3a-110">When you specify more than one option, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="56b3a-111">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="56b3a-111">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="56b3a-112">Especifica outros atributos de tipo ACF opcionais.</span><span class="sxs-lookup"><span data-stu-id="56b3a-112">Specifies other optional ACF-type attributes.</span></span> <span data-ttu-id="56b3a-113">Quando você especificar mais de um atributo de tipo, separe as opções com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="56b3a-113">When you specify more than one type attribute, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="56b3a-114">*nome do tipo*</span><span class="sxs-lookup"><span data-stu-id="56b3a-114">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="56b3a-115">Especifica um tipo definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="56b3a-115">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56b3a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="56b3a-116">Remarks</span></span>

<span data-ttu-id="56b3a-117">O atributo **\[ ALLOCATE \]** tem as seguintes opções válidas.</span><span class="sxs-lookup"><span data-stu-id="56b3a-117">The **\[allocate\]** attribute has the following valid options.</span></span>



| <span data-ttu-id="56b3a-118">Opção</span><span class="sxs-lookup"><span data-stu-id="56b3a-118">Option</span></span>           | <span data-ttu-id="56b3a-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="56b3a-119">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="56b3a-120">**todos os \_ nós**</span><span class="sxs-lookup"><span data-stu-id="56b3a-120">**all\_nodes**</span></span>   | <span data-ttu-id="56b3a-121">Faz uma chamada para alocar e liberar memória para todos os nós.</span><span class="sxs-lookup"><span data-stu-id="56b3a-121">Makes one call to allocate and free memory for all nodes.</span></span>             |
| <span data-ttu-id="56b3a-122">**\_nó único**</span><span class="sxs-lookup"><span data-stu-id="56b3a-122">**single\_node**</span></span> | <span data-ttu-id="56b3a-123">Faz muitas chamadas individuais para alocar e liberar cada nó de memória.</span><span class="sxs-lookup"><span data-stu-id="56b3a-123">Makes many individual calls to allocate and free each node of memory.</span></span> |
| <span data-ttu-id="56b3a-124">**gratuito**</span><span class="sxs-lookup"><span data-stu-id="56b3a-124">**free**</span></span>         | <span data-ttu-id="56b3a-125">Libera memória no retorno do stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="56b3a-125">Frees memory on return from the server stub.</span></span>                          |
| <span data-ttu-id="56b3a-126">**Não \_ livre**</span><span class="sxs-lookup"><span data-stu-id="56b3a-126">**dont\_free**</span></span>   | <span data-ttu-id="56b3a-127">Não libera memória no retorno do stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="56b3a-127">Does not free memory on return from the server stub.</span></span>                  |



 

<span data-ttu-id="56b3a-128">Por padrão, os stubs podem alocar armazenamento para dados referenciados por um ponteiro exclusivo ou completo chamando o [**usuário de MIDL \_ \_**](midl-user-allocate-1.md) e o [**usuário de MIDL \_ \_ gratuito**](midl-user-free-1.md) individualmente para cada ponteiro.</span><span class="sxs-lookup"><span data-stu-id="56b3a-128">By default, the stubs may allocate storage for data referenced by a unique or full pointer by calling [**midl\_user\_allocate**](midl-user-allocate-1.md) and [**midl\_user\_free**](midl-user-free-1.md) individually for each pointer.</span></span>

<span data-ttu-id="56b3a-129">Você pode otimizar a velocidade do seu aplicativo especificando a opção **todos os \_ nós**.</span><span class="sxs-lookup"><span data-stu-id="56b3a-129">You can optimize the speed of your application by specifying the option **all\_nodes**.</span></span> <span data-ttu-id="56b3a-130">Essa opção direciona o stub para computar o tamanho de toda a memória referenciada por meio do ponteiro do tipo especificado e fazer uma única chamada para o [**usuário de MIDL \_ \_ alocar**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="56b3a-130">This option directs the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span> <span data-ttu-id="56b3a-131">O stub libera a memória fazendo uma chamada para o [**\_ usuário MIDL \_ gratuitamente**](midl-user-free-1.md).</span><span class="sxs-lookup"><span data-stu-id="56b3a-131">The stub releases the memory by making one call to [**midl\_user\_free**](midl-user-free-1.md).</span></span>

<span data-ttu-id="56b3a-132">A opção **não \_ livre** DIRECIONA o compilador MIDL para gerar um stub de servidor que não chama o [**\_ usuário MIDL \_ livre**](midl-user-free-1.md) para o tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="56b3a-132">The **dont\_free** option directs the MIDL compiler to generate a server stub that does not call [**midl\_user\_free**](midl-user-free-1.md) for the specified type.</span></span> <span data-ttu-id="56b3a-133">A opção **não \_ livre** permite que as estruturas de ponteiro permaneçam acessíveis para o aplicativo de servidor após a chamada de procedimento remoto ser concluída e retornada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="56b3a-133">The **dont\_free** option allows the pointer structures to remain accessible to the server application after the remote procedure call has completed and returned to the client.</span></span>

<span data-ttu-id="56b3a-134">O atributo **\[ ALLOCATE \]** causará qualquer parâmetro **\[ in \] , out** que seja um ponteiro para um tipo qualificado com a opção **todos os \_ nós** para realocar a memória quando os dados forem desempacotados.</span><span class="sxs-lookup"><span data-stu-id="56b3a-134">The **\[allocate\]** attribute will cause any **\[in, out\]** parameter that is a pointer to a type qualified with the **all\_nodes** option to reallocate memory when the data is unmarshaled.</span></span> <span data-ttu-id="56b3a-135">É responsabilidade do aplicativo liberar a memória alocada anteriormente para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="56b3a-135">It is the responsibility of the application to free the memory allocated previously for this parameter.</span></span> <span data-ttu-id="56b3a-136">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="56b3a-136">For example:</span></span>

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

<span data-ttu-id="56b3a-137">O tipo de dados PTHISTYPE será realocado na direção de [**\[ saída \]**](out-idl.md) pelo stub antes do desempacotamento.</span><span class="sxs-lookup"><span data-stu-id="56b3a-137">The data type PTHISTYPE will be reallocated in the [**\[out\]**](out-idl.md) direction by the stub before unmarshaling.</span></span> <span data-ttu-id="56b3a-138">Portanto, o aplicativo deve liberar a memória alocada anteriormente para os dados desse parâmetro ou ocorrerá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="56b3a-138">Therefore, the application must free the memory it previously allocated for this parameter's data, or a memory leak will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="56b3a-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="56b3a-139">Examples</span></span>

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a><span data-ttu-id="56b3a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="56b3a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b3a-141">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="56b3a-141">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="56b3a-142">**no**</span><span class="sxs-lookup"><span data-stu-id="56b3a-142">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="56b3a-143">**\_alocar usuário de MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="56b3a-143">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="56b3a-144">**usuário de MIDL \_ \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="56b3a-144">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="56b3a-145">**fora**</span><span class="sxs-lookup"><span data-stu-id="56b3a-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="56b3a-146">**typedef**</span><span class="sxs-lookup"><span data-stu-id="56b3a-146">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




