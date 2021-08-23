---
description: Especifica, em segundos, o atraso máximo antes da tentativa de conexão de logon único falhar.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Elemento maxDelay (logon único)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cd4e82e8031f57e9672dd11a066a9a1fb2e8f3540c93dc4e1898afa4f1cf6302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684836"
---
# <a name="maxdelay-singlesignon-element"></a>Elemento maxDelay (logon único)

O elemento maxDelay (logon único) especifica, em segundos, o atraso máximo antes da tentativa de conexão de logon único falhar.

Esse elemento é opcional. Quando maxDelay não é especificado em um perfil, é usado um valor de 10 segundos.

**Windows xp com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **maxDelay** é definido pelo elemento [**logon único**](onexschema-singlesignon-onex-element.md) .

## <a name="remarks"></a>Comentários

Esse parâmetro pode ser definido na linha de comando usando o comando **netsh wlan set profileparameter** . Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Logon único**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Logon único (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
