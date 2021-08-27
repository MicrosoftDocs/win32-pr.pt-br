---
description: PurposeGroupGuid
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroupGuid
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroupGuid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a704d035371d6d7febc2f2d86e4d67736ab02ad2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985408"
---
# <a name="span-idwwan_profile_v4element_purposegroupguidspanpurposegroupguid"></a><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>PurposeGroupGuid

Representa um perfil em um dos perfis.

Os perfis são especificados pelo valor de [**guidtype**](simpletype-guidtype.md) .

Quatro valores GUID são definidos, conforme listado na tabela a seguir.

| Grupo de finalidade | GUID                                 |
|---------------|--------------------------------------|
| Internet      | 3E5545D2-1137-4DC8-A198-33F1C657515F |
| mms           | 53E2C5D3-D13C-4068-AA38-9C48FF2E55A8 |
| IMS           | 474D66ED-0E4B-476B-A455-19BB1239ED13 |
| SUPL          | 6D42669F-52A9-408E-9493-1071DCC437BD |

 

## <a name="element-hierarchy"></a>Hierarquia de elementos

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;PurposeGroups&gt;](element-purposegroups.md)  
**&lt;PurposeGroupGuid&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<PurposeGroupGuid>

  guidType

</PurposeGroupGuid>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

Nenhum.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai


| Elemento pai | Descrição | 
|----------------|-------------|
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>Uma lista opcional de grupos de perfis, onde cada grupo inclui perfis usados para uma finalidade comum.</p><p>Este elemento é novo para v4 do esquema.</p><p>Um perfil pode ser listado em vários grupos.</p> | 


 

## <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



