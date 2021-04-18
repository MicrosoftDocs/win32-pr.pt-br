---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161801e56a27e33cdf921cc07c93e59836d4dd90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105785952"
---
# <a name="jobname"></a><span data-ttu-id="dba51-104">JobName</span><span class="sxs-lookup"><span data-stu-id="dba51-104">JobName</span></span>

<span data-ttu-id="dba51-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="dba51-105">This topic is not current.</span></span> <span data-ttu-id="dba51-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dba51-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dba51-107">Especifica um nome descritivo para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="dba51-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="dba51-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dba51-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dba51-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="dba51-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="dba51-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="dba51-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="dba51-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dba51-111">Element Information</span></span>



| <span data-ttu-id="dba51-112">Nome</span><span class="sxs-lookup"><span data-stu-id="dba51-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="dba51-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dba51-113">Element Type</span></span> <br/>   | <span data-ttu-id="dba51-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dba51-114">Property</span></span><br/> |
| <span data-ttu-id="dba51-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="dba51-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dba51-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="dba51-116">Job</span></span><br/>      |
| <span data-ttu-id="dba51-117">Observações</span><span class="sxs-lookup"><span data-stu-id="dba51-117">Notes</span></span> <br/>          | <span data-ttu-id="dba51-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dba51-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="dba51-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="dba51-119">Structural Content</span></span>

<span data-ttu-id="dba51-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="dba51-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="dba51-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="dba51-121">Structure Variables</span></span>

<span data-ttu-id="dba51-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="dba51-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dba51-123">Nome</span><span class="sxs-lookup"><span data-stu-id="dba51-123">Name</span></span>                        | <span data-ttu-id="dba51-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dba51-124">Data type</span></span>         | <span data-ttu-id="dba51-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="dba51-125">Unit</span></span> | <span data-ttu-id="dba51-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="dba51-126">Supported values</span></span> | <span data-ttu-id="dba51-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="dba51-127">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="dba51-128">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="dba51-128">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="dba51-129">string</span><span class="sxs-lookup"><span data-stu-id="dba51-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="dba51-130">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="dba51-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="dba51-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dba51-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dba51-132">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="dba51-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




