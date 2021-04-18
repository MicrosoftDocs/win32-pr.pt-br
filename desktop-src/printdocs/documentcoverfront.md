---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b143ea6a3e1edd667d56619c190d99d1de93496f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105793364"
---
# <a name="documentcoverfront"></a><span data-ttu-id="a4071-104">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="a4071-104">DocumentCoverFront</span></span>

<span data-ttu-id="a4071-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a4071-105">This topic is not current.</span></span> <span data-ttu-id="a4071-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a4071-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4071-107">Descreve a folha de rosto frontal (começando).</span><span class="sxs-lookup"><span data-stu-id="a4071-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="a4071-108">Cada documento terá uma planilha separada.</span><span class="sxs-lookup"><span data-stu-id="a4071-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="a4071-109">A folha de rosto deve ser impressa no PageMediaSize e no PageMediaType usados para a primeira página do documento.</span><span class="sxs-lookup"><span data-stu-id="a4071-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="a4071-110">A folha de rosto deve ser integrada às opções de processamento (como DocumentDuplex, DocumentNUp), conforme indicado pela opção especificada.</span><span class="sxs-lookup"><span data-stu-id="a4071-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="a4071-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a4071-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a4071-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a4071-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a4071-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a4071-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a4071-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a4071-114">Element Information</span></span>



| <span data-ttu-id="a4071-115">Nome</span><span class="sxs-lookup"><span data-stu-id="a4071-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4071-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a4071-116">Element Type</span></span> <br/>   | <span data-ttu-id="a4071-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="a4071-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a4071-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a4071-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a4071-119">Documento</span><span class="sxs-lookup"><span data-stu-id="a4071-119">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a4071-120">Observações</span><span class="sxs-lookup"><span data-stu-id="a4071-120">Notes</span></span> <br/>          | <span data-ttu-id="a4071-121">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="a4071-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="a4071-122">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="a4071-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="a4071-123">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="a4071-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="a4071-124">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="a4071-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="a4071-125">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a4071-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a4071-126">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a4071-126">Structural Content</span></span>

<span data-ttu-id="a4071-127">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a4071-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a4071-128">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="a4071-128">Structure Variables</span></span>

<span data-ttu-id="a4071-129">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a4071-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a4071-130">Nome</span><span class="sxs-lookup"><span data-stu-id="a4071-130">Name</span></span>                               | <span data-ttu-id="a4071-131">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a4071-131">Data type</span></span>         | <span data-ttu-id="a4071-132">Unidade</span><span class="sxs-lookup"><span data-stu-id="a4071-132">Unit</span></span>                  | <span data-ttu-id="a4071-133">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="a4071-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a4071-134">Resumo</span><span class="sxs-lookup"><span data-stu-id="a4071-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a4071-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a4071-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a4071-136">string</span><span class="sxs-lookup"><span data-stu-id="a4071-136">string</span></span><br/> | <span data-ttu-id="a4071-137">characters</span><span class="sxs-lookup"><span data-stu-id="a4071-137">characters</span></span><br/> | <span data-ttu-id="a4071-138">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a4071-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a4071-139">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="a4071-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a4071-140">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="a4071-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a4071-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a4071-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a4071-142">string</span><span class="sxs-lookup"><span data-stu-id="a4071-142">string</span></span><br/> | <span data-ttu-id="a4071-143">N/D</span><span class="sxs-lookup"><span data-stu-id="a4071-143">n/a</span></span><br/>        | <span data-ttu-id="a4071-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="a4071-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a4071-145">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a4071-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a4071-146">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a4071-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a4071-147">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="a4071-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a4071-148">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="a4071-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a4071-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4071-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4071-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a4071-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




