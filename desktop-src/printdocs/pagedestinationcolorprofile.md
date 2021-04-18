---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde6077bc2bae611c2a791ecf041cb52588c2ebb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105761533"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="066a3-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="066a3-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="066a3-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="066a3-105">This topic is not current.</span></span> <span data-ttu-id="066a3-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="066a3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="066a3-107">Define as características do perfil de cor de destino.</span><span class="sxs-lookup"><span data-stu-id="066a3-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="066a3-108">Descreve se o aplicativo ou driver seleciona o perfil de cor de destino a ser usado.</span><span class="sxs-lookup"><span data-stu-id="066a3-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="066a3-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="066a3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="066a3-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="066a3-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="066a3-111">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="066a3-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="066a3-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="066a3-112">Element Information</span></span>



| <span data-ttu-id="066a3-113">Nome</span><span class="sxs-lookup"><span data-stu-id="066a3-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="066a3-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="066a3-114">Element Type</span></span> <br/>   | <span data-ttu-id="066a3-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="066a3-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="066a3-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="066a3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="066a3-117">?</span><span class="sxs-lookup"><span data-stu-id="066a3-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="066a3-118">Observações</span><span class="sxs-lookup"><span data-stu-id="066a3-118">Notes</span></span> <br/>          | <span data-ttu-id="066a3-119">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="066a3-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="066a3-120">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="066a3-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="066a3-121">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="066a3-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="066a3-122">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="066a3-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="066a3-123">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="066a3-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="066a3-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="066a3-124">Structural Content</span></span>

<span data-ttu-id="066a3-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="066a3-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="066a3-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="066a3-126">Structure Variables</span></span>

<span data-ttu-id="066a3-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="066a3-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="066a3-128">Nome</span><span class="sxs-lookup"><span data-stu-id="066a3-128">Name</span></span>                               | <span data-ttu-id="066a3-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="066a3-129">Data type</span></span>         | <span data-ttu-id="066a3-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="066a3-130">Unit</span></span>                  | <span data-ttu-id="066a3-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="066a3-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="066a3-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="066a3-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="066a3-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="066a3-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="066a3-134">string</span><span class="sxs-lookup"><span data-stu-id="066a3-134">string</span></span><br/> | <span data-ttu-id="066a3-135">characters</span><span class="sxs-lookup"><span data-stu-id="066a3-135">characters</span></span><br/> | <span data-ttu-id="066a3-136">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="066a3-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="066a3-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="066a3-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="066a3-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="066a3-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="066a3-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="066a3-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="066a3-140">string</span><span class="sxs-lookup"><span data-stu-id="066a3-140">string</span></span><br/> | <span data-ttu-id="066a3-141">N/D</span><span class="sxs-lookup"><span data-stu-id="066a3-141">n/a</span></span><br/>        | <span data-ttu-id="066a3-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="066a3-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="066a3-143">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="066a3-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="066a3-144">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="066a3-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="066a3-145">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="066a3-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="066a3-146">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="066a3-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="066a3-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="066a3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="066a3-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="066a3-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




