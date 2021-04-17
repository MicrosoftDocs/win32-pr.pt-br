---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105780414"
---
# <a name="option"></a><span data-ttu-id="5486a-104">Opção</span><span class="sxs-lookup"><span data-stu-id="5486a-104">Option</span></span>

<span data-ttu-id="5486a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5486a-105">This topic is not current.</span></span> <span data-ttu-id="5486a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5486a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5486a-107">Um elemento Option contém todos os elementos Property e ScoredProperty associados a essa opção.</span><span class="sxs-lookup"><span data-stu-id="5486a-107">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="5486a-108">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="5486a-108">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="5486a-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="5486a-109">XML Attributes</span></span>

<span data-ttu-id="5486a-110">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="5486a-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="5486a-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="5486a-111">XML Attribute</span></span>          | <span data-ttu-id="5486a-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5486a-112">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5486a-113">restrita</span><span class="sxs-lookup"><span data-stu-id="5486a-113">constrained</span></span><br/> | <span data-ttu-id="5486a-114">Esse atributo é opcional para um documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="5486a-114">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="5486a-115">Esse atributo indica se a opção está disponível para seleção ou uso.</span><span class="sxs-lookup"><span data-stu-id="5486a-115">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="5486a-116">Esse atributo XML pode ser definido como um dos seguintes valores: None, PrintTicketSettings, AdminSetting ou DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="5486a-116">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="5486a-117">Consulte [atributos XML](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="5486a-117">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="5486a-118">name</span><span class="sxs-lookup"><span data-stu-id="5486a-118">name</span></span><br/>        | <span data-ttu-id="5486a-119">Mantém o nome da opção, uma opção padrão ou uma opção definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="5486a-119">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="5486a-120">O atributo XML é usado dessa forma para diferenciar as instâncias de opção.</span><span class="sxs-lookup"><span data-stu-id="5486a-120">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="5486a-121">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5486a-121">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="5486a-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5486a-122">Element Information</span></span>

<span data-ttu-id="5486a-123">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="5486a-123">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="5486a-124">Category</span><span class="sxs-lookup"><span data-stu-id="5486a-124">Category</span></span>                   | <span data-ttu-id="5486a-125">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5486a-125">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5486a-126">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5486a-126">Parent elements</span></span><br/> | <span data-ttu-id="5486a-127">Recurso</span><span class="sxs-lookup"><span data-stu-id="5486a-127">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5486a-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5486a-128">Child elements</span></span><br/>  | <span data-ttu-id="5486a-129">*Propriedade* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5486a-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="5486a-130">*ScoredProperty* (zero ou mais opções com o atributo XML ' name '; uma ou mais opções for que não utilizam o atributo XML ' name ' \* )</span><span class="sxs-lookup"><span data-stu-id="5486a-130">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="5486a-131">\* somente as opções públicas definidas no esquema de impressão não podem ter nenhum atributo ' name ', como DocumentNUp)</span><span class="sxs-lookup"><span data-stu-id="5486a-131">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="5486a-132">Este elemento</span><span class="sxs-lookup"><span data-stu-id="5486a-132">This element</span></span><br/>    | <span data-ttu-id="5486a-133">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="5486a-133">No character data is permitted.</span></span><br/> <span data-ttu-id="5486a-134">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="5486a-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="5486a-135">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="5486a-135">Configuration Dependencies</span></span>

<span data-ttu-id="5486a-136">Um elemento de definição de opção não pode ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="5486a-136">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="5486a-137">Uso do elemento</span><span class="sxs-lookup"><span data-stu-id="5486a-137">Element Usage</span></span>

<span data-ttu-id="5486a-138">A finalidade do elemento Option é caracterizar um dos Estados que um atributo de configuração de dispositivo, representado por um elemento Feature, possa assumir.</span><span class="sxs-lookup"><span data-stu-id="5486a-138">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="5486a-139">Cada definição de elemento de opção contém um ou mais elementos ScoredProperty que descrevem uma característica intrínseca ou essencial dessa opção.</span><span class="sxs-lookup"><span data-stu-id="5486a-139">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="5486a-140">Para facilitar a portabilidade e a preservação da intenção, o esquema de impressão define muitos elementos de recursos comuns e uma variedade de elementos de opção para cada recurso.</span><span class="sxs-lookup"><span data-stu-id="5486a-140">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="5486a-141">Portanto, é importante usar elementos de opção de impressão definidos pelo esquema, se possível, antes de criar suas próprias definições de opção.</span><span class="sxs-lookup"><span data-stu-id="5486a-141">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="5486a-142">Entender o processo de definição de elementos de opção fornece informações úteis sobre o modo como os documentos e PrintCapabilities de impressão são usados nas arquiteturas do Microsoft .NET Framework versão 3,0 e do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5486a-142">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="5486a-143">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5486a-143">Example</span></span>

<span data-ttu-id="5486a-144">O exemplo a seguir define um nome para a opção.</span><span class="sxs-lookup"><span data-stu-id="5486a-144">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="5486a-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5486a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5486a-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5486a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




