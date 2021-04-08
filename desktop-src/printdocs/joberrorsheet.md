---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef9d613bf3b3af980b5cb8e916eac115cd1a0cb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "103837714"
---
# <a name="joberrorsheet"></a><span data-ttu-id="78c3f-104">JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="78c3f-104">JobErrorSheet</span></span>

<span data-ttu-id="78c3f-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="78c3f-105">This topic is not current.</span></span> <span data-ttu-id="78c3f-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="78c3f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="78c3f-107">Descreve a saída da planilha de erro.</span><span class="sxs-lookup"><span data-stu-id="78c3f-107">Describes the error sheet output.</span></span> <span data-ttu-id="78c3f-108">Todo o trabalho terá uma única folha de erro.</span><span class="sxs-lookup"><span data-stu-id="78c3f-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="78c3f-109">A folha de erros deve ser saída no PageMediaSize padrão e usando o PageMediaType padrão.</span><span class="sxs-lookup"><span data-stu-id="78c3f-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="78c3f-110">A folha de erros deve ser isolada do restante do trabalho.</span><span class="sxs-lookup"><span data-stu-id="78c3f-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="78c3f-111">Isso significa que qualquer opção de acabamento ou de processamento (como JobDuplex, JobStaple ou JobBinding) não deve incluir a planilha de erros.</span><span class="sxs-lookup"><span data-stu-id="78c3f-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="78c3f-112">A folha de erros deve ocorrer como a planilha final do trabalho.</span><span class="sxs-lookup"><span data-stu-id="78c3f-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="78c3f-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="78c3f-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="78c3f-114">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="78c3f-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="78c3f-115">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="78c3f-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="78c3f-116">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="78c3f-116">Element Information</span></span>



| <span data-ttu-id="78c3f-117">Nome</span><span class="sxs-lookup"><span data-stu-id="78c3f-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c3f-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="78c3f-118">Element Type</span></span> <br/>   | <span data-ttu-id="78c3f-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="78c3f-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="78c3f-120">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="78c3f-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="78c3f-121">Trabalho</span><span class="sxs-lookup"><span data-stu-id="78c3f-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="78c3f-122">Observações</span><span class="sxs-lookup"><span data-stu-id="78c3f-122">Notes</span></span> <br/>          | <span data-ttu-id="78c3f-123">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="78c3f-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="78c3f-124">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="78c3f-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="78c3f-125">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="78c3f-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="78c3f-126">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="78c3f-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="78c3f-127">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="78c3f-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="78c3f-128">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="78c3f-128">Structural Content</span></span>

<span data-ttu-id="78c3f-129">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="78c3f-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="78c3f-130">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="78c3f-130">Structure Variables</span></span>

<span data-ttu-id="78c3f-131">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="78c3f-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="78c3f-132">Nome</span><span class="sxs-lookup"><span data-stu-id="78c3f-132">Name</span></span>                                             | <span data-ttu-id="78c3f-133">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="78c3f-133">Data type</span></span>         | <span data-ttu-id="78c3f-134">Unidade</span><span class="sxs-lookup"><span data-stu-id="78c3f-134">Unit</span></span>                  | <span data-ttu-id="78c3f-135">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="78c3f-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="78c3f-136">Resumo</span><span class="sxs-lookup"><span data-stu-id="78c3f-136">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="78c3f-137">\_ErrorSheetWhenOptionName\_</span><span class="sxs-lookup"><span data-stu-id="78c3f-137">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="78c3f-138">string</span><span class="sxs-lookup"><span data-stu-id="78c3f-138">string</span></span><br/> | <span data-ttu-id="78c3f-139">characters</span><span class="sxs-lookup"><span data-stu-id="78c3f-139">characters</span></span><br/> | <span data-ttu-id="78c3f-140">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="78c3f-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="78c3f-141">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="78c3f-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="78c3f-142">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="78c3f-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="78c3f-143">\_ErrorSheetWhenIdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="78c3f-143">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="78c3f-144">string</span><span class="sxs-lookup"><span data-stu-id="78c3f-144">string</span></span><br/> | <span data-ttu-id="78c3f-145">N/D</span><span class="sxs-lookup"><span data-stu-id="78c3f-145">n/a</span></span><br/>        | <span data-ttu-id="78c3f-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="78c3f-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="78c3f-147">Define os critérios de seleção da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="78c3f-147">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="78c3f-148">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="78c3f-148">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="78c3f-149">string</span><span class="sxs-lookup"><span data-stu-id="78c3f-149">string</span></span><br/> | <span data-ttu-id="78c3f-150">N/D</span><span class="sxs-lookup"><span data-stu-id="78c3f-150">n/a</span></span><br/>        | <span data-ttu-id="78c3f-151">Nome totalmente qualificado válido, conforme definido pelo https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="78c3f-151">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="78c3f-152">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="78c3f-152">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="78c3f-153">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="78c3f-153">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="78c3f-154">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="78c3f-154">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="78c3f-155">string</span><span class="sxs-lookup"><span data-stu-id="78c3f-155">string</span></span><br/> | <span data-ttu-id="78c3f-156">N/D</span><span class="sxs-lookup"><span data-stu-id="78c3f-156">n/a</span></span><br/>        | <span data-ttu-id="78c3f-157">True, False.</span><span class="sxs-lookup"><span data-stu-id="78c3f-157">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="78c3f-158">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="78c3f-158">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="78c3f-159">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="78c3f-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="78c3f-160">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="78c3f-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="78c3f-161">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="78c3f-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="78c3f-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78c3f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78c3f-163">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="78c3f-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




