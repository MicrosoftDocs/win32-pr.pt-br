---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb06148438b0fd6715370c56ff9efe54d512219
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105810637"
---
# <a name="joburi"></a><span data-ttu-id="b32ab-104">JobURI</span><span class="sxs-lookup"><span data-stu-id="b32ab-104">JobURI</span></span>

<span data-ttu-id="b32ab-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b32ab-105">This topic is not current.</span></span> <span data-ttu-id="b32ab-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b32ab-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b32ab-107">Especifica um URI (Uniform Resource Identifier) para o documento.</span><span class="sxs-lookup"><span data-stu-id="b32ab-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="b32ab-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b32ab-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b32ab-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b32ab-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b32ab-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b32ab-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b32ab-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b32ab-111">Element Information</span></span>



| <span data-ttu-id="b32ab-112">Nome</span><span class="sxs-lookup"><span data-stu-id="b32ab-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="b32ab-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b32ab-113">Element Type</span></span> <br/>   | <span data-ttu-id="b32ab-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b32ab-114">Property</span></span><br/> |
| <span data-ttu-id="b32ab-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="b32ab-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b32ab-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="b32ab-116">Job</span></span><br/>      |
| <span data-ttu-id="b32ab-117">Observações</span><span class="sxs-lookup"><span data-stu-id="b32ab-117">Notes</span></span> <br/>          | <span data-ttu-id="b32ab-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b32ab-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="b32ab-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b32ab-119">Structural Content</span></span>

<span data-ttu-id="b32ab-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="b32ab-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="b32ab-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="b32ab-121">Structure Variables</span></span>

<span data-ttu-id="b32ab-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="b32ab-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b32ab-123">Nome</span><span class="sxs-lookup"><span data-stu-id="b32ab-123">Name</span></span>                       | <span data-ttu-id="b32ab-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b32ab-124">Data type</span></span>         | <span data-ttu-id="b32ab-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="b32ab-125">Unit</span></span> | <span data-ttu-id="b32ab-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="b32ab-126">Supported values</span></span> | <span data-ttu-id="b32ab-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="b32ab-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="b32ab-128">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="b32ab-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="b32ab-129">string</span><span class="sxs-lookup"><span data-stu-id="b32ab-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b32ab-130">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b32ab-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="b32ab-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b32ab-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b32ab-132">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b32ab-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




