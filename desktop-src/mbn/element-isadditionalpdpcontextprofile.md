---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d4547bd97645ec5f3e378ac53df0f9e1ed78e7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988709"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile

O **elemento IsAdditionalPdpContextProfile** conterá  um **boolão** que será verdadeiro se este for um perfil de "contexto PDP (Protocolo de Dados de Pacote) adicional" e **false,** caso contrário. O padrão é **false**.

Um perfil de "contexto PDP adicional" é um perfil que não é ativado pela porta padrão do adaptador físico e definir esse elemento como true garante que esse perfil não seja exibido inadequadamente na interface do usuário.

Observe que, se esse elemento estiver definido como true, o seguinte também deverá ser true.

-   O [**elemento IsDefault**](./schema-isdefault-mbnprofile-element.md) deve ser não especificado ou definido como **false** para que o perfil seja válido.
-   O [**elemento ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) deve ser não especificado ou definido como **manual** para que o perfil seja válido.

## <a name="element-hierarchy"></a>Hierarquia de elementos

**&lt;IsAdditionalPdpContextProfile&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

Nenhum.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai

Esse elemento mais externo (documento) pode não estar contido por outros elementos.

## <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v3</p> | 


 

 
