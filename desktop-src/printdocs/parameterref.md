---
description: Saiba mais sobre o elemento ParameterRef, que define uma referência a um elemento ParameterInit e como ele funciona com ScoredProperty.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407179"
---
# <a name="parameterref"></a><span data-ttu-id="2ed7f-103">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="2ed7f-103">ParameterRef</span></span>

<span data-ttu-id="2ed7f-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-104">This topic is not current.</span></span> <span data-ttu-id="2ed7f-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2ed7f-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2ed7f-106">Um elemento ParameterRef define uma referência a um elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-106">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="2ed7f-107">Um elemento ScoredProperty que contém um elemento ParameterRef não tem um elemento Value definido explicitamente.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-107">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="2ed7f-108">Em vez disso, o elemento ScoredProperty recebe seu valor do elemento ParameterInit referenciado por um elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-108">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="2ed7f-109">Marca de elemento</span><span class="sxs-lookup"><span data-stu-id="2ed7f-109">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="2ed7f-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="2ed7f-110">XML Attributes</span></span>

<span data-ttu-id="2ed7f-111">A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="2ed7f-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="2ed7f-112">XML Attribute</span></span>   | <span data-ttu-id="2ed7f-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2ed7f-113">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed7f-114">name</span><span class="sxs-lookup"><span data-stu-id="2ed7f-114">name</span></span><br/> | <span data-ttu-id="2ed7f-115">Contém o atributo name do elemento ParameterDef referenciado dentro do contexto do documento atual.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-115">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="2ed7f-116">Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="2ed7f-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="2ed7f-117">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2ed7f-117">Element Information</span></span>

<span data-ttu-id="2ed7f-118">A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="2ed7f-119">Categoria</span><span class="sxs-lookup"><span data-stu-id="2ed7f-119">Category</span></span>                   | <span data-ttu-id="2ed7f-120">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2ed7f-120">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed7f-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2ed7f-121">Parent elements</span></span><br/> | <span data-ttu-id="2ed7f-122">Scoredproperty</span><span class="sxs-lookup"><span data-stu-id="2ed7f-122">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="2ed7f-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2ed7f-123">Child elements</span></span><br/>  | <span data-ttu-id="2ed7f-124">Nenhum permitido.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-124">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="2ed7f-125">Esse elemento</span><span class="sxs-lookup"><span data-stu-id="2ed7f-125">This element</span></span><br/>    | <span data-ttu-id="2ed7f-126">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-126">No character data is permitted.</span></span><br/> <span data-ttu-id="2ed7f-127">Irmãos filhos duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-127">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="2ed7f-128">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="2ed7f-128">Configuration Dependencies</span></span>

<span data-ttu-id="2ed7f-129">Os elementos ParameterRef podem não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-129">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="2ed7f-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2ed7f-130">Example</span></span>

<span data-ttu-id="2ed7f-131">O exemplo a seguir ilustra como usar elementos ParameterRef para permitir que os usuários insiram parâmetros de tamanho de mídia personalizados.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-131">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2ed7f-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ed7f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed7f-133">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="2ed7f-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




