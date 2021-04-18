---
description: Gera definições de estrutura C para tipos conhecidos.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780277"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="18912-103">elemento structDefinitions</span><span class="sxs-lookup"><span data-stu-id="18912-103">structDefinitions element</span></span>

<span data-ttu-id="18912-104">Gera definições de estrutura C para tipos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="18912-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="18912-105">Uso</span><span class="sxs-lookup"><span data-stu-id="18912-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="18912-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="18912-106">Attributes</span></span>

<span data-ttu-id="18912-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="18912-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="18912-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="18912-108">Child elements</span></span>

<span data-ttu-id="18912-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="18912-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="18912-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="18912-110">Parent elements</span></span>



| <span data-ttu-id="18912-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="18912-111">Element</span></span>                         | <span data-ttu-id="18912-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="18912-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="18912-113">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="18912-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="18912-114">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="18912-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="18912-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="18912-115">Remarks</span></span>

<span data-ttu-id="18912-116">Estruturas para tipos conhecidos são referenciadas por grande parte do código gerado e pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18912-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="18912-117">Esse elemento é usado para gerar arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="18912-117">This element is used to generate include files.</span></span> <span data-ttu-id="18912-118">Esse elemento deve ocorrer após um elemento [**structDeclarations**](structdeclarations.md) para que as referências entre as estruturas sejam manipuladas corretamente.</span><span class="sxs-lookup"><span data-stu-id="18912-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="18912-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="18912-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="18912-120">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18912-120">Minimum supported system</span></span><br/> | <span data-ttu-id="18912-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18912-121">Windows Vista</span></span> |
| <span data-ttu-id="18912-122">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="18912-122">Can be empty</span></span>                        | <span data-ttu-id="18912-123">Sim</span><span class="sxs-lookup"><span data-stu-id="18912-123">Yes</span></span>           |



 

 




