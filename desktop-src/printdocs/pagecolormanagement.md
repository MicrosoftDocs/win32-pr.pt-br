---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ae8d161035d23149759345e8eb139dd3fb7a48
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105771265"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="ec536-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="ec536-104">PageColorManagement</span></span>

<span data-ttu-id="ec536-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ec536-105">This topic is not current.</span></span> <span data-ttu-id="ec536-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ec536-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ec536-107">Configura o gerenciamento de cores para a página atual.</span><span class="sxs-lookup"><span data-stu-id="ec536-107">Configures color management for the current page.</span></span> <span data-ttu-id="ec536-108">Isso é considerado automático em SHIM-DM \_ ICMMethod adicionar sistema.</span><span class="sxs-lookup"><span data-stu-id="ec536-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="ec536-109">Descreve qual componente deve executar o gerenciamento de cores (ou seja, Driver).</span><span class="sxs-lookup"><span data-stu-id="ec536-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="ec536-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ec536-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ec536-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ec536-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ec536-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ec536-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ec536-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ec536-113">Element Information</span></span>



| <span data-ttu-id="ec536-114">Nome</span><span class="sxs-lookup"><span data-stu-id="ec536-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="ec536-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ec536-115">Element Type</span></span> <br/>   | <span data-ttu-id="ec536-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="ec536-116">Feature</span></span><br/> |
| <span data-ttu-id="ec536-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="ec536-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ec536-118">?</span><span class="sxs-lookup"><span data-stu-id="ec536-118">Page</span></span><br/>    |
| <span data-ttu-id="ec536-119">Observações</span><span class="sxs-lookup"><span data-stu-id="ec536-119">Notes</span></span> <br/>          | <span data-ttu-id="ec536-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ec536-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="ec536-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ec536-121">Structural Content</span></span>

<span data-ttu-id="ec536-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="ec536-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ec536-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="ec536-123">Structure Variables</span></span>

<span data-ttu-id="ec536-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="ec536-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ec536-125">Nome</span><span class="sxs-lookup"><span data-stu-id="ec536-125">Name</span></span>                               | <span data-ttu-id="ec536-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ec536-126">Data type</span></span>         | <span data-ttu-id="ec536-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="ec536-127">Unit</span></span>                  | <span data-ttu-id="ec536-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="ec536-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ec536-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="ec536-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ec536-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ec536-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ec536-131">string</span><span class="sxs-lookup"><span data-stu-id="ec536-131">string</span></span><br/> | <span data-ttu-id="ec536-132">characters</span><span class="sxs-lookup"><span data-stu-id="ec536-132">characters</span></span><br/> | <span data-ttu-id="ec536-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ec536-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ec536-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="ec536-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ec536-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="ec536-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ec536-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ec536-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ec536-137">string</span><span class="sxs-lookup"><span data-stu-id="ec536-137">string</span></span><br/> | <span data-ttu-id="ec536-138">N/D</span><span class="sxs-lookup"><span data-stu-id="ec536-138">n/a</span></span><br/>        | <span data-ttu-id="ec536-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="ec536-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ec536-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="ec536-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ec536-141">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ec536-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ec536-142">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="ec536-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ec536-143">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="ec536-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ec536-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec536-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec536-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ec536-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




