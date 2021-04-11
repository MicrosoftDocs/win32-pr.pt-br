---
description: Especifica o tipo de criptografia de dados a ser usado para se conectar a uma LAN sem fio.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Elemento Encryption (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090661"
---
# <a name="encryption-authencryption-element"></a>Elemento Encryption (authEncryption)

O elemento Encryption (authEncryption) especifica o tipo de criptografia de dados a ser usado para se conectar a uma LAN sem fio.

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Comentários

Quando o elemento **Encryption** tem um valor de WEP, [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) deve ser definido como **networkKey**.

O método de criptografia AES é conforme especificado nas especificações [802.1 x](https://ieeexplore.ieee.org/document/1438730) e [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento de **criptografia** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**authEncryption (segurança)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




