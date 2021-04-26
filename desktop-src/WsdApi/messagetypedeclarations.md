---
description: Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998723"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="baf2d-103">elemento messageTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="baf2d-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="baf2d-104">Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="baf2d-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="baf2d-105">Uso</span><span class="sxs-lookup"><span data-stu-id="baf2d-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="baf2d-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="baf2d-106">Attributes</span></span>

<span data-ttu-id="baf2d-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="baf2d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="baf2d-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="baf2d-108">Child elements</span></span>



| <span data-ttu-id="baf2d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="baf2d-109">Element</span></span>                                   | <span data-ttu-id="baf2d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="baf2d-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="baf2d-111">**operacional**</span><span class="sxs-lookup"><span data-stu-id="baf2d-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="baf2d-112">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="baf2d-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="baf2d-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="baf2d-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="baf2d-114">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="baf2d-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="baf2d-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="baf2d-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="baf2d-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="baf2d-116">Parent elements</span></span>



| <span data-ttu-id="baf2d-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="baf2d-117">Element</span></span>                         | <span data-ttu-id="baf2d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="baf2d-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="baf2d-119">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="baf2d-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="baf2d-120">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="baf2d-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="baf2d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="baf2d-121">Remarks</span></span>

<span data-ttu-id="baf2d-122">As tabelas de esquema são referenciadas por definições de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="baf2d-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="baf2d-123">Esse elemento é, portanto, geralmente usado logo antes dos elementos [**portTypeDefinitions**](porttypedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="baf2d-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="baf2d-124">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="baf2d-124">Element information</span></span>



| <span data-ttu-id="baf2d-125">Label</span><span class="sxs-lookup"><span data-stu-id="baf2d-125">Label</span></span> | <span data-ttu-id="baf2d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="baf2d-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="baf2d-127">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baf2d-127">Minimum supported system</span></span><br/> | <span data-ttu-id="baf2d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="baf2d-128">Windows Vista</span></span> |
| <span data-ttu-id="baf2d-129">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="baf2d-129">Can be empty</span></span>                        | <span data-ttu-id="baf2d-130">Sim</span><span class="sxs-lookup"><span data-stu-id="baf2d-130">Yes</span></span>           |



 

 




