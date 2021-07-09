---
description: Revise o elemento PageDeviceFontSubstitution configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: PageDeviceFontSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc5650c687a4c96e6c54ef7ea0631e77407e874
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549194"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="341a0-105">PageDeviceFontSubstitution</span><span class="sxs-lookup"><span data-stu-id="341a0-105">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="341a0-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="341a0-106">This topic is not current.</span></span> <span data-ttu-id="341a0-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="341a0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="341a0-108">Descreve o estado habilitado/desabilitado da substituição de fonte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="341a0-108">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="341a0-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="341a0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="341a0-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="341a0-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="341a0-111">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="341a0-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="341a0-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="341a0-112">Element Information</span></span>



| <span data-ttu-id="341a0-113">Nome</span><span class="sxs-lookup"><span data-stu-id="341a0-113">Name</span></span> | <span data-ttu-id="341a0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="341a0-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="341a0-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="341a0-115">Element Type</span></span> <br/>   | <span data-ttu-id="341a0-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="341a0-116">Feature</span></span><br/> |
| <span data-ttu-id="341a0-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="341a0-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="341a0-118">Página</span><span class="sxs-lookup"><span data-stu-id="341a0-118">Page</span></span><br/>    |
| <span data-ttu-id="341a0-119">Observações</span><span class="sxs-lookup"><span data-stu-id="341a0-119">Notes</span></span> <br/>          | <span data-ttu-id="341a0-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="341a0-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="341a0-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="341a0-121">Structural Content</span></span>

<span data-ttu-id="341a0-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="341a0-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
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

## <a name="structure-variables"></a><span data-ttu-id="341a0-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="341a0-123">Structure Variables</span></span>

<span data-ttu-id="341a0-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="341a0-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="341a0-125">Nome</span><span class="sxs-lookup"><span data-stu-id="341a0-125">Name</span></span>                               | <span data-ttu-id="341a0-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="341a0-126">Data type</span></span>         | <span data-ttu-id="341a0-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="341a0-127">Unit</span></span>                  | <span data-ttu-id="341a0-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="341a0-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="341a0-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="341a0-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="341a0-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="341a0-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="341a0-131">string</span><span class="sxs-lookup"><span data-stu-id="341a0-131">string</span></span><br/> | <span data-ttu-id="341a0-132">characters</span><span class="sxs-lookup"><span data-stu-id="341a0-132">characters</span></span><br/> | <span data-ttu-id="341a0-133">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="341a0-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="341a0-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="341a0-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="341a0-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="341a0-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="341a0-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="341a0-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="341a0-137">string</span><span class="sxs-lookup"><span data-stu-id="341a0-137">string</span></span><br/> | <span data-ttu-id="341a0-138">n/d</span><span class="sxs-lookup"><span data-stu-id="341a0-138">n/a</span></span><br/>        | <span data-ttu-id="341a0-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="341a0-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="341a0-140">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="341a0-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="341a0-141">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="341a0-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="341a0-142">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="341a0-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="341a0-143">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="341a0-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Page device font substitution is off -->
  <psf:Option name="psk:Off" />
  <!--Page device font substitution is on -->
  <psf:Option name="psk:On" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="341a0-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="341a0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="341a0-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="341a0-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




