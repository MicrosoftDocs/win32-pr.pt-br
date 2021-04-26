---
description: Gera constantes C para tabelas de esquema XML para tipos de mensagem.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998703"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="f71f1-103">elemento messageTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="f71f1-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="f71f1-104">Gera constantes C para tabelas de esquema XML para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f71f1-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="f71f1-105">Uso</span><span class="sxs-lookup"><span data-stu-id="f71f1-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="f71f1-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="f71f1-106">Attributes</span></span>

<span data-ttu-id="f71f1-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="f71f1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f71f1-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f71f1-108">Child elements</span></span>



| <span data-ttu-id="f71f1-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f71f1-109">Element</span></span>                                   | <span data-ttu-id="f71f1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f71f1-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f71f1-111">**operacional**</span><span class="sxs-lookup"><span data-stu-id="f71f1-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="f71f1-112">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="f71f1-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="f71f1-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="f71f1-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="f71f1-114">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="f71f1-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="f71f1-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="f71f1-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="f71f1-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f71f1-116">Parent elements</span></span>



| <span data-ttu-id="f71f1-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="f71f1-117">Element</span></span>                         | <span data-ttu-id="f71f1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f71f1-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f71f1-119">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="f71f1-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f71f1-120">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="f71f1-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f71f1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f71f1-121">Remarks</span></span>

<span data-ttu-id="f71f1-122">Esse elemento é geralmente usado em arquivos de origem C para fornecer as tabelas de esquema declaradas por [**messageTypeDeclarations**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="f71f1-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="f71f1-123">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f71f1-123">Element information</span></span>



| <span data-ttu-id="f71f1-124">Label</span><span class="sxs-lookup"><span data-stu-id="f71f1-124">Label</span></span> | <span data-ttu-id="f71f1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f71f1-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="f71f1-126">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f71f1-126">Minimum supported system</span></span><br/> | <span data-ttu-id="f71f1-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f71f1-127">Windows Vista</span></span> |
| <span data-ttu-id="f71f1-128">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="f71f1-128">Can be empty</span></span>                        | <span data-ttu-id="f71f1-129">Sim</span><span class="sxs-lookup"><span data-stu-id="f71f1-129">Yes</span></span>           |



 

 




