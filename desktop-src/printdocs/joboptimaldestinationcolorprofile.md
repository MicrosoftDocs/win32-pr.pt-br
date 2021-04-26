---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45630b2ddbe94f19905f01c508fc4d852d29566b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999244"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="38382-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="38382-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="38382-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="38382-105">This topic is not current.</span></span> <span data-ttu-id="38382-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="38382-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="38382-107">Especifica o perfil de cor ideal, considerando a configuração atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38382-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="38382-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="38382-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="38382-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="38382-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="38382-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="38382-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="38382-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="38382-111">Element Information</span></span>



| <span data-ttu-id="38382-112">Nome</span><span class="sxs-lookup"><span data-stu-id="38382-112">Name</span></span> | <span data-ttu-id="38382-113">Valor</span><span class="sxs-lookup"><span data-stu-id="38382-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="38382-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="38382-114">Element Type</span></span> <br/>   | <span data-ttu-id="38382-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="38382-115">Property</span></span><br/> |
| <span data-ttu-id="38382-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="38382-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="38382-117">Trabalho</span><span class="sxs-lookup"><span data-stu-id="38382-117">Job</span></span><br/>      |
| <span data-ttu-id="38382-118">Observações</span><span class="sxs-lookup"><span data-stu-id="38382-118">Notes</span></span> <br/>          | <span data-ttu-id="38382-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="38382-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="38382-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="38382-120">Structural Content</span></span>

<span data-ttu-id="38382-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="38382-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="38382-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="38382-122">Structure Variables</span></span>

<span data-ttu-id="38382-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="38382-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="38382-124">Nome</span><span class="sxs-lookup"><span data-stu-id="38382-124">Name</span></span>                            | <span data-ttu-id="38382-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="38382-125">Data type</span></span>         | <span data-ttu-id="38382-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="38382-126">Unit</span></span>           | <span data-ttu-id="38382-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="38382-127">Supported values</span></span>          | <span data-ttu-id="38382-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="38382-128">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="38382-129">\_Profilevalue\_</span><span class="sxs-lookup"><span data-stu-id="38382-129">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="38382-130">string</span><span class="sxs-lookup"><span data-stu-id="38382-130">string</span></span><br/> | <span data-ttu-id="38382-131">N/D</span><span class="sxs-lookup"><span data-stu-id="38382-131">n/a</span></span><br/> | <span data-ttu-id="38382-132">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="38382-132">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="38382-133">Especifica o perfil de cor.</span><span class="sxs-lookup"><span data-stu-id="38382-133">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="38382-134">\_Caminhovalue\_</span><span class="sxs-lookup"><span data-stu-id="38382-134">\_PathValue\_</span></span><br/>        | <span data-ttu-id="38382-135">string</span><span class="sxs-lookup"><span data-stu-id="38382-135">string</span></span><br/> | <span data-ttu-id="38382-136">N/D</span><span class="sxs-lookup"><span data-stu-id="38382-136">n/a</span></span><br/> | <span data-ttu-id="38382-137">N/D</span><span class="sxs-lookup"><span data-stu-id="38382-137">n/a</span></span><br/>            | <span data-ttu-id="38382-138">Especifica o caminho do arquivo para o perfil.</span><span class="sxs-lookup"><span data-stu-id="38382-138">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="38382-139">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="38382-139">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="38382-140">string</span><span class="sxs-lookup"><span data-stu-id="38382-140">string</span></span><br/> | <span data-ttu-id="38382-141">N/D</span><span class="sxs-lookup"><span data-stu-id="38382-141">n/a</span></span><br/> | <span data-ttu-id="38382-142">N/D</span><span class="sxs-lookup"><span data-stu-id="38382-142">n/a</span></span><br/>            | <span data-ttu-id="38382-143">Contém conteúdo de dados de perfil.</span><span class="sxs-lookup"><span data-stu-id="38382-143">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="38382-144">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="38382-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="38382-145">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="38382-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="38382-146">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="38382-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="38382-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38382-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38382-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="38382-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




