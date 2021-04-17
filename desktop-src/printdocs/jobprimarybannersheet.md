---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc44973b06dc99c86ca9d50717ca9bf2b6335fa
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105812083"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="ed034-104">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="ed034-104">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="ed034-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ed034-105">This topic is not current.</span></span> <span data-ttu-id="ed034-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ed034-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ed034-107">Descreve a folha de faixa a ser impressa para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ed034-107">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="ed034-108">A folha de faixa deve ser saída no PageMediaSize padrão e usando o PageMediaType padrão.</span><span class="sxs-lookup"><span data-stu-id="ed034-108">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="ed034-109">A folha de faixa deve ser isolada do restante do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ed034-109">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="ed034-110">Isso significa que qualquer opção de acabamento ou de processamento (como JobDuplexAllDocumentsContiguously, JobStapleAllDocuments ou JobBindAllDocuments) não deve incluir a folha de faixa.</span><span class="sxs-lookup"><span data-stu-id="ed034-110">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="ed034-111">A folha de faixa deve ocorrer como a primeira planilha do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ed034-111">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="ed034-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ed034-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ed034-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ed034-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ed034-114">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ed034-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ed034-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ed034-115">Element Information</span></span>



| <span data-ttu-id="ed034-116">Nome</span><span class="sxs-lookup"><span data-stu-id="ed034-116">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed034-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ed034-117">Element Type</span></span> <br/>   | <span data-ttu-id="ed034-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="ed034-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ed034-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="ed034-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ed034-120">Trabalho</span><span class="sxs-lookup"><span data-stu-id="ed034-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ed034-121">Observações</span><span class="sxs-lookup"><span data-stu-id="ed034-121">Notes</span></span> <br/>          | <span data-ttu-id="ed034-122">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="ed034-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="ed034-123">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="ed034-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="ed034-124">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="ed034-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="ed034-125">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="ed034-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="ed034-126">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ed034-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="ed034-127">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ed034-127">Structural Content</span></span>

<span data-ttu-id="ed034-128">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="ed034-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="ed034-129">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="ed034-129">Structure Variables</span></span>

<span data-ttu-id="ed034-130">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="ed034-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ed034-131">Nome</span><span class="sxs-lookup"><span data-stu-id="ed034-131">Name</span></span>                               | <span data-ttu-id="ed034-132">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ed034-132">Data type</span></span>         | <span data-ttu-id="ed034-133">Unidade</span><span class="sxs-lookup"><span data-stu-id="ed034-133">Unit</span></span>                  | <span data-ttu-id="ed034-134">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="ed034-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ed034-135">Resumo</span><span class="sxs-lookup"><span data-stu-id="ed034-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ed034-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ed034-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ed034-137">string</span><span class="sxs-lookup"><span data-stu-id="ed034-137">string</span></span><br/> | <span data-ttu-id="ed034-138">characters</span><span class="sxs-lookup"><span data-stu-id="ed034-138">characters</span></span><br/> | <span data-ttu-id="ed034-139">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ed034-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ed034-140">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="ed034-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ed034-141">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="ed034-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ed034-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ed034-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ed034-143">string</span><span class="sxs-lookup"><span data-stu-id="ed034-143">string</span></span><br/> | <span data-ttu-id="ed034-144">N/D</span><span class="sxs-lookup"><span data-stu-id="ed034-144">n/a</span></span><br/>        | <span data-ttu-id="ed034-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="ed034-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ed034-146">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="ed034-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ed034-147">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ed034-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ed034-148">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="ed034-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ed034-149">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="ed034-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="ed034-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed034-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed034-151">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ed034-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




