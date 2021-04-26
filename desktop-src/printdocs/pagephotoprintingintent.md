---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d56a0b46c73bb3afdcefe96dc2131c861d5419
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997973"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="0bdab-104">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="0bdab-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="0bdab-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0bdab-105">This topic is not current.</span></span> <span data-ttu-id="0bdab-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0bdab-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0bdab-107">Indica uma intenção de alto nível para o driver para população de configurações de impressão de fotos.</span><span class="sxs-lookup"><span data-stu-id="0bdab-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="0bdab-108">Essas configurações lidam com a qualidade de saída esperada que um usuário pode especificar ao imprimir fotos.</span><span class="sxs-lookup"><span data-stu-id="0bdab-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="0bdab-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0bdab-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="0bdab-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="0bdab-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="0bdab-111">Conteúdo XML</span><span class="sxs-lookup"><span data-stu-id="0bdab-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0bdab-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0bdab-112">Element Information</span></span>



| <span data-ttu-id="0bdab-113">Nome</span><span class="sxs-lookup"><span data-stu-id="0bdab-113">Name</span></span> | <span data-ttu-id="0bdab-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0bdab-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0bdab-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0bdab-115">Element Type</span></span> <br/>   | <span data-ttu-id="0bdab-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="0bdab-116">Feature</span></span><br/> |
| <span data-ttu-id="0bdab-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="0bdab-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0bdab-118">?</span><span class="sxs-lookup"><span data-stu-id="0bdab-118">Page</span></span><br/>    |
| <span data-ttu-id="0bdab-119">Observações</span><span class="sxs-lookup"><span data-stu-id="0bdab-119">Notes</span></span> <br/>          | <span data-ttu-id="0bdab-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0bdab-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0bdab-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="0bdab-121">Structural Content</span></span>

<span data-ttu-id="0bdab-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="0bdab-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">  
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
    <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
  </psf:Property>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="0bdab-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="0bdab-123">Structure Variables</span></span>

<span data-ttu-id="0bdab-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="0bdab-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0bdab-125">Nome</span><span class="sxs-lookup"><span data-stu-id="0bdab-125">Name</span></span>                               | <span data-ttu-id="0bdab-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0bdab-126">Data type</span></span>         | <span data-ttu-id="0bdab-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="0bdab-127">Unit</span></span>                  | <span data-ttu-id="0bdab-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="0bdab-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0bdab-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="0bdab-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0bdab-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0bdab-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0bdab-131">string</span><span class="sxs-lookup"><span data-stu-id="0bdab-131">string</span></span><br/> | <span data-ttu-id="0bdab-132">characters</span><span class="sxs-lookup"><span data-stu-id="0bdab-132">characters</span></span><br/> | <span data-ttu-id="0bdab-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0bdab-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0bdab-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="0bdab-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0bdab-135">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="0bdab-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="0bdab-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0bdab-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0bdab-137">string</span><span class="sxs-lookup"><span data-stu-id="0bdab-137">string</span></span><br/> | <span data-ttu-id="0bdab-138">N/D</span><span class="sxs-lookup"><span data-stu-id="0bdab-138">n/a</span></span><br/>        | <span data-ttu-id="0bdab-139">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="0bdab-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="0bdab-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="0bdab-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0bdab-141">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0bdab-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0bdab-142">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="0bdab-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0bdab-143">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="0bdab-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- No Photoprinting Intent (Allows the application to specify no intent resolution.  (PrintTicket settings should not be altered) -->
  <psf:Option name="psk:None" />
  <!-- Best Quality Photoprinting (Provided mostly for marketing reasons; utilizes the highest capabilities of the device) -->
  <psf:Option name="psk:PhotoBest" />
  <!-- Draft Quality Photoprinting (Quick, low ink volume print for proofing purposes) -->
  <psf:Option name="psk:PhotoDraft" />
  <!-- Standard Quality Photoprinting (OEM suggested settings for standard photo-printing) -->
  <psf:Option name="psk:PhotoStandard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="0bdab-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0bdab-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bdab-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0bdab-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




