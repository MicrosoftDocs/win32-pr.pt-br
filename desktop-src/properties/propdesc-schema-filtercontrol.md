---
description: Especifica o controle a ser usado no menu de filtro de cabeçalho.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756786"
---
# <a name="filtercontrol"></a><span data-ttu-id="0a4f1-103">filterControl</span><span class="sxs-lookup"><span data-stu-id="0a4f1-103">filterControl</span></span>

<span data-ttu-id="0a4f1-104">Especifica o controle a ser usado no menu de filtro de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-104">Specifies what control to use in the header filter menu.</span></span> <span data-ttu-id="0a4f1-105">Deve haver apenas um elemento [filterControl]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4f1-105">There should be only one [filterControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="0a4f1-106">Se houver vários elementos, o último será usado.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="0a4f1-107">Se nenhum elemento [filterControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-107">If no [filterControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4f1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a4f1-108">Syntax</span></span>


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
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
```



## <a name="element-information"></a><span data-ttu-id="0a4f1-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0a4f1-109">Element Information</span></span>



| <span data-ttu-id="0a4f1-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="0a4f1-110">Parent Element</span></span>                                   | <span data-ttu-id="0a4f1-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0a4f1-111">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="0a4f1-112">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0a4f1-112">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="0a4f1-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0a4f1-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0a4f1-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0a4f1-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a4f1-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="0a4f1-115">Attribute</span></span></th>
<th><span data-ttu-id="0a4f1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a4f1-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a4f1-117">controle</span><span class="sxs-lookup"><span data-stu-id="0a4f1-117">control</span></span></td>
<td><span data-ttu-id="0a4f1-118">Público.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-118">Public.</span></span> <span data-ttu-id="0a4f1-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-119">Optional.</span></span> <span data-ttu-id="0a4f1-120">O padrão é &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="0a4f1-120">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="0a4f1-121">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="0a4f1-121">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0a4f1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0a4f1-122">Value</span></span></th>
<th><span data-ttu-id="0a4f1-123">Significado</span><span class="sxs-lookup"><span data-stu-id="0a4f1-123">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a4f1-124">Padrão</span><span class="sxs-lookup"><span data-stu-id="0a4f1-124">Default</span></span></td>
<td><span data-ttu-id="0a4f1-125">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-125">Default.</span></span> <span data-ttu-id="0a4f1-126">Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-126">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="0a4f1-127">O tipo padrão é &quot; DateTime &quot; e o controle padrão é &quot; Calendar &quot; .</span><span class="sxs-lookup"><span data-stu-id="0a4f1-127">The default type is &quot;DateTime&quot; and the default control is &quot;Calendar&quot;.</span></span> <span data-ttu-id="0a4f1-128">Qualquer outro tipo resulta em nenhum controle de filtro especial.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-128">Any other type results in no special filter control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4f1-129">Calendário</span><span class="sxs-lookup"><span data-stu-id="0a4f1-129">Calendar</span></span></td>
<td><span data-ttu-id="0a4f1-130">Usa o controle Calendar.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-130">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4f1-131">Classificação</span><span class="sxs-lookup"><span data-stu-id="0a4f1-131">Rating</span></span></td>
<td><span data-ttu-id="0a4f1-132">Usa o controle de classificação de 5 estrelas.</span><span class="sxs-lookup"><span data-stu-id="0a4f1-132">Uses the 5-star rating control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
