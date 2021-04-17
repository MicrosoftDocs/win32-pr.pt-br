---
description: Sem suporte no Windows 7 e posterior. Especifica o controle a ser usado no construtor de consultas.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759013"
---
# <a name="querycontrol"></a><span data-ttu-id="33e9e-104">queryControl</span><span class="sxs-lookup"><span data-stu-id="33e9e-104">queryControl</span></span>

<span data-ttu-id="33e9e-105">Sem suporte no Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="33e9e-105">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="33e9e-106">Especifica o controle a ser usado no construtor de consultas.</span><span class="sxs-lookup"><span data-stu-id="33e9e-106">Specifies what control to use in the query builder.</span></span> <span data-ttu-id="33e9e-107">Deve haver apenas um elemento [queryControl]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="33e9e-107">There should be only one [queryControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="33e9e-108">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="33e9e-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="33e9e-109">Se nenhum elemento [queryControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="33e9e-109">If no [queryControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e9e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="33e9e-110">Syntax</span></span>


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
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
```



## <a name="element-information"></a><span data-ttu-id="33e9e-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="33e9e-111">Element Information</span></span>



| <span data-ttu-id="33e9e-112">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="33e9e-112">Parent Element</span></span>                                   | <span data-ttu-id="33e9e-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="33e9e-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="33e9e-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="33e9e-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="33e9e-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="33e9e-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="33e9e-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="33e9e-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33e9e-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="33e9e-117">Attribute</span></span></th>
<th><span data-ttu-id="33e9e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="33e9e-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33e9e-119">controle</span><span class="sxs-lookup"><span data-stu-id="33e9e-119">control</span></span></td>
<td><span data-ttu-id="33e9e-120">Público.</span><span class="sxs-lookup"><span data-stu-id="33e9e-120">Public.</span></span> <span data-ttu-id="33e9e-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="33e9e-121">Optional.</span></span> <span data-ttu-id="33e9e-122">O padrão é &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="33e9e-122">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="33e9e-123">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="33e9e-123">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33e9e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="33e9e-124">Value</span></span></th>
<th><span data-ttu-id="33e9e-125">Significado</span><span class="sxs-lookup"><span data-stu-id="33e9e-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33e9e-126">Padrão</span><span class="sxs-lookup"><span data-stu-id="33e9e-126">Default</span></span></td>
<td><span data-ttu-id="33e9e-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="33e9e-127">Default.</span></span> <span data-ttu-id="33e9e-128">Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo.</span><span class="sxs-lookup"><span data-stu-id="33e9e-128">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="33e9e-129">Os tipos padrão são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="33e9e-129">The default types are listed below.</span></span> <span data-ttu-id="33e9e-130">Qualquer outro tipo resulta no uso do &quot; controle de texto &quot; .</span><span class="sxs-lookup"><span data-stu-id="33e9e-130">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="33e9e-131">ConditionType</span><span class="sxs-lookup"><span data-stu-id="33e9e-131">ConditionType</span></span></th>
<th><span data-ttu-id="33e9e-132">Control</span><span class="sxs-lookup"><span data-stu-id="33e9e-132">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33e9e-133">String</span><span class="sxs-lookup"><span data-stu-id="33e9e-133">String</span></span></td>
<td><span data-ttu-id="33e9e-134">Texto</span><span class="sxs-lookup"><span data-stu-id="33e9e-134">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33e9e-135">Cadeia de caracteres (valores múltiplos)</span><span class="sxs-lookup"><span data-stu-id="33e9e-135">String (multi-value)</span></span></td>
<td><span data-ttu-id="33e9e-136">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="33e9e-136">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33e9e-137">Número ou tamanho</span><span class="sxs-lookup"><span data-stu-id="33e9e-137">Number or Size</span></span></td>
<td><span data-ttu-id="33e9e-138">NumericText</span><span class="sxs-lookup"><span data-stu-id="33e9e-138">NumericText</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33e9e-139">Número ou tamanho (enum)</span><span class="sxs-lookup"><span data-stu-id="33e9e-139">Number or Size (enum)</span></span></td>
<td><span data-ttu-id="33e9e-140">Lista</span><span class="sxs-lookup"><span data-stu-id="33e9e-140">List</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33e9e-141">Datetime</span><span class="sxs-lookup"><span data-stu-id="33e9e-141">DateTime</span></span></td>
<td><span data-ttu-id="33e9e-142">Calendário</span><span class="sxs-lookup"><span data-stu-id="33e9e-142">Calendar</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33e9e-143">Booliano</span><span class="sxs-lookup"><span data-stu-id="33e9e-143">Boolean</span></span></td>
<td><span data-ttu-id="33e9e-144">Booliano</span><span class="sxs-lookup"><span data-stu-id="33e9e-144">Boolean</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33e9e-145">Booliano</span><span class="sxs-lookup"><span data-stu-id="33e9e-145">Boolean</span></span></td>
<td><span data-ttu-id="33e9e-146">Usa o controle booliano.</span><span class="sxs-lookup"><span data-stu-id="33e9e-146">Uses the boolean control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33e9e-147">Calendário</span><span class="sxs-lookup"><span data-stu-id="33e9e-147">Calendar</span></span></td>
<td><span data-ttu-id="33e9e-148">Usa o controle de calendário suspenso.</span><span class="sxs-lookup"><span data-stu-id="33e9e-148">Uses the dropdown calendar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33e9e-149">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="33e9e-149">CheckboxDropList</span></span></td>
<td><span data-ttu-id="33e9e-150">Usa o controle de lista com caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="33e9e-150">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33e9e-151">Lista suspensa</span><span class="sxs-lookup"><span data-stu-id="33e9e-151">DropList</span></span></td>
<td><span data-ttu-id="33e9e-152">Usa o controle lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="33e9e-152">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33e9e-153">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="33e9e-153">MultiValueText</span></span></td>
<td><span data-ttu-id="33e9e-154">Usa o controle de edição de texto de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="33e9e-154">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33e9e-155">NumericText</span><span class="sxs-lookup"><span data-stu-id="33e9e-155">NumericText</span></span></td>
<td><span data-ttu-id="33e9e-156">Usa o controle de edição de texto numérico.</span><span class="sxs-lookup"><span data-stu-id="33e9e-156">Uses the numeric text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33e9e-157">Classificação</span><span class="sxs-lookup"><span data-stu-id="33e9e-157">Rating</span></span></td>
<td><span data-ttu-id="33e9e-158">Usa o controle de classificação de 5 estrelas.</span><span class="sxs-lookup"><span data-stu-id="33e9e-158">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33e9e-159">Texto</span><span class="sxs-lookup"><span data-stu-id="33e9e-159">Text</span></span></td>
<td><span data-ttu-id="33e9e-160">Usa o controle de edição de texto.</span><span class="sxs-lookup"><span data-stu-id="33e9e-160">Uses the text edit control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
