---
title: Elemento User
description: Saiba mais sobre o elemento User. Esse elemento não é usado ao usar métodos herdado por meio das APIs EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Elemento de usuário EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0f21b22320029bf1d10a209eae6a3b2192512a541c1e681b71e112d488c87ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086400"
---
# <a name="user-element"></a>Elemento User

O **elemento** User não é usado ao usar métodos herdado por meio das APIs EAPHost.

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                  | Type | Descrição                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) |      | Captura o tipo de método e as informações de credencial específicas do método.<br/> |



## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





