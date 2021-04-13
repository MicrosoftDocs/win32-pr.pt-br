---
description: MBNProfileExt \/ ... \/ IPType (v4)
MS-HAID: WWAN\_profile\_v4.element\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918355cdfc90863539da5f29aff542654a95f5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501847"
---
# <a name="span-idwwan_profile_v4element_iptypespanmbnprofileextiptype-v4"></a><span data-ttu-id="14ea1-103"><span id="WWAN_profile_v4.element_IPType"></span>MBNProfileExt \/ ... \/ IPType (v4)</span><span class="sxs-lookup"><span data-stu-id="14ea1-103"><span id="WWAN_profile_v4.element_IPType"></span>MBNProfileExt\/...\/IPType (v4)</span></span>

<span data-ttu-id="14ea1-104">Especifica o tipo de IP a ser usado nessa conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="14ea1-104">Specifies the IP type to be used on this data connection.</span></span>

<span data-ttu-id="14ea1-105">Esse elemento é novo no v4 do esquema.</span><span class="sxs-lookup"><span data-stu-id="14ea1-105">This element is new in v4 of the schema.</span></span> <span data-ttu-id="14ea1-106">O elemento pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="14ea1-106">The element can have one of the following values.</span></span>

| <span data-ttu-id="14ea1-107">Valor</span><span class="sxs-lookup"><span data-stu-id="14ea1-107">Value</span></span>   | <span data-ttu-id="14ea1-108">Significado</span><span class="sxs-lookup"><span data-stu-id="14ea1-108">Meaning</span></span>                                       |
|---------|-----------------------------------------------|
| <span data-ttu-id="14ea1-109">Padrão</span><span class="sxs-lookup"><span data-stu-id="14ea1-109">Default</span></span> | <span data-ttu-id="14ea1-110">O tipo de IP deve ser escolhido por camadas inferiores</span><span class="sxs-lookup"><span data-stu-id="14ea1-110">IP type is to be picked by lower layer(s)</span></span>     |
| <span data-ttu-id="14ea1-111">IPv4</span><span class="sxs-lookup"><span data-stu-id="14ea1-111">IPv4</span></span>    | <span data-ttu-id="14ea1-112">Usar IPv4</span><span class="sxs-lookup"><span data-stu-id="14ea1-112">Use IPv4</span></span>                                      |
| <span data-ttu-id="14ea1-113">IPv6</span><span class="sxs-lookup"><span data-stu-id="14ea1-113">IPv6</span></span>    | <span data-ttu-id="14ea1-114">Use IPv6</span><span class="sxs-lookup"><span data-stu-id="14ea1-114">Use IPv6</span></span>                                      |
| <span data-ttu-id="14ea1-115">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="14ea1-115">IPv4v6</span></span>  | <span data-ttu-id="14ea1-116">Use IPv4 e/ou IPv6, como disponível.</span><span class="sxs-lookup"><span data-stu-id="14ea1-116">Use IPv4 and/or IPv6, as available.</span></span>           |
| <span data-ttu-id="14ea1-117">XLAT</span><span class="sxs-lookup"><span data-stu-id="14ea1-117">XLAT</span></span>    | <span data-ttu-id="14ea1-118">Usar o 464XLAT para encapsular IPv4 em redes IPv6</span><span class="sxs-lookup"><span data-stu-id="14ea1-118">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="14ea1-119">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="14ea1-119">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a><span data-ttu-id="14ea1-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="14ea1-120">Syntax</span></span>

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="14ea1-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="14ea1-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="14ea1-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="14ea1-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="14ea1-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="14ea1-123">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="14ea1-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="14ea1-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="14ea1-125">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="14ea1-125">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="14ea1-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="14ea1-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14ea1-127">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="14ea1-127">Parent Element</span></span></th>
<th><span data-ttu-id="14ea1-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="14ea1-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="14ea1-129"><a href="element-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="14ea1-129"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="14ea1-130">Especifica os parâmetros necessários para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="14ea1-130">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="14ea1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14ea1-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14ea1-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="14ea1-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



