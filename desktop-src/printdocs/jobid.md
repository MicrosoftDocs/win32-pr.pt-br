---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c182e5d0bfcfb395eb553570cca745b618fc56b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105752383"
---
# <a name="jobid"></a><span data-ttu-id="7c569-104">JobID</span><span class="sxs-lookup"><span data-stu-id="7c569-104">JobID</span></span>

<span data-ttu-id="7c569-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7c569-105">This topic is not current.</span></span> <span data-ttu-id="7c569-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7c569-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7c569-107">Especifica uma ID exclusiva para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="7c569-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="7c569-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7c569-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7c569-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="7c569-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7c569-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7c569-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7c569-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7c569-111">Element Information</span></span>



| <span data-ttu-id="7c569-112">Nome</span><span class="sxs-lookup"><span data-stu-id="7c569-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="7c569-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7c569-113">Element Type</span></span> <br/>   | <span data-ttu-id="7c569-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7c569-114">Property</span></span><br/> |
| <span data-ttu-id="7c569-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="7c569-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7c569-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="7c569-116">Job</span></span><br/>      |
| <span data-ttu-id="7c569-117">Observações</span><span class="sxs-lookup"><span data-stu-id="7c569-117">Notes</span></span> <br/>          | <span data-ttu-id="7c569-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7c569-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7c569-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="7c569-119">Structural Content</span></span>

<span data-ttu-id="7c569-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="7c569-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="7c569-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="7c569-121">Structure Variables</span></span>

<span data-ttu-id="7c569-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="7c569-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7c569-123">Nome</span><span class="sxs-lookup"><span data-stu-id="7c569-123">Name</span></span>                      | <span data-ttu-id="7c569-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7c569-124">Data type</span></span>         | <span data-ttu-id="7c569-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="7c569-125">Unit</span></span> | <span data-ttu-id="7c569-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="7c569-126">Supported values</span></span> | <span data-ttu-id="7c569-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="7c569-127">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="7c569-128">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="7c569-128">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="7c569-129">string</span><span class="sxs-lookup"><span data-stu-id="7c569-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7c569-130">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7c569-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="7c569-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c569-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c569-132">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7c569-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




