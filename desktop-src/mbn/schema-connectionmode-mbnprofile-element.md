---
description: Especifica a configuração de conexão automática a ser usada para um dispositivo de banda larga móvel.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: Elemento ConnectionMode (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920890"
---
# <a name="connectionmode-mbnprofile-element"></a>Elemento ConnectionMode (MBNProfile)

O elemento **ConnectionMode (MBNProfile)** especifica a configuração de conexão automática a ser usada para um dispositivo de banda larga móvel.

Esse elemento pode ter um dos valores a seguir.



| Valor       | Significado                                                                |
|-------------|------------------------------------------------------------------------|
| manual    | Nunca conecte-se automaticamente à rede.                            |
| detectar      | Sempre conecte-se automaticamente à rede.                           |
| "auto-Home" | Conectar-se automaticamente à rede, exceto quando estiver em uma rede de roaming. |



 

Esse elemento pode ter um máximo de uma ocorrência.

Este é um elemento obrigatório.

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **ConnectionMode** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

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

 

 




