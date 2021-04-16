---
description: Indica se a chave compartilhada será uma chave de rede ou uma frase secreta.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: Elemento KeyType (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789631"
---
# <a name="keytype-sharedkey-element"></a>Elemento KeyType (sharedKey)

O elemento KeyType (sharedKey) indica se a chave compartilhada será uma chave de rede ou uma frase secreta.

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Comentários

Quando o elemento [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) tem um valor de WEP, **KeyType** deve ser definido como **networkKey**.

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **KeyType** , consulte exemplo de [perfil sem difusão](non-broadcast-profile-sample.md), [exemplo de perfil WPA-Pessoal](wpa-personal-profile-sample.md)e [exemplo de perfil WPA2-Pessoal](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**sharedKey (segurança)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




