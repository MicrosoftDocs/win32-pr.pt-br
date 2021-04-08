---
description: Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922414"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="81612-103">elemento messageTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="81612-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="81612-104">Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="81612-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="81612-105">Uso</span><span class="sxs-lookup"><span data-stu-id="81612-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="81612-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="81612-106">Attributes</span></span>

<span data-ttu-id="81612-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="81612-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="81612-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="81612-108">Child elements</span></span>



| <span data-ttu-id="81612-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="81612-109">Element</span></span>                                   | <span data-ttu-id="81612-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="81612-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="81612-111">**operacional**</span><span class="sxs-lookup"><span data-stu-id="81612-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="81612-112">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="81612-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="81612-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="81612-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="81612-114">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="81612-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="81612-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="81612-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="81612-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="81612-116">Parent elements</span></span>



| <span data-ttu-id="81612-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="81612-117">Element</span></span>                         | <span data-ttu-id="81612-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="81612-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="81612-119">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="81612-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="81612-120">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="81612-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="81612-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="81612-121">Remarks</span></span>

<span data-ttu-id="81612-122">As tabelas de esquema são referenciadas por definições de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="81612-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="81612-123">Esse elemento é, portanto, geralmente usado logo antes dos elementos [**portTypeDefinitions**](porttypedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="81612-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="81612-124">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="81612-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="81612-125">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81612-125">Minimum supported system</span></span><br/> | <span data-ttu-id="81612-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81612-126">Windows Vista</span></span> |
| <span data-ttu-id="81612-127">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="81612-127">Can be empty</span></span>                        | <span data-ttu-id="81612-128">Sim</span><span class="sxs-lookup"><span data-stu-id="81612-128">Yes</span></span>           |



 

 




