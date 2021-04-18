---
description: Especifica as informações de exibição de uma propriedade.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff0bb441b4535c0b6c6f3183671fbe8ade09183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752547"
---
# <a name="displayinfo"></a><span data-ttu-id="a110c-103">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a110c-103">displayInfo</span></span>

<span data-ttu-id="a110c-104">Especifica as informações de exibição de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="a110c-104">Specifies a property's display information.</span></span> <span data-ttu-id="a110c-105">Deve haver apenas um elemento [DisplayInfo]() para cada [propertyDescription](./propdesc-schema-propertydescription.md).</span><span class="sxs-lookup"><span data-stu-id="a110c-105">There should be only one [displayInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span>

<span data-ttu-id="a110c-106">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="a110c-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="a110c-107">Se nenhum elemento [DisplayInfo]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a110c-107">If no [displayInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a110c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a110c-108">Syntax</span></span>


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="Percentage"/>
                                <xs:enumeration value="ByteSize"/>
                                <xs:enumeration value="KBSize"/>
                                <xs:enumeration value="SampleSize"/>
                                <xs:enumeration value="Bitrate"/>
                                <xs:enumeration value="SampleRate"/>
                                <xs:enumeration value="FrameRate"/>
                                <xs:enumeration value="Pixels"/>
                                <xs:enumeration value="DPI"/>
                                <xs:enumeration value="Duration"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatDurationAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="Month"/>
                                <xs:enumeration value="YearMonth"/>
                                <xs:enumeration value="Year"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatTimeAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="ShortTime"/>
                                <xs:enumeration value="LongTime"/>
                                <xs:enumeration value="HideTime"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatDateAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="ShortDate"/>
                                <xs:enumeration value="LongDate"/>
                                <xs:enumeration value="HideDate"/>
                                <xs:enumeration value="RelativeShortDate"/>
                                <xs:enumeration value="RelativeLongDate"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
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
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="PercentBar"/>
                                <xs:enumeration value="ProgressBar"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="StaticText"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Boolean"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="NumericText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="a110c-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a110c-109">Element Information</span></span>



| <span data-ttu-id="a110c-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a110c-110">Parent Element</span></span>                                                   | <span data-ttu-id="a110c-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a110c-111">Child Elements</span></span>                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a110c-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a110c-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="a110c-113">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a110c-113">stringFormat</span></span>](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [<span data-ttu-id="a110c-114">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a110c-114">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [<span data-ttu-id="a110c-115">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a110c-115">numberFormat</span></span>](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [<span data-ttu-id="a110c-116">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a110c-116">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [<span data-ttu-id="a110c-117">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a110c-117">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [<span data-ttu-id="a110c-118">drawControl</span><span class="sxs-lookup"><span data-stu-id="a110c-118">drawControl</span></span>](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="a110c-119">editControl</span><span class="sxs-lookup"><span data-stu-id="a110c-119">editControl</span></span>](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="a110c-120">filterControl</span><span class="sxs-lookup"><span data-stu-id="a110c-120">filterControl</span></span>](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | <span data-ttu-id="a110c-121">[queryControl](./propdesc-schema-querycontrol.md) (somente Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a110c-121">[queryControl](./propdesc-schema-querycontrol.md) (Windows Vista only.</span></span> <span data-ttu-id="a110c-122">Sem suporte no Windows 7 e posterior.)</span><span class="sxs-lookup"><span data-stu-id="a110c-122">Not supported in Windows 7 and later.)</span></span> |



 

## <a name="attributes"></a><span data-ttu-id="a110c-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="a110c-123">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a110c-124">Atributo</span><span class="sxs-lookup"><span data-stu-id="a110c-124">Attribute</span></span></th>
<th><span data-ttu-id="a110c-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="a110c-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a110c-126">defaultColumnWidth</span><span class="sxs-lookup"><span data-stu-id="a110c-126">defaultColumnWidth</span></span></td>
<td><span data-ttu-id="a110c-127">Público.</span><span class="sxs-lookup"><span data-stu-id="a110c-127">Public.</span></span> <span data-ttu-id="a110c-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a110c-128">Optional.</span></span> <span data-ttu-id="a110c-129">O padrão é &quot; 20 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a110c-129">Default is &quot;20&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-130">TipoDeExibição</span><span class="sxs-lookup"><span data-stu-id="a110c-130">displayType</span></span></td>
<td><span data-ttu-id="a110c-131">Público.</span><span class="sxs-lookup"><span data-stu-id="a110c-131">Public.</span></span> <span data-ttu-id="a110c-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a110c-132">Optional.</span></span> <span data-ttu-id="a110c-133">O padrão é &quot; cadeia de caracteres &quot; .</span><span class="sxs-lookup"><span data-stu-id="a110c-133">Default is &quot;String&quot;.</span></span> <span data-ttu-id="a110c-134">Especifica o tipo da cadeia de caracteres de exibição.</span><span class="sxs-lookup"><span data-stu-id="a110c-134">Specifies the type of the display string.</span></span> <span data-ttu-id="a110c-135">Uma vez definido aqui, os valores de <strong>PROPDESC_DISPLAYTYPE</strong> associados são recuperados por <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription:: getdisplaytype</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a110c-135">Once set here, the associated <strong>PROPDESC_DISPLAYTYPE</strong> values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>.</span></span> <span data-ttu-id="a110c-136">Os tipos a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="a110c-136">The following are valid types.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a110c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a110c-137">Value</span></span></th>
<th><span data-ttu-id="a110c-138">Significado</span><span class="sxs-lookup"><span data-stu-id="a110c-138">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a110c-139">String</span><span class="sxs-lookup"><span data-stu-id="a110c-139">String</span></span></td>
<td><span data-ttu-id="a110c-140">Padrão.</span><span class="sxs-lookup"><span data-stu-id="a110c-140">Default.</span></span> <span data-ttu-id="a110c-141">O valor é exibido como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a110c-141">Value is displayed as a string.</span></span> <span data-ttu-id="a110c-142">Use &quot; StringFormat &quot; para formatar.</span><span class="sxs-lookup"><span data-stu-id="a110c-142">Use &quot;stringFormat&quot; to format.</span></span> <span data-ttu-id="a110c-143">O método retorna PDDT_STRING.</span><span class="sxs-lookup"><span data-stu-id="a110c-143">Method returns PDDT_STRING.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-144">Número</span><span class="sxs-lookup"><span data-stu-id="a110c-144">Number</span></span></td>
<td><span data-ttu-id="a110c-145">Padrão para propriedades numéricas.</span><span class="sxs-lookup"><span data-stu-id="a110c-145">Default for numeric properties.</span></span> <span data-ttu-id="a110c-146">O valor é exibido como um número.</span><span class="sxs-lookup"><span data-stu-id="a110c-146">Value is displayed as a number.</span></span> <span data-ttu-id="a110c-147">Use &quot; NumberFormat &quot; para formatar.</span><span class="sxs-lookup"><span data-stu-id="a110c-147">Use &quot;numberFormat&quot; to format.</span></span> <span data-ttu-id="a110c-148">O método retorna PDDT_NUMBER.</span><span class="sxs-lookup"><span data-stu-id="a110c-148">Method returns PDDT_NUMBER.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="a110c-149">Boolean</span></span></td>
<td><span data-ttu-id="a110c-150">Padrão se <typeInfo type=&quot;Boolean&quot;> .</span><span class="sxs-lookup"><span data-stu-id="a110c-150">Default if <typeInfo type=&quot;Boolean&quot;>.</span></span> <span data-ttu-id="a110c-151">O valor é exibido como um booliano.</span><span class="sxs-lookup"><span data-stu-id="a110c-151">Value is displayed as a boolean.</span></span> <span data-ttu-id="a110c-152">Use &quot; booleanFormat &quot; para formatar.</span><span class="sxs-lookup"><span data-stu-id="a110c-152">Use &quot;booleanFormat&quot; to format.</span></span> <span data-ttu-id="a110c-153">O método retorna PDDT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="a110c-153">Method returns PDDT_BOOLEAN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-154">Datetime</span><span class="sxs-lookup"><span data-stu-id="a110c-154">DateTime</span></span></td>
<td><span data-ttu-id="a110c-155">Padrão se <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="a110c-155">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="a110c-156">O valor é exibido como uma data ou hora.</span><span class="sxs-lookup"><span data-stu-id="a110c-156">Value is displayed as a date or time.</span></span> <span data-ttu-id="a110c-157">Use &quot; DateTimeFormat &quot; para formatar.</span><span class="sxs-lookup"><span data-stu-id="a110c-157">Use &quot;dateTimeFormat&quot; to format.</span></span> <span data-ttu-id="a110c-158">O método retorna PDDT_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="a110c-158">Method returns PDDT_DATETIME.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-159">Enumeração</span><span class="sxs-lookup"><span data-stu-id="a110c-159">Enumeration</span></span></td>
<td><span data-ttu-id="a110c-160">O valor é exibido como um mapeamento de cadeia de caracteres de exibição fornecido pelo &quot; &quot; elemento enumeratedList.</span><span class="sxs-lookup"><span data-stu-id="a110c-160">Value is displayed as a display string mapping provided by the &quot;enumeratedList&quot; element.</span></span> <span data-ttu-id="a110c-161">O método retorna PDDT_ENUMERATED.</span><span class="sxs-lookup"><span data-stu-id="a110c-161">Method returns PDDT_ENUMERATED.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-162">alinhamento</span><span class="sxs-lookup"><span data-stu-id="a110c-162">alignment</span></span></td>
<td><span data-ttu-id="a110c-163">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a110c-163">Optional.</span></span> <span data-ttu-id="a110c-164">O padrão é &quot; Left &quot; .</span><span class="sxs-lookup"><span data-stu-id="a110c-164">Default is &quot;Left&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a110c-165">Valor</span><span class="sxs-lookup"><span data-stu-id="a110c-165">Value</span></span></th>
<th><span data-ttu-id="a110c-166">Significado</span><span class="sxs-lookup"><span data-stu-id="a110c-166">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a110c-167">Esquerda</span><span class="sxs-lookup"><span data-stu-id="a110c-167">Left</span></span></td>
<td><span data-ttu-id="a110c-168">Padrão.</span><span class="sxs-lookup"><span data-stu-id="a110c-168">Default.</span></span> <span data-ttu-id="a110c-169">Alinhar à esquerda.</span><span class="sxs-lookup"><span data-stu-id="a110c-169">Align left.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-170">Centro</span><span class="sxs-lookup"><span data-stu-id="a110c-170">Center</span></span></td>
<td><span data-ttu-id="a110c-171">Alinhar ao centro.</span><span class="sxs-lookup"><span data-stu-id="a110c-171">Align center.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-172">Direita</span><span class="sxs-lookup"><span data-stu-id="a110c-172">Right</span></span></td>
<td><span data-ttu-id="a110c-173">Alinhar à direita.</span><span class="sxs-lookup"><span data-stu-id="a110c-173">Align right.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-174">relativeDescriptionType</span><span class="sxs-lookup"><span data-stu-id="a110c-174">relativeDescriptionType</span></span></td>
<td><span data-ttu-id="a110c-175">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a110c-175">Optional.</span></span> <span data-ttu-id="a110c-176">O padrão é &quot; geral &quot; .</span><span class="sxs-lookup"><span data-stu-id="a110c-176">Default is &quot;General&quot;.</span></span> <span data-ttu-id="a110c-177">Especifica como dois valores dessa propriedade devem ser descritos quando eles são comparados entre si.</span><span class="sxs-lookup"><span data-stu-id="a110c-177">Specifies how two values of this property should be described when they are compared with one another.</span></span> <span data-ttu-id="a110c-178">No caso da equivalência, o &quot; mesmo &quot; sempre é usado.</span><span class="sxs-lookup"><span data-stu-id="a110c-178">In the case of equivalency, &quot;Same&quot; is always used.</span></span> <span data-ttu-id="a110c-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription:: GetRelativeDescription</strong></a> e <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription:: GetRelativeDescriptionType</strong></a> Use esse valor para determinar quais nomes de exibição de descrição relativa usar.</span><span class="sxs-lookup"><span data-stu-id="a110c-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> and <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> use this value to determine what relative description display names to use.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a110c-180">Valor</span><span class="sxs-lookup"><span data-stu-id="a110c-180">Value</span></span></th>
<th><span data-ttu-id="a110c-181">Significado</span><span class="sxs-lookup"><span data-stu-id="a110c-181">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a110c-182">Geral</span><span class="sxs-lookup"><span data-stu-id="a110c-182">General</span></span></td>
<td><span data-ttu-id="a110c-183">Padrão.</span><span class="sxs-lookup"><span data-stu-id="a110c-183">Default.</span></span> <span data-ttu-id="a110c-184">Usa diferentes diferentes &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a110c-184">Uses &quot;Different&quot; / &quot;Same&quot; / &quot;Different&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-185">Data</span><span class="sxs-lookup"><span data-stu-id="a110c-185">Date</span></span></td>
<td><span data-ttu-id="a110c-186">Padrão se <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="a110c-186">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="a110c-187">Usa &quot; o &quot;  /  &quot; mesmo &quot;  /  &quot; mais tarde &quot; , ou usa o &quot; mesmo mais &quot;  /  &quot; &quot;  /  &quot; recente &quot; , ou usa o &quot; mesmo mais cedo &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a110c-187">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;, or uses &quot;Older&quot; / &quot;Same&quot; / &quot;Newer&quot;, or uses &quot;Sooner&quot; / &quot;Same&quot; / &quot;Later&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-188">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a110c-188">Size</span></span></td>
<td><span data-ttu-id="a110c-189">Usa &quot; o &quot;  /  &quot; mesmo tamanho &quot;  /  &quot; maior&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-189">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-190">Contagem</span><span class="sxs-lookup"><span data-stu-id="a110c-190">Count</span></span></td>
<td><span data-ttu-id="a110c-191">Usa &quot; o &quot;  /  &quot; mesmo tamanho &quot;  /  &quot; maior&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-191">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-192">Revisão</span><span class="sxs-lookup"><span data-stu-id="a110c-192">Revision</span></span></td>
<td><span data-ttu-id="a110c-193">Usa o &quot; anterior &quot;  /  &quot; mesmo &quot;  /  &quot; mais tarde&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-193">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-194">Comprimento</span><span class="sxs-lookup"><span data-stu-id="a110c-194">Length</span></span></td>
<td><span data-ttu-id="a110c-195">Usa o &quot; &quot;  /  &quot; mesmo &quot;  /  &quot; mais curto&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-195">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-196">Duration</span><span class="sxs-lookup"><span data-stu-id="a110c-196">Duration</span></span></td>
<td><span data-ttu-id="a110c-197">Usa o &quot; &quot;  /  &quot; mesmo &quot;  /  &quot; mais curto&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-197">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-198">Velocidade</span><span class="sxs-lookup"><span data-stu-id="a110c-198">Speed</span></span></td>
<td><span data-ttu-id="a110c-199">Usa o &quot; &quot;  /  &quot; mesmo &quot;  /  &quot; mais rápido&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-199">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-200">Tarifa</span><span class="sxs-lookup"><span data-stu-id="a110c-200">Rate</span></span></td>
<td><span data-ttu-id="a110c-201">Usa o &quot; &quot;  /  &quot; mesmo &quot;  /  &quot; mais rápido&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-201">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-202">Classificação</span><span class="sxs-lookup"><span data-stu-id="a110c-202">Rating</span></span></td>
<td><span data-ttu-id="a110c-203">Usa &quot; o &quot;  /  &quot; mesmo &quot;  /  &quot; mais alto&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-203">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-204">Prioridade</span><span class="sxs-lookup"><span data-stu-id="a110c-204">Priority</span></span></td>
<td><span data-ttu-id="a110c-205">Usa &quot; o &quot;  /  &quot; mesmo &quot;  /  &quot; mais alto&quot;</span><span class="sxs-lookup"><span data-stu-id="a110c-205">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a110c-206">defaultSortDirection</span><span class="sxs-lookup"><span data-stu-id="a110c-206">defaultSortDirection</span></span></td>
<td><span data-ttu-id="a110c-207">Especifica a direção da classificação.</span><span class="sxs-lookup"><span data-stu-id="a110c-207">Specifies sort direction.</span></span> <span data-ttu-id="a110c-208">O padrão é &quot; Ascending &quot; .</span><span class="sxs-lookup"><span data-stu-id="a110c-208">Default is &quot;Ascending&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a110c-209">Valor</span><span class="sxs-lookup"><span data-stu-id="a110c-209">Value</span></span></th>
<th><span data-ttu-id="a110c-210">Significado</span><span class="sxs-lookup"><span data-stu-id="a110c-210">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a110c-211">Crescente</span><span class="sxs-lookup"><span data-stu-id="a110c-211">Ascending</span></span></td>
<td><span data-ttu-id="a110c-212">Classifica em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="a110c-212">Sorts ascending.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a110c-213">Decrescente</span><span class="sxs-lookup"><span data-stu-id="a110c-213">Descending</span></span></td>
<td><span data-ttu-id="a110c-214">Classifica decrescente.</span><span class="sxs-lookup"><span data-stu-id="a110c-214">Sorts descending.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
