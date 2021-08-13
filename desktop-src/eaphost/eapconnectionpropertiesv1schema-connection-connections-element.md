---
title: Elemento Connection (Connections)
description: Define cada definição de configuração e a associa a um nome. O elemento Connection é opcional.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Elemento Connection EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6948675f7910c46cb2b5db4285ce0df795fa057f275ce29b7f4c664b14c4ce1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498366"
---
# <a name="connection-connections-element"></a>Elemento Connection (Connections)

O elemento **Connection (Connections)** define cada definição de configuração e a associa a um nome. O elemento **Connection** é opcional.

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento **Connection** é definido pelo elemento [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                 | Digite   | Description                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Identifica o elemento de configuração EAP.<br/>                                                                    |
| [**Nome**](eapconnectionpropertiesv1schema-name-connection-element.md) | string | Captura o nome da conexão que está sendo definida, auxiliando na identificação de várias conexões. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**conexões**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**conexões**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





