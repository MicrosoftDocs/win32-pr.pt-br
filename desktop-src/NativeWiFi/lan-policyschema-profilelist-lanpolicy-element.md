---
description: Contém uma lista de perfis a serem aplicados no nível de domínio ou computador.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Elemento ProfileList (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757109"
---
# <a name="profilelist-lanpolicy-element"></a>Elemento ProfileList (LANPolicy)

O elemento ProfileList (LANPolicy) contém uma lista de perfis a serem aplicados no nível do domínio ou da máquina. Os perfis devem ser baseados no [ \_ esquema de perfil de LAN](lan-profileschema-schema.md), com um elemento raiz de [**LANProfile**](lan-profileschema-lanprofile-element.md). Perfis com base em qualquer outro esquema serão ignorados.

Quando [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) é definido como false, esse elemento não deve estar presente em um perfil de política de LAN. Quando **enableAutoConfig** é definido como true, esse elemento é necessário.

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento **ProfileList** é definido pelo elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .

## <a name="remarks"></a>Comentários

Esse elemento deve conter exatamente um perfil de rede. Se mais de um perfil for especificado na política, somente a primeira rede será aplicada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




