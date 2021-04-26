---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81a037b6b32ff71b53688dfd6fc8afd5f10bb69
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997653"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="f7a9a-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="f7a9a-104">PageColorManagement</span></span>

<span data-ttu-id="f7a9a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-105">This topic is not current.</span></span> <span data-ttu-id="f7a9a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f7a9a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f7a9a-107">Configura o gerenciamento de cores para a página atual.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-107">Configures color management for the current page.</span></span> <span data-ttu-id="f7a9a-108">Isso é considerado automático em SHIM-DM \_ ICMMethod adicionar sistema.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="f7a9a-109">Descreve qual componente deve executar o gerenciamento de cores (ou seja, Driver).</span><span class="sxs-lookup"><span data-stu-id="f7a9a-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="f7a9a-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f7a9a-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f7a9a-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f7a9a-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f7a9a-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f7a9a-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f7a9a-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f7a9a-113">Element Information</span></span>



| <span data-ttu-id="f7a9a-114">Nome</span><span class="sxs-lookup"><span data-stu-id="f7a9a-114">Name</span></span> | <span data-ttu-id="f7a9a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f7a9a-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f7a9a-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f7a9a-116">Element Type</span></span> <br/>   | <span data-ttu-id="f7a9a-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="f7a9a-117">Feature</span></span><br/> |
| <span data-ttu-id="f7a9a-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="f7a9a-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f7a9a-119">?</span><span class="sxs-lookup"><span data-stu-id="f7a9a-119">Page</span></span><br/>    |
| <span data-ttu-id="f7a9a-120">Observações</span><span class="sxs-lookup"><span data-stu-id="f7a9a-120">Notes</span></span> <br/>          | <span data-ttu-id="f7a9a-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f7a9a-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="f7a9a-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f7a9a-122">Structural Content</span></span>

<span data-ttu-id="f7a9a-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f7a9a-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="f7a9a-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="f7a9a-124">Structure Variables</span></span>

<span data-ttu-id="f7a9a-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f7a9a-126">Nome</span><span class="sxs-lookup"><span data-stu-id="f7a9a-126">Name</span></span>                               | <span data-ttu-id="f7a9a-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f7a9a-127">Data type</span></span>         | <span data-ttu-id="f7a9a-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="f7a9a-128">Unit</span></span>                  | <span data-ttu-id="f7a9a-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="f7a9a-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f7a9a-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="f7a9a-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f7a9a-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f7a9a-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f7a9a-132">string</span><span class="sxs-lookup"><span data-stu-id="f7a9a-132">string</span></span><br/> | <span data-ttu-id="f7a9a-133">characters</span><span class="sxs-lookup"><span data-stu-id="f7a9a-133">characters</span></span><br/> | <span data-ttu-id="f7a9a-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="f7a9a-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f7a9a-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f7a9a-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f7a9a-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f7a9a-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f7a9a-138">string</span><span class="sxs-lookup"><span data-stu-id="f7a9a-138">string</span></span><br/> | <span data-ttu-id="f7a9a-139">N/D</span><span class="sxs-lookup"><span data-stu-id="f7a9a-139">n/a</span></span><br/>        | <span data-ttu-id="f7a9a-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f7a9a-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f7a9a-142">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f7a9a-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f7a9a-143">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="f7a9a-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f7a9a-144">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="f7a9a-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f7a9a-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7a9a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7a9a-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f7a9a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




