---
description: Gera funções para criar proxies tipados.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768212"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="8be63-103">elemento proxyBuilderImplementations</span><span class="sxs-lookup"><span data-stu-id="8be63-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="8be63-104">Gera funções para criar proxies tipados.</span><span class="sxs-lookup"><span data-stu-id="8be63-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="8be63-105">Uso</span><span class="sxs-lookup"><span data-stu-id="8be63-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="8be63-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8be63-106">Attributes</span></span>

<span data-ttu-id="8be63-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="8be63-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8be63-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8be63-108">Child elements</span></span>



| <span data-ttu-id="8be63-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="8be63-109">Element</span></span>                                     | <span data-ttu-id="8be63-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8be63-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8be63-111">**Codinome**</span><span class="sxs-lookup"><span data-stu-id="8be63-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="8be63-112">O nome a ser usado para o tipo de porta no código gerado.</span><span class="sxs-lookup"><span data-stu-id="8be63-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="8be63-113">Por padrão, o nome do código é gerado a partir do nome qualificado do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="8be63-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="8be63-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="8be63-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="8be63-115">Tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="8be63-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="8be63-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="8be63-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="8be63-117">Nome da classe a ser gerada a partir da função do construtor de proxy.</span><span class="sxs-lookup"><span data-stu-id="8be63-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="8be63-118">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="8be63-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="8be63-119">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8be63-119">Parent elements</span></span>



| <span data-ttu-id="8be63-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="8be63-120">Element</span></span>                         | <span data-ttu-id="8be63-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="8be63-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8be63-122">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="8be63-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8be63-123">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="8be63-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="8be63-124">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8be63-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="8be63-125">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8be63-125">Minimum supported system</span></span><br/> | <span data-ttu-id="8be63-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8be63-126">Windows Vista</span></span> |
| <span data-ttu-id="8be63-127">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="8be63-127">Can be empty</span></span>                        | <span data-ttu-id="8be63-128">Não</span><span class="sxs-lookup"><span data-stu-id="8be63-128">No</span></span>            |



 

 




