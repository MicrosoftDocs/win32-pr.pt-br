---
description: CellularClass
MS-HAID: WWAN\_profile\_v4.element\_CellularClass
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CellularClass
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c442208c40dcfa42a7c603bc20fda94422794ef
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988839"
---
# <a name="span-idwwan_profile_v4element_cellularclassspancellularclass"></a><span id="WWAN_profile_v4.element_CellularClass"></span>CellularClass

Especifica que esse perfil está ativo somente quando a classe de celular atual é a especificada. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto PDP (Protocolo de Dados de Pacote).

## <a name="element-hierarchy"></a>Hierarquia de elementos

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;ProfileConditionedOn&gt;](element-profileconditionedon.md)  
**&lt;CellularClass&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<CellularClass>

  "3GPP" | "3GPP2"

</CellularClass>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

Nenhum.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai


| Elemento pai | Descrição | 
|----------------|-------------|
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Especifica as condições que devem ser atendidas para que um perfil seja aplicável.</p><p>Esse elemento é novo para v4. Ele permite que você especifique vários perfis que se aplicam em condições diferentes e que o perfil adequado seja usado automaticamente quando aplicável. Esse elemento é opcional. Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.</p> | 


 

## <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



