---
description: Obter informações sobre o elemento configurável pelo usuário do PagePoster. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b8bb7b57074fe058c7cc5be8dd609577ceb6c1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548964"
---
# <a name="pageposter"></a><span data-ttu-id="c4df8-105">PagePoster</span><span class="sxs-lookup"><span data-stu-id="c4df8-105">PagePoster</span></span>

<span data-ttu-id="c4df8-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c4df8-106">This topic is not current.</span></span> <span data-ttu-id="c4df8-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c4df8-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c4df8-108">Descreve a saída de uma única página para várias planilhas de mídia física.</span><span class="sxs-lookup"><span data-stu-id="c4df8-108">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="c4df8-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c4df8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c4df8-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c4df8-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c4df8-111">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="c4df8-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c4df8-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c4df8-112">Element Information</span></span>



| <span data-ttu-id="c4df8-113">Nome</span><span class="sxs-lookup"><span data-stu-id="c4df8-113">Name</span></span> | <span data-ttu-id="c4df8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c4df8-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c4df8-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c4df8-115">Element Type</span></span> <br/>   | <span data-ttu-id="c4df8-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="c4df8-116">Feature</span></span><br/> |
| <span data-ttu-id="c4df8-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="c4df8-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c4df8-118">Página</span><span class="sxs-lookup"><span data-stu-id="c4df8-118">Page</span></span><br/>    |
| <span data-ttu-id="c4df8-119">Observações</span><span class="sxs-lookup"><span data-stu-id="c4df8-119">Notes</span></span> <br/>          | <span data-ttu-id="c4df8-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c4df8-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c4df8-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c4df8-121">Structural Content</span></span>

<span data-ttu-id="c4df8-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="c4df8-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_SheetsPerPageValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="c4df8-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="c4df8-123">Structure Variables</span></span>

<span data-ttu-id="c4df8-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="c4df8-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c4df8-125">Nome</span><span class="sxs-lookup"><span data-stu-id="c4df8-125">Name</span></span>                               | <span data-ttu-id="c4df8-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c4df8-126">Data type</span></span>          | <span data-ttu-id="c4df8-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="c4df8-127">Unit</span></span>                  | <span data-ttu-id="c4df8-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="c4df8-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c4df8-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="c4df8-129">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c4df8-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="c4df8-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c4df8-131">string</span><span class="sxs-lookup"><span data-stu-id="c4df8-131">string</span></span><br/>  | <span data-ttu-id="c4df8-132">characters</span><span class="sxs-lookup"><span data-stu-id="c4df8-132">characters</span></span><br/> | <span data-ttu-id="c4df8-133">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="c4df8-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c4df8-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="c4df8-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c4df8-135">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="c4df8-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="c4df8-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c4df8-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c4df8-137">string</span><span class="sxs-lookup"><span data-stu-id="c4df8-137">string</span></span><br/>  | <span data-ttu-id="c4df8-138">n/d</span><span class="sxs-lookup"><span data-stu-id="c4df8-138">n/a</span></span><br/>        | <span data-ttu-id="c4df8-139">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="c4df8-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="c4df8-140">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="c4df8-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="c4df8-141">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="c4df8-141">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="c4df8-142">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="c4df8-142">integer</span></span><br/> | <span data-ttu-id="c4df8-143">páginas</span><span class="sxs-lookup"><span data-stu-id="c4df8-143">pages</span></span><br/>      | <span data-ttu-id="c4df8-144">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="c4df8-144">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="c4df8-145">Especifica o número de folhas físicas por página lógica.</span><span class="sxs-lookup"><span data-stu-id="c4df8-145">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c4df8-146">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="c4df8-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c4df8-147">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="c4df8-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c4df8-148">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="c4df8-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies media sheets per page. -->
  <psf:Option>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="c4df8-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4df8-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4df8-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c4df8-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




