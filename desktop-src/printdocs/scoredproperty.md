---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105794001"
---
# <a name="scoredproperty"></a><span data-ttu-id="5bbc1-104">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="5bbc1-104">ScoredProperty</span></span>

<span data-ttu-id="5bbc1-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-105">This topic is not current.</span></span> <span data-ttu-id="5bbc1-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5bbc1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5bbc1-107">Um elemento ScoredProperty declara uma propriedade que é intrínseca a uma definição de opção.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-107">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="5bbc1-108">Essas propriedades devem ser comparadas ao avaliar a precisão com que uma opção solicitada corresponde a uma opção com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-108">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="5bbc1-109">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="5bbc1-109">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="5bbc1-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="5bbc1-110">XML Attributes</span></span>

<span data-ttu-id="5bbc1-111">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="5bbc1-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="5bbc1-112">XML Attribute</span></span>   | <span data-ttu-id="5bbc1-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5bbc1-113">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbc1-114">name</span><span class="sxs-lookup"><span data-stu-id="5bbc1-114">name</span></span><br/> | <span data-ttu-id="5bbc1-115">Mantém o atributo Name de ScoredProperty, uma propriedade padrão ou uma propriedade definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-115">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="5bbc1-116">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5bbc1-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="5bbc1-117">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5bbc1-117">Element Information</span></span>

<span data-ttu-id="5bbc1-118">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="5bbc1-119">Categoria</span><span class="sxs-lookup"><span data-stu-id="5bbc1-119">Category</span></span>                   | <span data-ttu-id="5bbc1-120">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5bbc1-120">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbc1-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5bbc1-121">Parent elements</span></span><br/> | <span data-ttu-id="5bbc1-122">*Opção*</span><span class="sxs-lookup"><span data-stu-id="5bbc1-122">*Option*</span></span><br/> <span data-ttu-id="5bbc1-123">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="5bbc1-123">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="5bbc1-124">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5bbc1-124">Child elements</span></span><br/>  | <span data-ttu-id="5bbc1-125">Você pode usar o</span><span class="sxs-lookup"><span data-stu-id="5bbc1-125">Either</span></span><br/> <span data-ttu-id="5bbc1-126">*ParameterRef* (um)</span><span class="sxs-lookup"><span data-stu-id="5bbc1-126">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="5bbc1-127">ou</span><span class="sxs-lookup"><span data-stu-id="5bbc1-127">or</span></span><br/> <span data-ttu-id="5bbc1-128">*Valor* (um)</span><span class="sxs-lookup"><span data-stu-id="5bbc1-128">*Value* (one)</span></span><br/> <span data-ttu-id="5bbc1-129">*Propriedade* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5bbc1-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="5bbc1-130">*ScoredProperty* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5bbc1-130">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="5bbc1-131">Este elemento</span><span class="sxs-lookup"><span data-stu-id="5bbc1-131">This element</span></span><br/>    | <span data-ttu-id="5bbc1-132">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-132">No character data is permitted.</span></span><br/> <span data-ttu-id="5bbc1-133">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-133">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="5bbc1-134">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="5bbc1-134">Configuration Dependencies</span></span>

<span data-ttu-id="5bbc1-135">Um elemento ScoredProperty pode não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-135">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="5bbc1-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5bbc1-136">Example</span></span>

<span data-ttu-id="5bbc1-137">Declare um elemento ScoredProperty chamado MediaSizeWidth com um valor de 11.</span><span class="sxs-lookup"><span data-stu-id="5bbc1-137">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="5bbc1-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bbc1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bbc1-139">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5bbc1-139">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




