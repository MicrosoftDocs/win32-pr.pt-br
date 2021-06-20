---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade stringFormat como uma cadeia de caracteres.'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408349"
---
# <a name="stringformat"></a><span data-ttu-id="35c84-103">stringFormat</span><span class="sxs-lookup"><span data-stu-id="35c84-103">stringFormat</span></span>

<span data-ttu-id="35c84-104">Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="35c84-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="35c84-105">Isso é aplicável somente se <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="35c84-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="35c84-106">Deve haver apenas um elemento [StringFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="35c84-106">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="35c84-107">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="35c84-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="35c84-108">Se nenhum elemento [StringFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="35c84-108">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c84-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35c84-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="35c84-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="35c84-110">Element Information</span></span>



| <span data-ttu-id="35c84-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="35c84-111">Parent Element</span></span>                                   | <span data-ttu-id="35c84-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="35c84-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="35c84-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="35c84-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="35c84-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="35c84-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="35c84-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="35c84-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35c84-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="35c84-116">Attribute</span></span></th>
<th><span data-ttu-id="35c84-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="35c84-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35c84-118">formato de</span><span class="sxs-lookup"><span data-stu-id="35c84-118">formatAs</span></span></td>
<td><span data-ttu-id="35c84-119">Público.</span><span class="sxs-lookup"><span data-stu-id="35c84-119">Public.</span></span> <span data-ttu-id="35c84-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="35c84-120">Optional.</span></span> <span data-ttu-id="35c84-121">O padrão é &quot; geral &quot; .</span><span class="sxs-lookup"><span data-stu-id="35c84-121">Default is &quot;General&quot;.</span></span> <span data-ttu-id="35c84-122">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="35c84-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="35c84-123">Valor</span><span class="sxs-lookup"><span data-stu-id="35c84-123">Value</span></span></th>
<th><span data-ttu-id="35c84-124">Significado</span><span class="sxs-lookup"><span data-stu-id="35c84-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35c84-125">Geral</span><span class="sxs-lookup"><span data-stu-id="35c84-125">General</span></span></td>
<td><span data-ttu-id="35c84-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="35c84-126">Default.</span></span> <span data-ttu-id="35c84-127">Retorna o valor como uma cadeia de caracteres não formatada.</span><span class="sxs-lookup"><span data-stu-id="35c84-127">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35c84-128">FileName</span><span class="sxs-lookup"><span data-stu-id="35c84-128">FileName</span></span></td>
<td><span data-ttu-id="35c84-129">Formata o valor como um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="35c84-129">Formats the value as a file name.</span></span> <span data-ttu-id="35c84-130">Oculta a extensão de acordo com as configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="35c84-130">Hides the extension according to user settings.</span></span> <span data-ttu-id="35c84-131">Requer que o tipo de propriedade seja cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="35c84-131">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35c84-132">FilePath</span><span class="sxs-lookup"><span data-stu-id="35c84-132">FilePath</span></span></td>
<td><span data-ttu-id="35c84-133">Formata o valor como um caminho de arquivo.</span><span class="sxs-lookup"><span data-stu-id="35c84-133">Formats the value as a file path.</span></span> <span data-ttu-id="35c84-134">Oculta a extensão de acordo com as configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="35c84-134">Hides the extension according to user settings.</span></span> <span data-ttu-id="35c84-135">Requer que o tipo de propriedade seja cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="35c84-135">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35c84-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="35c84-136">Hyperlink</span></span></td>
<td><span data-ttu-id="35c84-137">Formata o valor como um hiperlink.</span><span class="sxs-lookup"><span data-stu-id="35c84-137">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
