---
description: ICE79 valida as referências a componentes e recursos inseridos nos campos de banco de dados usando o tipo de dado Condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090779"
---
# <a name="ice79"></a><span data-ttu-id="e3439-103">ICE79</span><span class="sxs-lookup"><span data-stu-id="e3439-103">ICE79</span></span>

<span data-ttu-id="e3439-104">ICE79 valida as referências a componentes e recursos inseridos nos campos de banco de dados usando o tipo de dado [Condition](condition.md) .</span><span class="sxs-lookup"><span data-stu-id="e3439-104">ICE79 validates the references to components and features entered in the database fields using the [Condition](condition.md) data type.</span></span>

## <a name="result"></a><span data-ttu-id="e3439-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="e3439-105">Result</span></span>

<span data-ttu-id="e3439-106">ICE79 posta dois avisos.</span><span class="sxs-lookup"><span data-stu-id="e3439-106">ICE79 posts two warnings.</span></span>



| <span data-ttu-id="e3439-107">Aviso de ICE79</span><span class="sxs-lookup"><span data-stu-id="e3439-107">ICE79 warning</span></span>                                                                      | <span data-ttu-id="e3439-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3439-108">Description</span></span>                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e3439-109">A tabela de validação está ausente no banco de dados \_ .</span><span class="sxs-lookup"><span data-stu-id="e3439-109">Database is missing \_Validation table.</span></span> <span data-ttu-id="e3439-110">Não foi possível verificar completamente os nomes das propriedades.</span><span class="sxs-lookup"><span data-stu-id="e3439-110">Could not completely check property names.</span></span> | <span data-ttu-id="e3439-111">A tabela de [ \_ validação](-validation-table.md)está ausente no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e3439-111">Database is missing [\_Validation table](-validation-table.md).</span></span> |
| <span data-ttu-id="e3439-112">Erro ao recuperar valores da coluna \[ 2 \] na tabela \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e3439-112">Error retrieving values from column \[2\] in table \[1\].</span></span> <span data-ttu-id="e3439-113">Ignorando coluna.</span><span class="sxs-lookup"><span data-stu-id="e3439-113">Skipping Column.</span></span>         | <span data-ttu-id="e3439-114">Erro ao recuperar o valor.</span><span class="sxs-lookup"><span data-stu-id="e3439-114">Error retrieving value.</span></span>                                          |



 

<span data-ttu-id="e3439-115">ICE79 posta dois erros.</span><span class="sxs-lookup"><span data-stu-id="e3439-115">ICE79 posts two errors.</span></span>



| <span data-ttu-id="e3439-116">Erro de ICE79</span><span class="sxs-lookup"><span data-stu-id="e3439-116">ICE79 error</span></span>                                                          | <span data-ttu-id="e3439-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3439-117">Description</span></span>                               |
|----------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="e3439-118">Componente '% ls ' referenciado na coluna '% s'. ' % s' da linha% s é inválido.</span><span class="sxs-lookup"><span data-stu-id="e3439-118">Component '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span> | <span data-ttu-id="e3439-119">Uma referência de componente inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="e3439-119">An invalid component reference was found.</span></span> |
| <span data-ttu-id="e3439-120">Recurso '% ls ' referenciado na coluna '% s'. ' % s' da linha% s é inválido.</span><span class="sxs-lookup"><span data-stu-id="e3439-120">Feature '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span>   | <span data-ttu-id="e3439-121">Foi encontrada uma referência de recurso inválida</span><span class="sxs-lookup"><span data-stu-id="e3439-121">An invalid feature reference was found</span></span>    |



 

## <a name="example"></a><span data-ttu-id="e3439-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3439-122">Example</span></span>

<span data-ttu-id="e3439-123">ICE79 relata os seguintes erros para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="e3439-123">ICE79 reports the following errors for the example:</span></span>

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

<span data-ttu-id="e3439-124">Neste exemplo, NoSuchComponent está ausente da tabela de [componentes](component-table.md) e NoSuchFeature está ausente da tabela de [recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e3439-124">In this example, NoSuchComponent is absent from the [Component table](component-table.md) and NoSuchFeature is absent from the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="e3439-125">[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e3439-125">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="e3439-126">Ação</span><span class="sxs-lookup"><span data-stu-id="e3439-126">Action</span></span>  | <span data-ttu-id="e3439-127">Condição</span><span class="sxs-lookup"><span data-stu-id="e3439-127">Condition</span></span>                                |
|---------|------------------------------------------|
| <span data-ttu-id="e3439-128">Personalizado1</span><span class="sxs-lookup"><span data-stu-id="e3439-128">Custom1</span></span> | <span data-ttu-id="e3439-129">TESTaction = 1046 e &NoSuchFeature>2</span><span class="sxs-lookup"><span data-stu-id="e3439-129">TESTACTION=1046 AND &NoSuchFeature>2</span></span>  |
| <span data-ttu-id="e3439-130">Custom2</span><span class="sxs-lookup"><span data-stu-id="e3439-130">Custom2</span></span> | <span data-ttu-id="e3439-131">TESTaction = 146 e $NoSuchComponent>2</span><span class="sxs-lookup"><span data-stu-id="e3439-131">TESTACTION=146 AND $NoSuchComponent>2</span></span> |



 

<span data-ttu-id="e3439-132">Para corrigir esses erros, insira registros válidos para NoSuchFeature e NoSuchComponent nas tabelas de recursos e componentes.</span><span class="sxs-lookup"><span data-stu-id="e3439-132">To fix these errors, enter valid records for NoSuchFeature and NoSuchComponent in the Feature and Component tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3439-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3439-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3439-134">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="e3439-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



