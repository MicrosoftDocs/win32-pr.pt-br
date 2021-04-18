---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eda63fe0d801bc1039af2c514c284440b1be47
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105780415"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="15ec5-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="15ec5-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="15ec5-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="15ec5-105">This topic is not current.</span></span> <span data-ttu-id="15ec5-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="15ec5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="15ec5-107">Descreve o método de recorte para o rolo de papel.</span><span class="sxs-lookup"><span data-stu-id="15ec5-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="15ec5-108">O roll deve ser recortado no final do trabalho.</span><span class="sxs-lookup"><span data-stu-id="15ec5-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="15ec5-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="15ec5-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="15ec5-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="15ec5-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="15ec5-111">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="15ec5-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="15ec5-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="15ec5-112">Element Information</span></span>



| <span data-ttu-id="15ec5-113">Nome</span><span class="sxs-lookup"><span data-stu-id="15ec5-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="15ec5-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="15ec5-114">Element Type</span></span> <br/>   | <span data-ttu-id="15ec5-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="15ec5-115">Feature</span></span><br/> |
| <span data-ttu-id="15ec5-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="15ec5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="15ec5-117">Trabalho</span><span class="sxs-lookup"><span data-stu-id="15ec5-117">Job</span></span><br/>     |
| <span data-ttu-id="15ec5-118">Observações</span><span class="sxs-lookup"><span data-stu-id="15ec5-118">Notes</span></span> <br/>          | <span data-ttu-id="15ec5-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="15ec5-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="15ec5-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="15ec5-120">Structural Content</span></span>

<span data-ttu-id="15ec5-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="15ec5-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="15ec5-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="15ec5-122">Structure Variables</span></span>

<span data-ttu-id="15ec5-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="15ec5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="15ec5-124">Nome</span><span class="sxs-lookup"><span data-stu-id="15ec5-124">Name</span></span>                               | <span data-ttu-id="15ec5-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="15ec5-125">Data type</span></span>         | <span data-ttu-id="15ec5-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="15ec5-126">Unit</span></span>                  | <span data-ttu-id="15ec5-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="15ec5-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="15ec5-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="15ec5-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="15ec5-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="15ec5-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="15ec5-130">string</span><span class="sxs-lookup"><span data-stu-id="15ec5-130">string</span></span><br/> | <span data-ttu-id="15ec5-131">characters</span><span class="sxs-lookup"><span data-stu-id="15ec5-131">characters</span></span><br/> | <span data-ttu-id="15ec5-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="15ec5-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="15ec5-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="15ec5-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="15ec5-134">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="15ec5-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="15ec5-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="15ec5-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="15ec5-136">string</span><span class="sxs-lookup"><span data-stu-id="15ec5-136">string</span></span><br/> | <span data-ttu-id="15ec5-137">N/D</span><span class="sxs-lookup"><span data-stu-id="15ec5-137">n/a</span></span><br/>        | <span data-ttu-id="15ec5-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="15ec5-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="15ec5-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="15ec5-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="15ec5-140">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="15ec5-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="15ec5-141">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="15ec5-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="15ec5-142">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="15ec5-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="15ec5-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15ec5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15ec5-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="15ec5-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




