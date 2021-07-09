---
description: Leia sobre o elemento configurável pelo usuário PageOrientation. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: Pageorientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f0af08fcd29f34bb55bd16b1eac50487e96ffb
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549114"
---
# <a name="pageorientation"></a><span data-ttu-id="9c541-105">Pageorientation</span><span class="sxs-lookup"><span data-stu-id="9c541-105">PageOrientation</span></span>

<span data-ttu-id="9c541-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="9c541-106">This topic is not current.</span></span> <span data-ttu-id="9c541-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9c541-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9c541-108">Descreve a orientação da folha de mídia física.</span><span class="sxs-lookup"><span data-stu-id="9c541-108">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="9c541-109">Opção</span><span class="sxs-lookup"><span data-stu-id="9c541-109">Option</span></span>                       | <span data-ttu-id="9c541-110">Definição</span><span class="sxs-lookup"><span data-stu-id="9c541-110">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c541-111">Paisagem</span><span class="sxs-lookup"><span data-stu-id="9c541-111">Landscape</span></span> <br/>        | <span data-ttu-id="9c541-112">O conteúdo é girado na página 90?? graus CCW em relação à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="9c541-112">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="9c541-113">Retrato</span><span class="sxs-lookup"><span data-stu-id="9c541-113">Portrait</span></span> <br/>         | <span data-ttu-id="9c541-114">Orientação Padrão.</span><span class="sxs-lookup"><span data-stu-id="9c541-114">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="9c541-115">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="9c541-115">ReverseLandscape</span></span> <br/> | <span data-ttu-id="9c541-116">O conteúdo é girado na página 270?? graus CCW em relação à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="9c541-116">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="9c541-117">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="9c541-117">ReversePortrait</span></span> <br/>  | <span data-ttu-id="9c541-118">O conteúdo é girado na página 180?? graus relativos à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="9c541-118">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="9c541-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9c541-119">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9c541-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="9c541-120">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9c541-121">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="9c541-121">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9c541-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9c541-122">Element Information</span></span>



| <span data-ttu-id="9c541-123">Nome</span><span class="sxs-lookup"><span data-stu-id="9c541-123">Name</span></span> | <span data-ttu-id="9c541-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9c541-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c541-125">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9c541-125">Element Type</span></span> <br/>   | <span data-ttu-id="9c541-126">Recurso</span><span class="sxs-lookup"><span data-stu-id="9c541-126">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="9c541-127">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="9c541-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9c541-128">Página</span><span class="sxs-lookup"><span data-stu-id="9c541-128">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="9c541-129">Observações</span><span class="sxs-lookup"><span data-stu-id="9c541-129">Notes</span></span> <br/>          | <span data-ttu-id="9c541-130">Se um Dispositivo de Impressora puder dar suporte apenas a uma direção paisagem e essa direção for chamada de "Paisagem Inversa", a orientação da página ainda será considerada "Paisagem".</span><span class="sxs-lookup"><span data-stu-id="9c541-130">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9c541-131">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="9c541-131">Structural Content</span></span>

<span data-ttu-id="9c541-132">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="9c541-132">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="9c541-133">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="9c541-133">Structure Variables</span></span>

<span data-ttu-id="9c541-134">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="9c541-134">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9c541-135">Nome</span><span class="sxs-lookup"><span data-stu-id="9c541-135">Name</span></span>                               | <span data-ttu-id="9c541-136">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9c541-136">Data type</span></span>         | <span data-ttu-id="9c541-137">Unidade</span><span class="sxs-lookup"><span data-stu-id="9c541-137">Unit</span></span>                  | <span data-ttu-id="9c541-138">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="9c541-138">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9c541-139">Resumo</span><span class="sxs-lookup"><span data-stu-id="9c541-139">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9c541-140">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="9c541-140">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9c541-141">string</span><span class="sxs-lookup"><span data-stu-id="9c541-141">string</span></span><br/> | <span data-ttu-id="9c541-142">characters</span><span class="sxs-lookup"><span data-stu-id="9c541-142">characters</span></span><br/> | <span data-ttu-id="9c541-143">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="9c541-143">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9c541-144">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="9c541-144">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9c541-145">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="9c541-145">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9c541-146">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9c541-146">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9c541-147">string</span><span class="sxs-lookup"><span data-stu-id="9c541-147">string</span></span><br/> | <span data-ttu-id="9c541-148">n/d</span><span class="sxs-lookup"><span data-stu-id="9c541-148">n/a</span></span><br/>        | <span data-ttu-id="9c541-149">True, False.</span><span class="sxs-lookup"><span data-stu-id="9c541-149">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9c541-150">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="9c541-150">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9c541-151">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="9c541-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9c541-152">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="9c541-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9c541-153">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="9c541-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9c541-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c541-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c541-155">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="9c541-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




