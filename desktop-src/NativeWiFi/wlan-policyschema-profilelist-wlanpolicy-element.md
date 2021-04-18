---
description: Contém uma lista de perfis a serem aplicados no nível de domínio ou computador.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Elemento ProfileList (WLANPolicy)
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
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769427"
---
# <a name="profilelist-wlanpolicy-element"></a>Elemento ProfileList (WLANPolicy)

O elemento ProfileList (WLANPolicy) contém uma lista de perfis a serem aplicados no nível do domínio ou da máquina. Esse elemento é opcional. Se esse elemento estiver presente, ele deverá conter pelo menos um perfil.

Os perfis devem ser baseados no [ \_ esquema de perfil de WLAN](wlan-profileschema-schema.md), com um elemento raiz de [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).

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

O elemento **ProfileList** é definido pelo elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




