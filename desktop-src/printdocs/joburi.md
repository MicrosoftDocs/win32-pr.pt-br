---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c80611a4e7dbd10f4841fae098578f0a8fdc96
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993883"
---
# <a name="joburi"></a><span data-ttu-id="d6572-104">JobURI</span><span class="sxs-lookup"><span data-stu-id="d6572-104">JobURI</span></span>

<span data-ttu-id="d6572-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d6572-105">This topic is not current.</span></span> <span data-ttu-id="d6572-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d6572-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d6572-107">Especifica um URI (Uniform Resource Identifier) para o documento.</span><span class="sxs-lookup"><span data-stu-id="d6572-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="d6572-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d6572-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d6572-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d6572-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d6572-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d6572-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d6572-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d6572-111">Element Information</span></span>



| <span data-ttu-id="d6572-112">Nome</span><span class="sxs-lookup"><span data-stu-id="d6572-112">Name</span></span> | <span data-ttu-id="d6572-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d6572-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="d6572-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d6572-114">Element Type</span></span> <br/>   | <span data-ttu-id="d6572-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d6572-115">Property</span></span><br/> |
| <span data-ttu-id="d6572-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="d6572-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d6572-117">Trabalho</span><span class="sxs-lookup"><span data-stu-id="d6572-117">Job</span></span><br/>      |
| <span data-ttu-id="d6572-118">Observações</span><span class="sxs-lookup"><span data-stu-id="d6572-118">Notes</span></span> <br/>          | <span data-ttu-id="d6572-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d6572-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="d6572-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d6572-120">Structural Content</span></span>

<span data-ttu-id="d6572-121">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="d6572-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="d6572-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="d6572-122">Structure Variables</span></span>

<span data-ttu-id="d6572-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d6572-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d6572-124">Nome</span><span class="sxs-lookup"><span data-stu-id="d6572-124">Name</span></span>                       | <span data-ttu-id="d6572-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d6572-125">Data type</span></span>         | <span data-ttu-id="d6572-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="d6572-126">Unit</span></span> | <span data-ttu-id="d6572-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="d6572-127">Supported values</span></span> | <span data-ttu-id="d6572-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="d6572-128">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="d6572-129">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="d6572-129">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="d6572-130">string</span><span class="sxs-lookup"><span data-stu-id="d6572-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d6572-131">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d6572-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="d6572-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6572-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6572-133">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d6572-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




