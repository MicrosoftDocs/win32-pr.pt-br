---
description: Saiba mais sobre o elemento PageColorManagement configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685794f1c9bb64c8bb3e966c4ec03bcac8821369
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549224"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="88b83-105">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="88b83-105">PageColorManagement</span></span>

<span data-ttu-id="88b83-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="88b83-106">This topic is not current.</span></span> <span data-ttu-id="88b83-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="88b83-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="88b83-108">Configura o gerenciamento de cores para a página atual.</span><span class="sxs-lookup"><span data-stu-id="88b83-108">Configures color management for the current page.</span></span> <span data-ttu-id="88b83-109">Isso é considerado automático em SHIM-DM \_ ICMMethod adicionar sistema.</span><span class="sxs-lookup"><span data-stu-id="88b83-109">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="88b83-110">Descreve qual componente deve executar o gerenciamento de cores (ou seja, Driver).</span><span class="sxs-lookup"><span data-stu-id="88b83-110">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="88b83-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="88b83-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="88b83-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="88b83-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="88b83-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="88b83-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="88b83-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="88b83-114">Element Information</span></span>



| <span data-ttu-id="88b83-115">Nome</span><span class="sxs-lookup"><span data-stu-id="88b83-115">Name</span></span> | <span data-ttu-id="88b83-116">Valor</span><span class="sxs-lookup"><span data-stu-id="88b83-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="88b83-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="88b83-117">Element Type</span></span> <br/>   | <span data-ttu-id="88b83-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="88b83-118">Feature</span></span><br/> |
| <span data-ttu-id="88b83-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="88b83-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="88b83-120">Página</span><span class="sxs-lookup"><span data-stu-id="88b83-120">Page</span></span><br/>    |
| <span data-ttu-id="88b83-121">Observações</span><span class="sxs-lookup"><span data-stu-id="88b83-121">Notes</span></span> <br/>          | <span data-ttu-id="88b83-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88b83-122">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="88b83-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="88b83-123">Structural Content</span></span>

<span data-ttu-id="88b83-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="88b83-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
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

## <a name="structure-variables"></a><span data-ttu-id="88b83-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="88b83-125">Structure Variables</span></span>

<span data-ttu-id="88b83-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="88b83-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="88b83-127">Nome</span><span class="sxs-lookup"><span data-stu-id="88b83-127">Name</span></span>                               | <span data-ttu-id="88b83-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="88b83-128">Data type</span></span>         | <span data-ttu-id="88b83-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="88b83-129">Unit</span></span>                  | <span data-ttu-id="88b83-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="88b83-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="88b83-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="88b83-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="88b83-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="88b83-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="88b83-133">string</span><span class="sxs-lookup"><span data-stu-id="88b83-133">string</span></span><br/> | <span data-ttu-id="88b83-134">characters</span><span class="sxs-lookup"><span data-stu-id="88b83-134">characters</span></span><br/> | <span data-ttu-id="88b83-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="88b83-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="88b83-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="88b83-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="88b83-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="88b83-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="88b83-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="88b83-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="88b83-139">string</span><span class="sxs-lookup"><span data-stu-id="88b83-139">string</span></span><br/> | <span data-ttu-id="88b83-140">n/d</span><span class="sxs-lookup"><span data-stu-id="88b83-140">n/a</span></span><br/>        | <span data-ttu-id="88b83-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="88b83-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="88b83-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="88b83-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="88b83-143">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="88b83-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="88b83-144">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="88b83-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="88b83-145">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="88b83-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Application has performed color management to the destination profile. -->
  <psf:Option name="psk:None" />
  <!--  Application has not performed color management and the device determines color management.-->
  <psf:Option name="psk:Device" />
  <!--  Application has not performed color management and the driver determines color management.-->
  <psf:Option name="psk:Driver" />
  <!--Color management is performed by the system. Not to be used when printing to XPSDrv print drivers -->
  <psf:Option name="psk:System" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="88b83-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88b83-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88b83-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="88b83-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




