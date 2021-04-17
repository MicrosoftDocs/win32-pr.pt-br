---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762970"
---
# <a name="enumeratedlist"></a><span data-ttu-id="f03c7-103">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f03c7-103">enumeratedList</span></span>

<span data-ttu-id="f03c7-104">Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f03c7-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="f03c7-105">Ele também influencia como a propriedade pode ser agrupada ou quais valores mostrar na lista se o "editControl" for um listblox.</span><span class="sxs-lookup"><span data-stu-id="f03c7-105">It also influences how the property may be grouped, or what values to show in the list if the "editControl" is a listblox.</span></span> <span data-ttu-id="f03c7-106">Isso é aplicável somente se <displayInfo displayType="Enumerated"> .</span><span class="sxs-lookup"><span data-stu-id="f03c7-106">This is applicable only if <displayInfo displayType="Enumerated">.</span></span> <span data-ttu-id="f03c7-107">Deve haver apenas um elemento [enumeratedList]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f03c7-107">There should be only one [enumeratedList]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="f03c7-108">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="f03c7-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="f03c7-109">Se nenhum elemento [enumeratedList]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="f03c7-109">If no [enumeratedList]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f03c7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f03c7-110">Syntax</span></span>


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f03c7-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f03c7-111">Element Information</span></span>



| <span data-ttu-id="f03c7-112">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f03c7-112">Parent Element</span></span>                                   | <span data-ttu-id="f03c7-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f03c7-113">Child Elements</span></span>                               |
|--------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="f03c7-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f03c7-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | [<span data-ttu-id="f03c7-115">enumera</span><span class="sxs-lookup"><span data-stu-id="f03c7-115">enum</span></span>](./propdesc-schema-enum.md)           |
|                                                  | [<span data-ttu-id="f03c7-116">enumRange</span><span class="sxs-lookup"><span data-stu-id="f03c7-116">enumRange</span></span>](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a><span data-ttu-id="f03c7-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="f03c7-117">Attributes</span></span>



| <span data-ttu-id="f03c7-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="f03c7-118">Attribute</span></span>          | <span data-ttu-id="f03c7-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="f03c7-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f03c7-120">defaultText</span><span class="sxs-lookup"><span data-stu-id="f03c7-120">defaultText</span></span>        | <span data-ttu-id="f03c7-121">Público.</span><span class="sxs-lookup"><span data-stu-id="f03c7-121">Public.</span></span> <span data-ttu-id="f03c7-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f03c7-122">Optional.</span></span> <span data-ttu-id="f03c7-123">Especifique o texto padrão a ser usado se um valor for fornecido a [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) que não é mapeado para um dos elementos enumerados na lista.</span><span class="sxs-lookup"><span data-stu-id="f03c7-123">Specify default text to use if a value is given to [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) that does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="f03c7-124">A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta; Use a referência, para que possa ser localizada.</span><span class="sxs-lookup"><span data-stu-id="f03c7-124">The syntax allows for a direct display string or an indirect display string reference; use the reference, so it can be localized.</span></span>                              |
| <span data-ttu-id="f03c7-125">useValueForDefault</span><span class="sxs-lookup"><span data-stu-id="f03c7-125">useValueForDefault</span></span> | <span data-ttu-id="f03c7-126">Público.</span><span class="sxs-lookup"><span data-stu-id="f03c7-126">Public.</span></span> <span data-ttu-id="f03c7-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f03c7-127">Optional.</span></span> <span data-ttu-id="f03c7-128">Definir isso como "true" informará [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) para usar o valor como está se o valor não for mapeado para um dos elementos enumerados na lista.</span><span class="sxs-lookup"><span data-stu-id="f03c7-128">Setting this to "true" will inform [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) to use the value as-is if the value does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="f03c7-129">Para **IPropertyDescription:: FormatForDisplay**, definir como "true" tem precedência sobre a definição de "DefaultText".</span><span class="sxs-lookup"><span data-stu-id="f03c7-129">For **IPropertyDescription::FormatForDisplay**, setting this to "true" takes precedence over setting the "defaultText".</span></span> <span data-ttu-id="f03c7-130">O padrão é "falso".</span><span class="sxs-lookup"><span data-stu-id="f03c7-130">The default is "false".</span></span> |



 

 

 
