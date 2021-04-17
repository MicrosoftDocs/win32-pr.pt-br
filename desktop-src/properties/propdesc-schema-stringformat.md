---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755141"
---
# <a name="stringformat"></a><span data-ttu-id="4bd64-104">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4bd64-104">stringFormat</span></span>

<span data-ttu-id="4bd64-105">Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4bd64-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="4bd64-106">Isso é aplicável somente se <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="4bd64-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="4bd64-107">Deve haver apenas um elemento [StringFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="4bd64-107">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="4bd64-108">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="4bd64-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="4bd64-109">Se nenhum elemento [StringFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="4bd64-109">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd64-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bd64-110">Syntax</span></span>


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="4bd64-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4bd64-111">Element Information</span></span>



| <span data-ttu-id="4bd64-112">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="4bd64-112">Parent Element</span></span>                                   | <span data-ttu-id="4bd64-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4bd64-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="4bd64-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4bd64-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="4bd64-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4bd64-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="4bd64-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="4bd64-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bd64-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="4bd64-117">Attribute</span></span></th>
<th><span data-ttu-id="4bd64-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bd64-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bd64-119">formato de</span><span class="sxs-lookup"><span data-stu-id="4bd64-119">formatAs</span></span></td>
<td><span data-ttu-id="4bd64-120">Público.</span><span class="sxs-lookup"><span data-stu-id="4bd64-120">Public.</span></span> <span data-ttu-id="4bd64-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bd64-121">Optional.</span></span> <span data-ttu-id="4bd64-122">O padrão é &quot; geral &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bd64-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="4bd64-123">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="4bd64-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4bd64-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4bd64-124">Value</span></span></th>
<th><span data-ttu-id="4bd64-125">Significado</span><span class="sxs-lookup"><span data-stu-id="4bd64-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bd64-126">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd64-126">General</span></span></td>
<td><span data-ttu-id="4bd64-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="4bd64-127">Default.</span></span> <span data-ttu-id="4bd64-128">Retorna o valor como uma cadeia de caracteres não formatada.</span><span class="sxs-lookup"><span data-stu-id="4bd64-128">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bd64-129">FileName</span><span class="sxs-lookup"><span data-stu-id="4bd64-129">FileName</span></span></td>
<td><span data-ttu-id="4bd64-130">Formata o valor como um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4bd64-130">Formats the value as a file name.</span></span> <span data-ttu-id="4bd64-131">Oculta a extensão de acordo com as configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="4bd64-131">Hides the extension according to user settings.</span></span> <span data-ttu-id="4bd64-132">Requer que o tipo de propriedade seja cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4bd64-132">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bd64-133">FilePath</span><span class="sxs-lookup"><span data-stu-id="4bd64-133">FilePath</span></span></td>
<td><span data-ttu-id="4bd64-134">Formata o valor como um caminho de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4bd64-134">Formats the value as a file path.</span></span> <span data-ttu-id="4bd64-135">Oculta a extensão de acordo com as configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="4bd64-135">Hides the extension according to user settings.</span></span> <span data-ttu-id="4bd64-136">Requer que o tipo de propriedade seja cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4bd64-136">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bd64-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="4bd64-137">Hyperlink</span></span></td>
<td><span data-ttu-id="4bd64-138">Formata o valor como um hiperlink.</span><span class="sxs-lookup"><span data-stu-id="4bd64-138">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
