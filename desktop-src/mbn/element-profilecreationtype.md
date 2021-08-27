---
description: ProfileCreationType (em MBNProfileExt)
MS-HAID: WWAN\_profile\_v4.element\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (em MBNProfileExt)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29892e6a9dd0f32bb571103668d3a2d7dea32311
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473942"
---
# <a name="span-idwwan_profile_v4element_profilecreationtypespanprofilecreationtype-in-mbnprofileext"></a><span id="WWAN_profile_v4.element_ProfileCreationType"></span>ProfileCreationType (em MBNProfileExt)

Especifica o criador do perfil.

Para obter mais informações sobre esse elemento, consulte a documentação do elemento [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Hierarquia de elementos

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileCreationType>**

## <a name="syntax"></a>Sintaxe

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

Nenhum.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai


| Elemento pai | Descrição | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>O <strong>elemento MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior. Ele identifica um perfil de Banda Larga Móvel com um conjunto mais avançado de opções do que o elemento MBNProfile.</p><p>Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um conjunto específico de condições operacionais. Use o <a href="element-profileconditionedon.md"><strong>elemento filho ProfileConditionedOn</strong></a> <strong>de MBNProfileExt</strong> para especificar quais condições operacionais fazem de um perfil específico o perfil ativo.</p> | 


 

## <a name="related-elements"></a>Elementos relacionados

Os elementos a seguir têm o mesmo nome que este, mas conteúdo ou atributos diferentes:

-   **[ProfileCreationType (em ModemDMConfigProfile)](element-1-profilecreationtype.md)**

## <a name="requirements"></a>Requisitos


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
