---
description: Gera declarações de constante C para tipos de porta.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: elemento portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996553"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="d3704-103">elemento portTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="d3704-103">portTypeDeclarations element</span></span>

<span data-ttu-id="d3704-104">Gera declarações de constante C para tipos de porta.</span><span class="sxs-lookup"><span data-stu-id="d3704-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="d3704-105">Uso</span><span class="sxs-lookup"><span data-stu-id="d3704-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="d3704-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3704-106">Attributes</span></span>

<span data-ttu-id="d3704-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="d3704-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d3704-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d3704-108">Child elements</span></span>



| <span data-ttu-id="d3704-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="d3704-109">Element</span></span>                                   | <span data-ttu-id="d3704-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3704-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3704-111">**Codinome**</span><span class="sxs-lookup"><span data-stu-id="d3704-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="d3704-112">Especifica o nome a ser usado para o tipo de porta no código gerado.</span><span class="sxs-lookup"><span data-stu-id="d3704-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="d3704-113">Por padrão, o nome do código é gerado a partir do nome qualificado do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="d3704-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="d3704-114">**operacional**</span><span class="sxs-lookup"><span data-stu-id="d3704-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="d3704-115">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="d3704-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="d3704-116">**portType**</span><span class="sxs-lookup"><span data-stu-id="d3704-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="d3704-117">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="d3704-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="d3704-118">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="d3704-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="d3704-119">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d3704-119">Parent elements</span></span>



| <span data-ttu-id="d3704-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="d3704-120">Element</span></span>                         | <span data-ttu-id="d3704-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3704-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d3704-122">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="d3704-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d3704-123">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="d3704-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d3704-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3704-124">Remarks</span></span>

<span data-ttu-id="d3704-125">Declarações de tipo de porta são referenciadas pelo aplicativo e grande parte do código gerado.</span><span class="sxs-lookup"><span data-stu-id="d3704-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="d3704-126">Esse elemento é usado para gerar arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="d3704-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="d3704-127">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d3704-127">Element information</span></span>



| <span data-ttu-id="d3704-128">Label</span><span class="sxs-lookup"><span data-stu-id="d3704-128">Label</span></span> | <span data-ttu-id="d3704-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d3704-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d3704-130">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3704-130">Minimum supported system</span></span><br/> | <span data-ttu-id="d3704-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3704-131">Windows Vista</span></span> |
| <span data-ttu-id="d3704-132">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="d3704-132">Can be empty</span></span>                        | <span data-ttu-id="d3704-133">Sim</span><span class="sxs-lookup"><span data-stu-id="d3704-133">Yes</span></span>           |



 

 




