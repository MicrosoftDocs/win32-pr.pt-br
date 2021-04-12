---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f004329c217d4aab6ddc3c1d166037e7c7b5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104370842"
---
# <a name="pageorientation"></a><span data-ttu-id="0f2dd-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="0f2dd-104">PageOrientation</span></span>

<span data-ttu-id="0f2dd-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-105">This topic is not current.</span></span> <span data-ttu-id="0f2dd-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0f2dd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0f2dd-107">Descreve a orientação da folha de mídia física.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="0f2dd-108">Opção</span><span class="sxs-lookup"><span data-stu-id="0f2dd-108">Option</span></span>                       | <span data-ttu-id="0f2dd-109">Definição</span><span class="sxs-lookup"><span data-stu-id="0f2dd-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f2dd-110">Paisagem</span><span class="sxs-lookup"><span data-stu-id="0f2dd-110">Landscape</span></span> <br/>        | <span data-ttu-id="0f2dd-111">O conteúdo é girado na página 90? graus CCW em relação à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="0f2dd-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="0f2dd-112">Retrato</span><span class="sxs-lookup"><span data-stu-id="0f2dd-112">Portrait</span></span> <br/>         | <span data-ttu-id="0f2dd-113">Orientação padrão.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="0f2dd-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="0f2dd-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="0f2dd-115">O conteúdo é girado na página 270? graus CCW em relação à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="0f2dd-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="0f2dd-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="0f2dd-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="0f2dd-117">O conteúdo é girado na página 180? graus em relação à orientação padrão (retrato).</span><span class="sxs-lookup"><span data-stu-id="0f2dd-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="0f2dd-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0f2dd-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0f2dd-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="0f2dd-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0f2dd-120">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0f2dd-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0f2dd-121">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0f2dd-121">Element Information</span></span>



| <span data-ttu-id="0f2dd-122">Nome</span><span class="sxs-lookup"><span data-stu-id="0f2dd-122">Name</span></span>                       |                                                                                                                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f2dd-123">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0f2dd-123">Element Type</span></span> <br/>   | <span data-ttu-id="0f2dd-124">Recurso</span><span class="sxs-lookup"><span data-stu-id="0f2dd-124">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="0f2dd-125">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="0f2dd-125">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0f2dd-126">?</span><span class="sxs-lookup"><span data-stu-id="0f2dd-126">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="0f2dd-127">Observações</span><span class="sxs-lookup"><span data-stu-id="0f2dd-127">Notes</span></span> <br/>          | <span data-ttu-id="0f2dd-128">Se um dispositivo de impressora só puder dar suporte a uma direção de paisagem e essa direção for conhecida como "paisagem reversa", a orientação da página ainda será considerada "paisagem".</span><span class="sxs-lookup"><span data-stu-id="0f2dd-128">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0f2dd-129">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="0f2dd-129">Structural Content</span></span>

<span data-ttu-id="0f2dd-130">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="0f2dd-130">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0f2dd-131">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="0f2dd-131">Structure Variables</span></span>

<span data-ttu-id="0f2dd-132">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0f2dd-133">Nome</span><span class="sxs-lookup"><span data-stu-id="0f2dd-133">Name</span></span>                               | <span data-ttu-id="0f2dd-134">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0f2dd-134">Data type</span></span>         | <span data-ttu-id="0f2dd-135">Unidade</span><span class="sxs-lookup"><span data-stu-id="0f2dd-135">Unit</span></span>                  | <span data-ttu-id="0f2dd-136">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="0f2dd-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0f2dd-137">Resumo</span><span class="sxs-lookup"><span data-stu-id="0f2dd-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0f2dd-138">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0f2dd-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0f2dd-139">string</span><span class="sxs-lookup"><span data-stu-id="0f2dd-139">string</span></span><br/> | <span data-ttu-id="0f2dd-140">characters</span><span class="sxs-lookup"><span data-stu-id="0f2dd-140">characters</span></span><br/> | <span data-ttu-id="0f2dd-141">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0f2dd-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0f2dd-142">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0f2dd-143">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0f2dd-144">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0f2dd-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0f2dd-145">string</span><span class="sxs-lookup"><span data-stu-id="0f2dd-145">string</span></span><br/> | <span data-ttu-id="0f2dd-146">N/D</span><span class="sxs-lookup"><span data-stu-id="0f2dd-146">n/a</span></span><br/>        | <span data-ttu-id="0f2dd-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0f2dd-148">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0f2dd-149">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0f2dd-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0f2dd-150">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="0f2dd-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0f2dd-151">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="0f2dd-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0f2dd-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f2dd-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f2dd-153">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0f2dd-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




