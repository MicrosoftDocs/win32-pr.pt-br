---
description: Contém informações sobre o criador do perfil.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Elemento ProfileCreationType (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090581"
---
# <a name="profilecreationtype-mbnprofile-element"></a>Elemento ProfileCreationType (MBNProfile)

O elemento **ProfileCreationType (MBNProfile)** contém informações sobre o criador do perfil.

Esse elemento pode ter um dos valores a seguir.



| Valor                 | Significado                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "Userprovisionado"     | Esse perfil é criado por informações fornecidas pelo usuário do dispositivo.                                                     |
| "AdminProvisioned"    | Esse perfil é criado por administradores de ti e distribuído aos usuários.                                                     |
| "OperatorProvisioned" | Esse perfil é criado por um operador de rede e distribuído aos usuários.                                                    |
| "DeviceProvisioned"   | Esse perfil é criado pelo serviço de banda larga móvel usando as informações armazenadas no contexto provisionado do dispositivo. |



 

Esse é um elemento opcional.

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **ProfileCreationType** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




