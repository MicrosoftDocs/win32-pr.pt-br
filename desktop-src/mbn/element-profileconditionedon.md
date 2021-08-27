---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44257377400ec8877b07b6aa29766552b72e28e6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882907"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn

Especifica as condições que devem ser atendidas para que um perfil seja aplicável.

Esse elemento é novo para v4. Ele permite que você especifique vários perfis que se aplicam em condições diferentes e que o perfil adequado seja usado automaticamente quando aplicável. Esse elemento é opcional. Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.

## <a name="element-hierarchy"></a>Hierarquia de elementos

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;ProfileConditionedOn&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a>Chave

`?`   opcional (zero ou um)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho


| Elemento filho | Description | 
|---------------|-------------|
| <a href="element-cellularclass.md">CellularClass</a> | <p>Especifica que esse perfil está ativo somente quando a classe de celular atual é a especificada. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto PDP (Protocolo de Dados de Pacote).</p> | 
| <a href="element-imsi.md">IMSI</a> | <p>Especifica que esse perfil está ativo somente quando o IMSI atual que está sendo usado no ICCID é o especificado. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto PDP (Protocolo de Dados de Pacote).</p> | 
| <a href="element-iwlanapplicability.md">IwlanApplicability</a> | <p>Especifica que esse perfil está ativo somente quando conectado a uma rede IWLAN. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto PDP (Protocolo de Dados de Pacote). O valor desse elemento deve ser um valor <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> válido.</p> | 
| <a href="element-ratapplicability.md">LICAAplicabilidade</a> | <p>Especifica que esse perfil está ativo somente quando o tipo DEM é o especificado. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto PDP (Protocolo de Dados de Pacote).</p> | 
| <a href="element-roamapplicability.md">RoamApplicability</a> | <p>Especifica que esse perfil está ativo somente quando a condição de roaming atual é a especificada. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto PDP (Protocolo de Dados de Pacote). O valor desse elemento deve ser um valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai


| Elemento pai | Description | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>O <strong>elemento MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior. Ele identifica um perfil de Banda Larga Móvel com um conjunto mais avançado de opções do que o elemento MBNProfile.</p><p>Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um conjunto específico de condições operacionais. Use o <a href="element-profileconditionedon.md"><strong>elemento filho ProfileConditionedOn</strong></a> <strong>de MBNProfileExt</strong> para especificar quais condições operacionais fazem de um perfil específico o perfil ativo.</p> | 


 

## <a name="requirements"></a>Requisitos


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



