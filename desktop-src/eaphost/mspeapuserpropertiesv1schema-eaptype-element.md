---
title: Elemento EapType (mspeapuserpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema baseeapuserpropertiesv1. Para o mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27923d77a36b917b3356b7c5c79d408bc0a99d49d70967677b56a9047ed0b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067176"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>Elemento EapType (mspeapuserpropertiesv1schema)

O elemento **EapType** é um tipo derivado do elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) do esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                               | Type                                                                                      | Descrição                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | O elemento [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) identifica o método interno e as credenciais a serem usadas com esse método. Quando a configuração de PEAP estiver configurada para acesso de convidado PEAP, esse elemento estará ausente.<br/>                                  |
| [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**PeapExtensionsType**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | O elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) permite aprimoramentos futuros no esquema. <br/> O elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) é opcional.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





