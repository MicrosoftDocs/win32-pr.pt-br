---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105811963"
---
# <a name="parameterref"></a><span data-ttu-id="f86e9-104">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="f86e9-104">ParameterRef</span></span>

<span data-ttu-id="f86e9-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f86e9-105">This topic is not current.</span></span> <span data-ttu-id="f86e9-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f86e9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f86e9-107">Um elemento ParameterRef define uma referência a um elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="f86e9-107">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="f86e9-108">Um elemento ScoredProperty que contém um elemento ParameterRef não tem um elemento Value explicitamente definido.</span><span class="sxs-lookup"><span data-stu-id="f86e9-108">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="f86e9-109">Em vez disso, o elemento ScoredProperty recebe seu valor do elemento ParameterInit referenciado por um elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="f86e9-109">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="f86e9-110">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="f86e9-110">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="f86e9-111">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="f86e9-111">XML Attributes</span></span>

<span data-ttu-id="f86e9-112">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="f86e9-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="f86e9-113">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="f86e9-113">XML Attribute</span></span>   | <span data-ttu-id="f86e9-114">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f86e9-114">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f86e9-115">name</span><span class="sxs-lookup"><span data-stu-id="f86e9-115">name</span></span><br/> | <span data-ttu-id="f86e9-116">Mantém o atributo Name do elemento ParameterDef que é referenciado no contexto do documento atual.</span><span class="sxs-lookup"><span data-stu-id="f86e9-116">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="f86e9-117">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e9-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="f86e9-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f86e9-118">Element Information</span></span>

<span data-ttu-id="f86e9-119">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="f86e9-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="f86e9-120">Categoria</span><span class="sxs-lookup"><span data-stu-id="f86e9-120">Category</span></span>                   | <span data-ttu-id="f86e9-121">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f86e9-121">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f86e9-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f86e9-122">Parent elements</span></span><br/> | <span data-ttu-id="f86e9-123">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="f86e9-123">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="f86e9-124">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f86e9-124">Child elements</span></span><br/>  | <span data-ttu-id="f86e9-125">Nenhum permitido.</span><span class="sxs-lookup"><span data-stu-id="f86e9-125">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="f86e9-126">Este elemento</span><span class="sxs-lookup"><span data-stu-id="f86e9-126">This element</span></span><br/>    | <span data-ttu-id="f86e9-127">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="f86e9-127">No character data is permitted.</span></span><br/> <span data-ttu-id="f86e9-128">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="f86e9-128">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="f86e9-129">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="f86e9-129">Configuration Dependencies</span></span>

<span data-ttu-id="f86e9-130">Elementos ParameterRef podem não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="f86e9-130">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="f86e9-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f86e9-131">Example</span></span>

<span data-ttu-id="f86e9-132">O exemplo a seguir ilustra como usar elementos ParameterRef para permitir que os usuários insiram parâmetros de tamanho de mídia personalizados.</span><span class="sxs-lookup"><span data-stu-id="f86e9-132">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a><span data-ttu-id="f86e9-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f86e9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f86e9-134">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f86e9-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




