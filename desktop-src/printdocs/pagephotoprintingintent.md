---
description: Revise o elemento pagePhotoPrintingIntent configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1cf9ae587062efc68b953f5931b55147940b1b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548974"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="1eddd-105">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="1eddd-105">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="1eddd-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="1eddd-106">This topic is not current.</span></span> <span data-ttu-id="1eddd-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1eddd-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1eddd-108">Indica uma intenção de alto nível para o driver para população de configurações de impressão de fotos.</span><span class="sxs-lookup"><span data-stu-id="1eddd-108">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="1eddd-109">Essas configurações lidam com a qualidade de saída esperada que um usuário pode especificar ao imprimir fotos.</span><span class="sxs-lookup"><span data-stu-id="1eddd-109">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="1eddd-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1eddd-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="1eddd-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="1eddd-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="1eddd-112">Conteúdo XML</span><span class="sxs-lookup"><span data-stu-id="1eddd-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1eddd-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1eddd-113">Element Information</span></span>



| <span data-ttu-id="1eddd-114">Nome</span><span class="sxs-lookup"><span data-stu-id="1eddd-114">Name</span></span> | <span data-ttu-id="1eddd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1eddd-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1eddd-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1eddd-116">Element Type</span></span> <br/>   | <span data-ttu-id="1eddd-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="1eddd-117">Feature</span></span><br/> |
| <span data-ttu-id="1eddd-118">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="1eddd-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1eddd-119">Página</span><span class="sxs-lookup"><span data-stu-id="1eddd-119">Page</span></span><br/>    |
| <span data-ttu-id="1eddd-120">Observações</span><span class="sxs-lookup"><span data-stu-id="1eddd-120">Notes</span></span> <br/>          | <span data-ttu-id="1eddd-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1eddd-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1eddd-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="1eddd-122">Structural Content</span></span>

<span data-ttu-id="1eddd-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="1eddd-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1eddd-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="1eddd-124">Structure Variables</span></span>

<span data-ttu-id="1eddd-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="1eddd-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1eddd-126">Nome</span><span class="sxs-lookup"><span data-stu-id="1eddd-126">Name</span></span>                               | <span data-ttu-id="1eddd-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1eddd-127">Data type</span></span>         | <span data-ttu-id="1eddd-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="1eddd-128">Unit</span></span>                  | <span data-ttu-id="1eddd-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="1eddd-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1eddd-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="1eddd-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1eddd-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="1eddd-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1eddd-132">string</span><span class="sxs-lookup"><span data-stu-id="1eddd-132">string</span></span><br/> | <span data-ttu-id="1eddd-133">characters</span><span class="sxs-lookup"><span data-stu-id="1eddd-133">characters</span></span><br/> | <span data-ttu-id="1eddd-134">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="1eddd-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1eddd-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="1eddd-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1eddd-136">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="1eddd-136">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="1eddd-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1eddd-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1eddd-138">string</span><span class="sxs-lookup"><span data-stu-id="1eddd-138">string</span></span><br/> | <span data-ttu-id="1eddd-139">n/d</span><span class="sxs-lookup"><span data-stu-id="1eddd-139">n/a</span></span><br/>        | <span data-ttu-id="1eddd-140">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="1eddd-140">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="1eddd-141">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="1eddd-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1eddd-142">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="1eddd-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1eddd-143">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="1eddd-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1eddd-144">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="1eddd-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1eddd-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1eddd-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eddd-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="1eddd-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




