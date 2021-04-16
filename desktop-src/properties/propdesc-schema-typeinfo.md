---
description: Especifica as informações de tipo de uma propriedade.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758362"
---
# <a name="typeinfo"></a><span data-ttu-id="0102a-103">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0102a-103">typeInfo</span></span>

<span data-ttu-id="0102a-104">Especifica as informações de tipo de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-104">Specifies a property's type information.</span></span> <span data-ttu-id="0102a-105">Deve haver apenas um elemento [TypeInfo]() para cada [propertyDescription](./propdesc-schema-propertydescription.md).</span><span class="sxs-lookup"><span data-stu-id="0102a-105">There should be only one [typeInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span> <span data-ttu-id="0102a-106">Esse elemento foi alterado para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0102a-106">This element has changed for Windows 7.</span></span>

<span data-ttu-id="0102a-107">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="0102a-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="0102a-108">Se nenhum elemento [TypeInfo]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-108">If no [typeInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="0102a-109">Sintaxe do Windows 7</span><span class="sxs-lookup"><span data-stu-id="0102a-109">Syntax for Windows 7</span></span>


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="0102a-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0102a-110">Element Information</span></span>



| <span data-ttu-id="0102a-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="0102a-111">Parent Element</span></span>                                                   | <span data-ttu-id="0102a-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0102a-112">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="0102a-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0102a-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="0102a-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0102a-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0102a-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="0102a-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0102a-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="0102a-116">Attribute</span></span></th>
<th><span data-ttu-id="0102a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0102a-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0102a-118">type</span><span class="sxs-lookup"><span data-stu-id="0102a-118">type</span></span></td>
<td><span data-ttu-id="0102a-119">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-119">Public.</span></span> <span data-ttu-id="0102a-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-120">Optional.</span></span> <span data-ttu-id="0102a-121">O padrão é &quot; Any &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-121">Default is &quot;Any&quot;.</span></span> <span data-ttu-id="0102a-122">Indica o tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-122">Indicates the type of the property.</span></span> <span data-ttu-id="0102a-123">Veja a seguir os tipos válidos e seus tipos de variantes associados são recuperados por <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: Getpropertytype</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-123">The following are valid types and their associated variant types are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0102a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0102a-124">Value</span></span></th>
<th><span data-ttu-id="0102a-125">Significado</span><span class="sxs-lookup"><span data-stu-id="0102a-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0102a-126">Qualquer</span><span class="sxs-lookup"><span data-stu-id="0102a-126">Any</span></span></td>
<td><span data-ttu-id="0102a-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0102a-127">Default.</span></span> <span data-ttu-id="0102a-128">O subsistema de propriedades não impedirá ou imporá o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-128">The property subsystem will not enforce or coerce the property value.</span></span> <span data-ttu-id="0102a-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: Getpropertytype</strong></a> retorna VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="0102a-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span> <span data-ttu-id="0102a-130">ISVs (fornecedores independentes de software) são altamente incentivados a fornecer um tipo em vez de fazer fallback nesse padrão.</span><span class="sxs-lookup"><span data-stu-id="0102a-130">Independent software vendors (ISVs) are strongly encouraged to provide a type rather than fall back on this default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-131">Nulo</span><span class="sxs-lookup"><span data-stu-id="0102a-131">Null</span></span></td>
<td><span data-ttu-id="0102a-132">Não há nenhum valor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-132">There is no value for this property.</span></span> <span data-ttu-id="0102a-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: Getpropertytype</strong></a> retorna VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="0102a-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-134">String</span><span class="sxs-lookup"><span data-stu-id="0102a-134">String</span></span></td>
<td><span data-ttu-id="0102a-135">O valor deve ser um VT_LPWSTR, que é uma cadeia de caracteres Unicode terminada por uma referência nula.</span><span class="sxs-lookup"><span data-stu-id="0102a-135">The value must be a VT_LPWSTR, which is a Unicode string terminated by a null reference.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="0102a-136">Boolean</span></span></td>
<td><span data-ttu-id="0102a-137">O valor deve ser um VT_BOOL, que é um booliano.</span><span class="sxs-lookup"><span data-stu-id="0102a-137">The value must be a VT_BOOL, which is a boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-138">Byte</span><span class="sxs-lookup"><span data-stu-id="0102a-138">Byte</span></span></td>
<td><span data-ttu-id="0102a-139">O valor deve ser um VT_UI1, que é um byte.</span><span class="sxs-lookup"><span data-stu-id="0102a-139">The value must be a VT_UI1, which is a byte.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-140">Buffer</span><span class="sxs-lookup"><span data-stu-id="0102a-140">Buffer</span></span></td>
<td><span data-ttu-id="0102a-141">O valor deve ser um VT_UI1 | Buffer de VT_VECTOR de bytes.</span><span class="sxs-lookup"><span data-stu-id="0102a-141">The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-142">Int16</span><span class="sxs-lookup"><span data-stu-id="0102a-142">Int16</span></span></td>
<td><span data-ttu-id="0102a-143">O valor deve ser um VT_I2, que é um inteiro de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0102a-143">The value must be a VT_I2, which is a 16-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-144">UInt16</span><span class="sxs-lookup"><span data-stu-id="0102a-144">UInt16</span></span></td>
<td><span data-ttu-id="0102a-145">O valor deve ser um VT_UI2, que é um inteiro sem sinal de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0102a-145">The value must be a VT_UI2, which is a 16-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-146">Int32</span><span class="sxs-lookup"><span data-stu-id="0102a-146">Int32</span></span></td>
<td><span data-ttu-id="0102a-147">O valor deve ser um VT_I4, que é um inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0102a-147">The value must be a VT_I4, which is a 32-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-148">UInt32</span><span class="sxs-lookup"><span data-stu-id="0102a-148">UInt32</span></span></td>
<td><span data-ttu-id="0102a-149">O valor deve ser um VT_UI4, que é um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0102a-149">The value must be a VT_UI4, which is a 32-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-150">Int64</span><span class="sxs-lookup"><span data-stu-id="0102a-150">Int64</span></span></td>
<td><span data-ttu-id="0102a-151">O valor deve ser um VT_I8, que é um inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0102a-151">The value must be a VT_I8, which is a 64-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-152">UInt64</span><span class="sxs-lookup"><span data-stu-id="0102a-152">UInt64</span></span></td>
<td><span data-ttu-id="0102a-153">O valor deve ser um VT_UI8, que é um inteiro sem sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0102a-153">The value must be a VT_UI8, which is a 64-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-154">Double</span><span class="sxs-lookup"><span data-stu-id="0102a-154">Double</span></span></td>
<td><span data-ttu-id="0102a-155">O valor deve ser um VT_R8, que é um duplo.</span><span class="sxs-lookup"><span data-stu-id="0102a-155">The value must be a VT_R8, which is a double.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-156">Datetime</span><span class="sxs-lookup"><span data-stu-id="0102a-156">DateTime</span></span></td>
<td><span data-ttu-id="0102a-157">O valor deve ser um VT_FILETIME, que é um <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-157">The value must be a VT_FILETIME, which is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-158">Guid</span><span class="sxs-lookup"><span data-stu-id="0102a-158">Guid</span></span></td>
<td><span data-ttu-id="0102a-159">O valor deve ser um VT_CLSID, que é um identificador de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="0102a-159">The value must be a VT_CLSID, which is a class identifier (CLSID).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-160">Blob</span><span class="sxs-lookup"><span data-stu-id="0102a-160">Blob</span></span></td>
<td><span data-ttu-id="0102a-161">O valor deve ser um VT_BLOB, que são bytes de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="0102a-161">The value must be a VT_BLOB, which are length-prefixed bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-162">Stream</span><span class="sxs-lookup"><span data-stu-id="0102a-162">Stream</span></span></td>
<td><span data-ttu-id="0102a-163">O valor deve ser um VT_STREAM, que é um objeto que implementa <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-163">The value must be a VT_STREAM, which is an object that implements <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-164">Área de Transferência</span><span class="sxs-lookup"><span data-stu-id="0102a-164">Clipboard</span></span></td>
<td><span data-ttu-id="0102a-165">O valor deve ser um VT_CF, que é um formato de área de transferência.</span><span class="sxs-lookup"><span data-stu-id="0102a-165">The value must be a VT_CF, which is a clipboard format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-166">Objeto</span><span class="sxs-lookup"><span data-stu-id="0102a-166">Object</span></span></td>
<td><span data-ttu-id="0102a-167">O valor deve ser um VT_UNKNOWN, que é um objeto que implementa <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-167">The value must be a VT_UNKNOWN, which is an object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-168">groupingRange</span><span class="sxs-lookup"><span data-stu-id="0102a-168">groupingRange</span></span></td>
<td><span data-ttu-id="0102a-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-169">Optional.</span></span> <span data-ttu-id="0102a-170">O padrão é &quot; discreto &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-170">Default is &quot;Discrete&quot;.</span></span> <span data-ttu-id="0102a-171">Especifica como a propriedade é exibida quando uma exibição é agrupada por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-171">Specifies how the property is displayed when a view is grouped by this property.</span></span> <span data-ttu-id="0102a-172">Uma vez definido aqui, esses valores são recuperados por <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription:: GetGroupingRange</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-172">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>.</span></span> <span data-ttu-id="0102a-173">Os tipos a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="0102a-173">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0102a-174">Valor</span><span class="sxs-lookup"><span data-stu-id="0102a-174">Value</span></span></th>
<th><span data-ttu-id="0102a-175">Significado</span><span class="sxs-lookup"><span data-stu-id="0102a-175">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0102a-176">Discreto</span><span class="sxs-lookup"><span data-stu-id="0102a-176">Discrete</span></span></td>
<td><span data-ttu-id="0102a-177">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0102a-177">Default.</span></span> <span data-ttu-id="0102a-178">Exibe valores individuais.</span><span class="sxs-lookup"><span data-stu-id="0102a-178">Displays individual values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-179">Alfanumérico</span><span class="sxs-lookup"><span data-stu-id="0102a-179">Alphanumeric</span></span></td>
<td><span data-ttu-id="0102a-180">Exibe intervalos alfanuméricos estáticos para valores.</span><span class="sxs-lookup"><span data-stu-id="0102a-180">Displays static alphanumeric ranges for values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-181">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0102a-181">Size</span></span></td>
<td><span data-ttu-id="0102a-182">Exibe intervalos de tamanho estático para valores.</span><span class="sxs-lookup"><span data-stu-id="0102a-182">Displays static size ranges for values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-183">Data</span><span class="sxs-lookup"><span data-stu-id="0102a-183">Date</span></span></td>
<td><span data-ttu-id="0102a-184">Exibe os grupos de mês/ano.</span><span class="sxs-lookup"><span data-stu-id="0102a-184">Displays month/year groups.</span></span> <span data-ttu-id="0102a-185">Padrão para propriedades de Type = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-185">Default for properties of type=&quot;DateTime&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-186">Timerelativo</span><span class="sxs-lookup"><span data-stu-id="0102a-186">TimeRelative</span></span></td>
<td><span data-ttu-id="0102a-187">Exibe em grupos relativos a tempo.</span><span class="sxs-lookup"><span data-stu-id="0102a-187">Displays in time-relative groups.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-188">Dinâmico</span><span class="sxs-lookup"><span data-stu-id="0102a-188">Dynamic</span></span></td>
<td><span data-ttu-id="0102a-189">Exibe intervalos criados dinamicamente para os valores.</span><span class="sxs-lookup"><span data-stu-id="0102a-189">Displays dynamically created ranges for the values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-190">Porcentagem</span><span class="sxs-lookup"><span data-stu-id="0102a-190">Percent</span></span></td>
<td><span data-ttu-id="0102a-191">Exibe o percentual de buckets.</span><span class="sxs-lookup"><span data-stu-id="0102a-191">Displays percent buckets.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-192">isInnate</span><span class="sxs-lookup"><span data-stu-id="0102a-192">isInnate</span></span></td>
<td><span data-ttu-id="0102a-193">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-193">Public.</span></span> <span data-ttu-id="0102a-194">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-194">Optional.</span></span> <span data-ttu-id="0102a-195">O padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="0102a-195">Default is &quot;false&quot;.</span></span> <span data-ttu-id="0102a-196">Especifica se a propriedade é considerada inato.</span><span class="sxs-lookup"><span data-stu-id="0102a-196">Specifies whether the property is considered innate.</span></span> <span data-ttu-id="0102a-197">Uma propriedade inato é uma que é calculada a partir do conteúdo de um arquivo ou de outros recursos ou sistemas.</span><span class="sxs-lookup"><span data-stu-id="0102a-197">An innate property is one which is either calculated from the content of a file, or from other resources or systems.</span></span> <span data-ttu-id="0102a-198">Por exemplo, System. Size é uma propriedade inato fornecida pelo sistema de arquivos; alterar o valor da propriedade não faz nada.</span><span class="sxs-lookup"><span data-stu-id="0102a-198">For example, System.Size is an innate property provided by the file system; changing the value of the property in and of itself does nothing.</span></span> <span data-ttu-id="0102a-199">Outros exemplos são System. Image. Dimensions e System.Document. PageCount, que são calculados por programas baseados no conteúdo do arquivo, não com base em uma configuração de alteração do usuário.</span><span class="sxs-lookup"><span data-stu-id="0102a-199">Other examples are System.Image.Dimensions and System.Document.PageCount, which are calculated by programs based upon the content of the file, not based upon a user-changeable setting.</span></span> <span data-ttu-id="0102a-200">Definir isInnate = &quot; true &quot; significa que o usuário não pode editar essa propriedade diretamente por meio de um controle de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-200">Setting isInnate=&quot;true&quot; means the user cannot edit this property directly via a property control.</span></span> <span data-ttu-id="0102a-201">Esse valor é mapeado para o sinalizador de PDTF_ISINNATE definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-201">This value maps to the PDTF_ISINNATE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-202">canBePurged</span><span class="sxs-lookup"><span data-stu-id="0102a-202">canBePurged</span></span></td>
<td><span data-ttu-id="0102a-203"><strong>Windows Vista com Service Pack 1 (SP1) e posterior somente</strong>.</span><span class="sxs-lookup"><span data-stu-id="0102a-203"><strong>Windows Vista with Service Pack 1 (SP1) and later only</strong>.</span></span> <span data-ttu-id="0102a-204">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-204">Public.</span></span> <span data-ttu-id="0102a-205">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-205">Optional.</span></span> <span data-ttu-id="0102a-206">Quando definido como &quot; true &quot; , permite que uma propriedade inato seja excluída.</span><span class="sxs-lookup"><span data-stu-id="0102a-206">When set to &quot;true&quot;, allows an innate property to be deleted.</span></span> <span data-ttu-id="0102a-207">As propriedades inato, que são calculadas a partir de outras propriedades, são somente leitura por definição.</span><span class="sxs-lookup"><span data-stu-id="0102a-207">Innate properties, which are calculated from other properties, are read-only by definition.</span></span> <span data-ttu-id="0102a-208">O valor padrão para esse atributo depende do valor de <em>isInnate</em> .</span><span class="sxs-lookup"><span data-stu-id="0102a-208">The default value for this attribute depends on the <em>isInnate</em> value.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0102a-209">isInnate</span><span class="sxs-lookup"><span data-stu-id="0102a-209">isInnate</span></span></th>
<th><span data-ttu-id="0102a-210">Valor padrão de canBePurged</span><span class="sxs-lookup"><span data-stu-id="0102a-210">canBePurged Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0102a-211">true</span><span class="sxs-lookup"><span data-stu-id="0102a-211">true</span></span></td>
<td><span data-ttu-id="0102a-212">false</span><span class="sxs-lookup"><span data-stu-id="0102a-212">false</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-213">false</span><span class="sxs-lookup"><span data-stu-id="0102a-213">false</span></span></td>
<td><span data-ttu-id="0102a-214">true</span><span class="sxs-lookup"><span data-stu-id="0102a-214">true</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0102a-215">Uma propriedade cujo valor de <em>isInnate</em> é &quot; false &quot; (o que significa que a propriedade é leitura/gravação) também não pode definir o valor de <em>canBePurged</em> como &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-215">A property whose <em>isInnate</em> value is &quot;false&quot; (meaning that the property is read/write) cannot also set the <em>canBePurged</em> value to &quot;false&quot;.</span></span> <span data-ttu-id="0102a-216">Essa restrição é imposta pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0102a-216">This restriction is enforced by the operating system.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0102a-217">Embora esse atributo tenha sido introduzido no Windows Vista com Service Pack 1 (SP1), um arquivo. propDesc que inclui esse atributo é compatível com o Windows Vista antes do Windows Vista com SP1.</span><span class="sxs-lookup"><span data-stu-id="0102a-217">Although this attribute was introduced in Windows Vista with Service Pack 1 (SP1), a .propdesc file that includes this attribute is compatible with Windows Vista prior to Windows Vista with SP1.</span></span> <span data-ttu-id="0102a-218">O atributo <em>canBePurged</em> é simplesmente ignorado nessa situação.</span><span class="sxs-lookup"><span data-stu-id="0102a-218">The <em>canBePurged</em> attribute is simply ignored in that situation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-219">multipleValues</span><span class="sxs-lookup"><span data-stu-id="0102a-219">multipleValues</span></span></td>
<td><span data-ttu-id="0102a-220">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-220">Public.</span></span> <span data-ttu-id="0102a-221">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-221">Optional.</span></span> <span data-ttu-id="0102a-222">O padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="0102a-222">Default is &quot;false&quot;.</span></span> <span data-ttu-id="0102a-223">Especifica se essa propriedade pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="0102a-223">Specifies whether this property can have multiple values.</span></span> <span data-ttu-id="0102a-224">Esse valor é mapeado para o sinalizador de PDTF_MULTIPLEVALUES definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-224">This value maps to the PDTF_MULTIPLEVALUES flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span> <span data-ttu-id="0102a-225">Isso também influencia se VT_VECTOR é ou não o VARTYPE do valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-225">This also influences whether VT_VECTOR is OR'd to the VARTYPE of the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-226">isGroup</span><span class="sxs-lookup"><span data-stu-id="0102a-226">isGroup</span></span></td>
<td><span data-ttu-id="0102a-227">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-227">Public.</span></span> <span data-ttu-id="0102a-228">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-228">Optional.</span></span> <span data-ttu-id="0102a-229">O padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="0102a-229">Default is &quot;false&quot;.</span></span> <span data-ttu-id="0102a-230">Especifica se a propriedade é um título de grupo.</span><span class="sxs-lookup"><span data-stu-id="0102a-230">Specifies whether the property is a group heading.</span></span> <span data-ttu-id="0102a-231">Um título de grupo é estritamente usado em proplistes, não tem valor, nunca é armazenado em um arquivo e também deve ter <typeInfo type=&quot;Null&quot;> .</span><span class="sxs-lookup"><span data-stu-id="0102a-231">A group heading is strictly used in proplists, has no value, is never stored in a file, and should also have <typeInfo type=&quot;Null&quot;>.</span></span> <span data-ttu-id="0102a-232">Algumas interfaces do usuário no sistema usam o proplistor para indicar a sequência das propriedades a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="0102a-232">Some UI in the system use proplists to indicate the sequence of the properties to display.</span></span> <span data-ttu-id="0102a-233">Essas proplistes podem incluir referências a títulos de grupo (por exemplo, System. propus. Camera), que dizem à interface do usuário para iniciar uma nova seção de grupo (por exemplo, &quot; configurações de câmera &quot; ).</span><span class="sxs-lookup"><span data-stu-id="0102a-233">These proplists may include references to group headings (eg, System.PropGroup.Camera), which tell the UI to start a new group section (eg, &quot;Camera Settings&quot;).</span></span> <span data-ttu-id="0102a-234">Uma descrição de propriedade com IsGroup = &quot; true &quot; deve especificar um <labelInfo label=&quot;Some localized label&quot;> , caso contrário, não é uma propriedade útil.</span><span class="sxs-lookup"><span data-stu-id="0102a-234">A property description with isGroup=&quot;true&quot; should specify a <labelInfo label=&quot;Some localized label&quot;>, otherwise it isn't a useful property.</span></span> <span data-ttu-id="0102a-235">Esse valor é mapeado para o sinalizador de PDTF_ISGROUP definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-235">This value maps to the PDTF_ISGROUP flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-236">aggregationType</span><span class="sxs-lookup"><span data-stu-id="0102a-236">aggregationType</span></span></td>
<td><span data-ttu-id="0102a-237">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-237">Public.</span></span> <span data-ttu-id="0102a-238">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-238">Optional.</span></span> <span data-ttu-id="0102a-239">O padrão é &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-239">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="0102a-240">Especifica como as propriedades de agregação são exibidas quando vários itens são selecionados.</span><span class="sxs-lookup"><span data-stu-id="0102a-240">Specifies how aggregate properties are displayed when multiple items are selected.</span></span> <span data-ttu-id="0102a-241">Uma vez definido aqui, esses valores são recuperados por <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription:: Getaggregationtype</strong></a> como um <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-241">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> as an <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span></span> <span data-ttu-id="0102a-242">Os tipos a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="0102a-242">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0102a-243">Valor</span><span class="sxs-lookup"><span data-stu-id="0102a-243">Value</span></span></th>
<th><span data-ttu-id="0102a-244">Significado</span><span class="sxs-lookup"><span data-stu-id="0102a-244">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0102a-245">Padrão</span><span class="sxs-lookup"><span data-stu-id="0102a-245">Default</span></span></td>
<td><span data-ttu-id="0102a-246">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0102a-246">Default.</span></span> <span data-ttu-id="0102a-247">Exibe um espaço reservado de <strong>vários valores</strong> na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0102a-247">Displays a <strong>Multiple Values</strong> placeholder in the UI.</span></span> <span data-ttu-id="0102a-248">Esse será o padrão se o <em>tipo</em> for incompatível com o <em>AggregationType</em>especificado.</span><span class="sxs-lookup"><span data-stu-id="0102a-248">This is the default if the <em>type</em> is incompatible with the specified <em>aggregationType</em>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-249">Primeiro</span><span class="sxs-lookup"><span data-stu-id="0102a-249">First</span></span></td>
<td><span data-ttu-id="0102a-250">Exibe o valor da Propriedade do primeiro item na seleção ou coleção.</span><span class="sxs-lookup"><span data-stu-id="0102a-250">Displays the property value of the first item in the selection or collection.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-251">Somar</span><span class="sxs-lookup"><span data-stu-id="0102a-251">Sum</span></span></td>
<td><span data-ttu-id="0102a-252">Exibe a soma dos valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="0102a-252">Displays the sum of the numerical values.</span></span> <span data-ttu-id="0102a-253">Útil para propriedades como System. Media. Duration ou System. Size.</span><span class="sxs-lookup"><span data-stu-id="0102a-253">Useful for properties such as System.Media.Duration or System.Size.</span></span> <span data-ttu-id="0102a-254">Esse valor não é compatível com tipos não numéricos.</span><span class="sxs-lookup"><span data-stu-id="0102a-254">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-255">Média</span><span class="sxs-lookup"><span data-stu-id="0102a-255">Average</span></span></td>
<td><span data-ttu-id="0102a-256">Exibe a média dos valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="0102a-256">Displays the average of the numerical values.</span></span> <span data-ttu-id="0102a-257">Útil para propriedades como System. rating.</span><span class="sxs-lookup"><span data-stu-id="0102a-257">Useful for properties such as System.Rating.</span></span> <span data-ttu-id="0102a-258">Esse valor não é compatível com tipos não numéricos.</span><span class="sxs-lookup"><span data-stu-id="0102a-258">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-259">DateRange</span><span class="sxs-lookup"><span data-stu-id="0102a-259">DateRange</span></span></td>
<td><span data-ttu-id="0102a-260">Exibe um intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="0102a-260">Displays a range of dates.</span></span> <span data-ttu-id="0102a-261">Útil para propriedades como System. Photo. DateTaken.</span><span class="sxs-lookup"><span data-stu-id="0102a-261">Useful for properties like System.Photo.DateTaken.</span></span> <span data-ttu-id="0102a-262">Esse valor não é compatível com nada exceto Type = &quot; DateTime &quot; e é o padrão para propriedades desse tipo.</span><span class="sxs-lookup"><span data-stu-id="0102a-262">This value is not compatible with anything except type=&quot;DateTime&quot; and is the default for properties of that type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-263">Union</span><span class="sxs-lookup"><span data-stu-id="0102a-263">Union</span></span></td>
<td><span data-ttu-id="0102a-264">Exibe uma União de todos os valores na seleção ou na coleção.</span><span class="sxs-lookup"><span data-stu-id="0102a-264">Displays a union of all the values in the selection or collection.</span></span> <span data-ttu-id="0102a-265">A ordem na qual os valores são mostrados é indefinida.</span><span class="sxs-lookup"><span data-stu-id="0102a-265">The order in which the values are shown is undefined.</span></span> <span data-ttu-id="0102a-266">Esse valor é o padrão para propriedades de Type = &quot; String &quot; e multipleValues = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-266">This value is the default for properties of type=&quot;String&quot; and multipleValues=&quot;true&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-267">Máximo</span><span class="sxs-lookup"><span data-stu-id="0102a-267">Maximum</span></span></td>
<td><span data-ttu-id="0102a-268">Exibe o valor máximo na coleção.</span><span class="sxs-lookup"><span data-stu-id="0102a-268">Displays the maximum value in the collection.</span></span> <span data-ttu-id="0102a-269">Útil para propriedades como System. DateModified.</span><span class="sxs-lookup"><span data-stu-id="0102a-269">Useful for properties like System.DateModified.</span></span> <span data-ttu-id="0102a-270">Não compatível com tipos não numéricos ou não de data.</span><span class="sxs-lookup"><span data-stu-id="0102a-270">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-271">Mínimo</span><span class="sxs-lookup"><span data-stu-id="0102a-271">Minimum</span></span></td>
<td><span data-ttu-id="0102a-272">Exibe o valor mínimo na coleção.</span><span class="sxs-lookup"><span data-stu-id="0102a-272">Displays the minimum value in the collection.</span></span> <span data-ttu-id="0102a-273">Não compatível com tipos não numéricos ou não de data.</span><span class="sxs-lookup"><span data-stu-id="0102a-273">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-274">istreeproperty</span><span class="sxs-lookup"><span data-stu-id="0102a-274">isTreeProperty</span></span></td>
<td><span data-ttu-id="0102a-275">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-275">Public.</span></span> <span data-ttu-id="0102a-276">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-276">Optional.</span></span> <span data-ttu-id="0102a-277">O valor padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="0102a-277">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-278">isviewable</span><span class="sxs-lookup"><span data-stu-id="0102a-278">isViewable</span></span></td>
<td><span data-ttu-id="0102a-279">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-279">Public.</span></span> <span data-ttu-id="0102a-280">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-280">Optional.</span></span> <span data-ttu-id="0102a-281">O valor padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="0102a-281">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="0102a-282">Especifica se esta propriedade deve ser visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="0102a-282">Specifies whether this property is intended to be viewable to the user.</span></span> <span data-ttu-id="0102a-283">Por exemplo, a interface do usuário do seletor de coluna mostra apenas as propriedades que têm isviewable = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-283">For example, the Column Chooser UI only shows the properties that have isViewable=&quot;true&quot;.</span></span> <span data-ttu-id="0102a-284">A exceção é a interface do usuário que é controlada por uma PropList, que sempre mostrará a propriedade.</span><span class="sxs-lookup"><span data-stu-id="0102a-284">The exception is UI that is driven by a proplist, which will always show the property.</span></span> <span data-ttu-id="0102a-285">Se você tiver uma propriedade que serve apenas para modelar dados entre dois objetos e nunca se destina a ser visualizada pelo usuário, esse atributo deverá ser false.</span><span class="sxs-lookup"><span data-stu-id="0102a-285">If you have a property that is only meant to shuttle data between two objects, and never intended to be viewed by the user, this attribute should be false.</span></span> <span data-ttu-id="0102a-286">Esse valor é mapeado para o sinalizador de PDTF_ISVIEWABLE definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-286">This value maps to the PDTF_ISVIEWABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-287">isconsultáable</span><span class="sxs-lookup"><span data-stu-id="0102a-287">isQueryable</span></span></td>
<td><span data-ttu-id="0102a-288">Somente Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0102a-288">Windows Vista only.</span></span> <span data-ttu-id="0102a-289">Sem suporte no Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="0102a-289">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="0102a-290">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-290">Public.</span></span> <span data-ttu-id="0102a-291">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-291">Optional.</span></span> <span data-ttu-id="0102a-292">O valor padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="0102a-292">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="0102a-293">Especifica se esta propriedade deve estar disponível na interface do usuário do Construtor de Consultas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0102a-293">Specifies whether this property is intended to be available in the Search Query Builder UI.</span></span> <span data-ttu-id="0102a-294">Uma propriedade deve ter isviewable = &quot; true &quot; antes de isconsultáable = &quot; true &quot; ser respeitada.</span><span class="sxs-lookup"><span data-stu-id="0102a-294">A property must have isViewable=&quot;true&quot; before isQueryable=&quot;true&quot; is respected.</span></span> <span data-ttu-id="0102a-295">Esse valor é mapeado para o sinalizador de PDTF_ISQUERYABLE definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0102a-295">This value maps to the PDTF_ISQUERYABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-296">searchRawValue</span><span class="sxs-lookup"><span data-stu-id="0102a-296">searchRawValue</span></span></td>
<td><span data-ttu-id="0102a-297"><strong>Windows 7 e posterior.</strong></span><span class="sxs-lookup"><span data-stu-id="0102a-297"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="0102a-298">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-298">Public.</span></span> <span data-ttu-id="0102a-299">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-299">Optional.</span></span> <span data-ttu-id="0102a-300">O valor padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="0102a-300">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-301">includeInFullTextQuery</span><span class="sxs-lookup"><span data-stu-id="0102a-301">includeInFullTextQuery</span></span></td>
<td><span data-ttu-id="0102a-302">Somente Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0102a-302">Windows Vista only.</span></span> <span data-ttu-id="0102a-303">Sem suporte no Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="0102a-303">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="0102a-304">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-304">Public.</span></span> <span data-ttu-id="0102a-305">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-305">Optional.</span></span> <span data-ttu-id="0102a-306">O valor padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="0102a-306">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-307">conditionType</span><span class="sxs-lookup"><span data-stu-id="0102a-307">conditionType</span></span></td>
<td><span data-ttu-id="0102a-308">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-308">Public.</span></span> <span data-ttu-id="0102a-309">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-309">Optional.</span></span> <span data-ttu-id="0102a-310">O padrão é &quot; cadeia de caracteres &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-310">Default is &quot;String&quot;.</span></span> <span data-ttu-id="0102a-311">Especifica uma dica para a interface do usuário de Construtor de Consultas de pesquisa para que ela possa determinar a lista de possíveis operadores de condição dentro de um predicado.</span><span class="sxs-lookup"><span data-stu-id="0102a-311">Specifies a hint to the Search Query Builder UI so that it can determine the list of possible condition operators inside a predicate.</span></span> <span data-ttu-id="0102a-312">Os valores a seguir são reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="0102a-312">The following are recognized values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0102a-313">Valor</span><span class="sxs-lookup"><span data-stu-id="0102a-313">Value</span></span></th>
<th><span data-ttu-id="0102a-314">Significado</span><span class="sxs-lookup"><span data-stu-id="0102a-314">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0102a-315">String</span><span class="sxs-lookup"><span data-stu-id="0102a-315">String</span></span></td>
<td><span data-ttu-id="0102a-316">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0102a-316">Default.</span></span> <span data-ttu-id="0102a-317">Os seguintes operadores serão usados: is, is,,,,, &quot; &quot; &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; , começa com, &quot; &quot; &quot; termina com &quot; , &quot; Contains &quot; , &quot; não contém, &quot; &quot; é como &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-317">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;&lt;&quot;, &quot;&gt;&quot;, &quot;<=&quot;, &quot;>=&quot;, &quot;starts with&quot;, &quot;ends with&quot;, &quot;contains&quot;, &quot;doesn't contain&quot;, &quot;is like&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-318">Número</span><span class="sxs-lookup"><span data-stu-id="0102a-318">Number</span></span></td>
<td><span data-ttu-id="0102a-319">Padrão para propriedades numéricas.</span><span class="sxs-lookup"><span data-stu-id="0102a-319">Default for numeric properties.</span></span> <span data-ttu-id="0102a-320">Os seguintes operadores serão usados: Equals, não é igual a, é menor que, é maior que, é &quot; &quot; menor que &quot; &quot; &quot; &quot; &quot; &quot; &quot; ou igual a &quot; , &quot; é maior ou igual a &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-320">The following operators will be used: &quot;equals&quot;, &quot;doesn't equal&quot;, &quot;is less than&quot;, &quot;is greater than&quot;, &quot;is less than or equal to&quot;, &quot;is greater than or equal to&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-321">Datetime</span><span class="sxs-lookup"><span data-stu-id="0102a-321">DateTime</span></span></td>
<td><span data-ttu-id="0102a-322">Padrão para propriedades de Type = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-322">Default for properties of type=&quot;DateTime&quot;.</span></span> <span data-ttu-id="0102a-323">Os operadores a seguir serão usados: is, is, is, is before, for After, é &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; before, mas includes &quot; , &quot; é After, mas inclui &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-323">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;is before&quot;, &quot;is after&quot;, &quot;is before but includes&quot;, &quot;is after but includes&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-324">Boolean</span><span class="sxs-lookup"><span data-stu-id="0102a-324">Boolean</span></span></td>
<td><span data-ttu-id="0102a-325">Padrão para propriedades de Type = &quot; Boolean &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-325">Default for properties of type=&quot;Boolean&quot;.</span></span> <span data-ttu-id="0102a-326">O mesmo que o número.</span><span class="sxs-lookup"><span data-stu-id="0102a-326">Same as Number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-327">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0102a-327">Size</span></span></td>
<td><span data-ttu-id="0102a-328">O mesmo que o número.</span><span class="sxs-lookup"><span data-stu-id="0102a-328">Same as Number.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-329">defaultoperation</span><span class="sxs-lookup"><span data-stu-id="0102a-329">defaultOperation</span></span></td>
<td><span data-ttu-id="0102a-330">Público.</span><span class="sxs-lookup"><span data-stu-id="0102a-330">Public.</span></span> <span data-ttu-id="0102a-331">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102a-331">Optional.</span></span> <span data-ttu-id="0102a-332">O padrão é &quot; igual &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-332">Default is &quot;Equal&quot;.</span></span> <span data-ttu-id="0102a-333">Especifica uma dica para a ferramenta de Construtor de Consultas de pesquisa para que ela possa determinar o operador padrão.</span><span class="sxs-lookup"><span data-stu-id="0102a-333">Specifies a hint to the Search Query Builder tool so that it can determine the default operator.</span></span> <span data-ttu-id="0102a-334">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="0102a-334">The possible values are as follows:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0102a-335">Valor</span><span class="sxs-lookup"><span data-stu-id="0102a-335">Value</span></span></th>
<th><span data-ttu-id="0102a-336">Significado</span><span class="sxs-lookup"><span data-stu-id="0102a-336">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0102a-337">Igual</span><span class="sxs-lookup"><span data-stu-id="0102a-337">Equal</span></span></td>
<td><span data-ttu-id="0102a-338">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0102a-338">Default.</span></span> <span data-ttu-id="0102a-339">Indica o equivalente.</span><span class="sxs-lookup"><span data-stu-id="0102a-339">Indicates equivalent.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-340">NotEqual</span><span class="sxs-lookup"><span data-stu-id="0102a-340">NotEqual</span></span></td>
<td><span data-ttu-id="0102a-341">Indica não equivalente.</span><span class="sxs-lookup"><span data-stu-id="0102a-341">Indicates not equivalent.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-342">LessThan</span><span class="sxs-lookup"><span data-stu-id="0102a-342">LessThan</span></span></td>
<td><span data-ttu-id="0102a-343">Indica menor que.</span><span class="sxs-lookup"><span data-stu-id="0102a-343">Indicates less than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102a-344">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="0102a-344">GreaterThan</span></span></td>
<td><span data-ttu-id="0102a-345">Padrão para propriedades de ConditionType = &quot; Size &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-345">Default for properties of conditionType=&quot;Size&quot;.</span></span> <span data-ttu-id="0102a-346">Indica maior que.</span><span class="sxs-lookup"><span data-stu-id="0102a-346">Indicates greater than.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102a-347">Contém</span><span class="sxs-lookup"><span data-stu-id="0102a-347">Contains</span></span></td>
<td><span data-ttu-id="0102a-348">Padrão para propriedades de ConditionType = &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="0102a-348">Default for properties of conditionType=&quot;String&quot;.</span></span> <span data-ttu-id="0102a-349">Indica a inclusão.</span><span class="sxs-lookup"><span data-stu-id="0102a-349">Indicates inclusion.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
