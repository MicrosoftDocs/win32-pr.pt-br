---
description: Encontre informações sobre o elemento ScoredProperty. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb93fbdaeb6101cbd1ff75d6c0b3a829afe0d317
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119111"
---
# <a name="scoredproperty"></a><span data-ttu-id="e7d40-105">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="e7d40-105">ScoredProperty</span></span>

<span data-ttu-id="e7d40-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="e7d40-106">This topic is not current.</span></span> <span data-ttu-id="e7d40-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e7d40-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e7d40-108">Um elemento ScoredProperty declara uma propriedade que é intrínseca a uma definição de opção.</span><span class="sxs-lookup"><span data-stu-id="e7d40-108">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="e7d40-109">Essas propriedades devem ser comparadas ao avaliar a precisão com que uma opção solicitada corresponde a uma opção com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7d40-109">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="e7d40-110">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="e7d40-110">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="e7d40-111">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="e7d40-111">XML Attributes</span></span>

<span data-ttu-id="e7d40-112">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="e7d40-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="e7d40-113">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="e7d40-113">XML Attribute</span></span>   | <span data-ttu-id="e7d40-114">Detalhes</span><span class="sxs-lookup"><span data-stu-id="e7d40-114">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d40-115">name</span><span class="sxs-lookup"><span data-stu-id="e7d40-115">name</span></span><br/> | <span data-ttu-id="e7d40-116">Mantém o atributo Name de ScoredProperty, uma propriedade padrão ou uma propriedade definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="e7d40-116">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="e7d40-117">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d40-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="e7d40-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e7d40-118">Element Information</span></span>

<span data-ttu-id="e7d40-119">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="e7d40-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="e7d40-120">Categoria</span><span class="sxs-lookup"><span data-stu-id="e7d40-120">Category</span></span>                   | <span data-ttu-id="e7d40-121">Detalhes</span><span class="sxs-lookup"><span data-stu-id="e7d40-121">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d40-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e7d40-122">Parent elements</span></span><br/> | <span data-ttu-id="e7d40-123">*Opção*</span><span class="sxs-lookup"><span data-stu-id="e7d40-123">*Option*</span></span><br/> <span data-ttu-id="e7d40-124">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="e7d40-124">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="e7d40-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e7d40-125">Child elements</span></span><br/>  | <span data-ttu-id="e7d40-126">Você pode usar o</span><span class="sxs-lookup"><span data-stu-id="e7d40-126">Either</span></span><br/> <span data-ttu-id="e7d40-127">*ParameterRef* (um)</span><span class="sxs-lookup"><span data-stu-id="e7d40-127">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="e7d40-128">ou</span><span class="sxs-lookup"><span data-stu-id="e7d40-128">or</span></span><br/> <span data-ttu-id="e7d40-129">*Valor* (um)</span><span class="sxs-lookup"><span data-stu-id="e7d40-129">*Value* (one)</span></span><br/> <span data-ttu-id="e7d40-130">*Propriedade* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="e7d40-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="e7d40-131">*ScoredProperty* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="e7d40-131">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="e7d40-132">Este elemento</span><span class="sxs-lookup"><span data-stu-id="e7d40-132">This element</span></span><br/>    | <span data-ttu-id="e7d40-133">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="e7d40-133">No character data is permitted.</span></span><br/> <span data-ttu-id="e7d40-134">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="e7d40-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="e7d40-135">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="e7d40-135">Configuration Dependencies</span></span>

<span data-ttu-id="e7d40-136">Um elemento ScoredProperty pode não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="e7d40-136">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="e7d40-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e7d40-137">Example</span></span>

<span data-ttu-id="e7d40-138">Declare um elemento ScoredProperty chamado MediaSizeWidth com um valor de 11.</span><span class="sxs-lookup"><span data-stu-id="e7d40-138">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="e7d40-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7d40-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7d40-140">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="e7d40-140">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




