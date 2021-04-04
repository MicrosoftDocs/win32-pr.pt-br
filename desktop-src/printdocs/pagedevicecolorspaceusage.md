---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77f143457ea24d5c23aba443209ba35ce02454
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "103837710"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="6cabc-104">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="6cabc-104">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="6cabc-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="6cabc-105">This topic is not current.</span></span> <span data-ttu-id="6cabc-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6cabc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6cabc-107">Em conjunto com o parâmetro PageDeviceColorSpaceProfileURI, esse parâmetro define o comportamento de renderização dos elementos apresentados em um espaço de cores do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6cabc-107">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="6cabc-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="6cabc-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6cabc-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="6cabc-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6cabc-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="6cabc-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6cabc-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="6cabc-111">Element Information</span></span>



| <span data-ttu-id="6cabc-112">Nome</span><span class="sxs-lookup"><span data-stu-id="6cabc-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cabc-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6cabc-113">Element Type</span></span> <br/>   | <span data-ttu-id="6cabc-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="6cabc-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6cabc-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="6cabc-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6cabc-116">?</span><span class="sxs-lookup"><span data-stu-id="6cabc-116">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6cabc-117">Observações</span><span class="sxs-lookup"><span data-stu-id="6cabc-117">Notes</span></span> <br/>          | <span data-ttu-id="6cabc-118">Isso se aplica somente a documentos XPS e não deve ser usado em PrintTickets arbitrários.</span><span class="sxs-lookup"><span data-stu-id="6cabc-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="6cabc-119">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="6cabc-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="6cabc-120">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="6cabc-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="6cabc-121">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="6cabc-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="6cabc-122">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="6cabc-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="6cabc-123">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6cabc-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6cabc-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="6cabc-124">Structural Content</span></span>

<span data-ttu-id="6cabc-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="6cabc-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
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

## <a name="structure-variables"></a><span data-ttu-id="6cabc-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="6cabc-126">Structure Variables</span></span>

<span data-ttu-id="6cabc-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="6cabc-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6cabc-128">Nome</span><span class="sxs-lookup"><span data-stu-id="6cabc-128">Name</span></span>                               | <span data-ttu-id="6cabc-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6cabc-129">Data type</span></span>         | <span data-ttu-id="6cabc-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="6cabc-130">Unit</span></span>                  | <span data-ttu-id="6cabc-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="6cabc-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6cabc-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="6cabc-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6cabc-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6cabc-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6cabc-134">string</span><span class="sxs-lookup"><span data-stu-id="6cabc-134">string</span></span><br/> | <span data-ttu-id="6cabc-135">characters</span><span class="sxs-lookup"><span data-stu-id="6cabc-135">characters</span></span><br/> | <span data-ttu-id="6cabc-136">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6cabc-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6cabc-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="6cabc-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6cabc-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="6cabc-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6cabc-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6cabc-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6cabc-140">string</span><span class="sxs-lookup"><span data-stu-id="6cabc-140">string</span></span><br/> | <span data-ttu-id="6cabc-141">N/D</span><span class="sxs-lookup"><span data-stu-id="6cabc-141">n/a</span></span><br/>        | <span data-ttu-id="6cabc-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="6cabc-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6cabc-143">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="6cabc-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6cabc-144">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="6cabc-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6cabc-145">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="6cabc-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6cabc-146">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="6cabc-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- If the device determines that the profile specified by the PageDeviceColorSpaceProfileURI parameter can be used as a device color space profile, all elements using the same profile are treated as already being specified in device color space. All other elements MUST use the profile specified for that element.
If the profile cannot be used as a device color space profile, elements using the profile MUST be color managed like any other element using the color profile. -->
  <psf:Option name="psk:MatchToDefault" />
  <!-- If the profile specified by the PageDeviceColorSpaceProfileURI parameter has a number of channels matching the number of primaries of the device, it SHOULD be used instead of the devices internal color management for all elements. Elements using this profile are assumed to be in device color space and will not be color managed further. -->
  <psf:Option name="psk:OverrideDeviceDefault" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6cabc-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cabc-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cabc-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="6cabc-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




