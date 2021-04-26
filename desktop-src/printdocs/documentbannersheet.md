---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef61001e45178989d6f89e17d8cc38b82c1354
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996303"
---
# <a name="documentbannersheet"></a><span data-ttu-id="a232a-104">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="a232a-104">DocumentBannerSheet</span></span>

<span data-ttu-id="a232a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a232a-105">This topic is not current.</span></span> <span data-ttu-id="a232a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a232a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a232a-107">Descreve a folha de faixa a ser impressa para um determinado documento.</span><span class="sxs-lookup"><span data-stu-id="a232a-107">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="a232a-108">A folha de faixa deve ser saída no PageMediaSize padrão, usando o PageMediaType padrão.</span><span class="sxs-lookup"><span data-stu-id="a232a-108">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="a232a-109">A folha de faixa também deve ser isolada do restante do documento.</span><span class="sxs-lookup"><span data-stu-id="a232a-109">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="a232a-110">Isso significa que todas as opções de acabamento ou de processamento de documentos (como DocumentDuplex, DocumentStaple ou Documentbinding) não devem incluir a folha de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="a232a-110">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="a232a-111">A folha de faixa pode ou não ser isolada do restante do trabalho.</span><span class="sxs-lookup"><span data-stu-id="a232a-111">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="a232a-112">Isso significa que qualquer trabalho de acabamento ou opções de processamento pode incluir a folha de cabeçalho do documento.</span><span class="sxs-lookup"><span data-stu-id="a232a-112">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="a232a-113">A folha de faixa deve ocorrer como a primeira planilha do documento.</span><span class="sxs-lookup"><span data-stu-id="a232a-113">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="a232a-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a232a-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a232a-115">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a232a-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="a232a-116">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a232a-116">Element Information</span></span>



| <span data-ttu-id="a232a-117">Nome</span><span class="sxs-lookup"><span data-stu-id="a232a-117">Name</span></span> | <span data-ttu-id="a232a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a232a-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a232a-119">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a232a-119">Element Type</span></span> <br/>   | <span data-ttu-id="a232a-120">Recurso</span><span class="sxs-lookup"><span data-stu-id="a232a-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a232a-121">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a232a-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a232a-122">Documento</span><span class="sxs-lookup"><span data-stu-id="a232a-122">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a232a-123">Observações</span><span class="sxs-lookup"><span data-stu-id="a232a-123">Notes</span></span> <br/>          | <span data-ttu-id="a232a-124">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="a232a-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="a232a-125">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="a232a-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="a232a-126">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="a232a-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="a232a-127">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="a232a-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="a232a-128">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a232a-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a232a-129">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a232a-129">Structural Content</span></span>

<span data-ttu-id="a232a-130">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a232a-130">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="a232a-131">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="a232a-131">Structure Variables</span></span>

<span data-ttu-id="a232a-132">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a232a-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a232a-133">Nome</span><span class="sxs-lookup"><span data-stu-id="a232a-133">Name</span></span>                               | <span data-ttu-id="a232a-134">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a232a-134">Data type</span></span>         | <span data-ttu-id="a232a-135">Unidade</span><span class="sxs-lookup"><span data-stu-id="a232a-135">Unit</span></span>                   | <span data-ttu-id="a232a-136">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="a232a-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a232a-137">Resumo</span><span class="sxs-lookup"><span data-stu-id="a232a-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a232a-138">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a232a-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a232a-139">string</span><span class="sxs-lookup"><span data-stu-id="a232a-139">string</span></span><br/> | <span data-ttu-id="a232a-140">characters</span><span class="sxs-lookup"><span data-stu-id="a232a-140">characters</span></span> <br/> | <span data-ttu-id="a232a-141">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a232a-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a232a-142">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="a232a-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a232a-143">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="a232a-143">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="a232a-144">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a232a-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a232a-145">string</span><span class="sxs-lookup"><span data-stu-id="a232a-145">string</span></span><br/> | <span data-ttu-id="a232a-146">N/D</span><span class="sxs-lookup"><span data-stu-id="a232a-146">n/a</span></span><br/>         | <span data-ttu-id="a232a-147">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="a232a-147">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="a232a-148">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a232a-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a232a-149">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a232a-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a232a-150">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="a232a-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a232a-151">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="a232a-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a232a-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a232a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a232a-153">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a232a-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




