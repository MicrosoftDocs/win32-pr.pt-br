---
description: Contém várias configurações de segurança usadas por fornecedores de hardware independentes.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Elemento security (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e4baeadc5e53dc53d0a526b62c4905da1a778a1015f58321ae8b96e4aa52dfcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912746"
---
# <a name="security-ihv-element"></a>Elemento security (IHV)

O elemento de segurança (IHV) contém várias configurações de segurança usadas por fornecedores de hardware independentes.

As configurações de segurança da Microsoft e as configurações de segurança de IHV são mutuamente exclusivas. Se ambos os conjuntos de configurações de segurança estão presentes no mesmo perfil, o perfil é inválido.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O **elemento** de segurança é definido pelo [**elemento IHV.**](wlan-profileschema-ihv-wlanprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Ihv**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




