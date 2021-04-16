---
title: atributo vararg
description: O atributo \ vararg \ especifica que a função usa um número variável de parâmetros. Para fazer isso, o último parâmetro deve ser uma matriz segura de tipo VARIANT que contém todos os parâmetros restantes.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- atributo vararg MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105751213"
---
# <a name="vararg-attribute"></a><span data-ttu-id="578f8-105">atributo vararg</span><span class="sxs-lookup"><span data-stu-id="578f8-105">vararg attribute</span></span>

<span data-ttu-id="578f8-106">O atributo **\[ vararg \]** especifica que a função usa um número variável de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="578f8-106">The **\[vararg\]** attribute specifies that the function takes a variable number of parameters.</span></span> <span data-ttu-id="578f8-107">Para fazer isso, o último parâmetro deve ser uma matriz segura de tipo **Variant** que contém todos os parâmetros restantes.</span><span class="sxs-lookup"><span data-stu-id="578f8-107">To accomplish this, the last parameter must be a safe array of **VARIANT** type that contains all the remaining parameters.</span></span>

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a><span data-ttu-id="578f8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="578f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="578f8-109">*opcional-atributos*</span><span class="sxs-lookup"><span data-stu-id="578f8-109">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="578f8-110">Especifica zero ou mais atributos a serem aplicados à função.</span><span class="sxs-lookup"><span data-stu-id="578f8-110">Specifies zero or more attributes to be applied to the function.</span></span> <span data-ttu-id="578f8-111">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="578f8-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="578f8-112">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="578f8-112">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="578f8-113">O tipo dos dados retornados pelo procedimento remoto após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="578f8-113">The type of the data returned by the remote procedure upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="578f8-114">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="578f8-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="578f8-115">O nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="578f8-115">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="578f8-116">*Optional-parâmetros-atributos*</span><span class="sxs-lookup"><span data-stu-id="578f8-116">*optional-param-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="578f8-117">Especifica zero ou mais atributos a serem aplicados ao parâmetro de função imediatamente após a listagem de atributos.</span><span class="sxs-lookup"><span data-stu-id="578f8-117">Specifies zero or more attributes to be applied to the function parameter immediately following the attribute listing.</span></span>

</dd> <dt>

<span data-ttu-id="578f8-118">*parâmetro-lista*</span><span class="sxs-lookup"><span data-stu-id="578f8-118">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="578f8-119">Especifica todos os parâmetros, salve o parâmetro final, variável,.</span><span class="sxs-lookup"><span data-stu-id="578f8-119">Specifies all the parameters, save the final, varying, parameter.</span></span>

</dd> <dt>

<span data-ttu-id="578f8-120">*Last-param-Name*</span><span class="sxs-lookup"><span data-stu-id="578f8-120">*last-param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="578f8-121">O nome do parâmetro variável.</span><span class="sxs-lookup"><span data-stu-id="578f8-121">The name of the varying parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="578f8-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="578f8-122">Remarks</span></span>

<span data-ttu-id="578f8-123">Você não pode aplicar os **\[** [](optional.md) **\]** atributos Optional ou **\[** [**DefaultValue**](defaultvalue.md) **\]** a quaisquer parâmetros em uma função que tenha o atributo **\[ vararg \]** .</span><span class="sxs-lookup"><span data-stu-id="578f8-123">You cannot apply the **\[**[**optional**](optional.md)**\]** or **\[**[**defaultvalue**](defaultvalue.md)**\]** attributes to any parameters in a function that has the **\[vararg\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="578f8-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="578f8-124">Examples</span></span>

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a><span data-ttu-id="578f8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="578f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578f8-126">**ValorPadrão**</span><span class="sxs-lookup"><span data-stu-id="578f8-126">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="578f8-127">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="578f8-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="578f8-128">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="578f8-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="578f8-129">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="578f8-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="578f8-130">**adicional**</span><span class="sxs-lookup"><span data-stu-id="578f8-130">**optional**</span></span>](optional.md)
</dt> </dl>

 

 