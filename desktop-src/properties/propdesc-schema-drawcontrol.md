---
description: Especifica o controle a ser usado ao exibir apenas a propriedade.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010792"
---
# <a name="drawcontrol"></a><span data-ttu-id="19ee1-103">drawControl</span><span class="sxs-lookup"><span data-stu-id="19ee1-103">drawControl</span></span>

<span data-ttu-id="19ee1-104">Especifica o controle a ser usado ao exibir apenas a propriedade.</span><span class="sxs-lookup"><span data-stu-id="19ee1-104">Specifies what control to use when simply displaying the property.</span></span> <span data-ttu-id="19ee1-105">Deve haver apenas um elemento [drawControl]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="19ee1-105">There should be only one [drawControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="19ee1-106">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="19ee1-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="19ee1-107">Se nenhum elemento [drawControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="19ee1-107">If no [drawControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="19ee1-108">Essa forma do controle não permite a edição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="19ee1-108">This form of the control does not allow for property editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ee1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ee1-109">Syntax</span></span>


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
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
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="19ee1-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="19ee1-110">Element Information</span></span>



| <span data-ttu-id="19ee1-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="19ee1-111">Parent Element</span></span>                                   | <span data-ttu-id="19ee1-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="19ee1-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="19ee1-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="19ee1-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="19ee1-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="19ee1-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="19ee1-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="19ee1-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19ee1-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="19ee1-116">Attribute</span></span></th>
<th><span data-ttu-id="19ee1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="19ee1-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19ee1-118">controle</span><span class="sxs-lookup"><span data-stu-id="19ee1-118">control</span></span></td>
<td><span data-ttu-id="19ee1-119">Público.</span><span class="sxs-lookup"><span data-stu-id="19ee1-119">Public.</span></span> <span data-ttu-id="19ee1-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19ee1-120">Optional.</span></span> <span data-ttu-id="19ee1-121">O padrão é &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="19ee1-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="19ee1-122">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="19ee1-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19ee1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="19ee1-123">Value</span></span></th>
<th><span data-ttu-id="19ee1-124">Significado</span><span class="sxs-lookup"><span data-stu-id="19ee1-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19ee1-125">Padrão</span><span class="sxs-lookup"><span data-stu-id="19ee1-125">Default</span></span></td>
<td><span data-ttu-id="19ee1-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="19ee1-126">Default.</span></span> <span data-ttu-id="19ee1-127">Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo.</span><span class="sxs-lookup"><span data-stu-id="19ee1-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="19ee1-128">O tipo padrão é &quot; cadeia de caracteres &quot; (valores múltiplos) e o controle padrão é &quot; MultiValueText &quot; .</span><span class="sxs-lookup"><span data-stu-id="19ee1-128">The default type is &quot;String&quot; (multi-value) and the default control is &quot;MultiValueText&quot;.</span></span> <span data-ttu-id="19ee1-129">Qualquer outro tipo resulta no uso do &quot; &quot; controle staticText.</span><span class="sxs-lookup"><span data-stu-id="19ee1-129">Any other type results in using the &quot;StaticText&quot; control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19ee1-130">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="19ee1-130">MultiLineText</span></span></td>
<td><span data-ttu-id="19ee1-131">Usa o controle de texto de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="19ee1-131">Uses the multi-line text control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19ee1-132">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="19ee1-132">MultiValueText</span></span></td>
<td><span data-ttu-id="19ee1-133">Usa o controle de texto de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="19ee1-133">Uses the multi-value text control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19ee1-134">PercentBar</span><span class="sxs-lookup"><span data-stu-id="19ee1-134">PercentBar</span></span></td>
<td><span data-ttu-id="19ee1-135">Usa o controle de barra de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="19ee1-135">Uses the percent bar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19ee1-136">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="19ee1-136">ProgressBar</span></span></td>
<td><span data-ttu-id="19ee1-137">Usa o controle da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="19ee1-137">Uses the progress bar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19ee1-138">Classificação</span><span class="sxs-lookup"><span data-stu-id="19ee1-138">Rating</span></span></td>
<td><span data-ttu-id="19ee1-139">Usa o controle de classificação de 5 estrelas.</span><span class="sxs-lookup"><span data-stu-id="19ee1-139">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19ee1-140">StaticText</span><span class="sxs-lookup"><span data-stu-id="19ee1-140">StaticText</span></span></td>
<td><span data-ttu-id="19ee1-141">Usa <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription:: FormatForDisplay</strong></a> para exibir o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="19ee1-141">Uses <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription::FormatForDisplay</strong></a> to display the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19ee1-142">Íconelist</span><span class="sxs-lookup"><span data-stu-id="19ee1-142">IconList</span></span></td>
<td><span data-ttu-id="19ee1-143"><strong>Windows 7 e posterior.</strong></span><span class="sxs-lookup"><span data-stu-id="19ee1-143"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="19ee1-144">Uma enumeração de ícones.</span><span class="sxs-lookup"><span data-stu-id="19ee1-144">An enumeration of icons.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19ee1-145">BooleanCheckMark</span><span class="sxs-lookup"><span data-stu-id="19ee1-145">BooleanCheckMark</span></span></td>
<td><span data-ttu-id="19ee1-146"><strong>Windows 7 e posterior.</strong></span><span class="sxs-lookup"><span data-stu-id="19ee1-146"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
