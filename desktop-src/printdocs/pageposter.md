---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46cad46abcad7541f1282d691c950211bb7670c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996083"
---
# <a name="pageposter"></a><span data-ttu-id="2e47f-104">PagePoster</span><span class="sxs-lookup"><span data-stu-id="2e47f-104">PagePoster</span></span>

<span data-ttu-id="2e47f-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="2e47f-105">This topic is not current.</span></span> <span data-ttu-id="2e47f-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2e47f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e47f-107">Descreve a saída de uma única página para várias folhas de mídia físicas.</span><span class="sxs-lookup"><span data-stu-id="2e47f-107">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="2e47f-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2e47f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2e47f-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="2e47f-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2e47f-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2e47f-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2e47f-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2e47f-111">Element Information</span></span>



| <span data-ttu-id="2e47f-112">Nome</span><span class="sxs-lookup"><span data-stu-id="2e47f-112">Name</span></span> | <span data-ttu-id="2e47f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2e47f-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="2e47f-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2e47f-114">Element Type</span></span> <br/>   | <span data-ttu-id="2e47f-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="2e47f-115">Feature</span></span><br/> |
| <span data-ttu-id="2e47f-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="2e47f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2e47f-117">?</span><span class="sxs-lookup"><span data-stu-id="2e47f-117">Page</span></span><br/>    |
| <span data-ttu-id="2e47f-118">Observações</span><span class="sxs-lookup"><span data-stu-id="2e47f-118">Notes</span></span> <br/>          | <span data-ttu-id="2e47f-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e47f-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="2e47f-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="2e47f-120">Structural Content</span></span>

<span data-ttu-id="2e47f-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="2e47f-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2e47f-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="2e47f-122">Structure Variables</span></span>

<span data-ttu-id="2e47f-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="2e47f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2e47f-124">Nome</span><span class="sxs-lookup"><span data-stu-id="2e47f-124">Name</span></span>                               | <span data-ttu-id="2e47f-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2e47f-125">Data type</span></span>          | <span data-ttu-id="2e47f-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="2e47f-126">Unit</span></span>                  | <span data-ttu-id="2e47f-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="2e47f-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2e47f-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="2e47f-128">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2e47f-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2e47f-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="2e47f-130">string</span><span class="sxs-lookup"><span data-stu-id="2e47f-130">string</span></span><br/>  | <span data-ttu-id="2e47f-131">characters</span><span class="sxs-lookup"><span data-stu-id="2e47f-131">characters</span></span><br/> | <span data-ttu-id="2e47f-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="2e47f-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2e47f-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="2e47f-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2e47f-134">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="2e47f-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="2e47f-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2e47f-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2e47f-136">string</span><span class="sxs-lookup"><span data-stu-id="2e47f-136">string</span></span><br/>  | <span data-ttu-id="2e47f-137">N/D</span><span class="sxs-lookup"><span data-stu-id="2e47f-137">n/a</span></span><br/>        | <span data-ttu-id="2e47f-138">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="2e47f-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="2e47f-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="2e47f-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="2e47f-140">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="2e47f-140">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="2e47f-141">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="2e47f-141">integer</span></span><br/> | <span data-ttu-id="2e47f-142">páginas</span><span class="sxs-lookup"><span data-stu-id="2e47f-142">pages</span></span><br/>      | <span data-ttu-id="2e47f-143">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="2e47f-143">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="2e47f-144">Especifica o número de folhas físicas por página lógica.</span><span class="sxs-lookup"><span data-stu-id="2e47f-144">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2e47f-145">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2e47f-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2e47f-146">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="2e47f-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2e47f-147">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="2e47f-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2e47f-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e47f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e47f-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="2e47f-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




