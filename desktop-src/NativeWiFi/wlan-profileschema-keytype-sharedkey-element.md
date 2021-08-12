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
ms.openlocfilehash: 88c9a48d1c70cd156fa3d8f63bd3b70d69a99a1151a18c95ffd556b2503c9575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619279"
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
| Cliente mínimo com suporte<br/> | Windows Vista, somente Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                |
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

 

 




