---
description: Especifica o número máximo de EAPOL-Start mensagens enviadas.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Elemento maxStart (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779608"
---
# <a name="maxstart-onex-element"></a>Elemento maxStart (OneX)

O elemento maxStart (OneX) especifica o número máximo de EAPOL-Start mensagens enviadas. Depois que o número máximo de mensagens de EAPOL-Start tiver sido enviado, o cliente assumirá que não há um autenticador presente na rede.

Esse elemento é opcional. Quando maxStart não é especificado em um perfil, é usado um valor de 3 mensagens.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **maxStart** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 




