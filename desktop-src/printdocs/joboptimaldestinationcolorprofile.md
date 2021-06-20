---
description: Saiba mais sobre o elemento JobOptimalDestinationColorProfile que especifica o perfil de cor ideal, considerando a configuração atual do dispositivo.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7ad2ea269594809b047922ea4f6c99b924e5ae
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408839"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="bdb98-103">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="bdb98-103">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="bdb98-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="bdb98-104">This topic is not current.</span></span> <span data-ttu-id="bdb98-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bdb98-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bdb98-106">Especifica o perfil de cor ideal de acordo com a configuração atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdb98-106">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="bdb98-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="bdb98-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bdb98-108">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="bdb98-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bdb98-109">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="bdb98-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bdb98-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="bdb98-110">Element Information</span></span>



| <span data-ttu-id="bdb98-111">Name</span><span class="sxs-lookup"><span data-stu-id="bdb98-111">Name</span></span> | <span data-ttu-id="bdb98-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bdb98-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="bdb98-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bdb98-113">Element Type</span></span> <br/>   | <span data-ttu-id="bdb98-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="bdb98-114">Property</span></span><br/> |
| <span data-ttu-id="bdb98-115">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="bdb98-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bdb98-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="bdb98-116">Job</span></span><br/>      |
| <span data-ttu-id="bdb98-117">Observações</span><span class="sxs-lookup"><span data-stu-id="bdb98-117">Notes</span></span> <br/>          | <span data-ttu-id="bdb98-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bdb98-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="bdb98-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="bdb98-119">Structural Content</span></span>

<span data-ttu-id="bdb98-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="bdb98-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="bdb98-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="bdb98-121">Structure Variables</span></span>

<span data-ttu-id="bdb98-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="bdb98-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bdb98-123">Nome</span><span class="sxs-lookup"><span data-stu-id="bdb98-123">Name</span></span>                            | <span data-ttu-id="bdb98-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bdb98-124">Data type</span></span>         | <span data-ttu-id="bdb98-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="bdb98-125">Unit</span></span>           | <span data-ttu-id="bdb98-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="bdb98-126">Supported values</span></span>          | <span data-ttu-id="bdb98-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="bdb98-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="bdb98-128">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="bdb98-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="bdb98-129">string</span><span class="sxs-lookup"><span data-stu-id="bdb98-129">string</span></span><br/> | <span data-ttu-id="bdb98-130">n/d</span><span class="sxs-lookup"><span data-stu-id="bdb98-130">n/a</span></span><br/> | <span data-ttu-id="bdb98-131">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="bdb98-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="bdb98-132">Especifica o perfil de cor.</span><span class="sxs-lookup"><span data-stu-id="bdb98-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="bdb98-133">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="bdb98-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="bdb98-134">string</span><span class="sxs-lookup"><span data-stu-id="bdb98-134">string</span></span><br/> | <span data-ttu-id="bdb98-135">n/d</span><span class="sxs-lookup"><span data-stu-id="bdb98-135">n/a</span></span><br/> | <span data-ttu-id="bdb98-136">n/d</span><span class="sxs-lookup"><span data-stu-id="bdb98-136">n/a</span></span><br/>            | <span data-ttu-id="bdb98-137">Especifica o caminho do arquivo para o perfil.</span><span class="sxs-lookup"><span data-stu-id="bdb98-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="bdb98-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="bdb98-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="bdb98-139">string</span><span class="sxs-lookup"><span data-stu-id="bdb98-139">string</span></span><br/> | <span data-ttu-id="bdb98-140">n/d</span><span class="sxs-lookup"><span data-stu-id="bdb98-140">n/a</span></span><br/> | <span data-ttu-id="bdb98-141">n/d</span><span class="sxs-lookup"><span data-stu-id="bdb98-141">n/a</span></span><br/>            | <span data-ttu-id="bdb98-142">Contém conteúdo de dados de perfil.</span><span class="sxs-lookup"><span data-stu-id="bdb98-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bdb98-143">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="bdb98-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bdb98-144">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="bdb98-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bdb98-145">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="bdb98-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bdb98-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bdb98-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdb98-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="bdb98-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




