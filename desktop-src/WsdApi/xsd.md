---
description: Especifica um arquivo XSD para processar informações de contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828498"
---
# <a name="xsd-element"></a><span data-ttu-id="b1922-103">elemento xsd</span><span class="sxs-lookup"><span data-stu-id="b1922-103">xsd element</span></span>

<span data-ttu-id="b1922-104">Especifica um arquivo XSD para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="b1922-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="b1922-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b1922-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="b1922-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1922-106">Attributes</span></span>



| <span data-ttu-id="b1922-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="b1922-107">Attribute</span></span>           | <span data-ttu-id="b1922-108">Type</span><span class="sxs-lookup"><span data-stu-id="b1922-108">Type</span></span>                       | <span data-ttu-id="b1922-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b1922-109">Required</span></span>       | <span data-ttu-id="b1922-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1922-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="b1922-111">**path**</span><span class="sxs-lookup"><span data-stu-id="b1922-111">**path**</span></span><br/> | <span data-ttu-id="b1922-112">Cadeia de nome do caminho</span><span class="sxs-lookup"><span data-stu-id="b1922-112">pathname string</span></span><br/> | <span data-ttu-id="b1922-113">Sim</span><span class="sxs-lookup"><span data-stu-id="b1922-113">Yes</span></span><br/> | <span data-ttu-id="b1922-114">Arquivo e caminho do arquivo de entrada XSD.</span><span class="sxs-lookup"><span data-stu-id="b1922-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b1922-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b1922-115">Child elements</span></span>



| <span data-ttu-id="b1922-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1922-116">Element</span></span>                               | <span data-ttu-id="b1922-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1922-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="b1922-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="b1922-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="b1922-119">Especifica um tipo a ser incluído de um arquivo XSD.</span><span class="sxs-lookup"><span data-stu-id="b1922-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b1922-120">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="b1922-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="b1922-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b1922-121">Parent elements</span></span>



| <span data-ttu-id="b1922-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1922-122">Element</span></span>                                     | <span data-ttu-id="b1922-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1922-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1922-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="b1922-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="b1922-125">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="b1922-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b1922-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1922-126">Remarks</span></span>

<span data-ttu-id="b1922-127">A cadeia de caracteres do nome do arquivo deve incluir informações completas de caminho também.</span><span class="sxs-lookup"><span data-stu-id="b1922-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="b1922-128">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b1922-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b1922-129">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1922-129">Minimum supported system</span></span><br/> | <span data-ttu-id="b1922-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1922-130">Windows Vista</span></span> |
| <span data-ttu-id="b1922-131">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="b1922-131">Can be empty</span></span>                        | <span data-ttu-id="b1922-132">Sim</span><span class="sxs-lookup"><span data-stu-id="b1922-132">Yes</span></span>           |



 

 




