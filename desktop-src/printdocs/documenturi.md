---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d339b1b469f276492f7989b0ed7951ca1edad8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997063"
---
# <a name="documenturi"></a><span data-ttu-id="5f899-104">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="5f899-104">DocumentURI</span></span>

<span data-ttu-id="5f899-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5f899-105">This topic is not current.</span></span> <span data-ttu-id="5f899-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5f899-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5f899-107">Especifica um URI (Uniform Resource Identifier) para o documento.</span><span class="sxs-lookup"><span data-stu-id="5f899-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="5f899-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5f899-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5f899-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5f899-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5f899-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5f899-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5f899-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5f899-111">Element Information</span></span>



| <span data-ttu-id="5f899-112">Nome</span><span class="sxs-lookup"><span data-stu-id="5f899-112">Name</span></span> | <span data-ttu-id="5f899-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5f899-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="5f899-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5f899-114">Element Type</span></span> <br/>   | <span data-ttu-id="5f899-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5f899-115">Property</span></span><br/> |
| <span data-ttu-id="5f899-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="5f899-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5f899-117">Documento</span><span class="sxs-lookup"><span data-stu-id="5f899-117">Document</span></span><br/> |
| <span data-ttu-id="5f899-118">Observações</span><span class="sxs-lookup"><span data-stu-id="5f899-118">Notes</span></span> <br/>          | <span data-ttu-id="5f899-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5f899-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="5f899-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5f899-120">Structural Content</span></span>

<span data-ttu-id="5f899-121">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="5f899-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="5f899-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="5f899-122">Structure Variables</span></span>

<span data-ttu-id="5f899-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="5f899-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5f899-124">Nome</span><span class="sxs-lookup"><span data-stu-id="5f899-124">Name</span></span>                            | <span data-ttu-id="5f899-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5f899-125">Data type</span></span>         | <span data-ttu-id="5f899-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="5f899-126">Unit</span></span> | <span data-ttu-id="5f899-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="5f899-127">Supported values</span></span> | <span data-ttu-id="5f899-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="5f899-128">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="5f899-129">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="5f899-129">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="5f899-130">string</span><span class="sxs-lookup"><span data-stu-id="5f899-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5f899-131">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5f899-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="5f899-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f899-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f899-133">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5f899-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




