---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954f67df5720e19de39d2c1c752c6d9eb860a502
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "103930257"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="88616-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="88616-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="88616-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="88616-105">This topic is not current.</span></span> <span data-ttu-id="88616-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="88616-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="88616-107">Especifica o perfil de cor ideal, considerando a configuração atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="88616-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="88616-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="88616-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="88616-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="88616-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="88616-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="88616-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="88616-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="88616-111">Element Information</span></span>



| <span data-ttu-id="88616-112">Nome</span><span class="sxs-lookup"><span data-stu-id="88616-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="88616-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="88616-113">Element Type</span></span> <br/>   | <span data-ttu-id="88616-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="88616-114">Property</span></span><br/> |
| <span data-ttu-id="88616-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="88616-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="88616-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="88616-116">Job</span></span><br/>      |
| <span data-ttu-id="88616-117">Observações</span><span class="sxs-lookup"><span data-stu-id="88616-117">Notes</span></span> <br/>          | <span data-ttu-id="88616-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88616-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="88616-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="88616-119">Structural Content</span></span>

<span data-ttu-id="88616-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="88616-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="88616-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="88616-121">Structure Variables</span></span>

<span data-ttu-id="88616-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="88616-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="88616-123">Nome</span><span class="sxs-lookup"><span data-stu-id="88616-123">Name</span></span>                            | <span data-ttu-id="88616-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="88616-124">Data type</span></span>         | <span data-ttu-id="88616-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="88616-125">Unit</span></span>           | <span data-ttu-id="88616-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="88616-126">Supported values</span></span>          | <span data-ttu-id="88616-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="88616-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="88616-128">\_Profilevalue\_</span><span class="sxs-lookup"><span data-stu-id="88616-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="88616-129">string</span><span class="sxs-lookup"><span data-stu-id="88616-129">string</span></span><br/> | <span data-ttu-id="88616-130">N/D</span><span class="sxs-lookup"><span data-stu-id="88616-130">n/a</span></span><br/> | <span data-ttu-id="88616-131">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="88616-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="88616-132">Especifica o perfil de cor.</span><span class="sxs-lookup"><span data-stu-id="88616-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="88616-133">\_Caminhovalue\_</span><span class="sxs-lookup"><span data-stu-id="88616-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="88616-134">string</span><span class="sxs-lookup"><span data-stu-id="88616-134">string</span></span><br/> | <span data-ttu-id="88616-135">N/D</span><span class="sxs-lookup"><span data-stu-id="88616-135">n/a</span></span><br/> | <span data-ttu-id="88616-136">N/D</span><span class="sxs-lookup"><span data-stu-id="88616-136">n/a</span></span><br/>            | <span data-ttu-id="88616-137">Especifica o caminho do arquivo para o perfil.</span><span class="sxs-lookup"><span data-stu-id="88616-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="88616-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="88616-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="88616-139">string</span><span class="sxs-lookup"><span data-stu-id="88616-139">string</span></span><br/> | <span data-ttu-id="88616-140">N/D</span><span class="sxs-lookup"><span data-stu-id="88616-140">n/a</span></span><br/> | <span data-ttu-id="88616-141">N/D</span><span class="sxs-lookup"><span data-stu-id="88616-141">n/a</span></span><br/>            | <span data-ttu-id="88616-142">Contém conteúdo de dados de perfil.</span><span class="sxs-lookup"><span data-stu-id="88616-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="88616-143">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="88616-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="88616-144">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="88616-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="88616-145">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="88616-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="88616-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88616-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88616-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="88616-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




