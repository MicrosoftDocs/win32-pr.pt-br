---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165276"
---
# <a name="datetimeformat"></a><span data-ttu-id="bab2d-104">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="bab2d-104">dateTimeFormat</span></span>

<span data-ttu-id="bab2d-105">Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bab2d-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="bab2d-106">Isso é aplicável somente se <displayInfo displayType="DateTime"> .</span><span class="sxs-lookup"><span data-stu-id="bab2d-106">This is applicable only if <displayInfo displayType="DateTime">.</span></span> <span data-ttu-id="bab2d-107">Deve haver apenas um elemento [DateTimeFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="bab2d-107">There should be only one [dateTimeFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="bab2d-108">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="bab2d-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="bab2d-109">Se nenhum elemento [DateTimeFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="bab2d-109">If no [dateTimeFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab2d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab2d-110">Syntax</span></span>


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
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
```



## <a name="element-information"></a><span data-ttu-id="bab2d-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="bab2d-111">Element Information</span></span>



| <span data-ttu-id="bab2d-112">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="bab2d-112">Parent Element</span></span>                                   | <span data-ttu-id="bab2d-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bab2d-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="bab2d-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="bab2d-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="bab2d-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bab2d-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="bab2d-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="bab2d-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bab2d-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="bab2d-117">Attribute</span></span></th>
<th><span data-ttu-id="bab2d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="bab2d-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bab2d-119">formato de</span><span class="sxs-lookup"><span data-stu-id="bab2d-119">formatAs</span></span></td>
<td><span data-ttu-id="bab2d-120">Público.</span><span class="sxs-lookup"><span data-stu-id="bab2d-120">Public.</span></span> <span data-ttu-id="bab2d-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bab2d-121">Optional.</span></span> <span data-ttu-id="bab2d-122">O padrão é &quot; geral &quot; .</span><span class="sxs-lookup"><span data-stu-id="bab2d-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="bab2d-123">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="bab2d-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bab2d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bab2d-124">Value</span></span></th>
<th><span data-ttu-id="bab2d-125">Significado</span><span class="sxs-lookup"><span data-stu-id="bab2d-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bab2d-126">Geral</span><span class="sxs-lookup"><span data-stu-id="bab2d-126">General</span></span></td>
<td><span data-ttu-id="bab2d-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="bab2d-127">Default.</span></span> <span data-ttu-id="bab2d-128">Formata o valor de data e hora usando <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bab2d-128">Formats the date-time value using <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span></span> <span data-ttu-id="bab2d-129">Use os atributos <em>formatTimeAs</em> e <em>formatDateAs</em> para especificar como a hora e a data são formatadas.</span><span class="sxs-lookup"><span data-stu-id="bab2d-129">Use the <em>formatTimeAs</em> and <em>formatDateAs</em> attributes to specify how the time and date are formatted.</span></span> <span data-ttu-id="bab2d-130">Requer que o tipo de propriedade seja DateTime.</span><span class="sxs-lookup"><span data-stu-id="bab2d-130">Requires the property type to be DateTime.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bab2d-131">Mês</span><span class="sxs-lookup"><span data-stu-id="bab2d-131">Month</span></span></td>
<td><span data-ttu-id="bab2d-132">Formata o valor como um dos meses do ano.</span><span class="sxs-lookup"><span data-stu-id="bab2d-132">Formats the value as one of the months of the year.</span></span> <span data-ttu-id="bab2d-133">Requer que o tipo de propriedade seja Int32.</span><span class="sxs-lookup"><span data-stu-id="bab2d-133">Requires the property type to be Int32.</span></span> <span data-ttu-id="bab2d-134">O valor deve ser armazenado como um valor numérico com 1 representando o primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="bab2d-134">The value must be stored as a numeric value with 1 representing the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bab2d-135">YearMonth</span><span class="sxs-lookup"><span data-stu-id="bab2d-135">YearMonth</span></span></td>
<td><span data-ttu-id="bab2d-136">Formata o valor como &quot; ano-mês &quot; .</span><span class="sxs-lookup"><span data-stu-id="bab2d-136">Formats the value as &quot;Year - Month&quot;.</span></span> <span data-ttu-id="bab2d-137">Requer que o tipo de propriedade seja Int32.</span><span class="sxs-lookup"><span data-stu-id="bab2d-137">Requires the property type to be Int32.</span></span> <span data-ttu-id="bab2d-138">O valor deve ser armazenado de modo que os dois bytes mais altos especifiquem o ano e os dois bytes inferiores especifiquem o mês.</span><span class="sxs-lookup"><span data-stu-id="bab2d-138">The value must be stored such that the two highest bytes specify the year and the lower two bytes specify the month.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bab2d-139">Year</span><span class="sxs-lookup"><span data-stu-id="bab2d-139">Year</span></span></td>
<td><span data-ttu-id="bab2d-140">Formata o valor como uma cadeia de caracteres simples.</span><span class="sxs-lookup"><span data-stu-id="bab2d-140">Formats the value as a simple string.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bab2d-141">formatTimeAs</span><span class="sxs-lookup"><span data-stu-id="bab2d-141">formatTimeAs</span></span></td>
<td><span data-ttu-id="bab2d-142">Público.</span><span class="sxs-lookup"><span data-stu-id="bab2d-142">Public.</span></span> <span data-ttu-id="bab2d-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bab2d-143">Optional.</span></span> <span data-ttu-id="bab2d-144">O padrão é &quot; curtotime &quot; .</span><span class="sxs-lookup"><span data-stu-id="bab2d-144">Default is &quot;ShortTime&quot;.</span></span> <span data-ttu-id="bab2d-145">Especifica o formato no qual exibir a hora.</span><span class="sxs-lookup"><span data-stu-id="bab2d-145">Specifies the format in which to display time.</span></span> <span data-ttu-id="bab2d-146">Aplica-se quando <strong>formatas = &quot; geral &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="bab2d-146">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="bab2d-147">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="bab2d-147">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bab2d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="bab2d-148">Value</span></span></th>
<th><span data-ttu-id="bab2d-149">Significado</span><span class="sxs-lookup"><span data-stu-id="bab2d-149">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bab2d-150">Curtotime</span><span class="sxs-lookup"><span data-stu-id="bab2d-150">ShortTime</span></span></td>
<td><span data-ttu-id="bab2d-151">Padrão.</span><span class="sxs-lookup"><span data-stu-id="bab2d-151">Default.</span></span> <span data-ttu-id="bab2d-152">Mostre o tempo como &quot; 7:48 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="bab2d-152">Show the time like &quot;7:48 PM&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bab2d-153">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="bab2d-153">LongTime</span></span></td>
<td><span data-ttu-id="bab2d-154">Mostre o tempo como &quot; 7:48:33 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="bab2d-154">Show the time like &quot;7:48:33 PM&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bab2d-155">Ocultartime</span><span class="sxs-lookup"><span data-stu-id="bab2d-155">HideTime</span></span></td>
<td><span data-ttu-id="bab2d-156">Não exibir a parte de hora da data.</span><span class="sxs-lookup"><span data-stu-id="bab2d-156">Do not display the time portion of the date.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bab2d-157">formatDateAs</span><span class="sxs-lookup"><span data-stu-id="bab2d-157">formatDateAs</span></span></td>
<td><span data-ttu-id="bab2d-158">Público.</span><span class="sxs-lookup"><span data-stu-id="bab2d-158">Public.</span></span> <span data-ttu-id="bab2d-159">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bab2d-159">Optional.</span></span> <span data-ttu-id="bab2d-160">O padrão é &quot; ShortDate &quot; .</span><span class="sxs-lookup"><span data-stu-id="bab2d-160">Default is &quot;ShortDate&quot;.</span></span> <span data-ttu-id="bab2d-161">Especifica o formato no qual exibir a data.</span><span class="sxs-lookup"><span data-stu-id="bab2d-161">Specifies the format in which to display the date.</span></span> <span data-ttu-id="bab2d-162">Aplica-se quando <strong>formatas = &quot; geral &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="bab2d-162">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="bab2d-163">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="bab2d-163">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bab2d-164">Valor</span><span class="sxs-lookup"><span data-stu-id="bab2d-164">Value</span></span></th>
<th><span data-ttu-id="bab2d-165">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bab2d-165">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bab2d-166">ShortDate</span><span class="sxs-lookup"><span data-stu-id="bab2d-166">ShortDate</span></span></td>
<td><span data-ttu-id="bab2d-167">Padrão.</span><span class="sxs-lookup"><span data-stu-id="bab2d-167">Default.</span></span> <span data-ttu-id="bab2d-168">Mostre a data como &quot; 5/13/59 &quot; .</span><span class="sxs-lookup"><span data-stu-id="bab2d-168">Show the date like &quot;5/13/59&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bab2d-169">LongDate</span><span class="sxs-lookup"><span data-stu-id="bab2d-169">LongDate</span></span></td>
<td><span data-ttu-id="bab2d-170">Mostre a data como &quot; quarta-feira, 13 de maio de 1959 &quot; .</span><span class="sxs-lookup"><span data-stu-id="bab2d-170">Show the date like &quot;Wednesday, May 13, 1959&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bab2d-171">HideDate</span><span class="sxs-lookup"><span data-stu-id="bab2d-171">HideDate</span></span></td>
<td><span data-ttu-id="bab2d-172">Não exibir a parte de data.</span><span class="sxs-lookup"><span data-stu-id="bab2d-172">Do not display the date portion.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bab2d-173">RelativeShortDate</span><span class="sxs-lookup"><span data-stu-id="bab2d-173">RelativeShortDate</span></span></td>
<td><span data-ttu-id="bab2d-174">Mostre a data como &quot; ShortDate &quot; , mas use descrições relativas, como &quot; ontem &quot; , sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="bab2d-174">Show the date like &quot;ShortDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bab2d-175">RelativeLongDate</span><span class="sxs-lookup"><span data-stu-id="bab2d-175">RelativeLongDate</span></span></td>
<td><span data-ttu-id="bab2d-176">Mostre a data como &quot; LongDate &quot; , mas use descrições relativas, como &quot; ontem &quot; , sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="bab2d-176">Show the date like &quot;LongDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
