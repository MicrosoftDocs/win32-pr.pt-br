---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758364"
---
# <a name="numberformat"></a><span data-ttu-id="8c017-104">numberFormat</span><span class="sxs-lookup"><span data-stu-id="8c017-104">numberFormat</span></span>

<span data-ttu-id="8c017-105">Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8c017-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="8c017-106">Isso é aplicável somente se <displayInfo displayType="Number"> .</span><span class="sxs-lookup"><span data-stu-id="8c017-106">This is applicable only if <displayInfo displayType="Number">.</span></span> <span data-ttu-id="8c017-107">Deve haver apenas um elemento [NumberFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="8c017-107">There should be only one [numberFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="8c017-108">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="8c017-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="8c017-109">Se nenhum elemento [NumberFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c017-109">If no [numberFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c017-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c017-110">Syntax</span></span>


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
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
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="8c017-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8c017-111">Element Information</span></span>



| <span data-ttu-id="8c017-112">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="8c017-112">Parent Element</span></span>                                   | <span data-ttu-id="8c017-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8c017-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="8c017-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="8c017-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="8c017-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8c017-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="8c017-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c017-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c017-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="8c017-117">Attribute</span></span></th>
<th><span data-ttu-id="8c017-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c017-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c017-119">formato de</span><span class="sxs-lookup"><span data-stu-id="8c017-119">formatAs</span></span></td>
<td><span data-ttu-id="8c017-120">Público.</span><span class="sxs-lookup"><span data-stu-id="8c017-120">Public.</span></span> <span data-ttu-id="8c017-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8c017-121">Optional.</span></span> <span data-ttu-id="8c017-122">O padrão é &quot; geral &quot; .</span><span class="sxs-lookup"><span data-stu-id="8c017-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="8c017-123">Especifica o formato de exibição.</span><span class="sxs-lookup"><span data-stu-id="8c017-123">Specifies the display format.</span></span> <span data-ttu-id="8c017-124">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="8c017-124">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8c017-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8c017-125">Value</span></span></th>
<th><span data-ttu-id="8c017-126">Significado</span><span class="sxs-lookup"><span data-stu-id="8c017-126">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c017-127">Geral</span><span class="sxs-lookup"><span data-stu-id="8c017-127">General</span></span></td>
<td><span data-ttu-id="8c017-128">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8c017-128">Default.</span></span> <span data-ttu-id="8c017-129">Exibe o valor como um número não formatado.</span><span class="sxs-lookup"><span data-stu-id="8c017-129">Displays the value as an unformatted number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c017-130">Percentual</span><span class="sxs-lookup"><span data-stu-id="8c017-130">Percentage</span></span></td>
<td><span data-ttu-id="8c017-131">Formata o valor como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="8c017-131">Formats the value as a percentage.</span></span> <span data-ttu-id="8c017-132">Requer que a propriedade seja UInt32.</span><span class="sxs-lookup"><span data-stu-id="8c017-132">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c017-133">ByteS</span><span class="sxs-lookup"><span data-stu-id="8c017-133">ByteSize</span></span></td>
<td><span data-ttu-id="8c017-134">Formata o valor como um byte, &quot; KB &quot; , &quot; MB &quot; ou &quot; GB, &quot; conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="8c017-134">Formats the value as a byte, &quot;KB&quot;, &quot;MB&quot;, or &quot;GB&quot; as appropriate.</span></span> <span data-ttu-id="8c017-135">Requer que a propriedade seja UInt64.</span><span class="sxs-lookup"><span data-stu-id="8c017-135">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c017-136">KBSize</span><span class="sxs-lookup"><span data-stu-id="8c017-136">KBSize</span></span></td>
<td><span data-ttu-id="8c017-137">Formata o valor como um &quot; KB &quot; , não importa qual é o valor.</span><span class="sxs-lookup"><span data-stu-id="8c017-137">Formats the value as a &quot;KB&quot;, no matter what the value is.</span></span> <span data-ttu-id="8c017-138">Requer que a propriedade seja UInt64.</span><span class="sxs-lookup"><span data-stu-id="8c017-138">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c017-139">Amostras</span><span class="sxs-lookup"><span data-stu-id="8c017-139">SampleSize</span></span></td>
<td><span data-ttu-id="8c017-140">Formata o valor como um número de bits.</span><span class="sxs-lookup"><span data-stu-id="8c017-140">Formats the value as a number of bits.</span></span> <span data-ttu-id="8c017-141">Requer que a propriedade seja UInt32.</span><span class="sxs-lookup"><span data-stu-id="8c017-141">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c017-142">Taxa de bits</span><span class="sxs-lookup"><span data-stu-id="8c017-142">BitRate</span></span></td>
<td><span data-ttu-id="8c017-143">Formata o valor em &quot; kbps &quot; .</span><span class="sxs-lookup"><span data-stu-id="8c017-143">Formats the value in &quot;Kbps&quot;.</span></span> <span data-ttu-id="8c017-144">Requer que a propriedade seja UInt32.</span><span class="sxs-lookup"><span data-stu-id="8c017-144">Requires the property to be UInt32.</span></span> <span data-ttu-id="8c017-145">O valor deve ser armazenado em &quot; unidades de bits por segundo &quot; .</span><span class="sxs-lookup"><span data-stu-id="8c017-145">The value must be stored in &quot;bits-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c017-146">SampleRate</span><span class="sxs-lookup"><span data-stu-id="8c017-146">SampleRate</span></span></td>
<td><span data-ttu-id="8c017-147">Formata o valor em &quot; kHz &quot; .</span><span class="sxs-lookup"><span data-stu-id="8c017-147">Formats the value in &quot;KHz&quot;.</span></span> <span data-ttu-id="8c017-148">Requer que a propriedade seja UInt32.</span><span class="sxs-lookup"><span data-stu-id="8c017-148">Requires the property to be UInt32.</span></span> <span data-ttu-id="8c017-149">O valor deve ser armazenado em &quot; &quot; unidades hertz.</span><span class="sxs-lookup"><span data-stu-id="8c017-149">The value must be stored in &quot;Hertz&quot; units.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c017-150">FrameRate</span><span class="sxs-lookup"><span data-stu-id="8c017-150">FrameRate</span></span></td>
<td><span data-ttu-id="8c017-151">Formata o valor em quadros/segundo.</span><span class="sxs-lookup"><span data-stu-id="8c017-151">Formats the value in frames/second.</span></span> <span data-ttu-id="8c017-152">Requer que a propriedade seja UInt32.</span><span class="sxs-lookup"><span data-stu-id="8c017-152">Requires the property to be UInt32.</span></span> <span data-ttu-id="8c017-153">O valor deve ser armazenado em &quot; unidades de quilobytes de quadros por segundo &quot; .</span><span class="sxs-lookup"><span data-stu-id="8c017-153">The value must be stored in &quot;kilo-frames-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c017-154">Pixels</span><span class="sxs-lookup"><span data-stu-id="8c017-154">Pixels</span></span></td>
<td><span data-ttu-id="8c017-155">Formata o valor em unidades de pixel.</span><span class="sxs-lookup"><span data-stu-id="8c017-155">Formats the value in pixel units.</span></span> <span data-ttu-id="8c017-156">Requer que a propriedade seja UInt32.</span><span class="sxs-lookup"><span data-stu-id="8c017-156">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c017-157">EXIBI</span><span class="sxs-lookup"><span data-stu-id="8c017-157">DPI</span></span></td>
<td><span data-ttu-id="8c017-158">Formata o valor em pontos por polegada.</span><span class="sxs-lookup"><span data-stu-id="8c017-158">Formats the value in dots-per-inch.</span></span> <span data-ttu-id="8c017-159">Requer que a propriedade seja UInt32.</span><span class="sxs-lookup"><span data-stu-id="8c017-159">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c017-160">Duration</span><span class="sxs-lookup"><span data-stu-id="8c017-160">Duration</span></span></td>
<td><span data-ttu-id="8c017-161">Formata o valor como uma duração.</span><span class="sxs-lookup"><span data-stu-id="8c017-161">Formats the value as a duration.</span></span> <span data-ttu-id="8c017-162">Use <formatDurationAs> para especificar o formato de duração.</span><span class="sxs-lookup"><span data-stu-id="8c017-162">Use <formatDurationAs> to specify the duration format.</span></span> <span data-ttu-id="8c017-163">Requer que a propriedade seja UInt64.</span><span class="sxs-lookup"><span data-stu-id="8c017-163">Requires the property to be UInt64.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c017-164">formatDurationAs</span><span class="sxs-lookup"><span data-stu-id="8c017-164">formatDurationAs</span></span></td>
<td><span data-ttu-id="8c017-165">Público.</span><span class="sxs-lookup"><span data-stu-id="8c017-165">Public.</span></span> <span data-ttu-id="8c017-166">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8c017-166">Optional.</span></span> <span data-ttu-id="8c017-167">O padrão é &quot; hh: mm: SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="8c017-167">Default is &quot;hh:mm:ss&quot;.</span></span> <span data-ttu-id="8c017-168">Aplica-se somente se <em>formatas = &quot; duração &quot; </em>.</span><span class="sxs-lookup"><span data-stu-id="8c017-168">Only applies if <em>formatAs=&quot;Duration&quot;</em>.</span></span> <span data-ttu-id="8c017-169">Requer que a propriedade seja UInt64.</span><span class="sxs-lookup"><span data-stu-id="8c017-169">Requires the property to be UInt64.</span></span> <span data-ttu-id="8c017-170">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="8c017-170">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8c017-171">Valor</span><span class="sxs-lookup"><span data-stu-id="8c017-171">Value</span></span></th>
<th><span data-ttu-id="8c017-172">Significado</span><span class="sxs-lookup"><span data-stu-id="8c017-172">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c017-173">hh:mm</span><span class="sxs-lookup"><span data-stu-id="8c017-173">hh:mm</span></span></td>
<td><span data-ttu-id="8c017-174">Formata o valor em horas e minutos.</span><span class="sxs-lookup"><span data-stu-id="8c017-174">Formats the value in hours and minutes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c017-175">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="8c017-175">hh:mm:ss</span></span></td>
<td><span data-ttu-id="8c017-176">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8c017-176">Default.</span></span> <span data-ttu-id="8c017-177">Formata o valor em horas, minutos e segundos.</span><span class="sxs-lookup"><span data-stu-id="8c017-177">Formats the value in hours, minutes, and seconds.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c017-178">hh: mm: SS. FFF</span><span class="sxs-lookup"><span data-stu-id="8c017-178">hh:mm:ss.fff</span></span></td>
<td><span data-ttu-id="8c017-179">Formata o valor em horas, minutos, segundos e milissegundos.</span><span class="sxs-lookup"><span data-stu-id="8c017-179">Formats the value in hours, minutes, seconds, and milliseconds.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
