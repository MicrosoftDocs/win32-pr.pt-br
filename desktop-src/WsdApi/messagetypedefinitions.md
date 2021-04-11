---
description: Gera constantes C para tabelas de esquema XML para tipos de mensagem.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f86043cc28b527778c91772ad731d3a271921f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165304"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="f5d40-103">elemento messageTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="f5d40-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="f5d40-104">Gera constantes C para tabelas de esquema XML para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f5d40-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="f5d40-105">Uso</span><span class="sxs-lookup"><span data-stu-id="f5d40-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="f5d40-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="f5d40-106">Attributes</span></span>

<span data-ttu-id="f5d40-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="f5d40-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f5d40-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f5d40-108">Child elements</span></span>



| <span data-ttu-id="f5d40-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f5d40-109">Element</span></span>                                   | <span data-ttu-id="f5d40-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5d40-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f5d40-111">**operacional**</span><span class="sxs-lookup"><span data-stu-id="f5d40-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="f5d40-112">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="f5d40-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="f5d40-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="f5d40-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="f5d40-114">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="f5d40-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="f5d40-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="f5d40-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="f5d40-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f5d40-116">Parent elements</span></span>



| <span data-ttu-id="f5d40-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="f5d40-117">Element</span></span>                         | <span data-ttu-id="f5d40-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5d40-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f5d40-119">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="f5d40-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f5d40-120">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="f5d40-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f5d40-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5d40-121">Remarks</span></span>

<span data-ttu-id="f5d40-122">Esse elemento é geralmente usado em arquivos de origem C para fornecer as tabelas de esquema declaradas por [**messageTypeDeclarations**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="f5d40-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="f5d40-123">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f5d40-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f5d40-124">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5d40-124">Minimum supported system</span></span><br/> | <span data-ttu-id="f5d40-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5d40-125">Windows Vista</span></span> |
| <span data-ttu-id="f5d40-126">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="f5d40-126">Can be empty</span></span>                        | <span data-ttu-id="f5d40-127">Sim</span><span class="sxs-lookup"><span data-stu-id="f5d40-127">Yes</span></span>           |



 

 




