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
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008790"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





