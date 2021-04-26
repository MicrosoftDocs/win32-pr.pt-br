---
description: Gera definições de estrutura C para tipos de mensagem.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: elemento messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a116658fc7ce7f985b7b717c7a7b4ce38be4637
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993663"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="fd524-103">elemento messageStructureDefinitions</span><span class="sxs-lookup"><span data-stu-id="fd524-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="fd524-104">Gera definições de estrutura C para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fd524-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="fd524-105">Uso</span><span class="sxs-lookup"><span data-stu-id="fd524-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="fd524-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="fd524-106">Attributes</span></span>

<span data-ttu-id="fd524-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="fd524-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fd524-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fd524-108">Child elements</span></span>



| <span data-ttu-id="fd524-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd524-109">Element</span></span>                                   | <span data-ttu-id="fd524-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd524-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="fd524-111">**operacional**</span><span class="sxs-lookup"><span data-stu-id="fd524-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="fd524-112">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="fd524-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="fd524-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="fd524-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="fd524-114">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="fd524-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="fd524-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="fd524-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="fd524-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fd524-116">Parent elements</span></span>



| <span data-ttu-id="fd524-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd524-117">Element</span></span>                         | <span data-ttu-id="fd524-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd524-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fd524-119">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="fd524-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="fd524-120">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="fd524-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fd524-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd524-121">Remarks</span></span>

<span data-ttu-id="fd524-122">As estruturas de mensagem são referenciadas pelo proxy gerado e pelo código stub.</span><span class="sxs-lookup"><span data-stu-id="fd524-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="fd524-123">Esse elemento é usado para gerar arquivos de inclusão.</span><span class="sxs-lookup"><span data-stu-id="fd524-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="fd524-124">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="fd524-124">Element information</span></span>



| <span data-ttu-id="fd524-125">Label</span><span class="sxs-lookup"><span data-stu-id="fd524-125">Label</span></span> | <span data-ttu-id="fd524-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fd524-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="fd524-127">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd524-127">Minimum supported system</span></span><br/> | <span data-ttu-id="fd524-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd524-128">Windows Vista</span></span> |
| <span data-ttu-id="fd524-129">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="fd524-129">Can be empty</span></span>                        | <span data-ttu-id="fd524-130">Sim</span><span class="sxs-lookup"><span data-stu-id="fd524-130">Yes</span></span>           |



 

 




