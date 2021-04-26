---
description: Define o prefixo a ser usado no código gerado para nomes de macros no namespace.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998743"
---
# <a name="macroprefix-element"></a><span data-ttu-id="94922-103">elemento macroPrefix</span><span class="sxs-lookup"><span data-stu-id="94922-103">macroPrefix element</span></span>

<span data-ttu-id="94922-104">Define o prefixo a ser usado no código gerado para nomes de macros no namespace.</span><span class="sxs-lookup"><span data-stu-id="94922-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="94922-105">Uso</span><span class="sxs-lookup"><span data-stu-id="94922-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="94922-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="94922-106">Attributes</span></span>

<span data-ttu-id="94922-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="94922-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="94922-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="94922-108">Child elements</span></span>

<span data-ttu-id="94922-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="94922-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="94922-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="94922-110">Parent elements</span></span>



| <span data-ttu-id="94922-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="94922-111">Element</span></span>                                   | <span data-ttu-id="94922-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="94922-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="94922-113">**nameSpace**</span><span class="sxs-lookup"><span data-stu-id="94922-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="94922-114">Um namespace a ser usado para geração de código.</span><span class="sxs-lookup"><span data-stu-id="94922-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="94922-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="94922-115">Remarks</span></span>

<span data-ttu-id="94922-116">Esse elemento substitui o prefixo de URI padrão usado para macros geradas.</span><span class="sxs-lookup"><span data-stu-id="94922-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="94922-117">Por exemplo, se o prefixo da macro for "AV \_ " e o nome for "TUNER", a macro gerada para o nome qualificado será " \_ sintonizador de AV".</span><span class="sxs-lookup"><span data-stu-id="94922-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="94922-118">Por padrão, o código gerado cria um prefixo de macro preferencial a partir do URI.</span><span class="sxs-lookup"><span data-stu-id="94922-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="94922-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="94922-119">Element information</span></span>



| <span data-ttu-id="94922-120">Label</span><span class="sxs-lookup"><span data-stu-id="94922-120">Label</span></span> | <span data-ttu-id="94922-121">Valor</span><span class="sxs-lookup"><span data-stu-id="94922-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="94922-122">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94922-122">Minimum supported system</span></span><br/> | <span data-ttu-id="94922-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94922-123">Windows Vista</span></span> |
| <span data-ttu-id="94922-124">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="94922-124">Can be empty</span></span>                        | <span data-ttu-id="94922-125">Sim</span><span class="sxs-lookup"><span data-stu-id="94922-125">Yes</span></span>           |



 

 




