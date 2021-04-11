---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296320"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span data-ttu-id="0fe9f-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span><span class="sxs-lookup"><span data-stu-id="0fe9f-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span></span>

<span data-ttu-id="0fe9f-104">O elemento **IsAdditionalPdpContextProfile** contém um **booliano** que será **verdadeiro** se este for um perfil adicional de "PDP (protocolo de dados de pacote)" e **false**, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-104">The **IsAdditionalPdpContextProfile** element contains a **boolean** that is **true** if this is an "additional PDP (Packet Data Protocol) context" profile and **false**, otherwise.</span></span> <span data-ttu-id="0fe9f-105">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-105">Default is **false**.</span></span>

<span data-ttu-id="0fe9f-106">Um perfil de "contexto PDP adicional" é um perfil que não é ativado pela porta padrão do adaptador físico e a definição desse elemento como true garante que esse perfil não seja exibido incorretamente na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-106">An "additional PDP context" profile is a profile that does not get activated over the physical adapter default port, and setting this element to true ensures that this profile is not displayed inappropriately in the user interface.</span></span>

<span data-ttu-id="0fe9f-107">Observe que, se esse elemento for definido como true, o seguinte também deverá ser verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-107">Note that if this element is set to true, then the following must also be true.</span></span>

-   <span data-ttu-id="0fe9f-108">O elemento [**IsDefault**](./schema-isdefault-mbnprofile-element.md) deve ser não especificado ou definido como **false** para que o perfil seja válido.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-108">The [**IsDefault**](./schema-isdefault-mbnprofile-element.md) element must be unspecified or set to **false** for the profile to be valid.</span></span>
-   <span data-ttu-id="0fe9f-109">O elemento [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) deve ser não especificado ou definido como **manual** para que o perfil seja válido.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-109">The [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element must be unspecified or set to **manual** for the profile to be valid.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="0fe9f-110">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="0fe9f-110">Element hierarchy</span></span>

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="0fe9f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fe9f-111">Syntax</span></span>

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="0fe9f-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="0fe9f-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="0fe9f-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="0fe9f-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="0fe9f-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-114">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="0fe9f-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0fe9f-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="0fe9f-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-116">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="0fe9f-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0fe9f-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="0fe9f-118">Esse elemento mais externo (documento) pode não estar contido em outros elementos.</span><span class="sxs-lookup"><span data-stu-id="0fe9f-118">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe9f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fe9f-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fe9f-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fe9f-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
