---
title: Elemento EapHostConfig
description: Contém o elemento EapMethod e o elemento config ou ConfigBlob. Os elementos config e ConfigBlob não podem ser usados simultaneamente.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Elemento EapHostConfig EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c34ddd1607a59c0425f7ec789bedb4981a05983ead276a14308fbf6aaadf26de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274860"
---
# <a name="eaphostconfig-element"></a>Elemento EapHostConfig

O elemento **EapHostConfig** contém o elemento [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) e o elemento [**config**](eaphostconfigschema-config-eaphostconfig-element.md) ou [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) .

Os elementos [**config**](eaphostconfigschema-config-eaphostconfig-element.md) e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) não podem ser usados simultaneamente.

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                    | Type                                                                                     | Descrição                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Configuração**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**BaseEapMethodConfig**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | É usado quando a configuração do método está no formato de texto XML em vez de em um BLOB binário.<br/>       |
| [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | É usado quando a configuração do método está em formato de BLOB binário em vez de formulário de texto de cadeia de caracteres.<br/> |
| [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                       | Identifica o método que está sendo referenciado. <br/>                                                 |



## <a name="remarks"></a>Comentários

O elemento **ProcessContents** permite aprimoramentos futuros no esquema. O elemento **ProcessContents** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





