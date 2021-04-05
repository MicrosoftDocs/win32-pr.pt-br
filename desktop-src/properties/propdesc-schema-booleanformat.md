---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91332f0cc062e7ee4a83e3584776ecf09c5c4b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921814"
---
# <a name="booleanformat"></a><span data-ttu-id="1e7fb-104">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1e7fb-104">booleanFormat</span></span>

<span data-ttu-id="1e7fb-105">Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="1e7fb-106">Isso é aplicável somente se <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="1e7fb-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="1e7fb-107">Deve haver apenas um elemento [booleanFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1e7fb-107">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="1e7fb-108">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="1e7fb-109">Se nenhum elemento [booleanFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-109">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e7fb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e7fb-110">Syntax</span></span>


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="1e7fb-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1e7fb-111">Element Information</span></span>



| <span data-ttu-id="1e7fb-112">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1e7fb-112">Parent Element</span></span>                                   | <span data-ttu-id="1e7fb-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1e7fb-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="1e7fb-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1e7fb-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="1e7fb-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1e7fb-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="1e7fb-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="1e7fb-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e7fb-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="1e7fb-117">Attribute</span></span></th>
<th><span data-ttu-id="1e7fb-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e7fb-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e7fb-119">formato de</span><span class="sxs-lookup"><span data-stu-id="1e7fb-119">formatAs</span></span></td>
<td><span data-ttu-id="1e7fb-120">Público.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-120">Public.</span></span> <span data-ttu-id="1e7fb-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-121">Optional.</span></span> <span data-ttu-id="1e7fb-122">O padrão é &quot; YesNo &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e7fb-122">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="1e7fb-123">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="1e7fb-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1e7fb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1e7fb-124">Value</span></span></th>
<th><span data-ttu-id="1e7fb-125">Significado</span><span class="sxs-lookup"><span data-stu-id="1e7fb-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e7fb-126">YesNo</span><span class="sxs-lookup"><span data-stu-id="1e7fb-126">YesNo</span></span></td>
<td><span data-ttu-id="1e7fb-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-127">Default.</span></span> <span data-ttu-id="1e7fb-128">Formata o valor como &quot; Sim &quot; ou &quot; não &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e7fb-128">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="1e7fb-129">Requer que o tipo de propriedade seja booliano.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-129">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7fb-130">OnOff</span><span class="sxs-lookup"><span data-stu-id="1e7fb-130">OnOff</span></span></td>
<td><span data-ttu-id="1e7fb-131">Formata o valor como &quot; on &quot; ou &quot; off &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e7fb-131">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="1e7fb-132">Requer que o tipo de propriedade seja booliano.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-132">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7fb-133">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="1e7fb-133">TrueFalse</span></span></td>
<td><span data-ttu-id="1e7fb-134">Formata o valor como &quot; true &quot; ou &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e7fb-134">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="1e7fb-135">Requer que o tipo de propriedade seja booliano.</span><span class="sxs-lookup"><span data-stu-id="1e7fb-135">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
