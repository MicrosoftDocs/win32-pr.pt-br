---
description: Saiba mais sobre o elemento ParameterInit, que define um valor para uma instância de um elemento ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e0cadbf26d6ff516ab0ace90165e11420a9b7
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118971"
---
# <a name="parameterinit"></a><span data-ttu-id="dfe35-103">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="dfe35-103">ParameterInit</span></span>

<span data-ttu-id="dfe35-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="dfe35-104">This topic is not current.</span></span> <span data-ttu-id="dfe35-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dfe35-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dfe35-106">Define um valor para uma instância de um elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="dfe35-106">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="dfe35-107">Um elemento ParameterInit é o destino da referência feita por um elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="dfe35-107">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="dfe35-108">Marca de elemento</span><span class="sxs-lookup"><span data-stu-id="dfe35-108">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="dfe35-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="dfe35-109">XML Attributes</span></span>

<span data-ttu-id="dfe35-110">A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="dfe35-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="dfe35-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="dfe35-111">XML Attribute</span></span>   | <span data-ttu-id="dfe35-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dfe35-112">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe35-113">name</span><span class="sxs-lookup"><span data-stu-id="dfe35-113">name</span></span><br/> | <span data-ttu-id="dfe35-114">Contém o atributo name do elemento ParameterDef que deve ser inicializado dentro do contexto do documento atual.</span><span class="sxs-lookup"><span data-stu-id="dfe35-114">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="dfe35-115">Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="dfe35-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="dfe35-116">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dfe35-116">Element Information</span></span>

<span data-ttu-id="dfe35-117">A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="dfe35-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="dfe35-118">Categoria</span><span class="sxs-lookup"><span data-stu-id="dfe35-118">Category</span></span>                   | <span data-ttu-id="dfe35-119">Nome ou restrição</span><span class="sxs-lookup"><span data-stu-id="dfe35-119">Name or restriction</span></span>                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe35-120">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="dfe35-120">Parent elements</span></span><br/> | <span data-ttu-id="dfe35-121">PrintTicket (raiz PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="dfe35-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="dfe35-122">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="dfe35-122">Child elements</span></span><br/>  | <span data-ttu-id="dfe35-123">Valor (um)</span><span class="sxs-lookup"><span data-stu-id="dfe35-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="dfe35-124">Esse elemento</span><span class="sxs-lookup"><span data-stu-id="dfe35-124">This element</span></span><br/>    | <span data-ttu-id="dfe35-125">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="dfe35-125">No character data is permitted.</span></span><br/> <span data-ttu-id="dfe35-126">Irmãos filhos duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="dfe35-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="dfe35-127">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="dfe35-127">Configuration Dependencies</span></span>

<span data-ttu-id="dfe35-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfe35-128">None</span></span>

## <a name="example"></a><span data-ttu-id="dfe35-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dfe35-129">Example</span></span>

<span data-ttu-id="dfe35-130">O exemplo a seguir inicializa um parâmetro como 1.</span><span class="sxs-lookup"><span data-stu-id="dfe35-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="dfe35-131">O exemplo em [ParameterDef](parameterdef.md) demonstra como definir todos os elementos property necessários para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dfe35-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="dfe35-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dfe35-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfe35-133">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="dfe35-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




