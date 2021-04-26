---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 29d0bf2d-4897-43ed-ba3d-0b38b2f30375
title: DocumentCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5822921fe3dc1852100569b29a1ded8b37bc9aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994533"
---
# <a name="documentcoverback"></a><span data-ttu-id="9fe6a-104">DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="9fe6a-104">DocumentCoverBack</span></span>

<span data-ttu-id="9fe6a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-105">This topic is not current.</span></span> <span data-ttu-id="9fe6a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9fe6a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9fe6a-107">Descreve a folha de rosto voltar (terminando).</span><span class="sxs-lookup"><span data-stu-id="9fe6a-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="9fe6a-108">Cada documento terá uma planilha separada.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="9fe6a-109">A folha de rosto deve ser impressa no PageMediaSize e no PageMediaType usados para a página final do documento.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the document.</span></span> <span data-ttu-id="9fe6a-110">A folha de rosto deve ser integrada às opções de processamento (como DocumentDuplex, DocumentNUp), conforme indicado pela opção especificada.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="9fe6a-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9fe6a-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9fe6a-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="9fe6a-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9fe6a-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9fe6a-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9fe6a-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9fe6a-114">Element Information</span></span>



| <span data-ttu-id="9fe6a-115">Nome</span><span class="sxs-lookup"><span data-stu-id="9fe6a-115">Name</span></span> | <span data-ttu-id="9fe6a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9fe6a-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe6a-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9fe6a-117">Element Type</span></span> <br/>   | <span data-ttu-id="9fe6a-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="9fe6a-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9fe6a-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="9fe6a-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9fe6a-120">Documento</span><span class="sxs-lookup"><span data-stu-id="9fe6a-120">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9fe6a-121">Observações</span><span class="sxs-lookup"><span data-stu-id="9fe6a-121">Notes</span></span> <br/>          | <span data-ttu-id="9fe6a-122">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="9fe6a-123">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="9fe6a-124">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="9fe6a-125">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="9fe6a-126">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9fe6a-127">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="9fe6a-127">Structural Content</span></span>

<span data-ttu-id="9fe6a-128">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="9fe6a-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!--Specifies the XPS specific part name for the back cover sheet-->
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="9fe6a-129">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="9fe6a-129">Structure Variables</span></span>

<span data-ttu-id="9fe6a-130">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9fe6a-131">Nome</span><span class="sxs-lookup"><span data-stu-id="9fe6a-131">Name</span></span>                               | <span data-ttu-id="9fe6a-132">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9fe6a-132">Data type</span></span>         | <span data-ttu-id="9fe6a-133">Unidade</span><span class="sxs-lookup"><span data-stu-id="9fe6a-133">Unit</span></span>                  | <span data-ttu-id="9fe6a-134">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="9fe6a-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9fe6a-135">Resumo</span><span class="sxs-lookup"><span data-stu-id="9fe6a-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9fe6a-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9fe6a-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9fe6a-137">string</span><span class="sxs-lookup"><span data-stu-id="9fe6a-137">string</span></span><br/> | <span data-ttu-id="9fe6a-138">characters</span><span class="sxs-lookup"><span data-stu-id="9fe6a-138">characters</span></span><br/> | <span data-ttu-id="9fe6a-139">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9fe6a-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9fe6a-140">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9fe6a-141">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9fe6a-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9fe6a-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9fe6a-143">string</span><span class="sxs-lookup"><span data-stu-id="9fe6a-143">string</span></span><br/> | <span data-ttu-id="9fe6a-144">N/D</span><span class="sxs-lookup"><span data-stu-id="9fe6a-144">n/a</span></span><br/>        | <span data-ttu-id="9fe6a-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9fe6a-146">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9fe6a-147">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9fe6a-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9fe6a-148">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="9fe6a-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9fe6a-149">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="9fe6a-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="9fe6a-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fe6a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fe6a-151">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="9fe6a-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




