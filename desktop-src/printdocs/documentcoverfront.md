---
description: Saiba mais sobre o elemento configurável pelo usuário DocumentCoverFront. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301b67c9a741caa48024646854b208ac5dffbb20
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119821"
---
# <a name="documentcoverfront"></a><span data-ttu-id="bbd9b-105">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="bbd9b-105">DocumentCoverFront</span></span>

<span data-ttu-id="bbd9b-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-106">This topic is not current.</span></span> <span data-ttu-id="bbd9b-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bbd9b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bbd9b-108">Descreve a folha de cobertura frontal (início).</span><span class="sxs-lookup"><span data-stu-id="bbd9b-108">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="bbd9b-109">Cada documento terá uma planilha separada.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-109">Each document will have a separate sheet.</span></span> <span data-ttu-id="bbd9b-110">A folha de cobertura deve ser impressa em PageMediaSize e PageMediaType usados para a primeira página do documento.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-110">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="bbd9b-111">A folha de cobertura deve ser integrada às opções de processamento (como DocumentDuplex, DocumentNUp) conforme indicado pela Opção especificada.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-111">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="bbd9b-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="bbd9b-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bbd9b-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="bbd9b-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bbd9b-114">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="bbd9b-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bbd9b-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="bbd9b-115">Element Information</span></span>



| <span data-ttu-id="bbd9b-116">Nome</span><span class="sxs-lookup"><span data-stu-id="bbd9b-116">Name</span></span> | <span data-ttu-id="bbd9b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bbd9b-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd9b-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bbd9b-118">Element Type</span></span> <br/>   | <span data-ttu-id="bbd9b-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="bbd9b-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="bbd9b-120">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="bbd9b-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bbd9b-121">Documento</span><span class="sxs-lookup"><span data-stu-id="bbd9b-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bbd9b-122">Observações</span><span class="sxs-lookup"><span data-stu-id="bbd9b-122">Notes</span></span> <br/>          | <span data-ttu-id="bbd9b-123">Os consumidores compatíveis com XPS DEVEM impor que uma referência de URI a um recurso, como uma imagem ou perfil de cor em um documento Recursos de Impressão ou PrintTicket, DEVE se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote do Documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="bbd9b-124">Um consumidor XPS compatível NÃO DEVE usar um URI que não está em conformidade com a sintaxe de nome da parte.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="bbd9b-125">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="bbd9b-126">URIs que são referenciados em um documento Funcionalidades de Impressão ou PrintTicket NÃO DEVEM ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="bbd9b-127">Isso não é seguro, pois eles podem não ser resolvidos conforme o esperado e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="bbd9b-128">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="bbd9b-128">Structural Content</span></span>

<span data-ttu-id="bbd9b-129">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="bbd9b-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="bbd9b-130">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="bbd9b-130">Structure Variables</span></span>

<span data-ttu-id="bbd9b-131">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bbd9b-132">Nome</span><span class="sxs-lookup"><span data-stu-id="bbd9b-132">Name</span></span>                               | <span data-ttu-id="bbd9b-133">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bbd9b-133">Data type</span></span>         | <span data-ttu-id="bbd9b-134">Unidade</span><span class="sxs-lookup"><span data-stu-id="bbd9b-134">Unit</span></span>                  | <span data-ttu-id="bbd9b-135">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="bbd9b-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bbd9b-136">Resumo</span><span class="sxs-lookup"><span data-stu-id="bbd9b-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bbd9b-137">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="bbd9b-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bbd9b-138">string</span><span class="sxs-lookup"><span data-stu-id="bbd9b-138">string</span></span><br/> | <span data-ttu-id="bbd9b-139">characters</span><span class="sxs-lookup"><span data-stu-id="bbd9b-139">characters</span></span><br/> | <span data-ttu-id="bbd9b-140">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="bbd9b-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bbd9b-141">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bbd9b-142">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="bbd9b-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bbd9b-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bbd9b-144">string</span><span class="sxs-lookup"><span data-stu-id="bbd9b-144">string</span></span><br/> | <span data-ttu-id="bbd9b-145">n/d</span><span class="sxs-lookup"><span data-stu-id="bbd9b-145">n/a</span></span><br/>        | <span data-ttu-id="bbd9b-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bbd9b-147">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="bbd9b-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bbd9b-148">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="bbd9b-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bbd9b-149">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="bbd9b-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bbd9b-150">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="bbd9b-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="bbd9b-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbd9b-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbd9b-152">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="bbd9b-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




