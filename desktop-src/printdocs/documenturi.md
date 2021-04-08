---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9964df145e75fe2b30d670d5575928485e00c5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930251"
---
# <a name="documenturi"></a><span data-ttu-id="5bdb3-104">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="5bdb3-104">DocumentURI</span></span>

<span data-ttu-id="5bdb3-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5bdb3-105">This topic is not current.</span></span> <span data-ttu-id="5bdb3-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5bdb3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5bdb3-107">Especifica um URI (Uniform Resource Identifier) para o documento.</span><span class="sxs-lookup"><span data-stu-id="5bdb3-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="5bdb3-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5bdb3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5bdb3-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5bdb3-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5bdb3-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5bdb3-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5bdb3-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5bdb3-111">Element Information</span></span>



| <span data-ttu-id="5bdb3-112">Nome</span><span class="sxs-lookup"><span data-stu-id="5bdb3-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="5bdb3-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5bdb3-113">Element Type</span></span> <br/>   | <span data-ttu-id="5bdb3-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5bdb3-114">Property</span></span><br/> |
| <span data-ttu-id="5bdb3-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="5bdb3-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5bdb3-116">Documento</span><span class="sxs-lookup"><span data-stu-id="5bdb3-116">Document</span></span><br/> |
| <span data-ttu-id="5bdb3-117">Observações</span><span class="sxs-lookup"><span data-stu-id="5bdb3-117">Notes</span></span> <br/>          | <span data-ttu-id="5bdb3-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5bdb3-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="5bdb3-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5bdb3-119">Structural Content</span></span>

<span data-ttu-id="5bdb3-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="5bdb3-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="5bdb3-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="5bdb3-121">Structure Variables</span></span>

<span data-ttu-id="5bdb3-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="5bdb3-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5bdb3-123">Nome</span><span class="sxs-lookup"><span data-stu-id="5bdb3-123">Name</span></span>                            | <span data-ttu-id="5bdb3-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5bdb3-124">Data type</span></span>         | <span data-ttu-id="5bdb3-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="5bdb3-125">Unit</span></span> | <span data-ttu-id="5bdb3-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="5bdb3-126">Supported values</span></span> | <span data-ttu-id="5bdb3-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="5bdb3-127">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="5bdb3-128">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="5bdb3-128">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="5bdb3-129">string</span><span class="sxs-lookup"><span data-stu-id="5bdb3-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5bdb3-130">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5bdb3-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="5bdb3-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bdb3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bdb3-132">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5bdb3-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




