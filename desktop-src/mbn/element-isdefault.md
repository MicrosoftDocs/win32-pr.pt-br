---
description: IsDefault
MS-HAID: WWAN\_profile\_v4.element\_IsDefault
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsDefault
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 886dab9e4388b5935503d21729d65ccc748caba0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883626"
---
# <a name="span-idwwan_profile_v4element_isdefaultspanisdefault"></a><span id="WWAN_profile_v4.element_IsDefault"></span>IsDefault

Especifica se esse perfil é o perfil padrão.

Para obter mais detalhes sobre esse elemento, consulte a documentação v1 para [**IsDefault**](./schema-isdefault-mbnprofile-element.md).

## <a name="element-hierarchy"></a>Hierarquia de elementos

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;IsDefault&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<IsDefault>

  boolean

</IsDefault>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

Nenhum.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai


| Elemento pai | Description | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior. Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</p><p>Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais. Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</p> | 


 

## <a name="requirements"></a>Requisitos


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
