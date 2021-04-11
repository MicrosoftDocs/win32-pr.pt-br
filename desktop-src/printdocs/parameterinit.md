---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cb985e746b400b1c804f21b5996352ae590e3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172549"
---
# <a name="parameterinit"></a><span data-ttu-id="411b1-104">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="411b1-104">ParameterInit</span></span>

<span data-ttu-id="411b1-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="411b1-105">This topic is not current.</span></span> <span data-ttu-id="411b1-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="411b1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="411b1-107">Define um valor para uma instância de um elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="411b1-107">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="411b1-108">Um elemento ParameterInit é o destino da referência feita por um elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="411b1-108">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="411b1-109">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="411b1-109">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="411b1-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="411b1-110">XML Attributes</span></span>

<span data-ttu-id="411b1-111">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="411b1-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="411b1-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="411b1-112">XML Attribute</span></span>   | <span data-ttu-id="411b1-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="411b1-113">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="411b1-114">name</span><span class="sxs-lookup"><span data-stu-id="411b1-114">name</span></span><br/> | <span data-ttu-id="411b1-115">Mantém o atributo Name do elemento ParameterDef que deve ser inicializado dentro do contexto do documento atual.</span><span class="sxs-lookup"><span data-stu-id="411b1-115">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="411b1-116">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="411b1-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="411b1-117">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="411b1-117">Element Information</span></span>

<span data-ttu-id="411b1-118">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="411b1-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="411b1-119">Category</span><span class="sxs-lookup"><span data-stu-id="411b1-119">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="411b1-120">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="411b1-120">Parent elements</span></span><br/> | <span data-ttu-id="411b1-121">PrintTicket (raiz do PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="411b1-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="411b1-122">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="411b1-122">Child elements</span></span><br/>  | <span data-ttu-id="411b1-123">Valor (um)</span><span class="sxs-lookup"><span data-stu-id="411b1-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="411b1-124">Este elemento</span><span class="sxs-lookup"><span data-stu-id="411b1-124">This element</span></span><br/>    | <span data-ttu-id="411b1-125">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="411b1-125">No character data is permitted.</span></span><br/> <span data-ttu-id="411b1-126">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="411b1-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="411b1-127">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="411b1-127">Configuration Dependencies</span></span>

<span data-ttu-id="411b1-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="411b1-128">None</span></span>

## <a name="example"></a><span data-ttu-id="411b1-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="411b1-129">Example</span></span>

<span data-ttu-id="411b1-130">O exemplo a seguir inicializa um parâmetro para 1.</span><span class="sxs-lookup"><span data-stu-id="411b1-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="411b1-131">O exemplo em [ParameterDef](parameterdef.md) demonstra como definir todos os elementos de propriedade necessários para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="411b1-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="411b1-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="411b1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="411b1-133">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="411b1-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




