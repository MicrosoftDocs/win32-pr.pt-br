---
description: Saiba mais sobre o elemento JobRollCutAtEndOfJob, que descreve o método de redução para o roll paper. O roll deve ser cortado no final do trabalho.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fdb973f3fda9fea28f64f0edb232910f2d2201
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408659"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="d9f83-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="d9f83-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="d9f83-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d9f83-105">This topic is not current.</span></span> <span data-ttu-id="d9f83-106">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d9f83-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d9f83-107">Descreve o método de corte para papel de rolagem.</span><span class="sxs-lookup"><span data-stu-id="d9f83-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="d9f83-108">O roll deve ser cortado no final do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d9f83-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="d9f83-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d9f83-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d9f83-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d9f83-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d9f83-111">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="d9f83-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d9f83-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d9f83-112">Element Information</span></span>



| <span data-ttu-id="d9f83-113">Name</span><span class="sxs-lookup"><span data-stu-id="d9f83-113">Name</span></span> | <span data-ttu-id="d9f83-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d9f83-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="d9f83-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d9f83-115">Element Type</span></span> <br/>   | <span data-ttu-id="d9f83-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="d9f83-116">Feature</span></span><br/> |
| <span data-ttu-id="d9f83-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="d9f83-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d9f83-118">Trabalho</span><span class="sxs-lookup"><span data-stu-id="d9f83-118">Job</span></span><br/>     |
| <span data-ttu-id="d9f83-119">Observações</span><span class="sxs-lookup"><span data-stu-id="d9f83-119">Notes</span></span> <br/>          | <span data-ttu-id="d9f83-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d9f83-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d9f83-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d9f83-121">Structural Content</span></span>

<span data-ttu-id="d9f83-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d9f83-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJobAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="d9f83-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="d9f83-123">Structure Variables</span></span>

<span data-ttu-id="d9f83-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d9f83-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d9f83-125">Nome</span><span class="sxs-lookup"><span data-stu-id="d9f83-125">Name</span></span>                               | <span data-ttu-id="d9f83-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d9f83-126">Data type</span></span>         | <span data-ttu-id="d9f83-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="d9f83-127">Unit</span></span>                  | <span data-ttu-id="d9f83-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="d9f83-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d9f83-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="d9f83-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d9f83-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="d9f83-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d9f83-131">string</span><span class="sxs-lookup"><span data-stu-id="d9f83-131">string</span></span><br/> | <span data-ttu-id="d9f83-132">characters</span><span class="sxs-lookup"><span data-stu-id="d9f83-132">characters</span></span><br/> | <span data-ttu-id="d9f83-133">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="d9f83-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d9f83-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="d9f83-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d9f83-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="d9f83-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d9f83-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d9f83-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d9f83-137">string</span><span class="sxs-lookup"><span data-stu-id="d9f83-137">string</span></span><br/> | <span data-ttu-id="d9f83-138">n/d</span><span class="sxs-lookup"><span data-stu-id="d9f83-138">n/a</span></span><br/>        | <span data-ttu-id="d9f83-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="d9f83-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d9f83-140">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="d9f83-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d9f83-141">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="d9f83-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d9f83-142">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="d9f83-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d9f83-143">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="d9f83-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies cutting at the edge of the image -->
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!--Specifies cutting for standard media size -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!--Specifies no job roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="d9f83-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9f83-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9f83-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d9f83-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




