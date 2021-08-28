---
description: AutoConnectOnInternet
MS-HAID: WWAN\_profile\_v4.element\_AutoConnectOnInternet
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AutoConnectOnInternet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1e62713d664d821282fdcf13b016a574bda8ab
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880520"
---
# <a name="span-idwwan_profile_v4element_autoconnectoninternetspanautoconnectoninternet"></a><span id="WWAN_profile_v4.element_AutoConnectOnInternet"></span>AutoConnectOnInternet

Especifica se o dispositivo de Banda Larga Móvel se conectará automaticamente a uma rede.

Para obter mais informações, consulte a documentação do [**elemento AutoConnectOnInternet**](./schema-autoconnectoninternet-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Hierarquia de elementos

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;AutoConnectOnInternet&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<AutoConnectOnInternet>

  boolean

</AutoConnectOnInternet>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

Nenhum.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai


| Elemento pai | Description | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>O <strong>elemento MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior. Ele identifica um perfil de Banda Larga Móvel com um conjunto mais avançado de opções do que o elemento MBNProfile.</p><p>Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um conjunto específico de condições operacionais. Use o <a href="element-profileconditionedon.md"><strong>elemento filho ProfileConditionedOn</strong></a> <strong>de MBNProfileExt</strong> para especificar quais condições operacionais fazem de um perfil específico o perfil ativo.</p> | 


 

## <a name="requirements"></a>Requisitos


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
