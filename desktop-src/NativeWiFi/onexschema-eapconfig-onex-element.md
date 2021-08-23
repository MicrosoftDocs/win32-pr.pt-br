---
description: Especifica a configuração do EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Elemento EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 539f30d6730ec0735006f9dd3812322468ce71c7b0fbd90610b6cd589e0d60bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684876"
---
# <a name="eapconfig-onex-element"></a>Elemento EAPConfig (OneX)

O elemento **EAPConfig** (Onex) especifica a configuração do EAPHost.

Ao contrário da maioria dos elementos no esquema de perfil 802.1 X, esse elemento está no `https://www.microsoft.com/provisioning/EapHostConfig` namespace. Seus elementos filho são definidos no [esquema eaphostconfig](../eaphost/eaphostconfigschema-schema.md). O elemento [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) é um filho do elemento **EAPConfig** .

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento **EAPConfig** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, somente Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 
