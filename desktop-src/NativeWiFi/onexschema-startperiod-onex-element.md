---
description: Especifica o período de tempo, em segundos, para aguardar antes que um EAPOL-Start seja enviado.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: Elemento startPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2d21381939348ce8c37a9b23abb2283ab209e766bbce452c3802b8c5defe0872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800716"
---
# <a name="startperiod-onex-element"></a>Elemento startPeriod (OneX)

O elemento startPeriod (OneX) especifica o período de tempo, em segundos, para aguardar antes que um EAPOL-Start seja enviado. Uma EAPOL-Start é enviada para iniciar o processo de autenticação 802.1X.

Esse elemento é opcional. Quando startPeriod não é especificado em um perfil, um valor de 5 segundos é usado.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="startPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O **elemento startPeriod** é definido pelo [**elemento OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




