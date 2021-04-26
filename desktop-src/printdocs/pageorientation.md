---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a94fb97ad1e64c7f55fd9520ed8a648a74f550
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997533"
---
# <a name="pageorientation"></a><span data-ttu-id="97387-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="97387-104">PageOrientation</span></span>

<span data-ttu-id="97387-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="97387-105">This topic is not current.</span></span> <span data-ttu-id="97387-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="97387-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="97387-107">Descreve a orientação da folha de mídia física.</span><span class="sxs-lookup"><span data-stu-id="97387-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="97387-108">Opção</span><span class="sxs-lookup"><span data-stu-id="97387-108">Option</span></span>                       | <span data-ttu-id="97387-109">Definição</span><span class="sxs-lookup"><span data-stu-id="97387-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97387-110">Paisagem</span><span class="sxs-lookup"><span data-stu-id="97387-110">Landscape</span></span> <br/>        | <span data-ttu-id="97387-111">O conteúdo é girado na página 90? graus CCW em relação à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="97387-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="97387-112">Retrato</span><span class="sxs-lookup"><span data-stu-id="97387-112">Portrait</span></span> <br/>         | <span data-ttu-id="97387-113">Orientação padrão.</span><span class="sxs-lookup"><span data-stu-id="97387-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="97387-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="97387-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="97387-115">O conteúdo é girado na página 270? graus CCW em relação à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="97387-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="97387-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="97387-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="97387-117">O conteúdo é girado na página 180? graus em relação à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="97387-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="97387-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="97387-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="97387-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="97387-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="97387-120">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="97387-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="97387-121">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="97387-121">Element Information</span></span>



| <span data-ttu-id="97387-122">Nome</span><span class="sxs-lookup"><span data-stu-id="97387-122">Name</span></span> | <span data-ttu-id="97387-123">Valor</span><span class="sxs-lookup"><span data-stu-id="97387-123">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97387-124">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="97387-124">Element Type</span></span> <br/>   | <span data-ttu-id="97387-125">Recurso</span><span class="sxs-lookup"><span data-stu-id="97387-125">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="97387-126">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="97387-126">Scoping Prefix</span></span> <br/> | <span data-ttu-id="97387-127">?</span><span class="sxs-lookup"><span data-stu-id="97387-127">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="97387-128">Observações</span><span class="sxs-lookup"><span data-stu-id="97387-128">Notes</span></span> <br/>          | <span data-ttu-id="97387-129">Se um dispositivo de impressora só puder dar suporte a uma direção de paisagem e essa direção for conhecida como "paisagem reversa", a orientação da página ainda será considerada "paisagem".</span><span class="sxs-lookup"><span data-stu-id="97387-129">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="97387-130">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="97387-130">Structural Content</span></span>

<span data-ttu-id="97387-131">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="97387-131">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
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

## <a name="structure-variables"></a><span data-ttu-id="97387-132">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="97387-132">Structure Variables</span></span>

<span data-ttu-id="97387-133">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="97387-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="97387-134">Nome</span><span class="sxs-lookup"><span data-stu-id="97387-134">Name</span></span>                               | <span data-ttu-id="97387-135">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="97387-135">Data type</span></span>         | <span data-ttu-id="97387-136">Unidade</span><span class="sxs-lookup"><span data-stu-id="97387-136">Unit</span></span>                  | <span data-ttu-id="97387-137">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="97387-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="97387-138">Resumo</span><span class="sxs-lookup"><span data-stu-id="97387-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="97387-139">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="97387-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="97387-140">string</span><span class="sxs-lookup"><span data-stu-id="97387-140">string</span></span><br/> | <span data-ttu-id="97387-141">characters</span><span class="sxs-lookup"><span data-stu-id="97387-141">characters</span></span><br/> | <span data-ttu-id="97387-142">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="97387-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="97387-143">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="97387-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="97387-144">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="97387-144">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="97387-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="97387-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="97387-146">string</span><span class="sxs-lookup"><span data-stu-id="97387-146">string</span></span><br/> | <span data-ttu-id="97387-147">N/D</span><span class="sxs-lookup"><span data-stu-id="97387-147">n/a</span></span><br/>        | <span data-ttu-id="97387-148">True, False.</span><span class="sxs-lookup"><span data-stu-id="97387-148">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="97387-149">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="97387-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="97387-150">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="97387-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="97387-151">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="97387-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="97387-152">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="97387-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.??-->
  <psf:Option name="psk:Landscape" />
  <!-- Standard Orientation-->
  <psf:Option name="psk:Portrait" />
  <!-- Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReverseLandscape" />
  <!-- Content is rotated on the page 180??degrees relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReversePortrait" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="97387-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97387-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97387-154">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="97387-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




