---
description: Saiba mais sobre o elemento JobURI, que especifica um URI (Uniform Resource Identifier) para o documento.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc145ac9a393c09ecab762b84e9ac7d58870ddf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408609"
---
# <a name="joburi"></a><span data-ttu-id="7bf8d-103">JobURI</span><span class="sxs-lookup"><span data-stu-id="7bf8d-103">JobURI</span></span>

<span data-ttu-id="7bf8d-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7bf8d-104">This topic is not current.</span></span> <span data-ttu-id="7bf8d-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7bf8d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7bf8d-106">Especifica um URI (Uniform Resource Identifier) para o documento.</span><span class="sxs-lookup"><span data-stu-id="7bf8d-106">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="7bf8d-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7bf8d-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7bf8d-108">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="7bf8d-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7bf8d-109">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="7bf8d-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7bf8d-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7bf8d-110">Element Information</span></span>



| <span data-ttu-id="7bf8d-111">Name</span><span class="sxs-lookup"><span data-stu-id="7bf8d-111">Name</span></span> | <span data-ttu-id="7bf8d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7bf8d-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="7bf8d-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7bf8d-113">Element Type</span></span> <br/>   | <span data-ttu-id="7bf8d-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7bf8d-114">Property</span></span><br/> |
| <span data-ttu-id="7bf8d-115">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="7bf8d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7bf8d-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="7bf8d-116">Job</span></span><br/>      |
| <span data-ttu-id="7bf8d-117">Observações</span><span class="sxs-lookup"><span data-stu-id="7bf8d-117">Notes</span></span> <br/>          | <span data-ttu-id="7bf8d-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7bf8d-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7bf8d-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="7bf8d-119">Structural Content</span></span>

<span data-ttu-id="7bf8d-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="7bf8d-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="7bf8d-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="7bf8d-121">Structure Variables</span></span>

<span data-ttu-id="7bf8d-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="7bf8d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7bf8d-123">Nome</span><span class="sxs-lookup"><span data-stu-id="7bf8d-123">Name</span></span>                       | <span data-ttu-id="7bf8d-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7bf8d-124">Data type</span></span>         | <span data-ttu-id="7bf8d-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="7bf8d-125">Unit</span></span> | <span data-ttu-id="7bf8d-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="7bf8d-126">Supported values</span></span> | <span data-ttu-id="7bf8d-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="7bf8d-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="7bf8d-128">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="7bf8d-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="7bf8d-129">string</span><span class="sxs-lookup"><span data-stu-id="7bf8d-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7bf8d-130">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="7bf8d-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="7bf8d-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bf8d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bf8d-132">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7bf8d-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




