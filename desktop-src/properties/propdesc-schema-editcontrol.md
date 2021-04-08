---
description: Especifica o controle a ser usado ao editar a propriedade.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921813"
---
# <a name="editcontrol"></a><span data-ttu-id="778b6-103">editControl</span><span class="sxs-lookup"><span data-stu-id="778b6-103">editControl</span></span>

<span data-ttu-id="778b6-104">Especifica o controle a ser usado ao editar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="778b6-104">Specifies what control to use when editing the property.</span></span> <span data-ttu-id="778b6-105">Deve haver apenas um elemento [editControl]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="778b6-105">There should be only one [editControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="778b6-106">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="778b6-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="778b6-107">Se nenhum elemento [editControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="778b6-107">If no [editControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="778b6-108">Se <typeInfo isInnate="true"> , esse elemento será ignorado porque uma propriedade inato não pode ser editada.</span><span class="sxs-lookup"><span data-stu-id="778b6-108">If <typeInfo isInnate="true">, this element is ignored because an innate property cannot be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="778b6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="778b6-109">Syntax</span></span>


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
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
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="778b6-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="778b6-110">Element Information</span></span>



| <span data-ttu-id="778b6-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="778b6-111">Parent Element</span></span>                                   | <span data-ttu-id="778b6-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="778b6-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="778b6-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="778b6-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="778b6-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="778b6-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="778b6-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="778b6-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="778b6-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="778b6-116">Attribute</span></span></th>
<th><span data-ttu-id="778b6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="778b6-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="778b6-118">controle</span><span class="sxs-lookup"><span data-stu-id="778b6-118">control</span></span></td>
<td><span data-ttu-id="778b6-119">Público.</span><span class="sxs-lookup"><span data-stu-id="778b6-119">Public.</span></span> <span data-ttu-id="778b6-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="778b6-120">Optional.</span></span> <span data-ttu-id="778b6-121">O padrão é &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="778b6-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="778b6-122">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="778b6-122">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="778b6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="778b6-123">Value</span></span></th>
<th><span data-ttu-id="778b6-124">Significado</span><span class="sxs-lookup"><span data-stu-id="778b6-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="778b6-125">Padrão</span><span class="sxs-lookup"><span data-stu-id="778b6-125">Default</span></span></td>
<td><span data-ttu-id="778b6-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="778b6-126">Default.</span></span> <span data-ttu-id="778b6-127">Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo.</span><span class="sxs-lookup"><span data-stu-id="778b6-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="778b6-128">Os tipos padrão são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="778b6-128">The default types are listed below.</span></span> <span data-ttu-id="778b6-129">Qualquer outro tipo resulta no uso do &quot; controle de texto &quot; .</span><span class="sxs-lookup"><span data-stu-id="778b6-129">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="778b6-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="778b6-130">Type</span></span></th>
<th><span data-ttu-id="778b6-131">Control</span><span class="sxs-lookup"><span data-stu-id="778b6-131">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="778b6-132">String</span><span class="sxs-lookup"><span data-stu-id="778b6-132">String</span></span></td>
<td><span data-ttu-id="778b6-133">Texto</span><span class="sxs-lookup"><span data-stu-id="778b6-133">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="778b6-134">Cadeia de caracteres (valores múltiplos)</span><span class="sxs-lookup"><span data-stu-id="778b6-134">String (multi-value)</span></span></td>
<td><span data-ttu-id="778b6-135">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="778b6-135">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="778b6-136">Datetime</span><span class="sxs-lookup"><span data-stu-id="778b6-136">DateTime</span></span></td>
<td><span data-ttu-id="778b6-137">Calendário</span><span class="sxs-lookup"><span data-stu-id="778b6-137">Calendar</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="778b6-138">Calendário</span><span class="sxs-lookup"><span data-stu-id="778b6-138">Calendar</span></span></td>
<td><span data-ttu-id="778b6-139">Usa o controle Calendar.</span><span class="sxs-lookup"><span data-stu-id="778b6-139">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="778b6-140">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="778b6-140">CheckboxDropList</span></span></td>
<td><span data-ttu-id="778b6-141">Usa o controle de lista com caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="778b6-141">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="778b6-142">Lista suspensa</span><span class="sxs-lookup"><span data-stu-id="778b6-142">DropList</span></span></td>
<td><span data-ttu-id="778b6-143">Usa o controle lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="778b6-143">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="778b6-144">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="778b6-144">MultiLineText</span></span></td>
<td><span data-ttu-id="778b6-145">Usa o controle de edição de texto de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="778b6-145">Uses the multi-line text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="778b6-146">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="778b6-146">MultiValueText</span></span></td>
<td><span data-ttu-id="778b6-147">Usa o controle de edição de texto de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="778b6-147">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="778b6-148">Classificação</span><span class="sxs-lookup"><span data-stu-id="778b6-148">Rating</span></span></td>
<td><span data-ttu-id="778b6-149">Usa o controle de classificação de 5 estrelas.</span><span class="sxs-lookup"><span data-stu-id="778b6-149">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="778b6-150">Texto</span><span class="sxs-lookup"><span data-stu-id="778b6-150">Text</span></span></td>
<td><span data-ttu-id="778b6-151">Usa o controle de edição de texto.</span><span class="sxs-lookup"><span data-stu-id="778b6-151">Uses the text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="778b6-152">Íconelist</span><span class="sxs-lookup"><span data-stu-id="778b6-152">IconList</span></span></td>
<td><span data-ttu-id="778b6-153"><strong>Windows 7 e posterior.</strong></span><span class="sxs-lookup"><span data-stu-id="778b6-153"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
