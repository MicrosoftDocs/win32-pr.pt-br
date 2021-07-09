---
description: Examine o elemento PageDestinationColorProfile configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c12e8b6e322f024c3603abc97b0e4e0413d5b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549214"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="03804-105">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="03804-105">PageDestinationColorProfile</span></span>

<span data-ttu-id="03804-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="03804-106">This topic is not current.</span></span> <span data-ttu-id="03804-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="03804-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="03804-108">Define as características do perfil de cor de destino.</span><span class="sxs-lookup"><span data-stu-id="03804-108">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="03804-109">Descreve se o aplicativo ou driver seleciona o perfil de cor de destino a ser usado.</span><span class="sxs-lookup"><span data-stu-id="03804-109">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="03804-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="03804-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="03804-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="03804-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="03804-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="03804-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="03804-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="03804-113">Element Information</span></span>



| <span data-ttu-id="03804-114">Nome</span><span class="sxs-lookup"><span data-stu-id="03804-114">Name</span></span> | <span data-ttu-id="03804-115">Valor</span><span class="sxs-lookup"><span data-stu-id="03804-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03804-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="03804-116">Element Type</span></span> <br/>   | <span data-ttu-id="03804-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="03804-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="03804-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="03804-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="03804-119">Página</span><span class="sxs-lookup"><span data-stu-id="03804-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="03804-120">Observações</span><span class="sxs-lookup"><span data-stu-id="03804-120">Notes</span></span> <br/>          | <span data-ttu-id="03804-121">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="03804-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="03804-122">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="03804-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="03804-123">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="03804-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="03804-124">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="03804-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="03804-125">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="03804-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="03804-126">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="03804-126">Structural Content</span></span>

<span data-ttu-id="03804-127">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="03804-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="03804-128">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="03804-128">Structure Variables</span></span>

<span data-ttu-id="03804-129">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="03804-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="03804-130">Nome</span><span class="sxs-lookup"><span data-stu-id="03804-130">Name</span></span>                               | <span data-ttu-id="03804-131">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="03804-131">Data type</span></span>         | <span data-ttu-id="03804-132">Unidade</span><span class="sxs-lookup"><span data-stu-id="03804-132">Unit</span></span>                  | <span data-ttu-id="03804-133">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="03804-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="03804-134">Resumo</span><span class="sxs-lookup"><span data-stu-id="03804-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="03804-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="03804-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="03804-136">string</span><span class="sxs-lookup"><span data-stu-id="03804-136">string</span></span><br/> | <span data-ttu-id="03804-137">characters</span><span class="sxs-lookup"><span data-stu-id="03804-137">characters</span></span><br/> | <span data-ttu-id="03804-138">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="03804-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="03804-139">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="03804-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="03804-140">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="03804-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="03804-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="03804-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="03804-142">string</span><span class="sxs-lookup"><span data-stu-id="03804-142">string</span></span><br/> | <span data-ttu-id="03804-143">n/d</span><span class="sxs-lookup"><span data-stu-id="03804-143">n/a</span></span><br/>        | <span data-ttu-id="03804-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="03804-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="03804-145">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="03804-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="03804-146">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="03804-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="03804-147">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="03804-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="03804-148">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="03804-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="03804-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03804-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03804-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="03804-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




