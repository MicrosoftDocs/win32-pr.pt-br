---
description: Saiba mais sobre o elemento JobID, que especifica uma ID exclusiva para o trabalho. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd17d068f34b56d45e4851c06b7ed1d9bd6fcc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408879"
---
# <a name="jobid"></a><span data-ttu-id="2956b-104">JobID</span><span class="sxs-lookup"><span data-stu-id="2956b-104">JobID</span></span>

<span data-ttu-id="2956b-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="2956b-105">This topic is not current.</span></span> <span data-ttu-id="2956b-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2956b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2956b-107">Especifica uma ID exclusiva para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="2956b-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="2956b-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2956b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2956b-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="2956b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2956b-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2956b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2956b-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2956b-111">Element Information</span></span>



| <span data-ttu-id="2956b-112">Name</span><span class="sxs-lookup"><span data-stu-id="2956b-112">Name</span></span> | <span data-ttu-id="2956b-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2956b-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="2956b-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2956b-114">Element Type</span></span> <br/>   | <span data-ttu-id="2956b-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2956b-115">Property</span></span><br/> |
| <span data-ttu-id="2956b-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="2956b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2956b-117">Trabalho</span><span class="sxs-lookup"><span data-stu-id="2956b-117">Job</span></span><br/>      |
| <span data-ttu-id="2956b-118">Observações</span><span class="sxs-lookup"><span data-stu-id="2956b-118">Notes</span></span> <br/>          | <span data-ttu-id="2956b-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2956b-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="2956b-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="2956b-120">Structural Content</span></span>

<span data-ttu-id="2956b-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="2956b-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="2956b-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="2956b-122">Structure Variables</span></span>

<span data-ttu-id="2956b-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="2956b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2956b-124">Nome</span><span class="sxs-lookup"><span data-stu-id="2956b-124">Name</span></span>                      | <span data-ttu-id="2956b-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2956b-125">Data type</span></span>         | <span data-ttu-id="2956b-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="2956b-126">Unit</span></span> | <span data-ttu-id="2956b-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="2956b-127">Supported values</span></span> | <span data-ttu-id="2956b-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="2956b-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="2956b-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="2956b-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="2956b-130">string</span><span class="sxs-lookup"><span data-stu-id="2956b-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2956b-131">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2956b-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="2956b-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2956b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2956b-133">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="2956b-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




