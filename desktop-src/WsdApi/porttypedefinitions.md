---
description: Gera constantes C para tipos de porta.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff073eb7b0f9cbc4b0b6df87c8f9fc84d4f62882
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996543"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="e28d1-103">elemento portTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="e28d1-103">portTypeDefinitions element</span></span>

<span data-ttu-id="e28d1-104">Gera constantes C para tipos de porta.</span><span class="sxs-lookup"><span data-stu-id="e28d1-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="e28d1-105">Uso</span><span class="sxs-lookup"><span data-stu-id="e28d1-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="e28d1-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e28d1-106">Attributes</span></span>

<span data-ttu-id="e28d1-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="e28d1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e28d1-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e28d1-108">Child elements</span></span>



| <span data-ttu-id="e28d1-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e28d1-109">Element</span></span>                                                   | <span data-ttu-id="e28d1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e28d1-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e28d1-111">**Codinome**</span><span class="sxs-lookup"><span data-stu-id="e28d1-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="e28d1-112">Especifica o nome a ser usado para o tipo de porta no código gerado.</span><span class="sxs-lookup"><span data-stu-id="e28d1-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="e28d1-113">Por padrão, o nome do código é gerado a partir do nome qualificado do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="e28d1-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="e28d1-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="e28d1-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="e28d1-115">Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações de notificação.</span><span class="sxs-lookup"><span data-stu-id="e28d1-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="e28d1-116">**operacional**</span><span class="sxs-lookup"><span data-stu-id="e28d1-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="e28d1-117">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="e28d1-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="e28d1-118">**portType**</span><span class="sxs-lookup"><span data-stu-id="e28d1-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="e28d1-119">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="e28d1-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="e28d1-120">**stubFunction**</span><span class="sxs-lookup"><span data-stu-id="e28d1-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="e28d1-121">Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações unidirecionais e bidirecionais.</span><span class="sxs-lookup"><span data-stu-id="e28d1-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="e28d1-122">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="e28d1-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="e28d1-123">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e28d1-123">Parent elements</span></span>



| <span data-ttu-id="e28d1-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="e28d1-124">Element</span></span>                         | <span data-ttu-id="e28d1-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="e28d1-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e28d1-126">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="e28d1-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e28d1-127">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="e28d1-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e28d1-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e28d1-128">Remarks</span></span>

<span data-ttu-id="e28d1-129">Esse elemento é geralmente usado em arquivos de origem C para fornecer as constantes de tipo de porta declaradas por [**portTypeDeclarations**](porttypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="e28d1-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="e28d1-130">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e28d1-130">Element information</span></span>



| <span data-ttu-id="e28d1-131">Label</span><span class="sxs-lookup"><span data-stu-id="e28d1-131">Label</span></span> | <span data-ttu-id="e28d1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e28d1-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="e28d1-133">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e28d1-133">Minimum supported system</span></span><br/> | <span data-ttu-id="e28d1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e28d1-134">Windows Vista</span></span> |
| <span data-ttu-id="e28d1-135">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="e28d1-135">Can be empty</span></span>                        | <span data-ttu-id="e28d1-136">Sim</span><span class="sxs-lookup"><span data-stu-id="e28d1-136">Yes</span></span>           |



 

 




