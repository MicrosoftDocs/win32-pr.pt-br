---
description: Especifica como os rótulos da propriedade são exibidos.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750881"
---
# <a name="labelinfo"></a><span data-ttu-id="2edae-103">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2edae-103">labelInfo</span></span>

<span data-ttu-id="2edae-104">Especifica como os rótulos da propriedade são exibidos.</span><span class="sxs-lookup"><span data-stu-id="2edae-104">Specifies how the property's labels are displayed.</span></span> <span data-ttu-id="2edae-105">Deve haver apenas um elemento [labelInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="2edae-105">There should be only one [labelInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

<span data-ttu-id="2edae-106">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="2edae-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="2edae-107">Se nenhum elemento [labelInfo]() for fornecido, o rótulo da propriedade não será exibido; no entanto, isso normalmente seria um defeito.</span><span class="sxs-lookup"><span data-stu-id="2edae-107">If no [labelInfo]() element is provided, then the property's label is not displayed; however, this would typically be a defect.</span></span>

## <a name="syntax"></a><span data-ttu-id="2edae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2edae-108">Syntax</span></span>


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="2edae-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2edae-109">Element Information</span></span>



| <span data-ttu-id="2edae-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="2edae-110">Parent Element</span></span>                                                   | <span data-ttu-id="2edae-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2edae-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="2edae-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2edae-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="2edae-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2edae-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="2edae-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2edae-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2edae-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="2edae-115">Attribute</span></span></th>
<th><span data-ttu-id="2edae-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2edae-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2edae-117">label</span><span class="sxs-lookup"><span data-stu-id="2edae-117">label</span></span></td>
<td><span data-ttu-id="2edae-118">Público.</span><span class="sxs-lookup"><span data-stu-id="2edae-118">Public.</span></span> <span data-ttu-id="2edae-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2edae-119">Optional.</span></span> <span data-ttu-id="2edae-120">O rótulo como é exibido na interface do usuário (por exemplo, o rótulo de coluna de detalhes ou o painel de visualização).</span><span class="sxs-lookup"><span data-stu-id="2edae-120">The label as it is displayed in the UI (for example, the details column label or preview pane).</span></span> <span data-ttu-id="2edae-121">A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta.</span><span class="sxs-lookup"><span data-stu-id="2edae-121">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="2edae-122">Use a cadeia de caracteres de exibição indireta porque ela pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="2edae-122">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="2edae-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription:: GetDisplayName</strong></a> retorna o nome de exibição resolvido.</span><span class="sxs-lookup"><span data-stu-id="2edae-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName</strong></a> returns the resolved display name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2edae-124">sortDescription</span><span class="sxs-lookup"><span data-stu-id="2edae-124">sortDescription</span></span></td>
<td><span data-ttu-id="2edae-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2edae-125">Optional.</span></span> <span data-ttu-id="2edae-126">Especifica as cadeias de caracteres oferecidas como opções de classificação.</span><span class="sxs-lookup"><span data-stu-id="2edae-126">Specifies the strings offered as sort options.</span></span> <span data-ttu-id="2edae-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription:: GetSortDescription</strong></a> retorna essa descrição de classificação.</span><span class="sxs-lookup"><span data-stu-id="2edae-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> returns this sort description.</span></span> <span data-ttu-id="2edae-128">Os valores a seguir fornecem as cadeias de caracteres da interface do usuário correspondentes.</span><span class="sxs-lookup"><span data-stu-id="2edae-128">The following values provide the corresponding UI strings.</span></span>
<ul>
<li><span data-ttu-id="2edae-129">Geral: &quot; classificação indo até a &quot;  /  &quot; classificação ficar inativa&quot;</span><span class="sxs-lookup"><span data-stu-id="2edae-129">General: &quot;Sort going up&quot; / &quot;Sort going down&quot;</span></span></li>
<li><span data-ttu-id="2edae-130">AToZ: &quot; A na parte superior &quot;  /  &quot; Z no início&quot;</span><span class="sxs-lookup"><span data-stu-id="2edae-130">AToZ: &quot;A on top&quot; / &quot;Z on top&quot;</span></span></li>
<li><span data-ttu-id="2edae-131">LowestHighest: &quot; mais baixo no topo superior &quot;  /  &quot; no início&quot;</span><span class="sxs-lookup"><span data-stu-id="2edae-131">LowestHighest: &quot;Lowest on top&quot; / &quot;Highest on top&quot;</span></span></li>
<li><span data-ttu-id="2edae-132">OldestNewest: mais &quot; antigo no início superior &quot;  /  &quot; na parte superior&quot;</span><span class="sxs-lookup"><span data-stu-id="2edae-132">OldestNewest: &quot;Oldest on top&quot; / &quot;Newest on top&quot;</span></span></li>
<li><span data-ttu-id="2edae-133">SmallestLargest: &quot; menor no &quot;  /  &quot; maior no início&quot;</span><span class="sxs-lookup"><span data-stu-id="2edae-133">SmallestLargest: &quot;Smallest on top&quot; / &quot;Largest on top&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2edae-134">invitationText</span><span class="sxs-lookup"><span data-stu-id="2edae-134">invitationText</span></span></td>
<td><span data-ttu-id="2edae-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2edae-135">Optional.</span></span> <span data-ttu-id="2edae-136">O texto da cadeia de caracteres de ajuda que é exibido como uma instrução para o usuário para o controle ou dica de ferramenta (por exemplo, &quot; Insira o nome do autor. &quot; ).</span><span class="sxs-lookup"><span data-stu-id="2edae-136">The Help string text that is displayed as an instruction to the user for the control or ToolTip (for instance, &quot;Enter author name.&quot;).</span></span> <span data-ttu-id="2edae-137">A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta.</span><span class="sxs-lookup"><span data-stu-id="2edae-137">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="2edae-138">Use a cadeia de caracteres de exibição indireta porque ela pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="2edae-138">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="2edae-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription:: GetEditInvitation</strong></a> retorna o texto de convite resolvido.</span><span class="sxs-lookup"><span data-stu-id="2edae-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation</strong></a> returns the resolved invitation text.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2edae-140">hideLabel</span><span class="sxs-lookup"><span data-stu-id="2edae-140">hideLabel</span></span></td>
<td><span data-ttu-id="2edae-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2edae-141">Optional.</span></span> <span data-ttu-id="2edae-142">O padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="2edae-142">The default is &quot;false&quot;.</span></span> <span data-ttu-id="2edae-143">Indica se o rótulo está oculto.</span><span class="sxs-lookup"><span data-stu-id="2edae-143">Indicates whether the label is hidden.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
