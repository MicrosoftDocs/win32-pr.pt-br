---
description: Saiba mais sobre a propriedade DocumentName, que especifica um nome descritivo para o documento.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: Documentname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202ff1f5bac85fec3feac9f141834adfcd37e70
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409269"
---
# <a name="documentname"></a><span data-ttu-id="f1e31-103">Documentname</span><span class="sxs-lookup"><span data-stu-id="f1e31-103">DocumentName</span></span>

<span data-ttu-id="f1e31-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f1e31-104">This topic is not current.</span></span> <span data-ttu-id="f1e31-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f1e31-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f1e31-106">Especifica um nome descritivo para o documento.</span><span class="sxs-lookup"><span data-stu-id="f1e31-106">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="f1e31-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f1e31-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f1e31-108">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f1e31-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f1e31-109">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f1e31-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f1e31-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f1e31-110">Element Information</span></span>



| <span data-ttu-id="f1e31-111">Name</span><span class="sxs-lookup"><span data-stu-id="f1e31-111">Name</span></span> | <span data-ttu-id="f1e31-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f1e31-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="f1e31-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f1e31-113">Element Type</span></span> <br/>   | <span data-ttu-id="f1e31-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f1e31-114">Property</span></span><br/> |
| <span data-ttu-id="f1e31-115">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="f1e31-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f1e31-116">Documento</span><span class="sxs-lookup"><span data-stu-id="f1e31-116">Document</span></span><br/> |
| <span data-ttu-id="f1e31-117">Observações</span><span class="sxs-lookup"><span data-stu-id="f1e31-117">Notes</span></span> <br/>          | <span data-ttu-id="f1e31-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f1e31-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="f1e31-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f1e31-119">Structural Content</span></span>

<span data-ttu-id="f1e31-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="f1e31-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="f1e31-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="f1e31-121">Structure Variables</span></span>

<span data-ttu-id="f1e31-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f1e31-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f1e31-123">Nome</span><span class="sxs-lookup"><span data-stu-id="f1e31-123">Name</span></span>                             | <span data-ttu-id="f1e31-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f1e31-124">Data type</span></span>         | <span data-ttu-id="f1e31-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="f1e31-125">Unit</span></span> | <span data-ttu-id="f1e31-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="f1e31-126">Supported values</span></span> | <span data-ttu-id="f1e31-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="f1e31-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="f1e31-128">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="f1e31-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="f1e31-129">string</span><span class="sxs-lookup"><span data-stu-id="f1e31-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f1e31-130">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f1e31-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="f1e31-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1e31-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1e31-132">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f1e31-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




