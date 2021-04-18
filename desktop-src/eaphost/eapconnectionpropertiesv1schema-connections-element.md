---
title: Elemento Connections
description: Saiba mais sobre o elemento Connections. Esse elemento coleta e contém zero ou mais elementos de conexão.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Elemento Connections EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105815533"
---
# <a name="connections-element"></a>Elemento Connections

O elemento **Connections** coleta e contém zero ou mais elementos [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) .

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                              | Type   | Descrição                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | Identifica o elemento de configuração EAP.<br/>                                                                                                                                       |
| [**Conexão**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | Define cada definição de configuração e a associa a um nome. O elemento [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) é opcional.<br/> |
| [**Nome**](eapconnectionpropertiesv1schema-name-connection-element.md)              | string | Captura o nome da conexão que está sendo definida, auxiliando na identificação de várias conexões.<br/>                                                                     |



## <a name="remarks"></a>Comentários

O elemento **Connections** não é usado com métodos herdados por meio de APIs EAPHost.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





