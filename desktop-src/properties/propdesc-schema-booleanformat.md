---
description: Especifica como IPropertyDescription::FormatForDisplay deve formatar o valor da propriedade booleanFormat como uma cadeia de caracteres.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 528458d9c31d54ef43eca8325b1daeef4eee1195
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405959"
---
# <a name="booleanformat"></a><span data-ttu-id="61118-103">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="61118-103">booleanFormat</span></span>

<span data-ttu-id="61118-104">Especifica como [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="61118-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="61118-105">Isso será aplicável somente se <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="61118-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="61118-106">Deve haver apenas um elemento [booleanFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)</span><span class="sxs-lookup"><span data-stu-id="61118-106">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="61118-107">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="61118-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="61118-108">Se nenhum [elemento booleanFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="61118-108">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="61118-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61118-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="61118-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="61118-110">Element Information</span></span>



| <span data-ttu-id="61118-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="61118-111">Parent Element</span></span>                                   | <span data-ttu-id="61118-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="61118-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="61118-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="61118-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="61118-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61118-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="61118-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="61118-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61118-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="61118-116">Attribute</span></span></th>
<th><span data-ttu-id="61118-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="61118-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61118-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="61118-118">formatAs</span></span></td>
<td><span data-ttu-id="61118-119">Público.</span><span class="sxs-lookup"><span data-stu-id="61118-119">Public.</span></span> <span data-ttu-id="61118-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="61118-120">Optional.</span></span> <span data-ttu-id="61118-121">O padrão é &quot; &quot; YesNo.</span><span class="sxs-lookup"><span data-stu-id="61118-121">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="61118-122">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="61118-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="61118-123">Valor</span><span class="sxs-lookup"><span data-stu-id="61118-123">Value</span></span></th>
<th><span data-ttu-id="61118-124">Significado</span><span class="sxs-lookup"><span data-stu-id="61118-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61118-125">Yesno</span><span class="sxs-lookup"><span data-stu-id="61118-125">YesNo</span></span></td>
<td><span data-ttu-id="61118-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="61118-126">Default.</span></span> <span data-ttu-id="61118-127">Formatar o valor como &quot; Sim &quot; ou &quot; &quot; Não.</span><span class="sxs-lookup"><span data-stu-id="61118-127">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="61118-128">Requer que o tipo de propriedade seja booliana.</span><span class="sxs-lookup"><span data-stu-id="61118-128">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61118-129">Onoff</span><span class="sxs-lookup"><span data-stu-id="61118-129">OnOff</span></span></td>
<td><span data-ttu-id="61118-130">Formatar o valor como &quot; On &quot; ou &quot; &quot; Off.</span><span class="sxs-lookup"><span data-stu-id="61118-130">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="61118-131">Requer que o tipo de propriedade seja booliana.</span><span class="sxs-lookup"><span data-stu-id="61118-131">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61118-132">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="61118-132">TrueFalse</span></span></td>
<td><span data-ttu-id="61118-133">Formatar o valor como &quot; True &quot; ou &quot; &quot; False.</span><span class="sxs-lookup"><span data-stu-id="61118-133">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="61118-134">Requer que o tipo de propriedade seja booliana.</span><span class="sxs-lookup"><span data-stu-id="61118-134">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
