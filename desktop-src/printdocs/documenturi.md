---
description: Obter informações sobre a propriedade DocumentURI. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb4d1572417ac85e14c25c238be1d49611ba858
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548804"
---
# <a name="documenturi"></a><span data-ttu-id="8ecd5-105">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="8ecd5-105">DocumentURI</span></span>

<span data-ttu-id="8ecd5-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="8ecd5-106">This topic is not current.</span></span> <span data-ttu-id="8ecd5-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8ecd5-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8ecd5-108">Especifica um URI (Uniform Resource Identifier) para o documento.</span><span class="sxs-lookup"><span data-stu-id="8ecd5-108">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="8ecd5-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8ecd5-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8ecd5-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="8ecd5-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8ecd5-111">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="8ecd5-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8ecd5-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8ecd5-112">Element Information</span></span>



| <span data-ttu-id="8ecd5-113">Nome</span><span class="sxs-lookup"><span data-stu-id="8ecd5-113">Name</span></span> | <span data-ttu-id="8ecd5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8ecd5-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="8ecd5-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8ecd5-115">Element Type</span></span> <br/>   | <span data-ttu-id="8ecd5-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8ecd5-116">Property</span></span><br/> |
| <span data-ttu-id="8ecd5-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="8ecd5-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8ecd5-118">Documento</span><span class="sxs-lookup"><span data-stu-id="8ecd5-118">Document</span></span><br/> |
| <span data-ttu-id="8ecd5-119">Observações</span><span class="sxs-lookup"><span data-stu-id="8ecd5-119">Notes</span></span> <br/>          | <span data-ttu-id="8ecd5-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8ecd5-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="8ecd5-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="8ecd5-121">Structural Content</span></span>

<span data-ttu-id="8ecd5-122">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="8ecd5-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="8ecd5-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="8ecd5-123">Structure Variables</span></span>

<span data-ttu-id="8ecd5-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="8ecd5-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8ecd5-125">Nome</span><span class="sxs-lookup"><span data-stu-id="8ecd5-125">Name</span></span>                            | <span data-ttu-id="8ecd5-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8ecd5-126">Data type</span></span>         | <span data-ttu-id="8ecd5-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="8ecd5-127">Unit</span></span> | <span data-ttu-id="8ecd5-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="8ecd5-128">Supported values</span></span> | <span data-ttu-id="8ecd5-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="8ecd5-129">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="8ecd5-130">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="8ecd5-130">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="8ecd5-131">string</span><span class="sxs-lookup"><span data-stu-id="8ecd5-131">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8ecd5-132">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="8ecd5-132">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="8ecd5-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ecd5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ecd5-134">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="8ecd5-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




