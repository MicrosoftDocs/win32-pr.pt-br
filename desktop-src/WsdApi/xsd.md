---
description: Especifica um arquivo XSD para processar informações de contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994543"
---
# <a name="xsd-element"></a><span data-ttu-id="ce016-103">elemento xsd</span><span class="sxs-lookup"><span data-stu-id="ce016-103">xsd element</span></span>

<span data-ttu-id="ce016-104">Especifica um arquivo XSD para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="ce016-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="ce016-105">Uso</span><span class="sxs-lookup"><span data-stu-id="ce016-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="ce016-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce016-106">Attributes</span></span>



| <span data-ttu-id="ce016-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="ce016-107">Attribute</span></span>           | <span data-ttu-id="ce016-108">Type</span><span class="sxs-lookup"><span data-stu-id="ce016-108">Type</span></span>                       | <span data-ttu-id="ce016-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ce016-109">Required</span></span>       | <span data-ttu-id="ce016-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce016-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="ce016-111">**path**</span><span class="sxs-lookup"><span data-stu-id="ce016-111">**path**</span></span><br/> | <span data-ttu-id="ce016-112">Cadeia de nome do caminho</span><span class="sxs-lookup"><span data-stu-id="ce016-112">pathname string</span></span><br/> | <span data-ttu-id="ce016-113">Sim</span><span class="sxs-lookup"><span data-stu-id="ce016-113">Yes</span></span><br/> | <span data-ttu-id="ce016-114">Arquivo e caminho do arquivo de entrada XSD.</span><span class="sxs-lookup"><span data-stu-id="ce016-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="ce016-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ce016-115">Child elements</span></span>



| <span data-ttu-id="ce016-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce016-116">Element</span></span>                               | <span data-ttu-id="ce016-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce016-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="ce016-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="ce016-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="ce016-119">Especifica um tipo a ser incluído de um arquivo XSD.</span><span class="sxs-lookup"><span data-stu-id="ce016-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="ce016-120">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="ce016-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="ce016-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ce016-121">Parent elements</span></span>



| <span data-ttu-id="ce016-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce016-122">Element</span></span>                                     | <span data-ttu-id="ce016-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce016-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce016-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="ce016-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="ce016-125">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ce016-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ce016-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce016-126">Remarks</span></span>

<span data-ttu-id="ce016-127">A cadeia de caracteres do nome do arquivo deve incluir informações completas de caminho também.</span><span class="sxs-lookup"><span data-stu-id="ce016-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="ce016-128">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ce016-128">Element information</span></span>



| <span data-ttu-id="ce016-129">Label</span><span class="sxs-lookup"><span data-stu-id="ce016-129">Label</span></span> | <span data-ttu-id="ce016-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ce016-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ce016-131">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce016-131">Minimum supported system</span></span><br/> | <span data-ttu-id="ce016-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce016-132">Windows Vista</span></span> |
| <span data-ttu-id="ce016-133">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="ce016-133">Can be empty</span></span>                        | <span data-ttu-id="ce016-134">Sim</span><span class="sxs-lookup"><span data-stu-id="ce016-134">Yes</span></span>           |



 

 




