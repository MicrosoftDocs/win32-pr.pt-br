---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92845b635aa7db1f44394cb6ef76b32292ea0dd4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996133"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="b245b-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="b245b-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="b245b-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b245b-105">This topic is not current.</span></span> <span data-ttu-id="b245b-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b245b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b245b-107">Define as características do perfil de cor de destino.</span><span class="sxs-lookup"><span data-stu-id="b245b-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="b245b-108">Descreve se o aplicativo ou driver seleciona o perfil de cor de destino a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b245b-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="b245b-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b245b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b245b-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b245b-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b245b-111">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b245b-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b245b-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b245b-112">Element Information</span></span>



| <span data-ttu-id="b245b-113">Nome</span><span class="sxs-lookup"><span data-stu-id="b245b-113">Name</span></span> | <span data-ttu-id="b245b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b245b-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b245b-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b245b-115">Element Type</span></span> <br/>   | <span data-ttu-id="b245b-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="b245b-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b245b-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="b245b-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b245b-118">?</span><span class="sxs-lookup"><span data-stu-id="b245b-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b245b-119">Observações</span><span class="sxs-lookup"><span data-stu-id="b245b-119">Notes</span></span> <br/>          | <span data-ttu-id="b245b-120">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="b245b-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="b245b-121">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="b245b-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="b245b-122">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="b245b-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="b245b-123">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="b245b-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="b245b-124">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b245b-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b245b-125">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b245b-125">Structural Content</span></span>

<span data-ttu-id="b245b-126">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="b245b-126">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="b245b-127">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="b245b-127">Structure Variables</span></span>

<span data-ttu-id="b245b-128">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="b245b-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b245b-129">Nome</span><span class="sxs-lookup"><span data-stu-id="b245b-129">Name</span></span>                               | <span data-ttu-id="b245b-130">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b245b-130">Data type</span></span>         | <span data-ttu-id="b245b-131">Unidade</span><span class="sxs-lookup"><span data-stu-id="b245b-131">Unit</span></span>                  | <span data-ttu-id="b245b-132">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="b245b-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b245b-133">Resumo</span><span class="sxs-lookup"><span data-stu-id="b245b-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b245b-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b245b-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b245b-135">string</span><span class="sxs-lookup"><span data-stu-id="b245b-135">string</span></span><br/> | <span data-ttu-id="b245b-136">characters</span><span class="sxs-lookup"><span data-stu-id="b245b-136">characters</span></span><br/> | <span data-ttu-id="b245b-137">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b245b-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b245b-138">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="b245b-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b245b-139">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="b245b-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b245b-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b245b-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b245b-141">string</span><span class="sxs-lookup"><span data-stu-id="b245b-141">string</span></span><br/> | <span data-ttu-id="b245b-142">N/D</span><span class="sxs-lookup"><span data-stu-id="b245b-142">n/a</span></span><br/>        | <span data-ttu-id="b245b-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="b245b-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b245b-144">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b245b-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b245b-145">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b245b-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b245b-146">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="b245b-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b245b-147">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="b245b-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="b245b-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b245b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b245b-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b245b-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




